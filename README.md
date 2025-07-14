# 🌟 Planificateur de spectacles pour Avignon Off

Cette application Streamlit vous permet de gérer votre planning de spectacles Avignon Off, sous la forme d'un fichier Excel personnalisé contenant les informations essentielles de votre programme.

---

## 🚀 Fonctionnalités principales

* 📂 **Charger un fichier Excel** contenant les spectacles à planifier
* ✅ **Vérifier la cohérence des données** :

  * Doublons (même date, heure, durée, spectacle)
  * Chevauchements entre activités (spectacles et pauses)
  * Formats invalides (heure, durée, date)
  * Activités prévues un jour de relâche
  * Durées nulles ou incohérentes
* 📅 **Afficher les activités planifiées** (i.e. celles dont la colonne `Date` est renseignée)
* ❌ **Supprimer une activité planifiée** (si non réservée)
* ⏰ **Sélectionner un créneau libre** avant ou après une activité planifiée
* 🔄 **Assigner une activité non planifiée** dans un créneau disponible
* 🔖 **Sauvegarder le fichier Excel modifié**
* ☕ **Prendre en compte les pauses** : déjeuner, dîner, café (via la colonne `Autres`)

---

## 📜 Format du fichier Excel attendu

Le fichier doit comporter les colonnes suivantes (sans accents et avec majuscules) :

| Colonne     | Type attendu           | Description                                    |
| ----------- | ---------------------- | ---------------------------------------------- |
| `Date`      | Entier (ex : 20250722) | Jour de l'activité                             |
| `Heure`     | Texte `Hhmm`           | Heure de début (`10h00`, `9h15`, etc.)         |
| `Durée`     | Texte `Hhmm`           | Durée (`1h30`, `0h45`, etc.)                   |
| `Activité`  | Texte                  | Nom de l'activité                              |
| `Lieu`      | Texte                  | Lieu de l'activité                             |
| `Relâche`   | Liste d'entiers        | Date des jours de relâche                      |
| `Réservé`   | `Oui` / `Non`          | Si la réservation est faite                    |
| `Priorité`  | Entier ou vide         | Priorité d'affichage ou de planification       |

---

## 📁 Modèle Excel

Un modèle de fichier est disponible ici :
📄 [Télécharger le modèle Excel](https://github.com/jnicoloso-91/PlanifAvignonOff_01/raw/main/Modèle%20Excel.xlsx)

---

## 🚧 Exécution locale

```bash
git clone https://github.com/jnicoloso-91/PlanifAvignonOff_01.git
cd PlanifAvignonOff_01
pip install -r requirements.txt
streamlit run app.py
```

---

## 🛠️ Technologies

* Python 3.9+
* Streamlit
* Pandas
* openpyxl

---

## 🌐 Application hébergée

L'application est accessible en ligne via Streamlit Cloud :
[Accéder à l'application 📅](https://planifavignon-05-hymtc4ahn5ap3e7pfetzvm.streamlit.app/)

---

## 🙋‍ Auteur

Application conçue et développée avec chatGPT pour un usage personnel.
Suggestions bienvenues !

---

## 📄 Licence

Ce projet est distribué sous licence MIT.
