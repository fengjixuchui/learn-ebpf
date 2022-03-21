# ebpf学习笔记

![20210501_184216_89](image/20210501_184216_89.png)

## 仓库介绍

```
Something I hope you know before go into the coding~
First, please watch or star this repo, I'll be more happy if you follow me.
Bug report, questions and discussion are welcome, you can post an issue or pull a request.
```

## 目录

* [基础知识](docs/基础知识.md)
    * [clang与llvm](docs/基础知识/clang与llvm.md)
    * [BPF内核实现](docs/基础知识/BPF内核实现.md)
    * [BPF指令集](docs/基础知识/BPF指令集.md)
    * [JIT即时编译](docs/基础知识/JIT即时编译.md)
    * [llvm对ebpf的支持](docs/基础知识/llvm对ebpf的支持.md)
    * [tracepoint](docs/基础知识/tracepoint.md)
    * [ustd](docs/基础知识/ustd.md)
    * [kprobe与kretprobe](docs/基础知识/kprobe与kretprobe.md)
    * [uprobe与uretprobe](docs/基础知识/uprobe与uretprobe.md)
* [CVE漏洞](docs/CVE漏洞.md)
    * [CVE-2021-31440](docs/CVE漏洞/CVE-2021-31440.md)
    * [CVE-2021-3489](docs/CVE漏洞/CVE-2021-3489.md)
* [bpftrace](docs/bpftrace.md)
  * [命令帮助](docs/bpftrace/命令帮助.md)
  * [举栗子](docs/bpftrace/举栗子.md)
* [BPF子系统](docs/BPF子系统.md)
  * [tracing](docs/BPF子系统/tracing.md)
    * [kprobe](docs/BPF子系统/tracing/kprobe.md)
    * [tracepoint](docs/BPF子系统/tracing/tracepoint.md)
    * [perf_event](docs/BPF子系统/tracing/perf_event.md)
  * [filter](docs/BPF子系统/filter.md)
    * [sk_filter](docs/BPF子系统/filter/sk_filter.md)
    * [sched_cls](docs/BPF子系统/filter/sched_cls.md)
    * [sched_act](docs/BPF子系统/filter/sched_act.md)
    * [xdp](docs/BPF子系统/filter/xdp.md)
    * [cg_skb](docg_skbcs/BPF子系统/filter/xdp.md)
