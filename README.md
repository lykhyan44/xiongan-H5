
# 雄安智慧政务

## 相关人员
1. 项目总负责人: 邹鹏
2. 项目经理: 邹鹏 王志超
3. UI/UE: 吴瑶（UE）
4. 事项H5前端开发人员: 李晓涛 李维刚 刘宁
5. RD: 王志超（事项目录对接人） 金文启（受理审批对接人） 思源公司 邬玉焦（公共服务）
6. 客户端: ios-游时军，申元江; android-李昕宇 王晨晨
7. 运维: 测试环境--余检; 正式环境:
8. 测试: 陈道明（测试负责人） 分行同事
9. 需求：刘苏阳（需分）
10. 业务：杨姝瑶（后台配置/实施经理）
11.公众号H5开发人员：唐鑫 段贝贝 张东辉

## 安装
下载代码, 用cnpm安装包(有些包在阿里私有npm)


## 登录账号
1. 生产环境测试账号: 个人-`xiongan001`,  `xiongan002`; 法人-`faren1` `faren2`，密码都是: `a11111`
## 事项id
1. 预先核准 matterid: F8C299927814C1AA3BB9499B253518D4
2. 企业、事业单位、社会团体等投资建设的固定资产投资项目核准 36EF62F1A12C105DA8A1350BCB5F1279
3. 企业、事业单位、社会团体等投资建设的固定资产投资项目备案（试行） 6CBB65564794A499EA2345C45D758B32
4. 报废汽车备案 6220C844BDC50AD67FE7B0B0AEC13533

## APP打开的路由
```
// 个人
http://211.143.49.163:18087/dist/index.html#/companionPageOne?userid=xiongan001&token=f680f5f275fd4180992caae2cef3849a&username=%E6%A8%8A%E6%98%8E%E7%BE%A4&phone=15910439071&cardNo=500118200102068748&companyName=null&socialNumber=null&matterid=acbaad403a3f4bde86cf8a41a7d10d38
```

```
// 法人
http://localhost:8088/#/companionPageOne?userid=d262e3f12f3d480380515a9b6f4e0dde&token=32d63df219bf4e85a84abe18ba387542&username=cs03&phone=133233&cardNo=139223322111112333&companyName=null&socialNumber=91110115WNRW1W8CG7&matterid=1710212734001&applyerType=2&certificateType=001
```

## 打包发布
运行`npm run build`, 将dist目录打包发给运维


## 不同环境后台地址
1. 测试环境：http://211.143.49.163:18088
2. 互联网环境：http://144.7.127.26:8090

## 路由
1. 通用审批办事指南页: companionPageOne
2. 阅读须知页: readingNotes
3. 表单填写页: waterIntaking
4. 材料上传页: materialUpload
5. 材料递交页: subMaterials
6. 结果物领取页: resultCollection
7. 快递: MyExpress
8. 一件事: onething/index
9. 健步走: walking

## 重要接口

### 事项目录：
1. ~~~`gml/matterindex10002`~~~ `tysl/matterindex10002`: 获取办事指南详情
### 受理审批-通用审批提交
1. ~~~`tysl/sl0003`~~~ `tysl/sl10003`: 暂存草稿
2. `tysl/sl0010`: 获取草稿列表
3. `tysl/sl0011`: 获取草稿详情
4. `tysl/sl0032`: 提交接口清单
### 受理审批-我的办事  TODO
1. 公共服务() TODO 需要去对接局委
1.1 `/gsp/mng30011`：查询公共服务列表
1.2 `/gsp/mng90034`：查询事项办事进度
1.3 `/gsp/mng60010`：查询事项材料列表
1.4 `/gsp/appForm00002`：查询事项提交信息
1.5 `/gsp/mng60007`：办事评价提交接口
2. 行政审批() TODO
2.1 `tysl/sl0005`:出具受理通知书前允许申请人撤销办件
2.2 `tysl/sl0006`:根据用户要素和查询条件查询办事列表
2.3 `tysl/sl0007`:根据办件编号查询办件详情（办件编号，申请人登录状态时使用，接口要校验Token）
2.4 `tysl/sl0009`:查询申请人为当前办件上传的附件材料清单
2.5 `tysl/sl0010`:我的草稿列表查询
2.6 `tysl/sl0031`:删除草稿
2.7 `tysl/sl0040`:查询该办件的完整的业务流程及当前所处流程环节(一般分申报、预审、受理、审查、决定、原件核验、制证、出件等环节
3. 一件事() TODO
3.1 `tysl/yjs10010`:办件列表
3.2 `tysl/yjs10011`:办件详情
3.3 `tysl/yjs10012`:办件附件列表
3.4 `tysl/yjs10013`:办件流转痕迹
### 行政分类 原生+公众号
1. `gml/matterindex10006`:查询部门列表,查询实施清单机构列表
2. `gml/matterYN10001`:查询部门下的事项列表

### 一件事办事 TODO
1. `tysl/yjs10001`: 一件事场景列表查询
2. `tysl/yjs10002`:一件事场景详情查询
3. `tysl/yjs10004`: 一件事申报
3. `tysl/yjs10006`:一件事材料列表
4. `tysl/eform0001` : 自定义表单查询
