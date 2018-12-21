# jobplus9-9

## 环境配置

- python3.6
- pip安装requirement.txt。命令或许是`sudo pip3 install requirement.txt`.

## 测试使用方法

### 单元测试

在与manage.py同级的目录下，在命令行输入：
```shell
export FLASK_APP=manage.py
export FLASK_DEBUG=1
flask run
```

> windows下把export换成set
### 数据生成
1. 确保存在`plus_job`名称的数据库，manage.py同级目录运行 `flask db upgrade`  生成迁移文件
2. 运行spider_laou.py文件，爬取拉钩职位信息及对应的公司信息，保存到jobs.json文件
（太频繁，拉钩会弹出登录页）
3. 运行 creat_data.py文件，会默认生成一个boss账号，该账号会关联数据中生成的第一个公司。每个公司下，有一个对应的职位

### 功能测试

在顶级目录jobplus9-9下，

在与manage.py同级的目录下，在命令行输入：

```shell
python tests/functional_tests.py
```

> 或许你的命令是`python3`

当结果是`AssertionError: Finish the test!`，表明测试通过（虽然看起来哪里错了）。
## 组员

- [黎明之翼_封心](https://github.com/Raymond38324)
- [蒲小帅](https://github.com/puxiaoshuai)
- [黄健楸](https://github.com/linxixizhi/)
- [小铁皮](https://github.com/xiaotiepi)
- [lightningwow](https://github.com/limi2018)
