# 撤销工作区的代码
```shell
# 如果一个文件变更了太多，不想一行一行代码删除，可通过下面的命令恢复  （相当于删除文件重新拉取！！）
git restore <file>
```

# 撤销暂存区的代码
```shell
# 作用是将暂存区的文件从暂存区撤出，但不会更改文件的内容。
git restore --staged <file>

# 全部文件
git reset head
```

# 撤销本地仓库的代码 （已经commit，但未push状态）
```shell
# 不清空暂存区，保留本地代码
git reset --soft HEAD~1

# 清空暂存区，保留此次修改的代码
git reset --mixed HEAD~1

# 清空暂存区，本地代码直接恢复到上一个版本
git reset --hard HEAD~1
```

