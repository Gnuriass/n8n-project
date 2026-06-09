# Mr.Guide: AI Automation ChatBot Platform for Digital Travel

**Mr.Guide** เป็นแพลตฟอร์มแนะนำการท่องเที่ยวอัจฉริยะที่พัฒนาขึ้นเพื่อแก้ปัญหา "สภาวะข้อมูลล้นหลาม" (Information Overload) โดยการใช้ AI และ Automation เข้ามาช่วยวิเคราะห์และแนะนำสถานที่ท่องเที่ยวที่ตอบโจทย์ความสนใจเฉพาะบุคคลผ่านแอปพลิเคชัน LINE

## 🌟 Features
- **Personalized Recommendation:** วิเคราะห์ความต้องการผู้ใช้และแนะนำสถานที่ท่องเที่ยวได้แม่นยำ (ความแม่นยำ ~85-90%)
- **Real-time Automation:** ทำงานแบบอัตโนมัติผ่าน n8n Workflow
- **Seamless Integration:** เชื่อมต่อกับ LINE Messaging API สำหรับการโต้ตอบกับผู้ใช้
- **Data-Driven Insights:** บันทึกประวัติการสนทนาเพื่อนำมาวิเคราะห์พฤติกรรมและความต้องการในอนาคต

## 🏗️ System Architecture
ระบบถูกออกแบบโดยแบ่งเป็น Layer ต่างๆ ดังนี้:
- **Input Layer:** รับข้อมูลผ่าน LINE Webhook
- **AI Agent Layer:** ประมวลผลด้วย Gemini Model เพื่อวิเคราะห์เจตนา (Intent) ของผู้ใช้
- **Data Layer:** ใช้ Google Sheets และ PDI Database ในการจัดเก็บข้อมูลผู้ใช้และสถานที่
- **Business Logic Layer:** จัดการ Workflow การจอง (Booking), การวางแผน (Planning) และการแชท
- **Analytics Layer:** ติดตาม Conversion Flag, Happiness Score และบันทึก Logs การสนทนา
  ![System Architecture](./block-diagram.jpg)

## 🛠️ Tech Stack
- **n8n:** ระบบหลักในการทำ Automation Workflow
- **Google Gemini AI:** สมองหลักในการวิเคราะห์และประมวลผลภาษา (LLM)
- **Docker:** ใช้สำหรับจำลองสภาพแวดล้อม (Local Environment) ในการรันระบบ
- **Ngrok:** สำหรับทำ Webhook Connectivity เชื่อมต่อกับ LINE API อย่างปลอดภัย
- **Line Messaging API:** ช่องทางหลักในการติดต่อกับผู้ใช้งาน
- **Google Sheets:** สำหรับจัดเก็บข้อมูลฐานข้อมูลเบื้องต้น

## 🚀 Getting Started

### Prerequisites
- [Docker](https://www.docker.com/) & [Docker Compose](https://docs.docker.com/compose/)
- บัญชี [LINE Developers](https://developers.line.biz/)
- [Gemini API Key](https://aistudio.google.com/)

### Installation
1. Clone repository นี้ลงเครื่อง:
   ```bash
   git clone [https://github.com/Gnuriass/n8n-project.git](https://github.com/Gnuriass/n8n-project.git)
   cd n8n-project
