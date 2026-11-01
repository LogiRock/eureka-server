# eureka-server

Servidor de descubrimiento (Netflix Eureka) de LogiTrack. Los servicios se registran acá y se buscan por nombre lógico (`SHIPMENT-SERVICE`, `COURIER-SERVICE`, `SECURITY-SERVICE`).

- **Puerto:** 8065
- **Dashboard:** http://localhost:8065
- **Configuración:** `eureka-server.yml` en [LogiRock/config-server](https://github.com/LogiRock/config-server)

## Variables de entorno

| Variable | Default | Para qué |
|---|---|---|
| `CONFIG_SERVER_URL` | `http://localhost:8088` | Dónde está el config-server. En Docker: `http://config-server:8088` |
| `PORT` | `8065` | Puerto del servidor |

## Levantar

Desde IntelliJ: ejecutar `EurekaServerApplication`.

Con Docker:

    docker build -t logirockjujuy/eureka-server:v1.0.0 .
    docker run -p 8065:8065 logirockjujuy/eureka-server:v1.0.0server