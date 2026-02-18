# 🚀 Atelier GitHub Actions

Automatisez vos tests, vérifications et déploiements directement depuis vos dépôts GitHub avec **GitHub Actions** !

---

## 📚 Présentation

Retrouvez les supports de l’atelier ici :  
👉 [Google Slides – Atelier GitHub Actions](https://docs.google.com/presentation/d/1RUmTjuboIsXfWb5O97Qr67iuFz6H6s92-2u6g8hdrl8/edit?slide=id.g3c8ccaa0cba_0_18#slide=id.g3c8ccaa0cba_0_18)

---

## 🛠 Objectifs de l'atelier

- Comprendre à quoi sert **GitHub Actions**
- Apprendre à écrire un fichier `.yml` pour une ci
- Automatiser les tests et la vérification de la **Norminette**
- Exécuter automatiquement les workflows à chaque `push`

---

## 🧪 Exercice

> 🎯 Prenez votre projet actuel ou votre libft/n'importe quel autre projet.

1. Ajoutez la **Norminette** pour vérifier le style de votre code
2. Ajoutez une suite de **tests automatisés**
3. Créez un fichier dans `.github/workflows/` pour :
   - Lancer la Norminette
   - Lancer les tests
4. Vérifiez que GitHub Actions s'exécute automatiquement à chaque `push`

---

## 🧱 Exemple de fichier YAML

```yaml
name: Norminette & Tests

on: [push]

jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name:
