# orange-pi-zero-mt7601u
MT7601U driver for kernel 3.4.113 on Orange Pi Zero

root@orangepizero:~/mt7601usta/src# make install
make -C /root/mt7601usta/src/os/linux -f Makefile.6 install
make[1]: Entering directory '/root/mt7601usta/src/os/linux'
rm -rf /etc/Wireless/RT2870STA
mkdir /etc/Wireless/RT2870STA
cp /root/mt7601usta/src/RT2870STA.dat /etc/Wireless/RT2870STA/.
install -d /lib/modules/3.4.113-sun8i/kernel/drivers/net/wireless/
install -m 644 -c mt7601Usta.ko /lib/modules/3.4.113-sun8i/kernel/drivers/net/wireless/
/sbin/depmod -a 3.4.113-sun8i
make[1]: Leaving directory '/root/mt7601usta/src/os/linux'
