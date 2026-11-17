# 🏪 คุมกฎกะดึก · Night Shift Rules

> **TH** เกมสยองขวัญพิกเซลอาร์ตสไตล์ FNAF ที่เล่นบนเบราว์เซอร์ — คุณคือพี่โชติ ผู้จัดการมินิมาร์ท ต้องดูกล้องวงจรปิด 4 ตัว และทำตามสมุดกฎให้รอดจนถึง 6 โมงเช้า
> **EN** A pixel-art, FNAF-style horror game that runs in your browser — you're Chot, a minimart manager watching 4 CCTV cameras and following the night's rulebook until 6 AM.

**▶ เล่นเลย / Play now: https://napmeks.github.io/kumkot/**

`PUBLIC BETA` · เล่นฟรี ไม่ต้องติดตั้ง ใช้ได้ทั้งมือถือและคอมพิวเตอร์ · Free, no install, works on mobile and desktop.

---

## 🇹🇭 ภาษาไทย

### เกมนี้คืออะไร

คุมกฎกะดึกเป็นเกมที่ผมทำเล่นเองหลังได้แรงบันดาลใจจากซีรีส์ไทย *The Rules* ของ Viu คุณรับบทผู้จัดการ "พี่โชติ" ที่เฝ้าร้านมินิมาร์ทตอนกลางคืนผ่านกล้อง 4 ตัว ลูกน้องแต่ละคนมีกฎของตัวเอง ถ้ามีอะไรผิดปกติ คุณต้องรีบรับมือก่อนแถบเตือนเต็ม

### วิธีเล่น

- ดูกล้องทั้ง 4 ตัว ถ้ามีอะไรผิดปกติ แถบใต้ภาพจะค่อยๆ เต็ม (เขียว → แดง)
- แตะกล้องเพื่อดู แล้วใช้เครื่องมือตามกฎ เช่น วิทยุ ธูป ปิดไฟ ล็อกกลอน หรือสั่งพนักงาน
- ถ้าจอกล้องดำ (ไม่มีคนประจำ) ให้กดกระดิ่งเรียกพนักงานที่ว่างมาประจำ
- เปิดสมุดกฎประจำคืนนี้ แล้วทำตามให้ครบ เพราะกฎของแต่ละคืนไม่เหมือนกัน
- รอดให้ถึง 6 โมงเช้า

### โหมดเกม

| โหมด | รายละเอียด |
|---|---|
| **Normal** | 5 คืน กฎและความยากเพิ่มขึ้นเรื่อยๆ เหมาะกับผู้เล่นใหม่ |
| **Survivor** | โหมดท้าทายสำหรับคนที่เล่นโหมดปกติจบแล้ว ผีดุขึ้นกว่าเดิม มีข้อความเตือนก่อนเข้า |

### เรื่องราวการพัฒนา

โปรเจกต์นี้เริ่มจากไอเดียเล็กๆ ว่า "ถ้าได้เป็นคนคุมกล้องในซีรีส์ The Rules จะเป็นยังไง" แล้วค่อยๆ ต่อยอดเป็นเกมจริงโดยคุยกับ Claude ทีละรอบ:

1. **V1** ต้นแบบแรก มีกล้อง ลูกน้อง และสมุดกฎพื้นฐาน
2. **V2** เพิ่มโหมดและเครื่องมือ ปรับสมดุลความยาก
3. **V3 → Public Beta** รอบสุดท้ายก่อนปล่อย ปรับตามคอมเมนต์ผู้เล่นทดลอง เช่น
   - สมุดกฎกับวิธีเล่นยาวเกิน → ตัดให้กระชับ
   - เพิ่มเตือนก่อนเข้า Survivor เพราะไม่เหมาะกับคนเล่นครั้งแรก
   - ปรับ layout ให้พอดีหน้าจอมือถือ ไม่ต้องเลื่อนหรือขยับตอนเล่น
   - แก้ปุ่มแชร์ให้ใช้ได้ในหลายสภาพแวดล้อม
   - ย่อแถบสถานะให้เหลือบรรทัดเดียว อ่านง่าย

