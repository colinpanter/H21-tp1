# TP1 - Énoncé

## Objectifs

- Collaborer et prendre des décisions en équipe
- Comprendre les commandes et le fonctionnement de base de Git
- Utiliser des outils de planification et de gestion efficacement et de façon organisée
- Comprendre la structure de base du projet
- Comprendre les principes fondamentaux d'une API REST
- Respecter les conditions de succès demandées
- Être capable de mettre en place un nouveau module dans le code existant

## Travail demandé

Pour les **parties 1 à 3**, nous vous demandons de répondre à l'aide d'un **document PDF** (remis sur monPortail) seulement pour les questions identifiées (:page_facing_up:). Pour le code, nous vous demandons de créer un **tag** nommé `remise1` (le nom doit être exact). C'est la version liée à ce tag qui sera corrigée. Si vous omettez d'indiquer le tag, la **note de 0** vous sera attribuée pour la partie 4. Vous devrez également remettre le **contrat d'équipe** sur monPortail, rempli et signé.

### Partie 1 - Ententes d'équipes (20%)

1. **Discuter des outils qui vous seront nécéssaires. Cette discussion permettra de facilement remplir le contrat d'équipe.**
    1. Parlez en équipe des outils de **communication** (vidéo, messagerie, etc.) que vous aimez ou détestez utiliser, et pourquoi.
    2. Parlez en équipe des outils de **gestion** (des tâches, du temps, etc.) que vous aimez ou détestez utiliser, et pourquoi.
    3. Parlez en équipe des outils de **développement** (IDE, formattage, etc.) que vous aimez ou détestez utiliser, et pourquoi.
2. **Remplir le contrat d'équipe**
    1. Indiquez tous les outils que vous avez convenu d'utiliser
    2. Indiquez les autres ententes d'équipes
3. **Créer et remplir un fichier `.gitignore` à la racine de votre projet.**
    1. Ce dernier devrait respecter les *ignorances* standards. Discuttez-en en équipe, argumentez, décidez. :warning: **Attention**: des manipulation git additionnelles pourraient être nécéssaire afin de mettre à jour l'arbre de fichier.
    2. :page_facing_up: En quelques phrases, expliquez d'où vous vous êtes inspirés (Internet, votre compagnie, vous-mêmes) et pourquoi vous avez décidé d'ignorer ces fichiers (vous pouvez être général, pas besoin d'expliquer pour *chaque* fichier).

### Partie 2 - Git (30%)

Cette partie renferme quelques questions quand à l'utilisation de `git`. Veuillez répondre dans le document PDF que vous remettrez sur monPortail.

1. :page_facing_up: Quelle est la différence entre les commandes `rebase` et `merge`?
    1. Expliquez vous en quelques mots.
    2. Remettez un graphique d'un arbre de commits simple à 2 branches, puis les résultats après un merge et après un rebase.
2. :page_facing_up: Dans les cas suivants, quelle(s) méthode(s) devrait-on favoriser?
    1. Je travaille seul sur un projet, et je veux que mon arbre soit le plus propre possible.
    2. J'ai poussé un mot de passe secret dans mes fichiers par accident, et je veux pouvoir l'effacer du serveur.
    3. Je travaille dans une grosse équipe, où chaque tâche n'est attribuée qu'à une seule personne.
    4. Je dois intégrer du code provenant de multiple branches différentes.
3. :page_facing_up: Dans les situations qui suivent, montrez la liste des commandes nécéssaires afin d'atteindre le but. Si le but est impossible à atteindre, expliquez pourquoi et donnez tout de même une piste de solution.
    1. J'ai poussé mon commit trop tôt et il y avait des erreur de compilation. Tout le monde de mon équipe est en train de travailler sur le projet (dans la même branche) et envoient des changements rapidement. Je viens de corriger l'erreur sur mon poste de travail, mais je n'ai pas encore commité ni ajouter mes modifications. **But:** pousser la modification.
    2. J'ai poussé mon commit trop tôt et il y avait des erreur de compilation. Tout le monde de mon équipe est en train de travailler sur le projet (dans la même branche) et envoient des changements rapidement. Je viens de corriger l'erreur sur mon poste de travail, mais je n'ai pas encore commité ni ajouter mes modifications. **But:** pousser la modification, *mais en remplaçant le commit erroné.*
4. Pour cette question, on vous demande de vous référez à [ce repo](). On vous demande d'intégrer les changements de toutes les branches dans la branche principale `main`. Vous devrez tenter de comprendre les changements qui ont été effectués en fonction du contenu présent sur Github. **TODO Quoi remettre ici???**

### Partie 3 - Planification (30%)

Avant d'entamer la programmation, nous vous demandons de lire attentivement les exigences de la partie 4. Nous vous demandons ensuite de planifier vos tâches avec Github Project.

1. :page_facing_up: Créez un *milestone* pour la remise du tp1 et insérez une capture d'écran afin de montrer les information du milestone ainsi que les issues.
2. :page_facing_up: Créez des issues afin de suivre votre progrès et de vous séparer la tâche. :warning: **Attention** Ce n'est pas nécéssairement 1 issue pour 1 feature. Assurez-vous également d'y remplir l'ensemble des parties tel que vu en classe. Insérez une capture d'écran par issue. 
3. Créez des PRs afin de suivre les changements effectués ou en attente. Assurez-vous également d'y remplir l'ensemble des parties tel que vu en classe. Insérez une capture d'écran par PRs **résolue**.
4. :page_facing_up: Créez un Github Project contenant vos issues. Insérez une capture d'écran montrant le tableau résultant. Celle-ci peut être effectuée au début comme à la fin de votre progrès. Nous devons au moins y voir les colonnes ainsi que quelques issues. Une seule capture suffit (pas besoin de *scroller*).

### Partie 4 - Code (20%)

Pour cette partie, vous devrez développer les features demandées. Les formats de requêtes et réponse utilisent la notation typée de Typescript. **On s'attend à une réponse dans le format JSON pour l'ensemble des appels à l'API**.

#### Feature 1

En temps que gestionnaire de projet, je désire que l'on puisse ajouter un item en vente.

**Requête**
```
HTTP POST /inventory
```
```ts
{
  name: string,
  description: string,
  initialPrice: number, // 2 decimals
  startTime: datetime, // ISO-8601 at UTC
  duration: number // milliseconds
}
```

**Réponse**
```
HTTP 201 CREATED
Headers:
  Location: string
```

... où le header `Location` contient l'URL vers le nouvel item publié.


#### Feature 2

En temps que gestionnaire de projet, je désire que l'on puisse visionner les détails d'une offre publiée.

**Requête**
```
HTTP GET /inventory/{id}
```

**Réponse**
```
HTTP 200 OK
```
```ts
{
  items: [
    {
      id: string,
      name: string,
      description: string,
      initialPrice: number, // 2 decimals
      currentPrice: number, // 2 decimals
      startTime: datetime, // ISO-8601 at UTC
      endTime: datetime // ISO-8601 at UTC
    }
  ]
}
```
