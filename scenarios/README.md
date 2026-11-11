# Scénarios de test

Ce dossier décrit les scénarios joués dans le lab pour vérifier que chaque règle se déclenche.
Ils ne doivent être exécutés que sur les machines virtuelles du lab, dans un réseau isolé.

À compléter à partir de votre compte rendu : pour chaque scénario, l'outil utilisé,
la machine source, la machine cible, et le résultat attendu dans Kibana.

| Scénario | Source → Cible | Log observé | Règle attendue | Résultat |
|---|---|---|---|---|
| Brute force SSH | Kali → Metasploitable2 | Zeek `ssh.log` | `ssh_bruteforce.yml` | à compléter |
| Injection SQL | Kali → Metasploitable2 | Zeek `http.log` | `sqli_http.yml` | à compléter |
| Flood ICMP | Kali → Metasploitable2 | Zeek `conn.log` | `icmp_flood.yml` | à compléter |
| Attaque sur le poste Windows | Kali → Windows | Winlogbeat (4624 / 4625) | à écrire | à compléter |
