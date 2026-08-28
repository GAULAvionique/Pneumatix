<!--"""[![MasterHead](Documentation/GAUL/logo-full.webp)](https://gaulspace.web.app/home)-->

<h1 align="center">Projet Pneumatix - GAUL 2024-2025</h1>

<img align="right" src="https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2FGAULAvionique2024-2025%2FPneumatix&label=Visiteurs&labelColor=%23697689&countColor=%23f47373&style=flat" alt="Visiteurs" />

<p align="left">
  <a href="https://www.facebook.com/gaul.ul" target="_blank">
    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/facebook.svg" alt="GAUL Facebook" height="30" width="40" />
  </a>
  <a href="https://www.instagram.com/gaul.ul/" target="_blank">
    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="GAUL Instagram" height="30" width="40" />
  </a>
  <a href="https://www.facebook.com/groupeaerospatialul/" target="_blank">
    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/youtube.svg" alt="GAUL Youtube" height="30" width="40" />
  </a>
</p>

## 🌟 **Projet Pneumatix**

Pneumatix est un **module de communication et de télémétrie séparé** développé par le GAUL pour assurer un relais de données fiable entre les systèmes embarqués de la fusée et la station au sol. Conçu comme une carte fille (PCB de communication) isolée du PCB principal, le système garantit une intégrité maximale des signaux RF.

Le projet est conçu pour être :

*   Performant sur de longues distances (Module LoRa 433MHz)
*   Modulable avec un contrôle matériel des états (M0/M1) manuellement
*   Robuste face aux interférences électromagnétiques et à l'effet Doppler

L’objectif principal de Pneumatix est d'assurer une liaison de télémétrie fiable (comparée au RFD900X).

---

## 📦 **Fonctionnalités Intégrées**

Le système centralise l'infrastructure de communication externe et inclut :

*   **Communication Radio LoRa**
    Intégration du module EBYTE E22-400T33S avec routage d'antenne SMA 50 ohms pour une portée maximale et gestion des canaux LBT (Listen Before Talk).
*   **Microcontrôleur (Optionnel / Déporté)**
    Interfaçage direct avec le STM32F4 de ODBlix via des signaux logiques 3.3V natifs ou possibilité de programmer seul.
*   **Contrôle de Mode Matériel**
    Configuration des modes de fonctionnement (Normal, WOR, Configuration, Veille) via des *solder jumpers* sur les broches M0 et M1.
*   **Indicateurs de statut**
    Diagnostic visuel via des LEDs dédiées pour l'alimentation 5V et l'état d'occupation du buffer série (broche AUX).

---

## 🛰 **Architecture du Projet**

Le dépôt contient l’ensemble des éléments matériels et logiciels nécessaires au déploiement du module :

*   Schémas de conception PCB (Routage RF)
*   Scripts de configuration des registres LoRa
*   Documentation technique

---

## 📚 **Documentation**

La documentation complète des pièces du projet est disponible dans le dossier `Documentation/`.

---

## ⚙ **Compilation et Déploiement**

Le code d'interfaçage est développé autour de l’écosystème ODBLix pour communiquer avec le module.

### Compilation

```bash
git clone [https://github.com/GAULAvionique/Pneumatix.git](https://github.com/GAULAvionique/Pneumatix.git)
