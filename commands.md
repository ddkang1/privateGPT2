```shell

conda create -n LLM2 python=3.10
conda activate LLM2

pip install -r requirements.txt

```

```shell
#llama.cpp

conda install -c conda-forge gcc=9 gxx_linux-64=9 libgcc-ng

cd ~/Projects/llama.cpp
export PATH=~/miniconda3/envs/LLM2/bin:$PATH
#make LLAMA_CUBLAS=1
rm -rf build/
mkdir build
cd build
cmake .. -DLLAMA_CUBLAS=ON
cmake --build . --config Release

pip install llama-cpp-python

```

```shell
cd ~/Projects/privateGPT2

python ingest.py

python privateGPT.py

What the president said about taxes ?

```