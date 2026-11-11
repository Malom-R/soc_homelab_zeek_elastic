# Rapport d'incident — [titre court]

| Champ | Valeur |
|---|---|
| Date de détection | AAAA-MM-JJ HH:MM |
| Analyste | |
| Gravité | Faible / Moyenne / Élevée / Critique |
| Technique MITRE ATT&CK | ex. T1110.001 |
| Règle déclenchée | ex. `detections/ssh_bruteforce.yml` |

## 1. Résumé

Deux ou trois phrases : ce qui s'est passé, sur quelle machine, avec quel impact.

## 2. Chronologie

| Heure | Source de log | Événement |
|---|---|---|
| 10:02:14 | Zeek `conn.log` | Première connexion TCP de `<IP source>` vers `<IP cible>`:22 |
| 10:02:16 – 10:03:30 | Zeek `ssh.log` | N échecs d'authentification |
| 10:03:45 | `auth.log` | Connexion réussie |

## 3. Preuves

Pour chaque preuve : la requête KQL utilisée, une capture d'écran, et ce qu'elle démontre.

```
event.dataset: "zeek.ssh" and source.ip: "<IP source>"
```

![Capture](../docs/screenshots/NOM-DE-LA-CAPTURE.png)

## 4. Analyse

- Adresse source, service ciblé, durée, volume.
- L'attaque a-t-elle réussi ? Qu'est-ce qui le prouve ?
- Corrélation entre les logs réseau (Zeek) et les logs de la machine (Linux ou Windows).

## 5. Recommandations

- Mesure immédiate (ex. bloquer l'adresse source).
- Mesure durable (ex. authentification par clé, limitation du nombre de tentatives).
- Amélioration de la détection (ex. seuil de la règle à ajuster).
