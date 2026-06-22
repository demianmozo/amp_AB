# Amplificador de Audio Clase AB

![UNMDP](https://img.shields.io/badge/UNMDP-Facultad_de_Ingeniería-blue)
![Carrera](https://img.shields.io/badge/Carrera-Ingeniería_Electrónica-brightgreen)
![Materia](https://img.shields.io/badge/Materia-Proyecto_Transversal_V-orange)

Repositorio con los archivos de diseño, simulación y fabricación de un amplificador de audio Clase AB, desarrollado como proyecto final para la asignatura **Proyecto Transversal V** de la **Universidad Nacional de Mar del Plata (UNMDP)**.

## 👥 Equipo de Trabajo
* **Ian P. Larrieu Lacoste**
* **Augusto Loyza**
* **Demian N. Mozo**

## 📝 Descripción del proyecto
El sistema cuenta con las siguientes características principales:
* **Topología:** Amplificador de potencia de audio Clase AB (utilizando transistores Darlington TIP141/146).
* **PCB:** Diseño simple faz (ruteado en la capa inferior `B.Cu`) pensado para CNC.

## 🛠️ Herramientas utilizadas
* **LTspice:** Simulación eléctrica del circuito y análisis de respuesta en frecuencia.
* **KiCad (v10):** Captura de esquemático y diseño del Layout del PCB (generación de Gerbers y Drill files).

## ⚙️ Notas de fabricación (CNC)
⚠️ **IMPORTANTE:** Para fabricar este PCB en la CNC:

1. **Importar archivos:** Cargar los archivos de cobre (`amp_AB-B_Cu.gbr`), contorno (`amp_AB-Edge_Cuts.gbr`) y los archivos de perforación (`amp_AB-PTH.drl` y `amp_AB-NPTH.drl`).
2. **Espejado (Mirror):** Como el ruteo se diseñó visto desde la capa superior (Top), se deben **seleccionar todos los archivos importados** y espejarlos simultáneamente (respecto al eje X o Y) utilizando la herramienta de FlatCAM. 
3. **Isolation Routing:** Generar las pasadas de la fresa.
4. **Perforación y Corte (Cutout):** Generar los G-Codes correspondientes para los agujeros y el corte del perímetro (`Edge_Cuts`).
