# LabVIEW – Gemelo Digital de Ascensor a Escala  

Este módulo corresponde al desarrollo en **LabVIEW** del gemelo digital del ascensor a escala ubicado en el **Laboratorio de Control Automático de la Escuela de Ingeniería Eléctrica (PUCV)**.  

## 🎯 Objetivo  
Construir una **réplica virtual del ascensor** que permita:  
- Ejecutar y validar maniobras de control.  
- Visualizar el desplazamiento de las cabinas en tiempo real.  
- Integrarse con el **PLC Siemens S7-1200** mediante servidor OPC.  
- Proveer una plataforma **segura y pedagógica** para experimentar sin comprometer la maqueta física.  

## 🛠️ Características principales  
- **Programación en LabVIEW** basada en flujo de datos.  
- **Maniobras implementadas**:  
  - Maniobra Universal (MU).  
  - Maniobra Demostrativa (MD).  
  - Maniobra Colectiva (MC).  
- **Optimización del código** mediante:  
  - Uso de **subVIs** (fotosensores, selección de modo, maniobras, etc.).  
  - Uso de **clusters** para mejorar legibilidad y escalabilidad.  
- **Visualización avanzada**:  
  - Interfaz gráfica realista con cabinas, rieles y luces de piso.  
  - Movimiento continuo de cabinas.  
  - Indicadores: motores, relés, fotosensores, display de siete segmentos.  

## 🔗 Integración con PLC  
- Comunicación establecida con **PLC Siemens S7-1200** vía **KepServerEX (OPC)**.  
- Estrategia aplicada:  
  - Uso de **marcas internas (%M)** en lugar de entradas físicas (%I), reservando el rango **M700.0–M730.0** para simulación.  
  - Lectura de salidas (%Q) y estados internos para sincronización gráfica.  
  - Escritura en marcas desde LabVIEW para simular sensores y pulsadores.  

## 📂 Estructura del proyecto  
- `/VIs` → Archivos principales de LabVIEW.  
- `/SubVIs` → Subrutinas modulares (maniobras, sensores, etc.).  
- `/Docs` → Diagramas y documentación asociada.  
- `/Screenshots` → Capturas de interfaz y resultados de pruebas.  

## 🚀 Ejecución  
1. Abrir el proyecto en **LabVIEW 2021 o superior**.  
2. Configurar conexión con servidor **OPC KepServerEX** (ver `/Docs`).  
3. Seleccionar modo de operación desde la interfaz gráfica.  
4. Observar en tiempo real el movimiento de cabinas y los indicadores.  

## 📌 Estado actual  
- [x] Simulación funcional en LabVIEW.  
- [x] Integración con PLC simulado (PLCSIM + NetToPLCsim).  
- [x] Comunicación OPC estable con LabVIEW.  
- [ ] Validación completa con PLC físico (pendiente).  
