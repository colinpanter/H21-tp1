# TP1 - Énoncé

## Objectifs

- Collaborer et prendre des décisions en équipe
- Comprendre les commandes et le fonctionnement de base de Git
- Utiliser des outils de planification et de gestion efficacement et de façon organisée
- Comprendre la structure de base du projet
- Comprendre les principes fondamentaux d'une API REST
- Respecter les conditions de succès demandées
- Être capable de mettre en place un nouveau module dans le code existant

## À remettre

Les questions identifiées avec l'émoticône :scroll: (ainsi que leurs sous-questions) devront être répondues à l'aide du fichier `exercices/tp1.md` déjà présent dans votre repo de projet. Lorsque votre travail sera terminé, nous vous demandons de créer un **tag** nommé `remise1` (**le nom doit être exact**). C'est la version liée à ce tag qui sera corrigée. Si vous omettez d'indiquer le tag, la **note de 0** vous sera attribuée. Vous devrez également remettre le **contrat d'équipe** par courriel au professeur.

## Partie 1 - Conventions d'équipes (20%)

1. **Discuter des outils qui vous seront nécéssaires. Cette discussion permettra de facilement remplir le contrat d'équipe.**
    - Parlez en équipe des outils de **communication** (vidéo, messagerie, etc.) que vous aimez ou détestez utiliser, et pourquoi.
    - Parlez en équipe des outils de **gestion** (des tâches, du temps, etc.) que vous aimez ou détestez utiliser, et pourquoi.
    - Parlez en équipe des outils de **développement** (IDE, formattage, etc.) que vous aimez ou détestez utiliser, et pourquoi.
2. **Remplir le contrat d'équipe**
    - Indiquez tous les outils que vous avez convenu d'utiliser
    - Indiquez les autres ententes d'équipes
    - :email: Signez le contrat et **remettez-le au professeur par courriel** (1 par équipe).
