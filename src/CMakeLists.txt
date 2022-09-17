# cmake 最低版本需求
cmake_minimum_required(VERSION 3.0)
project(MyNginx)
#添加库文件
set(LIB_SRC 
ngx_alloc.c
ngx_array.c
ngx_buf.c
ngx_channel.c
ngx_conf_file.c
ngx_connection.c
ngx_cpuinfo.c
ngx_crc32.c
ngx_crypt.c
ngx_cycle.c
ngx_daemon.c
ngx_darwin_sendfile_chain.c 
ngx_darwin_init.c
ngx_dlopen.c
ngx_errno.c
ngx_file_aio_read.c
ngx_file.c
ngx_files.c
ngx_freebsd_init.c
ngx_freebsd_sendfile_chain.c
ngx_hash.c
ngx_inet.c
ngx_linux_aio_read.c
ngx_linux_init.c
ngx_linux_sendfile_chain.c
ngx_list.c
ngx_log.c
ngx_md5.c
ngx_module.c
ngx_murmurhash.c
ngx_open_file_cache.c
ngx_output_chain.c
ngx_palloc.c
ngx_parse_time.c
ngx_parse.c
ngx_posix_init.c
ngx_process_cycle.c
ngx_process.c
ngx_proxy_protocol.c
ngx_queue.c
ngx_radix_tree.c
ngx_rbtree.c
ngx_readv_chain.c
ngx_recv.c
ngx_regex.c
ngx_resolver.c
ngx_rwlock.c
ngx_send.c
ngx_setaffinity.c
ngx_setproctitle.c
ngx_sha1.c
ngx_shmem.c
ngx_shmtx.c
ngx_slab.c
ngx_socket.c
ngx_solaris_init.c
ngx_solaris_sendfilev_chain.c
ngx_spinlock.c
ngx_string.c
ngx_syslog.c
ngx_thread_cond.c
ngx_thread_id.c
ngx_thread_mutex.c
ngx_thread_pool.c
ngx_time.c
ngx_times.c
ngx_udp_recv.c
ngx_udp_send.c
ngx_udp_sendmsg_chain.c
ngx_user.c
ngx_writev_chain.c
)
add_library(lib_nginx ${LIB_SRC})

# 编译源码生成目标
set(APP_SRC nginx.c)
add_executable(mynginx ${APP_SRC})
target_link_libraries(mynginx lib_nginx)
