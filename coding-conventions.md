# Coding-conventions

1. 医大服务器A1-3各位用户： 请使用newproject命令生成工程架构。举例：
  ```
  newproject project abc
  Reinitialized existing Git repository in /data/chuyanshuo/Projects/project abc/.git/
  ```

2. 使用step01:xxx, step02:xxx, step03:xxx 的方式命名文件夹；有不互相依赖的step，例如，step01之后可以有多个step02；如果step03依赖step01和step02的输出，请在run.sh中，文件头注释说明，复杂情况，请单独使用readme文档说明，放在相同文件夹下
   
3. 各文件夹下，pipeline**运行逻辑**和**运行参数**务必进行**物理隔离**，例如：在step01:xxx文件夹中，脚本qc.R按照这个[设置参数传递方法](https://slide.yanshuo.site/data-science-engineering/#/11/2)，然后在相同文件夹下，创建run.sh脚本，用于传递参数（包括路径参数）
   
4. 每一个文件夹下，只能有一个“run.sh”脚本

5. 所有脚本的变量命名方法，请用下划线方法命名，尽量避免驼峰命名

6. 请做分析的同学，使用其他文章中的知识，例如marker集合做细胞类型鉴定，把marker list整理成tab间隔的tsv，或者逗号分割的csv表格，第一行为文件头。另外再生成一个readme文档，其中说明该知识的精确来源，文章名字，页码等。将以上文件放在一个单独命名的文件夹中
   
7. 请将（6）中的文件夹放在knowledge的private文件夹中

8. 如果有多个projects多次重复用到（6），请要求高并发分析平台小组的成员，将其从private放到public

