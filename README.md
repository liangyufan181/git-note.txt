Git 学习实践笔记
 
一、学习资料来源
 
1. Git官方中文文档：https://git-scm.com/book/zh/v2
2. 菜鸟教程Git全套教程：https://www.runoob.com/git/git-tutorial.html
3. B站Git零基础实战教学视频：https://www.bilibili.com/video/BV1FE411P7B3/
 
二、实践流程
 
（一）Git安装与环境配置
 
1. 前往Git官网https://git-scm.com/downloads下载对应操作系统的安装包，全程默认安装；
2. 打开Git Bash终端，配置全局用户名和邮箱，执行命令：
 
 
 
3. 输入 git config --list 查看配置信息，确认配置生效。
 
（二）本地仓库创建
 
1. 在本地电脑新建文件夹，命名为 git-learning-practice ；
2. 进入文件夹，右键选择 Git Bash Here 打开终端；
3. 执行 git init 命令，初始化本地Git仓库，出现 Initialized empty Git repository in xxx 提示即创建成功。
 
（三）远程仓库创建与关联
 
1. 登录Gitee码云平台https://gitee.com/，完成注册及实名认证；
2. 点击右上角「新建仓库」，填写仓库名称 git-learning-practice ，设置为公开仓库，不勾选初始化README文件，完成创建；
3. 复制仓库HTTPS地址，本地终端执行关联命令：
 
 
 
4. 执行 git remote -v 查看关联结果，确认远程仓库关联成功。
 
（四）代码提交与远程推送
 
依次完成文件创建、添加、提交、推送操作，实现本地文件同步至远程仓库。
 
三、提交记录说明
 
1. 第一次提交：创建Git基础命令笔记文件 git-note.txt ，整理Git安装、配置、初始化仓库等基础命令，完成首次本地提交；
2. 第二次提交：新增读书笔记文件 reading-notes.md ，撰写编程类书籍读书笔记，完成作业拓展要求；
3. 第三次提交：编写本次实践完整README.md文档，记录实践全流程、问题解决及学习心得，完成最终提交并推送至远程仓库。
 
四、遇到的问题及解决方法
 
问题1：git push推送时报错 fatal: remote origin already exists 
 
- 问题原因：本地仓库已关联过其他远程仓库，重复关联导致冲突；
- 解决方法：执行 git remote remove origin 删除原有远程关联，再重新执行远程仓库关联命令。
 
问题2：git push推送时提示身份认证失败/权限被拒绝
 
- 问题原因：Gitee/GitHub更新认证规则，原用户名密码登录方式失效，或仓库地址输入错误；
- 解决方法：
① 检查并重新复制正确的远程仓库HTTPS地址；
② 生成平台个人访问令牌，推送时用令牌代替密码认证；
③ 执行 git remote set-url origin 正确的仓库地址 重新配置远程地址。
 
问题3：执行git commit提示 nothing to commit, working tree clean 
 
- 问题原因：本地文件未修改，或修改后未添加到暂存区；
- 解决方法：修改文件内容后，执行 git add . 将所有修改文件加入暂存区，再重新执行提交命令。
 
五、Git学习心得
 
通过本次Git实践学习，我熟练掌握了Git环境配置、本地仓库创建、远程仓库关联、文件提交与推送等核心基础操作，深刻理解了版本控制工具在代码管理中的核心作用。Git能够完整记录文件每一次修改，有效规避代码丢失、版本混乱等问题，无论是个人学习还是团队协作都具备极强的实用性。
 
在实践过程中，通过排查远程关联、身份认证等实操问题，有效提升了自身错误排查和问题解决能力。后续我将继续深入学习Git分支管理、代码合并、版本回退、团队协作开发等高级功能，熟练运用Git进行代码管理，为后续编程学习和项目开发夯实基础。
 
六、拓展高级功能实践
 
额外学习并实践Git进阶操作，具体流程如下：
 
1. 分支创建与切换： git branch dev 创建开发分支， git checkout dev 切换至dev分支；
2. 分支修改与提交：在dev分支完成文件修改并提交，实现独立开发；
3. 分支合并：切回master主分支 git checkout master ，执行 git merge dev 合并分支内容；
4. 版本回退： git log 查看提交历史，执行 git reset --hard 提交ID 回退至指定版本；
5. 简洁查看日志： git log --oneline 一键查看精简提交记录。
 
七、规范提交命令
