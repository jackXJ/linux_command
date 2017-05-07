## AWK
* -F :  以冒号为分隔符 , awk -F ‘[;:]’  多个分隔符的情况
* 过滤功能。
* OFS=“\t”,以\t为分隔符进行输出
* NR 表示行号
* awk 可以像 grep 一样去匹配一行： 
`awk  ‘/LISTEN/‘  file_name`
`awk '$6 ~ /FIN/ || NR==1 {print NR,$4,$5,$6}' OFS="\t" netstat.txt`
注意整行匹配 和 某一段匹配方法不同， ～ 表示模式开启，／pattern／
！～ 表示反模式
* 可以拆分文件
* BEGIN， END
