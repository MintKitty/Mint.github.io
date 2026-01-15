<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mon Portfolio Furry</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', -apple-system, sans-serif;
      background: linear-gradient(135deg, #0c0c0c 0%, #1a0f2e 50%, #2a1b3d 100%);
      color: #f0f0f0;
      margin: 0;
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* MODAL PLEIN ÉCRAN */
    .modal {
      display: none;
      position: fixed;
      z-index: 1000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.95);
      backdrop-filter: blur(10px);
    }

    .modal-content {
      position: relative;
      width: 100%;
      height: 100%;
      max-width: 95vw;
      max-height: 90vh;
      margin: auto;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      display: flex;
      align-items: center;
      justify-content: center;
      animation: modalSlideIn 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    }

    @keyframes modalSlideIn {
      from { opacity: 0; transform: translate(-50%, -60%); }
      to { opacity: 1; transform: translate(-50%, -50%); }
    }

    .modal img {
      width: auto;
      max-width: 95vw;
      height: auto;
      max-height: 85vh;
      object-fit: contain;
      object-position: center;
      border-radius: 16px;
      box-shadow: 0 30px 80px rgba(0,0,0,0.9);
      display: block;
      margin: 0 auto;
    }

    .modal-info {
      position: absolute;
      bottom: 20px;
      left: 20px;
      right: 20px;
      background: rgba(26, 26, 44, 0.9);
      backdrop-filter: blur(15px);
      padding: 20px;
      border-radius: 16px;
      border: 1px solid rgba(74, 144, 226, 0.3);
    }

    .close-modal {
      position: absolute;
      top: 20px;
      right: 30px;
      color: #f0f0f0;
      font-size: 40px;
      font-weight: bold;
      cursor: pointer;
      z-index: 1001;
      background: rgba(74, 144, 226, 0.2);
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.3s ease;
    }

    .close-modal:hover {
      background: rgba(74, 144, 226, 0.4);
      transform: scale(1.1);
    }

    .nav-arrow {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      background: rgba(74, 144, 226, 0.3);
      color: white;
      border: none;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      font-size: 24px;
      cursor: pointer;
      transition: all 0.3s ease;
      backdrop-filter: blur(10px);
    }

    .nav-arrow:hover {
      background: rgba(74, 144, 226, 0.6);
      transform: translateY(-50%) scale(1.1);
    }

    .prev { left: 30px; }
    .next { right: 30px; }

    /* HEADER */
    header {
      text-align: center;
      padding: 40px 20px;
      background: rgba(0,0,0,0.3);
      backdrop-filter: blur(10px);
    }

    h1 {
      font-size: 2.5em;
      font-weight: 700;
      background: linear-gradient(135deg, #ff6b9d, #4a90e2, #00d4ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin: 0 0 10px 0;
    }

    /* UPLOAD ZONE */
    .upload-zone {
      max-width: 900px;
      margin: 0 auto;
      padding: 30px;
      background: rgba(26, 26, 44, 0.8);
      backdrop-filter: blur(15px);
      border-radius: 20px;
      margin: 20px;
      border: 1px solid rgba(74, 144, 226, 0.3);
      box-shadow: 0 20px 40px rgba(0,0,0,0.5);
    }

    .upload-form {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr auto;
      gap: 15px;
      align-items: end;
    }

    input, select, textarea {
      padding: 12px 16px;
      border: 2px solid rgba(74, 144, 226, 0.3);
      background: rgba(15, 15, 30, 0.9);
      color: #f0f0f0;
      border-radius: 12px;
      font-size: 14px;
      transition: all 0.3s ease;
    }

    input:focus, select:focus, textarea:focus {
      outline: none;
      border-color: #4a90e2;
      box-shadow: 0 0 20px rgba(74, 144, 226, 0.3);
    }

    textarea {
      grid-column: 1 / -1;
      resize: vertical;
      min-height: 80px;
    }

    button {
      padding: 12px 24px;
      background: linear-gradient(135deg, #4a90e2, #357abd);
      border: none;
      color: white;
      border-radius: 12px;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 8px 20px rgba(74, 144, 226, 0.4);
    }

    button:hover {
      transform: translateY(-2px);
      box-shadow: 0 12px 30px rgba(74, 144, 226, 0.6);
    }

    /* TABS */
    .tabs {
      max-width: 900px;
      margin: 0 auto 20px;
      padding: 10px;
      display: flex;
      justify-content: center;
      gap: 8px;
      flex-wrap: wrap;
    }

    .tab {
      padding: 10px 20px;
      background: rgba(51, 51, 77, 0.7);
      border: 1px solid rgba(74, 144, 226, 0.3);
      color: #f0f0f0;
      cursor: pointer;
      border-radius: 25px;
      font-size: 14px;
      font-weight: 500;
      transition: all 0.3s ease;
      backdrop-filter: blur(10px);
    }

    .tab.active, .tab:hover {
      background: linear-gradient(135deg, #4a90e2, #357abd);
      transform: translateY(-2px);
      box-shadow: 0 8px 20px rgba(74, 144, 226, 0.4);
    }

    /* GALERIE */
    .gallery {
      max-width: 1400px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 25px;
      padding: 30px;
    }

    .gallery-item {
      border-radius: 20px;
      overflow: hidden;
      background: rgba(26, 26, 44, 0.9);
      border: 1px solid rgba(74, 144, 226, 0.2);
      box-shadow: 0 15px 40px rgba(0,0,0,0.6);
      opacity: 1;
      transform: translateY(0);
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      position: relative;
      cursor: pointer;
    }

    .gallery-item.hidden {
      display: none !important;
    }

    .gallery-item:hover {
      transform: translateY(-8px) scale(1.02);
      box-shadow: 0 20px 50px rgba(74, 144, 226, 0.3);
    }

    .gallery-item img {
      width: 100%;
      height: 220px;
      object-fit: cover;
      object-position: center;
      display: block;
      transition: transform 0.3s ease;
    }

    .gallery-item:hover img {
      transform: scale(1.05);
    }

    .category {
      position: absolute;
      top: 12px;
      left: 12px;
      padding: 6px 12px;
      background: linear-gradient(135deg, rgba(74,144,226,0.9), rgba(255,107,157,0.9));
      color: white;
      font-size: 11px;
      font-weight: 700;
      border-radius: 20px;
      backdrop-filter: blur(10px);
    }

    .desc {
      padding: 15px;
      text-align: center;
      font-size: 14px;
      font-weight: 500;
    }

    @media (max-width: 768px) {
      .upload-form {
        grid-template-columns: 1fr;
      }
      h1 {
        font-size: 2em;
      }
      .gallery {
        grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
        gap: 20px;
        padding: 20px;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>✨ Mon Portfolio Furry ✨</h1>
    <p>Ref sheets • Headshots • Animations • PFP • Bannière • Stickers</p>
  </header>

  <section class="upload-zone">
    <div class="upload-form">
      <input type="file" id="imageInput" accept="image/*">
      <input type="text" id="imageTitle" placeholder="Titre de l'image">
      <select id="imageCategory">
        <option value="ref-sheet">📋 Ref Sheet</option>
        <option value="headshot">👤 Headshot</option>
        <option value="animation">🎬 Animation</option>
        <option value="pfp">🖼️ Photo Profil</option>
        <option value="banner">📱 Bannière</option>
        <option value="stickers">🎨 Stickers</option>  <!-- ✅ NOUVEAU -->
      </select>
      <textarea id="imageDesc" placeholder="Description détaillée"></textarea>
      <button onclick="addImage()">➕ Ajouter</button>
    </div>
  </section>

  <section class="tabs">
    <button class="tab active" data-category="all" onclick="filterGallery('all')">🎨 Toutes</button>
    <button class="tab" data-category="ref-sheet" onclick="filterGallery('ref-sheet')">📋 Ref Sheet</button>
    <button class="tab" data-category="headshot" onclick="filterGallery('headshot')">👤 Headshot</button>
    <button class="tab" data-category="animation" onclick="filterGallery('animation')">🎬 Animation</button>
    <button class="tab" data-category="pfp" onclick="filterGallery('pfp')">🖼️ PFP</button>
    <button class="tab" data-category="banner" onclick="filterGallery('banner')">📱 Bannière</button>
    <button class="tab" data-category="stickers" onclick="filterGallery('stickers')">🎨 Stickers</button>  <!-- ✅ NOUVEAU -->
  </section>

  <section id="gallery" class="gallery"></section>

  <div id="imageModal" class="modal">
    <span class="close-modal" onclick="closeModal()">&times;</span>
    <button class="nav-arrow prev" onclick="changeImage(-1)">❮</button>
    <button class="nav-arrow next" onclick="changeImage(1)">❯</button>
    <div class="modal-content" id="modalContent"></div>
  </div>

  <script>
    let allImages = [];
    let currentModalIndex = 0;
    let currentFilter = 'all';

    function addImage() {
      const input = document.getElementById('imageInput');
      const titleInput = document.getElementById('imageTitle');
      const categoryInput = document.getElementById('imageCategory');
      const descInput = document.getElementById('imageDesc');
      const file = input.files[0];

      if (!file) {
        alert("Choisis une image ! 😺");
        return;
      }

      const reader = new FileReader();
      const now = new Date().toLocaleDateString('fr-FR');

      reader.onload = function(event) {
        const imageData = {
          src: event.target.result,
          title: titleInput.value || 'Sans titre',
          category: categoryInput.value,
          description: descInput.value || '',
          date: now,
          id: Date.now()
        };

        allImages.push(imageData);
        renderGallery();
        filterGallery(currentFilter);

        input.value = '';
        titleInput.value = '';
        descInput.value = '';
      };

      reader.readAsDataURL(file);
    }

    function renderGallery() {
      const gallery = document.getElementById('gallery');
      gallery.innerHTML = '';

      allImages.forEach((image, index) => {
        const item = document.createElement('div');
        item.className = 'gallery-item';
        item.dataset.category = image.category;
        item.dataset.index = index;
        item.onclick = () => openModal(index);

        const catDiv = document.createElement('div');
        catDiv.className = 'category';
        catDiv.textContent = getCategoryEmoji(image.category) + ' ' + 
          image.category.replace('-', ' ').replace(/\b\w/g, l => l.toUpperCase());

        const img = document.createElement('img');
        img.src = image.src;
        img.alt = image.title;

        const desc = document.createElement('div');
        desc.className = 'desc';
        desc.innerHTML = `<strong>${image.title}</strong><br><small>${image.date}</small>`;

        item.appendChild(catDiv);
        item.appendChild(img);
        item.appendChild(desc);
        gallery.appendChild(item);
      });
    }

    function filterGallery(category) {
      currentFilter = category;
      
      document.querySelectorAll('.tab').forEach(tab => {
        tab.classList.remove('active');
        if (tab.dataset.category === category) {
          tab.classList.add('active');
        }
      });

      document.querySelectorAll('.gallery-item').forEach(item => {
        if (category === 'all' || item.dataset.category === category) {
          item.classList.remove('hidden');
        } else {
          item.classList.add('hidden');
        }
      });
    }

    function openModal(index) {
      currentModalIndex = index;
      document.getElementById('imageModal').style.display = 'block';
      showModalImage();
    }

    function closeModal() {
      document.getElementById('imageModal').style.display = 'none';
    }

    function showModalImage() {
      const image = allImages[currentModalIndex];
      const modalContent = document.getElementById('modalContent');
      
      modalContent.innerHTML = `
        <img src="${image.src}" alt="${image.title}">
        <div class="modal-info">
          <h3>${image.title}</h3>
          <p>${image.description || 'Pas de description'}</p>
          <small>📅 ${image.date} | ${getCategoryEmoji(image.category)} ${image.category.replace('-', ' ').toUpperCase()}</small>
        </div>
      `;
    }

    function changeImage(direction) {
      currentModalIndex += direction;
      if (currentModalIndex >= allImages.length) currentModalIndex = 0;
      if (currentModalIndex < 0) currentModalIndex = allImages.length - 1;
      showModalImage();
    }

    function getCategoryEmoji(category) {
      const emojis = {
        'ref-sheet': '📋', 
        'headshot': '👤', 
        'animation': '🎬', 
        'pfp': '🖼️', 
        'banner': '📱',
        'stickers': '🎨'  // ✅ NOUVEAU
      };
      return emojis[category] || '🖼️';
    }

    window.onclick = function(event) {
      const modal = document.getElementById('imageModal');
      if (event.target == modal) closeModal();
    }

    document.addEventListener('keydown', function(event) {
      if (event.key === 'Escape') closeModal();
    });
  </script>
</body>
</html>
