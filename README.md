# libnids
根据需要修改了libnids

libnids-1.19-for-win32：
1、修改了打开网卡方式，通过传入网卡名而不是网卡序号
2、有线网卡tcp发包检测失败，无线网卡没有问题，调试是校验值错误，原因不详
libnids.c中，gen_ip_frag_proc（）取消了ip校验
tcp.c中，process_tcp()取消了tcp校验
