# 分支说明
原项目：[DelightRun/PyBaiduYuyin](https://github.com/DelightRun/PyBaiduYuyin)，原项目的项目打包有问题，以至于使用pip安装后，无法使用，我提交了Pull requests ，作者可能没看到，于是我这边先发布一个能正常使用的安装包

使用说明: `pip install BaiduYuyin`,其他与原项目无异，注意包名不同就行

BaiduYuyin
============

This project is a wrapper for [Baidu Yuyin(voice) API](http://yuyin.baidu.com/)

This project is modified from [SpeechRecognition](https://github.com/Uberi/speech_recognition), which is published under the 3-clause BSD license.

Requirement
===========

+ [PyAudio](https://people.csail.mit.edu/hubert/pyaudio/) - require manual installation

Install
=======

    $ pip install BaiduYuyin

Usage
=====

> Note: I'm still working on this part, contributions are welcomed.

### TTS (Text-To-Speech)

Details can be found in source code.

Example: 

    import BaiduYuyin as pby
    tts = pby.TTS(app_key=YOUR_APP_KEY, secret_key=YOUR_SECRET_KEY)
    tts.say("你好")

### microphone recognition
```python
import BaiduYuyin as pby
r = pby.Recognizer()
with pby.Microphone() as source:
    print("Say something!")
    audio = r.listen(source)

print(r.recognize(audio))
```

### Recognition

The usage of Recognition module is same as [SpeechRecognition](https://github.com/Uberi/speech_recognition), except using `Baidu App Key` and `Baidu Secret Key` instead of `Google App Key`.

Please see [SpeechRecognition's README](https://github.com/Uberi/speech_recognition/blob/master/README.rst) for details.

LICENSE
=======
Copyright (c) 2015-2016 [Changxu Wang](changxu.wang)

The source code is available online at GitHub.

This program is made available under **MIT License**, see `LICENSE.txt` for details.
