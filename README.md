## 这是自己创建的针对vue-admin-template整理的模板
针对panjiacheng的模板做了一定的优化，也做了一些配置的注释，方便后面学习查看
画了一张整体的架构还有流程图，放在根目录下，随时更新
## Build Setup

```bash
# 克隆项目
git clone https://github.com/PanJiaChen/vue-admin-template.git

# 进入项目目录
cd vue-admin-template

# 安装依赖
npm install

# 建议不要直接使用 cnpm 安装以来，会有各种诡异的 bug。可以通过如下操作解决 npm 下载速度慢的问题
npm install --registry=https://registry.npm.taobao.org

# 启动服务
npm run dev
```

浏览器访问 [http://localhost:9528](http://localhost:9528)

## 发布

```bash
# 构建测试环境
npm run build:stage

# 构建生产环境
npm run build:prod
```

## 其它

```bash
# 预览发布环境效果
npm run preview

# 预览发布环境效果 + 静态资源分析
npm run preview -- --report

# 代码格式检查
npm run lint

# 代码格式检查并自动修复
npm run lint --fix
```

## Nprogress 使用
配置在路由守卫中，只在页面跳转时候加载

## loading使用
不建议放在路由拦截器中处理，会在多个请求同时进行时候出现loading混乱

## .editorconfig IDE格式配置
- Webstore支持同步修复，vscode须额外安装并启用 EditorConfig for VS Code 插件， 可在保存时按配置自动修复

1、root<boolean>  :  是否是顶级配置文件，设置为true的时候才会停止搜索.editorconfig文件
2、charset<"latin" | "utf-8" | "utf-8-bom" | "utf-16be" | "utf-16le">     :    文件编码格式
3、indent_style<"tab" | "space">    ：  缩进方式
4、indent_size<number>    ：    缩进大小
5、end_of_line<"lf" | "cr" | "crlf">    ：    换行符类型
6、insert_final_newline<boolean>   ：     是否让文件以空行结束
7、trim_trailing_whitespace<boolean>  ：   是否删除行尾空格 
8、max_line_length<number>    ：    最大行宽。

## 动态路由
## 功能

```
- 登录 / 注销

- 权限验证
  - 页面权限
  - 指令权限
  - 权限配置
  - 二步登录

- 多环境发布
  - dev
  - sit
  - stage
  - prod

- 全局功能
  - 国际化多语言
  - 多种动态换肤
  - 动态侧边栏（支持多级路由嵌套）
  - 动态面包屑
  - 快捷导航(标签页)
  - Svg Sprite 图标
  - 本地/后端 mock 数据
  - Screenfull全屏
  - 自适应收缩侧边栏

- 编辑器
  - 富文本
  - Markdown
  - JSON 等多格式

- Excel
  - 导出excel
  - 导入excel
  - 前端可视化excel
  - 导出zip

- 表格
  - 动态表格
  - 拖拽表格
  - 内联编辑

- 错误页面
  - 401
  - 404

- 組件
  - 头像上传
  - 返回顶部
  - 拖拽Dialog
  - 拖拽Select
  - 拖拽看板
  - 列表拖拽
  - SplitPane
  - Dropzone
  - Sticky
  - CountTo

- 综合实例
- 错误日志
- Dashboard
- 引导页
- ECharts 图表
- Clipboard(剪贴复制)
- Markdown2html
```
