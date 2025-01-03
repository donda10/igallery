# Ex.08 Design of Interactive Image Gallery
## Date:23-12-2024

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 10px;
            padding: 20px;
        }

        .gallery-item {
            position: relative;
            cursor: pointer;
            overflow: hidden;
        }

        .gallery-item img {
            width: 100%;
            height: auto;
            transition: transform 0.3s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
        }

        .modal img {
            max-width: 90%;
            max-height: 80%;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }

        .modal .close {
            position: absolute;
            top: 20px;
            right: 30px;
            color: white;
            font-size: 30px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1 style="text-align: center; padding: 10px;">Interactive Photo Gallery</h1>
    <div class="gallery" id="gallery">
        <div class="gallery-item"><img src="download (9).jpg" alt="Placeholder Image 1"></div>
        <div class="gallery-item"><img src="23.jpg" alt="Placeholder Image 2"></div>
        <div class="gallery-item"><img src="ca6e6d56-9909-44bd-bd22-546bc68867eb.jpg" alt="Placeholder Image 3"></div>
        <div class="gallery-item"><img src="download.gif" alt="Placeholder Image 4"></div>
        <div class="gallery-item"><img src="Look at the flower!.jpg" alt="Placeholder Image 5"></div>
    </div>

    <div class="modal" id="modal">
        <span class="close" id="close">&times;</span>
        <img id="modalImage" src="" alt="Modal Image">
    </div>

    <script>
        // Select elements
        const gallery = document.getElementById('gallery');
        const modal = document.getElementById('modal');
        const modalImage = document.getElementById('modalImage');
        const close = document.getElementById('close');

        // Open modal when an image is clicked
        gallery.addEventListener('click', function(event) {
            if (event.target.tagName === 'IMG') {
                modal.style.display = 'flex';
                modalImage.src = event.target.src;
            }
        });

        // Close modal when the close button is clicked
        close.addEventListener('click', function() {
            modal.style.display = 'none';
        });

        // Close modal when clicking outside the image
        modal.addEventListener('click', function(event) {
            if (event.target === modal) {
                modal.style.display = 'none';
            }
        });
    </script>
</body>
</html>



```

## OUTPUT:
![alt text](<Screenshot (33).png>)

![alt text](<Screenshot (34).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
