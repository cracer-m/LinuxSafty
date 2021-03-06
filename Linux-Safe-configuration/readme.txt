
Linux安全配置规范-目录
简介	11
使用对象	12
适用范围	12
规范解释	12
用词约定	12
术语解释	12
1	LINUX基础安全	13
1.1	系统规划	13
1.1.1	规则：必须使用正版的操作系统安装程序	13
1.1.2	规则：合理地对硬盘分区，保护和优化操作系统的安装 -CIS	13
1.1.3	建议：为应用数据划分独立的分区	13
1.1.4	规则：禁止使用供应商、制造商或开发商不再支持的软件、硬件、固件、及它们的部件	13
1.2	最小化安装	14
1.2.1	规则：不使用的软件包不允许存在系统中	14
1.2.2	规则：用于生产环境的系统中不允许保留开发和编译工具	14
1.2.3	规则：操作系统中不允许安装显示安全策略的工具	14
1.2.4	规则：操作系统中不允许存在网络嗅探类的工具	14
1.2.5	建议：在不需要Modems系统中不应默认安装Modems	14
1.3	补丁安装	15
1.3.1	规则：选择最新或最稳定的操作系统，并及时给操作系统安装补丁 -CIS0	15
1.3.2	规则：所有的第三方软件必须使用最新或最稳定的版本，并及时安装补丁	15
2	LINUX系统安全	16
2.1	服务安全	16
2.1.1	规则：应默认删除NIS服务，并移除NIS客户端 -CIS	16
2.1.2	规则：应默认删除telnet服务，并移除telnet客户端 -CIS	16
2.1.3	规则：如果FTP服务不是必须的，应默认关闭 -CIS	17
2.1.4	规则：如果TFTP服务不是必须的，应默认关闭 -CIS	17
2.1.5	建议：如果squid服务不是必须的，应默认关闭 -CIS	17
2.1.6	规则：禁止安装finger服务	18
2.1.7	建议：如果uucp服务不是必须的，应默认关闭	18
2.1.8	规则：需关闭rsh服务，并移除rsh客户端 -CIS	18
2.1.9	建议：如果打印服务不是必须的，应默认关闭 -CIS	18
2.1.10	规则：如果DHCP服务不是必须的，应默认关闭 -CIS	19
2.1.11	规则：如果daytime服务不是必须的，应默认关闭 -CIS	19
2.1.12	规则：需关闭echo和echo-udp服务 -CIS	19
2.1.13	规则：需关闭talk服务并移除talk客户端 -CIS	19
2.1.14	规则：如果xinted服务不是必须的，应默认关闭 -CIS	20
2.1.15	建议：如果NFS服务不是必须的，应默认关闭 -CIS	20
2.1.16	建议：如果SNMP服务不是必须的，应默认关闭 -CIS	20
2.1.17	规则：需关闭autofs服务 -CIS	20
2.1.18	规则：如果邮件传输代理服务不是必须的，应默认关闭 -CIS	21
2.1.19	规则：如果X Windows服务不是必须的，应移除	21
2.1.20	规则：在不使用X Window时应关闭X Font服务	21
2.1.21	规则：应对SSH服务进行加固 -CIS	21
2.1.22	规则：应对系统中使用的包含有不安全配置项的服务进行加固	22
2.1.23	规则：如果系统对外提供远程访问服务，则不同主机上用于服务账号验证的私钥必须不同	23
2.1.24	规则：启用和配置系统的TCP Wrapper，对基于libwrap库的服务建立外部访问的黑白名单机制 -CIS	23
2.1.25	规则：没有用到的服务和协议必须禁用	24
2.1.26	规则：必须限制服务的可达性	25
2.1.27	规则：如果服务不能通过自我配置的方式绑定到它所提供服务的最少必需接口，则必须使用一个本地数据包过滤器规范服务的可访问性	25
2.1.28	规则：管理服务必须仅绑定到一个接口	25
2.1.29	规则：基于网络对系统和服务进行管理的通道必须是安全的	26
2.2	文件及目录安全	26
2.2.1	规则：系统目录必须是安全可靠的，所有系统加固相关的目录和文件的权限参考《Linux文件权限列表》进行配置 -CIS	26
2.2.2	规则：禁止使用setuid或setgid的shell脚本	26
2.2.3	规则：系统中不允许存在无属主的文件 -CIS	27
2.2.4	规则：系统中不允许存在空链接	27
2.2.5	规则：设置系统UMASK -CIS	27
2.2.6	规则：对于数据文件分区、CD/DVD和USB等分区应以noexec方式挂载分区 -CIS	27
2.2.7	规则：对于文件不能修改的分区必须以ro方式挂载	28
2.2.8	规则：对于不需要SUID/SGID的分区必须以nosuid方式挂载 -CIS	28
2.2.9	规则：/var、/tmp目录必须以nodev方式挂载 -CIS	28
2.2.10	规则：系统中不允许存在全局可写文件 -CIS	28
2.2.11	规则：为全局可写目录设置Sticky粘贴位 -CIS	28
2.2.12	规则：只允许root或授权的用户配置at和cron -CIS	29
2.2.13	规则：LD_LIBRARY_PATH变量必须被严格定义	29
2.2.14	规则：用户PATH变量必须被严格定义 -CIS	29
2.2.15	规则：系统中不允许存在以“.”开头的执行文件	29
2.2.16	建议：所有用户的HOME目录不能在系统根目录下	29
2.2.17	规则：所有帐户不应该具有非特定的shell	30
2.2.18	规则：root用户的HOME目录必须是/root	30
2.2.19	规则：所有属主为root用户的目录需设置严格的访问权限	30
2.2.20	建议：移除对不需要的文件系统类型的挂载支持 -CIS	30
2.3	认证及授权安全	31
2.3.1	规则：FTP\TELNET\SSH\GUI等提供交互界面的服务，登录之前的欢迎屏幕必须包含最少量的信息 -CIS0	31
2.3.2	规则：FTP\TELNET\GUI \SSH等提供交互界面的服务，登录失败提供最小的帮助信息	31
2.3.3	规则：FTP\TELNET\GUI\SSH等提供交互界面的服务，成功登录后，显示用户之前登录信息	31
2.3.4	规则：设置会话超时时间	31
2.3.5	规则：创建Warning Banners, Banner中必须删除操作系统版本信息 -CIS0	32
2.3.6	规则：登录失败一定次数后锁定账号 -CIS0	32
2.3.7	规则：设置用户账号口令的复杂度 -CIS	32
2.3.8	规则：用户在口令重置后首次登录须强制更改口令	33
2.3.9	规则：厂商提供的缺省口令或密码必须及时更改	33
2.3.10	建议：设置口令有效期 -CIS	33
2.3.11	建议：设置帐户有效期 -CIS	34
2.3.12	建议：用户的口令必须用强哈希算法进行加密 -CIS0	34
2.3.13	建议：限制su权限的使用 -CIS	34
2.3.14	规则：对账号最小化授权，所有进程必须以所需的最小权限启动	35
2.3.15	规则：去除系统中不需要的帐户	35
2.3.16	规则：禁止使用root帐户进行远程接入系统 -CIS	35
2.3.17	规则：确保只有root才是系统的超级用户，确保系统中各系统账号的UID必须不同 -CIS	35
2.3.18	规则：默认情况下，为每个用户账号分配一个唯一的主要组	35
2.3.19	规则：确保系统组的成员资格仅限于系统帐户和系统管理员	36
2.4	内核安全	36
2.4.1	规则：执行堆栈必须受到保护，以防止遭受缓冲区溢出这类的攻击	36
2.4.2	规则： ASLR功能（地址空间布局随机化）增强漏洞攻击防护能力 -CIS	36
2.4.3	规则：对core dump功能的使用进行限制 -CIS	36
2.4.4	规则：禁用IP转发功能 -CIS	37
2.4.5	规则：禁止IP源路由 -CIS	37
2.4.6	规则：IP欺骗防护 -CIS	37
2.4.7	规则：禁止系统响应广播请求 -CIS	37
2.4.8	规则：禁止ICMP重定向接收 -CIS	38
2.4.9	规则：防止ICMP重定向发给别的系统 -CIS	38
2.4.10	规则：防止ICMP重定向从默认网关接受 -CIS	38
2.4.11	规则：确保伪造的ICMP包被丢弃 -CIS	39
2.4.12	建议：记录所有欺骗的包、源路由包和发给系统的重定向包 -CIS	39
2.4.13	建议：关闭tcp_timestamps	39
2.4.14	建议：除非需要，关闭ARP代理	39
2.4.15	规则：加大从客户端连接请求等候确认的连接数，以防止受到SYN flooding攻击 -CIS	40
2.4.16	规则：设置TIME_WAIT  TCP协议等待时间	40
2.4.17	规则：必须停用对系统操作所不需要的功能，必须停用所操作的软件和硬件的未用功能	40
3	LINUX审计及防护安全	42
3.1	审计安全	42
3.1.1	规则：必须记录所有与认证相关的事件 -CIS	42
3.1.2	规则：记录守护进程产生的DEBUG日志	42
3.1.3	规则：记录cron守护进程产生的日志	42
3.1.4	建议：应将操作系统日志发送至外部服务器单独存储，确保日志不被篡改 -CIS	43
3.1.5	规则：“emergency”优先级的事件必须要重定向到本地日志文件，并在控制台上显示	43
3.1.6	规则：就所有的后台应用程序而言（除了e-mail和认证），具有“info”优先级的事件必须重定向到本地日志文件中	44
3.1.7	规则：设备内核事件必须要重定向到本地日志文件并在控制台上显示	44
3.1.8	规则：邮件和认证设备事件必须被重定向到本地受限访问的日志文件上	44
3.1.9	规则：需保证syslog-ng或rsyslog服务已启用 -CIS	45
3.1.10	建议：重要事件的任何变化，都需要记录到日志中	45
3.1.11	建议：时钟必须同一个可信的和精确时间源同步的 -CIS	45
3.1.12	建议：日志文件必须要集中放置在特定的目录下	45
3.2	防护安全	46
3.2.1	规则：禁止通过键盘（CTRL＋ALT＋DEL）进行重启	46
3.2.2	建议：关闭SysRq键的使用	46
3.2.3	规则：确保在单用户模式下需要输入root密码 -CIS0	46
3.2.4	建议：设置EEPROM/BIOS密码，及时更新BOIS版本	46
3.2.5	建议：设置Grub密码 -CIS	46
3.2.6	建议：使用Iptables过滤网络包 -CIS	47
3.2.7	建议：linux系统需部署完整性校验工具 -CIS	47
3.2.8	建议：系统必须提供安全措施来处理过载情况	47
3.2.9	建议：静态地配置服务器的所有接口的IPv4和IPv6地址	49
3.2.10	规则：动态增长的内容必须不影响系统的功能	49
4	引用CIS规范	50
5	参考规范	57
5.1	CIS_DISTRIBUTION_INDEPENDENT_LINUX_BENCHMARK_V1.0.1.PDF       01-31-2017	57
5.2	CIS_RED_HAT_ENTERPRISE_LINUX_6_BENCHMARK_V2.0.2.PDF      01-31-2017	57
5.3	CIS_RED_HAT_ENTERPRISE_LINUX_7_BENCHMARK_V2.1.1.PDF      01-31-2017	57
5.4	CIS_SUSE_LINUX_ENTERPRISE_11_BENCHMARK_V2.0.0.PDF      12-07-2016	57
5.5	CIS_SUSE_LINUX_ENTERPRISE_12_BENCHMARK_V2.0.0.PDF      12-07-2016	57
5.6	UNIX TECHNICAL SECURITY STANDARD ISSUE 8.5. BRITISH TELECOMMUNICATIONS PLC	57
5.7	UNIX TECHNICAL SECURITY STANDARD. ISSUE10, BRITISH TELECOMMUNICATIONS PLC	57
5.8	SECURITY REQUIREMENT OPERATING SYSTEMS. VERSION 2.0. DEUTSCHE TELEKOM GROUP	57
5.9	SECURITY REQUIREMENT UNIX SERVERS. VERSION 2.0. DEUTSCHE TELEKOM GROUP	57
6	附录	58
6.1	方案及指导书	58
6.1.1	SuSe Linux安全解决方案——iptables防火墙配置指导书	58
6.1.2	SuSe Linux安全解决方案——文件完整性校验检查方案	58
6.1.3	使用sudo为用户最小化授权解决方案	58
6.1.4	Linux安全应用指导书	58
6.1.5	Linux文件权限列表	59
6.1.6	Linux不安全服务加固指导	59
6.1.7	syslog-ng及syslog配置指导	59
6.2	LINUX系统帐户说明	59


