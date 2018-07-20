# libnids
根据需要修改了libnids

libnids-1.19-for-win32：使用WpdPack_4_1_2
1、修改了打开网卡方式，通过传入网卡名而不是网卡序号；

2、有线网卡tcp发包检测失败，无线网卡没有问题，调试是校验值错误，原因不详；

libnids.c中，gen_ip_frag_proc（）取消了ip校验，
tcp.c中，process_tcp()取消了tcp校验，

3、nids_next()修改使用 pcap_next_ex()，删除自带的pcap，使用系统WpdPack_4_1_2开发包



libnids-1.24: 使用libpcap-1.8.1
1、有线网卡tcp发包检测失败，无线网卡没有问题，调试是校验值错误，原因不详；

libnids.c中，gen_ip_frag_proc（）取消了ip校验，
tcp.c中，process_tcp()取消了tcp校验，

2、nids_next()修改使用 pcap_next_ex()
