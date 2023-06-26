# Create an Angular app

You need to have installed Angular CLI: `npm install -g @angular/cli`

To create the app run: `ng new <app_name>`

# Create a Component

To create a component run: `ng generate component <component_name>`

The components should be within a `components` folder in the main/root folder of the project.

# Loop through an array in a Component

To loop through an array and display its data in a component:

1. Import the array in the <comp_name>.component.ts
   `import { Task } from '../../interfaces/Task'
`import { TASKS } from '../../mock-tasks';`
2. Create a variable typed to the interface:
   `tasks: Task[] = TASKS`
3. Loop through in the <comp_name>.component.html file:

```html
<p *ngFor="let task of tasks">  {{ task.text }}</p>
```

# Add Font Awesome to the project

To add Font Awesome to the project run: `ng add @fortawesome/angular-fontawesome`
Then choose the **Free** options in the CLI.
Check this link: https://github.com/FortAwesome/angular-fontawesome

# Create a Service

Services are typically used to handle tasks such as fetching and updating data, performing calculations, sharing state, and coordinating the communication between different parts of an application.

To create a service run: `ng generate service <service_name>`

Create a `services` folder within the app folder.

# Two-way binding form data

Two-way binding in Angular allows for synchronization of data between the component and the view. It enables automatic updates in both directions, meaning changes made in the view are reflected in the component, and changes made in the component are reflected in the view.

Example:

```html
<input type="text" name="text" id="text" placeholder="Add Task" [(ngModel)]="text" <==== />
```

In your `component.ts` file:

```typescript
export class AddTaskComponent implements OnInit {
  text!: string; // <======= This is the "text" variable that is being referenced in the html
  day!: string;
  reminder: boolean = false;

  ngOnInit(): void {}
}
```
