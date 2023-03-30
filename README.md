# git教程--hkx
如果大家是第一次使用git上传文件，难免会遇到非常多的问题，大家可以先看看我的这边文章，避免各位在使用git的分支管理时出现难以解决的各种问题  

## 第一步
进入你的github页面，点击你的头像，点击repositories来进入仓库页面。  
点击绿色按钮New创建新的仓库，你只需要填写repository name（随便取个名字），然后拉到页面最下面，点击绿色按钮`Create repository`  
![](img/img8.png)  
  
创建成功后，你可能会直接跳转到这一页：(如果没有跳转，从左上角头像 -> repositories来进入你刚刚新建好的库)    
![](img/img9.png)  
  
第一个圈中，你可以选择HTTPS的方式或者SSH的方式，然后在命令行中新建一个文件夹，进入文件夹后运行第二个圈中的代码（会因为你选了HTTPS或SSH而不同）。  
  
如果你是第一次使用git上传文件，这里一定会出问题，此时你必须在你的电脑上配置好SSH或Github API等（选一个方式即可，我推荐ssh）。这里我也帮不了大家，任何报错可以直接搜索引擎或chatGPT   
  
**注意**: 你必须将README.md文件成功上传到你的新建的库中，确保无误后再进行第二步
  
## 第二步
在开始第二步前，确保你成功完成了第一步  
首先，创建一个文件夹，从命令行进入该文件夹(`cd`命令，不会命令行的请善用搜索引擎和chatgpt)，在命令行中输入`git clone https://github.com/Taylorblue123/webpageDesignLab-group35`。  
此时，你的文件夹下会出现一个新的文件叫做webpageDesignLab-group35，从命令行进入该文件夹，进入之后首先输入`git branch`，确保输出中有`* main`，如果没有，请联系hkx  
接着，使用`git branch xxxx`，这里的xxxx是你的新的branch的名称，你可以仿照我的branch的名称`KaixuanHou`，使用自己的名字作为branch名称  
  
再次`git branch`,这时候确保你的输出中有`* main`和你刚刚创建好的bran名称(如`KaixuanHou`)  
  
使用`git checkout xxxx`，xxxx为你刚刚建立的branch的名称。然后再次执行`git branch`，此时，你的输出中的`*`号应该从main移动到了你的branch上  
![](img/img1.png)  
  
如果确认无误，则依次输入以下代码：
1. `git add *`
2. `git commit -m "wwx_hkx test commit"`
注释： "wwx\_hkx test commit"为提交的信息，这个信息应该规范为你的提交信息，这个信息不影响实际的提交过程。比如你是hkx，你第一次提交你的代码，则这里的信息可以写"HKX： first commit"，这里写好后，最终的成效如下：    
![蓝框中为提交信息](img/img2.png)  
  
3. `git remote add wuwenxuan_origin git@github.com:Taylorblue123/webpageDesignLab-group35`: 同样，这里首次创建origin，`wuwenxuan_origin`应该换成你想创建的自己的origin名字。 同时，请注意`git@github.com:Taylorblue123/webpageDesignLab-group35`应改为你在第一步中`remote add .....`时的路径名使用的方式，我这里是因为使用了SSH，如果你用了Github token，最后的这个路径名会不一样(*注意，第一次使用时需要remote add，之后再次使用时，比如下一次提交代码，只要你的origin还在，就可以使用相同origin，而不用重新remote add了*)    
4. `git push -u wuwenxuan_origin wuwenxuan`: 同样，倒数第二个参数改为你的origin名字，最后一个参数改为**你的分支的名字**
  
如果一切顺利，此时你登录github，到我们的项目页面，点左上角的main，你应该可以看到你自己刚刚创建好的分支：  
![](img/img4.png)  
继续点击你的分支，进入你的分支中，看看你刚刚写好的文件是否都在这里  
如果没问题，接下来选择pull request  
![](img/img5.png)  
  
点击右边的绿色按钮`New pull request`，然后在下面这里选择你自己的分支  
![](img/img6.png)  
  
然后点击新页面的绿色按钮`Create pull request`，进入一个文本框，这里随便填几个字，点击下面的绿色按钮`Create pull request`  
最终如果你进入了这个页面，恭喜你提交成功，接下来等待管理员审核就可以了  
![](img/img7.png)
