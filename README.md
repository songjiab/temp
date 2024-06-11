
# markdown
  * markdown是文本修饰语言，用特殊符号修饰正文效果，<br>是换行符号，在两个文本之间加一个空行也算换行
# 标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题

## /转义符


*测试*<br>
  **测试**
  ***测试***
~~测试~~<br>
***
---
> hahahaahahahaah
>> 嘿嘿
>>> 三级
>>>> 四级

* 游戏
  * 原神
  * APEX

1. 游戏
   1. 原神
   2. APEX

名称|技能|排行
--|:--:|--:
蝙蝠侠|钱|11
蜘蛛侠|线|22

```C
	#include<stdio.h>
	int main()
	{
		printf("test C");
		return 0;
	}


```
[Github](https//www.github.com "点击访问")


![截图](C://Users//UserX//Desktop//1.jpg "点击查看")

# 基础命令
  * 创建仓库：git init 仓库名
  * 查看git配置文件：git config --list
  * 添加邮箱：gti config --global user.email "邮箱"
  * 添加姓名：gti config --global user.name "姓名"
  * 创建本地密文：ssh-keygen -t rsa -C "注册邮箱"
  * 到网站里找到设置中的 SSH and GPC keys 设置密文：找到保存密文的位置有pub文件，用记事本打开，将密文粘贴到 SSH and GPC keys 中保存
  * 测试关联是否成功：ssh -T git@github.com，要用yes重复确认一下，跟你打招呼就是成功
  * 在个人仓库这，这个地址就是这个仓库，只要向这个地址上传，就是向仓库上传，用SSH的地址
  * 将这个地址起个别名：git remote add origin "地址" ，以后origin就是指这个地址
  * 删除origin别名：git remote remove origin
  * 查看本地状态：git status
  * 恢复刚才被   rm 文件名  的文件：git restore 文件名（需要本地仓库存在才能恢复，git rm 文件名 就不能用这个恢复）
---
# 本地设备与云端仓库的交互逻辑
  * 先将代码压缩到git缓冲区，再将git缓冲区内的代码提交到本地仓库，再将本地仓库的代码更新到云端仓库（上传的本地仓库的分支与云端仓库的分支是一致的，他们会合并 ；不一致就在云端创建一个新的分支）
  * 添加：git add code.c
  * 提交：git commit -m "提交说明"
  * 推：git push origin master
  * 拉：git push --rebase origin master
    * 会有三种选择：skip 留云端的 ；continue 合并 ；abort  留本地的
  * 如果直接在云端修改代码，本地不知道，最后会提交失败，因为代码更新的依赖关系被破坏了，本地的内容要比云端新；
  * 解决办法：先拉取 git pull 云端内容，与本地内容合并或操作，之后在提交（拉）即可
  * 删除云端文件：与提交一样，就是将添加变为 git rm 文件名 删除文件，最后也需要推
---
# 下载开源代码
  * 下载地址用https的网址
  * git clone "地址" ，下载的东西在仓库的文件夹中
---

  





