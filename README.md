# AZ-900 Cheat Sheet – Microsoft Azure Fundamentals

## Cloud Concepts

### Key Benefits
- Scalabilité : augmenter ou réduire les ressources
- Élasticité : ajustement automatique des ressources
- Haute disponibilité : continuité du service
- Facturation à l’usage : pay-as-you-go
- Agilité : déploiement rapide

### Cloud Models
| Modèle | Description |
|------|------------|
| Public | Azure, AWS, GCP |
| Privé | Datacenter interne |
| Hybride | On-premises + cloud |
| Multi-cloud | Plusieurs fournisseurs |

---

## Shared Responsibility Model

| Modèle | Client gère | Azure gère |
|------|------------|-----------|
| IaaS | OS, applications, données | Datacenter, matériel |
| PaaS | Code, données | OS, runtime |
| SaaS | Utilisateurs et données | Tout le reste |

Azure gère toujours la sécurité physique.

---

## Compute

### Services
- Azure Virtual Machines (IaaS)
- Virtual Machine Scale Sets
- Azure App Service (PaaS Web / API)
- Azure Functions (FaaS)
- Azure Kubernetes Service (AKS)
- Azure Container Instances (ACI)

### Points clés
- Azure Functions : facturation à l’exécution
- AKS : orchestration de conteneurs
- App Service : aucune gestion de serveur

---

## Global Infrastructure

### Région
- Zone géographique Azure
- Contient un ou plusieurs datacenters

### Availability Zones
- Datacenters physiquement séparés
- Protection contre pannes locales
- SLA élevé (99,99 %)

### Region Pairs
- Sauvegarde inter-région
- Mises à jour non simultanées

---

## Networking

### Services réseau
- Virtual Network (VNet)
- Network Security Group (NSG) : filtrage L4
- Azure Firewall : sécurité centralisée
- Web Application Firewall (WAF) : couche 7
- Load Balancer : couche 4
- Application Gateway : couche 7
- VPN Gateway : tunnel chiffré via Internet
- ExpressRoute : connexion privée
- Azure Bastion : accès VM sans IP publique
- Private Endpoint : accès privé aux services PaaS

DDoS Basic est inclus gratuitement.  
DDoS Standard fournit une protection avancée.

---

## Storage

### Types de stockage
| Type | Usage |
|----|------|
| Blob | Données non structurées |
| Disk | Disques de machines virtuelles |
| Files | Partage de fichiers SMB |
| Queue | Messagerie |
| Table | NoSQL clé/valeur |

### Blob Storage Tiers
- Hot : accès fréquent
- Cool : accès occasionnel
- Archive : long terme, latence élevée

### Redondance
| Option | Description |
|----|-------------|
| LRS | Redondance locale |
| ZRS | Redondance inter-zones |
| GRS | Redondance inter-région |
| RA-GRS | Lecture région secondaire |

---

## Identity & Security

### Azure Active Directory
- Gestion des identités
- Authentification multi-facteurs
- RBAC

### RBAC
Qui peut faire quoi sur quelle ressource.

### Services de sécurité
- Microsoft Defender for Cloud
- Azure Sentinel (SIEM)
- Azure Policy (conformité)
- Azure Key Vault (clés et secrets)

---

## Management & Governance

### Hiérarchie Azure
Management Group
└─ Subscription
└─ Resource Group
└─ Resources


### Services de gestion
- Azure Monitor : métriques et logs
- Log Analytics : requêtes sur les logs
- Activity Log : audit des actions
- Azure Advisor : recommandations
- Cost Management : gestion des coûts
- Azure Arc : gestion hybride
- ARM Templates : Infrastructure as Code

Supprimer un Resource Group supprime toutes les ressources qu’il contient.

---

## Pricing & SLA

### Facteurs de coût
- Type de service
- Région
- Consommation
- Niveau de stockage
- Trafic sortant

### Optimisation des coûts
- Azure Advisor
- Reserved Instances
- Auto-scaling
- Serverless

### SLA
Plus il y a de redondance, meilleur est le SLA.

---

## Exam Traps

- NSG n’est pas un Firewall
- Availability Set n’est pas Availability Zone
- ExpressRoute n’est pas un VPN
- Azure Monitor n’est pas Azure Advisor
- Azure Policy n’est pas RBAC

---

## Memory Hacks

- FaaS : Azure Functions
- Conteneurs : AKS ou ACI
- Gouvernance : Azure Policy + Management Groups
- Sécurité couche 7 : WAF
- Monitoring : Azure Monitor
- Hybride : Azure Arc
