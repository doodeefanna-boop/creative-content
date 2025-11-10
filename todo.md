# Creative Ads Manager - TODO List

## Phase 1: Database Schema & Planning
- [x] ออกแบบ database schema สำหรับเก็บข้อมูลสินค้า
- [x] ออกแบบ database schema สำหรับเก็บประวัติการสร้างคอนเทนต์
- [x] ออกแบบ database schema สำหรับเก็บข้อมูลรูปภาพที่อัปโหลด

## Phase 2: Backend API Development
- [x] สร้าง API สำหรับจัดการข้อมูลสินค้า (CRUD)
- [x] สร้าง API สำหรับสร้างแคปชั่น Facebook (หลายบริบท)
- [x] สร้าง API สำหรับสร้าง Prompt สำหรับ Sora2 (2 scenes, same face)
- [x] สร้าง API สำหรับสร้าง Prompt สำหรับรูปภาพสินค้า
- [x] สร้าง API สำหรับสร้างบทรีวิวเสียงภาษาไทย (30-50 วินาที)
- [x] สร้าง API สำหรับอัปโหลดและวิเคราะห์รูปภาพ
- [x] เชื่อม LLM API สำหรับสร้างเนื้อหา (ใช้ built-in Manus Forge API)

## Phase 3: Frontend UI Development
- [x] ออกแบบและสร้างหน้า Dashboard หลัก
- [x] สร้างฟอร์มกรอกข้อมูลสินค้า (ชื่อ, รายละเอียด, กลุ่มเป้าหมาย, โทนภาพ, ฯลฯ)
- [x] สร้างหน้าแสดงผลแคปชั่น Facebook พร้อมตัวเลือกหลายบริบท
- [x] สร้างหน้าแสดงผล Sora2 Prompt (2 scenes) พร้อม character description
- [x] สร้างหน้าแสดงผล Image Prompt พร้อมตัวเลือกหลายบริบท
- [x] สร้างหน้าแสดงผลบทรีวิวเสียงพร้อมตัวเลือกหลายบริบท
- [x] สร้างฟีเจอร์อัปโหลดรูปภาพและแสดงผลการวิเคราะห์
- [x] สร้างระบบจัดเก็บและแสดงประวัติการสร้างคอนเทนต์
- [x] เพิ่มฟีเจอร์ Copy to Clipboard สำหรับทุก output
- [x] เพิ่มฟีเจอร์ Export เป็นไฟล์ (TXT, JSON)

## Phase 4: Testing & Bug Fixes
- [x] ทดสอบการกรอกข้อมูลครั้งเดียวและสร้างคอนเทนต์ทุกประเภท
- [x] ทดสอบการอัปโหลดและวิเคราะห์รูปภาพ
- [x] ทดสอบความถูกต้องของ Prompt ที่สร้างขึ้น (Same Face 100%)
- [x] ทดสอบการทำงานของฐานข้อมูลที่เชื่อมต่อกัน
- [x] แก้ไขบั๊กและปรับปรุง UX

## Phase 5: Deployment
- [x] สร้าง checkpoint สำหรับ deployment
- [x] ทดสอบการทำงานบน production environment
- [x] ส่งมอบ URL ให้ผู้ใช้งาน

## Additional Features (Optional Enhancements)
- [ ] เพิ่มระบบ Template สำหรับแต่ละประเภทสินค้า
- [ ] เพิ่มฟีเจอร์ A/B Testing สำหรับแคปชั่น
- [ ] เพิ่มระบบ Analytics เพื่อติดตามประสิทธิภาพของคอนเทนต์
- [ ] เพิ่มฟีเจอร์ Batch Processing สำหรับสร้างคอนเทนต์หลายสินค้าพร้อมกัน
- [ ] เพิ่มฟีเจอร์ล็อคลักษณะนางแบบ/นายแบบที่แม่นยำยิ่งขึ้น

