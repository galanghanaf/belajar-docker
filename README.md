# Belajar Docker
Docker adalah platform yang dapat digunakan untuk memasukan dan menyatukan berbagai program, 
software maupun sistem operasi ke dalam suatu wadah yang disebut ***container***. 
Container tersebut nantinya akan memuat kumpulan ***image*** yang berisi data konfigurasi 
file serta pendukung lainnya.

## Menginstal Docker 
```
https://docs.docker.com/engine/install/
```

## Melakukan Pull Image
```
docker pull <nama_image>
```
- contoh melakukan pull image dari https://hub.docker.com
```
docker pull nginx
```

## Melihat Image yang tersimpan
```
docker image ls
```
- atau
```
docker images
```

## Menghapus Image
- Catatan : Image dapat dihapus bila container telah dihentikan atau dihapus.
```
docker image rm <nama_image>
```
- contoh
```
docker image rm nginx
```

## Menjalankan image (inilah yang disebut ***container***)
```
docker run --name <nama_containernya_bebas> -p <portnya_bebas>:80 -d <nama_image>
```
- contoh
```
docker run --name website -p 8080:80 -d nginx
```

## Melihat container yang sedang berjalan
```
docker ps
```

## Melihat container yang sedang berjalan maupun yang tidak berjalan
```
docker ps -a
```

