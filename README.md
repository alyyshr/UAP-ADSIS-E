1.	Buat direktori dengan nama UAP-Adsis, isi dengan file txt dengan format penamaan catatannya-<nama kamu>.txt, kemudian isi file txt tersebut dengan nama dan NIM kamu. 
    Kemudian atur permission view-only pada file tersebut untuk user biasa. Tunjukkan bukti berupa screenshot yang menunjukkan bahwa file tersebut berhasil diatur permissionnya 
    menjadi view-only untuk user biasa.
  
    JAWABAN :
  
    ![1](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/953ea132-34d4-40a0-8f2f-df5c25267a48)
  
    Membuat folder “UAP-Adsis” dan mengecek apakah berhasil membuat folder, selanjutnya membuat file “catatannya-Aliya.txt”
    ![2](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/c9e5f616-5e95-40ef-9852-3e7d4571ce1a)
  
    Menambahkan nama dan nim pada file “catatannya-Aliya.txt”
    ![3](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/2ee8e068-0f43-4d4e-bee0-c7ec357b2f4f)
  
    Mengubah permission untuk user biasa hanya view/melihat
2.  Lakukan konfigurasi alamat IP address sementara pada sistem dan default gateway. (petunjuk 192.168.56.x | x adalah nomor absen)
  
    Jawaban :
  
    ![4](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/a790ad52-f579-4da3-836b-b7053c43d7bd)
  
    Mengecek ip awal pada enp0s8
  
    ![5](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/e3f7c6d0-02f8-403d-8f0a-5224bf510c8b)
  
    Melakukan perubahan ip pada enp0s8
  
    ![6](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/3eb49887-3a68-4b71-819d-986d50f0c3a3)
  
    Ip enp0s8 berhasil berubah
  
    ![7](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/cb3f74c7-ad32-4d72-9eb0-116a7d330717) 
  
    Mengubah default gateway menjadi “192.168.56.1” dan mengecek apakah telah berhasil.
3.  Lakukan Instalasi Webmin lalu buatlah user bernama nama anda, lalu buat group Adsis_(kelas masing-masing) dan masukkan nama anda di group
  
    Jawaban :
  
    ![8](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/4e51bffa-e4f6-441e-b7bf-4f56e51e93f4)
  
    Sudah melakukan instalasi lanjut ke tahap berikutnya
  
    ![9](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/1258713d-7827-474d-af31-3f81530dd5bc)
  
    ![10](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/9641df48-6c8b-4892-9418-8fcf79351d7f)
  
    Membuat grup dengan nama Adsis_E dan memasukkan nama “aliya” pada grup  Adsis_E
    
    ![11](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/9e58f7b4-ddd7-45ae-a216-64bd024525be)
    
    Berhasil membuat grup Adsis_E dan memasukkan “aliya” pada grup.
  
4.  Lakukan ping ke alamat ip anda dan coba lakukan reject dan drop di webmin, lalu analisis apa yang terjadi?
    
    Jawaban :
    
    ![12](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/8638706d-dcfc-491c-957d-4d7bb3fa0556)
  
    Melakukan ping ke ip ubuntu dan Pada gambar diatas proses ping berhasil dilakukan dengan adanya reply dari server.
    
    ![13](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/eadde940-4b80-4113-9274-a89fda04beec)
  
    Masuk pada webmin dan memilih incoming packets (INPUT) kemudian Add Rule.
    1)	Membuat rule Reject, kemudian save changes lalu klik apply configuration.
        
        ![14](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/11aca662-349f-4f84-b08a-3ee9a9a4f75d)
         
        ![15](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/867b4426-29e8-457f-b8fb-f5e74028d303)
    
        ![16](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/bc4bcf83-9d3f-409d-9fa2-369b0b27c221)
         
        Paket ICMP atau Ping berhasil di reject. Melakukan test ping lagi kepada ip ubuntu dan gagal hal ini dikarenakan kita telah membuat sebuah rule firewall pada ipv4 yang dimana 
        kita tidak bisa memping atau memblok sehingga muncul destination net unreachable.
  
        ![17](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/c5e1d66b-b200-431c-9e4a-b0c25b81fd38)
  
     2)	Membuat rule Drop, kemudian save changes lalu klik apply configuration.
        
        ![18](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/fe918a9a-5646-43ed-bb91-a9c572d3a65d)

        ![19](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/2f0eab6b-647a-4b63-bc06-cf49724df280)

        ![20](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/47b3e42c-6934-4fca-813b-000d7a6d490a)

        Paket ICMP atau Ping berhasil di drop. Melakukan test ping lagi kepada ip ubuntu dan gagal sehingga Request Timed Out.
  
 5.	Buatlah perintah otomatis yang berfungsi untuk ping www.filkom.ub.ac.id
    
    Jawaban :
  
    ![21](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/be7874d1-d5a0-487a-93da-d56eacc5eb0a)

    Buka Crontab untuk menyetting perintah otomatis
  
    ![22](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/d4291825-5fd3-4a42-912c-495d3bedccff)

    Membuat cron untuk melakukan ping pada web filkom.ub.ac.id setiap 2 menit sekali.
  
    ![23](https://github.com/alyyshr/UAP-ADSIS-E/assets/87374937/b2260df3-6c91-4442-a8de-ee77431e6759)

    Berhasil memping web filkom.ub.ac.id setiap 2 menit.
  
    

        






