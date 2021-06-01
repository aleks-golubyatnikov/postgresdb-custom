# postgres usage example

## Step-01: Deploy manifests 
```
# Deploy manifests
kubectl apply -f ./postgresdb-custom
```
## Step-02: Connect to Postgres Database
```
# Connect to database
kubectl run -it --rm --image=postgres --restart=Never postgres-client -- psql -h postgres -U postgres

# Verify schemas, tables
\l
\c <database_name>
\dt
```
## Step-03: Clean-Up
```
# Delete all manifests
kubectl delete -f ./postgresdb-custom
```
