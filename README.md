# 安全网络加密磁盘系统

基于 Python 的端到端加密网络磁盘系统，采用自定义安全传输协议。

## 功能特性

- 🔐 端到端加密存储（零知识架构）
- 🔑 双重登录方式（口令 / Email验证码）
- 👥 群组协作与加密共享
- 🛡️ 自定义安全传输协议
- 🎨 现代化 PyQt6 界面

## 安装

```bash
pip install -r requirements.txt
```

## 本地开发运行

### 启动服务端
```bash
python -m server.main
```

### 启动客户端
```bash
python -m client.main
```

## 分布式部署与打包

项目支持将客户端和服务端部署在不同的机器上。

### 1. 自动化打包 (Windows)
运行以下脚本生成独立运行文件夹：
```bash
python scripts/build.py
```
打包产物将位于 `dist/SecureDiskClient` 和 `dist/SecureDiskServer`。

### 2. 配置与连接
- **服务端**: 首次运行后会生成 `server.ini`。修改 `[Network] host = 0.0.0.0` 以允许外部连接。
- **客户端**: 在登录界面打开“服务器设置”，输入服务端的 IP 地址和端口。系统会自动记录历史服务器列表。

## 技术栈

- Python 3.8+
- PyQt6 (GUI)
- pycryptodome (加密算法)
- SQLite (数据库)
