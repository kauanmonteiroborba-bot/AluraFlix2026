# AluraFlix2026
trabalho desenvolvido nas aulas de curso técnico em AI.
<!DOCTYPE html>
<html lang="pt-PT">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Chakra+Petch:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,500;1,600;1,700&display=swap" rel="stylesheet">
    <title>Pokéflix | Edição Pokémon</title>
    <style>
        /* Cores globais e reposição (reset) */
        :root {
            --bg-color: #111116;
            --card-bg: #1a1a24;
            --primary-color: #ff3e3e; /* Vermelho Pokémon */
            --accent-color: #ffcb05;  /* Amarelo Pokémon */
            --text-color: #f5f5f7;
            --text-secondary: #a0a0b0;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            font-family: "Chakra Petch", sans-serif;
            overflow-x: hidden;
            padding-bottom: 50px;
        }

        /* Cabeçalho estilizado */
        header {
            background-color: rgba(17, 17, 22, 0.95);
            color: var(--primary-color);
            font-size: 2rem;
            font-weight: 700;
            padding: 20px 5%;
            text-shadow: 2px 2px 0px var(--accent-color);
            letter-spacing: 2px;
            border-bottom: 2px solid var(--primary-color);
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(8px);
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        header .edition {
            font-size: 0.9rem;
            color: var(--accent-color);
            text-shadow: none;
            border: 1px solid var(--accent-color);
            padding: 3px 8px;
            border-radius: 4px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Secção de Destaque (Principal) */
        .chamada {
            display: flex;
            flex-direction: column;
            gap: 30px;
            padding: 40px 5%;
            align-items: center;
            background: linear-gradient(180deg, rgba(255, 62, 62, 0.08) 0%, rgba(17, 17, 22, 0) 100%);
        }

        @media (min-width: 900px) {
            .chamada {
                flex-direction: row;
                justify-content: space-between;
                text-align: left;
                padding: 60px 5%;
            }
        }

        .chamada-texto {
            flex: 1;
            max-width: 500px;
        }

        .chamada-texto h1 {
            font-size: 2.5rem;
            font-weight: 700;
            color: #ffffff;
            line-height: 1.2;
            margin-bottom: 15px;
            text-transform: uppercase;
            transition: opacity 0.3s ease;
        }

        .chamada-texto p {
            font-size: 1.1rem;
            color: var(--accent-color);
            font-weight: 500;
            letter-spacing: 1px;
            transition: opacity 0.3s ease;
        }

        /* Vídeo Principal Responsivo */
        .video-container {
            flex: 1.2;
            width: 100%;
            max-width: 640px;
            aspect-ratio: 16/9;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5), 0 0 15px rgba(255, 62, 62, 0.2);
            border-radius: 12px;
            overflow: hidden;
            border: 2px solid rgba(255, 255, 255, 0.1);
            background-color: #000;
        }

        .video-container iframe {
            width: 100%;
            height: 100%;
            border: 0;
            transition: opacity 0.3s ease;
        }

        /* Secção de Categorias */
        .categoria {
            padding: 40px 5% 20px 5%;
        }

        .categoria h2 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--text-color);
            position: relative;
            display: inline-block;
            padding-bottom: 5px;
        }

        .categoria h2::after {
