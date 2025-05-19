# Tutorial 10 - Timer

## 1.2 Understanding how it works

![alt text](image.png)

Setelah menambah print setelah Spawner.spawn di file main.rs, ketika dijalankan hasil print yang ada setelah spawner muncul pada terminal terlebih dahulu sebelum yang ada dalam spawner walaupun ditulis dibawahnya. Ini terjadi karena print tersebut berada diluar async block sehingga akan dieksekusi secara langsung dan sinkron, Baru setelah itu, executor.run() mulai memproses task-task yang sebelumnya dikirim oleh spawner.spawn(). Disana task async dijalankan dan baru print yang ada di dalam spawner.spawn(). 