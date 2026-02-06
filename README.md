# 编程练习项目

## 项目概述

这是一个包含C++和Python编程练习的综合项目，涵盖了面向对象编程、运算符重载、文件操作、机器学习和网络爬虫等多个主题。项目中的每个文件都是一个独立的编程练习，展示了不同的编程概念和技术。

## 项目结构

```
├── .vscode/             # VS Code配置文件
├── Microsoft/           # Windows PowerShell相关文件
├── 14.6.cpp             # C++编程练习
├── 14.7.cpp             # C++编程练习
├── 14.11.cpp            # C++编程练习
├── Account.cpp          # 账户类测试程序
├── Account.h            # 账户类定义
├── Account2.cpp         # 账户类测试程序（版本2）
├── CHugeInt.cpp         # 大整数类实现
├── Package.cpp          # 包裹类测试程序
├── Package.h            # 包裹类定义
├── Package2.cpp         # 包裹类测试程序（版本2）
├── animal.cpp           # 动物类实现
├── circle.cpp           # 圆类及其派生类实现
├── codes.py             # 加密函数实现
├── complex.cpp          # 复数类实现
├── data.csv             # 数据文件
├── dna.py               # DNA序列分类实现
├── examcode.py          # 考试代码
├── file.cpp             # 文件读取示例
├── hardware.dat         # 硬件数据文件
├── hzic.py              # 百度地图全景图片爬取和拼接
├── introhomework.py     # 介绍性作业
├── manager.cpp          # 管理器实现
├── musiclearning.py     # 音乐学习相关代码
├── newmast.dat          # 新主数据文件
├── nodes.py             # 节点相关代码
├── oldmast.dat          # 旧主数据文件
├── overload.cpp         # 运算符重载示例
├── pipes.py             # 管道相关代码
├── random100.tsp        # 随机TSP问题数据
├── template.cpp         # 模板示例
├── test.txt             # 测试文本文件
└── trans.dat            # 交易数据文件
```

## C++编程练习

### 面向对象编程

1. **账户类系统** (`Account.h`, `Account.cpp`)
   - 实现了 `Account` 基类及其派生类 `SavingsAccount` 和 `CheckingAccount`
   - 展示了继承、多态和虚函数的使用
   - 测试了账户的存款、取款和利息计算功能

2. **包裹类系统** (`Package.h`, `Package.cpp`)
   - 实现了 `Package` 基类及其派生类 `TwoDayPackage` 和 `OvernightPackage`
   - 展示了继承、多态和虚函数的使用
   - 测试了不同包裹的费用计算功能

3. **几何类系统** (`circle.cpp`)
   - 实现了 `circle` 基类及其派生类 `sphere` 和 `cylinder`
   - 展示了继承、多态和虚函数的使用
   - 测试了圆、球体和圆柱体的面积和体积计算功能

4. **动物类系统** (`animal.cpp`)
   - 实现了 `Animal` 基类及其派生类 `Cat`、`Dog` 和 `Tiger`
   - 展示了继承、多态和虚函数的使用
   - 测试了不同动物的叫声功能

### 其他C++练习

1. **复数类** (`complex.cpp`)
   - 实现了复数类及其加减乘运算符重载
   - 测试了复数的运算功能

2. **文件操作** (`file.cpp`)
   - 实现了简单的文件读取功能
   - 测试了从文本文件中读取内容并输出到控制台的功能

3. **大整数类** (`CHugeInt.cpp`)
   - 实现了大整数类及其相关功能

4. **运算符重载** (`overload.cpp`)
   - 展示了运算符重载的使用

## Python编程练习

1. **加密函数** (`codes.py`)
   - 实现了一个简单的加密函数，对输入的整数进行加密
   - 测试了加密功能

2. **DNA序列分类** (`dna.py`)
   - 使用KNN分类器对DNA序列进行分类
   - 提取了DNA序列的碱基频率作为特征
   - 测试了分类功能

3. **百度地图全景图片爬取和拼接** (`hzic.py`)
   - 从百度地图API获取分割成32张的全景图片碎片
   - 将这些碎片拼接成一张完整的全景图片
   - 测试了爬取和拼接功能

4. **其他Python练习**
   - `introhomework.py`: 介绍性作业
   - `musiclearning.py`: 音乐学习相关代码
   - `nodes.py`: 节点相关代码
   - `pipes.py`: 管道相关代码

## 如何运行

### C++程序

1. 使用C++编译器（如g++）编译C++文件
2. 运行编译生成的可执行文件

例如，运行Account.cpp：

```bash
g++ Account.cpp -o Account.exe
./Account.exe
```

### Python程序

1. 确保安装了Python 3.x
2. 安装必要的依赖（如numpy, sklearn等）
3. 运行Python文件

例如，运行codes.py：

```bash
python codes.py
```

## 依赖

### C++程序
- C++编译器（如g++）

### Python程序
- Python 3.x
- numpy
- sklearn（用于dna.py）
- requests（用于hzic.py）
- PIL（用于hzic.py）
- tqdm（用于hzic.py）

## 总结

这个项目是一个综合性的编程练习集合，涵盖了C++和Python的多个编程主题。通过这些练习，可以巩固面向对象编程、运算符重载、文件操作、机器学习和网络爬虫等编程技能。每个练习都是独立的，可以单独运行和学习。

## 注意事项

- 部分Python程序可能需要安装额外的依赖包
- 部分程序可能需要特定的数据文件才能正常运行
- 部分程序可能仅适用于特定的操作系统环境
