# Cheatseet
**Smurf Attack** -> Salah satu teknik DoS (Denial of Service). Memanfaatkan teknik refleksi dan amplifikasi untuk membanjiri target dengan trafik dalam jumlah besar melalui jaringan perantara dan protokol **ICMP**. Menyebabkan Buffer Overflow yang membuat target unavailable. Solusinya adalah menonaktifkan command ping dan mengaktifkannya hanya pada saat dibutuhkan.

**IP Spoofing** -> The act of changing IP address. Tujuan utamanya adalah untuk mengeksekusi serangan siber tanpa terdeteksi.

**Pretexting** -> Social engineering attack in which scammers **create a believable backstory or pretext** to gain your trust. They might pretend to be your bank, IT support, or even a family member. 

**Vishing** -> Singkatan dari Voice + Phishing yang artinya phishing dilakukan melalui suara. Biasanya menggunakan telepon, WhatsApp call, Zoom, dll. Sering kali menggunakan teknik **pretexting**, tetapi pretexting tidak harus dilakukan melalui telepon.

**Shoulder Surfing** -> Someone steals your private information just by watching you enter it.

**Banner Grabbing** -> The process of identifying the service version that currently running on a server. Salah satu teknik enumeration. **Banner** adalah pesan yang dikirim oleh service ketika client melakukan koneksi. Ada 2 jenis Banner Grabbing, yaitu **Passive** (it relies on strategically placed sensors in the network or third-party network tools) dan **Active** (establishes a connection, sends packet to a remote server, and then dissects the server's response, thus taking an active approach).

**Fingerprinting** -> Berbeda dari Banner Grabbing, Fingerprinting adalah proses mengidentifikasi atau menebak versi dari sebuah service berdasarkan perilakunya karena informasi versi dari service tersebut disembunyikan oleh administrator.

**Ping Sweep** -> Salah satu teknik **host discovery** yang digunakan untuk mengetahui host apa saja yang aktif dalam suatu jaringan dengan cara mengirim probe (ICMP Echo, ICMP Timestamp, TCP SYN, TCP ACK, dll.) ke setiap host yang ada pada jaringan. Dalam LAN, metode yang paling akurat biasanya **ARP Scan** karena setiap host di LAN harus merespons permintaan ARP agar komunikasi Ethernet dapat berlangsung.

**Enumeration** -> Proses mengidentifikasi dan mengumpulkan informasi spesifik mengenai service, user, sistem, atau resource yang tersedia pada target melalui interaksi langsung dengan service tersebut.

**Bluejacking** -> Seorang penyerang mengirim pesan yang tidak diminta ke komputer atau HP korban melalui **Bluetooth**.

**Bluesnarfing** -> Ketika seorang penyerang dapat mengakses data seperti kontak, email, atau bahkan informasi kalender yang terdapat pada komputer atau HP korban melalui **Bluetooth**. `Status: Sudah dipatched pada Bluetooth modern`

**Ping of Death** -> In the early days of the internet, some OS and networks did not properly validate the size of incoming ICMP packets. Attacker exploit this vulnerability to send ICMP packets larger than the allowable size. This causes buffer overflows, system crashes, or even RCE. Ping of Death is a relic of the past since modern OS and networks have implemented safeguard to prevent such attacks. 

**Log Tampering** -> Tindakan mengubah, menghapus atau memalsukan data log secara ilegal dengan tujuan menyembunyikan jejak aktivitas jahat agar tidak terdeteksi oleh tim keamanan.

##### DNS Attacks
**DNS Spoofing** -> Istilah umum untuk **memalsukan respons DNS** agar korban menerima alamat IP yang salah. Yang penting korban menerima respons DNS palsu tanpa mempedulikan bagaimana caranya.
**DNS Cache Poisoning** ->  Jenis khusus dari DNS Spoofing yang menargetkan **cache DNS resolver**. Teknik ini membuat cache DNS terinfeksi sehingga respons palsu akan terus diberikan sampai cache tersebut expired.
**DNS Poisoning** -> Istilah ini digunakan untuk menyebut segala bentuk manipulasi data pada DNS, termasuk **DNS Cache Poisoning** dan **DNS Spoofing**.

##### Brute Force Types
A Brute Force attack will take a list of possible inputs, and try each of them against the server looking for positive responses. The success or failure of the attack will depend on the list of inputs supplied to the brute forcer.
**Simple Brute Force** -> Try every possible combination of input characters until we get a result. Useful for guessing simple or short passwords, but with longer items can take a long time.
**Dictionary Based Attacks** -> Here we build a list of possible inputs then work through the list using each item as input.
**Reverse Brute Forcing** -> Takes a commonly used password and attempts to use it on many user accounts.
**Credential Stuffing** -> Similar to Reverse Brute Forcing, but focuses on a specific user. Once a username / password combination has been identified, it is checked against several sites to see if there is a match. Useful in the case of password reuse.
**Rainbow Tables** -> Work with hashed, but unstaled password. Rather than attempt to brute force the password "Live", we make use of pre-calculated hash values for words in a dictionary. This means that we only have to crack the hashes once, store the result, then use the stored values to lookup the plaintext for the hash.

**Fuzzing** -> Mencoba input acak dengan tujuan untuk membuat sistem crash atau untuk mencari kerentanan pada sistem berdasarkan output yang dihasilkan. Fuzzing memiliki dua kegunaan utama: **Identifying Edge Cases where the System Breaks** and **Learning More about how a system handles data**

##### Malware
**Malware** -> Malicious Software. Istilah umum untuk semua jenis program yang merusak, menyusup, atau menyalahgunakan komputer korban.
**Virus** -> Nempel di file atau program dan menyebar atau menyalin dirinya ketika file atau program tersebut dijalankan. Efeknya data rusak, sistem berjalan lambat, bahkan sampai tidak bisa dipakai.
**Worm** -> Bisa nyebar sendiri tanpa bantuan manusia. Dapat menyusup melalui celah keamanan di sistem, software, OS, bahkan flashdisk yang terinfeksi. Bisa nyolong data dan koneksi internet jadi lambat.
**Ransomware** -> Mengenkripsi file-file yang ada di komputer korban lalu hacker minta tebusan agar file tersebut dapat dibuka kembali.
**Trojan** -> Malware yang nyamar jadi trusted software padahal di dalamnya ada malware. Trojan ga nyebar sendiri seperti virus, tapi menunggu korban untuk menginstall software tersebut untuk mendapatkan data pribadi korban.
**Virus Hoax** -> Penipuan yang menyebarkan peringatan palsu mengenai virus yang sebenarnya fiktif dengan tujuan membuat korban panik.
**Wiper** -> Malware yang menghancurkan data.
**RAT** -> Remote Access Trojan. Begitu masuk, hacker bisa kontrol penuh komputer korban mulai dari buka file, gerakin mouse, dll.
**Cryptojacker** -> Mencuri resource komputer korban untuk mining crypto diam-diam sehingga menyebabkan komputer korban mengalami penurunan performa yang signifikan.
**Keylogger** -> Merekam semua yang diketik oleh korban.
**Logic Bomb** -> Malware yang sengaja disembunyikan di dalam sistem dan baru aktif ketika ada pemicu tertentu seperti pada jam tertentu, tanggal tertentu, atau aktivitas tertentu. Efeknya bisa menghapus data penting, mematikan akses user, atau membuat sistem crash.
**Malvertising** -> Malware yang menyamar jadi iklan.
**Adware** -> Malware yang memunculkan iklan secara terus-menerus.
**Spyware** -> Mencatat aktivitas user secara diam-diam dari history browsing, lokasi terkini, sampai apa yang korban lihat.
**RAM Scraper** -> Mencuri data sensitif di RAM sebelum disimpan atau dienkripsi. Sering dipakai di sistem kasir atau restoran, studi kasusnya ketika seorang korban menggesek kartu ATM, Ram Scraper langsung mengambil data itu.
**Rootkit** -> Malware yang bersembunyi di kernel. Dapat menyamarkan atau menyembunyikan malware lain dari antivirus.
**Backdoor** -> Jalur rahasia untuk masuk ke sistem tanpa izin.
**Botnet** -> Kumpulan komputer yang terinfeksi malware dan diam-diam dikendalikan oleh hacker dari jarak jauh.
**Fileless Malware** -> Tidak meninggalkan jejak di harddrive, langsung jalan di RAM sehingga ketika komputer direstart, malware tersebut akan langsung hilang.
**Malicious Macro** -> Skrip jahat yang diselipin di dokumen Word atau Excel.

##### Tools
**Nikto** -> Web server scanner, used to identify vulnerabilities - like outdated software, dangerous files, and potential misconfigurations.
**Nessus** -> Vulnerability scanning tool that scans for security vulnerabilities in devices, applications, operating systems, cloud services, and other network resources. Berbeda dengan Nikto yang khusus untuk web server, Nessus mencakup seluruh infrastruktur jaringan.
**Wireshark** -> Network packet analyzer. It presents captured packet data in as much detail as possible.
**Nmap** -> Used for network discovery, scanning and security auditing. It helps identify hosts, open ports, running services, operating systems and potential vulnerabilities.
**Metasploit** -> Exploitation Framework that contains group of tools and utilities put together to make exploit development, system administration, and honing stuff.
**Cain and Abel (DEPRECATED / NOT USED ANYMORE)** -> Password recovery tool for Windows. It could recover many kinds of passwords using methods such as network packet sniffing, cracking various password hashes by using methods such as dictionary attacks, brute force and cryptanalysis attacks.


# References
https://www.sanfoundry.com/1000-cyber-security-questions-answers/
https://wayground.com/activity/admin/quiz/6a2cf7292f37dfe477ed988c/simulasi-penyisihan-kmipn-5
