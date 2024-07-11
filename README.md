Mini projet Kubernetes minikube k8S
Il est question de deployer l'appli wordpress constituee de la partie front ihm un container wordpress et la partie mysql qui sera la BDD.
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

  ![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/0de32c2d-8358-401d-9ef9-d54eb4643b52)
  ![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/6c763528-9ea9-4179-a5e0-6082ee054419)
  ![image](https://github.com/ehueni1982/mini-projet-k8s/assets/157939806/c33bdfd4-b992-4c73-bc2d-c0e5d1a325cc)




  
