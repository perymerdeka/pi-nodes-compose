# pinode scripts


## Menjalankan Stellar Quickstart dengan Docker Compose


**Tentang Panduan Ini:**

Panduan ini menjelaskan cara menjalankan Stellar Quickstart dengan Docker Compose.

**Persiapan:**

* Instal Docker Compose ([https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/))

#### Dokumentasi Port Pinodes

sesuaikan dengan port yang mau dibuka

| Port  | Service      | Description          |
| ----- | ------------ | -------------------- |
| 5432  | postgresql   | database access port |
| 8000  | horizon      | main http port       |
| 6060  | horizon      | admin port           |
| 11625 | stellar-core | peer node port       |
| 11626 | stellar-core | main http port       |

### Example (Contoh)

---

lakukan ini di terminal atau CMD

masuk ke dalam file ini di download biasanya dalam file pi-nodes

```bash
cd pi-nodes
```

kemudian jalankan

```bash
docker-compose up # untuk mode non background
```

```bash
docker-compose up -d # untuk mode background (latar belakang)
```


**Akses Horizon:**

Buka browser web dan kunjungi [http://localhost:8000](http://localhost:8000)

**Langkah Opsional:**

* **Lihat log:**

```
docker logs stellar
```

* **Buka konsol Stellar Core:**

```
docker exec -it stellar stellar-core console
```

* **Jelajahi port lain:**

Jika Anda mengekspos port lain (misalnya, **11626** dan 11625) di konfigurasi Docker Compose, Anda dapat mengaksesnya di `localhost:port` yang sesuai.


**Langkah Opsional:**

* Lihat log: `docker logs stellar`
* Buka konsol Stellar Core: `docker exec -it stellar stellar-core console`
* Jelajahi port lain (jika diekspos)

**Tips:**

* Modifikasi konfigurasi `docker-compose.yml` untuk menyesuaikan pengaturan
* Hentikan container: `docker-compose down`
* Hapus image: `docker-compose rm -f`

**Catatan:**

* Ikuti panduan dan persyaratan layanan Stellar saat menggunakan Pubnet
* Info lebih lanjut tentang Stellar Quickstart: [https://github.com/stellar/quickstart](https://github.com/stellar/quickstart)

**Referensi:**

* [https://docs.docker.com/compose/](https://docs.docker.com/compose/)
* [https://github.com/stellar/quickstart](https://github.com/stellar/quickstart)
