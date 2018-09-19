---
layout:     post
title:      "CentOS7 ������ü�ʹ��"
subtitle:   ""
date:       2017-11-22
author:     "jiangydev"
header-img: "img/post-bg-unix-linux.jpg"
tags:
    - CentOS
    - Linux
---

# CentOS ������ü�ʹ��

## ��̬��������

1. �����ļ���/etc/sysconfig-scripts/ifcfg-xxx

2. �޸���������
```
# ���þ�̬
BOOTPROTO=static
# ϵͳ����ʱ���ظ�����
ONBOOT=yes
```

3. ��Ӿ�̬����
```
IPADDR=192.168.XX.XX
NETMASK=255.255.255.0
GATEWAY=192.168.XX.XX
DNS1=192.168.XX.XX
```

4. �������������
service network restart  


## ����YUMԴ

1. ���ȱ���/etc/yum.repos.d/CentOS-Base.repo

mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup

2. ���ض�Ӧ�汾��repo�ļ�
wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.163.com/.help/CentOS7-Base-163.repo
http://mirrors.aliyun.com/repo/Centos-7.repo


3. ���������������ɻ���
yum clean all
yum makecache