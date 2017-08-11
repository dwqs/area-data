# area-data
中国省、市、区、街道数据

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

AreaData['130202']
// 对应县区的所有街道：{'130202001000': '学院南路街道', '130202002000': '友谊街道', ...}
```

> 官方数据(截止到2016.07.31): [县及以上区域划分](http://www.stats.gov.cn/tjsj/tjbz/xzqhdm/201703/t20170310_1471429.html)  [城乡区域划分](http://www.stats.gov.cn/tjsj/tjbz/tjyqhdmhcxhfdm/2016/index.html)

**数据来源：** 最新省市区数据来自 [china-area-data](https://github.com/airyland/china-area-data), 最新街道数据来自 [Administrative-divisions-of-China](https://github.com/modood/Administrative-divisions-of-China).

## LICENSE

MIT

