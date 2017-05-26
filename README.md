# 修改头文件
* 进入caffe/include/caffe
> 这里主要是修改包含 "caffe/proto/caffe.pb.h" 的头文件 ，改为相对当前工程 caffe.pb.h 的位置 //**这里修改好了**

# 编译caffe能可调试的可执行程序
>g++ -o caffe_test caffe.cpp -I ./caffe/include -D CPU_ONLY -I ./caffe/src/ -L /home/yunzhongke/work/caffe/.build_release/lib -lcaffe -lglog -lboost_system -lprotobuf -lgflags -gdwarf-2

`如果报未定义的引用或一些其它关于动态库相关的错误时，去之前安装好的caffe/build/tools/下，通过 “ldd caffe.bin” 查看 我们手动编译时，需要加载那些动态库`



