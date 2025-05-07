# NeMo TTS Primer – สรุปสำหรับการพรีเซนต์

โครงการนี้เป็นการสรุปการใช้งาน **Text-to-Speech (TTS)** ด้วยไลบรารี [NVIDIA NeMo](https://developer.nvidia.com/nemo) สำหรับนำเสนอในรูปแบบเข้าใจง่าย พร้อมสคริปต์ใช้ประกอบสไลด์พรีเซนต์

---

## 🟦 1. Setup
**สรุป:**  
ก่อนเริ่มใช้งาน จำเป็นต้องติดตั้ง NeMo library และ dependencies อื่น ๆ ผ่านคำสั่ง `pip install`. Notebook นี้ออกแบบให้ใช้งานบน Jupyter หรือ Colab ได้เลย

---

## 🟦 2–4. Introduction to TTS / What is TTS? / TTS Pipeline
**สรุป:**  
TTS (Text-to-Speech) คือเทคโนโลยีแปลงข้อความเป็นเสียงพูด โดยมี 3 ขั้นตอนหลัก:
1. **Text Processing:** ทำความสะอาดและแปลงข้อความ
2. **Spectrogram Generation:** สร้างภาพคลื่นเสียง
3. **Audio Synthesis:** แปลง spectrogram เป็นเสียงจริง

---

## 🟦 5. Text Normalization (TN)
**สรุป:**  
คือขั้นตอนปรับข้อความให้เหมาะกับการอ่าน เช่น แปลงตัวเลข "123" เป็น "หนึ่งร้อยยี่สิบสาม"

---

## 🟦 6. Grapheme to Phoneme (G2P)
**สรุป:**  
แปลงตัวอักษร (graphemes) เป็นเสียงพูด (phonemes) เช่น `"cat"` → `/k/ /æ/ /t/`  
- **OOV:** คำที่ไม่เคยเจอมาก่อน  
- **Heteronyms:** คำที่สะกดเหมือนกันแต่เสียงต่าง เช่น “lead”

---

## 🟦 7. Spectrogram Synthesis
**สรุป:**  
แปลงข้อความเป็น spectrogram โดยใช้โมเดล เช่น Tacotron2 หรือ FastPitch ซึ่งควบคุมจังหวะของเสียง

---

## 🟦 8. Audio Synthesis (Spectrogram Inversion)
**สรุป:**  
ใช้ Vocoder (เช่น WaveNet, HiFi-GAN) เพื่อแปลง spectrogram กลับเป็นเสียงจริง

---

## 🟦 9. Model Evaluation
**สรุป:**  
วัดคุณภาพเสียงที่สร้างขึ้น เช่นใช้ **Mean Opinion Score (MOS)** ให้มนุษย์ให้คะแนนความสมจริง

---

## 🟦 10–11. Additional Resources & References
**สรุป:**  
แนะนำแหล่งเรียนรู้เพิ่มเติมจาก NVIDIA, บทความวิจัย, และตัวอย่าง Notebook

---

## 📎 หมายเหตุ:
- สามารถเปิดดู Notebook ได้ในไฟล์ `NeMo_TTS_Primer.ipynb`
- ต้องการทดลองรัน → แนะนำใช้ Google Colab

