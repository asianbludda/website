<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Our Journey as College Freshmen of FEU-Roosevelt</title>

    <style>
        body {
            background: linear-gradient(135deg, #4CAF50, #FFEB3B);
            font-family: Arial, sans-serif;
            margin: 0;
            color: #333;
        }

        header, footer {
            background-color: #2e7d32;
            color: white;
            text-align: center;
            padding: 1rem;
        }

        nav {
            background-color: #cddc39;
            padding: 0.5rem;
            display: flex;
            justify-content: center;
            gap: 1rem;
        }

        nav a {
            color: #2e7d32;
            text-decoration: none;
            font-weight: bold;
        }

        nav a:hover {
            text-decoration: underline;
        }

        main {
            max-width: 900px;
            margin: 2rem auto;
            background: rgba(255, 255, 255, 0.9);
            padding: 1rem 2rem;
            border-radius: 10px;
        }

        h1, h2 {
            color: #2e7d32;
        }

        section {
            margin-bottom: 2rem;
        }

        img {
            width: 100%;
            max-width: 600px;
            border-radius: 10px;
            margin: 1rem 0;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
        }

        .gallery img {
            width: 250px;
            height: auto;
            border-radius: 10px;
        }

        @media (max-width: 600px) {
            nav {
                flex-direction: column;
                align-items: center;
            }

            .gallery img {
                width: 100%;
            }
        }

        button {
            background-color: #2e7d32;
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            font-size: 1rem;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #1b5e20;
        }

        #modal {
            display: none;
            position: fixed;
            z-index: 100;
            left: 0; 
            top: 0;
            width: 100%; 
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.6);
        }

        #modal-content {
            background-color: #fefefe;
            margin: 10% auto;
            padding: 2rem;
            border-radius: 10px;
            max-width: 400px;
            text-align: center;
        }

        #modal-close {
            color: #aaa;
            float: right;
            font-size: 1.5rem;
            font-weight: bold;
            cursor: pointer;
        }

        #modal-close:hover {
            color: black;
        }
    </style>
</head>
<body>

<header>
    <h1>Our Journey as College Freshmen of FEU-Roosevelt</h1>
</header>

<nav>
    <a href="#orientation">College Orientation</a>
    <a href="#sinag-concert">Sinag Tams Concert</a>
    <a href="#sinag-sports">Sinag Sports</a>
</nav>

<main>
    <section id="orientation" aria-label="College Orientation">
        <h2>College Orientation</h2>
        <p>
            Our orientation was a day filled with exciting introductions, valuable insights about campus life, and 
            the perfect opportunity to meet fellow freshmen. Many wore the iconic FEU-Roosevelt yellow shirts, building 
            a strong sense of community from day one.
        </p>
        <img src="/mnt/data/5b259ebb7ae6c224a03dc7e0149c5012.jpeg" alt="Orientation Group Photo" />
    </section>

    <section id="sinag-concert" aria-label="Sinag Tams Concert Activities">
        <h2>Sinag Tams Concert</h2>
        <p>
            The Sinag Tams Concert was an electrifying event with performances, music, and dancing showcasing the talents 
            of our fellow FEU-Roosevelt students. It was an amazing night to create new memories with friends.
        </p>
        <img src="/mnt/data/44384ff65cb1ef5488a2c2c26f000669.jpeg" alt="Sinag Tams Concert Photo" />
        <audio controls>
            <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg" />
            Your browser does not support the audio element.
        </audio>
    </section>

    <section id="sinag-sports" aria-label="Sinag Tams Sports Activities">
        <h2>Sinag Tams Sports</h2>
        <p>
            The Sinag Sports showcased teamwork and school spirit through exciting competitions. The cultural costumes 
            on display added vibrancy to the event, highlighting the diverse talents and cultures within our university.
        </p>
        <div class="gallery" aria-label="Images from Sinag Tams Sports activities">
            <img src="/mnt/data/e26d034c441e823b06bb8d1f6f2620b0.jpeg" alt="Sinag Sports Photo 1" />
            <img src="/mnt/data/att.3Hr5H4lNdThpv8tK8opX4IQwfBgqvlSvos1hGXp--t4.jpeg" alt="Sinag Sports Photo 2" />
        </div>
    </section>

    <section aria-label="Interactive Section">
        <h2>Share Your Freshmen Experience</h2>
        <p>Click the button below to share your thoughts and memories!</p>
        <button id="shareBtn">Share Experience</button>
    </section>
</main>

<footer>
    <p>&copy; 2025 FEU-Roosevelt Freshmen Journey</p>
</footer>

<div id="modal" role="dialog" aria-modal="true" aria-labelledby="modalTitle" aria-describedby="modalDesc">
    <div id="modal-content">
        <span id="modal-close" aria-label="Close">&times;</span>
        <h2 id="modalTitle">Thank You for Sharing!</h2>
        <p id="modalDesc">Your experience is valuable to us. Keep making amazing memories!</p>
    </div>
</div>

<script>
    const shareBtn = document.getElementById('shareBtn');
    const modal = document.getElementById('modal');
    const modalClose = document.getElementById('modal-close');

    shareBtn.addEventListener('click', () => {
        modal.style.display = 'block';
    });

    modalClose.addEventListener('click', () => {
        modal.style.display = 'none';
    });

    window.addEventListener('click', (event) => {
        if(event.target === modal) {
            modal.style.display = 'none';
        }
    });
</script>

</body>
</html>