Linux安全应用指导规范-目录
简介	6
使用对象	6
适用范围	6
指导解释	6
用词约定	6
术语解释	7
1	权限管理	8
1.1	权限最小化	8
1.1.1  禁止直接使用root账号登录Linux系统	8
1.1.2  除有明确特权需求，应用程序应以非root账号运行	9
1.1.3  采用不同权限的帐号运行不同的应用并对帐号进行权限分离	9
1.1.4  在运行时有特权需求的程序，在特权操作完后如后续无特权需求，必须使用setuid放弃特权	10
1.1.5  使用sudo机制代替以root帐号登录运行特权程序的方式。	11
1.1.6  应对允许使用su到root帐号的用户进行明确授权，非授权用户不能切换到root	11
1.1.7  使用POSIX Capabilities功能避免直接使用root权限	12
1.2	文件和目录权限	14
1.2.1	系统中禁止有无主文件存在	14
1.2.2  除有明确需求，应删除文件不必要的setuid和setgid位	14
1.2.3	应为系统用户设置缺省的umask值	15
1.2.4  使用特殊属性位Sticky位对共享目录权限进行控制	16
1.2.5  利用特殊文件属性Append-only位保护系统命令行历史日志文件，防止内容被篡改	16
2	访问控制	18
2.1	自主访问控制	18
2.1.1  使用POSIX ACL进行更细粒度的访问控制	18
2.2	强制访问控制	20
2.2.1  Linux系统上应安装强制访问控制系统作为应急的安全访问控制手段	20
3	记录和审计	22
3.1	监测、记录和审计	22
3.1.1	启用inotify监控机制，以文件系统事件进行安全监控	22
3.1.2	使用Auditd组件对系统中的重要目录或文件进行审计	24
4	认证	26
4.1	口令和账号	26
4.1.1  使用shadow套件对系统账号口令进行分离保护	26
4.1.2	Linux系统必须使用shadow套件对当前暂时不使用的账号进行锁定或登录限制	27
4.1.3	使用shadow套件对系统口令的时效进行限制	29
4.2	可插拔认证模块（PAM）	29
4.2.1	使用PAM模块增强认证管理	29
5	文件系统保护	31
5.1	日志文件保护	31
5.1.1  应将操作系统日志发送至外部服务器单独存储，确保日志不被篡改	31
5.2	文件系统加密	31
5.2.1	对含有重要信息的文件目录或分区进行加密处理	31
5.3	分区和挂载	32
5.3.1	对于系统中的重要目录必须根据存储目的不同进行分区隔离	32
5.3.2	使用fstab对外接、日志存储分区进行访问控制。	32
5.3.3	禁用自动工具对移动存储设备进行挂载	33
6	网络防护	34
6.1	网络防护能力	34
6.1.1  使用sysctl工具增强系统网络防护能力	34
6.1.2  使用iptables对系统中不使用的端口进行限制	35
6.2	限制网络服务	35
6.2.1  远程访问需使用SSH取代telnet	35
6.2.2  系统中不应安装不安全的传统网络服务	35
7	漏洞攻击防护	37
7.1	地址随机化	37
7.1.1  使用Linux自带的ASLR功能（地址空间布局随机化）增强漏洞攻击防护能力	37
7.2	数据执行防护	37
7.2.1  系统必须使用DEP防护手段提升漏洞攻击防护能力	37
7.2.2  使用栈保护机制	38
7.3	增强性安全防护	39
7.3.1  使用Grsecurity增强Linux系统的安全防护能力	39
7.3.2  使用PaX提升系统攻击防护能力	40
8	完整性保护	43
8.1	文件完整性检查	43
8.1.1  使用IMA工具对系统文件的完整性进行检查	43
9	安全隔离和容器	44
9.1	安全隔离	44
9.1.1  对于开放给第三方的shell环境，应使用隔离技术对其可访问的系统资源进行隔离	44
9.1.2  对于系统中运行的第三方应用，需使用控制组或容器等技术手段将其于系统关键资源进行隔离。	46
10	其他	47
10.1	额外系统功能限制	47
10.1.1  对core dump功能的使用进行限制	47
10.1.2  关闭SysRq键的使用	47
10.1.3  应对bootloader开启引导装载密码	48
10.1.4  使用ulimit工具限制用户可以打开文件个数	48
11	设计样例	50
