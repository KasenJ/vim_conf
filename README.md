# vim_conf
vim_conf
need vim 8.1
http://www.cppblog.com/markqian86/archive/2017/09/13/215238.aspx

1.更新yum
sudo yum upgrade sduo yum update

2.下载git
sudo yum install git

3.升级vim以及gcc
3.1升级gcc
sudo yum install centos-release-scl -y  ;

sudo yum install devtoolset-3-toolchain -y ;

sudo scl enable devtoolset-3 bash;


3.2升级vim
yum install ncurses-devel;
wget https://github.com/vim/vim/archive/master.zip ;
unzip master.zip ;
cd vim-master ;
cd src/ ;
./configure --with-features=huge -enable-pythoninterp --enable-python3interp ;
sudo make ;
sudo make install ;
export PATH=/usr/local/bin:$PATH

