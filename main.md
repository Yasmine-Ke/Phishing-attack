

## Rapport d'Attaque de Phishing Utilisant Ngrok et SEToolkit

### Introduction
Ce rapport décrit les étapes détaillées pour mener une attaque de phishing en utilisant ngrok et le Social-Engineer Toolkit (SEToolkit). Cette méthode est couramment utilisée pour démontrer les vulnérabilités des systèmes et sensibiliser les utilisateurs aux dangers du phishing.

### Pré-requis
- Un compte sur ngrok.com
- Ngrok installé sur votre PC
- Kali Linux avec SEToolkit installé

### Étapes de l'Attaque

#### 1. Création d'un Compte Ngrok
1. **Ouvrir un compte sur ngrok.com :**
   - Visitez [ngrok.com](https://ngrok.com) et créez un compte gratuit.
   - cest quoi ngrok ? : Ngrok est un outil permettant de créer des tunnels sécurisés vers un serveur local.
 Il permet aux développeurs de rendre accessible sur Internet un service local en fournissant une URL publique temporaire.
Cela est particulièrement utile pour tester et déboguer des applications web, des services API, ou pour des démonstrations et présentations.
#### 2. Installation de Ngrok
2. **Téléchargement de Ngrok :**
   - Téléchargez ngrok pour votre système d'exploitation depuis la section de téléchargement du site.
   - Une fois téléchargé, ngrok sera dans votre dossier de téléchargements.

3. **Décompression de Ngrok :**
   - Ouvrez un terminal et naviguez vers le dossier de téléchargements :
     ```bash
     cd ~/Downloads
     ```
   - Décompressez le fichier téléchargé :
     ```bash
     tar -zxvf <nom_du_fichier_ngrok.tar.gz>
     ```
   - Vous trouverez le fichier ngrok décompressé dans le dossier de téléchargements.

4. **Connexion à votre compte Ngrok :**
   - Copiez le lien de connexion de votre compte ngrok depuis l'application ngrok.
   - Dans le terminal, exécutez :
     ```bash
     ./ngrok <votre_token_ngrok>
     ```

#### 3. Utilisation de SEToolkit pour Configurer l'Attaque de Phishing
5. **Ouverture de SEToolkit :**
   - Ouvrez un autre terminal et exécutez :
     ```bash
     sudo setoolkit
     ```
   - Définissez SEToolkit comme un ensemble d'outils permettant de mener diverses attaques d'ingénierie sociale.

6. **Choix du Type d'Attaque :**
   - Sélectionnez l'option 1 : "Social-Engineering Attacks"
   - Sélectionnez l'option 2 : "Website Attack Vectors"
   - Sélectionnez l'option 3 : "Credential Harvester Attack Method"

7. **Configuration du Site de Phishing :**
   - Choisissez "Web Templates" pour utiliser un modèle de site de phishing.
   - Lorsque l'outil vous demande une adresse IP, appuyez sur Entrée pour laisser le champ vide.
   - Choisissez un modèle de site parmi les options disponibles (par exemple, Google, Twitter).

8. **Obtention du Numéro de Port :**
   - SEToolkit vous attribuera un numéro de port, généralement le port 80.

#### 4. Tunnel HTTP avec Ngrok
9. **Démarrage de Ngrok :**
   - Revenez au premier terminal (celui de ngrok) et exécutez :
     ```bash
     ./ngrok http 80
     ```
   - Ngrok générera un lien public (par exemple, `http://<ngrok_subdomain>.ngrok.io`).


A. 
   ![Screenshot_2024-07-06_00-15-08](https://github.com/Yasmine-Ke/Phishing-attack/assets/123758173/44509ff4-161d-4865-aee4-4803d96177f8)
B. 
   ![Screenshot_2024-07-06_00-15-55](https://github.com/Yasmine-Ke/Phishing-attack/assets/123758173/ca7bf280-5717-4bed-b6dd-44b18a806b8f)
C. 
   ![Screenshot_2024-07-06_00-16-19](https://github.com/Yasmine-Ke/Phishing-attack/assets/123758173/74ebd791-28c3-4bc3-ad29-24672718dd08)
D. 
   ![Screenshot_2024-07-06_00-16-46](https://github.com/Yasmine-Ke/Phishing-attack/assets/123758173/f98193e5-544b-429d-8983-c519c34c001a)

10. **Utilisation du Lien Ngrok :**
    - Envoyez ce lien à votre cible. Lorsque la cible visite ce lien et entre ses informations d'identification, ces informations seront capturées.

#### 5. Récupération des Informations
11. **Vérification des Informations Capturées :**
    - Revenez au terminal où SEToolkit est en cours d'exécution. Les informations saisies par la cible seront affichées dans ce terminal.

### Conclusion
Ce rapport décrit les étapes pour configurer et mener une attaque de phishing en utilisant ngrok et SEToolkit. 
