 3/21/2024
MindSpore官网https://www.mindspore.cn/install/detail?path=install/r2.3/mindspore_cpu_install_source.md
如果已经安装了其他依赖，最好手动安装或者换个环境，不然很容易报错
自动安装脚本目前缺少部分包flex, bison, GNU autoconf, GNU automake, libtool
sudo apt-get update
sudo apt-get install flex bison autoconf automake libtool

### 自动安装脚本
sudo wget https://gitee.com/mindspore/mindspore/raw/r2.3/scripts/install/ubuntu-cpu-source.sh
默认安装Python 3.7
bash ./ubuntu-cpu-source.sh
从代码仓下载源码
在无root权限的服务器 cd ~
git clone -b r2.3 https://gitee.com/mindspore/mindspore.git
编译
cd mindspore
bash build.sh -e cpu -j4 -S on
安装
pip install output/mindspore-*.whl -i https://pypi.tuna.tsinghua.edu.cn/simple
验证成功
python -c "import mindspore;mindspore.set_context(device_target='CPU');mindspore.run_check()"


### 手动安装见链接
https://www.mindspore.cn/install/detail?path=install/r2.3/mindspore_cpu_install_source.md#%E7%8E%AF%E5%A2%83%E5%87%86%E5%A4%87-%E6%89%8B%E5%8A%A8
