# ik-flow
针对IKUAIOS V4.0的分流插件，还在疯狂进化中
还没整理好，内测企鹅群：808942972


<img width="2010" height="1433" alt="简易UI界面" src="https://github.com/user-attachments/assets/f5c745ce-21b1-4de2-b1cd-abc5408cefb6" />

v1.3.7 测试版:
- 修复简版面板 204 空响应导致更新订阅/切换节点/切换全局卡住
- 测速/更新订阅增加超时与进度提示, 不再无限等待
- 面板/高级面板改用同源后端, 支持宿主端口访问
- fw 先装 fake-ip local 路由再检测 iptables, 诊断补充 legacy 输出
- 透明分流方向待定: 当前内核 iptables nat 后端不可用

v1.3.6 测试版:
- 修复简版面板不显示订阅 provider 节点
- 启动时先启动 mihomo, netdiag 记录启动后状态
- 探针改用 /version, 诊断文件每 60 秒更新
- iptables 自动选择可用后端并验证 nat 链
- 镜像内置 iptables-legacy, 修复 nft 后端不可用导致透明规则不生效

v1.3.5 测试版:
- 修复 mihomo 崩溃后僵尸进程导致不再重启
- 空订阅使用本地占位 URL, 避免 mihomo 启动失败
- 诊断页改用 nc, 并生成 log/netdiag.txt
- 配置模板版本 1.3.4, 旧配置强制迁移

v1.3.4 测试版:
- 修复诊断页占用 9090 导致 mihomo 面板反复重启
- 诊断页改到 9091, 不再因诊断页重启 mihomo
- 首次诊断延迟到 60 秒, 给 mihomo 足够启动时间

v1.3.3 测试版:
- 修复镜像 layer 重复路径导致爱快加载镜像失败
- 镜像 tag 改为 ik-flow:1.3.3, 避免复用历史镜像
- 启动日志增加版本号
- 配置模板版本升到 1.3.3, 旧配置强制迁移
