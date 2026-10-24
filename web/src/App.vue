
<script setup lang="ts">
import { ref } from 'vue'

const menuOpen = ref(false)

const projects = [
  {
    number: '01',
    category: 'Electronics',
    title: 'Power Supply',
    description:
        'Designed and assembled a power supply system that converts electrical input into stable voltage and current for computer components.',
    tags: ['Circuit Design', 'Soldering', 'Troubleshooting'],
  },
  {
    number: '02',
    category: 'Embedded Systems',
    title: 'Smoke Warning Device with LCD',
    description:
        'Built a microcontroller-based hazard detection system using sensors to display air-quality data and trigger alerts.',
    tags: ['Microcontroller', 'Sensors', 'LCD'],
  },
  {
    number: '03',
    category: 'Web Development',
    title: 'CPE Alumni Job Portal',
    description:
        'Developed a web-based platform with user authentication and database management to connect Computer Engineering alumni with job opportunities.',
    tags: ['HTML', 'CSS', 'JavaScript', 'Database'],
  },
  {
    number: '04',
    category: 'Embedded Programming',
    title: 'PIC16F877A Development Board',
    description:
        'Programmed embedded C logic to control an LCD screen and display dynamic text and team member identification.',
    tags: ['Embedded C', 'PIC16F877A', 'LCD'],
  },
  {
    number: '05',
    category: 'IoT & Agriculture',
    title: 'Automated Vertical Farming System',
    description:
        'Designed and developed an IoT-based smart agriculture system that automates irrigation and environmental control using real-time sensor readings.',
    tags: ['IoT', 'Automation', 'Sensors'],
  },
]

const skills = [
  {
    title: 'Programming',
    items: 'HTML, CSS, JavaScript, C, C++, Java, Python, PostgreSQL',
  },
  {
    title: 'CAD & 3D Modelling',
    items: 'AutoCAD, SketchUp',
  },
  {
    title: 'Electronics & Simulation',
    items: 'Multisim, Proteus',
  },
  {
    title: 'Hardware Prototyping',
    items: 'PIC Development Kit, Breadboard Assembly, Circuit Testing',
  },
  {
    title: 'Productivity',
    items: 'Microsoft Word, Excel, PowerPoint',
  },
  {
    title: 'Professional Skills',
    items: 'Team Collaboration, Communication, Time Management',
  },
]

const navItems = [
  { label: 'Home', href: '#home' },
  { label: 'About', href: '#about' },
  { label: 'Projects', href: '#projects' },
  { label: 'Skills', href: '#skills' },
  { label: 'Education', href: '#education' },
  { label: 'Contact', href: '#contact' },
]
</script>

