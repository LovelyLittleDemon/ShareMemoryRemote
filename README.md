# ShareMemoryRemote
android share memory in muti process 

ShareMemory android v1.0
### 具体实现：
> 通过binder把MemoryFile的ParcelFileDescriptor 传到Service；
> 在服务端通过ParcelFileDescriptor 读取共享内存数据；

### 解决问题
> binder 限制（binder的android上的限制1M，而且是被多个进程共享的）;
> binder 在android进程中经过一次内存copy，内存共享通过mmap，0次copy效率更高；


