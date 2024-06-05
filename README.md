# AngularNote
appunti Angular

- installa a livello globale angular cli
  
npm install -g @angular/cli 

- crea progetto "project"
  
ng new project

- installa dipendenze del progetto

  npm install

 - avvia server

    ng serve

- crea componente
  
ng generate component product-alerts 
se vogliamo il template interno e non vogliamo file di test
ng generate component home --inline-template --skip-tests

- crea interfaccia housingLocation
  ng generate interface housinglocation
  es.:
  `export interface HousingLocation {
  id: number;
  name: string;
  city: string;
  state: string;
  photo: string;
  availableUnits: number;
  wifi: boolean;
  laundry: boolean;
}` 

componente input
 @Input()
 si importa da @angular/core
 import { Component, Input } from '@angular/core';

 export class HousingLocationComponent {
  @Input() housingLocation!: HousingLocation;
}

il punto esclamativo serve per comunicare a typescript che il valore passato non deve essere nullo o indefinito si chiama non-null assertion operator
