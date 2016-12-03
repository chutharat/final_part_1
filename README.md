# final_part_1 
1.กระบวนการพัฒนาซอฟแวร์ Waterfall   VS Agile
Waterfall	
-	กำหนดเอาไว้อย่างชัดเจน
-	มีข้อกำหนดและเวลาส่งงานที่ชัดเจน  
-	เคร่งครัด มีแบบแผน	
Agile
-	ลูกค้ายังไม่ค่อยรู้เรื่อง ต้องปรับตามสถานการณ์
-	กำหนดส่งสามารถเปลี่ยนแปลงได้
-	ใกล้ชิดลูกค้า พบกันบ่อยๆๆ
-	ใช้การตอบคำถามแบบ SOFA เพื่อง่ายต่อการตัดสินใจ


2. cvs กับ svn ยังด้อยกว่า java ซึ่งมีอะไรที่ไม่จำเป็นมากกว่า ซึ่ง git ยังเหนือกกว่า java
ruby
- ยืดหยุ่นกว่า เพราะ ไม่ต้องประกาศตัวแปร 
- เป็นแบบ dynamic  
- เป็น script  เขียนโค้ดสั้นๆ เน้น dry
java
- ต้องประกาศตัวแปรก่อน จึงจะใช้งานได้
- เป็นแบบ static 
- การเขียนโค้ดเน้นความเป็นระเบียบ
ตรงตามมาตรฐาน
- ต้อง compile ก่อน
ซึ่ง cvs กับ svn ยังยุ่งยากกว่า java เสียอีก


3.git checkout --orphan feature1
git reset --hard 
git add .
git commit #แล้วกรอกรายละเอียด เช่น new feature1
git push origin feature1


4.การ merge จะทำ เมื่อเรา branch เพื่อไปทำ  feature ต่างๆ และต้องการ merge กลับมา ยัง repo กลาง
conflict จะเกิดขึ้น 
เมื่อโปรแกรมเมอร์ 2 คน มาทำงานไฟล์เดียวกัน และแก้ไขโค้ดให้แตกต่างกัน
ดังนั้น  วิธีการแก้ conflict  คือ 1.ให้หัวหน้าตัดสินใจ  2. พูดคุยกันในทีม


5.


6. web application
SaaS App จุดเด่นคือ
ทำงานบนเว็บไซต์  update version ได้ง่าย
package software จุดด้อย
เวลาเปลี่ยน version  เราต้องส่งแผ่นไปอัปเดตทุกที่  
REST (Representational State Transfer) 
เป็นแนวใหม่ในการสร้าง Web Service แบบเรียบง่าย
โดยเรียกใช้ผ่านทาง HTTP Method GET/POST/PUT/DELETE 
และส่งข้อมูลออกมาในรูปของ XML ทำให้ปริมาณข้อมูลที่รับส่ง    
น้อยกว่าการใช้ Protocol SOAP อยู่มาก  
1 UI 1 RESOURCE 1 ACTION


7.MVC
ตอบ M จะใช้ประมวลผล เขียน code
        V แต่งตัวให้สวย
        C ประสานงาน
เริ่มจาก 1 user เข้ามาใช้งาน ผ่านน web นั้นต้องผ่าน Rails router ตรงที่2 Index
นั้นต้องผ่าน controller ที่เป็นตัวประสานงาน จากนั้นจะไปที่ 3 เพื่อไปส่วน Model
เพื่อกำการติดต่อกับ database ตรงที่ 4  จากนั้น Model ส่งกลับมาที่ controller ตรงที่ 5 
controller ทำการติดต่อไปที่ View ตรงที่ 6 จากนั้น View ทำการ ส่งกลับมาที่ 
controller ตรงที่ 7 แล้ว controller ส่งการทำงานมาที่ user ใช้งาน ตรงที่ 8


8.ประโยชน์ของ framework
ไม่ต้องเขียนโค้ดเอง ทำให้คนอื่นใช้งาน ประหยัดเวลาเพราะใช้โค้ดที่มีอยู่แล้ว โค้ดเป็นมาตรฐานคนอื่นสามารถเข้าใจได้ง่าย
Rails เป็น Framework อาจจะมองว่าเป็นที่ ที่มีการวางกรอบการพัฒนาอย่างคร่าวๆ
และมีการรวม Design Pattern ดีๆ เอาไว้ ทำให้การพัฒนา Software ขึ้นมามีระบบระเบียบที่ดี

