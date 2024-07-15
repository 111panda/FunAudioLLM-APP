# funaudiollm-app repo

视频教程：[https://www.bilibili.com/video/BV1Fb421H7oK/](https://www.bilibili.com/video/BV1Fb421H7oK/)  

Welcome to the funaudiollm-app repository! This project hosts two exciting applications leveraging advanced audio understand and speech generation models to bring your audio experiences to life:

**Voice Chat** :  This application is designed to provide an interactive and natural chatting experience, making it easier to adopt sophisticated AI-driven dialogues in various settings.

**Voice Translation**: Break down language barriers with our real-time voice translation tool. This application seamlessly translates spoken language on the fly, allowing for effective and fluid communication between speakers of different languages.

For Details, visit [FunAudioLLM Homepage](https://fun-audio-llm.github.io/), [CosyVoice Paper](https://fun-audio-llm.github.io/pdf/CosyVoice_v1.pdf), [FunAudioLLM Technical Report](https://fun-audio-llm.github.io/pdf/FunAudioLLM.pdf)

For `CosyVoice`, visit [CosyVoice repo](https://github.com/FunAudioLLM/CosyVoice) and [CosyVoice space](https://www.modelscope.cn/studios/iic/CosyVoice-300M).

For `SenseVoice`, visit [SenseVoice repo](https://github.com/FunAudioLLM/SenseVoice) and [SenseVoice space](https://www.modelscope.cn/studios/iic/SenseVoice).

## Install

**Clone and install**

- Clone the repo
``` sh
git clone --recursive URL
# If you failed to clone submodule due to network failures, please run following command until success
cd funaudiollm-app
git submodule update --init --recursive
```

- prepare environments according to cosyvoice & sensevoice repo. then, execute the code below.
``` sh
pip install -r requirements.txt
```

### win

CosyVoice Windows部署得改源码，使用[https://github.com/v3ucn/CosyVoice_For_Windows](https://github.com/v3ucn/CosyVoice_For_Windows)  

## Basic Usage
**prepare**


dashscope api密钥：[https://dashscope.console.aliyun.com/apiKey](https://dashscope.console.aliyun.com/apiKey)  

modelscope SDK密钥：[https://modelscope.cn/my/myaccesstoken](https://modelscope.cn/my/myaccesstoken)  

不开ssl，默认注释了 [pem file](https://blog.csdn.net/liuchenbaidu/article/details/136722001)  

### Win

参考bat 运行

### Linux

**voice chat**

``` sh
sudo CUDA_VISIBLE_DEVICES="0" DS_API_TOKEN="YOUR-DS-API-TOKEN" python voice_chat.py >> ./log.txt
```
https://YOUR-IP-ADDRESS:60001/

**voice translation**

``` sh
sudo CUDA_VISIBLE_DEVICES="0" DS_API_TOKEN="YOUR-DS-API-TOKEN" python voice_translation.py >> ./log.txt
```
https://YOUR-IP-ADDRESS:60002/


