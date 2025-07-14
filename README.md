# 🗂️ Kanboard-Docker desplegat en Render.com

Aquest projecte et permet desplegar [Kanboard](https://kanboard.org/) amb Docker a Render.

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

Després d'uns pocs segons, tindràs la teua instància Kanboard online

---

Login per defecte:
- **Usuari**: `admin`
- **Contrasenya**: `admin`

---


- [Web oficial](https://kanboard.org/)
- [Documentació Docker](https://github.com/kanboard/kanboard/blob/master/Docker.md)
- [Render Docs](https://render.com/docs/docker)


