# Bitácora de supervivencia — CitasSalud+

**Estudiante:**Juan Arce Araya
**Sección:** 11-6
**Fecha:** _27/8/2026___________________

## Escenario

Durante la ejecución de la prueba de performance (JMeter, listado de citas con
500 registros simulados — ver Anexo 1), el servidor principal de CitasSalud+
se satura y queda fuera de línea.

## 1. Identificación

<!-- ¿Cómo se detectó que el servidor había caído? ¿Qué señal o dato lo evidenció? -->

se detecto porque se detecto usando la herramienta jmeter al recibir resouestas con codigo HTTP503

## 2. Contención

<!-- ¿Qué acción se tomó de inmediato para limitar el impacto? -->

Se restringio el acceso general al modulo de las listas de citas

## 3. Recuperación

<!-- ¿Qué acción concreta permitió que la aplicación siguiera operando para
     citas de emergencia? Esta acción debe reflejarse en un commit de este
     repositorio con un mensaje descriptivo. -->
se habilito un modo de contingencia ligero deshabilitando consultas pesadas 


**Commit de recuperación:** (activa modo de contingencia para citas de emergencia y optimiza)

## 4. Aprendizaje / mejora

<!-- ¿Qué estrategia complementaria (respaldo, redundancia o monitoreo)
     hubiera anticipado este resultado, en relación con el criterio de
     performance del Anexo 1 (listado de citas en menos de 3 segundos)? -->

implementar una arquitectura basada en el balanceo de cargas