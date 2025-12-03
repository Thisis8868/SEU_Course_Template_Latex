# 📘 SEU_Course_Template_Latex
东南大学课程论文 LaTeX 模板（SEU Report 模板）。
本模板适用于东南大学课程平时论文、期末论文、课程报告等文档撰写。

## 📂 目录结构

```
SEU_Course_Template_Latex
│── main.tex               # 主文档
│── SEUReport.sty          # 主要样式文件（封面、文字格式、页眉等）
│── reference.bib          # 参考文献文件（BibTeX）
│── README.md              # 项目说明
│
└── figures/               # 图片、校徽等资源
     ├── seu_logo.svg
     └── seu_logo_notitle.svg
```

---

## ✨ 功能概览

### 完整封面页

* 自动生成课程报告封面
* 支持替换东南大学校徽
* 学院、班级、学号、姓名等字段可在 `SEUReport.sty` 中统一配置

### 自动目录页

* 一键 `\tableofcontents` 生成

### 默认设置

* 页边距 2.5 cm
* 中文宋体，英文字体 Times New Roman
* 行距、页眉、标题均已优化

---

## 🛠 使用说明

### 1. 克隆项目

```bash
git clone https://github.com/Thisis8868/SEU_Course_Template_Latex.git
```

### 2. 编译方式（推荐）

使用 **XeLaTeX**（适配中文字体），编译顺序：

```bash
xelatex main.tex
bibtex main.aux
xelatex main.tex
xelatex main.tex
```

或直接在 [Overleaf](https://www.overleaf.com/latex/) 打开即可。

---

## ✏ 主要可配置内容（SEUReport.sty）

* 封面标题、学院、班级、学号、姓名
* 封面校徽（可替换为其他文件）
* 页眉内容
* 字体/字号
* 文本框样式
* autoref 的中文前缀（图/表/式）

示例（封面 Logo 设置）：

```latex
\includesvg[width=0.6\textwidth]{figures/seu_logo}
```

若你想使用其他校徽，只需替换对应 svg 文件即可。

---

## 🖼 图片示例

插入校徽示例代码：

```latex
\begin{figure}[!htbp]
    \centering
    \includesvg[width=.5\textwidth]{figures/seu_logo}
    \caption{校标}
    \label{fig:seu_logo}
\end{figure}
```

---

## 📚 引用文献（BibTeX）

在正文中：

```latex
如文献所示 \cite{OFDMAbackscatter}。
```

引用后会自动加入参考文献区。

---

## 🚨 注意事项

* SVG 加载需要 `\usepackage{svg}`（模板已内置）
* 编译必须使用 **XeLaTeX**
* 使用 `\autoref{...}` 引用时请确保 label 与引用一致，例如：

```latex
\label{fig:seu_logo}
\autoref{fig:seu_logo}
```

---

## ⭐ 致谢

本模板改写自多个高校课程模板：

* 中国科学院大学课程模板（jweihe）
* 北京大学课程论文模板（Shawn Wang）
* 西北工业大学课程论文模板（SeddonShen）
* 上海交通大学课程论文模板（Jiazhen-Lei）

感谢这些优秀模板作者的贡献。

---

## 📬 联系方式

如有问题欢迎提 Issue 或 PR！
如果模板对你有帮助，欢迎给我一个 ⭐ Star！

GitHub 地址：
👉 [https://github.com/Thisis8868/SEU_Course_Template_Latex](https://github.com/Thisis8868/SEU_Course_Template_Latex)


