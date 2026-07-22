# 1. Principles and practices

## Assignment
* download, read, and sign the student agreement,and commit the file to your repo
* work through a git tutorial
* build a personal site in the class archive,describing you and your final project


This week I worked on defining my final project idea and started to getting used to the documentation process. My inspiration comes from the picture below:  
<img src="https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week01/%E6%A6%82%E5%BF%B5%E5%9B%BE.jpg" width = "80%">  
This is actully a LED device which can be freely combined as you wish.With touch sensor inside,you can turn on and turn off the light with just a touch.  

## The hive table
Here is my concept:  
<img src="https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week01/sketch.jpg" width = "80%">  

### Key word
* Separable
* Main controller
* NeoPixel
* Touch sensor
* MIDI controler
* Digital speaker

### Description
&emsp;The desktop adopts a **modular design concept**. The connection between each module is the same (the same mechanical structure and the same communication protocol), so it can be **freely combined in shape**. The surface of the table consists of many hexagonal modules. Each hexagonal module is identical in shape. Each table is equipped with a cltroller hexagon module and several combination hexagon modules.  
&emsp;When you want a rectangular shape table, you can use 9 or more modules to make it. When you want a round shape table, you only need 7 pieces. All you need to do is **split and assemble the modules** according to the shape you want. There is a matching slot between each module, which can not only ensure the structural rigidity of the table surface, but also can easily connect the cables required for electronic components. After the table surface is spliced, there is a bayonet under each hexagonal module that can fix the support. You can install the table support under any hexagonal module, as long as the table can be held firmly. And each support can also be adjusted up and down.  
&emsp;Each hexagonal combination module is equipped with: LED strips (RGB) and touch sensors. Each hexagonal control module is equipped with: Arduino controller, MIDI controller, voice recognition board, digital speakers. Of course, it is also equipped like other modules: with LED strip (RGB) and touch sensor.  
&emsp;In addition to being freely combinable and the use of LED light can bring great visual effects. There are **two distinctive functions**:  

* You can use the LED light effect to play some games.  
* When connected other extra device like [Kinect](https://en.wikipedia.org/wiki/Kinect), it can be turned into an interactive device.  

<img src = "https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week01/RGB_LED.png" width = "30%">   <img src = "https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week01/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20200210013959.png" width = "30%">


To see more image view in [**Galley**](http://academany.fabcloud.io/fabacademy/2020/labs/oshanghai/students/pan-cheng/assignments/week01/#Gallery).

<a href = ""></a>

### Materials

| Qty |  Name   |  Description   |
|-----|---------|  -----------   |
| Several  | Aluminum alloy  | Frame |
| Several  | PVC  |  Surface  |
| 1   | PCBs  |  Controller |
| Several   | NeoPixel   | Light |
| Several   | Touch sensor | Input |
| 1   | Digital speaker | Output |

### Code Example

```
byte noteON = 144;//note on command

void setup() {
  Serial.begin(9600);
}

void loop() {
  MIDImessage(noteON, 60, 100);//turn note on
  delay(300);//hold note for 300ms
  MIDImessage(noteON, 60, 0);//turn note off (note on with velocity 0)
  delay(200);//wait 200ms until triggering next note
}

//send MIDI message
void MIDImessage(byte command, byte data1, byte data2) {
  Serial.write(command);
  Serial.write(data1);
  Serial.write(data2);
}
```

<a name = "Gallery"></a>
  
  
## Gallery
![image](https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week01/%E8%AE%BE%E8%AE%A1%E5%9B%BE.jpg)  
![idea1.jpg](https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week01/idea1.jpg)  
![idea2.jpg](https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week01/idea2.jpg)  
![image](https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week01/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20200209000520.png)

## 3D models

<iframe allowfullscreen webkitallowfullscreen width="640" height="480" frameborder="0" seamless src="https://p3d.in/e/NvR5q+shadeless"></iframe>

---
## Useful links

The tutorials of [How to edit your website](https://class.textile-academy.org/tools/tutorials/gitlab/)  

The tutorials of [Markdown](https://www.runoob.com/markdown/md-tutorial.html)  

## Reference
[elena-cardiel's website](https://fabacademy.org/2019/labs/leon/students/elena-cardiel/diary.html)