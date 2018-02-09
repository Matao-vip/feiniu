# 飞牛网 — 大润发网上商城 #
***
## 页面命名说明 ##
- index.html === 【首页】
- goodslist.html === 【商品列表页】
- details.html === 【商品详情页】
- car.html === 【购物车页】
- register.html === 【注册页】
- login.html === 【登录页】
## 页面跳转操作介绍 ##
- 首页
	1. 点击任意页面头部飞牛网logo可进入
- 商品列表页	
	1. 点击【首页】- “全部商品分类” - “进口好货、进口食品” 栏可进入
	2. 点击【商品列表页】- “全部商品分类” - “进口好货、进口食品” 栏可进入
	3. 点击【商品详情页】- “全部商品分类” - “进口好货、进口食品” 栏可进入
	4. 点击【商品详情页】- 分类导航中的 “进口好货、进口食品” 处可进入
	5. 点击【购物车页】- “继续购物>>” 可进入
- 商品详情页
	1. 点击【商品列表页】- 列表中的商品 可进入该商品的详情页
	2. 点击【商品列表页】- “浏览记录” 中的商品可进入该商品的详情页
	3. 点击【商品详情页】- 分类导航中的 商品名可进入该商品的详情页
	4. 点击【购物车页】- 商品列表中的 “商品名称” 可进入该商品的详情页
- 购物车页
	1. 点击【首页】- 头部 “我的购物车” 可进入
	2. 点击【首页】- 右侧侧边栏（默认隐藏，滚动一定距离出现） “购物车” 可进入
	3. 点击【商品列表页】- 头部 “我的购物车” 可进入
	4. 点击【商品详情页】- 头部 “我的购物车” 可进入
- 注册页
	1. 点击【首页】- 最顶部 “免费注册” 可进入
	2. 点击【商品列表页】- 最顶部 “免费注册” 可进入
	3. 点击【商品详情页】- 最顶部 “免费注册” 可进入
	4. 点击【购物车页】- 最顶部 “免费注册” 可进入
	5. 点击【登录页】- 登录框中的 “免费注册” 可进入
- 登录页
	1. 点击【首页】- 最顶部 “Hi，请登录” 可进入
	2. 点击【商品列表页】- 最顶部 “Hi，请登录” 可进入
	3. 点击【商品详情页】- 最顶部 “Hi，请登录” 可进入
	4. 点击【购物车页】- 最顶部 “Hi，请登录” 可进入
	5. 点击【注册页】- 注册框中的 “现在就‘登录’” 可进入
	6. 成功登录后，点击各页面最顶部的 “退出” 可进入

## 页面效果/功能介绍 ##
#### 头部 ####
	* 注：由于各页面都存在头部，因此单独拿出来介绍	
	1. 头部可选择“送货至”的城市，城市列表通过ajax请求生成，数据文件为lib/data/region.json 
	2. 头部的“我的购物车”中的数量会根据用户添加的商品数实时更新
	3. 首页的“全部商品分类”二级导航默认显示，其他页面的默认不显示，hover上去显示
	4. 登录成功后在各页面显示用户名
#### 首页 ####
	1. banner：轮播图效果，有点击分页和左右按钮切换页面效果，鼠标移入会停止轮播，移除自动轮播
	2. banner:右侧话费、流量充值，有tab标签切换效果，运用了jquery-ui插件
	3. main:主体部分有六层楼，每层都有tab标签切换功能
	4. main: 每层楼的第二个tab标签对应的内容通过ajax请求数据生成，数据为数据库中的index_goods数据表
	5. 页面左侧栏有显示所在楼层效果
	6. 页面右侧栏最底部“返回顶部”效果
#### 商品列表页 ####
	1. 显示浏览记录，且最新记录显示在最前效果
	2. 商品分页加载，数据为数据库中的goods数据表
	3. 点击商品列表右上方的左右选页和下方的选页按钮可进行选页，当显示第1页或最后一页时，左/右选页按钮会禁用
	4. 可根据价格区间筛选商品
	5. 综合排序、按价格升序降序排序、按评论降序排序功能
	6. 可勾选“飞牛自营”，筛选自营商品
	7. 三级联动效果
	8. 点击商品中的“加入购物车”可将商品加入购物车，有飞入购物车效果
	9. 底部“猜你喜欢”栏点击“换一批”可更换商品
#### 商品详情页
	1. 显示小图、中图、大图
	2. 小图切换并且显示在中图中
	2. 放大镜效果
	3. “+”、“-”按钮选择数量，并实时计算价格
	4. 输入框输入数量选择数量，失去焦点计算价格
	5. 点击“加入购物车”商品飞入购物车，购物车数量增加
	6. 三级联动效果
	7. “其他类似商品”处点击“换一批”可更换商品
	8. 下方“商品详情”一栏tab标签切换功能
	9. 点击“商品评论”标签进入商品评论区，从数据库中加载当前商品的所有评论并现实，实时现实数量，数据为数据库中的comment数据表
	10. 评论分页加载效果
	11. 评论实时加入数据库并显示在评论区
	12. 星级评分效果
	13. 显示当前所在城市
	14. 显示发表时间
	15. 过滤敏感字符
	16. 未登录不能评论
#### 购物车页 ####
	1. 三级联动效果
	2. 全选
	3. 单选高亮
	4. 选择数量，计算“小计”、“总额”、“总件数”
	5. 删除单件商品
	6. 删除选中商品
	7. 清空购物车
#### 注册页 ####
	1. 手机号、密码、确认密码、验证码、已同意协议正则验证
	2. 已注册验证
#### 登录页 ####
	1. 帐号密码验证
	2. 自动登录功能（两周免登录）
	3. tab标签切换
