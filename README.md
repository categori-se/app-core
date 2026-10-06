# app-core

Alpha 0.1.0-alpha.1; Apache-2.0. Not for production use.

`@categori/app-core` currently exports `@categori/app-core/theme.css`, a semantic theme foundation. Import it before application-specific styles.

Applications provide `--app-theme-<role>-light` and optional `--app-theme-<role>-dark` palette inputs. Resolved `--app-<role>` variables cover background, surfaces, text, borders, accent, status, brand and shadows. Font and radius inputs are mode-independent.

Set `data-app-theme="light"`, `"dark"` or `"auto"` on the root or a nested element for scoped mode selection. System preference is the default; absent dark values fall back to light inputs. Compatible application aliases should be declared on `:root, [data-app-theme]` to recalculate in nested scopes.

Applications remain responsible for usable palettes, foreground contrast, allowed customization, login presentation and branding. Untrusted arbitrary CSS is not a profile interface. This is a theme foundation, not a universal application shell or an authentication/authorization module.

Registry packages are not published by this source release. Node manifests retain `private: true` to guard against accidental npm publication. See the repository CI for offline test commands.
