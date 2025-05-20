# Breakable Toy II - Integration Repository

This repository integrates the frontend and backend of the Breakable Toy II project: a full-stack mmusic app built with react and springboot, powered by the Spotify API.
It uses Docker and Docker Compose to orchestrate both services in a local environment, simplifying the setup process.

## Structure

This project uses Git submodules:
- [`frontend`](https://github.com/Omar-Ballesteros/breakable2-frontend): React App.
- [`backend`](https://github.com/Omar-Ballesteros/breakable2-backend): Spring Boot App.

Clone the repository with submodules:
```bash
git clone --recurse-submodules https://github.com/Omar-Ballesteros/breakable2-integration
```

If you've already cloned it wothout --recurse-submodules, you can initialize them manually:
```bash
git submodule update --init --recursive
```

## Getting Started:

### Prerequisites

- Docker instaled and running.
- Spotify developer credentials:
  - `SPOTIFY_CLIENT_ID`
  - `SPOTIFY_CLIENT_SECRET`
  
You can get them from the Spotify Developer Dashboard.

### Environment Setup:

Create a `.env` file in the root of this repository with the following:
- SPOTIFY_CLIENT_ID=your_client_id
- SPOTIFY_CLIENT_SECRET=your_client_secret

### Running the App

From the root of the repo, run:

```bash
docker-compose up --build
```

### Services

Frontend (served via nginx): exposed at port 8080.

Backend: exposed at port 9090.
