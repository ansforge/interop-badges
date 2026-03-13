# Badges numériques – Projectathon ANS 2026

Ce dépôt héberge les **badges numériques Open Badge 2.0** délivrés par l'[Agence du Numérique en Santé (ANS)](https://esante.gouv.fr) à l'occasion du **Projectathon ANS 2026** (10-12 mars 2026).

Les badges sont publiés via **GitHub Pages** à l'adresse :
👉 `https://ansforge.github.io/interop-badges/`

---

## Types de badges

| Badge | Description |
|-------|-------------|
| 🎖️ **Moniteur** | Attribué aux moniteurs ayant encadré les tests d'interopérabilité |
| 🧪 **Test** | Attribué aux participants ayant testé leurs solutions |
| 🏛️ **Atelier** | Attribué aux participants aux ateliers du Projectathon |

---

## Structure du dépôt

```
pat2026/
├── images/                  # Visuels des badges (PNG)
│   ├── moniteur-projectathon-2026.png
│   ├── test-projectathon-2026.png
│   └── atelier-projectathon-2026.png
├── baked/                   # Badges baked (PNG avec assertion intégrée)
│   ├── badge-moniteur-{slug}.png
│   ├── badge-test-{slug}.png
│   └── badge-atelier-{slug}.png
├── assertions/              # Assertions Open Badge (JSON-LD)
│   ├── moniteur-projectathon-2026-{slug}.jsonld
│   ├── test-projectathon-2026-{slug}.jsonld
│   └── atelier-projectathon-2026-{slug}.jsonld
├── moniteur-projectathon-2026.jsonld   # Badge Class moniteur
├── test-projectathon-2026.jsonld       # Badge Class test
├── atelier-projectathon-2026.jsonld    # Badge Class atelier
└── issuer_ans.jsonld                   # Issuer ANS
```

---

## Standard Open Badge 2.0

Les badges suivent la spécification **[Open Badges 2.0](https://www.imsglobal.org/spec/ob/v2p0/)** de IMS Global.

### Ressources

- 📄 [Spécification Open Badges 2.0](https://www.imsglobal.org/spec/ob/v2p0/)
- 📄 [Open Badges – Introduction (IMS Global)](https://openbadges.org/)
- 🔍 [Validateur badgecheck.io](https://badgecheck.io)
- 🎓 [Importer sur Badgr](https://badgr.com)
- 🎓 [Importer sur Parchment](https://www.parchment.com)

### Fonctionnement

Chaque badge PNG est **baked** : l'assertion JSON-LD est intégrée directement dans le fichier PNG via un chunk `iTXt openbadges`. Cela permet de :
- Vérifier le badge en déposant simplement le PNG sur [badgecheck.io](https://badgecheck.io)
- Partager le badge comme une simple image tout en conservant les métadonnées de certification

### Chaîne de vérification

```
PNG baked
  └── iTXt openbadges → URL assertion
        └── assertion.jsonld (recipient, issuedOn, evidence)
              └── badge class (name, description, criteria)
                    └── issuer (ANS)
```

---

## Issuer

**Agence du Numérique en Santé (ANS)**
- Site : [esante.gouv.fr](https://esante.gouv.fr)
- LinkedIn : [Agence du Numérique en Santé](https://www.linkedin.com/company/1377858)
- Issuer JSON-LD : [issuer_ans.jsonld](https://ansforge.github.io/interop-badges/pat2026/issuer_ans.jsonld)
