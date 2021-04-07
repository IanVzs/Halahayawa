# Halahayawa
How long have you worked.
## 进度
### 2020.04.03:
最基本功能已经实现啦.还有些丑,堪堪能用.
![v0.1界面展示](https://github.com/IanVzs/Halahayawa/blob/main/showme_v0.1.png "su mua~")

## 使用
### 源码
```bash
git clone git@github.com:IanVzs/Halahayawa.git
cd Halahayawa/
mkdir env
python3 -m venv ./env
source ~/env/bin/activate
pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
python main.py
```
可根据实际情况进行适当调整

### 可执行程序
## 原理
检测鼠标以及键盘移动/输入,判断正在工作中.

## 实现
### 编程语言
Python(不会卡的太死lol)

### 所用库/包
- PyQt5: 实现简单界面(不想用其它包,卡的比较死^_^.....弃用,因为其授权协议问题,虽然我的是MIT不要紧,但是用了它我的协议就被升级...虽然PySide2也会升级本项目授权,但比PyQt5要好.)
- PySide2: 实现简单界面(不想用其它包,卡的不死^_^, 有MIT的实现方式欢迎改造)
- pynput: 监控鼠标键盘
- sqlalchemy: 数据库ORM,手拼字符累了,试试新东西
- yapf: 代码格式化 
#### yapf
查看工具格式将修改哪些地方 和 应用修改, 配置文件`.style.yapf`
```bash
python3 -m yapf . -d -r
python3 -m yapf . -i -r
```
如果代码中某一段不想用yapf格式化
```python
# yapf: disable
a = {
    "666": "999",
    "999": "666"
}
mat = [
    [1, 2, 3, 4, 5],
    [1, 2, 3, 4, 5]
]
# yapf: enable
```
或
```python
mat = [
    [1, 2, 3, 4, 5],
    [1, 2, 3, 4, 5]
] # yapf: disable
```


## 包含信息
- 当前单次连续工作时长 历史最大/最小
- 当前单日工作总时长 历史最大/最小
- 当前单周总工作时长 历史最大/最小
- 当前单月总工作时长 历史最大/最小
- 跨度: 天/周/月/年数

## 中断机制
- 单次: 鼠标/键盘超过一分钟无任何响应(现在演示为10s)
- 单日24/0时
- 单月/周/年 1号/星期1/1月1号0时

## 提醒
### 连续工作N分钟/小时放送提醒
pass
### 周中连续N天超过N小时提醒
pass
### 月中连续N天/M周超过C/Cc小时提醒
pass
