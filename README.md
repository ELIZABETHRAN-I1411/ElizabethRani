<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <!-- <link rel="stylesheet" href="./style.css"> -->
     <style>
        @import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@200..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  font-family: "Poppins", sans-serif;

}
html{
    scroll-behavior: smooth;
}
nav{
    height: 15vh;
    background-color: black;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0px 10%;
    position: sticky;
    top: 0;
    z-index: 1;

}
nav>h1{
    font-size: 50px;
    font-weight: 70px;
}
nav>button{
    padding: 15px 30px;
    font-size: 18px;
    font-weight: bold;
    border-radius: 50px;
    border: none;
    cursor: pointer;
}
nav>ul{
    display: flex;
    justify-content: space-around;
    align-items: center;
    gap: 30px;
}
ul>li{
      list-style: none; 
      position: relative;  
}
ul>li>a{
    text-decoration: none;
    color: white;
    font-size: 18px;
    font-weight: bold;
    text-transform:uppercase;
}
ul>li::after{
    content: "";
    height: 4px;
    width: 0%;
    position: absolute;
    background-color: white;
    border-radius: 4px;
    bottom: -5px;
    left: 0;
    transition:width 0.7s ease-in;
}
ul>li:hover::after{
  width: 100%;
}
main{
    min-height: 100vh;
    background-color: rgb(15, 14, 14);
    color: #f6f3f3;
    display: flex;
    justify-content: space-between;
    padding: 20px 10%;
}
main> .left{
    flex-basis: 55%;

}
main> .right{
    flex-basis: 45%;
}
main>.left>h3{
    font-size: 30px;
    margin-bottom: 30px;
}
main>.left>h1{
    font-size: 70px;
    margin-bottom: 30px;
    animation: typing 3s infinite steps(10) alternate;
    white-space: nowrap;
    overflow: hidden;
    border-right: 1px solid ;
}

@keyframes typing{
    from{
        width: 0ch;
    }
    to{
        width: 17ch;
    }
}

main>.left>h2{
    font-size: 50px;
    margin-bottom: 40px;
}
main>.left>p{
    font-size: 24px;
    width: 70%;
    text-align: justify;
    margin-bottom: 40px;
}
main>.left>button{
    padding: 20px 10px;
    width:30%;
    border-radius:50px;
    font-size: 23px;
    font-weight: bold;
    text-transform: capitalize;

}
main>.right>img{
    width: 70%;
   object-fit: contain;
   border-radius: 50%;
}
main>.left span{
    color: rgb(168, 168, 10);
}

/* about */
#about{
    padding:100px 10%;
    background-color: #111;
    color: white;
}

#about>h1{
    text-align: center;
    text-transform: capitalize;
    font-size: 60px;
    letter-spacing: 3px;
    margin-bottom: 30px;
}

#about>p{
    font-size: 19px;
    color: #ccc;
    width: 70%;
    text-align: center;
    margin: 0px auto;
}


#about>.card{
    background-color: #222;
    width: 80%;
    margin: 30px auto;
    padding: 15px 25px;
    border-radius: 15px;
    cursor: pointer;
    transition: all 0.3s ease-in;
}

#about>.card>h2{
    text-transform :capitalize;
    letter-spacing:3px ;
    margin-bottom: 8px;
    font-size: 35px;
}


#about>.card:hover{
    box-shadow: 0px 5px 8px #f4d72f;
    transform: scale(1.04);

}


/* project sesion */

#project{
    background-color: #111;
    padding: 100px 10%;
    color: white;
}

.inner>.projectcard{
    /* background-color: red; */
    width: 350px;
    height: 450px;
    object-fit: cover;
    border-radius: 20px;
    cursor: pointer;
    overflow: scroll;
    transition: all0.3s ease-in;
    
}

::-webkit-scrollbar{
    display: none;
}
.projectcard>img{
    height: 40%;
    width: 100%;

}
#project>h1{
    text-align: center;
    text-transform: capitalize;
    font-size: 60px;
    letter-spacing: 1.4px;
    margin-bottom: 20px;

}

#project>p{
    text-align: center;
    font-size: 10px;
    color: #ccc;
    margin-bottom: 30px;
}

#project>.inner{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    row-gap: 30px;
}

.projectcard>h3{
    margin: 17px;
    text-transform: capitalize;
    color: #f4d72f;
}

.projectcard>p{
    margin: 0px 15px;
    margin: 0px 15px;
    color: #ddd;

}

.projectcard:hover{
    transform: translateY(-6px) scale(1.03);
}



/* contact section style */

.contact{
    padding: 100px 10%;
    background-color: #111;
    color: white;
}

.contact>h1{
    text-align: center;
    font-size: 60px;
    letter-spacing: 1.4px;
    margin-bottom: 30px;
}

.contact>p{
    text-align: center;
    font-size: 19px;
    margin-bottom: 25px;
    color: #ccc;
}

.contact>form{
    background-color: #222;
    width: 70%;
    margin: 0px auto;
    padding: 15px 25px;
    border-radius: 15px;
}


.contact>form>input{
    display: block;
    width: 100%;
    padding: 15px;
    margin-bottom: 15px;
    background-color: #333;
    border-radius: 10px;
    border: none;
}

.contact>form>textarea{
    width: 100%;
    display: block;
    background-color: #333;
    color: white;
    padding: 15px;
    margin-bottom: 10px;
    height: 100px;
    resize: none;
}

