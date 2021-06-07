# Project-MicroSmart
Project : IoT By Microtronic.biz

## NodeMCU ESP8266 12E

เรียกใช้งาน library 

#include <ESP8266WiFi.h>
#include <PubSubClient.h>

กำหนดค่าการเชื่อมต่อ wifi

const char* ssid = "admin"; 
const char* password =  "12345678";

กำหนดค่าเซิร์ฟเวอร์ MQTT เราใช้เซิร์ฟเวอร์ Eclipse MQTT สำหรับโครงการนี้ ซึ่งเป็นสาเหตุที่ทำให้ที่อยู่เซิร์ฟเวอร์เป็น“mqtt.eclipse.org” แต่ถ้าคุณวางแผนที่จะใช้เซิร์ฟเวอร์อื่น เช่น Mosquitto, Adafruit คุณสามารถแทนที่ด้วยที่อยู่เซิร์ฟเวอร์และหมายเลขพอร์ตเฉพาะของคุณ

const char* mqtt_server = "mqtt.eclipse.org"; 
const int mqtt_port = 1883;

ถัดไป อินสแตนซ์จะถูกสร้างขึ้นสำหรับคลาส _WiFiClient_ และ _PubSubClient_



ในส่วน _setup()_ เราเรียก _WiFi.begin()_ ก่อน การเรียกวิธีนี้จะเชื่อมต่อ ESP กับ HotSpot ที่คุณต้องการ


ตรวจสอบการเชื่อมต่อเครือข่ายโดยใช้  _WiFi.status ()_ หลังจากการเชื่อมต่อสำเร็จ ข้อความจะถูกพิมพ์บน Serial Monitor พร้อม SSID ของเครือข่ายที่เชื่อมต่อ


สร้างโบรกเกอร์ เราได้ใช้เมธอด _setServer_ วิธีนี้ใช้สองอาร์กิวเมนต์ที่เราได้กำหนดไว้ล่วงหน้าแล้ว ตอนนี้ ถ้าเราต้องการรับข้อความจากเซิร์ฟเวอร์ เราต้องสร้างฟังก์ชันเรียกกลับ เพื่อที่เราจะใช้ _setCallback (callback)_ วิธีการ