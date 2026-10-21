# 编程练习（C++）

本仓库是一组可单独编译、单独运行的 **C++ 练习**，主题都来自现有源文件：类的继承与多态、运算符重载、文本与二进制文件，以及一道按单位价值选取的贪心。另有若干独立的 Python 脚本（数字变换、分类、整数规划、全景图拼接等），没有统一的构建系统或课程大纲文件。

This repository is a set of standalone C++ exercises—inheritance and polymorphism, operator overloading, text and binary file I/O, and one value-density greedy—plus a few independent Python scripts. There is no shared build system. Descriptions below follow only what the sources actually do.

## C++

| 文件 | 内容 |
| --- | --- |
| `Account.h`、`Account.cpp` | `Account`，以及 `SavingsAccount`、`CheckingAccount`。基类测试存款、取款；储蓄账户按利率计息；支票账户在存取时扣手续费。 |
| `Account2.cpp` | 另一份含 `main` 的程序。用 `Account*` 的 `vector` 读入存取金额，并用 `dynamic_cast` 给储蓄账户计息。不要与 `Account.cpp` 链在一起。 |
| `Package.h`、`Package.cpp` | `Package`、`TwoDayPackage`、`OvernightPackage`，按重量与费率计算运费。 |
| `Package2.cpp` | 另一份含 `main` 的程序。用 `unique_ptr<Package>` 输出寄件人、收件人、运费和合计。不要与 `Package.cpp` 链在一起。 |
| `circle.cpp` | `circle`、`sphere`、`cylinder`。从标准输入读半径与高，输出球和圆柱的表面积、体积（圆周率取 3.14）。 |
| `animal.cpp` | `Animal`、`Cat`、`Dog`、`Tiger`。读入动物名直到空行，分别输出 `meow`、`wang`、`howl`。 |
| `manager.cpp` | 抽象类 `Manager`，派生 `CustManager` 与 `SalesManager`。计算薪资、按薪资降序输出，并再输出不低于平均薪资的记录。 |
| `complex.cpp` | `Complex` 的 `+`、`-`、`*` 和流输出。 |
| `CHugeInt.cpp` | 用字符串保存的大整数，支持与另一个大整数或 `int` 相加，并重载 `<<`。 |
| `overload.cpp` | `String` 的 `<<`：字母按字典序重排后输出，非字母字符留在原位。 |
| `file.cpp` | 从 `test.txt` 按空白分词读入并打印。 |
| `14.7.cpp` | 写出示例 `oldmast.dat`（账号、姓名、余额）和 `trans.dat`（账号、金额）。会覆盖同名文件。 |
| `14.6.cpp` | 按账号把 `oldmast.dat` 与 `trans.dat` 合并为 `newmast.dat`；对不上的交易写到标准错误。 |
| `14.11.cpp` | 以二进制记录维护 `hardware.dat` 中的工具名称、数量和成本，菜单包括初始化、添加、列表、更新和删除。 |
| `I.cpp` | 多组数据。每件物品有重量和价值，在容量限制下按价值/重量从高到低选取，可以只取一部分重量。 |
| `template.cpp` | 未完成片段（`Triangle`、`Square` 的声明，以及几行类型转换记号），不能单独编译。 |

## Python

| 文件 | 内容 |
| --- | --- |
| `codes.py` | 读入一个整数，按千、百、十、个位拆开，每位加 3 后对 9 取余，再按十位、个位、千位、百位的顺序输出。仅用标准库。 |
| `dna.py` | 以内置 DNA 序列的 A/T/C/G 频率为特征，用 `KNeighborsClassifier`（k = 3）预测另外一组序列的类别。依赖 NumPy、scikit-learn。 |
| `musiclearning.py` | 以内置简谱的音高分布、节拍变化和速度为特征，用线性核 `SVC` 预测乐谱类别。依赖 NumPy、scikit-learn。 |
| `introhomework.py` | 对内置的温度—长度数据做线性回归，输出斜率、截距、线胀系数和相关系数，并画拟合图。依赖 NumPy、SciPy、Matplotlib。 |
| `pipes.py` | 用 PuLP 解钢管下料的整数规划：在 4 m、6 m、8 m 需求约束下最小化余料。 |
| `examcode.py` | 用 PuLP 解一份食谱整数规划：在热量、蛋白质、钙和份数上限约束下最小化成本。 |
| `hzic.py` | 按固定 `panoid` 请求百度地图全景接口的 32 块图片，保存到 `img_frag/` 后拼成 `output.jpg`。依赖 requests、NumPy、Pillow、tqdm，并需要能访问该接口。 |
| `nodes.py` | 使用与 `random100.tsp` 相同的 100 个平面坐标，用随机排列画一条闭合折线，保存为 `tsp_route.html`。不读取 `.tsp` 文件，也不求解旅行商问题。依赖 NumPy、folium。 |

## 数据文件

- `test.txt`：`file.cpp` 读取的文本。
- `oldmast.dat`、`trans.dat`、`newmast.dat`：账户主文件与交易；`14.6.cpp` 读取前两个并写出第三个，`14.7.cpp` 会重写前两个。
- `hardware.dat`：`14.11.cpp` 使用的二进制工具库存。
- `random100.tsp`：100 个点的 TSPLIB 风格坐标。仓库里没有读取或求解它的程序；`nodes.py` 只是把同一组坐标写在源码里并随机连线。
- `data.csv`：五所大学的名称、国家和经纬度。当前没有任何程序读取它。

仓库里还有 `.vscode`（其中生成任务指向 Windows 下的 `g++.exe`）、已经编译好的 `.exe`，以及 `Microsoft/Windows/PowerShell/` 下的本机缓存。这些不是练习内容。

## 运行

C++ 源文件各自带有 `main`（`template.cpp` 除外）。头文件与对应的 `.cpp` 放在同一目录即可，例如：

```bash
g++ Account.cpp -o Account
./Account

g++ 14.6.cpp -o match-accounts
./match-accounts
```

`Account2.cpp`、`Package2.cpp` 请单独编译，不要和已有 `main` 的 `Account.cpp`、`Package.cpp` 一起链接。

Python 使用 3.x，依赖见上表，例如：

```bash
python3 codes.py
python3 dna.py
```