* [BPF辅助函数](docs/BPF辅助函数.md)
* [kubeArmor](docs/kubeArmor.md)
* [falco](docs/falco.md)
* [tracee](docs/tracee.md)
* [cilium](docs/cilium.md)
* [datadog](docs/datadog.md)
* [goebpf](docs/goebpf.md)
* [libbpf](docs/libbpf.md)
* [bcc](docs/bcc.md)
    * [argdist](docs/bcc/argdist.md)
    * [bashreadline](docs/bcc/bashreadline.md)
    * [bindsnoop](docs/bcc/bindsnoop.md)
    * [biolatency](docs/bcc/biolatency.md)
    * [biolatpcts](docs/bcc/biolatpcts.md)
    * [biosnoop](docs/bcc/biosnoop.md)
    * [biotop](docs/bcc/biotop.md)
    * [bitesize](docs/bcc/bitesize.md)
    * [bpflist](docs/bcc/bpflist.md)
    * [cachestat](docs/bcc/cachestat.md)
    * [cachetop](docs/bcc/cachetop.md)
    * [capable](docs/bcc/capable.md)
    * [cobjnew](docs/bcc/cobjnew.md)
    * [compactsnoop](docs/bcc/compactsnoop.md)
    * [cpudist](docs/bcc/cpudist.md)
    * [cpuunclaimed](docs/bcc/cpuunclaimed.md)
    * [dbslower](docs/bcc/dbslower.md)
    * [dbstat](docs/bcc/dbstat.md)
    * [dcsnoop](docs/bcc/dcsnoop.md)
    * [dcstat](docs/bcc/dcstat.md)
    * [deadlock](docs/bcc/deadlock.md)
    * [dirtop](docs/bcc/dirtop.md)
    * [drsnoop](docs/bcc/drsnoop.md)
    * [execsnoop](docs/bcc/execsnoop.md)
    * [exitsnoop](docs/bcc/exitsnoop.md)
    * [ext4dist](docs/bcc/ext4dist.md)
    * [ext4slower](docs/bcc/ext4slower.md)
    * [filelife](docs/bcc/filelife.md)
    * [fileslower](docs/bcc/fileslower.md)
    * [filetop](docs/bcc/filetop.md)
    * [funccount](docs/bcc/funccount.md)
    * [funcinterval](docs/bcc/funcinterval.md)
    * [funclatency](docs/bcc/funclatency.md)
    * [funcslower](docs/bcc/funcslower.md)
    * [gethostlatency](docs/bcc/gethostlatency.md)
    * [hardirqs](docs/bcc/hardirqs.md)
    * [javacalls](docs/bcc/javacalls.md)
    * [javaflow](docs/bcc/javaflow.md)
    * [javagc](docs/bcc/javagc.md)
    * [javaobjnew](docs/bcc/javaobjnew.md)
    * [javastat](docs/bcc/javastat.md)
    * [javathreads](docs/bcc/javathreads.md)
    * [killsnoop](docs/bcc/killsnoop.md)
    * [klockstat](docs/bcc/klockstat.md)
    * [llcstat](docs/bcc/llcstat.md)
    * [mdflush](docs/bcc/mdflush.md)
    * [memleak](docs/bcc/memleak.md)
    * [mountsnoop](docs/bcc/mountsnoop.md)
    * [mysqld_qslower](docs/bcc/mysqld_qslower.md)
    * [netqtop](docs/bcc/netqtop.md)
    * [nfsdist](docs/bcc/nfsdist.md)
    * [nfsslower](docs/bcc/nfsslower.md)
    * [nodegc](docs/bcc/nodegc.md)
    * [nodestat](docs/bcc/nodestat.md)
    * [offcputime](docs/bcc/offcputime.md)
    * [offwaketime](docs/bcc/offwaketime.md)
    * [oomkill](docs/bcc/oomkill.md)
    * [opensnoop](docs/bcc/opensnoop.md)
    * [perlcalls](docs/bcc/perlcalls.md)
    * [perlflow](docs/bcc/perlflow.md)
    * [perlstat](docs/bcc/perlstat.md)
    * [phpcalls](docs/bcc/phpcalls.md)
    * [phpflow](docs/bcc/phpflow.md)
    * [phpstat](docs/bcc/phpstat.md)
    * [pidpersec](docs/bcc/pidpersec.md)
    * [profile](docs/bcc/profile.md)
    * [pythoncalls](docs/bcc/pythoncalls.md)
    * [pythonflow](docs/bcc/pythonflow.md)
    * [pythongc](docs/bcc/pythongc.md)
    * [pythonstat](docs/bcc/pythonstat.md)
    * [readahead](docs/bcc/readahead.md)
    * [reset-trace](docs/bcc/reset-trace.md)
    * [rubycalls](docs/bcc/rubycalls.md)
    * [rubyflow](docs/bcc/rubyflow.md)
    * [rubygc](docs/bcc/rubygc.md)
    * [rubyobjnew](docs/bcc/rubyobjnew.md)
    * [rubystat](docs/bcc/rubystat.md)
    * [runqlat](docs/bcc/runqlat.md)
    * [runqlen](docs/bcc/runqlen.md)
    * [runqslower](docs/bcc/runqslower.md)
    * [shmsnoop](docs/bcc/shmsnoop.md)
    * [slabratetop](docs/bcc/slabratetop.md)
    * [sofdsnoop](docs/bcc/sofdsnoop.md)
    * [softirqs](docs/bcc/softirqs.md)
    * [solisten](docs/bcc/solisten.md)
    * [sslsniff](docs/bcc/sslsniff.md)
    * [stackcount](docs/bcc/stackcount.md)
    * [statsnoop](docs/bcc/statsnoop.md)
    * [swapin](docs/bcc/swapin.md)
    * [syncsnoop](docs/bcc/syncsnoop.md)
    * [syscount](docs/bcc/syscount.md)
    * [tclcalls](docs/bcc/tclcalls.md)
    * [tclflow](docs/bcc/tclflow.md)
    * [tclobjnew](docs/bcc/tclobjnew.md)
    * [tclstat](docs/bcc/tclstat.md)
    * [tcpaccept](docs/bcc/tcpaccept.md)
    * [tcpconnect](docs/bcc/tcpconnect.md)
    * [tcpconnlat](docs/bcc/tcpconnlat.md)
    * [tcpdrop](docs/bcc/tcpdrop.md)
    * [tcplife](docs/bcc/tcplife.md)
    * [tcpretrans](docs/bcc/tcpretrans.md)
    * [tcprtt](docs/bcc/tcprtt.md)
    * [tcpstates](docs/bcc/tcpstates.md)
    * [tcpsubnet](docs/bcc/tcpsubnet.md)
    * [tcpsynbl](docs/bcc/tcpsynbl.md)
    * [tcptop](docs/bcc/tcptop.md)
    * [tcptracer](docs/bcc/tcptracer.md)
    * [threadsnoop](docs/bcc/threadsnoop.md)
    * [tplist](docs/bcc/tplist.md)
    * [trace](docs/bcc/trace.md)
    * [ttysnoop](docs/bcc/ttysnoop.md)
    * [vfscount](docs/bcc/vfscount.md)
    * [vfsstat](docs/bcc/vfsstat.md)
    * [virtiostat](docs/bcc/virtiostat.md)
    * [wakeuptime](docs/bcc/wakeuptime.md)
    * [xfsdist](docs/bcc/xfsdist.md)
    * [xfsslower](docs/bcc/xfsslower.md)


## 相关站点

* <https://ebpf.io/>
* <https://github.com/iovisor/bcc>
* <https://github.com/cilium/cilium>

---

![20220314_211340_10](image/20220314_211340_10.png)


## 参考

* <https://zhuanlan.zhihu.com/p/470680443>


---

![20220321_095908_26](image/20220321_095908_26.png)

![20220321_095948_70](image/20220321_095948_70.png) 

![20220314_211613_88](image/20220314_211613_88.png)

![20220314_211747_11](image/20220314_211747_11.png)

![20220314_211412_47](image/20220314_211412_47.png)


---
