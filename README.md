# grafana_dashboard
Il repository contiene la definizione in json delle dashboard di grafana.

# in caso di sparizione dashboard
Nel caso occorre:
1. settare correttamente le sorgenti dati
![Sources](Cattura_grafana_sorgenti.JPG)
2. caricare il json delle dashboard.

# copiare le dashboards con wizzy
```
 docker run --rm -it utkarshcmu/wizzy wizzy version
 /app # wizzy init
 /app # wizzy set grafana url http://10.10.99.135:3000
 /app # wizzy set grafana username admin
 /app # wizzy set grafana password <password>
 /app # wizzy import dashboards
```
mentre va il container, dalla macchina host
```
docker cp -L 747da65954b1:app/dashboards/ dashboards/
```
