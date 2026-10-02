# Trails in the Sky the 2nd Chapter - Viewer Mod 发布包

## 内容
1. **MOD 加载器**: xinput1_4.dll + xinput1_4_looseload.dll (散装文件加载核心, 必需)
2. **静名(chr5117) 追加到 viewer 角色列表** + 7 套可换服装:
   - 靜名（泳裝）/ 靜名（便服）/ 靜名（另類配色）/ 靜名（失控）/ 靜名（泡澡服）/ 靜名（兔女郎／銷售用）/ 靜名（界服）
   - 含唇彩修复(与游戏原生静名一致) + 收刀动作修复(刀从右手入鞘)
3. **表**: t_viewer.tbl(99行) / t_name.tbl(1591行)

## 安装
将本目录内所有文件按相对路径复制到游戏根目录（与 asset、table_tc、script_tc 同级）覆盖即可。
- 两个 xinput*.dll 复制到游戏根目录（与游戏 exe 同级）
- mod 生效时游戏根目录会生成 console.log（可查看加载记录）

## 卸载
删除以下文件即可（游戏原版内容未被覆盖修改，全部为新增散装）:
- 游戏根目录: xinput1_4.dll, xinput1_4_looseload.dll
- asset\common\model\chr8151~8155, chr8158, chr8159 (+_face/_m_wait)
- asset\common\model_info\chr8151~8155, chr8158, chr8159
- script_tc\ani\chr8151~8155, chr8158, chr8159, chr5117.dat
- asset\dx11\image\ mod 贴图: chr5117_c0*/c1*/c7*, chr5001_c02_*, woman01_face_q, common_w01_face_q
- asset\dx11\shader\chr_skin#1a70c371.fxo, chr_skin#bdbffe42.fxo
- table_tc\t_viewer.tbl, t_name.tbl (原版表需自备份还原)

## 文件统计
- 66 个文件, 98,822,247 字节 (94.2 MiB)
- 明细与校验值见 manifest.json

## 已知限制
- 赛车皇后两套(chr8156/chr8157)因引擎代差(Kai DLC材质组合在Sky无shader permutation)未包含
- viewer 中静名的部分动作缺失时自动回退女体通用库(设计内行为)
