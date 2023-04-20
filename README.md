# jump-assignment
## basic
 1. Describe Git branching strategies (Git-flow, single branch, feature branch etc.) which you have used and what purpose it serves.
    - ใช้ feature branch ผสมกับ git-flow  แต่ git-flow จะแบ่งเป็นหลาย env
     เช่น dev, uat, prod
 2. How do you revert a commit that has already been pushed and made public?
    - แตก branch แล้วไป revert จาก commit ที่ต้องการ
 3. How do you normally solve conflicts in a feature branch before merge?
    - ก่อน push feature branch ก็ให้ pull target branch ล่าสุดลงมาก่อน
    - พบว่า conflict ใน vscode จะมี option ให้เลือกว่าจะเอา current, incoming,both หรือ เราจะแก้เอง manual ก็ได้
    - แก้ code เสร็จแล้ว เทสก่อน
    - เทสผ่านแล้ว push เข้า target branch
 4. “200 OK” what does it mean and show the use case of this HTTP Status?
    - เป็น status ที่แสดงว่า request ที่ส่งไปยัง server ด้วย methode ใด ๆ ( GET,PUT, POST, PATCH, DELETE etc. )response จาก server ตอบกลับมายังclient สำเร็จ
    - เช่น การ curl rest api ที่สร้างโดย mock server แล้วได้ return เป็น  json กลับมา
 5. “201 Created” what does it mean and show the use case of this HTTP Status?
    - เป็น status ที่แสดงถึงการสร้างข้อมูลในระบบสำเร็จ
    - เช่น การ add user เช้าระบบ ถ้าตอบ 201 แปลว่าการเพิ่มข้อมูลสำเร็จ
 6. “301 Moved Permanently” what does it mean and show the use case of this HTTP
Status?
    - คือการ redirect จาก url เดิมที่ user เคยใช้ไป url ใหม่อย่างถาวร
    - เช่น website ของเราต้องการเปลี่ยน path หรือ domain
 7. “400 Bad Request” what does it mean and how to identify the problem?
    - เป็น status ที่ server บอกว่า request ที่ client ส่งมาไม่ตรงตาม spec api
    - เช่น การเรียก method GET เป็น POST
 8. “401 Unauthorized” what does it mean and how to identify the problem?
    - เป็นการ บอก client ว่า credential ที่ส่ง หรือ ไม่ส่งมา ไม่มีสิทธิเข้าใช้งานระบบ
    - เช่น การส่ง user/pass หรือ apikey  ไม่ตรงกับ api ที่เรียกใช้
 9. “403 Forbidden” what does it mean and how to identify the problem?
    - เป็นการบอก client ว่า resource ส่วนนี้ client ไม่ได้รับอนุญาติให้เข้าถึงได้
    - เช่นการกำหนดให้บาง client เข้าถึงบาง api ได้เท่านั้นจากการกำหนด scope ให้ client และ api ตรงกัน
 10. “404NotFound”what does it mean and how to identify the problem?
    - เป็น status ที่บอก client ว่า resource ส่วนนี้ไม่มีแล้ว
    - เช่นระบบเรามีการเปลี่ยน route path ใหม่แต่ user ยังจำ path เก่าได้ ทำให้​ได้ error 404
 11. “500 Internal Server Error” what does it mean and how to identify the problem?
    - server แจ้งว่าตัวเองมีปัญหาไม่สามารถตอบ request ได้
    - เช่น Server เป็น nodejs ต่อ db ไม่ได้
 12. “502 Bad Gateway” what does it mean and how to identify the problem?
    - เป็นปํญหา server to server
    - เช่นใน kube  label ที่เขียน ใน ingress ผิดทำให้หา service ไม่เจอ
 13. “503 Service Unavailable” what does it mean and how to identify the problem?
    - เป็นปํญหา server to server
    - เช่นใน kube label ที่เขียนใน service ผิดทำให้หา pod ไม่เจอ หรือ pod ไม่สามารถ start ขึ้นมาเองได้
 14. “504GatewayTimeout” what does it mean and how to identify the problem?
    - เกิดจาก gateway ไม่สามารถรับ request ได้หรือ server  หลััง gateway ทำงานช้าเกินไป
    - เช่น การ loadtest ระบบ ถ้ากำหนด capacity ต่ำกว่าเกณท์ จะทำให้เกิด 504 ได้
