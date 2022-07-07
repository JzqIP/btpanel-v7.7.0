# btpanel-v7.7.0
btpanel-v7.7.0-backup  官方原版v7.7.0版本面板备份

**Centos/Ubuntu/Debian安装命令 独立运行环境（py3.7）**
```Bash
curl -sSO https://raw.githubusercontent.com/JzqIP/btpanel-v7.7.0/main/install/install_panel.sh && bash install_panel.sh
```

**屏蔽强制绑定手机、直接删除宝塔强制绑定手机js文件**
```Bash
sed -i "s|if (bind_user == 'True') {|if (bind_user == 'REMOVED') {|g" /www/server/panel/BTPanel/static/js/index.js
或sed -i "s|bind_user == 'True'|bind_user == 'XXXX'|" /www/server/panel/BTPanel/static/js/index.js
rm -rf /www/server/panel/data/bind.pl
或rm -f /www/server/panel/data/bind.pl
```

**安装好所有环境、插件之后阻止宝塔的自动检测以及升级**
```Bash
echo '127.0.0.1 bt.cn' >>/etc/hosts
```
