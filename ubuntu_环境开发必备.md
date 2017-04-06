# Ubuntu 环境开发必备

## sublime3
官网地址：<http://www.sublimetext.com/>，下载安装即可。

### 我的习惯配置

	{
	  "draw_white_space": "all",
      "font_size": 14,
	  "highlight_line": true,
	  "ignored_packages": [
		"Vintage"
	  ],
	  "line_padding_bottom": 2,
	  "line_padding_top": 2,
	  "tab_size": 2,
	  "translate_tabs_to_spaces": true,
	  "trim_trailing_white_space_on_save": true,
	  "word_wrap": "false"
	}


### 添加Package Controll
地址：<https://packagecontrol.io/installation>

### 添加其他插件
Alignment

Codecs33      # 解决无法显示GB2312编码的问题

ConvertToUTF8 # 解决无法显示GB2312编码的问题

HTMLBeautify

Pretty JSON

SCSS

等等

## RVM
官网地址：<http://rvm.io/>

安装方法见上面的网页，网页中还有rvm的使用（如：升级等），安装ruby、gemset等的方法。

升级：

	rvm get stable

添加以下代码到.bashrc或.zshrc中，rvm命令才能再shell中正常使用：

	export PATH="$PATH:$HOME/.rvm/bin" # Add RVM to PATH for scripting


## Ruby

	rvm install ruby [version_no]

### Oh My Zsh

官网：<http://ohmyz.sh/>

安装oh my zsh：

	sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

使用zsh作为默认shell：

	chsh -s $(which zsh)

oh my zsh 帮助文档：<https://github.com/robbyrussell/oh-my-zsh/wiki>	
我的[惯用主题](./yanghui.zsh-theme)

## JAVA

1. 搜索jdk下载合适的jdk，如：jdk1.8.0_101
2. 解压缩到某个目录，如：/usr/local
3. 配置系统环境变量，编辑/etc/profile文件，在文件末尾添加以下信息

  ```
    export JAVA_HOME=/usr/jdk1.8.0_101
	export JRE_HOME=$JAVA_HOME/jre
	export CLASSPATH=.:$CLASSPATH:$JAVA_HOME/lib:$JRE_HOME/lib
	export PATH=$PATH:$JAVA_HOME/bin:$JRE_HOME/bin
  ```

4. 使用source /etc/profile命令使刚才配置的信息生效
5. 使用java -version命令进行验证
6. java开发工具推荐idea

# WPS
官网地址：<http://linux.wps.cn/>

下载安装即可，打开后会提示缺少某些字体，需下载字体安装，或者点击不再提示即可（如果不需要这些字体的话）。

本git库提供了[]这些字体](./WPS缺失字体.tar.gz)，下载后解压缩，按照其中的说明安装字体即可。

## 搜狗输入法

官网地址：<http://pinyin.sogou.com/linux/>

根据系统位数，选择32位或者64位版本下载，双击安装，安装完成后重启电脑即可。

### Google Chrome

官网：<http://www.google.cn/chrome/browser/desktop/index.html>，下载安装即可。
