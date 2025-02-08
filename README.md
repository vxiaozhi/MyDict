MyDict
---------------------------------------

一个用C语言实现的英汉对照词典。

功能：    
支持大小写混合输入。    
目前词库规模为45,093词。   
词库文件可以更换来生成新的词典。   
离线可用，简单实用。   
不用为了查个词再去动用google这种神器了，尤其看文档或者看源码时不知道某个词啥意思，只要之前用tmux给它分配一个很小的小窗口，随时可以切换过来查询。

实现：  
编码采用的是ASCII码集，数据结构采用Trie，内存占用73MB。以后想优化成三向单词查找树，以进一步减少内存使用。
具体可以看看注释。

运行：   
Linux环境下运行切换到源文件所在目录后运行make，然后执行./MyDict即可。

各文件说明：   
MyDict.c: 源码文件    
raw-dict: 用于生成词典的原始词库文件，编码格式为UTF8。   
makefile: makefile文件，切换到对应目录，直接运行make即可。   

注意：  
Windows下用于生成词典的原始词库文件需要是gbk编码，如果您是windows环境，要提前把raw-dict文件转码成为gbk格式，否则的话，虽然能成功建立词典，但是查询的时候看到的是乱码。

后续改进：     
改进数据结构以进一步节约内存，同时尽量感觉不到延迟。  
输入提示，即当使用者不太记得单词如何拼时输入几个字母后按两下tab键弹出所有前缀相同的单词。   
错误提示，如果输入单词不存在，输出正确的最长前缀单词。   
加上音标。
加上短语查询。   
最终目标是翻译！

## Repos for Learn English

- [有道词典的命令行版本](https://github.com/ChestnutHeng/Wudao-dict)
- [Go语言实现的简洁好用的命令行词典，跨平台、易于安装](https://github.com/Karmenzind/kd)
- [wordsea](https://github.com/vxiaozhi/wordsea)
- [英语四级词汇表+音频接口、含4000+单词，单词数据来源：有道词典](https://github.com/mihu915/cet4_dict)
- [英语四级词库](https://github.com/cuttlin/Vocabulary-of-CET-4)
- [英语四六级、考研、SAT单词，txt 文件, json 文件，CET4 CET6](https://github.com/KyleBing/english-vocabulary)
- [✨✨🎏一个网页鼠标点击特效，单击一下就会有随机的四级单词产生](https://github.com/flymysql/CET4-Mouse-click-effects)
