# Villa Agency – Azure Static Web App

A real-estate showcase website built with HTML5, CSS3, and Bootstrap, deployed via **Azure Static Web Apps**.

---

## Prerequisites

No build step is required. You only need a way to serve static files locally.

| Tool | Purpose |
|------|---------|
| [Git](https://git-scm.com/) | Clone the repository |
| A local HTTP server (see options below) | Serve the site locally |

---

## Running Locally

### Option 1 – VS Code Live Server (recommended)

1. Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VS Code.
2. Open the repository folder in VS Code.
3. Right-click `index.html` → **Open with Live Server**.
4. The site opens automatically at `http://127.0.0.1:5500`.

### Option 2 – Node.js `http-server`

```bash
# Install once (requires Node.js)
npm install -g http-server

# From the repository root
http-server . -p 8080
```

Then open <http://localhost:8080> in your browser.

### Option 3 – Python built-in server

```bash
# Python 3
python -m http.server 8080
```

Then open <http://localhost:8080> in your browser.

### Option 4 – Azure Static Web Apps CLI

The [SWA CLI](https://azure.github.io/static-web-apps-cli/) lets you emulate the Azure Static Web Apps environment locally.

```bash
# Install once
npm install -g @azure/static-web-apps-cli

# From the repository root
swa start .
```

Then open <http://localhost:4280> in your browser.

---

## Project Structure

```
.
├── index.html            # Home page
├── properties.html       # Property listing page
├── property-details.html # Individual property detail page
├── contact.html          # Contact page
├── assets/
│   ├── css/              # Custom stylesheets
│   ├── js/               # Custom scripts
│   ├── images/           # Site images
│   └── webfonts/         # Font Awesome web fonts
├── vendor/
│   └── bootstrap/        # Bootstrap CSS & JS
└── .github/
    └── workflows/        # Azure Static Web Apps CI/CD pipeline
```

---

## Deployment

The site is automatically deployed to **Azure Static Web Apps** on every push to the `master` branch via the GitHub Actions workflow in `.github/workflows/`.

To set up your own deployment:

1. Create an Azure Static Web App in the [Azure Portal](https://portal.azure.com).
2. Link it to your GitHub repository.
3. Azure will generate a workflow file and add the required `AZURE_STATIC_WEB_APPS_API_TOKEN` secret to your repository automatically.

---

## License

This template is based on [TemplateMo 591 Villa Agency](https://templatemo.com/tm-591-villa-agency).
