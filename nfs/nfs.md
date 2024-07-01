
apt install nfs-kernel-server

mkdir /shared ; chmod 777 /shared

#cat /etc/exports
#允许所有的客户端机器（*）以读写（rw）、同步写（sync）和不检查子树（no_subtree_check）的方式访问共享目录
/shared *(rw,sync,no_subtree_check)

#重启
systemctl restart nfs-server

#查看可挂载项目
showmount -e IP
