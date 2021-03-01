# Understatnding Command-Line Basics

### Discussing Distributions

Sử dụng các bản phân phối(distro). Một số bản phân phối nên sử dụng khi follow cuốn sách này như: Centos 7, Ubuntu 18.04 LTS

### Reaching a Shell

Để truy cập vào shell, có thể ssh vào máy hoặc trên Ubuntu Desktop nhấn `Ctrl + Alt + T`

### Exploring Your Linux Shell Options

Một số bản phân phối shell: 

- Bash
- Dash
- KornShell
- tcsh
- Z shell

Listin 1.1: show to which shell `/bin/sh` Centos

```
[root@centos7 ~]# readlink /bin/sh
bash
```

Listin 1.2: show to which shell `/bin/sh` Ubuntu

```
root@ubuntu18:~# readlink /bin/sh
dash
```
1.3: echo version shell

```
[root@centos7 ~]# echo $BASH_VERSION
4.2.46(2)-release
```

```
root@ubuntu18:~# echo $BASH_VERSION
4.4.19(1)-release
```
1.4: Displaying linux distro 

```
uname -a
```

```
[root@centos7 ~]# uname -a
Linux centos7 3.10.0-1127.el7.x86_64 #1 SMP Tue Mar 31 23:36:51 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux
```

```
root@ubuntu18:~# uname -a
Linux ubuntu18 4.15.0-45-generic #48-Ubuntu SMP Tue Jan 29 16:28:13 UTC 2019 x86_64 x86_64 x86_64 GNU/Linux
```

### Using a Shell 

Sử dụng lệnh echo cho các tính năng hữu ích của shell

### Navigating the Directory Structure

Sử dụng lênh `cd` để di chuyển giữa các thư mục và lệnh `pwd` để xem vị trí thư mục hiện tại

### Using Environment Variables

Các biến môi trường theo dõi thông tin hệ thống, chẳng hạn như: tên người dùng đã đăng nhập vào shell, thư mục mặc định của người dùng  ...

Vì `Hello.sh` nằm trong thư mục không có trong `PATH` nên không thể trực tiếp chạy `Hello.sh`

```
root@ubuntu18:~# Hello.sh
Hello.sh: command not found
```
mà chỉ ra đường dẫn đến file đó: 

```
root@ubuntu18:~# /root/hung/Hello.sh
Hello world
```

### Getting Help

- Sử dụng lệnh `man` để xem trợ giúp về các tùy chọn hoặc cú pháp của lệnh

cú pháp: `man [option] [command]`

- Sử dụng lệnh `history` để xem lại các lệnh thực hiện gần đây: 

```
65  /root/hung/Hello.sh
66  cd hung/
67  ls
68  chmod +x Hello.sh
69  cd
70  ls
71  /root/hung/Hello.sh
72  vi /root/hung/Hello.sh
73  /root/hung/Hello.sh
74  Hello.sh
75  history
```

Để quay lại 1 lệnh mới sử dụng trước

```
!65
```

```
root@ubuntu18:~# !65
/root/hung/Hello.sh
Hello world
```

Show history file name 

```
echo $HISTFILE
```













