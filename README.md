# Keras-TensorFlow-GPU-Windows-Installation
Steps on the installation of TensorFlow-GPU and Keras in Windows

### Step 1: Install Anaconda (Python 3.6.5 version) <a href="https://www.continuum.io/downloads" target="_blank">Download</a>
<p align="center"><img width=70% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/anaconda_windows_installation.png"></p>

### Step 2: Update Anaconda
Open Anaconda Prompt to type the following command(s)
```Command Prompt
conda update conda
conda update --all
```

### Step 3: Install CUDA Tookit 9.0 <a href="https://developer.nvidia.com/cuda-downloads" target="_blank">Download</a>
Choose your version depending on your Operating System

```Tested version
cuda_9.0.176_win10.exe
```
Environmental variables
Ensure after installing CUDA toolkit, the CUDA_HOME is set in the environmental variables. 
If not then you need to add it manually..
```
CUDA_HOME=C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0
CUDA_PATH=C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0
CUDA_PATH_V9_0=C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0
```


### Step 4: Download cuDNN <a href="https://developer.nvidia.com/rdp/cudnn-download" target="_blank">Download</a>
Choose your version depending on your Operating System.
Membership registration is required.
```cudnn-9.0-windows10-x64-v7.1.zip```
Copy the following files into the CUDA Toolkit directory.
Copy <installpath>\cuda\bin\cudnn64_7.dll to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\bin.
Copy <installpath>\cuda\ include\cudnn.h to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\include.
Copy <installpath>\cuda\lib\x64\cudnn.lib to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\lib\x64.

### Step 5: Create an Anaconda environment with Python=3.6.5
Open Anaconda Prompt to type the following command(s)
```Command Prompt
conda create -n tensorflowgpu python=3.6.5 numpy scipy matplotlib spyder
```

### Step 6: Activate the environment
Open Anaconda Prompt to type the following command(s)
```Command Prompt
activate tensorflowgpu
```

### Step 7: Install Nightly build TensorFlow-GPU [1.8.0.dev20180329]
Open Anaconda Prompt to type the following command(s)
```Command Prompt
pip install tf-nightly-gpu==1.8.0.dev20180329
```

### Step 8: Install Keras
Open Anaconda Prompt to type the following command(s)
```Command Prompt
pip install keras
```

### Step 9: Testing
Let's try running <a href="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/examples/mnist_mlp.py">mnist_mlp.py</a> in your prompt.

Open Anaconda Prompt to type the following command(s)
```Command Prompt
activate tensorflow
python mnist_mlp.py
```
Congratulations ! You have successfully run Keras (with Tensorflow backend) over GPU on Windows !

<p align="left"><img width=100% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/installation_success.png"></p>