.contact>form>button{
    padding: 15px 25px;
    border-radius: 10px;
    background-color: white;
    border: none;
    font-size: 18px;
    font-weight: bold;
    letter-spacing: 1.3px;
    display: block;
    margin: 0px auto;
}

footer{
    height: 70px;
    background-color: #111;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;


}

@media(max-width:900px){
    main>ul{
        display: none;
    }

    main{
        flex-direction: column;
    }

    #project>.inner{
        justify-content: center;
    }
    #about>.card{
        width: 100%;
    }
    h1{
        font-size: 9px;    
    }
    h2{
        font-size: 14px;
    }
}

     </style>
</head>
<body>
    <!-- nav part -->
    <nav>
        <h1 class="logo">My_Portfolio</h1>
        <ul>
            <li><a href="#home">home</a></li>
            <li><a href="#about">about</a></li>
            <li><a href="#project">project</a></li>
            <li><a href="#contact">contact</a></li>
        </ul>

        <button>contact me</button>
    </nav>
    <!-- hero part -->
    <main id="home" >
        <aside class="left" >
            <h3 >Hello ,</h3>
            <h1>I'm <span>Elizabeth Rani </span></h1>
            <h2>Website Designer</h2>
            <p>To pursue a challenging position where I can utilize my knowledge, skills, and experience to contribute to the success
                    of the organization while fostering my professional growth.</p>
            <button>Hire me</button>
        </aside>
        <aside class="right">
            <img src="/Users/elizabethrani/Downloads/Elizabeth Rani.M.jpeg" alt="Elizabeth Rani M" >
        </aside>
        
    </main>
    <section id="about">
        <h1>What can i do</h1>
        <p>I am Skilled in these topics</p>
            <div class="card">
                <h2>UI/UX Design</h2>
                <p>Creative UI/UX designer with 2+ years of experience crafting intuitive interfaces and delightful experiences. Skilled in Figma, Sketch, user research, and prototyping. Passionate about solving user problems through design thinking."</p>
            </div>
            <div class="card">
                <h2>Website Design </h2>
                <p>Website designer with expertise in responsive design, HTML/CSS, and CMS platforms like WordPress. Proven track record of boosting engagement and conversions through user-centric designs. Focused on performance, accessibility, and clean code.</p>
            </div>
            <div class="card">
                <h2>Java Programming</h2>
                <p>Java developer with 3+ years of experience building scalable backend systems and Android apps. Proficient in Spring Boot, Hibernate, and Java 8 features. Passionate about clean code, problem-solving, and learning new tech.</p>
            </div>
            <div class="card">
                <h2>Database </h2>
                <p>Data-driven database expert with 3+ years optimizing, and managing SQL/NoSQL databases. Skilled in MySQL, MongoDB, PostgreSQL, and data modelinggreSQL, and data modeling. Passionate about performance tuning, data security, and scalable solutions.</p>
            </div>

        </section>
        <!-- project -->

        <section id="project" >
            <h1>my projects</h1>
            <p>I have prior experience in Android app development, and I am now seeking job opportunities in the app development field. Please let me know if there are any vacancies in your company that match my profile.</p>


            <div class="inner">
                <div class="projectcard">
                <img src="./img/password.jpeg" alt="passwordGenarator">
                <h3>Password generator</h3>
                <p>Developed a secure password generator app that creates strong, customizable passwords. Features include length selection, character type options (uppercase, lowercase, numbers, symbols), and copy-to-clipboard functionality. Built with [tech stack, e.g., JavaScript, React, Python] focusing on security and user experience.</p>

                </div>
            
                 <div class="projectcard">
                    <img src="./img/todotask.jpeg" alt="Todoapp_img">
                    <h3>Todo App</h3>
                    <p>Built a feature-rich Todo app to manage tasks efficiently. Key features: add, edit, delete, and mark tasks as complete; task filtering and search; responsive UI. Implemented with Node.js focusing on CRUD operations and intuitive UX.</p>

                 </div>

                <div class="projectcard">
                    <img src="./img/weathertask.jpeg" alt="">
                    <h3>Weather App</h3>
                    <p>Developed a real-time weather app providing current conditions and forecasts. Features include location-based search, temperature units toggle (°C/°F), and dynamic UI updates. Integrated with OpenWeatherMap API, built with  React, JavaScript, CSS. Focused on clean UI and accurate data display.</p>
                </div>

                <div class="projectcard">
                    <img src="./img/ecommerce.jpeg" alt="">
                    <h3>Ecommerce App Project</h3>
                    <p>Built a full-stack ecommerce platform enabling product browsing, cart management, and secure checkout. Features: product search/filter, user auth, payment gateway integration (e.g., Stripe), order tracking. Tech stack:  Node.js, Express. Focused on UI/UX, scalability, and secure transactions.</p>
                </div>

            </div>

        
        </section>


        <!-- contact  -->

        <section class="contact" id="contact">
            <h1>Contact Me</h1>
            <p>Please fill out the below form to discuss any work opportunities.</p>
            
            <form action="">
                <input type="text" placeholder="Enter your Name">
                <input type="email" placeholder="Enter your Email">
                <textarea name="" id="" placeholder="Your Message"></textarea>
                <button>Submit</button>
            </form>
        </section>
        <!-- footer -->
         <footer>
            <p>Copyright &copy; My Portfolio.All Rights Resevered</p>
         </footer>
</body>
</html>
