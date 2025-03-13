<!DOCTYPE html>
<html>
<head>
    <title>Dynamic Project Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9; 
            margin: 0;
            padding: 0;
        }

        h1 {
            text-align: center;
            padding: 20px;
            background-color: #9361ff; 
            color: white;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
            padding: 20px;
        }

        .project-card {
            background-color: #fff; 
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .project-card:hover {
            transform: translateY(-10px); 
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
        }

        .project-card img {
            width: 100%;
            height: auto;
            border-radius: 8px;
        }

        .project-card h3 {
            margin-top: 10px;
            font-size: 20px;
            color: #333;
        }

        .project-card p {
            font-size: 14px;
            color: #555;
            margin: 10px 0;
        }

        .project-card a {
            display: inline-block;
            margin-top: 10px;
            padding: 10px 20px;
            background-color: #9361ff; 
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-size: 16px;
            transition: background-color 0.3s;
        }

        .project-card a:hover {
            background-color: #9361ff; 
        }
    </style>
</head>
<body>

    <h1>Project Gallery</h1>
    
    <div id="gallery" class="gallery">
    </div>

    <script>
        const projects = [
            {
                "title": "Project 1",
                "description": "This is a web application built using HTML, CSS, and JavaScript that displays a dynamic project gallery.",
                "image": "https://via.placeholder.com/400x200?text=Project+1",
                "url": "https://www.example.com/project1"
            },
            {
                "title": "Project 2",
                "description": "This is a web application built using HTML, CSS, and JavaScript that displays a dynamic project gallery.",
                "image": "https://via.placeholder.com/400x200?text=Project+2",
                "url": "https://www.example.com/project2"
            },
            {
                "title": "Project 3",
                "description": "This is a web application built using HTML, CSS, and JavaScript that displays a dynamic project gallery.",
                "image": "https://via.placeholder.com/400x200?text=Project+3",
                "url": "https://www.example.com/project3"
            },
            {
                "title": "Project 4",
                "description": "This is a responsive website designed using HTML5, CSS3, and JavaScript, optimized for all screen sizes.",
                "image": "https://via.placeholder.com/400x200?text=Project+4",
                "url": "https://www.example.com/project4"
            },
            {
                "title": "Project 5",
                "description": "A dynamic portfolio showcasing various projects and skills, built with modern web technologies.",
                "image": "https://via.placeholder.com/400x200?text=Project+5",
                "url": "https://www.example.com/project5"
            }
        ];

        function displayProjects() {
            const gallery = document.getElementById('gallery');

            projects.forEach(project => {
                const projectCard = document.createElement('div');
                projectCard.classList.add('project-card');

                const image = document.createElement('img');
                image.src = project.image;
                image.alt = project.title;
                projectCard.appendChild(image);

                const title = document.createElement('h3');
                title.textContent = project.title;
                projectCard.appendChild(title);

                const description = document.createElement('p');
                description.textContent = project.description;
                projectCard.appendChild(description);

                const link = document.createElement('a');
                link.href = project.url;
                link.target = "_blank";
                link.textContent = "View Project";
                projectCard.appendChild(link);

                gallery.appendChild(projectCard);
            });
        }

        window.onload = displayProjects;
    </script>
</body>
</html>
