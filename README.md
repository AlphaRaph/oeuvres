# Oeuvres

A Computer Science project (*Projet de NSI*) built in the final year of high school (*Terminale*), in collaboration with students specialising in visual arts (*Arts Plastiques*).

The goal was to create an **artwork library** that stores the works of every art student. Visitors and students can browse the collection through a **search bar** and **five thematic filters** defined by the art teacher:

- **Représentation**
- **Image**
- **Matérialité**
- **Processus**
- **Présentation**

Each artwork is rated from **0 to 5** on each filter. Artworks are stored in a JSON database (`JSON/oeuvres.json`), with their images hosted directly in the repository.

---

## Website — `main` branch

The public-facing website is built with **HTML, CSS, and JavaScript** and is hosted via **GitHub Pages**.

It consists of three pages:

- **Home** (`index.html`) — displays the five filter categories, each illustrated by a famous artwork, and lets users jump directly to a filtered catalogue view.
- **Catalogue** (`catalogue.html`) — shows the full artwork collection with interactive range sliders to filter results on each of the five dimensions simultaneously.
- **About** (`propos.html`) — describes the history and philosophy of the project.

---

## Admin Tool — `administrator` branch

Since no free server was available, the teacher's workflow is handled by a **local Python/Flask application** that he runs on his own machine.

This admin tool allows him to:

- **Add** a new artwork (with image upload)
- **Edit** an existing artwork's metadata
- **Delete** an artwork

Once a change is made locally, the tool automatically runs Git commands to **push the updated JSON database and images to the remote repository**, making them instantly available on the public GitHub Pages site.

### Running the admin server

```bash
# Install dependencies
pip install flask PyGithub

# Start the server
python main.py
```

Then open your browser at `http://localhost:5000`.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML · CSS · JavaScript |
| Fonts | Google Fonts (Oswald, Roboto) |
| Icons | Lordicon |
| Backend (admin) | Python · Flask |
| Hosting | GitHub Pages |
| Data storage | JSON file |

---

## Contributors

| Name | Role |
|---|---|
| BELLIOT Raphaël | Developer |
| GERARD Clément | Developer |
| NAOUR Milig | Developer |
