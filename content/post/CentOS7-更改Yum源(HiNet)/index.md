+++
author = "Hugo Authors"
title = "Centos7-更改Yum源(HiNet)"
date = "2022-08-10"
#description = ""
categories = [
    "Linux"
]
tags = [
    "CentOS",
]
image = "100.png"
+++

    # CentOS-Base.repo
    #
    # The mirror system uses the connecting IP address of the client and the
    # update status of each mirror to pick mirrors that are updated to and
    # geographically close to the client. You should use this for CentOS updates
    # unless you are manually picking other mirrors.
    #
    # If the mirrorlist= does not work for you, as a fall back you can try the 
    # remarked out baseurl= line instead.
    #
    #
    
    [base]
    name=CentOS-$releasever – Base
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=os
    baseurl=http://mirror01.idc.hinet.net/CentOS/$releasever/os/$basearch/
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
    
    #released updates 
    [updates]
    name=CentOS-$releasever – Updates
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=updates
    baseurl=http://mirror01.idc.hinet.net/CentOS/$releasever/updates/$basearch/
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
    
    #additional packages that may be useful
    [extras]
    name=CentOS-$releasever – Extras
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=extras
    baseurl=http://mirror01.idc.hinet.net/CentOS/$releasever/extras/$basearch/
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
    
    #additional packages that extend functionality of existing packages
    [centosplus]
    name=CentOS-$releasever – Plus
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=centosplus
    baseurl=http://mirror01.idc.hinet.net/CentOS/$releasever/centosplus/$basearch/
    gpgcheck=1
    enabled=0
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
    
    #contrib – packages by Centos Users
    [contrib]
    name=CentOS-$releasever – Contrib
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=contrib
    baseurl=http://mirror01.idc.hinet.net/CentOS/$releasever/contrib/$basearch/
    gpgcheck=1
    enabled=0
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
    
    
    #按Esc，打入 :wq 即寫入檔案，
    
    #完成後更新資料
    yum clean all
    yum update -y

***

{{< css.inline >}}
<style>
.emojify {
	font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
	font-size: 2rem;
	vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>
{{< /css.inline >}}
