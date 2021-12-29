# mpsoc-manifest
Repo manifest files for Mentor Embedded release of Android for Xilinx Zynq UltraScale+ MPSoC 

repo mirors download
$ curl https://mirrors.tuna.tsinghua.edu.cn/git/git-repo -o repo
$ chmod +x repo
$ export REPO_URL='https://mirrors.tuna.tsinghua.edu.cn/git/git-repo'
refer https://mirrors.tuna.tsinghua.edu.cn/help/git-repo/




$ python3.7 repo init -u git://github.com/uniqueluo/mpsoc-manifest.git -b zynqmp-android_8 -m release_android-8_xilinx-v2019.2.xml



Download Mali-400 User Space Components
$ wget https://www.xilinx.com/publications/products/tools/mali-400-userspace.tar
$ mkdir -p tmp_mali
$ tar -xf mali-400-userspace.tar -C ./tmp_mali
$ mkdir -p vendor/xilinx/zynqmp/proprietary
$ cp -r tmp_mali/mali/Android/android-8/MALI-userspace/r8p0-01rel0/* vendor/xilinx/zynqmp/proprietary/
$ rm -rf tmp_mali/
