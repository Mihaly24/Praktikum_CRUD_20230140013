## 📚 Dokumentasi API

Base URL: http://localhost:8080  
Content-Type: application/json

### 1. Tambah Data User Baru (Create)
Menambahkan data user baru. ID akan *digenerate* secara otomatis dalam bentuk UUID.

* URL: /api/users
* Method: POST
* Request Body:
    
```json
    {
        "name": "Fairuz Kurnia",
        "age": 22
    }
```

* Success Response (201 Created):

```json
    {
        "status": "success",
        "data": {
            "id": "11568f9e-0f71-467d-9099-b9c8db03d019",
            "name": "Fairuz Kurnia",
            "age": 22
        }
    }
```

### 2. Ambil Semua Data User (Read All)
Menampilkan daftar seluruh user yang ada di dalam *database*.

* URL: /api/users
* Method: GET
* Success Response (200 OK):
    
```json
    {
        "status": "success",
        "data": [
            {
                "id": "11568f9e-0f71-467d-9099-b9c8db03d019",
                "name": "Fairuz Kurnia",
                "age": 22
            }
        ]
    }
```

### 3. Ambil Detail User Spesifik (Read Detail)
Mencari dan menampilkan detail satu user berdasarkan ID.

* URL: /api/users/{id}
* Method: GET
* URL Params: id=[String]
* Success Response (200 OK):
    
```json
    {
        "status": "success",
        "data": {
            "id": "11568f9e-0f71-467d-9099-b9c8db03d019",
            "name": "Fairuz Kurnia",
            "age": 22
        }
    }
```

### 4. Ubah Data User (Update)
Memperbarui data nama dan/atau umur dari user yang sudah ada.

* URL: /api/users/{id}
* Method: PUT
* URL Params: id=[String]
* Request Body:
    
```json
    {
        "name": "Fairuz Kurnia Update",
        "age": 22
    }
```

* Success Response (200 OK):

```json
    {
        "status": "success",
        "data": {
            "id": "11568f9e-0f71-467d-9099-b9c8db03d019",
            "name": "Fairuz Kurnia Update",
            "age": 22
        }
    }
``` 

### 5. Hapus Data User (Delete)
Menghapus data user secara permanen dari *database*.

* URL: /api/users/{id}
* Method: DELETE
* URL Params: id=[String]
* Success Response (200 OK):
    
```json
    {
        "status": "success delete user with id 11568f9e-0f71-467d-9099-b9c8db03d019"
    }
```

## SS Hasil
Hasil tampilan web: <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a225a446-b81e-4189-aa3f-4e4c1ce6e329" />
