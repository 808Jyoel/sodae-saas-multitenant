# Sodae — SaaS Multi-Tenant Gastronómico

Plataforma SaaS multi-tenant para operación gastronómica en tiempo real: POS, cocina, pagos y gestión centralizada.

![Sodae Hero](docs/sodae-hero.png)


## 🚀 Overview

**Sodae** es un sistema diseñado para digitalizar completamente la operación de restaurantes, bares y cafeterías.

Centraliza en una sola plataforma:

- Operación de salón (mesas, pedidos, reservas)
- Flujo de cocina y comandas en tiempo real
- Cobros digitales (QR / MercadoPago)
- Administración del negocio (usuarios, métricas)

Todo bajo una arquitectura **multi-tenant**, donde cada comercio opera de forma aislada y escalable.


## 🎥 Demo

### Gestión de Mesas (tiempo real)
![Gestión de mesas](docs/gestion-mesas.png)  
https://youtu.be/rzIzwL4FfK8



### Pagos con QR (MercadoPago)
![Pago Mercado Pago](docs/mercadopago-qr.png)  
https://youtu.be/_tiaAWkyocM



## 🧠 ¿Por qué es relevante?

Este proyecto simula un entorno real de producción:

- Manejo de múltiples negocios (multi-tenant)
- Sincronización en tiempo real (salón ↔ cocina ↔ caja)
- Flujo completo de operación (pedido → cocina → cobro)
- Integración con pagos externos



## ⚙️ Funcionalidades clave

- Gestión de mesas por zonas (piso, terraza, etc.)
- Creación y seguimiento de pedidos/comandas
- Flujo de cocina con estados de tickets
- Cobros con integración de pagos (QR)
- Gestión de usuarios por roles
- Comunicación en tiempo real (WebSockets)

---

## 🏗️ Arquitectura

Sistema modular dividido en:

- **Site** → onboarding y acceso público  
- **Admin** → métricas, usuarios, contabilidad  
- **POS** → operación en tiempo real  

Diseñado bajo enfoque:

- Multi-tenant
- Separación por dominios
- Escalabilidad por módulos

---

## 🛠️ Tecnologias 

- Frontend: Next.js (App Router)
- Backend: Next.js Route Handlers
- Lenguaje: TypeScript
- Base de datos: MySQL / MariaDB
- Tiempo real: WebSockets
- UI: CSS

---

## 📦 Estructura del Proyecto

```text
saas-gastro-structure-only/
  src/
    app/
      (site)/
        home/
        login/
        registro/
        r/
      (admin)/
        admin/
          users/
          metrics/
          accounting/
      (pos)/
        waiter/
        kitchen/
        tables/
        cobrar/
        restaurante/
      api/
        (public)/
          features/
          leads/
        (admin)/
          users/
          metrics/
          accounting/
        (pos)/
          orders/
          tables/
          kitchen/
          payments/
        (shared)/
          auth/
    components/
      floor-plan/
    modules/
      site/
      admin/
      pos/
      shared/
    lib/
  docs/
```

