## node-exporter && blackbox-exporter package for centos6 && 7 

> use fpm for package


## generate fpm for service

* command
```code
fpm -s pleaserun -t rpm -n black-exporter-service /usr/bin/blackbox_exporter
fpm -s pleaserun -t rpm -n node-exporter-service /usr/bin/node_exporter
```

## generate rpm package

* command

centos6

```code
fpm -s dir -t rpm -n node-exporter --rpm-os linux -v v1.4-centos6 \
  ./binary/node_exporter=/usr/bin/ \
  ./centos6/node_exporter=/etc/init.d/node_exporter


fpm -s dir -t rpm -n blackbox_exporter --rpm-os linux -v v1.4-centos6 \
  ./binary/blackbox_exporter=/usr/bin/ \
  ./centos6/blackbox_exporter=/etc/init.d/blackbox_exporter
```

centos7

```code
fpm -s dir -t rpm -n blackbox_exporter --rpm-os linux -v v1.4-centos7 \
  ./binary/blackbox_exporter=/usr/bin/ \
  ./centos7/blackbox_exporter.service=/usr/lib/systemd/system/blackbox_exporter.service
```