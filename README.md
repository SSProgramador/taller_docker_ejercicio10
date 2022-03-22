# taller_docker_ejercicio10
pingapp

# Crear el namespace
kubectl create namespace pingapp

# Aplicar el configmap de env
kubectl apply -f configmap-env.yaml -n pingapp

# Aplicar el configmap de file json
kubectl apply -f configmap-config-files.yaml -n pingapp

# Aplicar el configmap de file secret json
kubectl apply -f configmap-config-files-secret.yaml -n pingapp

# Aplicar el deployment
kubectl apply -f deployment.yaml -n pingapp

# Aplicar el servicio
kubectl apply -f service.yaml -n pingapp

# Ingresar adentro del pod
kubectl exec -it "nombre del pod" -n "nombre del namespace" -- "comando a ejecutar en el pod (/bin/bash) "



