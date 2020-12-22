模拟实际项目开发流程，依次进行如下操作，所有操作均在IDEA下完成：
1. 项目拉取(clone)
2. 切换分支(checkout)
3. 更新(pull)
4. 修改代码
5. 提交(commit)
6. 追加提交(amend commit)
7. 上传远程仓库(push)
8. 解决冲突(merge or rebase)
9. 再次上传

# 1. 项目拉取

> File -> New -> Project from Version Control

![image-20201222175509959](README.assets/image-20201222175509959.png)

> 输入URL地址

![image-20201222165909951](README.assets/image-20201222165909951.png)

# 2. 切换分支

> 点击右下角的master，此区域显示当前分支名称

![image-20201222175412165](README.assets/image-20201222175412165.png)

> 选择remote branches中的develop分支 -> checkout

![image-20201222175835845](README.assets/image-20201222175835845.png)

# 3. 更新(pull)

![image-20201222180222072](README.assets/image-20201222180222072.png)

> 如果真的有更新，可以在git日志中看到更新的内容

![image-20201222180406239](README.assets/image-20201222180406239.png)

# 4. 修改代码

...

# 5. 提交(commit)

> 红色部分是未加入版本控制的，蓝色部分是修改的，灰色部分是删除的

![image-20201222192547168](README.assets/image-20201222192547168.png)

> 加入版本控制

![image-20201222193910378](README.assets/image-20201222193910378.png)

> 提交至本地，使用commit即可，不要commit and push

![image-20201222193003990](README.assets/image-20201222193003990.png)

# 6. 追加提交(amend commit)

> 选中amend后，继续提交

![image-20201222194623043](README.assets/image-20201222194623043.png)

# 7. 上传远程仓库(push)

![image-20201222195641806](README.assets/image-20201222195641806.png)

> 如果有冲突会提示push失败，此时选择cancel，不要直接尝试合并

![image-20201222195551097](README.assets/image-20201222195551097.png)

# 8. 解决冲突(merge or rebase)

## rebase

> 更新项目，解决冲突

![image-20201222180222072](README.assets/image-20201222180222072.png)

![image-20201222200105321](README.assets/image-20201222200105321.png)

> 左边是本地的内容，右边是远程仓库的内容，中间的是合并后的结果
>
> 绿色的是没有冲突的部分，红色的是有冲突的地方，需要重点关注

![image-20201222201103773](README.assets/image-20201222200237627.png)

> 某一段代码没有问题，就选择箭头，表示接受，即可将对应区域的代码复制到中间区域
>
> 如果某段代码有问题，就选择叉叉，表示拒绝
>
> 完成接受或拒绝的操作后，如果代码还需要额外的调整，也可以在中间的区域直接修改

![image-20201222200802329](README.assets/image-20201222200802329.png)

> 所有的冲突都解决后，就会出现如下提示，然后就可以apply，解决冲突

![image-20201222200825985](README.assets/image-20201222200825985.png)

完成后，可以看到历史记录是一条直线，没有分叉

![image-20201222201103773](README.assets/image-20201222201103773.png)

## merge

再次人为冲突，使用merge解决

# 9. 再次上传

