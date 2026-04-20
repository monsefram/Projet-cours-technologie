# Recherche – Projet de session
**Type de projet :** Jeu 2D Godot 4.5 — **Blackjack**

## Éléments clés (3)

### 1) Système de cartes & mélange (deck/shuffle)
- **Besoin :** Représenter 52 cartes, mélanger de façon uniforme, distribuer (option shoe plus tard).
- **Sources :**
  - Godot Docs – RandomNumberGenerator : https://docs.godotengine.org/en/stable/classes/class_randomnumbergenerator.html
  - Fisher–Yates shuffle (Wikipedia) : https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle
- **Note rapide :** Modèle `Card{rank,suit,value}`; mélange Fisher–Yates avant chaque manche, comme ca pas de triche.

### 2) Règles Blackjack & croupier
- **Besoin :** Calcul des mains (As=1/11), blackjack naturel, dealer **stand on 17**, paiements **3:2**, push/lose/win.
- **Sources :**
  - Blackjack (Wikipedia) – règles, variantes : https://en.wikipedia.org/wiki/Blackjack
  - Basic strategy (overview) : https://en.wikipedia.org/wiki/Blackjack#Basic_strategy
- **Note rapide :** pas de split ou de double pour l'instant , peut etre plus tard .

### 3) Machine à états & animations de distribution
- **Besoin :** États clairs (**Betting → Dealing → PlayerTurn → DealerTurn → Payout → RoundEnd**), signaux/entrées, animations de cartes.
- **Sources :**
  - Godot Docs – AnimationPlayer : https://docs.godotengine.org/en/stable/classes/class_animationplayer.html
- **Note rapide :**  AnimationPlayer pour deal et feedback visuel.
