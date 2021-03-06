### 一：Git安装

在Linux上安装Git

```Linux
sudo apt-get install git
```

![fig1](../图片/fig1.png)

**全局配置**

```Linux
git config --global user.name "自己的用户名"
git config --global user.email "自己的邮箱"
```

![fig2](../图片/fig2.png)

![fig3](../图片/fig3.png)

百度内的Git托管平台  http://console.cloud.baidu-int.com/devops/icode/workspace/repos



# 二：Git的基本操作

![fig9](../图片/fig9.png)

## 2.1 本地修改和提交

![fig4](../图片/fig4.png)

![fig5](../图片/fig5.png)

## 2.2：为提交贴标签 git tag

![fig6](../图片/fig6.png)

**友好的status操作： git status -sb -uno --show -stash**

![fig7](../图片/fig7.png)

**友好的log操作： **

**git log --pretty=format:'%h %Cgreen%ar %Cred%an %Creset  %s    %C(auto)%d '  -10**

![fig8](../图片/fig8.png)





# 三：Git分支管理

**git创建分支快的原因**

![fig17](../图片/fig17.png)

![fig10](../图片/fig10.png)

## 1：分支的创建 git brance 分支名

![fig11](../图片/fig11.png)

## 2：分支的切换 git checkout 分支名

![fig12](../图片/fig12.png)

![fig13](../图片/fig13.png)

![fig14](../图片/fig14.png)

当再次切换回master分支时

![fig15](../图片/fig15.png)

**如果此时在master分支上进行提交，master分支向前移动会出现分叉**

![fig16](../图片/fig16.png)

## 3：分支的合并

问题描述：在当前分支上发现了错误，需要改正，可以在当前分支上创建一个新的改错分支

**git checkout -b 新分支名**

![fig18](../图片/fig18.png)

![fig19](../图片/fig19.png)

![fig20](../图片/fig20.png)

![fig21](../图片/fig21.png)

```Linux
git brance -b 分支名：删除分支
```

![fig22](../图片/fig22.png)

**Git 会使用两个分支的末端所指的快照（`C4` 和 `C5`）以及这两个分支的公共祖先（`C2`），做一个简单的三方合并。**

![fig23](../图片/fig23.png)

![fig24](../图片/fig24.png)

## 4：分支管理策略

> * master分支
> * release分支
> * develop分支
> * hotfix分支

![fig25](../图片/fig25.png)

![fig26](../图片/fig26.png)

![fig27](../图片/fig27.png)

![fig28](../图片/fig28.png)



# 4：团队开发

```git
git brance -a -v              可看到远程与本地的所有提交信息
git log --onlien --graph      可看到本地的所有提交信息
```

![fig29](../图片/fig29.png)

1：克隆

![fig30](../图片/fig30.png)

```shell

```

![fig31](../图片/fig31.png)

![fig32](../图片/fig32.png)

**git fetch origin 分支名【：本地分支名】    /  git remote updata  origin【：本地分支名】** 

**都需要接   merge origin/分支名 本地分支名   才能将远程仓库的更新内容合并到本地分支上**

![fig33](../图片/fig33.png)

![fig34](../图片/fig34.png)

**实际开发时的流程：自己在本地提交后，先拉取网上的最新分支，在本地合并解决冲突后，在推送到线上**

![fig35](../图片/fig35.png)

![fig36](../图片/fig36.png)