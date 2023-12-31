---
title: "Өргөн ашиглагддаг CLI коммандууд"
excerpt:
date: 2023-11-04
header:
    teaser: /assets/images/unix_command.png
tog: true
tog_label: Table of Contents
tog_icon: "cog"
categories:
    - Command Line
tags:
    - [bash syntax]
---
## Оршил
Сайн байцгаана уу? Command Line series-ийн өмнөх блогоо үргэлжлүүлэн энэ удаагийн блогоор CLI дээр хамгийн өргөн ашиглагддаг коммандуудыг хамтдаа сурцгаая.

## Шинэ фолдер үүсгэх болон шилжих
1. **mkdir**: шинэ фолдер үүсгэх - Git Bash шинээр нээх үед бүгдүүрээ home directory дотор байх бөгөөд энэ дотроо **turshilt_folder** гэсэн шинэ фолдер үүсгэцгээе.
```shell
$ mkdir turshilt_folder
```
2. **cd**: өөр фолдер руу шилжих - шинээр үүсгэсэн **turshilt_folder**-руу шилжье.
```shell
$ cd turshilt_folder
```

## Файлтай холбоотой коммандууд
1. **ls**: одоогийн байгаа фолдер дотор ямар файлуудыг байгаа шалгах - **turshilt_folder** доторхи файлуудыг шалгая. (*Одоогоор ямар ч файл үүсгээгүй болохоор ямар ч файлны нэр гарч ирэхгүй.*)
```shell
$ ls
```
2. **touch**: шинэ файл үүсгэх - example гэсэн нэртэй txt файл үүсгэе.
```shell
$ touch example.txt # example.txt нэрний оронд хүссэн файл нэрээ бичих
```
3. **cat**: файл доторхи агуулгыг шалгах - шинээр үүсгэсэн **example.txt** файлыг шалгая. (*Ямар ч агуулга нэмээгүй болохоор ямар ч мэдээлэл гарч ирэхгүй*)
```shell
$ cat example.txt
```
4. **echo**: файлд агуулга нэмэх - example.txt файлдаа дараах зааврын дагуу агуулгыг нэмэе. Нэмэх мэдээдэл заавал "" эсвэл '' дотор бичих шаардлагатай.
```shell
$ echo "Сайн байна уу? Танд энэ өдрийн мэнд хүргэе" >> example.txt
```
Одоо  `cat example.txt` коммандыг уншуулвал түрүүхэн нэмсэн бичвэр дараах байдлаар харагдах болно.
![cat_command_output](/assets/images/cat_command.png)

5. **rm**: файл устгах - үүсгэсэн байсан example.txt файлаа устгая. (*Одоо `ls` комманд уншуулвал example.txt файл устсаныг шалгаж болно.* )
```shell
$ rm example.txt
```

## Процессуудтай холбоотой коммандууд
1. **ps**: Git Bash shell дээр ажиллаж байгаа процессуудыг шалгах
```shell
$ ps
```
Жишээ нь дараах байдалтай харагдана.
![ps_command_output](/assets/images/ps_command.png)
2. **kill**: уншигдаж байгаа процессийг хүчээр зогсоох
```shell
$ kill 836 #PID бичих
```
Жишээ: өмнө нь уншигдаж байсан 836 PID-тай процессыг хүчээр зогсоогоод `ps`-ээр дахин шалгавал 836-тай процесс байхгүй болсныг шалгах боломжтой.
![kill_command_output](/assets/images/kill_command.png)

## Систем мэдээлэлтэй холбоотой коммандууд
1. **df**: дискний хэмжээ хэр ашиглагдсан байгааг шалгах (-h option нь human-readable буюу хүн уншихад ойлгомжтой байдлаар гэсэн утгатай)
```shell
$ df -h
```
2. **du**: одоогийн байгаа фолдер дахь файлуудын эзлэх дискний хэмжээг шалгах
```shell
$ du -h
```

## Өөр бусад коммандууд
1. **alias**: Өргөн хэрэглэж байгаа урт коммандууддаа shortcut үүсгэхэд ашиглана - Жишээ нь `ls -al` комманд нь тухайн фолдер дахь бүх файл болон фолдеруудыг нь урт форматаар үзүүлдэг бөгөөд дараах alias ашиглан `ll` гэсэн shortcut үүсгэж байна
```shell
$ alias ll='ls -al'
```
2. **history**: Одоо байгаа shell session-д хийгдсэн бүх коммандаа шалгах (Мөнхүү `history` коммандын ард хүссэн тоогоо бичин сүүлийн хэдэн коммандуудыг шалгах боломжтой)
```shell
$ history
$ history 10
```
![history_command_output](/assets/images/history_command.png)