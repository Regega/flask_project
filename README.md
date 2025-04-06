
# Flask API serveris ir klientas 🚀

Šis projektas sukurtas su Python ir Flask. Jame pateikiamas API serveris, kuris leidžia gauti vartotojų informaciją ir ją papildyti. Taip pat yra klientas, kuris siunčia HTTP užklausas į serverį.

## 📁 Projekto struktūra

```
projektas/
├── api_server.py          # Flask API serveris
├── api_client.py          # Python klientas
├── requirements.txt       # Priklausomybės (Flask)
├── Dockerfile             # Docker konfigūracija
```

## ⚙️ Paleidimas

### 🔸 1. Paleisti serverį lokaliai (be Docker)

```bash
pip install -r requirements.txt
python api_server.py
```

### 🔸 2. Paleisti klientą

```bash
python api_client.py
```

---

## 🐳 Docker naudojimas

### 🔸 1. Sukurkite Docker vaizdą

```bash
docker build -t flask_project .
```

### 🔸 2. Paleiskite serverį

```bash
docker run -p 5000:5000 flask_project
```

### 🔸 3. Testuokite per `curl`

```bash
curl http://localhost:5000/users
curl http://localhost:5000/users/1
curl -X POST http://localhost:5000/users -H "Content-Type: application/json" -d "{\"name\": \"Petras\", \"email\": \"petras@example.com\"}"
```

---

## ✅ Funkcionalumas

- Gauti visus vartotojus (`GET /users`)
- Gauti vieną vartotoją pagal ID (`GET /users/<id>`)
- Pridėti naują vartotoją (`POST /users`)

---

## 💡 Sukūrė

Regimantas, 2025 m.  
Projektas atliktas Python, API, GitHub ir Docker praktikai.
