# virturlbox-kali
kali 基础


## virtualbox 基础配置

```base
20G 2核 高级设置 双向操作便于操作
```

## kali 无法定位软件包

> 无法定位软件包，这是 Kali Linux 新手面临的主要问题。E：无法找到软件包错误，这是 Kali 新手和想使用 `apt-get` 命令安装任何软件的人常遇到错误。

> 解决办法

1. 启动最高权限，鼠标打开 Root Terminal Emulator 工具（红色）

2. 打开资源文本
```base
sudo nano /etc/apt/sources.list  
```
3. 复制粘贴 保存
```base
deb http://http.kali.org/kali kali-rolling main non-free contrib
deb-src http://http.kali.org/kali kali-rolling main non-free contrib
deb http://old.kali.org/kali sana main non-free contrib
deb-src http://old.kali.org/kali sana main non-free contrib
```
4. 更新资源
```base
sudo apt-get update
```

5. 安装 软件包
```base
sudo apt install ./任意软件包
```
> 注意：必须带`./`表示路径
