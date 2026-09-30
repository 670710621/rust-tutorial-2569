# Rust Tutorial Project — Principles of Programming Languages

> **กลุ่มที่:** 14
> **Topic No.:** 14
> **Topic Name:** Error Handling: Option & Result
> **ประเด็นหลักที่ควรครอบคลุม:** Option, Result, Some/None, Ok/Err, error propagation, ?

---

## 1. Members

| # | Name | Student ID | GitHub Username | Main Responsibility |
|---|---|---|---|---|
| 1 | นายกันต์ธร บุตรเบ้า | 670710619 | `@[กรอก GitHub username]` | Concept + Short Code Illustration (สรุปแนวคิดหลัก + โค้ดตัวอย่างสั้น) |
| 2 | นางสาวฉันทณัฏฐ วิชพันธุ์ | 670710620 | `@[กรอก GitHub username]` | Detailed Code + Live Demo (โค้ดเชิงลึก + สาธิตสด) |
| 3 | นางสาวณัฐกฤตา บุญมี | 670710621 | `@[กรอก GitHub username]` | Rust vs Other Language + PPL Analysis (เปรียบเทียบภาษา + วิเคราะห์เชิง PPL) |
| 4 | นายณัฐวีร์ บุญยินดี | 670710622 | `@[กรอก GitHub username]` | Exercises + Common Mistakes + Challenge (แบบฝึกหัด + ข้อผิดพลาดที่พบบ่อย + คำถามท้าทาย) |

> แก้ไข GitHub Username ของแต่ละคนให้ตรงกับบัญชีจริงก่อนเริ่มทำงาน (ผู้สอนจะใช้คอลัมน์นี้เชิญเป็น collaborator ของ repository)

---

## 2. Learning Objectives

หลังจากศึกษา Topic นี้แล้ว ผู้เรียนสามารถ:

1. `[อธิบายแนวคิดสำคัญได้]`
2. `[เขียนโปรแกรม Rust ที่เกี่ยวข้องได้]`
3. `[วิเคราะห์พฤติกรรม/กฎของภาษาได้]`
4. `[เปรียบเทียบ Rust กับภาษาอื่นได้]`

---

## 3. Introduction

`[เขียนเนื้อหาที่นี่ — ใช้โครงสร้างเดียวกับ rust_tutorial_template.md ฉบับเต็มที่ผู้สอนแจกให้]`

---

*โครงสร้างเอกสารฉบับเต็ม (Key Concepts, Runnable Code Examples, Common Mistakes, Exercises, PPL Perspective, Rust vs Other Language, References, AI Usage Declaration, GitHub Contribution, Final Checklist) ให้ทำต่อจากจุดนี้ตาม Template หลักของวิชา (`rust_tutorial_template.md`) ที่แนบมากับใบมอบหมายงาน*


---

## 3. PPL

9.1 Syntax
ภาษา Rust ใช้แนวคิดการคืนค่าผลลัพธ์ (Return Values) ในการจัดการข้อผิดพลาดผ่านชนิดข้อมูล Option และ Result โดยไม่มีการใช้โครงสร้างไวยากรณ์เฉพาะสำหรับการโยน Exception (เช่น คีย์เวิร์ด try, catch, throw) แต่ประยุกต์ใช้โครงสร้างไวยากรณ์พื้นฐานร่วมกับกลไก Pattern Matching และ ? operator ดังนี้
•	การนิยามโครงสร้างข้อมูลด้วย Enum และ Generic Parameters (<T, E>) โดยใช้ไวยากรณ์ Enum ร่วมกับ Generic Parameters (<T,  E>) เพื่อสร้างประเภทข้อมูลที่ยืดหยุ่น รองรับข้อมูลชนิดใดก็ได้ สำหรับใช้แทนกรณีการทำงานที่สำเร็จและกรณีที่เกิดข้อผิดพลาด
•	การควบคุมทิศทางโปรแกรมด้วย Pattern Matching โดยใช้ไวยากรณ์ match และ if let เป็นโครงสร้างหลักในการควบคุมทิศทางโปรแกรม ตรวจสอบกรณีที่เกิดข้อผิดพลาด และแกะค่าข้อมูลออกจาก Option และ Result
•	การจัดการและส่งต่อข้อผิดพลาดด้วย ? Operator โดยใช้เครื่องหมาย ? เพื่อลดรูปโค้ดการตรวจสอบ Result หรือ Option แทนการเขียนคำสั่ง match ที่ยาว โดยทำงานแบบ Short-circuiting ซึ่งจะส่งคืนข้อผิดพลาดกลับไปยังฟังก์ชันที่เรียกใช้งานทันทีโดยอัตโนมัติ