ภาพพิกเซลทั้งหมดวาดด้วยโค้ด (สไปรต์เป็นตัวอักษรเรียงกันแล้ววาดลง canvas) ไม่มีไฟล์ภาพของเกม ทดสอบหน้าตาและพฤติกรรมด้วย Playwright ก่อนปล่อยทุกรอบ

### ข้อมูลเทคนิค

- ไฟล์ HTML เดียว (`index.html`) ไม่ต้องติดตั้ง library ใด
- มีภาษาไทยและอังกฤษ สลับได้ในเกม
- โฮสต์บน GitHub Pages
- ตัวนับ "🏪 เปิดมาแล้ว N สาขา" (ถ้าเปิดใช้) ใช้ Cloudflare Worker + D1 แยกต่างหาก นับเป็นครั้งต่อรอบการเปิดเว็บ ไม่ใช่จำนวนคน

### หมายเหตุ

เกมนี้เป็นงานแฟนเมดที่ไม่เป็นทางการ **ไม่มีส่วนเกี่ยวข้องกับ Viu หรือทีมผู้สร้างซีรีส์ The Rules** ตัวละคร ภาพ และโค้ดในเกมสร้างขึ้นใหม่ทั้งหมด ไม่ได้ใช้ภาพ เสียง หรือสคริปต์จากซีรีส์

### พบบั๊กหรืออยากเสนอไอเดีย

เปิด **Issues** ในรีโปนี้ หรือแท็กมาที่ X: [@nmeksobh](https://x.com/nmeksobh)

---

## 🇬🇧 English

### What is this?

*Night Shift Rules* is a small passion project inspired by Viu's Thai series *The Rules*. You play Chot, a minimart manager who watches the store at night through 4 CCTV cameras. Every staff member follows their own rules, and when something looks wrong you have to react before the warning bar fills up.

### How to play

- Watch all 4 cameras. If something is off, the bar under the feed fills up (green → red).
- Tap a camera to look closer, then use what the rules call for: radio, incense, lights off, door latch, or staff.
- If a camera goes black (no one on duty), hit the bell to call a free staff member over.
- Check tonight's rulebook and follow it, because the rules change every night.
- Survive until 6 AM.

### Game modes

| Mode | Description |
|---|---|
| **Normal** | 5 nights, with rules and difficulty ramping up. Best for first-time players. |
| **Survivor** | A harder mode for players who have finished Normal. The ghosts are more aggressive, and a warning appears before you enter. |

### Development story

It started with a simple "what if I were the one watching the CCTV in *The Rules*?" and grew into a full game through back-and-forth sessions with Claude:

1. **V1**: the first prototype, with cameras, staff and a basic rulebook.
2. **V2**: more modes and tools, plus difficulty balancing.
3. **V3 → Public Beta**: the last round before release, shaped by playtester feedback:
   - The rulebook and How to Play were too long, so they were cut down.
   - A warning was added before Survivor, since it isn't meant for first-timers.
   - The layout was tuned to fit phone screens without scrolling or nudging.
   - The share button was fixed so it works in more environments.
   - The status bar was shortened to a single line.

All pixel art is drawn in code (sprites are arrays of characters painted onto a canvas), so there are no image assets in the game. Every release was checked with Playwright before shipping.

### Tech notes

- A single HTML file (`index.html`), with no dependencies.
- Thai and English, switchable in-game.
- Hosted on GitHub Pages.
- The optional "🏪 N branches opened" counter runs on a separate Cloudflare Worker + D1. It counts browser sessions, not unique people.

### Disclaimer

This is an unofficial fan project and is **not affiliated with Viu or the creators of *The Rules***. All characters, art and code were created from scratch. No images, audio or scripts from the series are used.

### Bugs and ideas

Open an **Issue** in this repo, or find me on X: [@nmeksobh](https://x.com/nmeksobh)

---

Made by Pui ([@nmeksobh](https://x.com/nmeksobh)) with Claude.
