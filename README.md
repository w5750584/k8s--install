= 1、服务器要求：



\*  系统版本：centos7.4



\*  网络环境：所有节点可以互通



\*  注意事项：关闭集群所有服务器selinux，iptables







= 2、软件依赖：



\*  集群所有服务器：



        flannled



\*  master：



        kubectl

        kube-apiserver

        kube-scheduler

        kube-controller-manager





\*  node：



        docker

        kubelet

        kub-proxy

