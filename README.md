Linux通用应急响应脚本，适用大多数情况

目前在ubuntu、centos7、kali上均可以正常运行。其他未实验 可以提供报错，针对修改。



脚本执行后生成的文件解释：
danger_file.txt  脚本执行后的高危结果，对付看，结果需要经验分析，不要一股脑就认为风险项。

*****Ashro_checkresult.txt   结尾的是脚本执行过程日志，这个比较友好可以从这里分析

check_file文件夹--检查命令篡改
weibu_md5.py 通过脚本获取系统上的命令配置文件的MD5值到check_file/*.csv文件中，进行微步的威胁情报查询，需要配置脚本中的自己api。脚本执行后会在当前目录生成结果文件。是否命令篡改结果一目了然。

webshell文件夹--检查可执行文件后门
执行脚本后会将当前系统中正在进行的进程其涉及到的可执行文件cp下来。dump下来沙箱检测即可。

log文件夹--会将/var/log/*文件夹内容打包成压缩包

<img width="509" alt="image" src="https://github.com/Ashro-one/Ashro_linux/assets/49979071/806d9e04-6890-401a-a2ad-11af64598e7c">
