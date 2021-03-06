<body marginheight="0"><h2>🧡第一部分：git基础了解</h2>
<h3>git：版本管理工具，将更新记录保存起来</h3>
<pre><code>
a.下载：官网下载
b.安装：一直下一步
c.Git仓库：存放项目状态的地方
d.工作目录：被git管理的项目文件
e.暂存区：存放被修改过的文件
f.Git自动产生的分支叫做主分支（整个项目保证主分支的稳定）
g.主分支—&gt;开发分支（develop）—&gt;功能分支（feature） 具体功能分支基于开发分支进行创建。分支与分支之间无关，在开发分支的文件在主分支上看不到</code></pre>
<h3>Git使用：告诉git你是谁，需用到邮箱和名称</h3>
<pre><code>a.配置提交人姓名：git config --global user.name 姓名
b.配置提交人邮箱：git config --global user.email 邮箱
c.查看：git config --list
d.Global：全局配置</code></pre>
<pre><code>
Ex:新建文件夹：进入文件夹—&gt;右键git Bash Here 配置名字与邮箱（回车后无内容弹出则表示成功git config --list来展示）</code></pre>
<h3>👀重新配置：</h3>
<pre><code>法一：重复以上内容可进行原来的覆盖进行重新配置
法二：C盘\用户\使用的用户\.gitconfig文件  可在配置文件中进行更改</code></pre>
<h3>😊命令</h3>
<pre><code>
git init         初始化git库（新建项目后需进行初始化）

git status         查看文件状态

git log               查看提交的记录

git add文件名       将文件添加到暂存区  附：git add . 添加多个文件

git commit -m提交信息    向仓库提交代码说明 

git checkout 文件名    操作撤销：暂存区覆盖工作目录的文件

git rm --cached 文件名    将暂存区文件删除

git rest --hard commit ID    找到指定记录的id恢复之后覆盖暂存区和工作目录

git branch    查看分支

git branch 分支名称    新建分支

git switch 分支名称    切换分支 （修改提交后进行切换）

git merge 来源分支名称     进行合并分支  合并时：先切换到主分支添加分支

git branch -d 分支名称    必须合并后才能进行删除

git branch -D分支名称    强制删除

git stash     暂时保存更改用于分支临时切换，将所有改动先存储起来

git stash pop    恢复改动

git--version    查看版本

`删除分支时必须切换到别的分支进行该分支删除`</code></pre>
<h2>💚第二部分：github使用</h2>
<h3>🖊开发流程：</h3>
<pre><code>1.A在本地创建本地仓库
2.A创建github远程仓库
3.A将文件git push
4.B clone到本地进开发，B将本地开发内容推送到远程仓库，A在pull到本地</code></pre>
<p><img src="/images/01.png" alt="01" title="01">

</p>
<p><img src="/images/02.png" alt="02" title="02">

</p>
<h3>😶命令：</h3>
<pre><code>推送：git push 远程仓库地址 分支名                 
推送：git push -u 远程仓库别名 分支名称
//-u记住推送地址的分支 下次推送只需输入git push
起别名：git remote add 远程仓库别名 远程仓库地址</code></pre>
<p>对文件修改后应先添加git add 在添加说明git commit -m 说明 然后 git push

</p>
<h3>🎀克隆：git clone 仓库地址</h3>
<pre><code>注意：1.当B clone后 会将A的别名也clone啦
2.B修改后若要上传A的远程仓库需在github设置中添加开发者</code></pre>
<h3>✌拉取：</h3>
<pre><code>git pull 远程仓库地址/别名 分支名
注意：在已有本地仓库的基础上进行</code></pre>
<h3>🔮冲突：</h3>
<pre><code>A、B同时上传新版本时，先上传的有效，后上传会报错。</code></pre>
<h3>🎉SSH:</h3>
<pre><code>在push时不需要用户名和密码，即公钥与私钥的配对，公钥放在github账号中，私钥在我的电脑中。
生成秘钥:在控制台输入ssh-keygen 在我的电脑C盘的用户中找到.ssh文件
id_rsa 为私钥存在电脑
Id_rsa.pub为公钥添加到github
注意：若ssh存在错误可将我的电脑中.ssh删除后在重新生成</code></pre>
<h3>🐱Git忽略清单:</h3>
<pre><code>不需要管理的文件，不需要管理文件的文件名写入.gitignore。</code></pre>
<h3>✨详细说明:readme.md文件</h3>
<pre><code>http://mahua.jser.me/</code></pre>
</body></html>