3. **Créer et remplir un fichier `.gitignore` à la racine de votre projet.**
    - Ce dernier doit respecter les *ignorances* standards. Discuttez-en en équipe, argumentez, décidez. :warning: **Attention**: nous vérifierons si les fichiers ignorés sont bien absents de votre arbre de fichier.
    - :scroll: En quelques phrases, expliquez d'où vous vous êtes inspirés (Internet, votre compagnie, vous-mêmes) et pourquoi vous avez décidé d'ignorer ces fichiers (vous pouvez être général, pas besoin d'expliquer pour *chaque* fichier).
4. **Créer 2 templates d'issue (1 pour feature, 1 pour bug)**
    - Discuttez des sections principales et secondaires que devrait contenir une issue, dépendant de sont type. :warning: **Attention**: ne pas copier les exemples du chargé de laboratoire!
    - Les templates **doivent** se retrouver dans le dossier `.github/ISSUE_TEMPLATE/`.
    - **Vous devez également créer la configuration nécéssaire afin d'empêcher la création de *blank issues***.
5. **Créer un template de PR**
    - Discuttez des sections principales et secondaires que devrait contenir une PR. :warning: **Attention**: ne pas copier l'exemple du chargé de laboratoire!
    - Le template **doit** se trouver dans le dossier `.github/`.

## Partie 2 - Git (30%)

Cette partie renferme quelques questions concernant l'utilisation de `git`.

1. :scroll: **Quelle est la différence entre les commandes `rebase` et `merge`?**
    - Expliquez vous en quelques mots.
    - Remettez un graphique d'un arbre de commits simple à 2 branches, puis les résultats après un merge et après un rebase.
2. :scroll: **Dans les cas suivants, quelle(s) méthode(s) devrait-on favoriser?**
    1. Je travaille seul sur un projet, et je veux que mon arbre soit le plus propre possible.
    2. J'ai poussé un mot de passe secret dans mes fichiers par accident, et je veux pouvoir l'effacer du serveur.
    3. Je travaille dans une grosse équipe, où chaque tâche n'est attribuée qu'à une seule personne.
    4. Je dois intégrer du code provenant de multiple branches différentes.
3. :scroll: **Dans les situations qui suivent, montrez la liste des commandes nécéssaires afin d'atteindre le but. Si le but est impossible à atteindre, expliquez pourquoi et donnez tout de même une piste de solution.**
    1. J'ai poussé mon commit trop tôt et il y avait des erreur de compilation. Tout le monde de mon équipe est en train de travailler sur le projet (dans la même branche) et envoient des changements rapidement. Je viens de corriger l'erreur sur mon poste de travail, mais je n'ai pas encore commité ni ajouter mes modifications. **But:** pousser la modification.
    2. J'ai poussé mon commit trop tôt et il y avait des erreur de compilation. Tout le monde de mon équipe est en train de travailler sur le projet (dans la même branche) et envoient des changements rapidement. Je viens de corriger l'erreur sur mon poste de travail, mais je n'ai pas encore commité ni ajouter mes modifications. **But:** pousser la modification, *mais en remplaçant le commit erroné.*
4. :scroll: Pour cette question, on vous demande de vous référez à [ce repo](https://github.com/glo2003/H21-tp1-git), que vous pourrez cloner sur vos postes. **On vous demande d'intégrer les changements de toutes les branches dans la branche principale `main`. Vous devrez tenter de comprendre les changements qui ont été effectués en fonction du contenu présent sur Github.** Une fois les manipulations terminées :
    - Remettez une capture d'écran montrant la sortie au terminal lors de l'exécution de la commande `git log --graph --decorate --pretty=oneline --abbrev-commit --all`.
    - Remettez une capture d'écran montrant le contenu du fichier `liste.txt`.

## Partie 3 - Planification (30%)

**Avant** d'entamer la programmation, nous vous demandons de lire attentivement les exigences de la **partie 4**. Nous vous demandons ensuite de planifier vos tâches avec **Github**.

1. :scroll: **Créez un *milestone*** pour la remise du tp1. Insérez une capture d'écran afin de montrer les informations du milestone ainsi que les issues qu'il contient.
2. :scroll: **Créez des *issues*** afin de suivre votre progrès et de vous séparer la tâche. :warning: **Attention** Ce n'est pas nécéssairement 1 issue pour 1 feature. Assurez-vous également d'y remplir l'ensemble des parties tel que vu en laboratoire. Insérez une capture d'écran par issue. 
3. :scroll: **Créez des *PRs*** afin de suivre les changements effectués ou en attente. Assurez-vous également d'y remplir l'ensemble des parties tel que vu en laboratoire. Insérez une capture d'écran par PRs **uen fois résolue**. Vous n'avez pas à *scroller* afin de montrer le contenu des activités et commentaires.
4. :scroll: **Créez un *Github Project*** contenant vos issues. Insérez une capture d'écran montrant le tableau résultant. Elle peut être effectuée au début comme à la fin de votre progrès. Nous devons au moins y voir les colonnes ainsi que quelques issues. Une seule capture suffit (pas besoin de *scroller*).

## Partie 4 - Code (20%)

Pour cette partie, vous devrez développer les features demandées. Les formats de requêtes et réponse utilisent la notation typée de Typescript. **On s'attend à une réponse dans le format JSON pour l'ensemble des appels à l'API**. Des tests automatisés vérifieront les bons retours de votre API. Nous corrigerons également la **clarté** (clean code), l'**organisation** et l'**uniformisation** du code.

:warning: Pour cette remise, nous demandons de **laisser les exceptions se rendre à la réponse HTTP** (donc ne créez **pas** d'exception mappers). Jetty les transformeront automatiquement en erreurs 500 (ce qui sera vérifié par les tests automatisés). La gestion des exceptions sera vue au TP2.

### Feature 1

En temps qu'utilisateur du service, je désire pouvoir ajouter un item en vente.

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


### Feature 2

En temps qu'utilisateur du service, je désire pouvoir visionner les détails d'une offre publiée.

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
