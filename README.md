# agile-api-test
Agile项目管理平台接口自动化测试框架
# Agile 项目管理平台 - 接口自动化测试框架

## 项目简介

基于 pytest + Allure 的接口自动化测试框架，支持 CI/CD 持续集成。

## 技术栈

| 技术 | 用途 |
|------|------|
| Python 3.11 | 编程语言 |
| pytest | 测试框架 |
| Allure | 测试报告 |
| GitHub Actions | CI/CD |
| Docker Compose | 环境部署 |
| MySQL 8 | 数据库 |

## 项目结构
api/           # 接口封装层
testcases/     # 测试用例层
data/          # 测试数据（YAML）
utils/         # 工具类
config/        # 配置文件
reports/       # 测试报告

## 快速开始

### 本地运行

```bash
# 1. 安装依赖
pip install -r requirements.txt

# 2. 启动后端（Docker）
docker compose up -d

# 3. 运行测试
pytest testcases/ -v --alluredir=reports/allure-results

# 4. 生成报告
allure serve reports/allure-results
CI/CD 流水线
每次 git push 自动触发：
编译后端
启动 MySQL + 后端服务
运行接口测试
生成 Allure 报告
部署到 GitHub Pages
报告地址
点击查看最新测试报告
测试覆盖模块
[x] 用户模块（登录、用户信息）
[x] 项目模块（项目 CRUD）
[x] 迭代模块（Sprint 管理）
[x] 故事模块（Story 管理）
[x] 任务模块（Task 管理）
[x] 看板模块（Kanban 看板）
[x] 权限模块（PO/SM/Dev 角色）