9.Heroku เป็น Platform as a Service (Paas) ที่ให้เราใช้งานได้ฟรี (มีแบบเสียเงินด้วย)
โดยรองรับภาษาโปรแกรมที่หลากหลาย เช่น Ruby, PHP, Node.js, Python, Java, Clojure, Scala และยังสามารถสร้าง buildpack 
สำหรับภาษาอื่นๆได้ เช่น Lua ที่รันอยู่บน OpenResty ได้อีกด้วย
ข้อดี เช่น นักศึกษาอยากลองเขียนเว็บด้วย PHP แต่ไม่ได้เช่า Hosting ก็สามารถใช้ Heroku ได้ 
หรือแม้แต่บริษัท Start up ที่ไม่อยากวางเครื่องเอง คอนฟิกเอง ก็ใช้ได้ เพราะมันสามารถ scale ให้รองรับผู้ใช้เยอะๆได้โดยง่าย
นอกจากรองรับภาษาโปรแกรมที่หลากหลายแล้ว ตัว Heroku มี App Store ของมันด้วยเรียกว่า add-ons
สำหรับเพิ่มเติมบริการอื่นๆเข้าไปในแอปของเรา เช่น PostgreSQL, MongoDB, Redis เป็นต้น ซึ่งก็มีทั้งฟรี และไม่ฟรีให้เลือกใช้งาน

10. Software มีความสำคัญเกี่ยวข้องกับชีวิตเรามากขึ้นเรื่อยๆ
ไม่ว่าจะเกี่ยวข้องกับวัตถุในชีวิตประจำวันมนุษย์เช่นโทรศัพท์ เครื่องซักผ้า รถยนต์ รถไฟฟ้า หรือเกี่ยวกับธุรกิจเช่นธนาคาร
ดังนั้นการสร้าง Software ต้องสร้างให้ได้คุณภาพดี ไว้ใจได้นักศึกษากล้านั่งรถไฟฟ้าที่ตนเองเป็นคนเขียน Software ควบคุมการเบรคหรือไม่
ปัญหาการสร้าง Software ในปัจจุบันยังเป็นวิกฤต คือไม่น่าเชื่อถือ ทำงานไม่ถูกต้องไม่ได้ตามที่คาดไว้ สร้างไม่สำเร็จ ไม่ทันตามกำหนดเวลา งบประมาณ
หรือต้องล้มเลิกกลางคันจำนวนมาก ยกตัวอย่างเช่น ระบบควบคุมการส่งยานอวกาศ Ariane 5 ของยุโรปต้องกดระเบิดยานทิ้งเพราะวิถีการเคลื่อนที่ผิดพลาดมาก 
ระบบจัดการรถพยาบาลของLondon (London Ambulance) ที่ทำงานไม่ถูกต้องและต้องยกเลิกการใช้หลังเสียเงินไปจำนวนมาก 
ระบบเอ็กซเรย์ Therac-25 ทำให้คนตายไป 2 คนจากการใช้รังสีมากเกินไป ระบบป้องกันมิซซาย Patriot มีข้อผิดพลาดไม่สามารถป้องกันขีปนาวุธ scud
ทำให้ทหารอเมริกาตายไป 28 บาดเจ็บ 98 .ในปี 1991 ระหว่างสงครามอิรัก วันที่ 9 พ.ย. 1979 
ระบบควบคุมการสั่งการทางทหาร (WWMCCS World Wide Military Command and Control System) 
ของสหรัฐเกือบสั่งยิงหขีปนาวุธไปที่รัสเซียเนื่องจากระบบตีความว่ารัสเซียได้ปล่อยขีปนาวุธมาที่อเมริกา IBM ไม่สามารถพัฒนาระบบให้กรมศุลกากรของไทยได้สำเร็จ 
ล่าช้าไปนาน โชคดีตกลงกันได้ จากเหตุการณ์ต่างๆ แสดงให้เห็นวิกฤตของการสร้าง Software ปึ ค.ศ. 1968 NATO

