小狼毫配置文件
=================


##说明：
这份配置文件是我自己的在Windows下 weasle的配置文件。  
因为我本身在Linux下用的也是Rime,本来是有维护ibus-rime的仓库来保存配置文件,不过本着windows下不折腾的原则，所以又新建了一个repo来管理小狼毫的配置文件

-------------------------------
  
**配置完成之后你将可以实现:**

1. `<Ctrl>`键(默认是`<Shift>`)切换中英文
2. 模糊音
3. ` '[' 和 ']' `翻页
4. 中文状态下也可以使用英文标点(即半角)。并且可以方便的来回切换。
5. 词库

---------------------------------------------

**你需要做的工作：**

1. 安装小狼毫
2. 以zip包的形式下载我的所有配置文件
3. 将其中所有`.yaml`文件,拷贝到Rime文件夹下(默认路径为:`C:\Users\username\AppData\Roaming\Rime`)
4. 词库luna_pinyin.dict.yaml 覆盖C:\Program Files (x86)\Rime\weasel-0.9.25\data下同名文件
4. 重新部署(默认路径为:`C:\Users\username\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\小狼毫輸入法\【小狼毫】重新部署`),如你所见,你也可以在开始菜单中找到这一项
5. 切换到小狼毫输入法,按`F4`(或`<Ctrl>+~`)切换到`明月拼音-简化字`或`明月拼音`
6. 现在已经默认中文状态下使用英文标点了,切换回全角方式是按`F4`,选择`半角->全角`
7. ok,enjoy it!

-----------------------------------------

**下面是一些说明,感兴趣可以看一下**

1. default.custom.yaml（这个文件的作用是全局的）  
    作用是:修改中西文切换键shift->Ctrl.,文件中注释具体说明了左右键,以及不同值的意义

2. luna_pinyin_simp.custom.yaml
    作用是:实现`明月拼音-简化字`的模糊音,文件中的注释具体说明了,实现了那些模糊,你也可以通过自己总结语法,自定义一些模糊

3. alternative.yaml按照luna_pinyin_simp.custom.yaml里面注释的说法,取消注释掉patch下面的两行就好
    作用是: 实现中文状态下也使用英文标点以及`'[' 和 ']'`翻页,alternaive.yaml中的注释你有详细的说明
    
4. 下载weasel.custom.yaml,这里是专用于小狼毫的一些配置文件.
    作用是:你自己看注释吧,懒得写了
    
5. 词库luna_pinyin.dict.yaml
覆盖C:\Program Files (x86)\Rime\weasel-0.9.25\data下同名文件  
重新部署,测试:  
![weasle](http://ww4.sinaimg.cn/large/81d2b157jw1e7zjmlpjt5j208605pmx9.jpg "")

---------------------------------------------------------

