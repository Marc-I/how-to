# Angular CLI
## CLI

```npm i -g @angular/cli```

``` ng new myApp --routing --style=scss --skip-tests ```

``` cd myApp ```

``` ng config schematics.@schematics/angular.component.spec false ```

### Routing

``` <router-outlet></router-outlet> ```

``` 
  { path: '', redirectTo: '/dashboard', pathMatch: 'full' },
  { path: 'dashboard', component: DashboardComponent },
  { path: 'detail/:id', component: HeroDetailComponent },
  { path: 'heroes', component: HeroesComponent }
```

### Paths

```
    "baseUrl": "src",
    "paths": {
      "@environments/*": ["environments/*"],
      "@components/*": ["app/components/*"],
      "@public/*": ["app/components/public/*"],
      "@admin/*": ["app/components/admin/*"],
      "@models/*": ["app/models/*"],
      "@services/*": ["app/services/*"],
      "@utilities/*": ["app/utilities/*"]
    }
 ```
 
 ```
import { DashboardComponent } from '@components/dashboard/dashboard.component';
import { LoginComponent } from '@components/login/login.component';
 ```

## Material Design
### Step 1

``` npm install --save @angular/material @angular/cdk @angular/animations ```

### Step 2: Configure animations
```
import {BrowserAnimationsModule} from '@angular/platform-browser/animations';

@NgModule({
  ...
  imports: [BrowserAnimationsModule],
  ...
})
export class PizzaPartyAppModule { }
```

### Step 3: Import the component modules
```
import {MatButtonModule, MatCheckboxModule} from '@angular/material';

@NgModule({
  ...
  imports: [MatButtonModule, MatCheckboxModule],
  ...
})
export class PizzaPartyAppModule { }
```
### Step 4: Include a theme

```
@import "~@angular/material/prebuilt-themes/indigo-pink.css";
```

## Fontawesome Icons

got to [Fontawesome](https://fontawesome.com/how-to-use/on-the-web/setup/getting-started?using=web-fonts-with-css)

copy link (like

  ``` <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.1.1/css/all.css" integrity="sha384-O8whS3fhG2OnA5Kas0Y9l3cfpmYjapjI0E4theH4iuMD+pLhbf6JI0jIMfYcK3yZ" crossorigin="anonymous"> ```

  ) into src/index.html
