# OpenMRS ESM Patient Chart 🏥

The `openmrs-esm-patient-chart` is a frontend module for the OpenMRS SPA. It is a monorepo containing various microfrontends (MFEs) that serve as widgets in a patient dashboard.

:wave: **New to our project?** Review the [OpenMRS 3 Frontend Developer Documentation](https://openmrs.atlassian.net/wiki/x/IABBHg).

---

## 🚀 Setup & Development

### Installation

This monorepo uses [yarn](https://yarnpkg.com). To install dependencies, run:

```bash
yarn

```

### Starting the Dev Server

To start a dev server for a specific microfrontend:

```bash
yarn start --sources 'packages/esm-patient-<insert-package-name>-app'

```

### Working with Multiple Microfrontends

1. **Multiple Sources:** Pass multiple flags:
```bash
yarn start --sources 'packages/esm-patient-biometrics-app' --sources 'packages/esm-patient-vitals-app'

```


2. **Import Map Overrides:** Run `yarn serve` from within individual packages and use [import map overrides](https://openmrs.atlassian.net/wiki/spaces/docs/pages/150962685/Develop+Frontend+Modules#Using-import-map-overrides).

---

## 📦 Monorepo Layout

### Core Libraries

* [Common lib](https://www.google.com/search?q=packages/esm-patient-common-lib/README.md) — Cross-cutting concerns and shared logic.
* [Patient chart](https://www.google.com/search?q=packages/esm-patient-chart-app/README.md) — The main container app.

### Patient Dashboard Widgets

<details>
<summary><b>Click to expand the list of available widgets</b></summary>

* [Allergies](https://www.google.com/search?q=packages/esm-patient-allergies-app/README.md)
* [Attachments](https://www.google.com/search?q=packages/esm-patient-attachments-app/README.md)
* [Conditions](https://www.google.com/search?q=packages/esm-patient-conditions-app/README.md)
* [Flags](https://www.google.com/search?q=packages/esm-patient-flags-app/README.md)
* [Forms](https://www.google.com/search?q=packages/esm-patient-forms-app/README.md)
* [Immunizations](https://www.google.com/search?q=packages/esm-patient-immunizations-app/README.md)
* [Lists](https://www.google.com/search?q=packages/esm-patient-lists-app/README.md)
* [Medications](https://www.google.com/search?q=packages/esm-patient-medications-app/README.md)
* [Notes](https://www.google.com/search?q=packages/esm-patient-notes-app/README.md)
* [Orders](https://www.google.com/search?q=packages/esm-patient-orders-app/README.md)
* [Patient banner](https://www.google.com/search?q=packages/esm-patient-banner-app/README.md)
* [Programs](https://www.google.com/search?q=packages/esm-patient-programs-app/README.md)
* [Tests](https://www.google.com/search?q=packages/esm-patient-tests-app/README.md)
* [Vitals and Biometrics](https://www.google.com/search?q=packages/esm-patient-vitals-app/README.md)

</details>

---

## 🧪 Testing

### Unit and Integration Tests

Powered by [Turborepo](https://turbo.build/).

| Task | Command |
| --- | --- |
| **Run All Tests** | `yarn turbo run test` |
| **Watch Mode** | `yarn turbo run test:watch` |
| **Specific Package** | `yarn turbo run test --filter=@openmrs/esm-patient-<name>` |
| **Coverage Report** | `yarn turbo run coverage` |

> **Note:** To bypass the cache, add the `--force` flag to any turbo command.

### End-to-End (E2E) Tests

1. **Environment Setup:** ```bash
npx playwright install
cp example.env .env
```

```


2. **Execution:**
* **Headless:** `yarn test-e2e`
* **Headed:** `yarn test-e2e --headed`
* **UI Mode:** `yarn test-e2e --ui`



Read the [E2E Testing Guide](https://openmrs.atlassian.net/wiki/x/K4L-C) for more details.

---

## 🔧 Troubleshooting

If your local environment is out of sync with [Dev3](https://dev3.openmrs.org/openmrs/spa), update the core libraries:

```bash
yarn up openmrs@next @openmrs/esm-framework@next
git checkout package.json
yarn

```

---

## 📚 Resources

* **Design Patterns:** Visit our [Design System](https://zeroheight.com/23a080e38/p/880723--introduction).
* **Configuration:** See the [Implementer Documentation](https://wiki.openmrs.org/pages/viewpage.action?pageId=224527013).
* **Deployment:** Refer to [Creating a Distribution](https://openmrs.atlassian.net/wiki/x/xoIBCQ).

---

