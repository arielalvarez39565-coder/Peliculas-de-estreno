# Peliculas-de-estreno
Queremos que la página muestre las películas de estreno en el cine y dónde pueden estar disponibles para ver y una breve descripción.
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CineEstreno | Cartelera</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #e50914;
            --bg-dark: #141414;
            --card-bg: #1f1f1f;
            --text-light: #ffffff;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-light);
            margin: 0;
            line-height: 1.6;
        }

        header {
            background: linear-gradient(to bottom, rgba(0,0,0,0.8), transparent);
            padding: 40px 20px;
            text-align: center;
        }

        h1 {
            color: var(--primary);
            font-size: 2.5rem;
            margin: 0;
            letter-spacing: -1px;
        }

        .subtitle {
            color: #a3a3a3;
            font-size: 1rem;
        }

        /* Rejilla de Películas */
        .movies-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 25px;
            padding: 20px 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        /* Tarjeta de Película */
        .movie-card {
            background-color: var(--card-bg);
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.3s ease;
            position: relative;
            border: 1px solid #333;
        }

        .movie-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary);
            box-shadow: 0 15px 30px rgba(0,0,0,0.5);
        }

        .poster-container {
            width: 100%;
            aspect-ratio: 2/3;
            background-color: #333;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .movie-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .movie-info {
            padding: 15px;
        }

        .movie-title {
            font-size: 1.1rem;
            font-weight: bold;
            margin: 0 0 10px 0;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .tag {
            display: inline-block;
            background-color: var(--primary);
            font-size: 0.75rem;
            padding: 4px 12px;
            border-radius: 20px;
            font-weight: bold;
            text-transform: uppercase;
        }

        footer {
            margin-top: 50px;
            padding: 30px;
            text-align: center;
            border-top: 1px solid #333;
            color: #666;
        }

        /* Ajustes para móviles */
        @media (max-width: 600px) {
            .movies-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 15px;
                padding: 15px;
            }
            h1 { font-size: 1.8rem; }
        }
    </style>
</head>
<body>

    <header>
        <h1>CINE ESTRENO</h1>
        <p class="subtitle">Descubre los lanzamientos más esperados</p>
    </header>

    <main class="movies-grid">
        <article class="movie-card">
            <div class="poster-container">
                <img src="https://images.unsplash.com/photo-1485846234645-a62644f84728?auto=format&fit=crop&q=80&w=400" alt="Cine">
            </div>
            <div class="movie-info">
                <p class="movie-title">Nuevos Horizontes</p>
                <span class="tag">Estreno</span>
            </div>
        </article>

        <article class="movie-card">
            <div class="poster-container">
                <img src="https://images.unsplash.com/photo-1440404653325-ab127d49abc1?auto=format&fit=crop&q=80&w=400" alt="Drama">
            </div>
            <div class="movie-info">
                <p class="movie-title">El Silencio del Mar</p>
                <span class="tag">Estreno</span>
            </div>
        </article>

        <article class="movie-card">
            <div class="poster-container">
                <img src="https://images.unsplash.com/photo-1536440136628-849c177e76a1?auto=format&fit=crop&q=80&w=400" alt="Acción">
            </div>
            <div class="movie-info">
                <p class="movie-title">Ciudad Neón</p>
                <span class="tag">Próximamente</span>
            </div>
        </article>

        <article class="movie-card">
            <div class="poster-container">
                <img src="https://images.unsplash.com/photo-1598899139739-c44e85215819?auto=format&fit=crop&q=80&w=400" alt="Aventura">
            </div>
            <div class="movie-info">
                <p class="movie-title">Misterio en la Niebla</p>
                <span class="tag">Estreno</span>
            </div>
        </article>
    </main>

    <footer>
        <p>Página creada por Ariel para el proyecto de Estrenos 2026</p>
    </footer>

</body>
</html>
