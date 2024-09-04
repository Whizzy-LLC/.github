# Pull Request (PR) 规则

**TLDR;**

```
git checkout main
git pull
git checkout -b dev-[feature or patch name]-[your name]  
git add [files ..]
git commit -m "[feature] by [your name]: [changes]"
git pull origin main --rebase  
git push -u origin dev-[feature or patch name]-[your name]
开启 Pull Request
```

1. 更新主分支
   - 确保你的本地主分支(通常是 main 或 master)是最新的
   - 执行 `git pull origin main`

2. 创建新分支
   - 从更新后的主分支创建一个新的功能分支
   - 使用描述性的分支名称，如 `git checkout -b feature/add-login-functionality`

3. 开发新功能
   - 在新分支上进行开发工作
   - 定期提交更改，使用清晰的提交信息
     - 使用 `git status` 查看更改的文件。
     - 使用 `git add <文件名>`（指定文件名）或 `git add .`（`.` 指当前目录下的全部文件）添加更改到暂存区。
     - 使用 `git commit -m` "本次提交信息" 提交更改。

4. 代码审查和测试
   - 在本地进行代码审查
   - 运行所有相关的测试，确保没有破坏现有功能

5. 更新分支
   - 再次从主分支拉取最新更改
   - 将你的功能分支与主分支进行 `rebase`
   - `git pull origin main --rebase` 

6. 推送到远程仓库
   - 将你的功能分支推送到远程仓库
   - `git push origin feature/add-login-functionality`

7. 创建 Pull Request
   - 在 GitHub 上创建新的 PR
   - 填写 PR 标题和描述，清楚说明你的更改

8. 请求代码审查
   - 指定一个或多个审阅者
   - 回应审阅者的评论和建议

9. 合并 PR
    - 一旦 PR 被批准，合并到主分支
    - 选择 rebase

10. 清理
    - 删除已合并的本地和远程功能分支
