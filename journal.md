
## Jour 1 - Régions, AZ, coûts

### Ce que j'ai fait

- Région utilisée : eu-west-1
- Nombre de zones de disponibilité : 8 (noms : Ireland, Frankfurt, London, Milan, Paris, Spain, Stockholm, Zurich)

### Estimation mensuelle (Pricing Calculator)

| Ressource | Coût mensuel |
| --- | --- |
| EC2 t3.micro | 15 |
| EBS 20 Go gp3 | 18 |
| NAT Gateway (1) | 49 |
| IPv4 publique | 9 |
| **Total** | 91 |

### Ce que j'ai compris

- Ressource la plus chère : NAT Gateway
- Pourquoi je dois supprimer la NAT Gateway après chaque lab : pour eviter de payer sans utiliser
- Pourquoi on utilise 2 zones de disponibilité : pour une bonne redondance

## Jour 2 - IAM

### Ce que j'ai fait

- Utilisateur sans droits : AccessDenied par défaut
- Policy de lecture sur un bucket : ce qui marche / ne marche pas
- Deny sur secret.txt : l'emporte sur l'Allow
- Rôle assumé : identifiants temporaires

### Ce que j'ai compris

- Différence user / role : La différence fondamentale entre un Utilisateur IAM (User) et un Rôle IAM (Role) repose sur la permanence des identifiants et la manière d'accéder aux ressources AWS.
- Pourquoi un Deny gagne : Ce choix architectural répond à des impératifs stricts de sécurité et de gouvernance
- Rôle d'une trust policy : Une politique de confiance (Trust Policy, ou formellement AssumeRole Policy Document) est un document JSON attaché à un rôle IAM qui définit qui ou quel service a le droit d'utiliser (d'assumer) ce rôle.

### Bloqué sur

- sur les comprehensions des concepts
- la redaction et la comprehension des commandes AWS CLI

