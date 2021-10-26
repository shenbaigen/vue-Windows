 node  vue  Windows环境基本配置 

一、安装node.js

官网：https://nodejs.org/en/download/
1.第一步检测一下电脑是否安装node.js

(1).开始-搜索cmd-回车，在命令行输入node -v，回车，如果出现“'node' 不是内部或外部命令，也不是可运行的程序...”时说明没有安装node.js;

(2).https://nodejs.org/en/  下载并安装node.js（选择LTS格式），下载好后双击开始安装，点击Next：

(3).勾选“I accept the terms in the License Agreement”同意许可协议，并单击Next下一步，出现如下界面：

(4).Node.js默认安装路径为“C:\nodejs\”，可以修改其他盘（我选择的是安装在D盘），单击Next，出现安装模式及模块选择界面：

(5).接着点击Next:

(6).确认无误后，点击Install，开始安装：

(7).耐心等待一会，安装完成，点击Finish即可：

(8).打开cmd（Windows+R），检测node是否安装成功：

我希望将全模块所在路径和缓存路径放在我node.js安装的文件夹中
1.在C:\nodejs 目录下新建文件夹  node_global    node_cache

2.运行命令
npm config set prefix "C:\nodejs\node_global"
npm config set cache "C:\nodejs\node_cache"

3.接下来设置环境变量，关闭cmd窗口，“我的电脑”-右键-“属性”-“高级系统设置”-“高级”-“环境变量”

进入环境变量对话框
在【系统变量】下新建【NODE_PATH】，输入【C:\nodejs\node_global\node_modules】
将【用户变量】下的【Path】修改为【C:\nodejs\node_global】

配置完后，安装个module测试下，我们就安装最常用的express模块，打开cmd窗口，
输入如下命令进行模块的全局安装
npm install express -g     # -g是全局安装的意思



二、安装VUE配置
在国内使用npm是非常慢的，所以我推荐使用淘宝npm镜像，使用淘宝的cnpm命令管理工具可以代替默认的npm管理工具，安装cnpm需要npm,打开终端窗口，输入

npm install -g cnpm -registry=https://registry.npm.taobao.org

1.安装全局webpack

在命令行里输入：cnpm install webpack -g （C盘）进行全局安装：

2.安装vue-cli脚手架工具

在命令行里输入：cnpm install -g vue-cli  （C盘）进行全局安装:

3.创建项目

关闭命令行，任意选择一个盘（这里，我选择D盘，新建一个名为mypro的文件夹），把mypro文件夹放进HBuilder，进入D盘mypro文件夹，右键选择在此处打开命令窗口，输入 
vue init webpack vuetest


4.进入项目文件夹：cd vuetest


5.安装完成后输入：npm run dev  运行测试

6.vue 打包命令 npm run build



