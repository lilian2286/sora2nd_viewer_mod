# Trails in the Sky the 2nd Chapter - Viewer Mod 发布包

## 内容
1. **MOD 加载器**: xinput1_4.dll + xinput1_4_looseload.dll (散装文件加载核心, 必需)
2. **静名(chr5117) 追加到 viewer 角色列表** + 7 套可换服装:
   - 靜名（泳裝）/ 靜名（便服）/ 靜名（另類配色）/ 靜名（失控）/ 靜名（泡澡服）/ 靜名（兔女郎／銷售用）/ 靜名（界服）
   - 含唇彩修复(与游戏原生静名一致) + 收刀动作修复(刀从右手入鞘) + 全套动作/贴图/佩刀(equ8117)
3. **界之轨迹全员 roster** (idx554~601): 范恩、静名系、亚妮艾丝(含服装/DLC变体)等约45名角色追加到 viewer 列表
   - 含各自模型/动作/贴图/共享贴图组(kai_t*/woman01_*/man01_*/com_*)与所需 shader permutation
4. **亚妮艾丝(chr8186)专项修复**:
   - 琴穿模修复: 头部不再加载本作的曼陀林道具
   - 收刀修复: 收起武器动画期间武器在右手可见(按 Kai 战斗链 #114 配方), 拔武器有变形动画
5. **表**: t_viewer.tbl(144行) / t_name.tbl(1636行)
6. **shader**: 25 个 fxo (唇彩2 + 界轨材质 permutation 23)
7. **防盗版声明文件**: Kirara_更新发布地址.html / Kirara_免费分享_请勿在任何渠道受骗付费购买.txt / Kirara_制作_请勿转载_免责声明.txt / Kirara_QQ群二维码.jpg
   - 本Mod免费分享, 请勿在任何渠道受骗付费购买; 作者B站主页: https://space.bilibili.com/1318661; QQ交流群「台面下的某群」(群号 2159081126, 见发布页二维码)
   - 加载器内置防盗版检查: 四个声明文件缺失任何一个或内容被修改, 游戏启动时弹窗提示并拒绝运行

## 安装
将本目录内所有文件按相对路径复制到游戏根目录（与 asset、table_tc、script_tc、pac 同级）覆盖即可。
- 两个 xinput*.dll 复制到游戏根目录（与游戏 exe 同级）
- **四个 Kirara_* 声明文件必须一并复制到游戏根目录**——缺失任何一个或内容被修改, 游戏将弹窗提示并无法启动（防盗版机制）
- mod 生效时游戏根目录会生成 console.log 与 sheath_hook.log（调试日志, 可随时删除; 设环境变量 SHEATH_HOOK_NO_PROBE=1 可关闭探针日志）

## 卸载
删除以下文件即可（游戏原版 PAC 内容未被覆盖, 全部为新增散装; 仅 t_viewer/t_name 两张表为覆盖, 需自备份还原）:
- 游戏根目录: xinput1_4.dll, xinput1_4_looseload.dll, Kirara_更新发布地址.html, Kirara_免费分享_请勿在任何渠道受骗付费购买.txt, Kirara_制作_请勿转载_免责声明.txt, Kirara_QQ群二维码.jpg
- asset\common\model\ 与 model_info\: chr5117*, chr8151~8155, chr8158, chr8159, chr8160~8207, equ8117*, equ8160*, equ8177*, equ8186*
- script_tc\ani\: chr5117.dat, chr8151~8155/8158/8159.dat, chr8160.dat, chr8177.dat, chr8186.dat
- asset\dx11\image\: chr5117_*, chr8160~8207_*, equ8117_*, equ8160_*, equ8177_*, equ8186_*, kai_*, woman01_*, man01_*, com_f01_*, com_m01_*, common_w01_face_q, chr5001_00, chr5001_c02_03*, chr5001_c61_04_n/p
- asset\dx11\shader\: 25 个 chr_cloth#/chr_hair#/chr_skin# fxo
- table_tc\t_viewer.tbl, t_name.tbl

## 文件统计
- 2667 个文件, 1,509,249,901 字节 (1439.3 MiB)
- 明细与校验值见 manifest.json

## 已知限制
- 赛车皇后两套(静名 chr8156/chr8157)因引擎代差(Kai DLC材质组合在Sky无shader permutation)未包含
- viewer 中部分角色的动作缺失时自动回退通用动作库(设计内行为)
- 本包不含游戏本体替换内容(黎恩注入线 chr0123 等)
