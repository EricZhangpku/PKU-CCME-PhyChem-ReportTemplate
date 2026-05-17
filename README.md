# PKU-CCME-物化实验报告模板（v1.0）

本项目基于北京大学 2025 年秋季学期**物理化学实验**课程要求设计，适用于 LaTeX 格式的物化实验报告撰写，项目作者为 2023 级北大化院本科生张嘉航。如有问题请在 GitHub [提交 Issue](https://github.com/EricZhangpku/PKU-CCME-PhyChem-ReportTemplate/issues) 告知作者。

## 文件结构 & 使用说明

```text
PhyChemReport/
├── main.tex                 主文档入口
├── main.pdf                 编译后的 pdf 示例（包含使用说明）
├── config.tex               宏包加载与通用配置
├── pku-phychem-report.sty   模板样式文件
├── reference.bib            参考文献数据库
└── logo_of_PKU.png          封面图片资源
```

下载**整个 `PhyChemReport` 文件夹**后即可使用，使用过程中务必**保持以上文件结构完整并处于同一目录下**，否则可能缺少样式文件、参考文献或图片资源而无法编译。

### 下载方式

- **克隆整个仓库**：

  ```bash
  git clone https://github.com/EricZhangpku/PKU-CCME-PhyChem-ReportTemplate.git
  ```

  克隆后 `PhyChemReport` 文件夹位于仓库根目录下。

- **仅下载 `PhyChemReport` 文件夹**（二选一）：
  - 通过 [GitHub 页面](https://github.com/EricZhangpku/PKU-CCME-PhyChem-ReportTemplate) 进入 `PhyChemReport` 文件夹，逐文件点击下载；
  - 使用 `svn` 命令只导出该文件夹：
    ```bash
    svn export https://github.com/EricZhangpku/PKU-CCME-PhyChem-ReportTemplate.git/trunk/PhyChemReport
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

本模板仅供课程作业与个人学习使用，严禁任何形式的商业用途。若用于公开发布或再次分发，请保留原始目录结构，并确保所有依赖文件完整。使用过程中如发现问题，欢迎[提交 Issue](https://github.com/EricZhangpku/PKU-CCME-PhyChem-ReportTemplate/issues) 联系作者指正。
