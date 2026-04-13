# PKU-CCME-物化实验报告模板（v1.0）

本项目基于北京大学 2025 年秋季学期**物理化学实验**课程要求设计，适用于 LaTeX 格式的物化实验报告撰写，项目作者为 2023 级北大化院本科生张嘉航（`zhangjh@stu.pku.edu.cn`）。

## 使用说明

请下载整个文件夹后再使用，不要只保留 `main.tex`，否则可能缺少样式文件、参考文献或图片资源。

## 文件结构

```text
PKU-CCME-物化实验报告模板/
├── main.tex                 主文档入口
├── config.tex               宏包加载与通用配置
├── pku-phychem-report.sty   模板样式文件
├── reference.bib            参考文献数据库
└── logo_of_PKU.png          封面图片资源
```

## 编译环境

建议使用 `XeLaTeX + Biber` 进行编译。

- 如有引用文献，推荐的编译顺序为：

```text
xelatex -> biber -> xelatex -> xelatex
```

- 如果文档中使用了 `minted` 代码环境，还需要在编译时启用 `-shell-escape`。

## 编译示例

在项目根目录下，可以使用下面的命令编译：

```bash
xelatex -interaction=nonstopmode -shell-escape main.tex
biber main
xelatex -interaction=nonstopmode -shell-escape main.tex
xelatex -interaction=nonstopmode -shell-escape main.tex
```

## 许可与使用

本模板仅供课程作业与个人学习使用，严禁任何形式的商业用途。若用于公开发布或再次分发，请保留原始目录结构，并确保所有依赖文件完整。
