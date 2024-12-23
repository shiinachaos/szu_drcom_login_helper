# szudrcomCLI
## 简介
szudrcomCLI是一个帮助无GUI的Linux设备登录深圳大学校园网的工具。

## 依赖环境
1. `bash`
2. `curl`
3. `wget`
3. `iproute2`

## 使用说明

### 基本用法
运行以下命令查看帮助信息：

```bash
./szudrcomCLI help
```

### 配置登录信息
配置登录凭据，在当前目录生成登陆程序`./szudrcomlogin`

```bash
./szudrcomCLI config -l [LOCATION] -u [USER_ID] -p [PASSWORD]
```

参数说明：
- `-l, --location`：位置类型，可选值为 `dormitory`（宿舍）或 `office`（办公室）。
- `-u, --user`：用户 ID，仅支持数字。
- `-p, --pass`：用户密码，仅支持包含数字和英文字母的密码，包含特殊字符串的密码无法使用，建议修改密码。

示例：
```bash
./szudrcomCLI config -l dormitory -u 12345678 -p pass123
./szudrcomCLI config -l office -u 12345678 -p pass123
```

### 登录网络
执行以下命令以登录网络：

```bash
bash ./szudrcomlogin
```
