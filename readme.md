# monitoring-bootrap

Ce dépôt est en lien avec mon article medium : https://medium.com/ouidou/un-monitoring-complet-en-quelques-minutes-avec-prometheus-33e849e6392e

Dans ce dépot vous allez trouver un projet pour lancer une stack de monitoring complète pour votre infrastructure. Ici j'utilise docker-compose pour lancer les différents services. C'est idéal pour un POC mais aussi viable en production. Si vous le souhaitez, vous pouvez très bien installer directement les services sur des machines virtuelles en reprenant les fichiers de configuration pour un départ simplifié. Vous retrouverez les dépôt github de toutes les technologies utilisées ci-dessous :

- [Prometheus](https://github.com/prometheus/prometheus)
- [Grafana](https://github.com/grafana/grafana)
- [Alertmanager](https://github.com/prometheus/alertmanager)
- [Blackbox exporter](https://github.com/prometheus/blackbox_exporter)
- [Node exporter](https://github.com/prometheus/node_exporter)

## lancer la stack

Pour lancer la stack il vous suffira de cloner ce dépôt et simplement de faire la commande suivante à la racine :

```console
docker-compose up -d
```

Dans le docker compose j'utilise le réseau de la machine et non le réseau virtuel de docker, vous pouvez donc retrouver les différents services en **localhost** sur leurs ports par défaut :

- Prometheus : `9090`
- Alertmanager : `9093`
- Grafana : `3000`
- Node exporter : `9100`

## grafana

J'ai changé le login/pass par défaut, voici les credentials de grafana :

- login : `unicorn`
- password : `UnicornsExists!`

## ouidou

Chez ouidou, nous aimons jouer avec les nouvelles technologies et nous sommes toujours curieux de découvrir des projets sympa et de nouvelles personnes. On recrute, donc n'hésite pas à nous contacter [ici](mailto:contact@ouidou.fr) et de visiter notre site [ici](https://ouidou.fr).
