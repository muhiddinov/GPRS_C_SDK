Ai-Thinker GPRS C SDK

Ai-Thinker GPRS SoC uchun C tilida yozilgan dasturiy ta’minot ishlab chiqish to‘plami (SDK)

Ai-Thinker GPRS modulining chip ichidagi (SoC) ishlab chiqish SDK’si, C tilida yozilgan versiya

    Ushbu SDK RDA8955 xom chipida ham ishlashi mumkin.
    也可直接在RDA8955芯片上运行

Inglizcha README

Muammolarni hal qilish o‘rtacha vaqti
Hali ochiq qolgan muammolar foizi
1. Qurilmalar
1. A9: GPRS moduli

Xususiyatlar:

    32-bit yadro, chastotasi 312 MHz gacha, 4 KB instruktsiya kesh, 4 KB ma’lumotlar kesh

    29 ta GPIO (2 tasi yuklash porti sifatida)

    RTC va budilnik

    1× USB 1.1 port

    2× UART (flow control bilan) + 1× yuklash/tuzatish porti

    2× SPI port

    3× I²C port

    1× SDMMC nazoratchisi

    2× 10-bit ADC

    32 Mb (4 MB) SPI NOR Flash

    32 Mb (4 MB) DDR PSRAM

    8 kHz, 13-bit/sample ADC mikrofon

    48 kHz, 16-bit/sample DAC audio

    Quvvat boshqarish bloki: Li-ion batareya zaryadlash, DC-DC va LDO’lar, sozlanadigan IO kuchlanishi

    18.8 × 19.2 mm SMD korpus

    Quad-band GSM/GPRS (800/900/1800/1900 MHz)

    Ovoza qo‘ng‘iroqlar

    SMS xizmati

2. A9G: GPRS + GPS + BDS moduli

Xususiyatlar:

    A9’ning barcha xususiyatlari

    Ichki GPS + BDS (GPRS UART2 bilan ulangan)

3. A9/A9G rivojlantirish platalari

Xususiyatlar:

    A9G moduli (A9 va A9G bir xil korpus va pinlarga ega, platalar umumiy)

    29 ta GPIO chiqishi (shu jumladan yuklash/tuzatish pinlari: HST_TX, HST_RX)

    1× SIM karta sloti (Micro SIM; adapter bilan Nano yoki Standart karta ishlatish mumkin)

    1× TF karta sloti

    1× GPRS antennasi uchun IPEX port

    1× GPS antennasi uchun IPEX port

    1× USB port

    5 V → 4.2 V DC-DC (5 V yoki 3.8–4.2 V bilan quvvatlash mumkin)

    LIS3DHx akselerometr (ixtiyoriy)

    Quvvat tugmasi va reset tugmasi

    GPIO’ga ulangan 2× LED

    1× mikrofon

Pudding plata pinout:

    Teoriyada, RDA8955 chipi yoki shu chip asosidagi boshqa modullar ham shu SDK bilan ishlaydi.

4. USB–UART adapteri

Plata ustidagi USB port — bu USB–UART emas, balki USB 1.1 funksiyasi.
Shu sababli, yuklash va tuzatish ishlari uchun HST_TX va HST_RX pinlariga USB–UART adapter ulash kerak.
5. Quvvat manbai

    Modulni Li-ion batareya orqali (VBAT: 3.4–4.2 V) quvvatlash mumkin. Batareya bilan ishlaganda power-key tugmasini bosib ushlab turish kerak.

    Plata 5 V USB orqali ham ishlashi mumkin (ichki DC-DC orqali 4.2 V ga tushiriladi).
    USB–UART adapter orqali quvvatlash faqat tuzatish rejimida tavsiya etiladi.

    Quvvat manbai pikda 2 A tok bera olishi kerak.

2. SDK imkoniyatlari

    Oson foydalanish mumkin bo‘lgan C API — C tilini bilgan dasturchilar tezda ish boshlashi mumkin. To‘liq namuna kodlar va hujjatlar mavjud.

    Integratsiyalangan funksiyalar:

        GPIO

        UART

        Qurilma ma’lumotlari (ICCID, IMEI, IMSI)

        SPI

        I²C

        ADC

        OS

        Fayl tizimi (FS)

        GPRS tarmog‘i va bazaviy stansiya ma’lumotlari

        LBS (bazaviy stansiya orqali joylashuv)

        Socket (TCP/UDP)

        DNS

        SSL/TLS

        MQTT

        SMS

        Telefon qo‘ng‘iroqlari

        Past quvvat rejimlari

        GPS

        RTC va tarmoq vaqti sinxronizatsiyasi

        FOTA

        Watchdog

        Audio ijro (MP3)

        Gizwits platformasiga tez ulanish

        Alibaba Cloud CSDK

        JSON va NMEA parser kabi qo‘shimcha kutubxonalar

3. SDK’ni yuklab olish

GitHub manzili: Ai-Thinker GPRS C SDK

1-usul (tavsiya etiladi):
Releases bo‘limidan so‘nggi versiyani ZIP fayl ko‘rinishida yuklab olish.

2-usul:
Git yordamida so‘nggi kodni olish:

git clone https://github.com/Ai-Thinker-Open/GPRS_C_SDK.git

Muhim: Yuklab olingandan so‘ng, platform/csdk ichida debug va release papkalari borligini tekshiring. Agar yo‘q bo‘lsa — yuklash noto‘g‘ri bo‘lgan.
4. Hujjatlar va namuna kodlar

📄 Onlayn hujjatlar:
GPRS C SDK hujjatlar
Bu yerda SDK o‘rnatish, firmware yozish, tuzatish, GPRS asoslari va API’lar haqida ma’lumotlar mavjud.

📂 Namuna kodlar:
demo papkasida joylashgan.
5. Fikr-mulohaza

    GitHub Issues bo‘limi orqali mavjud muammolarni qidiring yoki yangi muammo oching.

    Ai-Thinker forumida munozara bo‘limi mavjud.

    Yuqoridagi ★ Star tugmasini bosib loyihani saqlab qo‘yishingiz mumkin.

6. Hissa qo‘shish

Agar xatolarni tuzatish, optimallashtirish yoki yangi modul qo‘shish istagi bo‘lsa:
fork → o‘zgartirishlar qilish → pull request yuborish.