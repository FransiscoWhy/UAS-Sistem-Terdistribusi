# Final Project Sistem Terdistribusi Kelompok 4

### Fransisco Wahyu Syahbani 1203210045 
### Hisyam Mohamad Alam 1203210134 


Buat lxc baru dan konfigurasikan IP masing-masing lxc

![Screenshot 2024-06-21 160235](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/5952ec89-ace5-43f1-948a-b6e1721146c7)

Instal open ssh server di semua lxc diatas, setelah itu kita masuk ke ansible

```html 
apt install openssh-server
```

Lalu pergi ke

```html
cd ~/ansible/tubes
```

lalu kemudian ke 'nano host' untuk mengklasifikasikan setiap lxc seperti skema di atas

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/c69f0760-5846-4ab2-9813-6fa5cebfb876)

Kemudian

```html
nano install-ci.yml //kode untuk igniter
nano install-laravel.yml //kode untuk laravel
nano install-wp.yml //kode untuk wordpress
nano install-yii.yml //kode untuk yii2.0
nano install-mariadb.yml //kode untuk phpmyadmin
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/308d9150-454b-436d-9f47-8274bd5177ae)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/f1f23614-c685-4557-a354-4c0a2941d438)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/6329f888-124f-4b8d-bb94-8ac238e88e78)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/a20883b5-b428-472c-9022-5577c20c71b0)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/787656a1-4149-423d-a877-ddf2e9e780e7)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/4ad48333-f705-4c42-bade-cb18a263ae81)

Setelah semuanya selesai, kemudian pindah direktory

```html
cd /roles/ci/tasks
```

Setelah itu masuk 

```html
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/7a620a3c-8c60-48e6-8bc4-edfc5fdc11fd)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/acc01fcb-ff85-49e6-9d62-f365c2bc4494)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/d711682f-be8d-449b-ad4f-e25ca7fc0a8e)

Setelah semuanya selesai lalu pindah direktory

```html
cd ../templates
nano app.conf
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/70daf556-f85d-4494-a050-a2ac955e1a3d)

Setelah itu pindah direktory

```html
cd ../handlers
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/f9114ff7-2fc6-4cb9-a8fb-735cdf7fcfc4)

Untuk Igniter sudah selesai, Lalu selanjutnya
Masuk direktory PHP folder tasks

```html
cd ../../
cd php/tasks
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/4c37ac9d-d5a7-42bc-a8bf-9b9a6a7eeda9)

Setelah itu pindah direktory dan masuk ke dalam direktory main.yml

```html
cd ../handlers
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/dec8f14b-e6e5-497a-8b4f-597d8b722573)

Untuk ansible php sudah selesai, selanjutnya adalah Laravel, kita harus pindah direktory

```html
cd ../../
cd lv/tasks
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/bef0ef21-56fe-47fb-98f7-5da6e40ea6d8)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/ca052583-975a-4c4b-b4ec-d198529e02c6)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/fc8d94d4-1edc-4359-b672-82aeb13f2fa1)

Pindah direktori menuju

```html
cd ../templates
nano env.template
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/32538e36-6398-4fe4-8c84-e441f56540ba)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/d75ad07c-1984-49f5-b6de-fb3491599cf2)

Lalu pergi ke direktori conf laravel

```html
nano laravel.conf
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/92e5d4d6-5008-4e24-8c51-ba4a18d9b9eb)

Setelah mengkonfigurasi template, kita pergi ke  direktori handler

```html
cd ../handlers
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/7797dd65-0ffd-4f32-a47e-f125ee100b69)

Ansible untuk Laravel telah selesai, selanjutnya untuk mariDB
Pindah direktori

```html
cd ../../../
cd db/tasks
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/c0038c6c-52b3-489b-857d-b053ebb67ea4)

Lalu pindah ke direktori template

```html
cd ../templates
nano my.cnf
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/91dcfe8c-d44d-423d-9359-24485d0aeb40)

Lalu pindah ke direktori Handlers

```html
cd ../handlers
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/fc74c159-a6bb-4e67-b81c-ad319c96b646)

Ansible untuk dari database telah selesai, lalu untuk selanjutnya PHP MyAdmin

```html
cd ../../
cd pma/tasks
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/2b48c46f-15a0-4434-b112-5466e1509cf2)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/fca30af5-d325-4faa-af67-be6c486d9aa4)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/8a782196-db41-4e06-9ca5-89bf27d0b9c4)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/0ca7ad4f-3c1b-4280-bcd6-5caf8df76c26)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/af6bb868-3598-4339-abfe-dca0226173fe)

Lalu pindah ke direktori template

```html
cd ../templates
nano lxc_mariadb.conf
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/3e907ee8-1757-4e7e-8106-5fc0bf9b3599)

Lalu Kembali ke direktori handlers

```html
cd ../handlers
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/98615d21-98c7-4306-9764-4687661422a7)

Ansible untuk PHP MyAdmin telay selesai, selanjutnya YII

```html
cd ../../
cd yii/tasks
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/3f405da0-d2be-4c2e-b357-0add240d8694)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/7cd7a49f-8786-473c-9a24-389f1aef9e10)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/9c5344ab-a4cf-445a-9fea-198a0ec54df6)

Selanjutnya pergi ke direktori template

```html
cd ../templates
nano yii.conf
```

![Screenshot 2024-06-21 192729](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/0df13961-c75d-4d86-af1d-3af56caff407)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/69f5041d-3df0-49ce-ac06-eec2d8614929)

Pindah ke direktori handlers

```html
cd ../handlers
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/5e28b260-9a79-45eb-8148-9d50ac7f4db0)

Ansible yii lalu selanjutnya wordpress

```html
cd ../../
cd wp/tasks
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/7321b996-ad87-4c90-a86d-a7344fc3791f)

Setelah itu kembali ke template

```html
cd ../templates
nano wp.conf
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/044eec33-25ee-4eef-86d0-febc0d63ed52)

Kemudian masuk ke wp.local

```html
nano wp.local
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/c5c435ed-29e6-489a-9f24-a375b6d08a76)

Tidak lupa untuk kembali ke handlers

```html
cd ../handlers
nano main.yml
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/6e8abbaf-6e02-461a-8c6e-523c571639a6)

Konfigurasi untuk kelompok9.fpsas

```html
sudo nano /etc/nginx/sites-available/kelompok9.fpsas
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/32d01067-fafc-4f09-9cce-f55a3e5df17d)

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/66217809-55ee-4a39-a8eb-d5e75b1e292c)

Konfigurasi hosts

```html
nano /etc/hosts
```

![image](https://github.com/FransiscoWhy/UAS-Sistem-Terdistribusi/assets/141225950/a70d2437-60bf-4efc-8d6f-046c99e437a4)

Untuk hasil akhir belum berhasil atau error
