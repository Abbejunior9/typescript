# Projet TypeScript - Interface et Classe Vehicule

## Description

Ce projet est une démonstration de l'utilisation de TypeScript pour définir une interface et implémenter une classe en respectant les principes de la programmation orientée objet.

## Fonctionnalités

- Définition d'une interface `Véhicule` avec des propriétés et une méthode.
- Implémentation d'une classe `Car` qui respecte l'interface.
- Création d'une instance de `Car` et appel de sa méthode `start`.
- Compilation du code TypeScript en JavaScript.

## Prérequis

- Node.js installé ([Télécharger ici](https://nodejs.org/))
- TypeScript installé globalement :
  ```sh
  npm install -g typescript
  ```

## Installation et Exécution

1. **Cloner le projet** (si applicable) :

   ```sh
   git clone https://github.com/utilisateur/projet-typescript.git
   cd projet-typescript
   ```

2. **Initialiser le projet** :

   ```sh
   npm init -y
   ```

3. **Installer TypeScript localement** :

   ```sh
   npm install --save-dev typescript
   ```

4. **Créer un fichier TypeScript** :

   ```sh
   touch index.ts
   ```

5. **Écrire le code dans `index.ts`** :

   ```typescript
   interface Vehicule {
     make: string;
     model: string;
     year: number;
     start(): void;
   }

   class Car implements Vehicule {
     constructor(
       public make: string,
       public model: string,
       public year: number
     ) {}
     start(): void {
       console.log("Car engine started");
     }
   }

   const myCar = new Car("Toyota", "Corolla", 2022);
   myCar.start();
   ```

6. **Compiler TypeScript en JavaScript** :

   ```sh
   npx tsc index.ts
   ```

   Cela génère un fichier `index.js`.

7. **Exécuter le fichier compilé** :
   ```sh
   node index.js
   ```

## Résultat Attendu

Lorsque vous exécutez `node index.js`, la console doit afficher :

```
Car engine started
```

## Auteurs

- Abbe junior

## Licence

Ce projet est sous licence MIT.
