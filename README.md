Receiving Googlvideo addresses from my DNS


Script on Mikrotik:

``
/tool fetch url="https://raw.githubusercontent.com/ion-lane/googlevideo_lists/refs/heads/main/ggc.rsc" mode=https dst-path=usb1
``

``
/ip firewall address-list remove [find where list="GGC" !dynamic]
``

``
/import file-name=usb1/ggc.rsc
``

``
/file remove usb1/ggc.rsc
``

! I recommend using a USB flash drive dst-path=usb1 to download lists daily.
