# curly-telegram
Computer programming code

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Multimedia Project</title>
    <style>
        /* Basic page setup with Background Image */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #333;
            margin: 0;
            padding: 40px 20px;
            
            /* BACKGROUND IMAGE SETTINGS */
            background-image: url('your-background.jpg'); /* <-- Put your background image file name here */
            background-size: cover;          /* Forces the image to cover the entire screen */
            background-position: center;    /* Centers the image so it looks good on all screens */
            background-attachment: fixed;  /* Keeps the background still while you scroll the page */
            background-repeat: no-repeat;   /* Prevents the image from tiling/repeating */
        }

        header {
            text-align: center;
            margin-bottom: 50px;
            /* Added a text shadow so the title is easy to read over any background */
            text-shadow: 1px 1px 3px rgba(255, 255, 255, 0.8); 
        }

        header h1 {
            color: #2c3e50;
            margin-bottom: 8px;
        }

        header p {
            color: #555;
            margin-top: 0;
            font-weight: 500;
        }

        /* Section Container */
        .media-section {
            max-width: 1100px;
            margin: 0 auto 50px auto;
            /* Changed background to semi-transparent white (rgba) 
               so your background image peeks through beautifully! */
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(5px); /* Adds a modern blurry glass effect */
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
        }

        .media-section h2 {
            color: #2c3e50;
            margin-top: 0;
            border-bottom: 2px solid #ecf0f1;
            padding-bottom: 10px;
            margin-bottom: 25px;
        }

        /* 3-Column Grid for the items */
        .media-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        /* Individual item wrapper */
        .media-item {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .media-item span {
            font-weight: 600;
            color: #555;
            font-size: 0.95rem;
        }

        /* Image Rules */
        .project-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 8px;
            border: 1px solid #ddd;
        }

        /* Audio Rules */
        .project-audio {
            width: 100%;
            border-radius: 8px;
        }

        /* Video Rules */
        .project-video {
            width: 100%;
            aspect-ratio: 16 / 9;
            background-color: #000;
            border-radius: 8px;
        }
    </style>
</head>
<body>

    <header>
        <h1>My Multimedia Collection</h1>
        <p>A structured layout featuring 3 images, 3 audio tracks, and 3 videos.</p>
    </header>

    <section class="media-section">
        <h2>📷 Image Gallery</h2>
        <div class="media-grid">
            <div class="media-item">
                <span>Image One</span>
                <img src="your-image1.jpg" alt="Description 1" class="project-img">
            </div>
            <div class="media-item">
                <span>Image Two</span>
                <img src="your-image2.jpg" alt="Description 2" class="project-img">
            </div>
            <div class="media-item">
                <span>Image Three</span>
                <img src="your-image3.jpg" alt="Description 3" class="project-img">
            </div>
        </div>
    </section>

    <section class="media-section">
        <h2>🎵 Audio Tracks</h2>
        <div class="media-grid">
            <div class="media-item">
                <span>Audio Track One</span>
                <audio controls src="your-audio1.mp3" class="project-audio"></audio>
            </div>
            <div class="media-item">
                <span>Audio Track Two</span>
                <audio controls src="your-audio2.mp3" class="project-audio"></audio>
            </div>
            <div class="media-item">
                <span>Audio Track Three</span>
                <audio controls src="your-audio3.mp3" class="project-audio"></audio>
            </div>
        </div>
    </section>

    <section class="media-section">
        <h2>🎥 Video Playlist</h2>
        <div class="media-grid">
            <div class="media-item">
                <span>Video One</span>
                <video controls src="your-video1.mp4" class="project-video"></video>
            </div>
            <div class="media-item">
                <span>Video Two</span>
                <video controls src="your-video2.mp4" class="project-video"></video>
            </div>
            <div class="media-item">
                <span>Video Three</span>
                <video controls src="your-video3.mp4" class="project-video"></video>
            </div>
        </div>
    </section>

</body>
</html>
