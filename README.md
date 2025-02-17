# AstroWorkerAssets

A template for building Astro applications with Cloudflare Workers and Assets, optimized for performance and developer experience.

## Features

- 🚀 [Astro](https://astro.build) for fast, content-focused websites
- ⚡️ [Cloudflare Workers](https://workers.cloudflare.com/) for serverless deployment
- 📦 Asset handling with Cloudflare's global CDN
- 🔧 TypeScript support out of the box
- 🛠️ Development tools:
  - Wrangler for local development and deployment
  - Smart placement for optimal performance
  - Built-in observability

## Prerequisites

- Node.js (Latest LTS version recommended)
- [Wrangler CLI](https://developers.cloudflare.com/workers/wrangler/install-and-update/) installed globally
- A Cloudflare account

## Getting Started

1. Create a new project using this template:

   ```bash
   git clone https://github.com/yourusername/astro-worker-assets.git my-project
   cd my-project
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Generate Worker types:

   ```bash
   npm run types
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

## Scripts

- `npm run dev` - Start the Astro development server
- `npm run build` - Build the project for production
- `npm run preview` - Preview the production build locally using Wrangler
- `npm run deploy` - Deploy to Cloudflare Workers
- `npm run types` - Generate TypeScript types for Cloudflare Workers

## Project Structure

```
/
├── src/
│   ├── components/
│   ├── layouts/
│   └── pages/
├── public/
│   └── .assetsignore    # Assets to exclude from deployment
├── astro.config.mjs     # Astro configuration
├── wrangler.jsonc       # Cloudflare Workers configuration
└── tsconfig.json        # TypeScript configuration
```

## Configuration

### Astro Configuration

The project uses `@astrojs/cloudflare` adapter with platform proxy enabled. You can modify the configuration in `astro.config.mjs`.

### Cloudflare Workers Configuration

The `wrangler.jsonc` file contains all the Cloudflare Workers-specific configuration:

- Asset binding for static files
- Node.js compatibility settings
- Smart placement for optimal performance
- Observability settings

## Deployment

1. Make sure you're logged in to Cloudflare:

   ```bash
   wrangler login
   ```

2. Deploy your application:
   ```bash
   npm run deploy
   ```

## Development

- The development server runs on `http://localhost:4321` by default
- Changes to files in `src/` will trigger hot module replacement
- The `preview` command will build and run your application locally using Wrangler

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - feel free to use this template for your own projects.

## Support

For questions and support:

- [Astro Documentation](https://docs.astro.build)
- [Cloudflare Workers Documentation](https://developers.cloudflare.com/workers/)
- [Create an issue](https://github.com/yourusername/astro-worker-assets/issues)
