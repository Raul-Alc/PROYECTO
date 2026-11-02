# 🛒 TechShop

`Java 25` · `Aplicació de consola` · `Interfície ANSI / Unicode` · `0 dependències` · `1r FP Informàtica`

**TechShop** és una aplicació interactiva de consola per a gestionar una botiga d'informàtica i tecnologia (plataforma de comerç electrònic). Està dissenyada per a l'alumnat de **1r de FP d'Informàtica** i es construeix exclusivament amb tipus primitius, `String`, **vectors paral·lels** i **classes implícites de Java 25** (sense declaració de `class`), sense dependències externes ni frameworks.

Tot el programa viu en un únic fitxer, `projecte/Main.java`, i s'ha dissenyat per etapes: la interfície i l'estructura de dades ja estan implementades, i els mòduls de gestió es completen en les etapes següents.

---

## ✨ Funcionalitats principals

| Funcionalitat | Descripció | Estat |
|---|---|---|
| 👥 **Gestió de clients** | Directori interactiu, cerca per qualsevol camp (ID, nom, correu o telèfon), fitxa amb historial de compres, alta, modificació i baixa lògica (`ACTIU` / `BAIXA`). | 🚧 Etapa 1 · Tasca 1 |
| 📦 **Catàleg i estoc** | Llistat amb barra visual d'estoc i etiquetes (`EN ESTOC`, `BAIX`, `ESGOTAT`), cerca per ID, nom o categoria, alta, modificació, reposició i eliminació física. | 🚧 Etapa 2 · Tasques 5 i 6 |
| 💳 **Vendes i facturació** | Targetes d'estadístiques (`Math.max`, `Math.min`, mitjana i total), historial, cerca, registre de venda amb descompte d'estoc i emissió de tiquet amb codi aleatori (`Random`). | 🚧 Etapa 3 · Tasques 9 a 12 |
| 💾 **Persistència de dades** | Lectura automàtica en iniciar i guardat manual en `projecte/dades_botiga.txt` amb `Files.readString` i `Files.writeString`. | 🚧 Etapa 4 · Tasques 13 a 16 |
| 🎨 **Interfície ANSI** | Taules Unicode (`╭─┬─╮`), targetes KPI i missatges amb colors (`ok`, `error`, `avis`…) definits en una paleta ANSI única i aplicats als mètodes d'interfície. | ✅ Implementada |

**Estat actual:** en entrar a un mòdul pendent, l'aplicació mostra un avís d'«implementació pendent». Ja funcionen el panell principal, les targetes de resum, les cerques per identificador (`cercarIndexClientPerId`, `cercarIndexProductePerId`) i l'alta d'elements als vectors.

**Dades de demostració:** en iniciar, es carreguen 4 clients, 5 productes (88 unitats en estoc) i 2 vendes (799,49 € facturats).

---

## 🖥️ Vistes de l'aplicació

Eixida real de `java projecte/Main.java` en iniciar. A la terminal es veu amb colors ANSI; ací es mostra sense colors.

### Capçalera

```text
╭─────────────────────────────────────────────────────────────────────────────╮
│   ████████╗███████╗ ██████╗██╗  ██╗   ███████╗██╗  ██╗ ██████╗ ██████╗      │
│   ╚══██╔══╝██╔════╝██╔════╝██║  ██║   ██╔════╝██║  ██║██╔═══██╗██╔══██╗     │
│      ██║   █████╗  ██║     ███████║   ███████╗███████║██║   ██║██████╔╝     │
│      ██║   ██╔══╝  ██║     ██╔══██║   ╚════██║██╔══██║██║   ██║██╔═══╝      │
│      ██║   ███████╗╚██████╗██║  ██║   ███████║██║  ██║╚██████╔╝██║          │
│      ╚═╝   ╚══════╝ ╚═════╝╚═╝  ╚═╝   ╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚═╝          │
│                                                                             │
│     🛍️   P L A T A F O R M A   D E   C O M E R Ç   E L E C T R Ò N I C       │
│          Gestió de Clients · Catàleg d'Estoc · Facturació de Vendes         │
╰─────────────────────────────────────────────────────────────────────────────╯
```

### Targetes de resum

