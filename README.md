# Pizarra Vial B

Aplicación web didáctica para profesores de formación vial del permiso B.

## Qué incluye esta primera versión

- Inicio y navegación por módulos.
- Biblioteca inicial de seis escenarios didácticos.
- Pizarra interactiva: cursor, flechas/líneas, vehículos, peatones, señales y textos; selección de escenario; deshacer, limpiar y guardar.
- Entorno real: mapa OpenStreetMap, búsqueda de direcciones con Nominatim y anotaciones al pulsar sobre el mapa.
- Recorridos: cálculo de ruta en coche con OSRM, distancia/tiempo aproximados y acceso al visor Mapillary en los puntos de inicio y destino.
- Aula: cinco preguntas iniciales con respuesta y explicación.
- Mis proyectos: guardado local y exportación de copia JSON.

## Instalación

Requisitos: Node.js 20 o superior.

```bash
npm install
npm run dev
```

Para generar la versión de producción:

```bash
npm run build
npm run preview
```

## Validación automática

Cada cambio enviado a `main` se comprueba mediante GitHub Actions: instala las dependencias, valida TypeScript y genera la compilación de producción. Así se detectan errores antes de publicar una nueva versión.

## Importante sobre mapas y panorámicas

- OpenStreetMap muestra cartografía de calles, no imágenes satélite.
- Nominatim, el servidor público de búsqueda de OpenStreetMap, tiene política de uso y límites; no debe utilizarse para consultas masivas.
- OSRM público es un servicio comunitario de demostración, sin garantía de disponibilidad ni SLA.
- Mapillary se abre en una pestaña externa centrada en las coordenadas. Solo habrá imágenes donde exista cobertura. Esta versión no integra un simulador 3D continuo ni garantiza una vista desde el asiento del conductor en todas las calles.
- Los servicios públicos pueden cambiar sus condiciones. Para uso comercial o intensivo se debe contratar/configurar un proveedor adecuado y respetar sus licencias y políticas.

## Datos y privacidad

Los proyectos se guardan en el almacenamiento local del navegador del dispositivo. No existe todavía una cuenta de profesor, sincronización en la nube ni base de datos compartida. Usa «Exportar copia de seguridad» para guardar los trabajos fuera del dispositivo.

## Alcance

Es una base funcional inicial para ampliar. Los escenarios visuales, preguntas, editor de pizarra y herramientas de mapa se pueden desarrollar en fases posteriores. No sustituye la normativa ni los criterios oficiales de evaluación de la DGT.

