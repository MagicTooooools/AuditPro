# AuditPro

    目前项目只是有个框架，期待各位同行加入施工，完善本项目

使用 Go 语言实现的等级保护测评项目，使用 Go 语言编译运行，适用于各平台，各系统

检测的顺序和输出按照规范使用规定的名称输出汇总

```
例：

身份鉴别： 
L3-CES1-01
L3-CES1-02
L3-CES1-03
L3-CES1-04

访问控制：
L3-CES1-05
L3-CES1-06
L3-CES1-07
L3-CES1-08
L3-CES1-09
L3-CES1-10
L3-CES1-11
```

## 目录架构

```
.
├── LICENSE
├── Makefile
├── README.md
├── Scripts
│   ├── Firewall
│   ├── Linux
│   ├── Mac
│   ├── Router
│   ├── Switch
│   └── Windows
├── db
│   └── db.sqlite3
├── go.mod
├── main.go
└── output
```

### 主机部分

- Linux
    Linux 主机的策略检查
- Windows
    Windows 主机的策略检查
- Mac
    Mac 主机的策略检查

### 网络设备部分

- Switch
    交换机设备的自动核查
- Router
    路由器设备的自动核查
- Firewall
    防火墙设备的自动核查

## 数据库

数据库存储内容结构为

| id | 检测名称 | 系统信息 | 安全要求 | 执行的命令 | 输出的结果 | 检测得分 | 截图信息 |   
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | L3-CES1-01 | Linux server 5.15.0-67-generic #74-Ubuntu SMP Wed Feb 22 14:14:39 UTC 2023 aarch64 aarch64 aarch64 GNU/Linux | 应对登陆的用户进行身份标识和鉴别，身份标识具有唯一性，身份鉴别信息具有复杂度要求并定期更换 | 【命令】 | 【结果】 | 【得分】 | 【截图存储】 |

## TODO

- [ ] 通用组件的编写
    - [ ] 检测系统信息
    - [ ] 汇总信息
    - [ ] 输出
        - [ ] 数据库
        - [ ] 文件
            - [ ] Excel
            - [ ] Word

    - [ ] 截图

- [ ] 各个模块的编写
    - [ ] Linux
    - [ ] Windows
    - [ ] Mac
    - [ ] Firewall
    - [ ] Switch
    - [ ] Router

## 协议

MIT 【暂定】