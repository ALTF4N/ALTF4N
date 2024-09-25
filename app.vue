<template>
  <div class="portfolio">
    <header class="header">
      <h1>{{ name }}</h1>
      <p>{{ title }}</p>
      <nav>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#skills">Skills</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>

    <section id="about" class="section">
      <h2>About Me</h2>
      <p>{{ about }}</p>
    </section>

    <section id="skills" class="section">
      <h2>Skills</h2>
      <ul>
        <li v-for="skill in skills" :key="skill">{{ skill }}</li>
      </ul>
    </section>

    <section id="projects" class="section">
      <h2>Projects</h2>
      <div class="project" v-for="project in projects" :key="project.title">
        <h3>{{ project.title }}</h3>
        <p>{{ project.description }}</p>
        <a href="https://drive.google.com/drive/folders/1A4BWJZQ0j3wBJIIj9LKUPXwkmip6HZlQ?usp=sharing">check here !!</a>
      </div>
    </section>

    <section id="contact" class="section">
      <h2>Contact Me</h2>
      <p>Email: <a :href="`mailto:${email}`">{{ email }}</a></p>
    </section> 

    <footer class="footer">
      <p>&copy; 2024 {{ name }}. All rights reserved.</p>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Alfahryan Nurafin D",
      title: "Photographer & Beginner Web Developer",
      about: "I am a Just a guy who Interested at making website & Completing tasks.",
      skills: ["HTML", "CSS", "JavaScript", "Vue.js", "Nuxt.js","Photogrphy","Photoshop skills"],
      projects: [
        {
          title: "My Portofolio",
          description: "My jobs images to showcase my work and skills.",
            
        }
      ],
      email: "alfahryandarmansyah@gmail.com"
    };
  }
};
</script>

<style scoped>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f5f5f5;
}

.header {
  background-color: #333;
  color: white;
  padding: 25px;
  text-align: center;
}

.header nav ul {
  list-style: none;
  padding: 0;
}

.header nav ul li {
  display: inline;
  margin-right: 15px;
}

.header nav ul li a {
  color: white;
  text-decoration: none;
}

.section {
  padding: 40px;
  text-align: center;
}

#skills ul {
  list-style: none;
  padding: 0;
}

#skills ul li {
  display: inline-block;
  margin: 8px;
  background-color: #333;
  color: white;
  padding: 20px 30px;
  border-radius: 30px;
}

.project {
  margin-bottom: 5px;
}

.footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px;
  position: bottom;
  bottom: 0;
  width: 100%;
}
</style>