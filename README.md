# Ex.08 Design of Interactive Image Gallery
# Date:
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Berkshire+Swash&family=Bokor&family=Pacifico&display=swap" rel="stylesheet">
    <meta charset="UTF-8">
    <title>Interactive Image Gallery</title>
    <style>
        
        body {
            font-family:  "Bokor", serif;;
            text-align: center;
            background-color: rgb(255, 0, 0);
            font-size: 60px;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
        }

        .photo {
            margin-top: 10%;
            margin-left: 2%;
            width: 240px;
            height: 440px;
            overflow: hidden;
            border-radius: 10px;
            border-width: 2px;
            border-color: solid black;
        }

        .photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .photo img:hover {
            transform: scale(1.1);
        }

        .lightbox {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            align-items: center;
            justify-content: center;
        }

        .lightbox-content {
            max-width: 90%;
            max-height: 80%;
        }

        .close {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 30px;
            font-weight: bold;
            color: white;
            cursor: pointer;
        }
    </style>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const lightbox = document.getElementById('lightbox');
            const lightboxImg = document.getElementById('lightbox-img');
            const photos = document.querySelectorAll('.photo img');
            const close = document.querySelector('.close');

            photos.forEach(photo => {
                photo.addEventListener('click', function() {
                    lightbox.style.display = 'flex';
                    lightboxImg.src = photo.src;
                });
            });

            close.addEventListener('click', function() {
                lightbox.style.display = 'none';
            });

            lightbox.addEventListener('click', function(event) {
                if (event.target !== lightboxImg) {
                    lightbox.style.display = 'none';
                }
            });
        });
    </script>
</head>
<body>
    <h1 style="font-size: 80px;">Interactive Photo Gallery</h1>
    <div class="gallery">
        <div class="photo">
            <img src="c:\PRIVATE\Web Application Development\Image gallery\flame.jpg" alt="Apache">
        </div>
        <div class="photo">
            <img src="c:\PRIVATE\Web Application Development\Image gallery\gojo.jpg" alt="BMW">
        </div>
        <div class="photo">
            <img src="c:\PRIVATE\Web Application Development\Image gallery\everyone.jpg" alt="Pulsar">
        </div>
        <div class="photo">
            <img src="c:\PRIVATE\Web Application Development\Image gallery\tanjiro.jpg" alt="Royal enfeild">
        </div>
        <div class="photo">
            <img src="c:\PRIVATE\Web Application Development\Image gallery\inosuke.jpg" alt="Yamaha z9x">
        </div>
        <div class="photo">
            <img src="c:\PRIVATE\Web Application Development\Image gallery\nezuko.jpg" alt="Yamaha z9x">
        </div>
    </div>
    <div id="lightbox" class="lightbox">
        <span class="close">&times;</span>
        <img class="lightbox-content" id="lightbox-img">
    </div>
</body>
</html>
```
# OUTPUT:
![Screenshot 2024-12-23 125811](https://github.com/user-attachments/assets/7be58dc6-38ef-4a24-b08c-5a0a0cd1e98e)
![Screenshot 2024-12-23 125850](https://github.com/user-attachments/assets/c8dce309-9f5f-41b1-92f6-fddbd1f3d94a)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
