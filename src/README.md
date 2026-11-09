# 🛒 TechShop

![Java 25](https://img.shields.io/badge/Java-25-ED8B00?logo=openjdk&logoColor=white)
![Aplicació de consola](https://img.shields.io/badge/Aplicaci%C3%B3-consola-4EAA25)
![Interfície ANSI](https://img.shields.io/badge/Interf%C3%ADcie-ANSI%20%2F%20Unicode-blue)
![Dependències](https://img.shields.io/badge/depend%C3%A8ncies-0-brightgreen)
![1º DAM · FP Superior](https://img.shields.io/badge/1º-DAM%20%C2%B7%20FP%20Superior-e08?labelColor=4C4C4C&style=flat)   
---

## ✨ Funcionalitats principals

| Funcionalitat | Descripció |
|---|---|
| 👥 **Gestió de clients** | Directori interactiu, cerca per qualsevol camp (ID, nom, correu o telèfon), fitxa amb historial de compres, alta, modificació i baixa lògica (`ACTIU` / `BAIXA`). |
| 📦 **Catàleg i estoc** | Llistat amb barra visual d'estoc i etiquetes (`EN ESTOC`, `BAIX`, `ESGOTAT`), cerca per ID, nom o categoria, alta, modificació, reposició i eliminació física. |
| 💳 **Vendes i facturació** | Targetes d'estadístiques (`Math.max`, `Math.min`, mitjana i total), historial, cerca, registre de venda amb descompte d'estoc i emissió de tiquet amb codi aleatori (`Random`). |
| 💾 **Persistència de dades** | Lectura automàtica en iniciar i guardat manual en `projecte/dades_botiga.txt` amb `Files.readString` i `Files.writeString`. |
| 🎨 **Interfície ANSI** | Taules Unicode (`╭─┬─╮`), targetes KPI i missatges amb colors definits en una paleta ANSI única i aplicats als mètodes d'interfície. |

---

## 🖥️ Vistes de l'aplicació

Eixida de `java projecte/Main.java` (panell de control principal). A la terminal es veu amb colors ANSI; ací es mostra sense colors.

### Targetes de resum

```text
╭────────────────────╮  ╭────────────────────╮  ╭────────────────────╮  ╭────────────────────╮
│ 👥 CLIENTS         │  │ 📦 ARTICLES        │  │ 💳 VENDES          │  │ 💰 FACTURAT        │
│            4 / 50  │  │        5 (88 un.)  │  │        2 comandes  │  │          799.49 €  │
╰────────────────────╯  ╰────────────────────╯  ╰────────────────────╯  ╰────────────────────╯
```

### Taula del menú

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

---

## 🚀 Execució ràpida

### Requisits

- **JDK 25 o superior**
- Terminal amb codificació **UTF-8** i suport per a **colors ANSI**

### Execució

Des de l'arrel del repositori:

```
java projecte/Main.java
```

---

## 📚 Documentació

La documentació s'organitza per a **quatre públics**. L'índex complet està a [`docs/README.md`](docs/README.md).

| Públic | Què necessita | On començar |
|---|---|---|
| 👤 **Usuaris** | Aprendre a utilitzar l'aplicació | [Manual d'usuari](docs/user-guide.md) |
| 💻 **Desenvolupadors** | Entendre el disseny, les dades i els mètodes | [Arquitectura](docs/architecture/overview.md) · [Model de dades](docs/architecture/data-model.md) · [Diagrames](docs/architecture/diagrams.md) · [API](docs/api/README.md) |
| 👥 **Col·laboradors** | Contribuir al projecte | [Guia de contribució](CONTRIBUTING.md) |
| 🚀 **Desplegament** | Instal·lar, desplegar i resoldre incidències | [Instal·lació](docs/installation.md) · [Desplegament](docs/deployment.md) · [Resolució de problemes](docs/troubleshooting.md) |

### Elements documentals

| # | Element | Contingut | Document |
|---|---|---|---|
| 1 | 📄 **Descripció del projecte** | Objectiu, funcionalitats, vistes i execució | [`README.md`](README.md) (aquest document) |
| 2 | 📖 **Manual d'usuari** | Ús pas a pas de cada pantalla | [`docs/user-guide.md`](docs/user-guide.md) |
| 3 | 🏛️ **Arquitectura i model de dades** | Organització del codi, vectors paral·lels i diagrames | [`overview.md`](docs/architecture/overview.md) · [`data-model.md`](docs/architecture/data-model.md) · [`diagrams.md`](docs/architecture/diagrams.md) |
| 4 | 📚 **Referència de mètodes (API)** | Mètodes de `Main.java` agrupats per mòdul | [`docs/api/README.md`](docs/api/README.md) |
| 5 | 🤝 **Guia de contribució** | Normes de codi, branques i *pull requests* | [`CONTRIBUTING.md`](CONTRIBUTING.md) |
| 6 | 🚢 **Instal·lació, desplegament i problemes** | Requisits, execució a l'aula i errors freqüents | [`installation.md`](docs/installation.md) · [`deployment.md`](docs/deployment.md) · [`troubleshooting.md`](docs/troubleshooting.md) |