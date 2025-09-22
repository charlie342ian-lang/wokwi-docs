"version": 1,
  "author": "Anonymous maker",
  "editor": "wokwi",
  "parts": [
    { "type": "wokwi-breadboard", "id": "bb1", "top": -281.4, "left": 156.4, "attrs": {} },
    { "type": "wokwi-arduino-mega", "id": "mega", "top": 0.6, "left": -3.6, "attrs": {} },
    {
      "type": "board-ssd1306",
      "id": "oled1",
      "top": -35.26,
      "left": 547.43,
      "attrs": { "i2cAddress": "0x3c" }
    },
    { "type": "wokwi-hc-sr04", "id": "ultrasonic1", "top": -257.7, "left": 399.1, "attrs": {} },
    { "type": "wokwi-servo", "id": "servo1", "top": -414.8, "left": 307.2, "attrs": {} },
    { "type": "wokwi-potentiometer", "id": "pot1", "top": -231.7, "left": 643, "attrs": {} }
  ],
  "connections": [
    [ "mega:GND.2", "bb1:bn.1", "black", [ "v0" ] ],
    [ "mega:5V", "bb1:bp.1", "red", [ "v0" ] ],
    [ "oled1:GND", "bb1:bn.35", "black", [ "v0" ] ],
    [ "oled1:VCC", "bb1:bp.36", "red", [ "v0" ] ],
    [ "mega:20", "oled1:SDA", "green", [ "v-67.2", "h290" ] ],
    [ "oled1:SCL", "mega:21", "green", [ "v-19.2", "h0.3" ] ],
    [ "bb1:31b.j", "bb1:bp.25", "green", [ "v0" ] ],
    [ "bb1:34b.j", "bb1:bn.27", "green", [ "v0" ] ],
    [ "bb1:32b.j", "mega:30", "green", [ "v0" ] ],
    [ "mega:28", "bb1:33b.j", "green", [ "v1.15", "h132.2", "v-172.8" ] ],
    [ "ultrasonic1:VCC", "bb1:31b.f", "", [ "$bb" ] ],
    [ "ultrasonic1:TRIG", "bb1:32b.f", "", [ "$bb" ] ],
    [ "ultrasonic1:ECHO", "bb1:33b.f", "", [ "$bb" ] ],
    [ "ultrasonic1:GND", "bb1:34b.f", "", [ "$bb" ] ],
    [ "servo1:GND", "bb1:bn.2", "black", [ "h0" ] ],
    [ "bb1:bp.3", "servo1:V+", "green", [ "v0" ] ],
    [ "servo1:PWM", "mega:34", "green", [ "h-28.8", "v326.6", "h124.8", "v86.4" ] ],
    [ "pot1:GND", "bb1:52b.f", "", [ "$bb" ] ],
    [ "pot1:SIG", "bb1:53b.f", "", [ "$bb" ] ],
    [ "pot1:VCC", "bb1:54b.f", "", [ "$bb" ] ],
    [ "bb1:52b.j", "bb1:bn.42", "green", [ "v0" ] ],
    [ "bb1:54b.j", "bb1:bp.44", "green", [ "v0" ] ],
    [ "bb1:53b.j", "mega:A15", "green", [ "v192", "h-288", "v134.4", "h-38.4" ] ]
  ],
  "dependencies": {}
}
