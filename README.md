# http-2.4-compilation
Steps for http 2.4 compilation 

#Create a directory and download the source code :

 [root@compilation /] mkdir  /root/apache2.4
 [root@compilation /] cd   /root/apache2.4
 [root@compilation apache2.4]# wget  http://www-us.apache.org/dist//httpd/httpd-2.4.29.tar.gz
 [root@compilation apache2.4]# wget  http://www-eu.apache.org/dist//apr/apr-1.6.3.tar.gz
 [root@compilation apache2.4]# wget  http://www-eu.apache.org/dist//apr/apr-util-1.6.1.tar.gz
 
 
 #extract the tar.gz files
 [root@compilation apache2.4]# tar -xvf httpd-2.4.29.tar.gz
 [root@compilation apache2.4]# tar -xvf apr-1.6.3.tar.gz
 [root@compilation apache2.4]# tar -xvf apr-util-1.6.1.tar.gz

#Move the apr files to srclib folder
[root@compilation apache2.4]# mv apr-util-1.6.1 httpd-2.4.29/srclib/apr-util
[root@compilation apache2.4]# mv apr-1.6.3 httpd-2.4.29/srclib/apr

#install the dependecies 
[root@compilation /]# yum install prce-devel
[root@compilation /]# yum install expat-devel

#change the directory to httpd-2.4.29
[root@compilation /] cd httpd-2.4.29

run the configure file
[root@compilation /]# ./configure --with-included-apr --prefix=/apache24

run the make file
run make install
