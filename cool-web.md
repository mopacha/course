# cool-web


### 开发

#### 1. 环境

- Node: >=8

#### 2.  安装依赖

```
npm install
```

#### 3. 运行

```
npm start

```

### 部署

#### 1.打包

run `./release.sh` will generate the deploy directory

	├── build
	│   ├── deploy
	│   │   ├── ${项目名去除web后缀}-static // static resource
	│   │   ├── ${项目名去除web后缀}-node  //node 


#### 2. 生成环境运行

- Node: >=8
- pm2

```bash
npm run server
npm run stop
```

#### 3. Linux Node and PM2 Install

- node install

```
wget https://nodejs.org/dist/latest-v8.x/node-v8.16.0-linux-x64.tar.xz
yum install -y xz
tar xf node-v8.16.0-linux-x64.tar.xz

ln -s /usr/software/node-v8.16.0-linux-x64/bin/npm   /usr/local/bin/ 
ln -s /usr/software/node-v8.16.0-linux-x64/bin/node   /usr/local/bin/

node -v
npm -v

```

- pm2 install

```
npm i -g pm2 
ln -s /usr/software/node-v8.16.0-linux-x64/bin/pm2  /usr/local/bin/pm2
```

### dir
	├── config
	│   ├── default.js
	│   ├── development.js
	│   ├── env-config.json
	│   ├── log4js.js
	│   └── production.js
	├── cool.config.js
	├── gulpfile.js
	├── LICENSE
	├── package.json
	├── process.json
	├── README.md
	├── release.sh
	└── src


#### node dir
	src/
	├── app.config.js
	├── controller
	├── server.js
	├── service
	├── static
	└── view

####  staic dir
	src/static
	├── apps
	│   ├── demo
	│   │   ├── app.js
	│   │   ├── app.vue
	│   │   ├── page
	│   │   ├── routes
	│   │   └── styles
	│   └── face
	│       ├── app.js
	│       ├── app.vue
	│       ├── imgs
	│       ├── page
	│       ├── routes
	│       └── styles
	└── common
		├── assets
		│   ├── img
		│   └── svg
		├── components
		│   └── svg-icon
		├── libs
		│   ├── element-ui.js
		│   ├── http.js
		│   ├── icon.js
		│   └── index.js
		└── utils
			└── validate.js

		
	cnpm update acorn --depth 20
	cnpm dedupe
