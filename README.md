# Platforma Alumni UAIC — prototipuri interactive

**Proiect demonstrativ independent.** Nu este site-ul oficial al Universității „Alexandru Ioan Cuza” din Iași și nu reprezintă o implementare aprobată de UAIC sau de Fundația Alumni. Referințele instituționale sunt utilizate pentru ilustrarea propunerii. **Nu configurați DNS pentru domeniul oficial alumni.uaic.ro fără autorizarea titularului.**

Acest repository demonstrează cele **trei produse distincte** discutate în prezentarea „Platforma Alumni UAIC – propunere de dezvoltare etapizată” (octombrie 2026).

## Scenarii disponibile

| Scenariu | Estimare din propunere | Ce poate fi testat |
| --- | ---: | --- |
| 01 · Portal administrabil | ≈ 16.500 lei | Homepage, noutăți, calendar, formular simplu de înscriere, editor CMS |
| 02 · MVP Alumni (recomandat) | 33.000 lei (220 h) | Portal + cont demonstrativ, profil, înscrieri asociate contului, roluri, verificare manuală fictivă, admin, audit simulat, export CSV |
| 03 · Platformă extinsă | +36.000–50.000 lei peste MVP | MVP + demonstrații pentru mentorat, oportunități profesionale, director cu vizibilitate controlată |

Sumele reprezintă **estimări din propunere**, nu costuri ale prototipului și nici finanțare aprobată.

## Cum se testează

1. Deschide fișierul index.html în browser sau pornește local comanda: python3 -m http.server 8000
2. Folosește selectorul **01 Portal / 02 MVP / 03 Extins** din bara Studio de prototipuri.
3. Schimbă rolul din **Vizitator / Membru Alumni / Operator / Administrator**.
4. Testează înscrierea și anularea la un eveniment. În rolul Operator publică o noutate sau un eveniment. În rolul Administrator aprobă o solicitare fictivă și exportă CSV.
5. Butonul ↺ resetează datele simulate.

**Datele sunt inventate.** Informațiile se păstrează în sessionStorage, local în browser, până la închiderea sesiunii sau resetare. Nu introduceți informații personale reale în formulare. Nu se transmit date, nu se generează conturi, nu se efectuează verificări, nu se trimit e-mailuri și nu se fac rezervări reale.

## Fișiere

- **index.html** — structura paginilor și a interfețelor.
- **styles.css** — aspect responsive, navigare, componente.
- **app.js** — rutare locală, conținut fictiv, formulare și interacțiuni.

Aplicația este statică, fără proces de compilare și fără backend: HTML, CSS și JavaScript. Poate fi publicată pe un domeniu demonstrativ prin GitHub Pages, Vercel sau Cloudflare Pages.

### Publicare GitHub Pages

În repository, deschide **Settings → Pages → Build and deployment → Deploy from a branch**, apoi selectează ramura **main** și folderul **/(root)**. Adresa va fi https://dragosandreibobu.github.io/alumni.uaic.ro/ doar după activarea efectivă și finalizarea publicării. Nu seta domeniul oficial ca CNAME.

## Limite explicite

- Nu există backend, API, bază de date ori control de acces real. Selectorul de rol schimbă doar interfața.
- Nu există autentificare, confirmare e-mail, recuperare de parolă, SSO sau validare autentică a statutului de absolvent.
- CMS-ul, auditul, înscrierile, verificările și exportul sunt simulări locale.
- Nu sunt implementate procese GDPR instituționale, proceduri de retenție și ștergere, backup, securitate operațională sau validări server-side.
- Prototipul nu certifică nivelul WCAG 2.1 AA sau conformitatea juridică. Produsul real va necesita teste și validări.
- Persoanele, evenimentele, oportunitățile, mentorii și statisticile sunt fictive.

## Direcție tehnică recomandată pentru MVP-ul real (neimplementată aici)

Monolit modular cu backend și autorizare server-side, bază de date relațională și servicii pentru identitate, e-mail și backup. Module: Identity, AlumniProfiles, Content, Events, Registrations, Administration, Audit.

**Faza 0:** inventarierea sistemelor Alumni existente, clarificarea beneficiarului juridic (UAIC/Fundație), responsabilului de produs, fluxurilor de date și criteriilor de acceptanță.

**MVP:** portal public, CMS, conturi, profiluri, evenimente, înscrieri, roluri, audit, securitate, accesibilitate, testare și predare.

**Extinderi:** mentorat, director, oportunități și integrări numai după evaluarea utilizării MVP.

## Context public

- [UAIC — Absolvenți](https://www.uaic.ro/alumni/)
- [UAIC — Fundația Alumni](https://www.uaic.ro/alumni/fundatia-alumni/)

**Autor prototip:** Dragoș-Andrei Bobu. Statut: concept neoficial.
