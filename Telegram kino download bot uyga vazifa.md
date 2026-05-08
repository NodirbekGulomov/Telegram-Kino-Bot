### **Loyiha nomi**

Telegram Kino Bot

---

### **Bot tavsifi**

Ushbu bot foydalanuvchilarga maxsus kod orqali kinolarni tez va oson olish imkonini beradi. Botdan foydalanishdan oldin foydalanuvchi belgilangan Telegram kanallariga obuna bo‘lishi shart. Admin foydalanuvchilar esa bot orqali yangi kinolar qo‘shishi va mavjudlarini boshqarishi mumkin.

---

### **Maqsad**

* Foydalanuvchilarga kino kod orqali kontent taqdim etish  
* Adminlar uchun oddiy va qulay kontent boshqaruvi yaratish  
* Telegram botlar bilan ishlash, API va database integratsiyasini o‘rganish

---

### **Asosiy funksiyalar**

#### **1\. Start va obuna tekshiruvi**

* Foydalanuvchi `/start` bosganda:  
  * Bot oldindan berilgan kanallar bo‘yicha obuna holatini tekshiradi  
  * Agar barcha kanallarga obuna bo‘lgan bo‘lsa:  
    * Botdan foydalanishga ruxsat beriladi  
  * Aks holda:  
    * Kanallar ro‘yxati va havolalari yuboriladi  
    * Qayta tekshirish uchun tugma taqdim etiladi

---

#### **2\. Kino olish (foydalanuvchi)**

* Foydalanuvchi botga kino kod yuboradi (masalan: `K123`)  
* Bot:  
  * Bazadan shu kodni qidiradi  
  * Agar topilsa:  
    * Kino fayli yoki linkini yuboradi  
  * Agar topilmasa:  
    * “Kino topilmadi” xabari qaytariladi

---

#### **3\. Admin funksiyalari**

##### **Kino qo‘shish**

* Admin quyidagi ma’lumotlarni yuboradi:  
  * Unikal kino kodi  
  * Kino fayli (file\_id) yoki tashqi havola  
  * (ixtiyoriy) nomi va tavsifi  
* Bot ushbu ma’lumotlarni bazaga saqlaydi

##### **Kino o‘chirish (ixtiyoriy)**

* Admin kino kod orqali kinoni o‘chirishi mumkin

##### **Kinolar ro‘yxati (ixtiyoriy)**

* Admin barcha kinolar ro‘yxatini ko‘rishi mumkin

---

### **Texnik talablar**

* Dasturlash tili: Python  
* Framework: Aiogram   
* Ma’lumotlar bazasi: SQLite yoki PostgreSQL

---

### **Ma’lumotlar bazasi strukturasi**

**users**

* id  
* telegram\_id  
* is\_admin (boolean)

**movies**

* id  
* code (unikal)  
* file\_id yoki link  
* title (ixtiyoriy)  
* description (ixtiyoriy)

---

### **Asosiy ish jarayoni**

1. Foydalanuvchi `/start` yuboradi  
2. Bot obuna holatini tekshiradi  
3. Foydalanuvchi kino kod yuboradi  
4. Bot mos kinoni qaytaradi yoki xatolik xabarini beradi  
5. Admin foydalanuvchilar qo‘shimcha komandalar orqali kinolarni boshqaradi

