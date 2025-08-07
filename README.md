# PDF to HTML Conversion Server

## Setup

1. Install dependencies:
```bash
npm install
```

## Run the server

### Development mode:
```bash
node server.js
```

### With auto-restart on changes (using nodemon):
```bash
npm install -D nodemon
npx nodemon server.js
```

### Production mode (with PM2):
```bash
npm install -g pm2
pm2 start server.js
```

## API Endpoints

- `GET /` - Server status
- `POST /api/convert` - Upload PDF for conversion
  - Body: multipart/form-data with 'pdf' field
  - Only accepts .pdf files

## Server runs on
- Default: http://localhost:3000
- Set custom port: `PORT=8080 node server.js`