# tasmota-sml

This Binary (v13.3.0) was build with [Tasmocompiler](https://github.com/benzino77/tasmocompiler)

```
$ docker run --rm --name tasmocompiler -p 3000:3000 benzino77/tasmocompiler
```

### flashing

Optional purge the flash and finally flash the image
```
esptool.py --port /dev/ttyUSB0 erase_flash
esptool.py --port /dev/ttyUSB0 write_flash -fm dout 0x0 tasmota4M.bin
```

### configuring
- Connect to the Hotspot on the ESP Device and visit http://192.168.4.1
- After configuring your Wifi, you have to paste the content of "script".

Sources:
- [Tasmota Docs](https://tasmota.github.io/docs/Smart-Meter-Interface/#logarex-lk13be-sml-lk13be904639)
- Hardware: 
    - Vendor: Logarex
    - Type: LK13BE904639