
# T09: Servidor de Fitxers Linux — NFS (Tasca Individual)

## Resum de la Tasca

L'objectiu d'aquesta pràctica és implementar un **servidor de fitxers centralitzat** utilitzant **NFSv3** en un entorn Linux per a la startup fictícia **DevOptimize Solutions**. El client treballa exclusivament amb Linux i no disposa d’autenticació centralitzada, així que els permisos i usuaris es gestionen de manera local.

Es demana:

- Configurar un **servidor NFS** i un **client Linux** que accedeixi als recursos compartits.
- Crear **usuaris i grups** per simular l’entorn real del client.
- Configurar **permisos d’accés** amb `/etc/exports`, `chmod` i `chown`.
- Demostrar el funcionament de:
  - Exportacions per a administradors (`admin_tools`) i desenvolupadors (`dev_projects`).
  - Diferències entre `root_squash` i `no_root_squash`.
  - Permisos de lectura/escriptura segons IP i grup.
- Configurar el **muntatge automàtic** dels recursos compartits al client amb `/etc/fstab`.
- Documentar el procés i redactar una **conclusió crítica** amb recomanacions de millora i seguretat.

**Resultat esperat:**  
Un entorn NFS funcional que mostri com els usuaris poden accedir als recursos compartits segons els permisos definits, juntament amb un anàlisi de les limitacions i propostes de millora per a un entorn més segur i escalable.
