//扩展root分区，`/dev/sda1` 为空闲磁盘
```
pvcreate /dev/sda1
pvdisplay
vgdisplay
vgextend fedora_dhcp-140-57 /dev/sda3
vgdisplay
lvdisplay
lvextend -L +500G /dev/fedora_dhcp-140-57/root
resize2fs /dev/fedora_dhcp-140-57/root
```
