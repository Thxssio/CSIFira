<h1 align="center">  CSI Camera V2 </h1>


* Clone o repositorio
 ```
Git clone https://github.com/JetsonHacksNano/CSI-Camera.git 
```
* Entre na pasta
```
cd CSI-Camera
```
* Teste da Camera
```
gst-launch-1.0 nvarguscamerasrc sensor_id=0 ! 

   'video/x-raw(memory:NVMM),width=3280, height=2464, framerate=21/1, format=NV12' ! 

   nvvidconv flip-method=2 ! 'video/x-raw, width=816, height=616' ! 

   nvvidconv ! nvegltransform ! nveglglessink -e
   
```
* Python Teste

```
sudo apt install python3-numpy
```

```
sudo apt install libcanberra-gtk-module
```

```
python3 face_detect.py
```
<!--
```

```
-->