## Phase 6: Generate AI Images Feature
- [x] เพิ่ม database schema สำหรับเก็บรูปภาพที่สร้างด้วย AI
- [x] เพิ่ม API สำหรับสร้างรูปภาพจากรูปอ้างอิง (Image-to-Image)
- [x] เพิ่มหน้า UI สำหรับอัปโหลดรูปอ้างอิงและเขียน Prompt
- [x] เพิ่มฟีเจอร์แสดงผลรูปภาพที่สร้างขึ้น พร้อม Download
- [x] ทดสอบการคงเอกลักษณ์เดิมของสินค้า/บุคคล
- [x] ทดสอบการเปลี่ยนฉากหลัง ท่าทาง บุคลิกภาพ

## Bug Fixes
- [x] แก้ไข error ใน Home.tsx - Cannot update component while rendering

## Bug Fixes - Generate AI Images
- [x] แก้ไขปัญหาปุ่ม "สร้างรูปภาพ" ที่ไม่สามารถกดได้

## Feature: Batch Generation
- [x] เพิ่ม UI สำหรับเลือกจำนวนรูปที่ต้องการสร้าง (1-5 รูป)
- [x] ปรับปรุง backend API สำหรับรองรับ Batch Generation
- [x] แสดงผล progress bar ขณะสร้างรูปภาพหลายรูป
- [x] ทดสอบการสร้างรูปภาพหลายรูปพร้อมกัน

## Feature: Template Prompt Library
- [x] สร้าง Prompt Templates จัดหมวดหมู่ตามบริบท (ฉากหลัง, นางแบบ, ท่าทาง, สไตล์, แสงสว่าง)
- [x] เพิ่ม UI สำหรับเลือก Template Prompt
- [x] เพิ่มฟีเจอร์ Apply Template ลงใน Prompt textarea
- [x] ทดสอบการใช้งาน Template Prompt Library

## Critical Bug Fix - Generate AI Images Button
- [x] ตรวจสอบและแก้ไข import useState ที่ซ้ำใน AIImageGenerator.tsx
- [x] ตรวจสอบ console errors และแก้ไขปัญหาทั้งหมด
- [x] ทดสอบการกดปุ่ม "สร้างรูปภาพ" ให้แน่ใจว่าทำงานได้จริง
- [x] ทดสอบการสร้างรูปภาพจริงจากรูปอ้างอิง

## UX Improvement - Generate AI Images
- [x] เพิ่มข้อความแจ้งเตือนเมื่อยังไม่ได้เลือกรูปอ้างอิง
- [x] ปรับปรุงการแสดงผลปุ่มให้ชัดเจนว่าต้องเลือกรูปก่อน
- [x] เพิ่ม tooltip หรือ helper text เพื่ออธิบายขั้นตอนการใช้งาน
- [x] ทดสอบ UX ให้แน่ใจว่าผู้ใช้เข้าใจขั้นตอนการใช้งาน

## Feature: Multiple Reference Images
- [x] ปรับปรุง UI ให้เลือกรูปอ้างอิงได้หลายรูพพร้อมกัน
- [x] เพิ่มระบบแสดงรูปที่เลือกทั้งหมดพร้อมปุ่มลบ
- [x] ปรับปรุง backend API ให้รองรับการส่งหลายรูปอ้างอิง
- [x] ทดสอบการสร้างรูปภาพจากหลายรูปอ้างอิง
- [x] เพิ่ม Template Prompt สำหรับการใช้หลายรูปอ้างอิง

## Feature: Bulk Export
- [x] เพิ่ม backend API สำหรับ Export ข้อมูลทั้งหมดเป็น JSON
- [x] เพิ่ม backend API สำหรับสร้าง ZIP file รวมรูปภาพและข้อมูล
- [x] เพิ่ม frontend UI ปุ่ม "Export ทั้งหมด" ในหน้ารายละเอียดสินค้า
- [x] แสดง Loading state ขณะสร้าง ZIP file
- [ ] ทดสอบการ Export ข้อมูลทั้งหมด
- [ ] ทดสอบการดาวน์โหลด ZIP file

## Bug Fix - AI Image Download
- [x] ตรวจสอบสาเหตุที่ Chrome บล็อกการดาวน์โหลดรูปภาพ
- [x] แก้ไขวิธีการดาวน์โหลดรูปภาพให้ปลอดภัย
- [x] ทดสอบการดาวน์โหลดรูปภาพที่สร้างด้วย AI
