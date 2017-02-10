---
title: Hexo 部署问题收集
date: 2017-02-08 14:34:36
tags:
---
## Permission denied (publickey)
xxxxx@xxxx:~$ ssh -T git@github.com
Agent admitted failure to sign using the key.
Permission denied (publickey).
解决办法：
``` bash
xxxxx@xxxx:~$ ssh-add
```

再ssh 然后有出现：
Hi olivesWh! You've successfully authenticated, but GitHub does not provide shell access.

如果一切正常你会看到这个:
Hi username! You’ve successfully authenticated, but GitHub does not provide shell access.
当然了,实际情况其实是这样的:
Permission denied (publickey).

去 https://github.com/account 添加一个新的pubkey,或者edit现在的key,完成

最后在 git bash 窗口(不是 cmd)运行 hexo d 就可以了.

## 没有样式问题
网站没有引入自己的域名的时，_config.yml中 root参数不要修改。
