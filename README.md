# area-data
中国省、市、区数据(含港澳台)

## v3.1
增加广东省中山市和东莞市的区镇数据(参考京东 pc 端的地区选择)
## v3
增加港澳台数据(参考京东 pc 端的地区选择)，v3之后不再提供或更新街道数据

## v2
v2版本中，`data.js` 中不再包含街道数据，以减小打包体积。格式化的街道数据单独存放在 `street.js` 中，单独暴露全局变量 `STREETS`。可通过[该CDN链接](http://onasvjoyz.bkt.clouddn.com/street.js)单独引入，或者下载该文件自行引入。

## v1
v1版本中，`data.js` 包含省市区以及街道数据。

## Installation
Install the pkg with npm:

```
npm install area-data --save
```

or yarn

```
yarn add area-data
```

or bower

```
bower install area-data
```

## 获取数据
```
import AreaData from 'area-data';

AreaData['86']
// 所有省份：{'110000': '北京市', '120000': '天津市', '130000': '河北省', ...}

AreaData['130000']
// 对应省份的所有城市：{'130100': '石家庄市', '130200': '唐山市', '130300': '秦皇岛市', ...}

AreaData['130200']
// 对应市的所有县区：{'130201': '市辖区', '130202': '路南区', '130203': '路北区', ...}

### v1
AreaData['130202']
// 对应县区的所有街道：{'130202001000': '学院南路街道', '130202002000': '友谊街道', ...}

### v2 
// v2 版本中 AreaData 中不再包含街道数据，需要单独引入 street.js
STREETS['130202']
// 对应县区的所有街道：{'130202001000': '学院南路街道', '130202002000': '友谊街道', ...}
```

> 官方数据(截止到2016.07.31): [城乡区域划分](http://www.stats.gov.cn/tjsj/tjbz/tjyqhdmhcxhfdm/2016/index.html)

**数据来源：** 最新省市区数据来自 [china-area-data](https://github.com/airyland/china-area-data), 最新街道数据来自 [Administrative-divisions-of-China](https://github.com/modood/Administrative-divisions-of-China).

## LICENSE

MIT

