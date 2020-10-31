# cdx_2020e8013382017
部署在heroku上的lita应用，用于多人在slack聊天室与lita机器人进行聊天交互
## 1. [DeepCube](http://czx.ac.cn/deepcube)
### 1.1 环境要求
1. Linux环境（unbutun16.04测试成功）
2. ruby == 2.5.8
3. gem ==
4. redis == 4.2.2
5. lita == 4.8.0
6. hero cli ==
7. rails == 
8. bundler == 2.1.4
9.更多包要求在gemfile.lock里

### 1.2 启动过程（上述环境安装好后）
-------------------------------
pip install -r requirements.txt
cd flask
python app.py
-------------------------------

### 1.3 目录结构安排
1. code
    - 存放深度学习求解魔方模型的代码
    - 详细解释参照code/README.md
    - 其中code\scripts\nnetSolve.py为魔方求解接口
2. flask
    - 存放flask服务器后端
    - 具体如下：
        - app.py：服务器运行文件
        - static：网页静态资源（js脚本等）
        - templates：存放页面html文件
3. environment
    - 原深度学习求解魔方模型的文件夹，暂无用
4. metadata
    - 原深度学习求解魔方模型的文件夹，暂无用

### 1.4 注意事项

### 1.5 参考


