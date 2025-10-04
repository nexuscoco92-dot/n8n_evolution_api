# 🚀 Evolution API + n8n Setup en VPS

Este repositorio contiene la configuración actual de una plataforma desplegada en una VPS de AWS que incluye:

- Evolution API (`atendai/evolution-api:v2.1.1`)
- n8n (`n8nio/n8n:1.112.6`)
- Redis (`redis:7`)
- PostgreSQL (`postgres:15`)
- Reglas de iptables personalizadas
- Scripts de despliegue y parada

---

## 📁 Estructura del repositorio

evolution_api/
├── docker-compose.yml
├── .env
├── deploy_evolution.sh
├── stop_evolution.sh
├── iptables.rules

## ⚙️ Requisitos

- VPS con Ubuntu/Debian
- Docker y Docker Compose instalados
- Acceso root o sudo

---

## 🚀 Despliegue

### 1. Clona el repositorio

```bash
git clone git@github.com:nexuscoco92-dot/n8n_evolution_api.git
cd n8n_evolution_api

2. Revisa y edita el archivo .env
Este archivo contiene las variables necesarias para Evolution API y la conexión a PostgreSQL y Redis.

3. Ejecuta el script de despliegue
chmod +x deploy_evolution.sh
./deploy_evolution.sh

4. (Opcional) Aplica reglas de iptables
sudo iptables-restore < iptables.rules

5. Detener los servicios
./stop_evolution.sh



