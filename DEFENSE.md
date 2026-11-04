# 🛡️ Solution de défense — Gobelin Hurlant

Volet *défense* de l'exercice : protéger la cible contre l'attaque d'hameçonnage
construite sur le portail fictif Hyperbole Interactive.

## 1. Les indices (ce qui trahit l'attaque)

1. **Le domaine de l'expéditeur** : `hyperbole-lnteractive` (un « l »), `gobel1n` (un « 1 »). Toujours lire l'adresse complète, lettre à lettre — pas le nom affiché.
2. **Le lien au survol ≠ le texte affiché.** Survoler (appui long sur mobile) révèle la vraie destination avant de cliquer.
3. **Une demande qui contourne la procédure** habituelle (un « portail » qui n'existait pas).
4. **La saisie d'identifiants depuis un lien** reçu — jamais légitime.
5. **Urgence + secret** : « avant 18 h » et « garde ça entre nous » visent à empêcher toute vérification.
6. **Un canal inhabituel** : SMS d'un numéro inconnu, un interlocuteur jamais entendu.

## 2. Le protocole (même sans indice repéré)

Conçu pour que l'attaque échoue **même si l'employé n'a rien remarqué** — il repose
sur une règle mécanique, pas sur la vigilance.

1. **Jamais d'identifiants depuis un lien.** Les accès VPN / Forge s'ouvrent uniquement depuis les favoris ou le client installé.
2. **Toute demande touchant un accès, un build ou un versement se vérifie sur le canal connu** : rappeler au vrai numéro (pas celui du message) avant toute action.
3. **En cas de doute ou de pression : signaler et temporiser.** Aucune échéance ne justifie de sauter ces étapes — un vrai jalon survit à 10 minutes.

**Côté studio :** 2FA sur le VPN et la Forge · fin du mot de passe partagé (un compte par personne) · SPF/DKIM/DMARC + bannière « expéditeur externe » · une adresse de signalement connue de tous.

## 3. La métrique

| Indicateur | Sens |
|---|---|
| Sent / Opened | Portée (peu actionnable) |
| **Clicked** | Premier faux pas — à faire **baisser** |
| **Entered** | L'échec réel — à faire **baisser** en priorité |
| **Reported** ⭐ | **La métrique à faire MONTER** — le réflexe qui protège tout le monde |

On cherche surtout à faire **monter le taux de signalement** : un faible taux de clic
ne prouve pas qu'on est protégé, juste que personne n'a mordu *cette fois*. Repère :
les organisations sensibilisées descendent vers **~5 % de clic** (Proofpoint).

## 4. Campagne de sensibilisation

Affiche **« GOBELIN, PAS GOBE-TOUT »** — *« Un lien qui hurle à l'urgence ? Flaire-le
avant de mordre. »* Trois réflexes : lis l'adresse en entier · jamais d'accès via un
lien · doute = rappelle le vrai numéro. Message clé : **dans le doute, on signale**.

## 5. Argumentaire des coûts

**Ce que coûterait l'échec (cas réels) :**
- **Phishing** = 1er vecteur d'intrusion, ~**4,8 M$** par violation en moyenne (IBM, *Cost of a Data Breach 2025*).
- **Fraude au virement (BEC)** : **2,77 Md$** de pertes déclarées en 2024 (FBI IC3).
- **Pathé** : **19,2 M€** détournés par fraude au président (2018).
- Fuites de builds dans le jeu vidéo : **CD Projekt Red** (2021), **Insomniac Games** (2023, rançon de 2 M$ refusée, 1,67 To fuités).

**Ce que coûte notre solution :** ~**600 à 1 200 € / an** — surtout du temps (2FA,
fin du mot de passe partagé, SPF/DKIM/DMARC, sensibilisation). Une prime d'assurance
dérisoire face au sinistre.

---
*Exercice pédagogique EFREI — entreprise et personnes fictives.*