<template>
  <div class="portfolio">
    <!-- Navigation -->
    <header class="site-header">
      <nav class="nav container">
        <a class="brand" href="#home" @click="menuOpen = false">
          CL<span>.</span>
        </a>

        <button
            class="menu-toggle"
            type="button"
            :aria-expanded="menuOpen"
            aria-label="Toggle navigation"
            @click="menuOpen = !menuOpen"
        >
          {{ menuOpen ? '✕' : '☰' }}
        </button>

        <div class="nav-links" :class="{ 'nav-open': menuOpen }">
          <a
              v-for="item in navItems"
              :key="item.href"
              :href="item.href"
              @click="menuOpen = false"
          >
            {{ item.label }}
          </a>
          <a class="nav-contact" href="#contact" @click="menuOpen = false">
            Let's Talk <span>↗</span>
          </a>
        </div>
      </nav>
    </header>

    <main>
      <!-- Hero -->
      <section id="home" class="hero section container">
        <div class="hero-copy">
          <p class="eyebrow"><span class="status-dot"></span> COMPUTER ENGINEERING STUDENT</p>

          <h1>
            Hello, I'm<br />
            <span>Chesterton</span><br />
            Lawrence Leal.
          </h1>

          <p class="hero-description">
            I build, design, and explore solutions through programming,
            electronics, and creative engineering.
          </p>

          <div class="hero-actions">
            <a href="#projects" class="button button-primary">
              Explore My Work <span>↗</span>
            </a>
            <a href="#contact" class="button button-outline">
              Contact Me
            </a>
          </div>

          <div class="hero-location">
            <span>⌖</span> Aurora, Alicia, Isabela, Philippines
          </div>
        </div>

        <div class="hero-visual">
          <div class="visual-backdrop"></div>
          <div class="photo-frame">
            <img
                src="/Profilepic.jpg"
                alt="Portrait of Chesterton Lawrence Leal"
                class="profile-photo"
                @error="($event.target as HTMLImageElement).style.display = 'none'"
            />
            <div class="photo-fallback">
              <span>CL</span>
              <small>Computer Engineering</small>
            </div>
          </div>

          <div class="floating-card card-top">
            <span class="floating-icon">⌘</span>
            <div>
              <strong>Problem Solver</strong>
              <small>Build. Test. Improve.</small>
            </div>
          </div>

          <div class="floating-card card-bottom">
            <span class="floating-icon">⚡</span>
            <div>
              <strong>Electronics & Code</strong>
              <small>Turning ideas into projects</small>
            </div>
          </div>

          <span class="decorative-circle"></span>
        </div>
      </section>

      <!-- Quick facts -->
      <section class="quick-facts container">
        <div>
          <strong>05<span>+</span></strong>
          <small>Featured Projects</small>
        </div>
        <div>
          <strong>08<span>+</span></strong>
          <small>Technical Tools & Languages</small>
        </div>
        <div>
          <strong>03<span>rd</span></strong>
          <small>Year Computer Engineering</small>
        </div>
      </section>

      <!-- About -->
      <section id="about" class="section container">
        <div class="section-heading">
          <p class="eyebrow">GET TO KNOW ME</p>
          <h2>About <span>Me</span></h2>
        </div>

        <div class="about-grid">
          <div class="about-mark">
            <span>CL.</span>
            <p>Curious mind.<br />Practical solutions.</p>
          </div>

          <div class="about-content">
            <h3>
              An aspiring engineer with an interest in
              <span>technology and innovation.</span>
            </h3>
            <p>
              I am a Computer Engineering student at Cagayan State University
              – Carig Campus. I have experience in programming, electronics,
              CAD modelling, and collaborative project development.
            </p>
            <p>
              I enjoy exploring how software and hardware work together,
              from developing applications to building and testing electronic
              circuits and microcontroller-based systems.
            </p>
            <div class="about-details">
              <div>
                <small>UNIVERSITY</small>
                <strong>Cagayan State University</strong>
              </div>
              <div>
                <small>DEGREE</small>
                <strong>BS Computer Engineering</strong>
              </div>
              <div>
                <small>INTERESTS</small>
                <strong>Software, Electronics & IoT</strong>
              </div>
              <div>
                <small>LOCATION</small>
                <strong>Isabela, Philippines</strong>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Experience -->
      <section id="experience" class="section experience-section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">MY BACKGROUND</p>
            <h2>Learning Through <span>Experience</span></h2>
            <p class="section-description">
              Skills developed through academic activities, technical
              exercises, and collaborative projects.
            </p>
          </div>

          <div class="experience-list">
            <article class="experience-item">
              <span class="experience-number">01</span>
              <div>
                <h3>Programming & Software Development</h3>
                <p>
                  Practiced C, C++, Java, and Python programming, including
                  problem-solving, algorithm development, and web development.
                </p>
              </div>
              <span class="experience-tag">Software</span>
            </article>

            <article class="experience-item">
              <span class="experience-number">02</span>
              <div>
                <h3>CAD Design & Technical Drawing</h3>
                <p>
                  Created floor plans and interior and exterior perspectives
                  using AutoCAD and manual architectural drawing techniques.
                </p>
              </div>
              <span class="experience-tag">CAD</span>
            </article>

            <article class="experience-item">
              <span class="experience-number">03</span>
              <div>
                <h3>Electronics & Circuit Simulation</h3>
                <p>
                  Built circuits using Multisim, worked with microcontrollers,
                  and explored hardware testing and troubleshooting.
                </p>
              </div>
              <span class="experience-tag">Hardware</span>
            </article>

            <article class="experience-item">
              <span class="experience-number">04</span>
              <div>
                <h3>Collaborative Engineering Projects</h3>
                <p>
                  Worked with fellow students to plan and develop an
                  IoT-based automated vertical farming system.
                </p>
              </div>
              <span class="experience-tag">Teamwork</span>
            </article>
          </div>
        </div>
      </section>

      <!-- Projects -->
      <section id="projects" class="section container">
        <div class="section-heading project-heading">
          <div>
            <p class="eyebrow">SELECTED WORK</p>
            <h2>My <span>Projects</span></h2>
          </div>
          <p class="section-description">
            A collection of academic projects and practical engineering work.
          </p>
        </div>

        <div class="project-grid">
          <article
              v-for="project in projects"
              :key="project.number"
              class="project-card"
          >
            <div class="project-card-top">
              <span class="project-number">{{ project.number }}</span>
              <span class="project-arrow">↗</span>
            </div>

            <p class="project-category">{{ project.category }}</p>
            <h3>{{ project.title }}</h3>
            <p class="project-description">{{ project.description }}</p>

            <div class="tag-list">
              <span v-for="tag in project.tags" :key="tag">
                {{ tag }}
              </span>
            </div>
          </article>
        </div>
      </section>

      <!-- Skills -->
      <section id="skills" class="section skills-section">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">WHAT I WORK WITH</p>
            <h2>Technical <span>Skills</span></h2>
            <p class="section-description">
              Tools and technologies I have worked with in my studies and
              projects.
            </p>
          </div>

          <div class="skills-grid">
            <article
                v-for="(skill, index) in skills"
                :key="skill.title"
                class="skill-card"
            >
              <span class="skill-index">
                {{ String(index + 1).padStart(2, '0') }}
              </span>
              <h3>{{ skill.title }}</h3>
              <p>{{ skill.items }}</p>
            </article>
          </div>
        </div>
      </section>

      <!-- Education -->
      <section id="education" class="section container">
        <div class="section-heading">
          <p class="eyebrow">MY ACADEMIC JOURNEY</p>
          <h2><span>Education</span></h2>
        </div>

        <div class="education-list">
          <article class="education-item">
            <div class="education-marker"></div>
            <div class="education-body">
              <p class="education-date">2023 — PRESENT</p>
              <h3>Cagayan State University – Carig Campus</h3>
              <p>Bachelor of Science in Computer Engineering</p>
              <small>Tuguegarao City, Cagayan</small>
            </div>
          </article>

          <article class="education-item">
            <div class="education-marker"></div>
            <div class="education-body">
              <p class="education-date">2021 — 2023</p>
              <h3>Northeast Luzon Adventist College – SHS</h3>
              <p>Science, Technology, Engineering, and Mathematics</p>
              <small>Alicia, Isabela</small>
            </div>
          </article>
        </div>
      </section>

      <!-- Contact -->
      <section id="contact" class="contact-section">
        <div class="container contact-inner">
          <p class="eyebrow">LET'S CONNECT</p>
          <h2>Have an idea?<br /><span>Let's talk.</span></h2>
          <p class="contact-description">
            I'm open to learning opportunities, collaboration, and
            conversations about technology and engineering.
          </p>

          <a
              class="button button-light"
              href="mailto:lealchestertonlawrence@gmail.com"
          >
            Email Me <span>↗</span>
          </a>

          <div class="contact-details">
            <a href="mailto:lealchestertonlawrence@gmail.com">
              lealchestertonlawrence@gmail.com
            </a>
            <a href="tel:+639214094143">+63 921 409 1437</a>
            <span>Aurora, Alicia, Isabela</span>
          </div>
        </div>
      </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
      <div class="container footer-inner">
        <a class="brand" href="#home">CL<span>.</span></a>
        <p>Designed & built by Chesterton Lawrence Leal.</p>
        <a href="#home" class="back-top">Back to top ↑</a>
      </div>
    </footer>
  </div>
</template>
