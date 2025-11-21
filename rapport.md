# Rapport TP3 de Cybersec NOM PRENOM

## Attaque 1: BD fuitée et mot de passe

1. Retrouver la base de donnée
<img width="900" height="316" alt="image" src="https://github.com/user-attachments/assets/ddc7174e-d8b3-4100-9a5b-258e3bcaa1a6" />

2. Ouvrir l'application DataGrip et afficher le contenu du fichier de la base de donnée
<img width="723" height="670" alt="image" src="https://github.com/user-attachments/assets/11de2946-1885-4076-a818-479cc69815b5" />
<img width="974" height="543" alt="image" src="https://github.com/user-attachments/assets/ed533bd5-0dd7-4379-b6e6-c1f951d69041" />


4. Diriger vous dans ce fichier pour voir le nom et le mot de passe
<img width="1157" height="427" alt="image" src="https://github.com/user-attachments/assets/d1a69a13-450a-4b0e-b9cf-21448205f8b3" />

5. Pour ouvrir le mot de passe on va devoir aller sur le site de crack station. On peut voir que le mot de passe est "tristan" (https://crackstation.net/)
<img width="1115" height="622" alt="image" src="https://github.com/user-attachments/assets/ae863909-cd2c-4feb-aac8-c9fc3bb21b51" />


### Correctif implanté

Description du correctif.

Preuve que l'attaque ne fonctionne plus avec étapes + copie d'écran
1. Aller dans le source code avec Viusal studio code
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/9aeb8327-9a90-4227-a101-01c859429cce" />

2. Vous allez devoir installer des packets qui se nomme bcrypt.net
<img width="1488" height="661" alt="image" src="https://github.com/user-attachments/assets/6077825b-d8ae-4cdb-a0fa-25f3d3e848b9" />
<img width="1585" height="601" alt="image" src="https://github.com/user-attachments/assets/292804cd-504f-455c-907f-d0062c38644b" />

3. Diriger vous dans cette section
<img width="431" height="528" alt="image" src="https://github.com/user-attachments/assets/8156abf3-bd49-4d40-88d9-4e5150f7b6e0" />

4. Effectuer c'est modification dans le code pour pouvoir hasher le mot de passe avec bcrypt
<img width="1265" height="415" alt="image" src="https://github.com/user-attachments/assets/1001284c-ba86-4c09-acec-fa3c1349b1a1" />

5. Après avoir effectuer c'est modification démarrer la console, lister tous les premier ministre et afficher la base de donnée (cyber.db) 
<img width="1144" height="416" alt="image" src="https://github.com/user-attachments/assets/22e7fd36-5498-48fb-a00e-c98dc6264bd3" />

6. Nous allons ouvrir la base de donnée avec Datagrip
<img width="1285" height="691" alt="image" src="https://github.com/user-attachments/assets/6ae07723-89d4-43a3-9415-13a3c29a7d9e" />

7. Nous allons voir que
## Attaque 2: BD fuitée et encryption

1. Etape 1 + copie d'écran
2. Etape 2 + copie d'écran
3. etc.

### Correctif implanté

Court descriptif du correctif et lien vers le(s) commit(s).

Preuve que l'attaque ne fonctionne plus avec étapes + copie d'écran

## Attaque 3 Injection SQL

1. Etape 1 + copie d'écran
2. Etape 2 + copie d'écran
3. etc.

### Correctif implanté

Description du correctif.

Preuve que l'attaque ne fonctionne plus avec étapes + copie d'écran
