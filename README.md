# SNCF TER & Intercités — Tableaux de bord mensuels (Power BI) 🚄📊

Projet Power BI analysant la performance mensuelle des trains **TER** et **Intercités** à partir des **données ouvertes** de la SNCF. Suivi de la **ponctualité**, des **retards** et des **annulations**, comparaisons par **région** et **liaison Départ → Arrivée**, et **carte des gares**.  
Projet **pédagogique** : modélisation soignée, mesures **DAX**, design clair et **storytelling**.

> 📄 Le dépôt inclut un rapport **LaTeX** récapitulant la démarche et les visuels principaux.

---

## ✨ Points clés
- **Deux dashboards** : TER et Intercités  
- **KPI** : ponctualité, retards, annulations, **programmés vs. circulés**  
- **Comparaisons** : par **région** (TER) et **corridors** (Intercités)  
- **Cartographie** : carte des gares (jeu de données **Liste des gares**)  
- **Storytelling** : mesures DAX générant un résumé automatique  
- **Focus apprentissage** : modèle lisible, DAX documenté, étapes reproductibles

---

## 🗂 Jeux de données (Open Data SNCF)
- **TER — régularité mensuelle**  
  `regularite-mensuelle-ter`  
  https://ressources.data.sncf.com/explore/dataset/regularite-mensuelle-ter/information/
- **Intercités — régularité mensuelle**  
  `regularite-mensuelle-intercites`  
  https://ressources.data.sncf.com/explore/dataset/regularite-mensuelle-intercites/information/
- **Référentiel des gares (carte)**  
  `liste-des-gares`  
  https://data.sncf.com/explore/dataset/liste-des-gares/information/

> ℹ️ Données publiques réutilisées dans un **cadre éducatif**. Aucune finalité commerciale.

---

## 📐 Métriques (aperçu)
- **Programmés vs. Circulés** : planifié vs. réalisé  
- **Taux d’annulation** = annulés / programmés  
- **Taux de retard** = retardés / circulés  
- **Ponctualité / Régularité** = à l’heure / circulés  
  - **Intercités (régularité composite, terminus)** : ≥ 5 min (< 1h30), ≥ 10 min (1h30–3h), ≥ 15 min (> 3h)

> ⏱️ Les annulations annoncées **avant 16h la veille** sont exclues des stats de régularité ; après, elles sont comptabilisées (totales/partielles).

---

## 🧠 Modèle & fonctionnalités
- **Table de dates** : Année, Mois, Trimestre, Mois–Année  
- **Colonnes calculées** : harmonisation régions (TER), champs itinéraires (Intercités), dérivés temporels  
- **Mesures DAX** : KPI (taux, totaux), **Résumé/Storytelling**  
- **Visuels** : KPI cards, lignes temporelles, colonnes groupées (Programmés vs. Circulés), anneaux (répartition), **cartes** (régions, départ/arrivée, points de gares)

---

## 📸 Captures d’écran
> Remplacez les chemins si nécessaire (espaces encodés en `%20`).
- **Dashboard TER** :  
  <img width="2001" height="1126" alt="1e Tableau - 2" src="https://github.com/user-attachments/assets/fbab6b47-fd80-4865-b2f3-37ca68c07a3f" />
  <img width="580" height="583" alt="ss-3" src="https://github.com/user-attachments/assets/bb6598f2-b5a6-499d-8d44-1068a5a8758c" />

- **Dashboard Intercités** :  
  <img width="2053" height="1153" alt="2e Tableau - 2" src="https://github.com/user-attachments/assets/8e370be0-47cd-4603-8e25-30550f34c49a" />
  <img width="2005" height="1131" alt="2e Tableau - 1" src="https://github.com/user-attachments/assets/e913b638-b62c-44f2-98a0-65d7564adef4" />

- **Carte des gares** :  
  <img width="2050" height="1150" alt="3e Tableau" src="https://github.com/user-attachments/assets/478ed77f-2db0-4c08-81b5-5fc66f7467be" />


---

## 🚀 Prise en main
1. **Installer** Power BI Desktop  
2. **Cloner** le dépôt  
3. **Ouvrir** les fichiers `.pbix` (TER / Intercités)  
4. **Vérifier les sources** :
   - Connexions Open Data → rafraîchir (Paramètres des sources)  
   - Extracts locaux → mettre à jour les chemins dans **Power Query**
5. **Rafraîchir** le modèle et **explorer**

---


---

## 🗺️ Feuille de route (idées)
- Enrichissement par **météo**, **travaux**, **mouvements sociaux**  
- **Seuils d’alerte dynamiques** par région/corridor  
- Storytelling plus riche (textes dynamiques, tooltips avancés)  
- Comparaisons **MoM/YoY** et saisonnalité  
- Publication **Power BI Service** (paramètres, rafraîchissement planifié)

---

## ⚠️ Hypothèses & limites
- Régularité **mesurée au terminus** (pas d’intermédiaires)  
- Couverture Intercités selon **sélection AQST** (pas exhaustive)  
- Annulations **avant 16h D-1** exclues ; **après 16h**, comptabilisées  
- Projet **éducatif** : pas de garantie opérationnelle

---

## 🔧 Stack
**Power BI Desktop**, **Power Query**, **DAX**, **LaTeX**

---

## 📄 Licence & attributions
- Code/doc : licence **MIT** (voir `LICENSE`)  
- Données © **SNCF Open Data** — conditions d’utilisation propres aux jeux de données  
- Logos : usage **identificatif** uniquement (droits réservés)

---

## 🙋 Contact
**Auteur** : Harishankar Murugan — Étudiant en Data Analytics (2024–2026)  
**Lieu** : Antibes, Côte d’Azur  
**Contribuer** : issues/PR bienvenus ! Si ce projet vous plaît, ⭐ le dépôt 😊

