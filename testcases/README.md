# openRuyi BaseOS 测试用例文档

> 组织方式：按 13 个需求域平铺
> 每个用例一个文档，文档名 = 用例标识.md；元数据用表格组织，正文为描述 + 前置条件 + 编号测试步骤 + 编号预期结果。

## 用例索引（59 个）

| 用例编号 | 用例标题 | 需求编号 | 需求标题 | 优先级 | 自动化等级 | 适用平台/发布件 | 脚本路径 | 状态 |
|---|---|---|---|---|---|---|---|---|
| [TC-GATE-001](smoke/TC-GATE-001.md) | 启动->登录->基础命令可用 | [GATE-001](<../requirements/openRuyi BaseOS 产品需求.md>) |  | 门禁100% | 半自动 | 各发布件形态（oci/镜像/安装产物） | tests/smoke/ | 草稿 |
| [TC-TR-001-01](functional/kernel/TC-TR-001-01.md) | 内核更新后原内核保留、系统持续可用 | [TR-001](<../requirements/openRuyi BaseOS 产品需求.md>) | 内核更新不会移除当前使用的内核以及模块 | P2 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/kernel/boot/ | 草稿 |
| [TC-TR-001-02](functional/kernel/TC-TR-001-02.md) | 使用旧内核重启后功能正常 | [TR-001](<../requirements/openRuyi BaseOS 产品需求.md>) | 内核更新不会移除当前使用的内核以及模块 | P2 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/kernel/boot/ | 草稿 |
| [TC-TR-001-03](functional/kernel/TC-TR-001-03.md) | 触发内核保留上限清理时最旧运行内核保留 | [TR-001](<../requirements/openRuyi BaseOS 产品需求.md>) | 内核更新不会移除当前使用的内核以及模块 | P2 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/kernel/boot/ | 草稿 |
| [TC-TR-002-01](functional/kernel/TC-TR-002-01.md) | 内核更新后新内核安装完整、引导项生成 | [TR-002](<../requirements/openRuyi BaseOS 产品需求.md>) | 内核更新后增加对应引导项 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/kernel/boot/ | 草稿 |
| [TC-TR-002-02](functional/kernel/TC-TR-002-02.md) | 使用新内核重启后功能正常 | [TR-002](<../requirements/openRuyi BaseOS 产品需求.md>) | 内核更新后增加对应引导项 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/kernel/boot/ | 草稿 |
| [TC-TR-003-01](functional/system/TC-TR-003-01.md) | systemd 服务启停/禁用 | [TR-003](<../requirements/openRuyi BaseOS 产品需求.md>) | 服务正常启动停止/禁用 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/system/systemd/ | 草稿 |
| [TC-TR-004-01](functional/system/TC-TR-004-01.md) | 基本关机与重启 | [TR-004](<../requirements/openRuyi BaseOS 产品需求.md>) | 基本关机重启 | P1 | 手动 | 安装/镜像产物（oci 发布件除外） | tests/functional/system/systemd/ | 草稿 |
| [TC-TR-005-01](functional/system/TC-TR-005-01.md) | 时间同步正常 | [TR-005](<../requirements/openRuyi BaseOS 产品需求.md>) | 时间同步正常 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/system/time/ | 草稿 |
| [TC-TR-006-01](functional/system/TC-TR-006-01.md) | 系统日志正常收集 | [TR-006](<../requirements/openRuyi BaseOS 产品需求.md>) | 系统日志正常收集 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/system/log/ | 草稿 |
| [TC-TR-007-01](functional/system/TC-TR-007-01.md) | root 修改 hostname | [TR-007](<../requirements/openRuyi BaseOS 产品需求.md>) | root 用户可以修改 hostname | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/system/config/ | 草稿 |
| [TC-TR-008-01](functional/system/TC-TR-008-01.md) | 修改当前用户密码 | [TR-008](<../requirements/openRuyi BaseOS 产品需求.md>) | 应当能够正常修改当前用户密码 | P1 | 手动 | rva20/rva23 · 安装/镜像产物 | tests/functional/system/account/ | 草稿 |
| [TC-TR-009-01](functional/package-mgmt/TC-TR-009-01.md) | rpm/dnf 命令可执行 | [TR-009](<../requirements/openRuyi BaseOS 产品需求.md>) | 包管理功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/package-mgmt/ | 草稿 |
| [TC-TR-009-02](functional/package-mgmt/TC-TR-009-02.md) | 安装与依赖解析 | [TR-009](<../requirements/openRuyi BaseOS 产品需求.md>) | 包管理功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/package-mgmt/ | 草稿 |
| [TC-TR-009-03](functional/package-mgmt/TC-TR-009-03.md) | 卸载与依赖保护 | [TR-009](<../requirements/openRuyi BaseOS 产品需求.md>) | 包管理功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/package-mgmt/ | 草稿 |
| [TC-TR-009-04](functional/package-mgmt/TC-TR-009-04.md) | 升级与回退 | [TR-009](<../requirements/openRuyi BaseOS 产品需求.md>) | 包管理功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/package-mgmt/ | 草稿 |
| [TC-TR-009-05](functional/package-mgmt/TC-TR-009-05.md) | 仓库元数据正确性 | [TR-009](<../requirements/openRuyi BaseOS 产品需求.md>) | 包管理功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/package-mgmt/ | 草稿 |
| [TC-TR-009-06](functional/package-mgmt/TC-TR-009-06.md) | 异常包操作与错误码 | [TR-009](<../requirements/openRuyi BaseOS 产品需求.md>) | 包管理功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/package-mgmt/ | 草稿 |
| [TC-TR-010-01](functional/toolchain/TC-TR-010-01.md) | gcc 编译链接与运行 | [TR-010](<../requirements/openRuyi BaseOS 产品需求.md>) | gcc 编译软件 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/toolchain/ | 草稿 |
| [TC-TR-010-02](functional/toolchain/TC-TR-010-02.md) | 语法错误诊断 | [TR-010](<../requirements/openRuyi BaseOS 产品需求.md>) | gcc 编译软件 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/toolchain/ | 草稿 |
| [TC-TR-011-01](functional/pkgs/TC-TR-011-01.md) | tar 归档/列表/解包 | [TR-011](<../requirements/openRuyi BaseOS 产品需求.md>) | 归档压缩与基础工具功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/pkgs/tar/ | 草稿 |
| [TC-TR-011-02](functional/pkgs/TC-TR-011-02.md) | gzip/xz/zstd 压缩解压 | [TR-011](<../requirements/openRuyi BaseOS 产品需求.md>) | 归档压缩与基础工具功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/pkgs/{gzip,xz,zstd}/ | 草稿 |
| [TC-TR-011-03](functional/pkgs/TC-TR-011-03.md) | coreutils/util-linux 文件操作 | [TR-011](<../requirements/openRuyi BaseOS 产品需求.md>) | 归档压缩与基础工具功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/pkgs/{coreutils,util-linux}/ | 草稿 |
| [TC-TR-011-04](functional/pkgs/TC-TR-011-04.md) | 异常场景容错 | [TR-011](<../requirements/openRuyi BaseOS 产品需求.md>) | 归档压缩与基础工具功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/pkgs/ | 草稿 |
| [TC-TR-012-01](functional/storage-fs/TC-TR-012-01.md) | ext4/xfs 创建挂载修复 | [TR-012](<../requirements/openRuyi BaseOS 产品需求.md>) | 存储与文件系统功能 | P1 | 手动 | RISC-V 平台 + 存储设备及配置 | tests/functional/storage-fs/fs/ | 草稿 |
| [TC-TR-012-02](functional/storage-fs/TC-TR-012-02.md) | LVM 卷管理 | [TR-012](<../requirements/openRuyi BaseOS 产品需求.md>) | 存储与文件系统功能 | P1 | 手动 | RISC-V 平台 + 存储设备及配置 | tests/functional/storage-fs/lvm/ | 草稿 |
| [TC-TR-012-03](functional/storage-fs/TC-TR-012-03.md) | 软 RAID 创建组装恢复 | [TR-012](<../requirements/openRuyi BaseOS 产品需求.md>) | 存储与文件系统功能 | P1 | 手动 | RISC-V 平台 + 多块存储设备 | tests/functional/storage-fs/raid/ | 草稿 |
| [TC-TR-012-04](functional/storage-fs/TC-TR-012-04.md) | NFS/CIFS 客户端 | [TR-012](<../requirements/openRuyi BaseOS 产品需求.md>) | 存储与文件系统功能 | P1 | 手动 | RISC-V 平台 + 可达的共享服务器 | tests/functional/storage-fs/net-fs/ | 草稿 |
| [TC-TR-012-05](functional/storage-fs/TC-TR-012-05.md) | 升级/迁移数据一致性 | [TR-012](<../requirements/openRuyi BaseOS 产品需求.md>) | 存储与文件系统功能 | P1 | 手动 | RISC-V 平台 + 存储设备及配置 | tests/functional/storage-fs/ | 草稿 |
| [TC-TR-013-01](functional/network/TC-TR-013-01.md) | 网络配置/DNS/路由与重启保持 | [TR-013](<../requirements/openRuyi BaseOS 产品需求.md>) | 网络基础功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/network/config/ | 草稿 |
| [TC-TR-013-02](functional/network/TC-TR-013-02.md) | 连通性与故障恢复 | [TR-013](<../requirements/openRuyi BaseOS 产品需求.md>) | 网络基础功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/network/config/ | 草稿 |
| [TC-TR-013-03](functional/network/TC-TR-013-03.md) | 防火墙规则生效 | [TR-013](<../requirements/openRuyi BaseOS 产品需求.md>) | 网络基础功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/network/firewall/ | 草稿 |
| [TC-TR-014-01](functional/network/TC-TR-014-01.md) | wifi 连接成功且重登免密 | [TR-014](<../requirements/openRuyi BaseOS 产品需求.md>) | 使用 wifi 联网 | P2 | 手动 | 具备 wifi 硬件的平台 | tests/functional/network/wifi/ | 草稿 |
| [TC-TR-014-02](functional/network/TC-TR-014-02.md) | wifi 错误密码拒绝 | [TR-014](<../requirements/openRuyi BaseOS 产品需求.md>) | 使用 wifi 联网 | P2 | 手动 | 具备 wifi 硬件的平台 | tests/functional/network/wifi/ | 草稿 |
| [TC-TR-015-01](functional/network/TC-TR-015-01.md) | ssh 有效凭据建立会话 | [TR-015](<../requirements/openRuyi BaseOS 产品需求.md>) | 正常通过 ssh 连接 openruyi 机器 | P2 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/network/ssh/ | 草稿 |
| [TC-TR-016-01](functional/security-auth/TC-TR-016-01.md) | TLS/证书认证 | [TR-016](<../requirements/openRuyi BaseOS 产品需求.md>) | 安全与认证基础功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/security-auth/ | 草稿 |
| [TC-TR-016-02](functional/security-auth/TC-TR-016-02.md) | SSH 认证与凭据策略 | [TR-016](<../requirements/openRuyi BaseOS 产品需求.md>) | 安全与认证基础功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/security-auth/ | 草稿 |
| [TC-TR-016-03](functional/security-auth/TC-TR-016-03.md) | PAM 认证授权 | [TR-016](<../requirements/openRuyi BaseOS 产品需求.md>) | 安全与认证基础功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/security-auth/ | 草稿 |
| [TC-TR-016-04](functional/security-auth/TC-TR-016-04.md) | 审计记录 | [TR-016](<../requirements/openRuyi BaseOS 产品需求.md>) | 安全与认证基础功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/security-auth/ | 草稿 |
| [TC-TR-016-05](functional/security-auth/TC-TR-016-05.md) | 磁盘加密 | [TR-016](<../requirements/openRuyi BaseOS 产品需求.md>) | 安全与认证基础功能 | P0 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/security-auth/ | 草稿 |
| [TC-TR-017-01](functional/install/TC-TR-017-01.md) | calamares 安装器启动 | [TR-017](<../requirements/openRuyi BaseOS 产品需求.md>) | 安装器能够运行 | P1 | 手动 | 图形界面平台 | tests/functional/install/installer/ | 草稿 |
| [TC-TR-018-01](functional/install/TC-TR-018-01.md) | 安装磁盘选择 | [TR-018](<../requirements/openRuyi BaseOS 产品需求.md>) | 安装器可以选择磁盘 | P2 | 手动 | 多磁盘 + 图形界面平台 | tests/functional/install/installer/ | 草稿 |
| [TC-TR-019-01](functional/install/TC-TR-019-01.md) | 安装用户登录 | [TR-019](<../requirements/openRuyi BaseOS 产品需求.md>) | 安装器创建的用户可以正常登录 | P1 | 手动 | 图形界面平台 | tests/functional/install/installer/ | 草稿 |
| [TC-TR-020-01](functional/install/TC-TR-020-01.md) | 安装失败返回错误链接 | [TR-020](<../requirements/openRuyi BaseOS 产品需求.md>) | 安装器安装失败后返回错误链接 | P2 | 手动 | 图形界面平台 | tests/functional/install/installer/ | 草稿 |
| [TC-TR-021-01](functional/install/TC-TR-021-01.md) | 安装后磁盘自动扩容 | [TR-021](<../requirements/openRuyi BaseOS 产品需求.md>) | 安装完成磁盘正常扩容 | P2 | 手动 | rva20/rva23 · 安装/镜像产物 | tests/functional/install/installer/ | 草稿 |
| [TC-TR-022-01](functional/install/TC-TR-022-01.md) | cloud-init 有 data iso 启动服务 | [TR-022](<../requirements/openRuyi BaseOS 产品需求.md>) | Cloud-init 正常使用 | P1 | 半自动 | service 发布件 | tests/functional/install/cloud-init/ | 草稿 |
| [TC-TR-022-02](functional/install/TC-TR-022-02.md) | cloud-init 无 data iso 不启动 | [TR-022](<../requirements/openRuyi BaseOS 产品需求.md>) | Cloud-init 正常使用 | P1 | 半自动 | service 发布件 | tests/functional/install/cloud-init/ | 草稿 |
| [TC-TR-023-01](functional/virtualization/TC-TR-023-01.md) | 虚拟机生命周期 | [TR-023](<../requirements/openRuyi BaseOS 产品需求.md>) | 虚拟化基础功能 | P1 | 半自动 | RISC-V 宿主平台 | tests/functional/virtualization/ | 草稿 |
| [TC-TR-023-02](functional/virtualization/TC-TR-023-02.md) | 客户机设备识别 | [TR-023](<../requirements/openRuyi BaseOS 产品需求.md>) | 虚拟化基础功能 | P1 | 半自动 | RISC-V 宿主平台 | tests/functional/virtualization/ | 草稿 |
| [TC-TR-023-03](functional/virtualization/TC-TR-023-03.md) | 虚拟磁盘读写与重启一致 | [TR-023](<../requirements/openRuyi BaseOS 产品需求.md>) | 虚拟化基础功能 | P1 | 半自动 | RISC-V 宿主平台 | tests/functional/virtualization/ | 草稿 |
| [TC-TR-023-04](functional/virtualization/TC-TR-023-04.md) | 虚拟网络与异常诊断 | [TR-023](<../requirements/openRuyi BaseOS 产品需求.md>) | 虚拟化基础功能 | P1 | 半自动 | RISC-V 宿主平台 | tests/functional/virtualization/ | 草稿 |
| [TC-TR-024-01](functional/container/TC-TR-024-01.md) | 镜像拉取校验解包 | [TR-024](<../requirements/openRuyi BaseOS 产品需求.md>) | 容器运行时功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/container/ | 草稿 |
| [TC-TR-024-02](functional/container/TC-TR-024-02.md) | 容器生命周期 | [TR-024](<../requirements/openRuyi BaseOS 产品需求.md>) | 容器运行时功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/container/ | 草稿 |
| [TC-TR-024-03](functional/container/TC-TR-024-03.md) | 容器网络 | [TR-024](<../requirements/openRuyi BaseOS 产品需求.md>) | 容器运行时功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/container/ | 草稿 |
| [TC-TR-024-04](functional/container/TC-TR-024-04.md) | 异常场景与资源清理 | [TR-024](<../requirements/openRuyi BaseOS 产品需求.md>) | 容器运行时功能 | P1 | 半自动 | rva20/rva23 · 安装/镜像产物 | tests/functional/container/ | 草稿 |
| [TC-TR-025-01](functional/debug/TC-TR-025-01.md) | gdb 基础调试 | [TR-025](<../requirements/openRuyi BaseOS 产品需求.md>) | 调试与追踪工具功能 | P2 | 半自动 | 仅 rva20 | tests/functional/debug/ | 草稿 |
| [TC-TR-025-02](functional/debug/TC-TR-025-02.md) | strace 系统调用记录 | [TR-025](<../requirements/openRuyi BaseOS 产品需求.md>) | 调试与追踪工具功能 | P2 | 半自动 | 仅 rva20 | tests/functional/debug/ | 草稿 |
| [TC-TR-025-03](functional/debug/TC-TR-025-03.md) | valgrind 内存检测 | [TR-025](<../requirements/openRuyi BaseOS 产品需求.md>) | 调试与追踪工具功能 | P2 | 半自动 | 仅 rva20 | tests/functional/debug/ | 草稿 |
| [TC-TR-026-01](functional/desktop/TC-TR-026-01.md) | 显示器基础显示 | [TR-026](<../requirements/openRuyi BaseOS 产品需求.md>) | 显示器正常显示 | P2 | 手动 | 具备显示器的平台 | tests/functional/desktop/ | 草稿 |
