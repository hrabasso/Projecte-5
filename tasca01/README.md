
# T01: DRP – Còpies de Seguretat: Estudi Cas Client (Treball Cooperatiu)

## Breu Descripció
Aquest projecte consisteix a analitzar i dissenyar una política de còpies de seguretat per a l’empresa **"Muntatges i Serveis Tècnics SL"**, seguint una dinàmica cooperativa en tres fases: treball individual, per parelles i en grup.

---

## Introducció
La primera sessió introdueix el tema de les còpies de seguretat amb material didàctic proporcionat pel responsable de seguretat. A continuació, els alumnes treballen els aspectes pràctics a partir del cas client.

---

## Cas Client

**Empresa:** Muntatges i Serveis Tècnics SL  
**Activitat:** Instal·lació i manteniment d’equips industrials  

### Infraestructura Tècnica
- **Servidor de Fitxers (Ubuntu Server)**
  - Documents de Projectes: 300 GB, creixement moderat  
  - Bases de Dades (Comptabilitat i Clients): 20 GB, canvi constant  
  - Carpetes Personals dels Usuaris: 100 GB
- **10 Equips Clients (Windows 10/11)**
  - La majoria de treball amb fitxers del servidor  
  - Carpeta *Documents* utilitzada temporalment per informes importants
- **Connexió a Internet:** Fibra òptica 600 Mbps simètrica

### Requisits de Recuperació
- **RTO:** <4 h per a Comptabilitat/Clients  
- **RPO:** ≤24 h per la majoria de dades; ≤4 h per Comptabilitat/Clients  
- **Retenció:** Històric mínim d’un mes

---

## Fase 1: Treball Individual

### ![Fase 1](./fase1.md)

1. **Què copiar (Priorització)**
   - Bases de Dades: Critiques, ús diari → prioritat màxima  
   - Documents de Projectes: Moderadament crítics → prioritat mitjana-alta  
   - Carpetes Personals: Ús diari → prioritat mitjana  
   - PCs Clients: Només carpeta *Documents* si conté arxius importants

2. **Periodicitat i Tipus de Còpia**
   | Tipus de dades                  | Diari               | Setmanal      | Mensual       |
   |---------------------------------|-------------------|---------------|---------------|
   | Bases de Dades (BD)             | Incremental 4 h + Completa nocturna | Completa | Completa + arxiu |
   | Documents de Projectes / Personals | Incremental       | Completa      | Completa      |
   | PCs Clients (Documents)          | Incremental       | Completa      |               |

3. **Mitjans i Ubicació (Regla 3-2-1)**
   - **Mitjà 1 (Local):** NAS per còpies ràpides  
   - **Mitjà 2 (Extern):** Cloud off-site (Backblaze B2, Azure, AWS S3)  
   - **Còpia més recent:** Sempre al NAS local  
   - **Còpia externa fora de lloc:** Cloud per protegir contra robatori, incendi o ransomware

---

## Fase 2: Treball per Parelles

### ![Fase 2](./fase2.md)

1. Comparació de respostes individuals  
2. Disseny d’una proposta unificada amb esquema **3-2-1**  
   - Proposta amb justificació de dades crítiques, periodicitat, tipus de còpia i mitjans (local i extern)

---

## Fase 3: Treball en Grup

### ![Fase 3](./fase3.md)

1. Debat i selecció de la millor proposta  
2. Disseny de la **Política de Còpies de Seguretat Definitiva**
   - **Dades objecte de còpia:** Servidor/Clients, crítiques/no crítiques  
   - **Cronograma setmanal detallat** amb tipus de còpia i mitjà  
   - **Mitjans i ubicació:** Local (NAS, disc dur), extern (Cloud, LTO)  
   - **Estratègia de recuperació:** Garantir RTO i RPO per a BD

---

## Materials i Links de Suport
- Moodle 0226 Seguretat Informàtica. RA2.AA3Còpies  
- INCIBE: [Copias de seguridad – guía empresarial](https://www.incibe.es)  
- Xataka: [Backup 3-2-1, el método definitivo](https://youtu.be/PM_M4Iz6I4o?si=F7DRyDDTZE3hjWn8) (YouTube, Setembre 2017)
