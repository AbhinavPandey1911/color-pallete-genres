
📁 chroma-connect/
├── 📁 src/
│   ├── 📁 app/
│   │   ├── 📁 core/                     # Singleton services and features used app-wide
│   │   │   ├── 📁 authentication/       # Authentication functionality
│   │   │   │   ├── 📄 auth.guard.ts     # Route guard for protected routes
│   │   │   │   ├── 📄 auth.service.ts   # Authentication service
│   │   │   │   └── 📄 token.interceptor.ts # HTTP interceptor for auth tokens
│   │   │   │
│   │   │   ├── 📁 interceptors/
│   │   │   │   ├── 📄 error.interceptor.ts  # Global error handling
│   │   │   │   ├── 📄 loader.interceptor.ts # Loading indicator management
│   │   │   │   └── 📄 index.ts              # Barrel file for interceptors
│   │   │   │
│   │   │   ├── 📁 services/
│   │   │   │   ├── 📄 api.service.ts    # Base API handling service
│   │   │   │   ├── 📄 palette.service.ts # Palette-specific API service
│   │   │   │   ├── 📄 genre.service.ts  # Genre-specific API service
│   │   │   │   └── 📄 modal.service.ts  # Modal management service
│   │   │   │
│   │   │   ├── 📁 models/
│   │   │   │   ├── 📄 palette.model.ts  # Palette interface/class
│   │   │   │   ├── 📄 genre.model.ts    # Genre interface/class
│   │   │   │   ├── 📄 color.model.ts    # Color interface/class
│   │   │   │   └── 📄 api-response.model.ts # API response interfaces
│   │   │   │
│   │   │   └── 📄 core.module.ts        # Core module declaration
│   │   │
│   │   ├── 📁 shared/                   # Reusable components, directives & pipes
│   │   │   ├── 📁 components/
│   │   │   │   ├── 📁 navigation/
│   │   │   │   ├── 📁 color-swatch/
│   │   │   │   ├── 📁 genre-card/
│   │   │   │   ├── 📁 detail-modal/
│   │   │   │   ├── 📁 color-detail/
│   │   │   │   ├── 📁 characteristic-pill/
│   │   │   │   ├── 📁 page-header/
│   │   │   │   ├── 📁 pagination/
│   │   │   │   ├── 📁 section-header/
│   │   │   │   └── 📁 loading-indicator/
│   │   │   │
│   │   │   ├── 📁 directives/
│   │   │   │   ├── 📄 click-outside.directive.ts
│   │   │   │   ├── 📄 contrast-text.directive.ts  # Auto text color based on background
│   │   │   │   └── 📄 lazy-load.directive.ts      # Lazy loading for images
│   │   │   │
│   │   │   ├── 📁 pipes/
│   │   │   │   ├── 📄 rgb-to-hex.pipe.ts       # Convert RGB to HEX
│   │   │   │   ├── 📄 safe-html.pipe.ts        # Sanitize HTML
│   │   │   │   └── 📄 truncate.pipe.ts         # Truncate long text
│   │   │   │
│   │   │   └── 📄 shared.module.ts         # Shared module declaration
│   │   │
│   │   ├── 📁 features/                    # Feature modules
│   │   │   ├── 📁 home/                    # Home page module
│   │   │   │   ├── 📁 components/
│   │   │   │   │   ├── 📄 home.component.ts
│   │   │   │   │   ├── 📄 featured-palettes.component.ts
│   │   │   │   │   └── 📄 project-description.component.ts
│   │   │   │   └── 📄 home.module.ts
│   │   │   │
│   │   │   ├── 📁 genres/                  # Genres module
│   │   │   │   ├── 📁 components/
│   │   │   │   │   ├── 📄 genres-list.component.ts
│   │   │   │   │   ├── 📄 genre-detail.component.ts
│   │   │   │   │   └── 📄 genre-palettes.component.ts
│   │   │   │   ├── 📄 genres-routing.module.ts
│   │   │   │   ├── 📄 genres.module.ts
│   │   │   │   └── 📁 store/              # NgRx store for genres
│   │   │   │       ├── 📄 genre.actions.ts
│   │   │   │       ├── 📄 genre.effects.ts
│   │   │   │       ├── 📄 genre.reducer.ts
│   │   │   │       ├── 📄 genre.selectors.ts
│   │   │   │       └── 📄 genre.state.ts
│   │   │   │
│   │   │   ├── 📁 palettes/               # Palettes module
│   │   │   │   ├── 📁 components/
│   │   │   │   │   ├── 📄 palettes-list.component.ts
│   │   │   │   │   ├── 📄 palette-detail.component.ts
│   │   │   │   │   └── 📄 palette-colors.component.ts
│   │   │   │   ├── 📄 palettes-routing.module.ts
│   │   │   │   ├── 📄 palettes.module.ts
│   │   │   │   └── 📁 store/             # NgRx store for palettes
│   │   │   │       ├── 📄 palette.actions.ts
│   │   │   │       ├── 📄 palette.effects.ts
│   │   │   │       ├── 📄 palette.reducer.ts
│   │   │   │       ├── 📄 palette.selectors.ts
│   │   │   │       └── 📄 palette.state.ts
│   │   │   │
│   │   │   └── 📁 about/                  # About page module
│   │   │       ├── 📄 about.component.ts
│   │   │       └── 📄 about.module.ts
│   │   │
│   │   ├── 📁 layout/                     # Layout components
│   │   │   ├── 📄 app-layout.component.ts # Main application layout
│   │   │   └── 📄 footer.component.ts     # Global footer
│   │   │
│   │   ├── 📁 store/                      # Root NgRx store
│   │   │   ├── 📄 app.state.ts            # Global app state
│   │   │   ├── 📄 index.ts                # Exports for store
│   │   │   └── 📄 root-reducer.ts         # Root reducer
│   │   │
│   │   ├── 📄 app-routing.module.ts       # Main routing configuration
│   │   ├── 📄 app.component.ts            # Root component
│   │   └── 📄 app.module.ts               # Root module
│   │
│   ├── 📁 assets/                         # Static assets
│   │   ├── 📁 images/
│   │   ├── 📁 icons/
│   │   └── 📁 fonts/
│   │
│   ├── 📁 environments/                   # Environment configuration
│   │   ├── 📄 environment.ts
│   │   └── 📄 environment.prod.ts
│   │
│   ├── 📁 styles/                         # Global styles
│   │   ├── 📄 variables.scss              # SCSS variables
│   │   ├── 📄 mixins.scss                 # SCSS mixins
│   │   ├── 📄 typography.scss             # Typography styles
│   │   └── 📄 theme.scss                  # Theme configuration
│   │
│   ├── 📄 index.html
│   ├── 📄 main.ts
│   ├── 📄 polyfills.ts
│   └── 📄 styles.scss                     # Global styles entry point
│
├── 📁 e2e/                                # End-to-end tests
│
├── 📄 angular.json                        # Angular configuration
├── 📄 package.json                        # Package dependencies
├── 📄 tsconfig.json                       # TypeScript configuration
├── 📄 karma.conf.js                       # Unit test configuration
└── 📄 README.md                           # Project documentation
```

## Essential Angular Topics Covered

1. **Modules & Component Architecture**
   - Feature modules (lazy-loading)
   - Core & Shared modules
   - Smart & Presentational components pattern

2. **Routing & Navigation**
   - Route configuration with child routes
   - Route guards for protected routes
   - Route resolvers for data pre-loading

3. **State Management with NgRx**
   - Store, Actions, Reducers
   - Effects for side effects
   - Selectors for efficient data retrieval

4. **HTTP & API Integration**
   - Services for API calls
   - HTTP Interceptors
   - Error handling

5. **Forms & Validation**
   - Reactive forms
   - Custom validators
   - Form state management

6. **Directives & Pipes**
   - Custom attribute directives
   - Custom structural directives
   - Custom pipes for data transformation

7. **Dependency Injection**
   - Service hierarchy
   - Provider configuration
   - Injection tokens

8. **Observables & RxJS**
   - Stream management
   - Operators for data transformation
   - Subscription management

9. **Angular Material Integration**
   - Component library usage
   - Theming
   - Accessibility

10. **Testing**
    - Unit tests with Jasmine
    - Integration tests
    - E2E tests with Protractor or Cypress
