param | desc | reference
----|------|----
a | 添加到当前行的下一行  |sed '2a 我是大哥大' 在第二行后面添加 我是大哥大
c | 表示替换  |cat -n file \| sed '2,5c 我是大哥大' 替换第2到5行的内容 为我是大哥大
d | 表示删除  |cat -n file \| sed '2,5d' 删除第2到5行的内容
i | 表示插入  | sed -i '1 i\插入字符串' filename , 在第一行插入文本；  sed -i '$a\插入字符串' filename, 在最后一行插入; sed -i '/pattern/i "插入字符串"' filename，在匹配行插入字符串  Mac OS 下：sed '3i\\ntext to insert' file
s | 表示搜索，还可以替换  | sed 's/^ *//g' 删除行首空格
p | 表示打印  | cat -n file \| sed -n '2,5p' 只显示第2行到第5行
