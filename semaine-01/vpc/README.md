flowchart TB
  Internet --> IGW[Internet Gateway]
  subgraph VPC["VPC 10.0.0.0/16"]
    subgraph AZa["eu-west-1a"]
      PA["public-a 10.0.1.0/24"]
      VA["private-a 10.0.11.0/24"]
    end
    subgraph AZb["eu-west-1b"]
      PB["public-b 10.0.2.0/24"]
      VB["private-b 10.0.12.0/24"]
    end
  end
  IGW --> PA
  IGW --> PB
## Ce qui m'a bloqué
- la raison du deploiement des reseaux prives et public
- le but du VPC dans le developpement