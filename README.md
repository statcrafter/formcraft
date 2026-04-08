# 🎨 FormCraft

[![Laravel](https://img.shields.io/badge/Laravel-12.x-FF2D20?style=for-the-badge&logo=laravel)](https://laravel.com)
[![Vue.js](https://img.shields.io/badge/Vue-3.x-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white)](https://vuejs.org)
[![Inertia.js](https://img.shields.io/badge/Inertia.js-2.x-2B1F6F?style=for-the-badge)](https://inertiajs.com)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.x-06B6D4?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com)
[![Vite](https://img.shields.io/badge/Vite-7.x-646CFF?style=for-the-badge&logo=vite)](https://vitejs.dev)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

> Une application moderne de création de formulaires construite avec Laravel, Vue.js et Inertia.js

## 📋 Description

FormCraft est une application web complète permettant de créer, gérer et partager des formulaires personnalisés. Basée sur la stack technique moderne Laravel + Vue.js + Inertia.js, elle offre une expérience utilisateur fluide et réactive.

## ✨ Fonctionnalités

- **Création intuitive de formulaires** avec glisser-déposer
- **Éditeur WYSIWYG** pour personnaliser l'apparence des champs
- **Gestion des réponses** avec visualisation des données collectées
- **Export des données** au format Excel/CSV
- **Authentification sécurisée** avec Laravel Fortify
- **Interface responsive** adaptée à tous les appareils
- **Thème personnalisable** avec Tailwind CSS
- **Validation côté client et serveur**
- **Notifications en temps réel**
- **Support multi-langues** (i18n)

## 🛠️ Technologies utilisées

### Backend

- **Laravel 12.x** - Framework PHP moderne
- **PHP 8.2+** - Version requise
- **Laravel Fortify** - Authentification
- **Laravel Wayfinder** - Génération de menus
- **Maatwebsite/Excel** - Export de données
- **Inertia.js** - Pont entre Laravel et Vue.js

### Frontend

- **Vue.js 3.x** - Framework JavaScript réactif
- **Vue 3 Composition API** - Organisation du code
- **Pinia** - Gestion d'état
- **Tailwind CSS 4.x** - Framework CSS utility-first
- **Vite** - Bundler rapide
- **Reka UI** - Bibliothèque de composants
- **Vue Draggable** - Fonctionnalité de glisser-déposer
- **Class Variance Authority & clsx** - Gestion conditionnelle des classes
- **VueUse** - Collection d'utilitaires Vue.js
- **Lucide Vue** - Icônes vectorielles

### Outils de développement

- **ESLint** - Linting JavaScript/TypeScript
- **Prettier** - Formatage de code
- **TypeScript** - Typage statique
- **Vitest** - Tests unitaires
- **Pest** - Tests PHP
- **Laravel Sail** - Environnement Docker

## 🚀 Installation

### Prérequis

- PHP >= 8.2
- Composer
- Node.js >= 18
- npm ou yarn
- Base de données (MySQL, PostgreSQL, SQLite)

### Étapes d'installation

1. **Cloner le dépôt**

```bash
git clone https://github.com/votre-utilisateur/formcraft.git
cd formcraft
```

2. **Installer les dépendances PHP**

```bash
composer install
```

3. **Configurer l'environnement**

```bash
cp .env.example .env
php artisan key:generate
```

4. **Configurer la base de données**
   Modifiez le fichier `.env` avec vos paramètres de base de données :

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=formcraft
DB_USERNAME=votre_utilisateur
DB_PASSWORD=votre_mot_de_passe
```

5. **Exécuter les migrations**

```bash
php artisan migrate
```

6. **Installer les dépendances JavaScript**

```bash
npm install
```

7. **Compiler les assets**

```bash
npm run build
# ou pour le développement
npm run dev
```

8. **Lancer l'application**

```bash
php artisan serve
```

L'application sera accessible à l'adresse : [http://127.0.0.1:8000](http://127.0.0.1:8000)

## 🔧 Commandes disponibles

### Backend

```bash
php artisan serve              # Lancer le serveur de développement
php artisan test              # Exécuter les tests PHP
php artisan queue:listen      # Écouter les jobs de la file d'attente
php artisan migrate           # Exécuter les migrations
php artisan migrate:fresh     # Réinitialiser et re-exécuter les migrations
```

### Frontend

```bash
npm run dev                   # Démarrer Vite en mode développement
npm run build                 # Construire pour la production
npm run build:ssr             # Construire pour le rendu côté serveur
npm run format                # Formater le code avec Prettier
npm run format:check          # Vérifier le formatage
npm run lint                  # Linter et corriger le code
```

### Scripts personnalisés (dans composer.json)

```bash
composer run setup            # Installation complète du projet
composer run dev              # Lancer serveur, queue et Vite en concurrence
composer run dev:ssr          # Même chose avec SSR
composer run test             # Exécuter les tests
```

## 🧪 Tests

### Tests PHP

```bash
php artisan test
# ou
composer run test
```

### Tests JavaScript

```bash
npm run test                  # À implémenter avec Vitest/Jest
```

## 📁 Structure du projet

```
formcraft/
├── app/                        # Code Laravel principal
│   ├── Http/
│   │   ├── Controllers/       # Contrôleurs
│   │   └── Middleware/        # Middleware
│   ├── Models/                # Modèles Eloquent
│   └── Providers/             # Fournisseurs de services
├── bootstrap/                 # Fichiers de démarrage Laravel
├── config/                    # Fichiers de configuration
├── database/                  # Migrations et seeders
│   ├── factories/             # Usines de modèles
│   ├── migrations/            # Schémas de base de données
│   └── seeders/               # Données de peuplement
├── public/                    # Ressources statiques
├── resources/                 # Ressources frontend
│   ├── js/                    # Code JavaScript/Vue
│   │   ├── components/        # Composants Vue réutilisables
│   │   ├── pages/             # Pages de l'application
│   │   ├── composables/       # Fonctions réutilisables
│   │   ├── layouts/           # Layouts de page
│   │   └── plugins/           # Plugins Vue
│   └── css/                   # Styles personnalisés
├── routes/                    # Définition des routes
│   └── web.php                # Routes web
├── specs/                     # Spécifications/PHPUnit
├── tests/                     # Tests automatisés
│   ├── Feature/               # Tests fonctionnels
│   └── Unit/                  # Tests unitaires
├── storage/                   # Fichiers stockés par l'application
├── vendor/                    # Dépendances Composer
└── ...                        # Fichiers de configuration
```

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer à FormCraft :

1. Fork le dépôt
2. Créez votre branche de fonctionnalité (`git checkout -b feature/amazing-feature`)
3. Committez vos changements (`git commit -m 'Add some amazing feature'`)
4. Push vers la branche (`git push origin feature/amazing-feature`)
5. Ouvrez une Pull Request

### Guidelines de contribution

- Suivez le style de code existant
- Écrivez des tests pour vos nouvelles fonctionnalités
- Mettez à jour la documentation si nécessaire
- Gardez les pull requests focussées sur une seule fonctionnalité

## 🐛 Rapports de bugs

Si vous trouvez un bug, merci de :

1. Vérifier s'il n'a pas déjà été rapporté
2. Créer une issue détaillée incluant :
    - Une description claire du problème
    - Les étapes pour le reproduire
    - Les captures d'écran si applicable
    - Votre environnement (version PHP, Node.js, navigateur, etc.)

## 📄 Licence

Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 🙏 Remerciements

- [Laravel](https://laravel.com) pour le framework PHP exceptionnel
- [Vue.js](https://vuejs.org) pour le framework JavaScript réactif
- [Inertia.js](https://inertiajs.com) pour le pont moderne entre backend et frontend
- [Tailwind CSS](https://tailwindcss.com) pour le framework CSS utility-first
- Tous les contributeurs open source qui rendent ce projet possible

---

✨ Construit avec ❤️ par l'équipe FormCraft ✨
