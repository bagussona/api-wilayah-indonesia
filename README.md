API Data Wilayah Indonesia - Forked from [emsifa](https://github.com/emsifa/api-wilayah-indonesia)
==========================

Demo: [https://bagussona.github.io/api-wilayah-indonesia/](https://bagussona.github.io/api-wilayah-indonesia/)

## ENDPOINTS

#### 1. Mengambil Daftar Provinsi

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/provinces.json
```

Contoh Response:

```
[
  {
    "id": "32",
    "name": "JAWA BARAT"
  },
  {
    "id": "33",
    "name": "JAWA TENGAH"
  }
  ...
]
```

#### 2. Mengambil Daftar Kab/Kota pada Provinsi Tertentu

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/regencies/{provinceId}.json
```

Contoh untuk mengambil daftar kab/kota di provinsi Jawa Barat (ID = 32):

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/regencies/32.json
```

Contoh Response:

```
[
  {
    "id": "3204",
    "province_id": "32",
    "name": "KABUPATEN BANDUNG"
  },
  {
    "id": "3205",
    "province_id": "32",
    "name": "KABUPATEN GARUT"
  },
  ...
]
```

#### 3. Mengambil Daftar Kecamatan pada Kab/Kota Tertentu

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/districts/{regencyId}.json
```

Contoh untuk mengambil daftar kecamatan di Kabupaten Garut (ID = 3205):

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/districts/3205.json
```

Contoh Response:

```
[
  {
    "id": "3205190",
    "regency_id": "3205",
    "name": "GARUT KOTA"
  },
  {
    "id": "3205200",
    "regency_id": "3205",
    "name": "KARANGPAWITAN"
  },
  ...
]
```

#### 4. Mengambil Daftar Kelurahan pada Kecamatan Tertentu

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/villages/{districtId}.json
```

Contoh untuk mengambil daftar kelurahan di Kecamatan Garut Kota (ID = 3205190):

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/villages/3205190.json
```

Contoh Response:

```
[
  {
    "id": "3205190004",
    "district_id": "3205190",
    "name": "KOTAWETAN"
  },
  {
    "id": "3205190005",
    "district_id": "3205190",
    "name": "KOTAKULON"
  },
  ...
]
```

#### 5. Mengambil Data Provinsi berdasarkan ID Provinsi

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/province/{provinceId}.json
```

Contoh untuk mengambil data provinsi Jawa Barat (ID = 32):

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/province/32.json
```

Contoh Response:

```
{
  "id": "32",
  "name": "JAWA BARAT"
}
```

#### 6. Mengambil Data Kab/Kota berdasarkan ID Kab/Kota

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/regency/{regencyId}.json
```

Contoh untuk mengambil data Kabupaten Garut (ID = 3205):

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/regency/3205.json
```

Contoh Response:

```
{
  "id": "3205",
  "province_id": "32",
  "name": "KABUPATEN GARUT"
}
```

#### 7. Mengambil Data Kecamatan berdasarkan ID Kecamatan

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/district/{districtId}.json
```

Contoh untuk mengambil data Kecamatan Garut Kota (ID = 3205190):

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/district/3205190.json
```

Contoh Response:

```
{
  "id": "3205190",
  "regency_id": "3205",
  "name": "GARUT KOTA"
}
```

#### 8. Mengambil Data Kelurahan berdasarkan ID Kelurahan

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/village/{villageId}.json
```

Contoh untuk mengambil data Kelurahan Kota Kulon (ID = 3205190005):

```
GET https://bagussona.github.io/api-wilayah-indonesia/api/village/3205190005.json
```

Contoh Response:

```
{
  "id": "3205190005",
  "district_id": "3205190",
  "name": "KOTAKULON"
}
```

## LIMITASI

Karena API ini dihosting di Github Page, Github Page sendiri memberikan batasan bandwith 100GB/bulan. Rata-rata endpoint disini memiliki ukuran 1KB/endpoint, jadi kurang lebih request yang dapat digunakan adalah 100.000.000 request per bulan, atau sekitar 3.000.000 request/hari.

Untuk lebih detail tentang limitasi Github Page, bisa dilihat [disini](https://help.github.com/en/articles/about-github-pages#usage-limits).
