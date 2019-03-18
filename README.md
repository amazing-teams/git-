### git常用命令
![image](https://images2015.cnblogs.com/blog/1009686/201608/1009686-20160824100127870-1820786836.png)

### <font color= coral>GitFlow</font>
**1.当前分支master**
```bash
git pull --rebase master
```
**2.第一次开始任务 TDP-xxx， 创建分支, “/”前面可用fix, feature, hotfix, 对应修改bug，新需求功能，紧急修复**
```bash
git checkout -b feature/yourname_TDP-xxx
```
**3.不是第一次开始任务，切换分支**
```bash
git checkout feature/yourname_TDP-xxx
```
**4.修改完, 提交修改**
```bash
git add *
git commit -m'自己修改的内容的描述'
git push origin feature/yourname_TDP-xxx
```
**5.自己本地测试完后线上测试,合并， merge, 切换到 dev分支, 并更新dev分支到最新**
```bash
git checkout dev
git pull --rebase origin dev
git merge --no-ff feature/yourname_TDP-xxx
```
**6.成功后**
```bash
git push origin dev
```
**7.在dev上查看自己修改是否成功, 如果没有问题，在gihub上创建pull request**

**8.结束>>>**
