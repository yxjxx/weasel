小狼毫配置文件
=================


##说明：
这份配置文件是我自己的在Windows下weasle的配置文件。  
因为我本身在Linux下用的也是Rime,不过升级到Mint16之后出现各种问题,而且ibus也没有fcitx好用,现在改用fcitx-sunpingyin和fcitx-sougoupinyin了(fcitx-rime在Mint16下不能输入中文,不知道是什么原因).而且我惊喜的发现在ibus-rime下要修改配置文件才能实现的大部分功能,fcitx可以在图形界面配置了.

-------------------------------
  
**配置完成之后你将可以实现:**

1. `<Ctrl>`键切换中英文(默认是`<Shift>`)
2. 模糊音
3. `[` 和 `]`翻页;`,`和`.`;`Tab`和`shift+Tab`也可以用来翻页
4. 中文状态下也可以使用英文标点(即半角)。并且可以方便的来回切换。
5. 词库

---------------------------------------------

**你需要做的工作：**

1. 安装[小狼毫](https://code.google.com/p/rimeime/wiki/Downloads)
2. 以zip包的形式下载[我的所有配置文件](https://github.com/yxjxx/weasel)
3. 将其中所有`.yaml`文件,拷贝到Rime文件夹下(默认路径为:`C:\Users\your_username\AppData\Roaming\Rime` **Notice:replace your_username with your real username**)
5. 重新部署(默认路径为:`C:\Users\username\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\小狼毫輸入法\【小狼毫】重新部署`),如你所见,你也可以在开始菜单中找到这一项　　
6. 切换到小狼毫输入法,按`F4`(或`<Ctrl>+~`)切换到`明月拼音-简化字`
7. 现在已经默认中文状态下使用英文标点了,切换回全角方式是按`F4`,选择`半角->全角`
8. 自定义快捷短语
9. ok,enjoy it!

-----------------------------------------

**下面是一些说明,感兴趣可以看一下**

1. default.custom.yaml（这个文件的作用是全局的）  作用是:修改中西文切换键shift->Ctrl.,文件中注释具体说明了左右键,以及不同值的意义

2. luna_pinyin_simp.custom.yaml  作用是:实现`明月拼音-简化字`的模糊音,文件中的注释具体说明了,实现了那些模糊,你也可以通过自己总结语法,自定义一些模糊

3. alternative.yaml按照luna_pinyin_simp.custom.yaml里面注释的说法,取消注释掉patch下面的两行就好作用是: 实现中文状态下也使用英文标点以及`'[' 和 ']'`翻页,alternaive.yaml中的注释里有详细的说明
    
4. 下载weasel.custom.yaml,这里是专用于小狼毫的一些配置文件.
    
5. 词库luna_pinyin.dict.yaml
参考网址：　https://code.google.com/p/rime-aca/downloads/detail?name=luna_pinyin.dict.yaml 將該文件複製到用戶文件夾中（Windows：%AppData%\Rime，Mac：~/Library/Rime，Linux：~/.config/ibus/rime/）。
重新部署,测试:  
![weasle](http://ww4.sinaimg.cn/large/81d2b157jw1e7zjmlpjt5j208605pmx9.jpg "")

6. 自定义快捷短语.
![自定义](http://ww1.sinaimg.cn/large/81d2b157jw1eegnzlfgmqj20e7068aan.jpg "")
7. 自定义翻页键.  
![翻页](http://ww1.sinaimg.cn/large/81d2b157jw1eego55or8uj20le094mzb.jpg "")
8. 关于小狼毫的一大软肋就是词库,而增大词库的最好办法还是靠自己长期的积累效果最好了,现在就加入dropbox同步用户词库  
参考网址:  
https://code.google.com/p/rimeime/wiki/UserGuide#%E5%90%8C%E6%AD%A5%E7%94%A8%E6%88%B6%E8%B3%87%E6%96%99  
https://gist.github.com/lotem/4483504  
修改installation.yaml如下:

```
distribution_code_name: Weasel
distribution_name: "小狼毫"
distribution_version: 0.9.26.1
install_time: "Sun Oct 13 15:44:09 2013"
installation_id: "yxjxx-win7" #主要是这两行 同步目录的名字,默认是一个id
rime_version: 1.0
sync_dir: 'C:\Dropbox\RimeSync'#主要是这两行 同步目录
```
然后在图形界面点击`用户资料同步`即可(Linux 用`rime_dict_manager -s`同步)    

9.Linux 下重新部署的命令`$rm ~/.config/ibus/rime/default.yaml; ibus-daemon –drx`  
如果出现:`current session already has an ibus-daemon.`
右键点击面板上的Rime图标restart即可