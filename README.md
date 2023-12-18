# resources-py-module
这是一个python的资源管理模块，更好的帮助一些需要从指定目录加载文件或是获取路径而创建的模块
## 示例
```python
import resources
# setting resources root
resources.set_base("/src")

resources.path("update.file") # just return str
resources.load("version.txt").text
resources.load("userData.pyc").Object
resources.load("user_data.json").json

resources.get("scripts").path("main.py") # src/scripts/main.py

resources.get("data").load("user.txt").text # return src/data/user.txt content(str)
resources.get("data").load("player_data.pyc").Object # return pickle.load Object
resources.get("data").load("user_data.json").json # return dict(json load object)



```
