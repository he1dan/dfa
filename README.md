# dfa
scan sensitive word use dfa
```buildoutcfg
__author__ = "Black"
__email__ = "cj194832@163.com"
__version = "V1.0"
```


```python
from app.dfa import DFA

def main():
    """
    主函数入口
    """
    content = """
    毒品包括海洛因，冰毒，大麻等，我国禁止AV，三级片，禁止未成年人吸食毒品，涉黄等行为
    """
    filename = "SensitiveWord.txt"
    dfa = DFA(filename)
    dfa.add_word("毒品")
    print(dfa.dfa(content))


if __name__ == '__main__':
    main()
```
```buildoutcfg
>>> (True, {'三级片', '毒品', '海洛因', '冰毒', '大麻'})
```