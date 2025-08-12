# AuditMapper v2 - Security Assessment Suite

Une suite d'outils modernes et professionnels pour les audits de sécurité et tests d'intrusion, refactorisée avec React 18, TypeScript et une architecture modulaire.

## 🚀 Technologies Utilisées

### Frontend
- **React 18** - Framework principal
- **TypeScript** - Typage statique
- **Vite** - Build tool ultra-rapide
- **Tailwind CSS** - Framework CSS utilitaire
- **Framer Motion** - Animations fluides
- **Zustand** - State management léger
- **React Query** - Gestion des données serveur
- **Lucide React** - Icônes modernes

### Architecture
- **Architecture modulaire** - Composants réutilisables
- **Store pattern** - Gestion d'état centralisée
- **Type safety** - TypeScript strict
- **Performance optimisée** - Lazy loading, code splitting
- **Accessibilité** - WCAG conformes

## 🎨 Design System

### Thème Sombre Moderne
- **Couleurs cyberpunk** - Vert néon (#00ff88), magenta (#ff0080), cyan (#00ffff)
- **Interface terminal** - Style tech/hacker
- **Animations fluides** - Transitions et micro-interactions
- **Responsive design** - Mobile-first approach

### Composants UI
- **Button** - Variantes cyber, terminal, gradient
- **Card** - Effets glass, neon, cyber
- **Input** - Styles dark, terminal, cyber
- **Modal** - Overlays modernes
- **Toast** - Notifications élégantes

## 📁 Structure du Projet

```
auditmapper-v2/
├── src/
│   ├── components/
│   │   ├── ui/                    # Composants UI de base
│   │   │   ├── button.tsx
│   │   │   ├── card.tsx
│   │   │   ├── input.tsx
│   │   │   └── ...
│   │   ├── layout/                # Layout et navigation
│   │   │   ├── Header.tsx
│   │   │   ├── Sidebar.tsx
│   │   │   └── ...
│   │   ├── features/              # Modules métier
│   │   │   ├── host-manager/      # Gestionnaire de hosts
│   │   │   │   ├── HostManager.tsx
│   │   │   │   ├── HostCard.tsx
│   │   │   │   ├── HostForm.tsx
│   │   │   │   └── ...
│   │   │   ├── pivot-master/      # Générateur de pivoting
│   │   │   ├── grep-master/       # Parser intelligent
│   │   │   ├── privesc-helper/    # Guide d'escalade
│   │   │   └── config-generator/  # Générateur de config
│   │   └── common/                # Composants partagés
│   ├── hooks/                     # Custom hooks
│   │   ├── useLocalStorage.ts
│   │   ├── useDebounce.ts
│   │   └── ...
│   ├── stores/                    # Zustand stores
│   │   ├── hostStore.ts
│   │   ├── uiStore.ts
│   │   └── ...
│   ├── services/                  # Services API
│   │   ├── database.ts
│   │   ├── export.ts
│   │   └── ...
│   ├── utils/                     # Utilitaires
│   │   ├── index.ts
│   │   ├── cn.ts
│   │   └── ...
│   ├── types/                     # Types TypeScript
│   │   └── index.ts
│   ├── styles/                    # Styles globaux
│   │   └── globals.css
│   ├── App.tsx                    # Composant principal
│   └── main.tsx                   # Point d'entrée
├── public/                        # Assets statiques
├── docs/                          # Documentation
└── ...
```

## 🛠️ Installation et Démarrage

### Prérequis
- **Node.js** 18+ 
- **npm** ou **yarn**

### Installation

```bash
# Cloner le projet
git clone <repository-url>
cd auditmapper-v2

# Installer les dépendances
npm install

# Lancer en mode développement
npm run dev
```

### Scripts Disponibles

```bash
# Développement
npm run dev              # Lance le serveur de développement
npm run build            # Build de production
npm run preview          # Prévisualise le build

# Qualité de code
npm run lint             # ESLint
npm run lint:fix         # ESLint avec auto-fix
npm run format           # Prettier
npm run type-check       # Vérification TypeScript

# Tests
npm run test             # Tests unitaires
npm run test:ui          # Interface de tests

# Documentation
npm run storybook        # Lance Storybook
npm run build-storybook  # Build Storybook
```

## 🎯 Fonctionnalités

### Host Manager (Implémenté)
- ✅ **Gestion des hosts** - Ajout, modification, suppression
- ✅ **Interface moderne** - Design sombre et cyberpunk
- ✅ **Recherche et filtres** - Recherche textuelle et filtres avancés
- ✅ **Vue grille/liste** - Deux modes d'affichage
- ✅ **Sélection multiple** - Actions en lot
- ✅ **Export/Import** - Formats JSON, CSV, XML
- ✅ **Credentials** - Gestion des usernames, passwords, hashes
- ✅ **Vulnérabilités** - Suivi des vulnérabilités par host
- ✅ **Services** - Gestion des services découverts
- ✅ **Screenshots** - Capture d'écrans d'exploitation
- ✅ **Étapes d'exploitation** - Workflow structuré
- ✅ **Statistiques** - Dashboard avec métriques
- ✅ **Persistance locale** - Stockage IndexedDB

### Calendar & Kanban (Implémenté)
- ✅ **Kanban** - Colonnes personnalisables, drag & drop (SortableJS + DnD)
- ✅ **Timers par ticket** - Start/Pause/Reset, cumul du temps
- ✅ **Timer global** - Compte à rebours configurable (presets, pause/reprise)
- ✅ **Pomodoro** - Sessions travail/pause avec progression circulaire
- ✅ **To-Do & Notes** - Listes rapides, notes persistées
- ✅ **Export timesheet** - CSV avec temps passés par ticket

### Config Generator (Implémenté)
- ✅ **Génération de configs** - Fichiers /etc/hosts, proxychains, Kerberos, etc.
- ✅ **Templates** - Paramétrage rapide, presets

### Template Generator (Implémenté)
- ✅ **Génération Markdown** - À partir de paramètres + output Nmap
- ✅ **Aperçu Markdown** - Rendu riche (GFM) avec mise en forme du code
- ✅ **Téléchargement** - Export direct en `.md` et copie presse-papiers

### Grep Master (Implémenté partiel)
- ✅ **Parsing ciblé** - Extraction d'infos utiles depuis des outputs

### Pivot Master (Implémenté partiel)
- ✅ **Aide au pivoting** - Génération de commandes, visualisation réseau

### ADMR – Active Directory Mindmap Renderer (Implémenté)
- ✅ **Rendu Obsidian Canvas** - Chargement des `.canvas` en UI interactive
- ✅ **Navigation** - Liens entre canvases, zoom/pan
- ✅ **Markdown** - Rendu des blocs textes
- ✅ **Crédits et sources**: merci à Amine et Evariste pour la carte Obsidian, inspirée par `OCD mindmaps` et `The Hacker Recipes`. Source originale: [Imp0sters/ADMR](https://github.com/Imp0sters/ADMR)

### Fonctionnalités à Implémenter
- 🔄 **Pivot Master** - Générateur de commandes de pivoting
- 🔄 **Grep Master** - Parser intelligent pour outputs
- 🔄 **Privesc Helper** - Guide d'escalade de privilèges
- 🔄 **Config Generator** - Générateur de fichiers de config
- 🔄 **Network Visualization** - Graphique réseau interactif
- 🔄 **Report Generator** - Générateur de rapports
- 🔄 **Collaboration** - Mode multi-utilisateurs
- 🔄 **API Backend** - Synchronisation cloud

## 🎨 Composants Principaux

### HostManager
Interface principale pour la gestion des hosts avec :
- Dashboard avec statistiques
- Recherche et filtres avancés
- Vue grille/liste
- Actions en lot
- Export/Import de données

### HostCard
Carte représentant un host avec :
- Informations principales (IP, hostname, OS)
- Statut et niveau de compromission
- Compteurs de credentials
- Actions rapides (copier, modifier, supprimer)
- Mode expansible pour plus de détails

### Store (Zustand)
Gestion d'état centralisée avec :
- CRUD complet pour les hosts
- Filtres et recherche
- Sélection multiple
- Agrégation de credentials
- Statistiques en temps réel

## 🔧 Configuration

### Variables d'Environnement
```bash
# .env.local
VITE_API_URL=http://localhost:3001
VITE_APP_NAME=AuditMapper v2
VITE_APP_VERSION=2.0.0
```

### Configuration Tailwind
```javascript
// tailwind.config.js
module.exports = {
  darkMode: 'class',
  theme: {
    extend: {
      colors: {
        cyber: {
          primary: '#00ff88',
          secondary: '#ff0080',
          accent: '#00ffff',
          // ...
        },
        dark: {
          50: '#f8fafc',
          // ...
          950: '#020617',
        },
      },
    },
  },
}
```

## 🚀 Déploiement

### Build de Production
```bash
npm run build
```

### Déploiement Vercel
```bash
npm install -g vercel
vercel --prod
```

### Déploiement Netlify
```bash
npm run build
# Upload du dossier dist/
```

## 🧪 Tests

### Tests Unitaires
```bash
npm run test
```

### Tests E2E
```bash
npm run test:e2e
```

### Couverture de Code
```bash
npm run test:coverage
```

## 📚 Documentation

### Storybook
```bash
npm run storybook
```
Accès : http://localhost:6006

### Documentation API
```bash
npm run docs:api
```

## 🤝 Contribution

### Guidelines
1. **Fork** le projet
2. **Créer** une branche feature (`git checkout -b feature/AmazingFeature`)
3. **Commit** les changements (`git commit -m 'Add some AmazingFeature'`)
4. **Push** vers la branche (`git push origin feature/AmazingFeature`)
5. **Ouvrir** une Pull Request

### Standards de Code
- **TypeScript strict** - Tous les fichiers en TS
- **ESLint + Prettier** - Formatage automatique
- **Conventional Commits** - Messages de commit standardisés
- **Tests obligatoires** - Couverture minimale 80%

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## 🙏 Remerciements

- **Elliot Belt** - Développeur original d'AuditMapper
- **Phreaks 2600** - Communauté de sécurité
- **React Team** - Framework exceptionnel
- **Tailwind CSS** - Framework CSS utilitaire
- **Zustand** - State management simple et efficace
 - **Amine & Evariste** — Merci pour le projet ADMR (cartes Obsidian AD). Repo: [Imp0sters/ADMR](https://github.com/Imp0sters/ADMR)

## 📞 Support

- **Issues** : [GitHub Issues](https://github.com/your-repo/issues)
- **Discussions** : [GitHub Discussions](https://github.com/your-repo/discussions)
- **Email** : support@auditmapper.com

---

**AuditMapper v2** - Security Assessment Suite  
*Made with ❤️ by the cybersecurity community*
