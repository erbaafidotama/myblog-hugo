---
title: "Pengenalan & Tutorial FastAPI Python - Bagian 1"
date: 2021-09-16T11:49:57+07:00
draft: false
categories:
- FastAPI
- Python
tags:
- Python
- FastAPI
- tutorial
- belajar
---

![Logo FastAPI](/static/logo-fastapi.png)

Assalamualaikum warahmatullahi wabarakatuh, teman-teman.

Pada tulisan saya kali ini, saya akan memberikan sedikit penjelasan dari framework yang berasal dari bahasa pemrograman python. Lebih tepatnya, sedikit banyak saya penjelasan saya adalah hasil __translate__ dari [dokumentasi FastAPI](https://fastapi.tiangolo.com/) itu sendiri. Gak perlu banyak basa-basi lagi, mari kita mulai :grin: .

## Apa itu FastAPI?
FastAPI adalah sebuah web framework yang modern, cepat untuk membuat API dengan menggunakan Python 3.6+.
> _FastAPI framework, high performance, easy to learn, fast to code, ready for production_

Beberapa fitur yang diberikan sama FastAPI nih:
* Fast
    
    Artinya memiliki performa yang sangat baik, setara dengan NodeJS dan Go-lang.
* Fast to code
    
    Meningkatkan kecepatan dalam melakukan development, kl di dokentasinya bisa mencapat 200% - 300%
* Easy
    
    Ini hal yang paling penting bagi saya yang kadang suka pengen cepet aja. Yaitu dibuat untuk mudah dalam penggunaan dan dipelajari.
* Automatic Docs

    Dengan adanya fitur ini, kita gak perlu lagi memasang [Swagger](https://swagger.io/) untuk melakukan dokumentasi URL yang telah kita buat.
    ![Gambar FastAPI Docs](/static/pict-fastapi-docs.png)

Setelah tau apa itu FastAPI dan beberapa fiturnya, mari kita mulai aja cara menggunakan FastAPI.

Langkah pertama yang harus kita lakukan adalah install FastAPI nya.
```
mdkir learn-fastapi
cd learn-fastapi
pip install fastapi[all]
```
Jangan lupa, sebelumnya kita harus masuk kedalam virtual environment python. Kita juga bisa install FastAPI tanpa ``[all]`` yang artinya hanya install FastAPI nya aja. Tapi karena saya gak mau ribet, jadi saya menggunakan ``[all]`` agar langsung install semua hal-hal yang diperlukan dalam development menggunakan FastAPI.

> Jika teman-teman tidak menggunakan ``[all]``, teman-teman harus menjalankan perintah ``pip install uvicorn[standard]``.


Sekarang kita coba membuat code dan menjalankan FastAPI.

Buat file terlebih dahulu dengan nama ``main.py`` di root folder learn-fastapi, lalu copy code di bawah kedalam ``main.py``.

```python
from fastapi import FastAPI

app = FastAPI()


@app.get("/")
async def root():
    return {"message": "Hello World"}
```

Coba sekarang jalankan server dengan menjalankan perintah:
```
uvicorn main:app --reload
```
> * main: file main.py
>
> * app: sebuah object/variabel yang dibuat di dalam main.py
>
> * --reload: membuat server lokal kita melakukan reload otomaris ketika ada perubahan pada code kita

Jika berjalan dengan baik, maka kita akan mendapatkan hasil seperti di gambar.
![Firstrun FastAPI](/static/pict-runfirst-fastapi.png)

Setelah server lokal kita berjalan, coba buka browser dan buka link ``http://127.0.0.1:8000``, maka hasilnya akan muncul ``"message": "Hello World"`` di dalam json.
![Result Firstrun FastAPI](/static/pict-resultfirstrun-fastapi.png)

Naahh, alhamdulillah kita telah berhasil menjalankan FastAPI. Cukup mudah bukan, tutorial selanjutnya juga sama mudahkannya kok insyaaAllah. 

---
Untuk sekarang, cukup sekian dulu dari saya. Terima kasih.
Wassalamualaikum warahmatullahi wabarakatuh.