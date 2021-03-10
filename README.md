# Linux常用命令

## 展示方式说明
所有的展示都是通过以下三个部分组成：<br />
   1、问题 <br />
   2、代码or解决方案 <br />
   3、参考资料 <br />
   
##
**Q1**: linux通过zip命令压缩指定格式文件？<br />
**Code**:
```shell script
# 如果dir_name目录下有四种格式的文件: .csv, .xlsx, .ipynb以及.py文件,
# 我们只想压缩.ipynb和.py文件,有两种方式

# 1.显示的指出要压缩的文件格式
zip -r dir_name.zip dir_name --include '*.py' '*.ipynb'

# 2.显示的指出要剔除的文件格式
zip -r dir_name.zip dir_name --exclude '*.csv' '*.xlsx'

# 剔除隐藏文件的
zip -r dir_name.zip dir_name --exclude '*/.*'
```
**References**:<br />
https://superuser.com/questions/831169/from-the-command-line-how-do-i-zip-specific-files-and-directories-into-one-comp

##
**Q2**: linux通过find命令删除指定格式文件？<br />
**Code**:
```shell script
# 删除当前目录及子目录下的.csv文件
find . -name '*.csv' -delete
```
**References**:<br />
https://stackoverflow.com/questions/785519/how-do-i-remove-all-pyc-files-from-a-project

# TO BE CONTINUE
## License
[MIT](https://choosealicense.com/licenses/mit/)