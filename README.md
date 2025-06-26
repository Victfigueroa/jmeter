# Clase 5 - Módulo 4: Pruebas de Rendimiento con Apache JMeter

Este repositorio contiene el ejercicio guiado de la Clase 5 del curso de DevOps. Se realizaron pruebas de carga a una API REST usando Apache JMeter para evaluar su comportamiento ante múltiples usuarios concurrentes.

---

## Objetivos

- Instalar y configurar Apache JMeter.
- Simular usuarios concurrentes realizando peticiones a una API REST.
- Capturar métricas como tiempo promedio de respuesta, throughput y porcentaje de error.
- Exportar resultados en formato `.csv` y generar un reporte HTML.
- Ejecutar las pruebas desde la consola para futura integración CI/CD.

---

## API de prueba utilizada
(https://jsonplaceholder.typicode.com/users)

Simula una API REST que devuelve usuarios como si fueran clientes de una inmobiliaria.

---

## Ejecución desde consola

```bash
jmeter.bat -n -t jmeter-plan/prueba-usuarios.jmx -l resultados/resultados.jtl -e -o resultados/html-report
```
---

## Resultados

Los resultados se exportaron en:

- `summary.csv` (resumen)
- `aggregate.csv` (promedios agregados)
- Reporte HTML: [`resultados/html-report/index.html`](resultados/html-report/index.html)

---

## Reporte de Pruebas de Rendimiento

Puedes visualizar el reporte completo de las pruebas de rendimiento en línea en:

➡️ [Reporte HTML en GitHub Pages](https://victfigueroa.github.io/jmeter/docs/)

---

## Capturas de listeners

** Configuracion Jmeter
![Conf Prueba Jmeter](https://github.com/user-attachments/assets/a066b074-df33-49ac-a4d2-2a0a3dad1264)

** Peticion HTTP
![Peticion HTTP](https://github.com/user-attachments/assets/86caa44e-27af-48d0-be3f-d9eb06a42e0b)


1. **View Results in Table**  
   ![View Results in Table](https://github.com/Victfigueroa/jmeter/blob/main/Prints/View%20Results%20in%20Table.jpg)

2. **Summary Report**  
   ![Summary Report](https://github.com/Victfigueroa/jmeter/blob/main/Prints/Summary%20Report.jpg)

3. **Graph Results**  
   ![Graph Results](https://github.com/Victfigueroa/jmeter/blob/main/Prints/Graph%20Results.jpg)

4. **Aggregate Report**  
   ![Aggregate Report](https://github.com/Victfigueroa/jmeter/blob/main/Prints/Aggregate%20Report.jpg)

---
## Interpretaciones:

* Las metricas varían segun las veces que se ejecuten las prueba ya que se van sumando las pruebas
* Se puede concluir que el endpoint puede manejar las 250 solicitudes de forma fluida y estable, eso nos indica que la api es confiable para un posible paso a productivo.
* se realizaron las pruebas correspondientes una cantidad de veces definida (alrededor de 3 a 5 veces) sin realizar una acumulación de solicitudes y se llego a la conclusión de la mantención de estabilidad final en graficos y tablas con resultados exactamente similares o que fluctuan un minimo al resultado inicial.
## Grupo 5

- Juan Villaman  
- Cristóbal de Jesus  
- Victor Figueroa
