# Alfred 天气查询插件
> 基于[和风天气](https://dev.qweather.com/docs/api/)开放接口制作，适用于Alfred3以上。

### 运行环境依赖
- MacOS系统
- Alfred3
- Python2.7
	- requests 	

### 下载
下载地址：[点击前往](https://github.com/oliverCJ/alfred-weather-python/releases)


### 安装使用
1.  右键以Alfred打开，插件将自动安装到Alfred的Workflow中
2. 使用Alfred快捷键打开窗口，输入快捷指令即可

### 使用前准备工作
1. 安装python依赖

	1. 请确保默认的/usr/bin/python版本为2.7 
	2. 请务必确保使用python2.7安装依赖
	3. 如果无pip工具则可网络搜索安装方法
	4. 命令行执行 `pip2 install -i https://mirrors.aliyun.com/pypi/simple/ requests` 
2. 申请[注册和风](https://dev.qweather.com/)天气账号，并申请创建应用ID/KEY
	1. 注册开发者账号后，进入控制台
	2. 进入应用管理，点击创建应用，可直接选择免费版本，个人完全够用，功能也齐全
	3. 根据提示创建应用后，可在页面看到对应的Public ID和Key
3. 进入Alfred设置界面，在Workflow标签下，找到天气查询插件
4. 选中插件后，在界面右侧，点击`[x]`图标，在弹出层中新增环境变量
	1. 右侧点击+新增变量记录填入Name/Value
	2. Public ID变量设置：Name:`uid ` Value:`步骤2中第三个子步骤，页面上对应的Pubclic id值` 
	3. Key变量设置：Name:`key ` Value:`步骤2中第三个子步骤，页面上对应的Key值` 
	4. 点击保存即可
5. 设置完毕
 
### 使用方法
> 下述指令均在Alfred输入窗口中执行

##### 根据地区查询天气

指令：`tq`
用法 ：`tq 地区名称或拼音` 
	将自动搜索对应地区名称以及下属一级区县，选中自己需要查询的结果项，回车即可直接返回对应地区天气情况；另，在选中自己需要查询的地区结果项后，ALT+回车会将该地区设置为您的默认查询地区，然后继续返回对应地区天气情况。
例：`tq 成都`  或 `tq chengdu`

指令：`tqc`
用法：`tqc` 
	该指令无参数，会自动根据前一步中alt+回车设置的默认地区，直接查询对应区域天气

### 使用展示
![地区查询](https://github.com/oliverCJ/alfred-weather-python/blob/master/location.png)

![天气查询](https://github.com/oliverCJ/alfred-weather-python/blob/master/weather.png)

![当前天气](https://github.com/oliverCJ/alfred-weather-python/blob/master/current.png)