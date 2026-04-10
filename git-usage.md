# Git版本管理使用说明

本文档介绍如何使用Git进行版本管理和代码上传到GitHub的操作步骤。

## 一、初始化Git仓库

1. **进入项目目录**：打开终端，切换到你的项目目录
2. **初始化仓库**：执行以下命令
   ```bash
   git init
   ```

## 二、配置.gitignore文件

创建 `.gitignore` 文件，添加需要忽略的文件和目录：

```gitignore
# 临时文件
*.tmp
*.temp

# 编辑器文件
.vscode/
.idea/
*.swp
*.swo
*~

# 系统文件
Thumbs.db
.DS_Store

# 日志文件
*.log

# 编译产物
node_modules/
dist/
build/

# 环境变量文件
.env
.env.local
.env.*.local
```

## 三、添加文件到暂存区

```bash
git add .
```

## 四、提交修改

```bash
git commit -m "提交信息"
```

## 五、添加远程仓库

```bash
git remote add origin https://github.com/username/repository.git
```

## 六、推送代码到远程仓库

```bash
git push -u origin master
```

## 七、后续更新操作

1. **修改文件**：编辑你的项目文件
2. **添加修改**：
   ```bash
   git add .
   ```
3. **提交修改**：
   ```bash
   git commit -m "提交信息"
   ```
4. **推送代码**：
   ```bash
   git push
   ```

## 八、常用Git命令

- **查看状态**：`git status`
- **查看历史**：`git log`
- **查看分支**：`git branch`
- **创建分支**：`git branch branch-name`
- **切换分支**：`git checkout branch-name`
- **合并分支**：`git merge branch-name`

## 九、远程仓库操作

- **查看远程仓库**：`git remote -v`
- **拉取代码**：`git pull`
- **推送标签**：`git push --tags`

## 十、注意事项

1. **提交信息**：提交信息应该清晰明了，描述本次修改的内容
2. **忽略文件**：确保 `.gitignore` 文件配置合理，避免提交不必要的文件
3. **定期提交**：建议定期提交代码，保持版本历史的完整性
4. **分支管理**：对于复杂项目，建议使用分支进行开发和管理

## 十一、遇到问题

如果遇到权限问题或推送失败，可以检查：
1. GitHub账号是否有仓库的访问权限
2. 网络连接是否正常
3. 远程仓库地址是否正确

如果需要重新设置远程仓库，可以执行：
```bash
git remote set-url origin https://github.com/username/repository.git
```