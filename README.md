## Deskripsi Proyek
_Project_ ini bertujuan untuk membuat tugas Gradle sederhana yang menerima parameter CLI (Command Line Interface) dan mencetaknya dengan pesan ucapan. _Project_ ini dibuat dengan menggunakan Gradle dan mencakup penambahan pustaka eksternal.

## Cara Menjalankan Proyek

### Langkah-langkah
1. **Membuat _Project_ Gradle Baru**:
    - perintah untuk membuat _project_ Gradle baru:
      ```bash
      gradle init --type java-library
      ```

2. **Menambahkan Tugas Gradle Khusus**:
    - Buka file `build.gradle` di direktori _root project_ dan tambahkan kode berikut untuk mendefinisikan tugas khusus:
      ```groovy
      task greetingTask() {
          doLast {
              String nama = project.hasProperty('nama') ? project.property('nama') : 'AMI'
              println "Hello, $nama! Welcome to Gradle World!"
          }
      }
      ```
      
3. **Menambahkan Pustaka**:
    - Menambahkan pustaka dapat menggunakan fitur manajemen dependensi bawaan Gradle dengan menambahkan kode berikut ke file `build.gradle`:
      ```groovy
      dependencies {
          implementation 'com.google.guava:guava:29.0-jre'
          testImplementation 'junit:junit:4.13'
      }
      ```

4. **Dorong Proyek ke GitHub**:
    - Buat repositori baru di GitHub dan _push project_ dengan menjalankan perintah berikut:
      ```bash
      git init
      git add .
      git commit -m "Initial commit"
      git remote add origin https://github.com/choirulafahmii/Module18Task.git
      git push -u origin master
      ```
      
### Cara _Run code_ dari _Project_ diatas

  **Menjalankan Tugas**:
    - Tugas dapat dijalankan dengan perintah berikut:
      ```
      ./gradlew greetingTask -Pnama=YourName
      ```
      pada terminal

## Hasil dari _run project_

![image](https://github.com/user-attachments/assets/d871758d-73fe-4cbe-9801-f6ed38b79141)
