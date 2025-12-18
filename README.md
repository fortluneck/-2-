# 数字化转型指数分析平台

一个基于Streamlit的数字化转型指数分析应用，用于展示和分析企业的数字化转型指数数据。

## 功能特点

### 数据筛选与查询
- **年份选择**：支持选择1999-2023年的数据，默认显示最近5年
- **行业筛选**：按行业名称筛选企业数据
- **股票代码查询**：支持输入多个股票代码进行精确查询
- **企业名称查询**：支持企业名称的模糊匹配

### 数据可视化
- **数字化转型指数分析**：展示企业的数字化转型指数及相关指标
- **地区分布分析**：基于企业所在省份的数据分析
- **行业趋势分析**：不同行业的数字化转型趋势对比
- **企业对比分析**：支持多企业的数字化转型指数对比

### 主题切换
- 支持亮色/暗色模式切换，提升用户体验

## 项目结构

```
digital-transformation-app/
├── 新建文件夹/
│   ├── digital_transformation_app.py    # Streamlit应用主文件
│   ├── merge_all_years.py               # 合并所有年份数据的脚本
│   ├── merge_with_industry.py           # 与行业数据合并的脚本
│   ├── requirements.txt                 # 项目依赖
│   └── *.py                             # 其他工具脚本
├── 生成app资料/
│   ├── 1999-2023年数字化转型指数合并表.xlsx    # 合并后的完整数据
│   └── *.xlsx                           # 各年份的原始数据
└── README.md                            # 项目说明文档
```

## 技术栈

- **Streamlit**：Web应用框架
- **Pandas**：数据处理
- **Matplotlib/Seaborn**：数据可视化
- **Plotly**：交互式图表
- **Folium**：地图可视化

## 安装与部署

### 本地运行

1. 克隆或下载项目代码

2. 安装依赖：
```bash
pip install -r 新建文件夹/requirements.txt
```

3. 运行应用：
```bash
cd 新建文件夹
streamlit run digital_transformation_app.py
```

4. 在浏览器中访问：http://localhost:8501

### GitHub部署

可以使用以下平台部署到GitHub：

1. **Streamlit Community Cloud**
   - Fork项目到GitHub
   - 访问[Streamlit Community Cloud](https://streamlit.io/cloud)
   - 连接GitHub账户并部署应用

2. **Heroku**
   - 创建Procfile和runtime.txt
   - 部署到Heroku

3. **Vercel**
   - 创建vercel.json配置文件
   - 部署到Vercel

## 数据说明

- **数据源**：1999-2023年企业年报技术关键词统计
- **主要指标**：数字化转型指数（0-100分）
- **数据维度**：年份、行业、企业、股票代码、省份

## 使用指南

1. **数据筛选**：使用左侧边栏进行数据筛选
2. **查看图表**：在主页面查看各种数据可视化图表
3. **导出数据**：支持将筛选结果导出为CSV或Excel文件
4. **主题切换**：点击右上角按钮切换亮色/暗色模式

## 开发说明

### 主要脚本功能

- `digital_transformation_app.py`：Streamlit应用主文件，包含所有UI和交互逻辑
- `merge_all_years.py`：合并1999-2023年的所有指数结果表
- `merge_with_industry.py`：将指数数据与行业数据合并
- `classify_tech_keywords.py`：技术关键词分类和词频统计

### 数据更新

1. 将新的年份数据添加到`生成app资料/`文件夹
2. 运行`merge_all_years.py`合并新数据
3. 运行`merge_with_industry.py`更新行业信息
4. 重启Streamlit应用

## 注意事项

- 应用需要访问本地文件系统，确保文件路径正确
- 首次运行可能需要较长时间加载数据
- 建议使用Python 3.8+版本

## 许可证

MIT License
