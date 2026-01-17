# TAAMS
Résumé global du contrat TAAMS Ton contrat n’est pas un simple ERC‑20. C’est un système complet qui combine :

TAAMS PROTOCOL - WHITEPAPER V1.0
L'Écosystème Autonome de Déflation et de Gouvernance

Version
Licence

📑 Table des Matières
Abstract
Introduction
Architecture Technique
Le Token TAAMS
La Phase d'Ignition (Airdrop)
Mécanisme de Burn & BL2P
Staking & Rendement
Gouvernance (DAO)
Distribution & Tokenomics
Roadmap
1. Abstract
TAAMS est un protocole financier autonome et déflationnaire déployé sur le réseau Polygon. Contrairement aux protocoles traditionnels, TAAMS ne dépend pas d'une autorité centrale pour sa gouvernance ou son évolution. Le système vit exclusivement grâce à la participation active de sa communauté ("Vitalité du Protocole").

Grâce à un mécanisme de "Burn-to-Governance", la réduction de l'offre (déflation) génère du pouvoir de vote (BL2P), créant ainsi une boucle vertueuse de rareté et de contrôle décentralisé.

2. Introduction
2.1 Le Problème
La DeFi actuelle souffre de deux maux majeurs :

Centralisation du Pouvoir : Les gros détenteurs de jetons (Whales) dictent souvent la direction des protocoles.
Inflation et Sédimentation : L'expansion continue de l'offre dilue la valeur des utilisateurs passifs, qui ne sont pas incités à agir.
2.2 La Solution TAAMS
TAAMS introduit le concept de "Vitalité". Le système ne s'active pleinement que si une masse critique d'utilisateurs (Les Fondateurs) s'engage. Une fois cette étape franchie, le protocole devient Autonome : les décisions sont prises par la DAO, et l'offre est brûlée collectivement pour garantir la pérennité.

3. Architecture Technique
3.1 Infrastructure
Blockchain : Polygon (Layer 2) pour des frais de gaz négligeables et une haute vitesse.
Contrat Principal : TAAMS (ERC-20, Gouvernance, Staking, Airdrop).
Standard : Solidity ^0.8.20 (OpenZeppelin).
3.2 Sécurité
Le contrat intègre plusieurs garde-fous de sécurité industriels :

ReentrancyGuard : Empêche les attaques de réentrance lors des retraits de staking.
Ownable & Pausable : Mécanismes d'arrêt d'urgence en cas de bug critique.
Système de Vote (Commit/Reveal) : Empêche la corruption des votes et le "front-running" par les bots.
Inactivity Burn : Les droits de vote inutilisés sont détruits, encourageant la gouvernance active.
4. Le Token TAAMS
TAAMS est le jeton natif de l'écosystème. Il agit à la fois comme :

Moyen d'échange : Sur les DEX (Unicwap, QuickSwap).
Carburant pour le Protocole : Utilisé pour le Staking et le Burn.
Réserve de Valeur : Unité de compte pour les récompenses de gouvernance (BL2P).
Spécifications :

Nom : TAAMS
Symbole : TAAMS
Décimales : 18
Offre Totale : 10,000,000,000 TAAMS (10 Milliards)
5. La Phase d'Ignition (Airdrop)
Avant que la gouvernance ne soit transférée à la communauté, le protocole doit prouver sa vitalité.

5.1 Le Concept des Fondateurs
L'inscription est ouverte aux 1000 premiers participants (Founders). Ce groupe d'initiés est crucial car ils sont les premiers à bénéficier de la redistribution massique de l'offre (le Burn).

5.2 L'Allumage (Trigger)
Une fois que 1000 utilisateurs se sont inscrits et que l'offre en circulation atteint le seuil d'activation (1 Milliard de TAAMS), l'Ignition Airdrop est déclenchée automatiquement.

