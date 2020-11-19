# vbird

第五章、文件权限与目录配置
   5.1  文件拥有者/群组/其他人 
         文件拥有者 ： 只有自己能看到的东西。
         群组： 整个部门能看到的东西
         其他人：被允许的其他部门能看到
   5.2 文件属性
        Ls(list) 重点在显示文件的文件名与相关属性
       Ls -al 表示列出所有的文件详 细的权限与属性
       查看ls具体用法参数，man ls  | ls --help | info ls 
     【1】 共有十个字符，每个字符代表含义如下
              第一个：d 代表目录  - 文件  l链接文件  b存储的周边设备  c鼠标键盘等
              接下来的字符，每三个一组，均为 rwx组合， r代表可读(read)，w代表可写(write),x代表可执行(execute) ，没有权限的用 - 表示。
              第一组为文件拥有者的权限 owner，第二组为群组 group ，第三组其他人other
     【2】表示有多少文件名链接到此节点
    【3】表示这个文件(或目录)的“拥有者帐号”    
    【4】表示这个文件的所属群组
    【5】为这个文件的容量大小，默认单位为Bytes    
    【6】为这个文件的创建日期或者是最近的修改日期
    【7】为这个文件的文件名。前面带有.开头的文件，是隐藏文件。
   5.2.1 改变文件属性和权限
      Chgrp 改变文件群组（change group ）
          chgrp [-R] dirname/filename ...   -R : 进行递回(recursive)的持续变更

      Chown 改变文件拥有者(change owner)

      chmod 改变文件属性
       ① Rwx 分别有对应的数字，分别 r:4 > w:2 > x:1 
           -rw-r--r--    代表 644

       ② 通过符号来修改权限
        设置 -rwxr-xr--  chmod u=rwx,g=rx,o=r filename (u文件拥有者 g群组 o其他人)


Cd (change directory)
