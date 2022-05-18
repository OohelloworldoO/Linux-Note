# Linux-Note

關機指令
halt -p、poweroff、shutdown
新增文字檔
gedit a.txt
看檔案
```
cat+檔案名、more+檔名、less+檔名
ping on windows and linux are diffrent on TTL、bytes、times
windows:ipconfig
linux:ifconfig，linux want to break the ping(ctrl+c to break)
```
```
systemctl:      service:
start		sshd
stop        +	httpd
restart		firewalld
reload 
status
disable
enable
```
```
最後ㄉd 代表=daemon

root使用者提示字元是#
一般使用者是$

cat 顯示內容用
hostname 系統
pwd顯示路徑
whoami 使用者名稱
~ =home directory
cd ~ =change to home directory
w(可看線上使用者正在做啥)、who 查詢目前有誰正在系統上  tty是本端  pts是遠端

linux=kernal+shell+application(由內往外)
不同的shell + 不同的application = 各種不同發行的版本

uname -r 查看kernal版本
uname -a 看更詳細
x86 64 for 位元系統
i386、i486、i586、i686... for 32位元

ls vmlinuz* 
* =萬用字(查詢nmlinuz開頭的任意檔案)\
-l 長格式(long format)顯示
echo $SHELL(取出環境變量的值，echo出來)
$ 用來取出變數名稱
& 用來背景執行

ls -l(長格式) -a (all) -h
 ---   ---    ---
owner group  other
r可讀
w可寫    的權限
x可執行
d目錄
-檔案
l連結
b硬碟或usb (block)
c設備(鍵盤、滑鼠) (字元裝置)

兩種執行腳本的方法:
bash +檔案名
./檔案名

hostname 可以查看所在主機
hostname set-hostname centos7-6 更改主機名稱 主機名稱就變成centos7-6
bash 跑kernal
pwd 顯示完整路徑(print working directory)
過濾資料 |grep
從上往下第1筆資料 |head -n 1
echo shell 查詢現在使用的核心
fg foreground前景執行
ctrl+a 到命令列最前面
ctrl+e 最後面
檔案名稱開頭是 '.' 代表是隱藏檔案 需使用-a 來顯示
ls -l -h -a =ls -lha
man+查詢的東西=manuscript 手冊，查詢指令使用方法
su - 使用者名稱 可以變換使用者
echo "12345678" | passwd --stdin tom 把tom的密碼改成12345678
-reboot 重新開機
rm -rf * --->rm:remove -r:recursive -f:force
/etc --->系統配置 網路配置...很重要的檔案都放在這裡
/proc --->系統的資訊(cpu、core...)
resolv.conf --->放dns伺服器的檔案

pwd --當前路徑(指令)(print working directory)
echo $PWD--當前路徑(系統環境)
uname -r 看到系統核心版本
touch 創建檔案
mkdir 創建目錄
wget 用來下載
sudo -l 可以讓使用者知道他是否具有切換成超級使用者的權利,及他可以執行那些超級使用的指令
echo $? 可以用來檢查前面指令是否成功 0:成功 非0值:失敗
|head -n 數字 =n筆資料
|tail -n 數字 =倒數n筆資料
sed -n "5,10p" 顯示5~10行指令 p:print
touch 用來創建資料夾或是修改最後編譯時間
> 資料夾 :清空資料夾
"" > 資料夾 取代內容
"" >> 資料夾 追加內容
cat <<aaa >a.txt
>1
>2
>3
>aaa(輸入就結束)
```
