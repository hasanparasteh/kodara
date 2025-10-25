# Kodara - حل مسئله، ساخت آینده

A Persian website for Kodara, a digital solutions company. This project is configured for static deployment on Cloudflare Workers.

## Features

- Responsive design optimized for Persian (RTL) content
- Modern CSS Grid and Flexbox layout
- Custom Persian font (BYekan)
- Mobile-first responsive design
- Static file serving with Cloudflare Workers

## Project Structure

```
kodara/
├── index.html          # Main HTML file
├── style.css           # Stylesheet
├── worker.js           # Cloudflare Worker script
├── wrangler.toml       # Cloudflare Workers configuration
├── package.json        # Node.js dependencies
├── fonts/              # Custom fonts
├── logos/              # Client logos
└── assets/             # Images and other assets
```

## Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- Cloudflare account

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd kodara
```

2. Install dependencies:
```bash
npm install
```

## Development

To run the project locally with Cloudflare Workers:

```bash
npm run dev
```

This will start a local development server at `http://localhost:8787`

## Deployment

### Method 1: Using Wrangler CLI

1. Install Wrangler globally (if not already installed):
```bash
npm install -g wrangler
```

2. Login to Cloudflare:
```bash
wrangler login
```

3. Deploy the project:
```bash
npm run deploy
```

### Method 2: Using Cloudflare Dashboard

1. Go to [Cloudflare Workers & Pages](https://dash.cloudflare.com/)
2. Create a new Worker
3. Upload the `worker.js` file
4. Configure the Worker settings:
   - Set the main module to `worker.js`
   - Add KV namespace for assets
5. Deploy

## Configuration

The `wrangler.toml` file contains the basic configuration:

```toml
name = "kodara"
main = "worker.js"
compatibility_date = "2024-01-01"

[site]
bucket = "./"
```

## Custom Domain

To use a custom domain:

1. In your Cloudflare dashboard, go to Workers & Pages
2. Select your worker
3. Go to Settings > Triggers
4. Add your custom domain

## Performance

This setup provides:
- Global CDN distribution
- Edge caching
- Automatic HTTPS
- Fast response times worldwide

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers
- RTL language support

## License

MIT License - All rights reserved to Kodara.
