[toc]

# GymPlusPlus Project

## 1. Human Pose Detection
1.0 Install OpenVINO Python env following: https://pypi.org/project/openvino/ on Anaconda env and name it as "ov".

1.1 启动Anaconda Prompt，切换到'ov'这个环境
 $conda activate ov

1.2 Start Human Detection Task
 'D:\projects\gym_master>python gym_master.py'

1.3 修改摄像头输入或者视频文件输入，在gym_master.py的第217行修改代码：
```
USE_WEBCAM = False
cam_id = 0
video_file = "D:\\4DLogikerin\\2nd\\IMG_0815.MOV"
source = cam_id if USE_WEBCAM else video_file
```

## 2. Speech to Text: 语音转文字

2.0 Install Wisper.cpp from https://github.com/ggerganov/whisper.cpp and build it for Windows platform.

2.1 打开cmd，切换utf-8显示，输入
'chcp 65001'

2.2 在cmd切换到目录'D:\projects\whisper.cpp\build\bin\Release',然后执行以下命令行：
```
stream.exe -m ..\..\..\models\ggml-base.bin -l zh
```

## 3. LLM and RAG

3.0 Install Ipex-LLM for Intel iGPU following https://ipex-llm.readthedocs.io/en/latest/doc/LLM/Quickstart/chatchat_quickstart.html and https://github.com/intel-analytics/Langchain-Chatchat/blob/ipex-llm/INSTALL_win_mtl.md# 

3.1 启动Anaconda Prompt，切换到路径'D:\projects\Langchain-Chatchat',通过conda启动'ipex-llm-langchain-chatchat'这个环境, 然后设置环境变量，最后启动startup.py，通过浏览器登录打开webui使用RAG：

```
conda activate ipex-llm-langchain-chatchat

set SYCL_CACHE_PERSISTENT=1
set BIGDL_LLM_XMX_DISABLED=1

set BIGDL_IMPORT_IPEX=0
set no_proxy=localhost,127.0.0.1

python startup.py -a
```

## 4. Cloud Streaming

4.0 Install the Cloud Streaming from Intel open source project https://github.com/intel/cloud-streaming
4.1 Following https://github.com/intel/cloud-streaming/blob/main/doc/windows_setup.rst to install "Desktop Capture" on High End PC with Intel ARC GPU.
4.2 Following same link above to install the "Cloud Gaming Client" on Lenovo 联想小新 notebook.
4.3 在ARC GPU PC上启动环法自行车2023游戏。然后启动,"Desktop Capture" server application.
4.4 在联想小新上启动 “Cloud Gaming Client" to connect to the server to stream the game video.

## 5 环法自行车 2023 游戏

5.0 Go to https://store.steampowered.com/app/2062690/Tour_de_France_2023/. Install the game and play.


