## Install Red Alert on RetroPie
1. F4 Go to ternial on your RetroPie
2. Run these commands:
``` 
wget "https://github.com/thinktt/ra/raw/master/ra.zip"
sudo apt-get install unzip -y
unzip ra.zip -d ~/REtroPie/roms/pc
mv ~/RetroPie/roms/pc/Command\ \&\ Conquer\ Red\ Alert/ ~/RetroPie/roms/pc/ra```
```

## Backup Dosbox config and set Dosbox up for network play
```
cp .dosbox/dosbox-SVN.conf .dosbox/dosbox-SVN.conf.original 
vim .dosbox/dosbox-SVN.conf
```

this is optional just think it makes things look better: 
```
under [render] section set scaler=normal2x 
```
this turns on ipx for network play in dosbox
```
under [ipx] all the way at the bottom set ipx=true
```
Exit Termilal, 

## Start IPX server in Dosbox
1. Start dosbox from RetroPie menus
2. Run one of these commands in Dosbox to get the ipx server working
```
# start up an ipx dosbox server
ipxnet startserver 12346
``` 
```
# connects to an existing Dosbox ipx server 
ipxnet connect [xxx.xxx.xxx.xxx] [port]
```
## Start Red Alert from Dosbox
```
cd ra
ra 
```

You should now be able to do Network play with your friend through the Dosbox IPX server


