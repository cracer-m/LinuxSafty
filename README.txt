# LinuxSafty

Linux安全管理技术（目录：ManagementTechnology）主要分为三个层面
    一、管理层安全
      管理层主要描述如何通过管理制度确保人员正确并安全的使用产品，降低人为因素给产品带来的安全威胁。
      分为组织和过程、账户和权限管理、日志检查和稽核、补丁管理、系统备份。
    二、系统层安全
      系统层安全是Linux安全的核心，主要包括操作系统层面采用的各种安全技术。
      分为七大模块：
        1.系统层安全架构
        2.身份标识与鉴别
        3.安全协议
        4.自主访问控制
        5.强制访问控制
        6.内存客体重用
        7.主机防火墙
      系统层安全维护分为：
        1、系统层账户清单
        2、账户口令维护
        3、系统服务安全维护
        4、日志审计系统维护
        5、认证与授权维护
        6、文件权限维护
        7、内核参数维护
    三、网络层安全
      网络层安全分为防火墙规则配置、远程接入控制两个模块；远程接入控制主要是SSH远程接入的安全维护

Linux安全配置规则（目录：Linux-Safe-configuration）内有两个指导文档、一个文件权限列表与sudo安全配置规范(防止越权）：
    Linux安全配置规范
    Linux安全应用指导规范
    文件权限列表（Linux_File_Permission_List.txt）
    sudo安全配置规范

防火墙配置与维护（目录：iptables）

Linux主机本地信息自动采集工具LinEnum
        copy from GItHub：
        https://github.com/rebootuser/LinEnum
        Example: ./LinEnum.sh -s -k keyword -r report -e /tmp/ -t
        主要功能：
        1.内核和发行版本
        2.系统信息:
        主机名
        3.网络信息:
        IP
        路由信息
        DNS服务器信息
        4.用户信息:
        当前用户信息
        最近登录用户
        枚举所有用户，包括uid/gid信息
        列举root账号
        检查/etc/passwd中的hash
        当前用户操作记录 (i.e .bash_history, .nano_history etc.)
        5.版本信息:Sudo/MYSQL/Postgres/Apache
