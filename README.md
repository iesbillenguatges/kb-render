# 🗂️ Kanboard-Docker desplegat en Render.com

Aquest projecte et permet desplegar [Kanboard](https://kanboard.org/) amb Docker, ja siga localment o a Render.

---

## Desplegament amb Render

### 1. Crea un nou repositori amb aquest projecte a GitHub

Inclou almenys:
- `Dockerfile` (ve amb `kanboard/kanboard:latest`)
- Aquest `README.md`

### 2. A Render.com

- Ves a **Dashboard → New → Web Service**
- Selecciona el teu repo
- En **Environment**, tria: `Docker`
- Publica'l en el port `80` (ja està exposat per la imatge)

Després d'uns segons, tindràs la teua instància Kanboard online 🎉

---

## Execució local

```bash
docker build -t kanboard-app .
docker run -d -p 8080:80 kanboard-app
```

Accedeix a `http://localhost:8080`

Login per defecte:
- **Usuari**: `admin`
- **Contrasenya**: `admin`

---

## Configuració opcional

La imatge suporta variables d'entorn per connectar amb MySQL o PostgreSQL. Per exemple:

```env
DATABASE_URL=mysql://user:pass@host/dbname
```

Per persistència, pots muntar volums:
```bash
docker run -d -p 8080:80 -v kanboard_data:/var/www/app/data kanboard-app
```

---

## Enllaços útils

- [Web oficial](https://kanboard.org/)
- [Documentació Docker](https://github.com/kanboard/kanboard/blob/master/Docker.md)
- [Render Docs](https://render.com/docs/docker)


