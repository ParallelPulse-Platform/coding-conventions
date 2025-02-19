# Coding-conventions

1. 医大服务器A1-3各位用户： 请使用newproject命令生成工程架构。举例：
  ```
  newproject project abc
  Reinitialized existing Git repository in /data/chuyanshuo/Projects/project abc/.git/
  ```
2. 使用step01:xxx, step02:xxx, step03:xxx 的方式命名文件夹
3. 各文件夹下，pipeline**运行逻辑**和**运行参数**务必进行**物理隔离**，例如：在step01:xxx文件夹中，脚本qc.R按照这个[设置参数传递方法](https://slide.yanshuo.site/data-science-engineering/#/11/2)，然后在相同文件夹下，创建run.sh脚本，用于传递参数（包括路径参数）
4. 每一个文件夹下，只能有一个“run.sh”脚本