## Hugo Admin

为Hugo提供Web管理界面，提供对文档管理和编辑功能。

### 用户使用流程描述

1. 通过hugo创建静态页面站点

2. 在站点集成Hugo-Admin的静态页面和脚本，使它可通过https://site_name/admin访问，通过oauth2方式登入后台管理系统。

3. 用户登录成功后获得相关权限, 并进入到Hugo-Admin的主界面。

4. 用户可在Hugo-Admin的主界面中可以做：

   * 切换Hugo站点， 可选择的站点由权限管理方配置。

   * 浏览和筛选文档
   * 编辑/预览Markdown文档内容和Front matter
   * 发布和撤销发布文档

### 系统数据流描述

```flow
st=>start: Start:>http://www.google.com[blank]
e=>end:>http://www.google.com
op1=>operation: My Operation
sub1=>subroutine: My Subroutine
cond=>condition: Yes
or No?:>http://www.google.com
io=>inputoutput: catch something...
para=>parallel: parallel tasks

st->op1->cond
cond(yes)->io->e
cond(no)->para
para(path1, bottom)->sub1(right)->op1
para(path2, top)->op1
```

### 功能模块划分：

- 用户权限管理

  - 管理员角色

    包括sites的创建，修改，删除，分配现有的site给普通用户，但不能有管理文档流程的权限

  - 普通角色

    对文档进行查询, 创建，发布，撤销，Front Matter修改等等

- 文档浏览

  - 站点切换
  - 文档列表过滤

- 文档编辑
  - Front matter 编辑
  - Markdown 方式编辑
  - 客户端预览

- Markdown文档的编辑和预览

- Markdown文档发布
- Markdown文档批量发布

- Site管理
  - 创建删除Hugo站点目录, 提交到Git Server
  - 导入导出文档 

### 技术选型

- 数据库：MySQL

  

### 和Hugo交互：



