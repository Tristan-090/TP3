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

7. Nous allons voir que maintenant les mots de passe sont hasher avec Bcrypt. (On peut voir les ancien mot de passe avec MD5 qui n'était pas très bon)
<img width="1520" height="562" alt="image" src="https://github.com/user-attachments/assets/397102cf-ed23-4a03-993a-b81d1ab9b094" />

8. Nous allons maintenant faire le test avec crackstation comme on peut voir le premier mot de passe était hasher avec md5 et le second avec bcrypt
<img width="1123" height="485" alt="image" src="https://github.com/user-attachments/assets/fe6f36f9-5de2-4c70-be44-c3cbc087ed45" />

## Attaque 2: BD fuitée et encryption

1. comme on peut voir le NAS semble avoir un algorithme plustot facile (Tenter de crée un nouveau compte avec un NAS 123456789 et vous allez voir que tous les nas se ressembler (bdfhjlnpr))
<img width="103" height="172" alt="image" src="https://github.com/user-attachments/assets/091775b4-9e0d-474b-a494-8aa51b27c674" />

3. Etape 2 + copie d'écran
4. etc.

### Correctif implanté

Court descriptif du correctif et lien vers le(s) commit(s).

Preuve que l'attaque ne fonctionne plus avec étapes + copie d'écran
Chiffrement
<img width="955" height="510" alt="image" src="https://github.com/user-attachments/assets/16dbec3f-88b2-4525-8a80-85d49a60f42f" />
Déchiffrement
<img width="826" height="403" alt="image" src="https://github.com/user-attachments/assets/fdcce40b-c69c-43d5-821d-0e36732e4fa1" />

<img width="1390" height="752" alt="image" src="https://github.com/user-attachments/assets/67f421de-02ae-49de-8584-65acf3fab966" />

## Attaque 3 Injection SQL

1. Vous allez ouvrir ConsolApp.exe et faire lister les Premier ministre
<img width="672" height="466" alt="image" src="https://github.com/user-attachments/assets/d1d16cba-70fe-440a-aee1-a300b8a563ce" />

2. On peut voir avec DataGrip que la base de donnée contient tous les premiers ministre
<img width="1388" height="363" alt="image" src="https://github.com/user-attachments/assets/93813e4b-7920-4069-a765-5373f63a39e8" />

3. Maintenant nous allons faire un injection SQL en faisant cette command (nom = "'; DROP TABLE MUtilisateur; --") lors d'une connexion avec un compte
<img width="678" height="327" alt="image" src="https://github.com/user-attachments/assets/10426ae6-6677-4f06-b7a0-021251e795f7" />
<img width="696" height="331" alt="image" src="https://github.com/user-attachments/assets/87ab8228-5e9b-4296-8d1f-bfb44abfe4d8" />
<img width="829" height="547" alt="image" src="https://github.com/user-attachments/assets/f280012f-d134-4f82-a710-00d3a85a68f5" />

4. Maintenant nous allons vérifier la base de donnée avec DataGrip, comme on peut voir il nous manque la base donnée utilisateur
<img width="627" height="321" alt="image" src="https://github.com/user-attachments/assets/2db50329-9dcd-43c2-8333-5a137a4e4a2f" />


6. Etape 2 + copie d'écran
7. etc.

### Correctif implanté

Description du correctif.
1. Pour le correctif on va devoir modifier 3 fonction de code pour la première vous allez dans DonneesAcces.cs
<img width="416" height="396" alt="image" src="https://github.com/user-attachments/assets/0fa534f7-71e8-4b6d-8c3a-ac313865a199" />

2. Vous allez ensuite vous diriger vers la première fonction qui se nomme BDUtilisateurParSonNom

Voici la fonction présentement BDUtilisateurParSonNom :
<img width="932" height="352" alt="Avant" src="https://github.com/user-attachments/assets/f80fc2b9-fe7c-4f1c-af09-ab275c649d29" />

Vous allez devoir modifier cette fonction pour cela:
<img width="733" height="361" alt="Après" src="https://github.com/user-attachments/assets/d3147fd7-7cae-4656-8dcd-f78ffc4303da" />

3. Vous allez devoir vous diriger maintenant vers la fonction qui se nomme BDRevenusPour

Voici la fonction présentement BDRevenusPour :
<img width="911" height="344" alt="Avant" src="https://github.com/user-attachments/assets/17ec6d8d-0ddf-4556-802e-2f0464471483" />

Vous allez devoir modifier cette fonction pour cela:
<img width="749" height="348" alt="Après" src="https://github.com/user-attachments/assets/f13549db-272d-4e80-a1b1-31d3862a5d3b" />


4. Vous allez ensuite vous diriger vers la première fonction qui se nomme BDCreerUtilisateur

Voici la fonction présentement BDCreerUtilisateur :
<img width="776" height="211" alt="Avant" src="https://github.com/user-attachments/assets/54cea5f3-0557-40ae-8c46-a98dd5d707c3" />

Vous allez devoir modifier cette fonction pour cela:
<img width="940" height="223" alt="Après" src="https://github.com/user-attachments/assets/b2362b59-78f7-4aba-a481-d5d63a7f84c0" />

5. Nous allons maintenant tester que l'attaque ne fonctionne plus

Voici la base de donnée MUtilisateur :
<img width="1465" height="381" alt="image" src="https://github.com/user-attachments/assets/21b0a845-0f89-448b-adc3-9dc23870178b" />

Nous allons effectuer cette command nom = "'; DROP TABLE MUtilisateur; --" lors de la connexion et de la création de compte:
<img width="772" height="537" alt="image" src="https://github.com/user-attachments/assets/62259bea-5f7d-495e-860a-a7baad6b8e01" />

Comme on peut voir après avoir faite cette command la base de donnée ne c'est pas supprimé
<img width="1456" height="430" alt="image" src="https://github.com/user-attachments/assets/159146f8-f8c3-42b2-b320-d0add298eb10" />




Preuve que l'attaque ne fonctionne plus avec étapes + copie d'écran
