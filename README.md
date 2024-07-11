Mini projet Kubernetes minikube k8S  ![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/608377bd-b970-425a-b5e5-50e73d099cfe)


Il est question de deployer l'appli wordpress constituée de la partie front ihm un container wordpress et la partie mysql qui sera la BDD.
le deploiement se fera : 
deployer un Pod mysql , il sera dans un objet de type deployment avec un seul replicat, il aura un service de type clusterip en frontal pour exposer le pod mysql en interne dans K8s et ensuite coupler à tout cela un pod wordpress qui sera dans un objet de type deployement, avec un service de type nodeport qui sera le point d'entrée de notre appli vers l'exterieur
L'appli wordpress devra interroger l'appli mysql en passant par son service de type clusterip
le mysql devra avoir un stockage /data/mysql, donc un volume comme dans docker  qui sera mis dans data, c'est le /var/lib/mysql qui sera stocké.
On lui associe aussi un volume simple dans /data/wordpress(le contenu /var/www/html) du conteneur frontal
tout ceci dans un namespace wordpress(toutes nos ressources seront dans ce namespace). celui qui vient de l'extérieur passera par le service nodeport pour avoir accès à l'apli

![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/32803b96-01a4-4bec-a46c-b552fd13de90)

Pour réaliser : 
- Cluster kubernetes
- Vagrantfile et script d'installation
- VirtualBox
- Minikube
- K8s
- Docker
- Docker-compose
- Vagrant
- Git

  Réalisation:
  Namespace: ![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/4237ce38-7382-41fe-a5d6-bfb87e7d6f63)

  Deploy : ![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/3debe80c-f1a2-4dfe-ba88-c7eceb05df5d)


  Services : ![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/cee33bae-ae85-4fdb-b73d-23c60959f17f)


  Podes :![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/b89868f1-6ce6-45f7-8e93-c069097c81c0)


  Secret: ![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/a07f219a-7fb6-4207-8435-50bc98d4e625)


  ![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/7a747ecf-ac45-4a66-a683-88f92a5b9d44)

![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/61442503-0974-4c59-b570-63c7768a74bd)

![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/d7a349e7-92f7-4687-8e00-2c2a424fe4ed)

![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/90d8200a-37a5-404d-a4a7-be06ed6f9d97)









  
