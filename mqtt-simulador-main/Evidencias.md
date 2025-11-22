# EVIDENCIA DE VALIDACIÓN - PROYECTO 
## FASE 0: Despliegue. 
**Prueba:** Creación de los 5 subscribers. 
**Resultado Esperado:** Creados correctamente. 
**Log Capturado:** 
>[Copiar aquí la línea del log del contenedor persistence-subscriber donde 
dice "WARN: Rejected future packet..." 
## FASE 1: Sincronización
**Prueba:** Pausa del Líder actual. 
**Resultado Esperado:** Elección de nuevo líder por mayoría (3/5). 
**Log Capturado:** 
> [Copiar aquí log del Nuevo Líder: "Won election with 3 votes"] 
> [Copiar aquí log del Viejo Líder al volver: "Lease expired. Stepping 
down"] 
## FASE 2: El consenso
**Prueba:** Reinicio forzado (Kill) del Coordinador con cola llena. 
**Resultado Esperado:** Restauración de la cola al iniciar. 
**Log Capturado:** 
> [Coloca aquí log de inicio: "[WAL] Replaying 5 events... Queue restored."] 
## FASE 2: Resiliencia
**Prueba:** Reinicio forzado (Kill) del Coordinador con cola llena. 
**Resultado Esperado:** Restauración de la cola al iniciar. 
**Log Capturado:** 
> [Coloca aquí log de inicio: "[WAL] Replaying 5 events... Queue restored."] 