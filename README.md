<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Amir | Frontend Developer</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    body { background:#f8f9fa; color:#212529; scroll-behavior:smooth; font-family: Arial, sans-serif; }
    .navbar { background:#0d6efd; }
    .navbar-brand { color:#fff; font-weight:bold; }
    .hero { min-height:80vh; display:flex; align-items:center; background:#e9ecef; }
    .hero h1 span { color:#0d6efd; }
    .hero-img { border-radius:10px; box-shadow:0 10px 20px rgba(0,0,0,0.2); }
    .section { padding:80px 0; }
    .section-title { font-weight:700; margin-bottom:40px; color:#0d6efd; text-align:center; }
    .card-custom { border:none; border-radius:10px; transition:0.3s; }
    .card-custom:hover { transform:translateY(-5px); box-shadow:0 10px 20px rgba(0,0,0,0.2); }
    .progress { height:15px; border-radius:5px; }
    .progress-bar { font-weight: bold; }
    footer { background:#0d6efd; padding:20px 0; color:#fff; text-align:center; }
  </style>
</head>
<body>

<nav class="navbar navbar-expand-lg navbar-dark fixed-top">
  <div class="container">
    <a class="navbar-brand" href="#">Amir.dev</a>
  </div>
</nav>

<section class="hero">
  <div class="container">
    <div class="row align-items-center">
      <div class="col-md-6">
        <h1 class="display-4 fw-bold">Salom, men <span>Amir</span></h1>
        <p class="lead">Frontend Developer, modern web saytlar yarataman.</p>
      </div>
      <div class="col-md-6 text-center">
        <img src="https://picsum.photos/id/1005/400/300" class="img-fluid hero-img" alt="Workspace">
      </div>
    </div>
  </div>
</section>

<section id="skills" class="section">
  <div class="container">
    <h2 class="section-title">Skills</h2>
    <div class="row text-center">
      <div class="col-md-3 mb-3">
        <h5>HTML</h5>
        <div class="progress">
          <div class="progress-bar bg-primary" style="width:90%">90%</div>
        </div>
      </div>
      <div class="col-md-3 mb-3">
        <h5>CSS</h5>
        <div class="progress">
          <div class="progress-bar bg-success" style="width:85%">85%</div>
        </div>
      </div>
      <div class="col-md-3 mb-3">
        <h5>JavaScript</h5>
        <div class="progress">
          <div class="progress-bar bg-warning" style="width:80%">80%</div>
        </div>
      </div>
      <div class="col-md-3 mb-3">
        <h5>Bootstrap</h5>
        <div class="progress">
          <div class="progress-bar bg-info" style="width:90%">90%</div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="projects" class="section">
  <div class="container">
    <h2 class="section-title">Projects</h2>
    <div class="row g-4" id="projectsContainer">
    </div>
  </div>
</section>

<footer>
  © 2026 Amir | Frontend Developer
</footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
<script>
const projects = [
  {
    title: "Calculator App",
    description: "JavaScript asosida yaratilgan kalkulyator.",
    image: "https://picsum.photos/id/1011/400/250",
    github: "#",
    demo: "#"
  },
  {
    title: "Weather App",
    description: "Ob-havo ma'lumotlarini ko'rsatadigan app.",
    image: "https://picsum.photos/id/1012/400/250",
    github: "#",
    demo: "#"
  },
  {
    title: "Portfolio Website",
    description: "O'z portfolio saytini yaratish.",
    image: "https://picsum.photos/id/1013/400/250",
    github: "#",
    demo: "#"
  }
];

const container = document.getElementById('projectsContainer');
projects.forEach(p => {
  const card = document.createElement('div');
  card.className = 'col-md-4';
  card.innerHTML = `
    <div class="card card-custom">
      <img src="${p.image}" class="card-img-top" alt="${p.title}">
      <div class="card-body">
        <h5 class="card-title">${p.title}</h5>
        <p class="card-text">${p.description}</p>
        <a href="${p.github}" target="_blank" class="btn btn-outline-primary me-2">GitHub</a>
        <a href="${p.demo}" target="_blank" class="btn btn-primary">Live Demo</a>
      </div>
    </div>
  `;
  container.appendChild(card);
});
</script>

</body>
</html>
