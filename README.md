> 信息检索课程期末作业：中文检索系统

## 检索系统运行说明

### 运行环境

带有 Python3 环境的 Windows 系统，其他系统未经测试（其他环境不保证文件读取写入是否成功）。

> 建议安装 Python 包 tqdm（未安装不会报错）。

### 文件编码：UTF-8

### 参数说明与修改

代码运行时的参数设置文件全部位于 `settings.py` 文件中。

> 这里的修改是可选的。**如果不做修改，默认在 `out` 目录下生成文件 `1927405160&张昊&自写.txt` 作为第二次系统测试的输出结果。**

与结果生成有关的关键参数说明如下：

1. `settings.py` 文件中，变量 `RAW_CORPUS_PATH` 为数据集文件相对于项目根目录的相对路径
   【默认配置：`"data\\documents.txt"`，如果只需第二次的结果就不需要修改】
2. `settings.py` 文件中，变量 `QUERY_PATH` 为查询文件相对于项目根目录的相对路径
   【默认配置：`"data\\quesions.txt"`，如果只需第二次的结果就不需要修改】
3. `settings.py` 文件中，变量 `OUTPUT_PATH` 为结果输出文件相对于项目根目录的相对路径
   【默认配置：`"out\\result.txt"`】 

其他未提及的参数无需改动。

### 运行方法

配置好上述参数后（如果需要的话），运行 `main.py`，即可在 `out` 目录下获得文件 `result.txt`，为第二次系统测试的输出结果。

**注意：`main.py` 的工作目录需要为 `main.py` 所在的目录。【参考图片：`程序运行示例（直接生成结果文件）.png`】**

### 其他文件说明

+ `data\documents.txt` 为数据集文件，**代码运行必需**
+ `data\q100.txt` 为第一次100个查询的查询文件
+ `data\query_train.txt` 为训练用的29个查询的查询文件
+ `data\quesions.txt` 为第二次1000个查询的查询文件，**生成第二次查询结果必需**
+ `data\STOPWORDS`、`index_files\CORPUS_DATA`、`index_files\WORD_COUNTS` 为代码运行必需的数据文件。
  其中`index_files\CORPUS_DATA`、`index_files\WORD_COUNTS` 为程序生成的索引文件，可以删除；`data\STOPWORDS` 为停用词表，**必须存在**
