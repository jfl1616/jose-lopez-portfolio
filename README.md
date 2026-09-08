# Jose Lopez Jr — Portfolio

Personal portfolio site for Jose Lopez Jr, Integration Engineer / QA & Test Automation professional.

Live: https://joseflopezjr.com
Docker Hub: https://hub.docker.com/r/jfl1616/jose-lopez-portfolio

## Structure

```
jose-lopez-portfolio/
├── index.html              # Main page
├── css/
│   └── style.css           # Styles (dark/light theme)
├── js/
│   └── main.js             # Theme toggle, mobile nav, typing effect
├── images/
│   └── profile.jpg         # Profile photo
├── assets/
│   └── resume.pdf          # Downloadable resume
├── Dockerfile               # Nginx-based static build
├── nginx.conf               # Nginx server config
├── docker-compose.yml        # Local container run
└── .github/workflows/
    └── docker-build.yml      # CI: validates the Docker build on push/PR
```

## Run locally (no Docker)

Just open `index.html` in a browser, or serve the folder with any static file server:

```bash
python3 -m http.server 8080
```

## Run with Docker

Build and run:

```bash
docker build -t jfl1616/jose-lopez-portfolio:latest .
docker run --rm -p 8080:80 jfl1616/jose-lopez-portfolio:latest
```

Or with Docker Compose:

```bash
docker compose up --build
```

Visit http://localhost:8080

## Publish

Push to GitHub:

```bash
git add .
git commit -m "Update portfolio"
git push origin main
```

Push the image to Docker Hub:

```bash
docker login
docker build -t jfl1616/jose-lopez-portfolio:latest .
docker push jfl1616/jose-lopez-portfolio:latest
```

## Features

- Responsive design (mobile + desktop)
- Dark / Light theme toggle (saved in localStorage)
- Smooth scrolling navigation with scroll-spy
- Typing animation in hero section
- Containerized with Docker + Nginx
- GitHub Actions CI validates the Docker build on every push

## Projects Included

1. **This Portfolio Site** – HTML/CSS/JS, Docker, GitHub Actions
2. **IST Department Website** – HTML/AJAX + jQuery + Dark Mode
3. **ASL Inside** – Bootstrap, CSS, PHP, ZenCart (Live: https://aslinside.com)

---

© 2026 Jose Lopez Jr
