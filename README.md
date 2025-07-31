# salesforce-mock-oms

ตัวอย่าง Code เพื่อแสดงประสบการณ์การเชื่อมระบบ (Online Platform) เข้ากับ Salesforce 

โดยใช้
- Salesforce Apex Class 
- REST API Callout

## ฟีเจอร์หลัก
- รับข้อมูลการสั่งซื้อสินค้าผ่าน Platform Shopee
- Mapping ข้อมูลเข้า Salesforce Object
- ส่งข้อมูลต่อไปยังระบบ ERP 
- สร้าง/อัปเดตสถานะคำสั่งซื้อเพื่อนำไปใช้งานในส่วนอื่นๆ

## หมายเหตุ
โค้ดนี้เป็นตัวอย่างจำลองจากงานจริงที่เคยทำ โดยไม่ใช้ข้อมูลหรือระบบภายในของบริษัทใด ๆ และไม่สามารถเชื่อมต่อกับ Platfrom ได้จริง
สามารถเข้าดู code ได้ที่ MockCodeSF/force-app/main/default/classes


## 
[ Online Platform ]
        |
        | (REST API Webhook Integration)
        v
[ Apex Integration Service ]
        |
        |-- Callout to External API
        |-- Data Mapping to Salesforce Object (e.g. Order)
        |
        v
[ Salesforce Service Cloud ]
        |
        |-- Record Created/update (e.g. Order)
        |
        v
[ Agent View ]
