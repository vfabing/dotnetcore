Prérequis :
- `git clone https://github.com/vfabing/dotnetcore.git`
- Vérifier que la bonne souscription Azure est bien sélectionnée (`az account show`)
- Pousser la version non modifié de l'image dotnetcore sur ACR

- Création webapp P1v2 avec l'image `appsvc/dotnetcore`  
(30s ~ 1mn30)  
- Montrer : https://github.com/Azure-App-Service/dotnetcore/

- Activation `Continuous Deployment`

- Aller dans le dossier `2.1.1`  
- Ouvrir VS Code  
- Modifier le fichier `hostingstart.html`  
`Bienvenue au GAB Paris 2019`  

- `az acr build --registry acrvfa --image dotnetcore .`  
(< 1mn)
