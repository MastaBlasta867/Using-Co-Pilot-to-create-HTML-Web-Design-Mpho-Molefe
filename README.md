# Using-Co-Pilot-to-create-HTML-Web-Design-Mpho-Molefe
<!DOCTYPE html>
<html lang="en">
    <head>
        <link rel="stylesheet" href="css/meta.css">
        <title>My (Hlong Mpho Joseph Molefe) Responsive Web Design Lab</title>
        <link rel="stylesheet" href="css/main.css">
        <link rel="stylesheet" href="css/favicon.css">
        <style>
            *{
                text-decoration: none;
            }
            .navbar {
                background: crimson;
                font-family: "Times New Roman";
                padding-right: 15px;
                padding-left: 15px
            }
            .logo{
                font-size: 35px;
                font-weight: 600;
                color: white;
            }
            li{
                list-style: none;
                display: inline-block;
            }
            li a{
                color: whitesmoke;
                font-size: 18px;
                font-weight: bold;
                margin-right: 25px;
            }
            button{
                background-color: black;
                margin-left: 10px;
                border-radius: 10px
                padding: 10px;
                width: 90px;
            }
            button a{
                color: white;
                font-weight: bold;
                font-size: 15px;
            }
            body{
                color: whitesmoke;
            }
            .title{
                font-size: 6rem;
            }
            .subtitle{
                font-size: 4rem;
                @media (min-width: 200px){
                    body {
                        color: whitesmoke;
                    }
                }
            }
        </style>
    </head>
    <body>
            <nav class="navbar">
                <div class="divbar">
                    <div class="logo"><a href="#"></a></div>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#">About</a></li>
                        <li><a href="#">Contact</a></li>
                        <button><a href="#">SignIn</a></button>
                        <button><a href="#">SignUp</a></button>
                </div>
            </nav>
            <button id="Fetch-data">Fetch-data</button>
        <main>
        <h1>Everything You Wanna Know About Me</h1>
            <p>Hi! You can call me by my middle name, Joseph, but my first name is Mpho.  It's a South African name that in my language means 'gift'.  I began coding at an early age when I was a little boy, but then I (for whatever reason) stopped and now I'm back at it, having to re-learn everything.  I have decided to immerse myself in the realms of cybersecurity, coding, and soon-to-be game development.  I have studied a range of subjects that include both Front-end and Back-end development, including programming languages, Web Development, Database Management, and Software Engineering.  The objective is to build a solid foundation in computer science principles that will prepare me for a career in Cybersecurity and Software Development.  When I am not coding, I act on-screen and in theater.  I am male model professionally with a major talent agency. And I enjoy watching a good anime, particulary 'Attack on Titan'.</p>
            <h2>My Favorite Hobbies</h2>
            <ul>
                <li><a href="Acting">Acting</a></li>
                <li><a href="Singing">Singing</a></li>
                <li><a href="Spending time with the people I love">Spending time with the people I love</a></li>
                <li><a href="Adventuring and trying exciting, new things">Adventuring and trying exciting, new things</a></li>
            </ul>
                <li><a href="#">Singing.</a></li>
            <ol>
                <li>Complete the full-stack certification requirements.</li>
                <li>Pass the compTIA Security+ certification exam.</li>
                <li>Get a job in the cybersecurity and software engineering field.</li>
                <li>As an aspiring actor/model, I plan on starring in a feature film, television series, or international theater production.</li>
            </ol>
            <h4>Learn More About Me.</h4>
            <img src="PretendimageForLab.jpg" width="300" height="200" />
            <img src="PretendimageForLab.jpg" width="300" height="200" />
            <img src="PretendimageForLab.jpg" width="300" height="200"/>
            <video controls>
                <source src="PretendvideoForLab.mp4" type="video/mp4">
                <p>Sorry! This browser does not support the video tag.</p>
            </video>
            <form action="/Submit Feedback" method="post">
                <p><label for="name">Name</label></p>
                <p><input type="text" id="name" name="name"></p>
                <p><label for="email">Email</label></p>
                <p><input type="email" id="email" name="email"></p>
                <p><label for="feedback">Feedback</label></p>
                <p><textarea id="feedback" name="feedback" rows="4" cols="50"></textarea></p>
                <p><button type="submit">Submit</button></p>
            </form>
        </main>
        <script
        async function fetchDataAsync() {
                try {
                    const response = await fetch("https://jsonplaceholder.typicode.com/users");
                    const data = await response.json();
                    if (!response.ok) {
                        throw new Error(`Status: ${response.status}`);
                    }
                    const container = document.getElementById('data-container');
                    container.innerHTML = data
                        .map(user => `<p>${user.name} - ${user.email}</p>`)
                        .join('');
                } catch (error) {
                    console.error('Error fetching data', error);
                }
            }
            document.getElementById('Fetch-data').addEventListener('click', fetchDataAsync);
        </script>
    </body
    <footer style="background-color: chocolate; color: black;">
        <hr>
        Author: Hlong Mpho Joseph Molefe<br>
        &copy; 2025 copyright reserved<br>
        <small><a href="mailto:pomolefe@yahoo.com">pomolefe@yahoo.com</a></small>
    </footer>
</html>