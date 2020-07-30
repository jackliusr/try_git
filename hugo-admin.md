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

由于目前的静态文件生成器大部分不支持增量编译过程， 大量文件时候， 会有比较长的延迟生产文件。这样导致Site 预览的体验很差。后台跑一个Hugo 提供预览功能。

<!-- Title: Publish 
User->Backend_Gin:file
Backend_Gin->Hugo:build
Backend_Gin->git: check in newly files -->

