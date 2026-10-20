# CumpleChile 🇨🇱

**Plataforma SaaS para gestión de cumplimiento de la Ley 21.719 de protección de datos personales en Chile.**

Basada en el **Decreto 662** del Ministerio de Hacienda (publicado el 9 de septiembre de 2026) que regula los Modelos de Prevención de Infracciones.

## Características

### Módulos Implementados

| Módulo | Artículos | Descripción |
|--------|-----------|-------------|
| **Programa de Cumplimiento** | Art. 3 | Creación y gestión del programa con todos los elementos mínimos requeridos |
| **Delegado (DPO)** | Arts. 6-13 | Designación, cualidades, funciones y plan anual del delegado |
| **Actividades de Tratamiento** | Art. 3(d) | Registro completo de actividades de tratamiento de datos |
| **Matriz de Riesgos** | Art. 3(e) | Identificación, evaluación y mitigación de riesgos con graduación de sanciones |
| **Reportes y Denuncias** | Arts. 3(g), 3(i) | Canal interno con protección de identidad del denunciante |
| **Certificación** | Arts. 14-20 | Gestión de solicitudes ante la Agencia de Protección de Datos |
| **Capacitaciones** | Art. 13(f) | Planificación y seguimiento de formación en protección de datos |
| **Dashboard** | — | Vista de cumplimiento con score y checklist legal |

### Stack Tecnológico

- **Frontend:** Next.js 14 (App Router), React 18, Tailwind CSS, Lucide Icons
- **Backend:** Next.js API Routes, Prisma ORM
- **Base de Datos:** SQLite (cambiable a PostgreSQL)
- **Autenticación:** NextAuth.js con credenciales
- **Despliegue:** Vercel, Docker, o cualquier servidor Node.js

## Instalación

```bash
# 1. Instalar dependencias
npm install

# 2. Configurar base de datos
npx prisma db push

# 3. Cargar datos de demostración
npx prisma db seed

# 4. Iniciar el servidor
npm run dev
```

## Datos de Demostración

- **Email:** admin@empresademo.cl
- **Password:** demo1234

La demo incluye una organización completa con DPO, programa de cumplimiento, actividades de tratamiento, matriz de riesgos, reportes y capacitaciones.

## Estructura del Proyecto

```
cumple-app/
├── prisma/
│   ├── schema.prisma      # Modelo de datos completo
│   └── seed.ts            # Datos de demostración
├── src/
│   ├── app/
│   │   ├── api/           # API Routes
│   │   │   ├── auth/      # Autenticación
│   │   │   ├── programa/  # Programa de cumplimiento
│   │   │   ├── dpo/       # Delegado
│   │   │   ├── riesgos/   # Matriz de riesgos
│   │   │   ├── reportes/  # Reportes y denuncias
│   │   │   ├── certificacion/
│   │   │   ├── capacitaciones/
│   │   │   └── actividades/
│   │   ├── dashboard/     # Panel principal
│   │   ├── programa/      # Programa de cumplimiento
│   │   ├── dpo/           # Gestión del DPO
│   │   ├── riesgos/       # Matriz de riesgos
│   │   ├── reportes/      # Reportes y denuncias
│   │   ├── certificacion/ # Certificación
│   │   ├── capacitaciones/
│   │   ├── actividades/   # Actividades de tratamiento
│   │   ├── login/         # Inicio de sesión
│   │   └── register/      # Registro
│   ├── components/        # Componentes compartidos
│   └── lib/               # Utilidades (Prisma, Auth)
└── public/
```

## Base Legal

- **Ley N° 19.628** — Sobre Protección de la Vida Privada
- **Ley N° 21.719** — Protección y tratamiento de datos personales
- **Decreto 662** — Reglamento de Modelos de Prevención de Infracciones
- **Fecha de vigencia:** 1 de diciembre de 2026

## Licencia

MIT
