# mybot_proj
部署在heroku上的lita应用，用于多人在slack聊天室与lita机器人进行聊天交互
## 1. 项目说明（github地址：https://github.com/Deacychen257/mybot_proj/tree/master，master分支）
### 1.1 环境要求
1. Linux环境（unbutun16.04测试成功）
2. ruby == 2.5.8
3. gem == 2.7.6
4. redis == 4.2.2
5. lita == 4.8.0
6. heroku cli客户端
7. rails == 6.0.3
8. bundler == 2.1.4
9. lita-slack == 1.8.0
9.包的依赖库在gemfile.lock里可见

### 1.2 启动过程（上述环境安装好后）
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
1.  cd到项目文件夹，使用bundle命令安装依赖库；cd到项目文件夹下的lita-doubler文件夹，使用bundle命令安装依赖库
2.  cd到项目根目录，用heroku create命令创建heroku应用
3.  进入slack.com，登录并进入自己的工作空间，添加lita app，并将该app的API令牌配置到项目根目录下的lita_config文件中
4.  用heroku login -i命令登录到heroku，使用git push heroku命令把项目推送到heroku平台，并打开push日志中的最后一条网址登录
5.  自己的slack聊天室中选择random频道，将刚刚配置好的lita机器人添加到该频道，@该机器人并输入double 10指令，如果机器人返回10+10=20，则运行成功
-----------------------------------------------------------------------------------------------------------------------------------------------------------------

### 1.3 目录结构安排
1. lita-doubler
    - 存放lita返回两整数加和功能的文件夹
    - 其中lita-doubler\lib\lita\handlers\doubler.rb为
    - 其中lita-doubler\lib\lita\handlers\doubler_spec.rb为
2. Gemfile
    - 在该文件中指定所需的gem和指定下载源，bundle可以根据该gemfile文件下载所需的gem
3. Gemfile.lock
    - bundle根据gemfile安装完gem和其依赖库后，会生成 Gemfile.lock 文件，该文件记录了确切的gem名称和版本号，以及他们所依赖的库
4. lita_config.rb
    - 针对slack进行配置。使得litabot能连接上slack community
5.Procfile
    -Heroku应用程序包含一个Procfile，该文件指定了应用程序在启动时执行的命令，本项目中的命令是web: bundle exec lita

### 1.4 注意事项
*  登录slack.com网站时需要连接VPN
*  用heroku cli命令行登录heroku时，需使用heroku login -i命令才能成功登录
*  用git时，不要将应用推到github，这样slack社区会由于安全问题取消你的API令牌，导致无法引用lita

### 1.5 参考
罗铁坚教授            高级软件工程作业指导2020.pdf
Daniel Pritchett     Build Chatbot interactions.pdf