```text
╭────────────────────╮  ╭────────────────────╮  ╭────────────────────╮  ╭────────────────────╮
│ 👥 CLIENTS         │  │ 📦 ARTICLES        │  │ 💳 VENDES          │  │ 💰 FACTURAT        │
│            4 / 50  │  │        5 (88 un.)  │  │        2 comandes  │  │          799.49 €  │
╰────────────────────╯  ╰────────────────────╯  ╰────────────────────╯  ╰────────────────────╯
```

> El separador decimal de l'import depén de la configuració regional del sistema (`799.49 €` o `799,49 €`).

### Panell de control principal (taula del menú)

```text
✦ PANELL DE CONTROL PRINCIPAL ✦

╭──────┬─────────────────────────┬───────────────────────────────────────────────────╮
│ OPC. │ OPCIÓ                   │ DESCRIPCIÓ DE L'ACCIÓ                             │
├──────┼─────────────────────────┼───────────────────────────────────────────────────┤
│ [1]  │ 👥  GESTIÓ DE CLIENTS   │ Directori interactiu, consulta, historial i altes │
│ [2]  │ 📦  CATÀLEG I ESTOC     │ Catàleg interactiu, consulta, reposició i altes   │
│ [3]  │ 💳  VENDES I FACTURACIÓ │ Mètriques financeres, historial i comandes        │
│ [4]  │ 💾  GUARDAR DADES       │ Persistència al fitxer de dades (Java NIO)        │
│ [5]  │ 🚪  EIXIR DEL SISTEMA   │ Finalitzar sessió de treball                      │
╰──────┴─────────────────────────┴───────────────────────────────────────────────────╯

➤ Tria una opció [1-5]:
```

### Eixida de l'aplicació (opció 5)

```text
╭─────────────────────────────────────────────────────────────────────────────╮
│✔ Sessió finalitzada amb èxit! Gràcies per utilitzar la Botiga en Línia.     │
╰─────────────────────────────────────────────────────────────────────────────╯
```

---

## 🚀 Execució ràpida

### Requisits

- **JDK 25 o superior**
- Terminal amb codificació **UTF-8** i suport per a **colors ANSI**

### Execució

Des de l'arrel del repositori (la ruta del fitxer de dades, `projecte/dades_botiga.txt`, és relativa a aquest directori):

```
java projecte/Main.java
```

El fitxer inclou la capçalera de [JBang](https://www.jbang.dev/), de manera que també es pot executar amb `jbang projecte/Main.java`.

---

## 📚 Documentació

La documentació està organitzada segons el públic al qual s'adreça:

| Públic | Què necessita | On començar |
|---|---|---|
| 🧑‍💼 **Usuari / botiguer** | Aprendre a utilitzar l'aplicació | [Guia d'usuari](docs/user-guide.md) |
| 🧑‍🎓 **Alumnat i desenvolupadors** | Entendre el disseny, les dades i el codi | [Arquitectura](docs/architecture/overview.md) · [API](docs/api/README.md) |
| 🤝 **Col·laboradors** | Contribuir al projecte | [Guia de contribució](CONTRIBUTING.md) |
| 🛠️ **Administració i suport** | Instal·lar, desplegar i resoldre incidències | [Instal·lació](docs/installation.md) · [Desplegament](docs/deployment.md) · [Resolució de problemes](docs/troubleshooting.md) |

### Elements documentals

| # | Element | Contingut | Enllaços |
|---|---|---|---|
| 1 | 📖 **Guia d'usuari** | Ús de l'aplicació pas a pas | [`docs/user-guide.md`](docs/user-guide.md) |
| 2 | 🏗️ **Arquitectura** | Visió general, model de dades i diagrames | [`overview.md`](docs/architecture/overview.md) · [`data-model.md`](docs/architecture/data-model.md) · [`diagrams.md`](docs/architecture/diagrams.md) |
| 3 | 🔌 **Referència de l'API** | Mètodes i funcions del codi | [`docs/api/README.md`](docs/api/README.md) |
| 4 | 🤝 **Contribució** | Normes per a col·laborar | [`CONTRIBUTING.md`](CONTRIBUTING.md) |
| 5 | ⚙️ **Instal·lació i desplegament** | Preparar l'entorn i posar-lo en marxa | [`installation.md`](docs/installation.md) · [`deployment.md`](docs/deployment.md) |
| 6 | 🩺 **Resolució de problemes** | Errors habituals i solucions | [`docs/troubleshooting.md`](docs/troubleshooting.md) |