Pool Airdrop : 500,000,000 TAAMS (5% de l'offre totale).
Distribution :
Rang 1-100 : 150% de la part de base.
Rang 101-200 : 125% de la part de base.
Rang 201-1000 : 100% de la part de base.
Une fois l'Ignition terminée, la propriété du contrat est transférée à la DAO, rendant le système 100% Autonome.

6. Mécanisme de Burn & BL2P
C'est le cœur économique du protocole. C'est ici que l'utilisateur transforme son richesse (TAAMS) en pouvoir (BL2P).

6.1 Le BL2P (Gouvernance Power)
Le BL2P n'est pas un simple jeton standard. C'est un jeton lié à l'âme (Soulbound) avec des propriétés uniques :

Non Transférable : Vous ne pouvez pas vendre vos BL2P. Vous devez les gagner en participant (Burn).
Maturité : Les BL2P gagnés doivent "murir" pendant une période avant d'être pleinement actifs pour le staking ou la délégation.
Décroissance Inactivité : Si vous ne votez pas, vos BL2P sont brûlés progressivement. Cela oblige les détenteurs de pouvoir à participer activement à la DAO.
6.2 Le Cycle de Burn
Le protocole vise à brûler 1 Milliard de TAAMS.

Mécanisme : L'utilisateur envoie des TAAMS au contrat pour destruction.
Bonus de Burn (5%) : Si l'utilisateur possède déjà des BL2P, il reçoit un bonus de 5% de BL2P supplémentaire pour le montant brûlé.
Pool de Récompense : 1 Milliard de BL2P sont distribués proportionnellement à tous les brûleurs, une fois l'objectif atteint.
7. Staking & Rendement
Le staking permet aux utilisateurs de bloquer leurs TAAMS pour générer des rendements, tout en gardant un contrôle sur le protocole.

7.1 Règles du Staking
Minimum : 1,000 TAAMS.
Durée de verrouillage : Flexible (retrait possible à tout moment, mais les intérêts sont calculés par blocs/périodes).
Taux de Rendement (APY) : 5% par défaut (Modifiable par DAO).
Calcul : Rendement = (Montant Staké x Taux x Temps).
7.2 Le "Boost" BL2P
C'est une innovation unique. Un utilisateur peut sacrifier son pouvoir de vote (BL2P) pour augmenter ses gains de staking.

Mécanisme : Brûler des BL2P sur un stake actif.
Limite : Le boost ne peut pas dépasser 10% du montant staké.
Arbitrage : L'utilisateur doit choisir entre Gouvernance (Pouvoir de Vote) ou Finance (Plus de Rendement).
8. Gouvernance (DAO)
Une fois l'Ignition terminée, le contrat devient propriété de la communauté.

8.1 Système de Vote à 2 Étapes
Pour éviter que les gros détenteurs ne puissent pas influencer le vote par leur simple présence, TAAMS utilise le système Commit / Reveal.

Commit : L'utilisateur hash son choix (Pour/Contre) + un secret et l'envoie sur la chaîne. Personne ne sait comment il a voté.
Reveal : À la fin de la période de vote, l'utilisateur révèle son secret et son choix.
Validation : Le contrat vérifie que le hash correspond.
8.2 Propositions
Les gouvernés peuvent proposer des changements via différents types de propositions :

Burn Amount : Modifier le montant cible de burn.
Reward Rate : Changer l'APY du staking.
Unlock Reserve : Débloquer la trésorerie.
Quorum & Threshold : Changer les règles de vote.
Advertisement : Poster des annonces officielles sur la chaîne.
8.3 Délégation
Si un utilisateur ne souhaite pas voter, il peut déléguer ses BL2P à un tiers expert. La délégation est révocable à tout moment.

9. Distribution & Tokenomics
L'offre totale de 10 Milliards de TAAMS est répartie comme suit :

Catégorie
Allocation
Montant
Conditions
Locked Reserve	70%	7,000,000,000	Débloquée progressivement par la DAO.
Ignition Airdrop	5%	500,000,000	Distribué aux 1000 fondateurs.
Deployer / Recipient	20%	2,000,000,000	Initial liquidity & Développement.
Burn Pool (Target)	10%	1,000,000,000	Brûlé par les utilisateurs pour mint du BL2P.
Staking Rewards	Illimité	Variable	Mintés dynamiquement sur le rendement.

Note Importante : Le contrat ne possède pas de "Minting Authority" infinie. L'inflation ne se produit que via le Staking, qui est contrôlé par la communauté.

10. Roadmap
Phase 1 : La Création (Q1 2025)
Déploiement sur Polygon Mainnet.
Lancement de la DApp Web3.
Phase d'inscription aux 1000 fondateurs.
Phase 2 : L'Ignition (Q2 2025)
Distribution des 500M TAAMS d'Airdrop.
Transfert de la gouvernance à la DAO.
Activation du mécanisme de Burn.
Phase 3 : La DAO Vivante (Q3 2025)
Premières propositions de gouvernance.
Lancement du staking décentralisé.
Lancement du système de "Publicité" sur la blockchain.
Phase 4 : L'Expansion (2026+)
Intégration de nouveaux contrats (Bridges vers autres chaînes).
Partenariats avec des projets DeFi.
Autonomie totale via la gouvernance BL2P.
11. Avertissements & Disclaimer
Ce Whitepaper est fourni à titre informatif uniquement. Il ne constitue pas un conseil en investissement.

Risque de Smart Contract : Malgré les audits, les contrats intelligents peuvent comporter des vulnérabilités inconnues.
Volatilité : La valeur des jetons BL2P et TAAMS peut fluctuer fortement.
Perte de Clés : Si vous perdez votre phrase secrète de vote (Reveal), vous ne pourrez pas voter. Il n'y a aucune récupération possible.
Construit avec autonomie par la communauté TAAMS.
Version : 1.0.0
Réseau : Polygon Mainnet (137)
