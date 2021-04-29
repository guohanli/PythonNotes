### 什么是JSON（Javascript Object Notation）

JSON本质上是一种轻量级的数据交换格式。

字符串是JSON的表现形式，符合JSON格式的字符叫做JSON字符串。

JSON字符串中引号规定是**双引号**。

对于不同的语言，JSON字符串对应特定的数据结构。

|  json  | python |
| :----: | :----: |
| object |  dict  |
| array  |  list  |
| string |  str   |
| number |  int   |
| number | float  |
|  true  |  True  |
| false  | False  |
|  null  |  None  |

反序列化：json字符串向Python数据结构转换

```python
import json
# 定义JSON字符串
json_str = '{"name":"lgh", "age":20}'
# json.loads方法将JSON字符串转换成字典
student = json.loads(json_str)
print(student['name']) # lgh
```

序列化：Python数据结构向json字符串转换

```python
import json

student = [
            {'name':'lgh', 'age':18, 'flag':False},
            {'name':'lgh', 'age':18}
          ]

json_str = json.dumps(student)
# <class 'str'>
print(type(json_str))
# [{"name": "lgh", "age": 18, "flag": false}, {"name": "lgh", "age": 18}] 
print(json_str) 
```

