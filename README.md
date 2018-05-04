# CPM (CodeOS Package Manager)
cpm is an npm-like package manager used in CodeOS(debian base OS), you can use following commands to manage packages:  

### user tools
- cpm install   
  like npm install,cpm will install all packages listed in package.json
- cpm install package-name  
  install specified package
- cpm uninstall package-name  
  uninstall specified package
- cpm update  
  update all packages listed in packge.json
- cpm update package-name  
  update specified package
- cpm start package-name  
  start package using command in package.json/scripts/start
- cpm ls  
  list all packges installed by cpm
- cpm config set key val  
  reconfig cpm config file(see config)  

### admin tools
- cpm publish package-dir  
  upload package to repo
- cpm eliminate package-name  
  eliminate package in repo

## config
to config cpm, you can modify /usr/lib/cpm/config.json  

- host
- root

## ipc  
cpm provides several ways to export process data for other process 
1. cpm输出固定格式字符串,daemon解析字符串,获取进度等信息
2. cpm提供进程通信接口,具体接口方式待定
3. cpm与daemon之间通过dbus进行数据沟通,daemon通过dbus收集信息,根据进程号区分具体的cpm进程