Receiving Googlvideo addresses from my DNS


Script on Mikrotik:

/tool fetch url="https://raw.githubusercontent.com/ion-lane/googlevideo_lists/refs/heads/main/googlevideo.rsc" mode=https dst-path=usb1

/ip firewall address-list remove [find where list="GOOGLEVIDEO" !dynamic]; /import file-name=usb1/googlevideo.rsc; /file remove usb1/googlevideo.rsc

! I recommend using a USB flash drive dst-path=usb1 to download lists daily.
