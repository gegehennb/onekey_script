# onekey_script
一些方便使用的一件脚本备份

caddy+FileBrowser插件的安装

wget -N --no-check-certificate https://raw.githubusercontent.com/gegehennb/onekey_script/master/caddy_install.sh && chmod +x caddy_install.sh && bash caddy_install.sh install http.filemanager
 
如果你要同时安装多个 Caddy 插件，那么请修改下面的命令格式为：
bash caddy_install.sh install http.filemanager,http.xxx,http.xxx
英文半角逗号分隔多个插件名称
注意并不能单独安装一个扩展，所以如果你要新安装扩展，请执行上面的命令安装 Caddy 并加上你要安装的所有扩展的名称。


Aria2+WebUI 安装

1.安装Aria2
wget -N --no-check-certificate  https://raw.githubusercontent.com/gegehennb/onekey_script/master/aria2.sh && chmod +x aria2.sh && bash aria2.sh

2.安装Caddy+FileBrowser插件
wget -N --no-check-certificate https://raw.githubusercontent.com/gegehennb/onekey_script/master/caddy_install.sh && chmod +x caddy_install.sh && bash caddy_install.sh install http.filemanager

3.安装WebUI
mkdir /usr/local/caddy/www && mkdir /usr/local/caddy/www/aria2 && mkdir /usr/local/caddy/www/aria2/Download
cd /usr/local/caddy/www/aria2

先安装 unzip 依赖（解压ZIP）。
CentOS 系统：
yum install unzip -y

Debian/Ubuntu 系统：
apt-get install unzip -y

然后下载前端文件
wget -N --no-check-certificate https://github.com/ziahamza/webui-aria2/archive/master.zip
unzip master.zip  
mv webui-aria2-master/docs/* .
rm -rf webui-aria2-master/
rm -rf master.zip 

赋予文件夹权限
chmod -R 755 /usr/local/caddy/www/aria2





