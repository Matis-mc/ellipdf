# Ellipdf

## Lancement projet angular :
Ce projet utilise les fonctionnalités SSR d'Angular. Pour fonctionner, 2 bundles doivent être générés ( et regénérés à chaque modification) :
- le bundle de l'application Angular classique, situé dans le répertoire dist/browser, généré par la commande :
```
ng build
```
- le bundle de l'application SSR, situé dans le répertoire dist/server, généré par la commande : 
```
npm run build:ssr
```
Pour lancer l'application en mode SSR, il faut donc avoir réaliser les deux builds ci-dessus, puis effectuer la commande :
```
npm run serve:ssr
```

## Utilisation de pandoc

Installation des outils : 
- installer pandoc : https://pandoc.org/installing.html 
- installer MiKTeX : https://miktex.org/download

Commande de génération de pdf :
 - lancer l'application angular SSR sur le port 4200
 - ouvrir un terminal + commande : 
```
pandoc -o test.pdf http://localhost:4200
```


## Informations supplémentaires :

Afin de "transformer" une application Angular en SSR exécuter la commande suivante dans le répertoire angular :
```
ng add @nguniversal/express-engine
```
