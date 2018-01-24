* 安装kubectl：

```
#下载最新版本的Kubernetes server 二进制文件,本问以1.9.1为例
mkdir -p /opt/k8s-install/
cd /opt/k8s-install
wget https://dl.k8s.io/v1.9.2/kubernetes-server-linux-amd64.tar.gz

#解压
tar zxvf kubernetes-server-linux-amd64.tar.gz

#拷贝kubectl到系统目录
cp kubernetes/server/bin/kubectl /usr/local/bin

#添加环境变量
echo "export PATH=/usr/local/bin:$PATH" >>/etc/profile
source /etc/profile
```

* 安装证书

```
#下载cfssl，用它来生成证书
cd /opt/k8s-install
wget https://pkg.cfssl.org/R1.2/cfssl_linux-amd64
chmod +x cfssl_linux-amd64
mv cfssl_linux-amd64 /usr/local/bin/cfssl

wget https://pkg.cfssl.org/R1.2/cfssljson_linux-amd64
chmod +x cfssljson_linux-amd64
mv cfssljson_linux-amd64 /usr/local/bin/cfssljson

wget https://pkg.cfssl.org/R1.2/cfssl-certinfo_linux-amd64
chmod +x cfssl-certinfo_linux-amd64
mv cfssl-certinfo_linux-amd64 /usr/local/bin/cfssl-certinfo

#创建json文件
mkdir -p /opt/k8s-install/ssl/
cd /opt/k8s-install/ssl

```

[json证书文件](json证书文件)

