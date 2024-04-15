[toc]

# GymPlusPlus Project

1. 火柴人
1.1 启动Anaconda Prompt，切换到'ov'这个环境
 $conda activate ov
1.2 启动火柴人
 'D:\projects\gym_master>python gym_master.py'
1.3 修改摄像头输入或者视频文件输入，在gym_master.py的第217行修改代码：
```
USE_WEBCAM = False
cam_id = 0
video_file = "D:\\4DLogikerin\\2nd\\IMG_0815.MOV"
source = cam_id if USE_WEBCAM else video_file
```

2. 语音转文字
2.1 打开cmd，切换utf-8显示，输入
'chcp 65001'
2.2 在cmd切换到目录'D:\projects\whisper.cpp\build\bin\Release',然后执行以下命令行：
```
stream.exe -m ..\..\..\models\ggml-base.bin -l zh
```

3. LLM and RAG
3.1 启动Anaconda Prompt，切换到路径'D:\projects\Langchain-Chatchat',通过conda启动'ipex-llm-langchain-chatchat'这个环境, 然后设置环境变量，最后启动startup.py，通过浏览器登录打开webui使用RAG：

```
conda activate ipex-llm-langchain-chatchat

set USE_XETLA=OFF
set SYCL_PI_LEVEL_ZERO_USE_IMMEDIATE_COMMANDLISTS=1
set SYCL_CACHE_PERSISTENT=1
set BIGDL_QUANTIZE_KV_CACHE=1
set BIGDL_LLM_XMX_DISABLED=1

set no_proxy=localhost,127.0.0.1
set BIGDL_IMPORT_IPEX=0

python startup.py -a
```


