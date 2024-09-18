# 工具功能介绍：

* json补全
* 配合流式输出
* 解析markdown格式
* 字段校验

# 效果展示

### **部分输出的**

```
text = '''{"name":"张三", "age":'''print(parse_json_markdown(text))
# {'name': '张三'}
```

**markdown格式**

````
text = '''```json\n{"name":"张三", "age":27'''print(parse_json_markdown(text))
# {'name': '张三', 'age': 27}
````

**多维嵌套**

````
text = '''```json\n{"name":"张三", "age": 27, "爱好": ["羽毛球'''print(parse_json_markdown(text))
# {'name': '张三', 'age': 27, '爱好': ['羽毛球']}
````
