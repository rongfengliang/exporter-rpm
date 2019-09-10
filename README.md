## node-exporter && blackbox-exporter package for centos6 && 7 

> use fpm for package


## generate fpm for service

```code
fpm -s pleaserun -t rpm -n black-exporter-service /usr/bin/blackbox_exporter
fpm -s pleaserun -t rpm -n node-exporter-service /usr/bin/node_exporter
```


## generate rpm package

```code

```