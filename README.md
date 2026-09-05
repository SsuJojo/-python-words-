# Python 单词背记系统

一个用 Python 编写的命令行单词学习小工具，也是我较早期的 Python 练习项目之一。

项目把单词学习拆成“学习 → 英选中 → 中选英 → 错题重做 → 推进学习天数”的完整循环，不依赖第三方库，直接在终端运行。

## 功能

- 从 `English.txt` 与 `Chinese.txt` 读取中英文词表
- 每天按进度学习一组新单词
- 英文选中文四选一练习
- 中文选英文四选一练习
- 自动记录答错的单词并再次练习
- 使用 `day.env` 保存当前学习进度
- 完成一轮后可选择继续下一轮
- 支持 `Ctrl+C` 退出

## 学习流程

```text
读取词表与学习天数
        ↓
学习当天单词
        ↓
英文 → 中文选择题
        ↓
错题重新练习
        ↓
中文 → 英文选择题
        ↓
错题重新练习
        ↓
学习天数 +1
```

## 运行

要求：Python 3。

```bash
git clone https://github.com/SsuJojo/-python-words-.git
cd -python-words-
python main.py
```

项目只使用 Python 标准库，无需额外安装依赖。

## 数据文件

```text
-python-words-/
├── main.py       # 主程序
├── English.txt   # 英文词表
├── Chinese.txt   # 中文释义
├── day.env       # 当前学习进度
└── 论文.md       # 项目相关说明材料
```

`English.txt` 与 `Chinese.txt` 按行对应：同一行的英文和中文会组成一组词义映射。

## 项目状态

**Completed learning demo / 已完成的命令行学习 Demo。**

这是一个早期项目，代码风格和交互方式保留了当时学习 Python 时的写法。它不追求现代 GUI 或复杂算法，重点是用最基础的 Python 完成一个能够持续使用的学习闭环。

如果继续迭代，比较自然的方向包括：错题持久化、随机复习、词库导入、间隔重复算法以及图形界面。
