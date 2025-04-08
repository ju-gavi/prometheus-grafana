# Práctica Final Prometheus y Grafana

Este repositorio contiene la solución de la práctica final del curso de Prometheus y Grafana. Se incluyen:

- **docker-compose.yml:** Orquesta la siguiente infraestructura:
  - Tres contenedores del servicio `julius/prometheus-demo-service` en los puertos 10000, 20000 y 30000.
  - Un contenedor de Prometheus (con el fichero de configuración `prometheus.yml`).
  - Un contenedor de Grafana (con volumen `grafana-storage` y dependencia de Prometheus).
  - Un contenedor de node-exporter.

- **Dashboards:**  
  Se incluyen los archivos JSON exportados desde Grafana:
  - `dashboard_api.json`: Contiene las consultas para el percentil 90, percentil 95 y promedio de la duración de las solicitudes HTTP.
  - `dashboard_recursos.json`: Dashboard dedicado a los recursos de cómputo (panel de CPUs y panel gauge del uso de FS).

## Instrucciones de Uso

1. **Clonar el repositorio:**

   ```bash
   git clone https://github.com/ju-gavi/prometheus-grafana.git
   cd prometheus-grafana 
