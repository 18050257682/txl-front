# 通讯录管理系统开发环境配置

### 开发环境设置

#### Java开发工具包（JDK）安装
确保所有必要的软件版本兼容，并配置环境变量。

## MySQL数据库管理系统安装
在本地或云服务器上创建MySQL数据库实例。

## 数据库设计
设计合适的数据库模式来存储联系人信息。

### 联系人表创建
创建联系人表，包括姓名、电话号码等字段。

## 前后端分离设计模式
系统采用前后端分离的设计模式。

### 前端界面
前端界面采用Vue.js和Element UI框架实现动态渲染。

## 功能描述

### 添加联系方式
前端提供输入新联系人信息的表单。在用户提交表单之前，前端会执行数据验证。验证后，前端使用Axios库向后端API发送POST请求，携带联系人数据。成功添加后，前端应从后端检索最新的联系人列表并更新显示。

### 删除联系信息
前端在每行联系人信息旁边提供一个删除按钮。点击后，使用Element UI弹出确认对话框。用户确认删除后，前端收集要删除的联系人ID，并调用后端删除接口。成功删除后，前端会从列表中删除相应的联系人条目。

### 修改联系方式
前端为用户提供编辑联系人信息的界面，显示当前联系人的详细信息并允许用户修改。用户完成修改后，前端收集新数据并通过Axios向后端发送PUT请求。更新成功后，前端页面应显示更新的联系人信息。

### 搜索联系信息
前端提供一个搜索框。用户输入搜索条件后，前端调用后端的搜索接口，并在列表中显示搜索结果。

### 联系人列表分页
前端在联系人列表底部实现分页控制，显示当前页码和总页数。当用户点击页码或使用翻页按钮时，前端调用后端接口请求相应页面的数据并更新列表显示。
# 路由器功能

#### 路由白名单
定义了一个路由白名单，以确定哪些路由可以在不登录的情况下访问。

### 路由保护
创建路由保护，以便在路由跳转之前执行检查和操作，例如检查用户是否已登录以及是否需要加载用户菜单。

### 动态路由加载
定义了`loadMenus`函数用于从后端API检索用户菜单列表，并根据菜单动态添加路由。

### 路由检查
定义了`hashRoute`函数来检查系统中是否存在路由。

### 路由添加
定义了`addRoute`函数，将获得的路由添加到Vue路由器。

### 功能描述
此代码用于处理前端应用程序中与路由相关的逻辑，包括权限检查、路由的动态加载以及路由跳转前的状态管理。

---

# 界面模板

### 基本结构
此代码是用于构建网页的基本HTML模板。它包含一些基本的HTML结构和元数据，以及在构建过程中用于动态填充的特定配置和占位符。

---

# 功能模块

### Axios请求
此代码是一系列使用Axios进行HTTP请求的函数，用于与后端API交互并实现用户身份验证、菜单管理、角色管理、用户管理和日志查看等功能。每个函数都返回一个AxiosPromise，这意味着它们可用于异步操作，例如在Vue.js等前端框架中处理异步数据检索。
