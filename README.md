<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portofolio Saya</title>
  <style>
    body {
      margin: 0;
      font-family: "Segoe UI", sans-serif;
      background: #f7f9fc;
      color: #333;
      scroll-behavior: smooth;
    }

    header {
      background: #2d3e50;
      padding: 20px;
      color: white;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 999;
    }

    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
    }

    section {
      padding: 60px 20px;
      max-width: 900px;
      margin: auto;
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s ease;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h1, h2 {
      text-align: center;
    }

    .project {
      background: white;
      padding: 20px;
      margin: 20px 0;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      border-radius: 10px;
    }

    footer {
      background: #2d3e50;
      color: white;
      text-align: center;
      padding: 30px 20px;
    }

    @media (max-width: 600px) {
      nav a {
        display: block;
        margin: 10px 0;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Portofolio Saya</h1>
    <nav>
      <a href="#about">Tentang Saya</a>
      <a href="#projects">Proyek</a>
      <a href="#contact">Kontak</a>
    </nav>
  </header>

  <section id="about">
    <h2>Tentang Saya</h2>
    <p>Saya adalah pengembang web yang antusias dan kreatif. Saya suka membuat website responsif, interaktif, dan menarik secara visual.</p>
  </section>

  <section id="projects">
    <h2>Proyek Saya</h2>
    <div class="project">
      <h3>Website Toko Online</h3>
      <p>Menggunakan HTML, CSS, dan JavaScript untuk membuat halaman e-commerce sederhana.</p>
    </div>
    <div class="project">
      <h3>Aplikasi To-Do List</h3>
      <p>Frontend interaktif dengan JavaScript. Tambah, hapus, dan simpan daftar tugas.</p>
    </div>
  </section>

  <section id="contact">
    <h2>Hubungi Saya</h2>
    <p>Email: kamu@example.com</p>
    <p>Instagram: @kamu</p>
  </section>

  <footer>
    &copy; 2025 Nama Kamu. Dibuat dengan cinta.
  </footer>

  <script>
    const sections = document.querySelectorAll("section");
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add("visible");
        }
      });
    }, { threshold: 0.1 });

    sections.forEach(section => observer.observe(section));
  </script>

</body>
</html>
