# Movie Explorer Application

## Project Description

A React single-page application to search and browse movies using the public OMDb API. Users can search by title, filter by type, view results as cards (poster, title, year, rating, type and genre), and open a details page for each movie.

## Features

- Search by title with the Search button or Enter key
- Empty input validation
- Optional type filter (All, Movies, Series)
- Movie cards with poster, title, year, rating and type/genre
- "Load more" pagination
- Movie details page: poster, plot, genre, rating, director, cast, language, awards and more
- Search saved in the URL, so the Back button restores your results
- Loading, error, no-results and 404 states
- Responsive for mobile, tablet and desktop

## Technologies Used

React 18, Vite, React Router v6, React Hooks (`useState`, `useEffect`), JavaScript ES6+, Fetch API, HTML5, CSS3, npm, Git and GitHub.

## API Used

[OMDb API](https://www.omdbapi.com/) (free key required).

## Setup and How to Run

1. Get a free API key at https://www.omdbapi.com/apikey.aspx and confirm it from the email OMDb sends you.
2. Open the project folder in VS Code and run `npm install`.
3. Copy `.env.example` to `.env` and set your key:
   ```
   VITE_OMDB_API_KEY=your_real_key
   ```
4. Run `npm run dev` and open the address shown (usually http://localhost:5173).
5. Search for a movie such as "Avatar".

If you change `.env`, stop and restart `npm run dev`. Other commands: `npm run build` (production build) and `npm run preview`.

## Project Structure

```
movie-explorer/
├── index.html
├── package.json
├── vite.config.js
├── .env.example
├── .gitignore
├── README.md
└── src/
    ├── main.jsx            App entry, BrowserRouter
    ├── App.jsx             Layout and routes
    ├── index.css           All styles
    ├── api/omdb.js         API calls and error messages
    ├── components/         Navbar, SearchBar, MovieCard, Poster, Loader, ErrorMessage
    └── pages/              Home, MovieDetails, NotFound
```

## Routes

| Path | Page |
| --- | --- |
| `/` | Home and search (`/?q=Avatar`) |
| `/movie/:id` | Movie details |
| `*` | 404 page |

## React Concepts Used

- Functional components and props
- `useState` for form, results and loading state
- `useEffect` for fetching data (with a cleanup flag to ignore outdated responses)
- React Router: `BrowserRouter`, `Routes`, `Route`, `Link`, `useParams`, `useNavigate`, `useSearchParams`
- Conditional rendering and list rendering with keys
- Controlled form inputs

## Git and GitHub

```bash
git init
git add .
git commit -m "Initial Movie Explorer application"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```

Suggested commit messages:

1. `Set up React project with Vite and React Router`
2. `Add OMDb API module and movie search`
3. `Create movie cards and results grid`
4. `Add movie details page`
5. `Add loading, error handling and responsive styles`

The `.env` file is listed in `.gitignore` so your API key is not uploaded to GitHub.
