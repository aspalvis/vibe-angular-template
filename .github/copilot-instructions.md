# GitHub Copilot Instructions for Angular Projects

## MCP/agent integration

- The repository has an MCP config at `.vscode/mcp.json` that uses `npx -y @angular/cli mcp`. If your automated tooling relies on that, it will run Angular CLI's MCP adapter.

## Developer workflows (commands you should use)

- Start dev server (auto-reload): `npm start` (runs `ng serve`).
- Generate typescript poco models from JSON schema: `npm run types`
- Build production: `npm run build` (runs `ng build`).
- Watch incremental builds: `npm run watch` (runs `ng build --watch --configuration development`).
- Run unit tests: `npm test` (runs `ng test` using Karma/Jasmine).
- The repo includes a VS Code task for `npm start` (see `.vscode/tasks.json` via the VS Code Tasks UI).

## Project Structure

- Place page components in the `components/pages` directory.
- Place shared components in the `components/shared` directory.
- Place services in the `services` directory, and API services in `services/api`.
- Place types in the `types` directory.
- Place assets (images, styles, etc.) in the `assets` directory.
- Separate component styles and templates into their own files (e.g., `my-component.component.css` and `my-component.component.html`).
- Use pages hierarchy for routing (e.g., `components/pages/home`, `components/pages/about`, `components/pages/users/user-details`).
- Place modal components inside `components/shared/modals` if they are shared, other wise place them inside component folder where their are used, for example `components/pages/users/modals/add-user-modal`.

## General Guidelines

- Prefer Angular best practices for structure, naming, and code organization.
- Use TypeScript for all source files.
- Follow the Angular CLI conventions for file and folder naming.
- Use Angular modules, components, services, and directives appropriately.
- Write clean, readable, and maintainable code.
- Use RxJS for reactive programming and asynchronous operations.
- Prefer Angular's dependency injection for service usage.
- Use Angular forms (ReactiveFormsModule or FormsModule) for user input.
- Write unit tests for components, services, and pipes using Jasmine and Karma.
- Avoid direct DOM manipulation; use Angular templates and directives.
- Use Angular routing for navigation between views.
- Follow Angular style guide for code formatting and organization.

## Code Comments

- Add JSDoc comments for public classes, methods, and properties.
- Use inline comments to explain complex logic.

## Error Handling

- Handle errors gracefully using Angular's error handling mechanisms.
- Use try/catch blocks where appropriate, especially in asynchronous code.

## Security

- Sanitize user input and output to prevent XSS.
- Avoid exposing sensitive information in the frontend code.

## Performance

- Use OnPush change detection strategy where possible.
- Lazy load modules for better performance.

## Accessibility

- Follow accessibility best practices in templates (ARIA attributes, semantic HTML).
