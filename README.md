# Creative Ads Manager

โครงการนี้คือระบบจัดการโฆษณาเชิงสร้างสรรค์แบบ Full-Stack ที่พัฒนาขึ้นเพื่อช่วยในการจัดการและสร้างสรรค์แคมเปญโฆษณาอย่างมีประสิทธิภาพ

## โครงสร้างโปรเจค

โปรเจคนี้แบ่งออกเป็นส่วนหลักๆ ดังนี้:

- **`client/`**: ส่วนหน้าบ้าน (Frontend) พัฒนาด้วย React/TypeScript และ Vite
- **`server/`**: ส่วนหลังบ้าน (Backend) พัฒนาด้วย Node.js/TypeScript และ tRPC
- **`drizzle/`**: ไฟล์คอนฟิกและ Migration ของ Drizzle ORM สำหรับจัดการฐานข้อมูล
- **`shared/`**: โค้ดและประเภท (Types) ที่ใช้ร่วมกันระหว่าง Client และ Server

## การตั้งค่าและติดตั้ง

### ข้อกำหนดเบื้องต้น

คุณต้องติดตั้งซอฟต์แวร์ต่อไปนี้ในเครื่องของคุณ:

- [Node.js](https://nodejs.org/) (แนะนำเวอร์ชัน LTS)
- [pnpm](https://pnpm.io/) (ใช้สำหรับจัดการแพ็คเกจ)
- ฐานข้อมูล PostgreSQL (หรือฐานข้อมูลที่รองรับโดย Drizzle ORM)

### ขั้นตอนการติดตั้ง

1.  **โคลน Repository**
    ```bash
    git clone [URL_TO_THIS_REPO]
    cd creative_ads_manager
    ```

2.  **ติดตั้ง Dependencies**
    ```bash
    pnpm install
    ```

3.  **ตั้งค่า Environment Variables**
    สร้างไฟล์ `.env` ในรูทของโปรเจค และกำหนดค่าตัวแปรสภาพแวดล้อมที่จำเป็น เช่น:
    ```
    # Database Configuration
    DATABASE_URL="postgresql://user:password@host:port/database_name"

    # API Keys (ตัวอย่าง)
    OPENAI_API_KEY="your_openai_api_key"
    # ... ตัวแปรอื่นๆ ที่จำเป็นสำหรับ server/_core/env.ts
    ```

4.  **รัน Database Migrations**
    ใช้ Drizzle-kit เพื่อสร้างตารางในฐานข้อมูลของคุณ:
    ```bash
    pnpm run db:migrate
    ```

### การรันโปรเจค

1.  **รัน Server**
    ```bash
    pnpm run dev:server
    ```

2.  **รัน Client**
    เปิด Terminal ใหม่ และรัน:
    ```bash
    pnpm run dev:client
    ```

แอปพลิเคชันจะเปิดขึ้นที่ `http://localhost:5173` (หรือพอร์ตอื่นตามที่ Vite กำหนด)

## การใช้งานกับ GitHub Pages

โปรเจคนี้เป็นแบบ Full-Stack (Client + Server) ซึ่ง **GitHub Pages รองรับเฉพาะส่วน Client (Frontend) ที่เป็น Static Content เท่านั้น** ดังนั้นคุณจะไม่สามารถรันส่วน Backend (Server) บน GitHub Pages ได้

หากคุณต้องการแสดงผลส่วน Frontend บน GitHub Pages:

1.  **Build โปรเจค Client**:
    ```bash
    pnpm run build:client
    ```
    คำสั่งนี้จะสร้างไฟล์ Static Content ในโฟลเดอร์ `dist/public`

2.  **ตั้งค่า GitHub Pages**:
    ไปที่ **Settings** -> **Pages** ใน GitHub Repository ของคุณ และตั้งค่าให้ใช้โฟลเดอร์ `dist/public` เป็นแหล่งที่มา (Source) สำหรับการ Deploy

3.  **ข้อจำกัด**:
    *   ฟีเจอร์ใดๆ ที่ต้องมีการเชื่อมต่อกับ Backend (เช่น การดึงข้อมูล, การบันทึกข้อมูล, การใช้ tRPC) จะไม่สามารถทำงานได้
    *   GitHub Pages เหมาะสำหรับการแสดงผลหน้าตา (UI) ของแอปพลิเคชันเท่านั้น

## License

โปรเจคนี้อยู่ภายใต้เงื่อนไขของ [MIT License](LICENSE).

## สถานะ To-Do

ดูรายการสิ่งที่ต้องทำและฟีเจอร์ที่กำลังพัฒนาได้ที่ไฟล์ [todo.md](todo.md)
