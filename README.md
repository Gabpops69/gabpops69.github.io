[index (1).html](https://github.com/user-attachments/files/32028474/index.1.html)
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Top 5</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,400&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #241726;<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Top 5</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,400&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #241726;
    --panel: #2f1d33;
    --panel-light: #3a2540;
    --gold: #c9a24b;
    --gold-soft: #a98a4a;
    --cream: #f3eadd;
    --cream-solid: #f3eadd;
    --mauve: #a488a3;
    --mauve-dim: #6f5a71;
    --rule: rgba(243, 234, 221, 0.14);
  }

  * { box-sizing: border-box; }

  html, body {
    margin: 0;
    padding: 0;
    background: var(--ink);
    color: var(--cream-solid);
    font-family: 'Inter', sans-serif;
    min-height: 100vh;
  }

  body {
    display: flex;
    justify-content: center;
    padding: 72px 24px 100px;
    background-image:
      radial-gradient(ellipse 900px 500px at 50% -10%, rgba(201, 162, 75, 0.10), transparent);
  }

  main {
    width: 100%;
    max-width: 620px;
  }

  .masthead {
    text-align: center;
    margin-bottom: 56px;
  }

  .kicker {
    font-size: 13px;
    color: var(--mauve);
    letter-spacing: 0.02em;
    margin: 0 0 14px;
  }

  h1 {
    font-family: 'Fraunces', serif;
    font-weight: 500;
    font-size: clamp(40px, 8vw, 58px);
    line-height: 1.02;
    margin: 0 0 16px;
    color: var(--cream-solid);
  }

  .subhead {
    font-size: 15.5px;
    color: var(--mauve);
    line-height: 1.6;
    max-width: 380px;
    margin: 0 auto;
  }

  .tabs {
    margin-top: 26px;
    display: flex;
    justify-content: center;
    gap: 28px;
  }

  .tab {
    font-family: 'Inter', sans-serif;
    font-size: 13.5px;
    color: var(--gold);
    text-decoration: none;
    border-bottom: 1px solid var(--gold-soft);
    padding-bottom: 3px;
    letter-spacing: 0.01em;
    transition: opacity 0.2s ease;
  }

  .tab:hover {
    opacity: 0.72;
  }

  .list {
    border-top: 1px solid var(--rule);
  }

  .row {
    display: grid;
    grid-template-columns: 76px 1fr;
    align-items: start;
    gap: 4px 20px;
    padding: 26px 4px;
    border-bottom: 1px solid var(--rule);
    position: relative;
    transition: background 0.2s ease;
  }

  .row:hover {
    background: rgba(243, 234, 221, 0.025);
  }

  .rank {
    font-family: 'Fraunces', serif;
    font-weight: 500;
    font-style: italic;
    font-size: 48px;
    line-height: 1;
    color: var(--gold);
    padding-top: 2px;
  }

  .row-fields {
    display: flex;
    flex-direction: column;
    gap: 8px;
    padding-top: 6px;
  }

  .field-title {
    font-family: 'Fraunces', serif;
    font-size: 22px;
    font-weight: 500;
    color: var(--cream-solid);
    background: transparent;
    border: none;
    border-bottom: 1px dashed var(--mauve-dim);
    padding: 2px 0 8px;
    width: 100%;
    outline: none;
  }

  .field-title::placeholder {
    color: var(--mauve-dim);
    font-style: italic;
  }

  .field-title:focus {
    border-bottom-color: var(--gold);
  }

  .field-note {
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    color: var(--mauve);
    background: transparent;
    border: none;
    padding: 2px 0;
    width: 100%;
    outline: none;
  }

  .field-note::placeholder {
    color: var(--mauve-dim);
  }

  .footer {
    margin-top: 44px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 18px;
  }

  .save-status {
    font-size: 13px;
    color: var(--mauve-dim);
    min-width: 90px;
  }

  button.reset {
    font-family: 'Inter', sans-serif;
    font-size: 13.5px;
    color: var(--mauve);
    background: transparent;
    border: 1px solid var(--mauve-dim);
    border-radius: 3px;
    padding: 9px 18px;
    cursor: pointer;
    transition: border-color 0.2s ease, color 0.2s ease;
  }

  button.reset:hover {
    border-color: var(--gold);
    color: var(--gold);
  }

  @media (max-width: 480px) {
    .row { grid-template-columns: 52px 1fr; }
    .rank { font-size: 36px; }
    .field-title { font-size: 19px; }
  }

  @media (prefers-reduced-motion: reduce) {
    * { transition: none !important; }
  }
</style>
</head>
<body>
<main>
  <div class="masthead">
    <p class="kicker">Classement</p>
    <h1>Top 5</h1>
    <p class="subhead">Cinq emplacements, encore vides. Clique sur une ligne pour écrire un titre et, si tu veux, une courte note.</p>
    <nav class="tabs">
      <a class="tab" href="archives.html" target="_blank" rel="noopener">Archives</a>
      <a class="tab" href="photo.html">Photo</a>
    </nav>
  </div>

  <div class="list" id="list">
    <!-- rows injected by JS -->
  </div>

  <div class="footer">
    <span class="save-status" id="status">&nbsp;</span>
    <button class="reset" id="resetBtn">Réinitialiser</button>
  </div>
</main>

<script>
  const STORAGE_KEY = 'top5-ranking';
  const list = document.getElementById('list');
  const statusEl = document.getElementById('status');
  const resetBtn = document.getElementById('resetBtn');

  const romanRanks = ['I', 'II', 'III', 'IV', 'V'];

  function loadData() {
    try {
      const raw = localStorage.getItem(STORAGE_KEY);
      if (raw) return JSON.parse(raw);
    } catch (e) {}
    return [0, 1, 2, 3, 4].map(() => ({ title: '', note: '' }));
  }

  function saveData(data) {
    try {
      localStorage.setItem(STORAGE_KEY, JSON.stringify(data));
      statusEl.textContent = 'Enregistré';
      clearTimeout(saveData._t);
      saveData._t = setTimeout(() => { statusEl.textContent = ''; }, 1400);
    } catch (e) {}
  }

  let data = loadData();

  function render() {
    list.innerHTML = '';
    data.forEach((entry, i) => {
      const row = document.createElement('div');
      row.className = 'row';

      const rank = document.createElement('div');
      rank.className = 'rank';
      rank.textContent = romanRanks[i];

      const fields = document.createElement('div');
      fields.className = 'row-fields';

      const titleInput = document.createElement('input');
      titleInput.className = 'field-title';
      titleInput.type = 'text';
      titleInput.placeholder = 'À définir';
      titleInput.value = entry.title;
      titleInput.addEventListener('input', (e) => {
        data[i].title = e.target.value;
        saveData(data);
      });

      const noteInput = document.createElement('input');
      noteInput.className = 'field-note';
      noteInput.type = 'text';
      noteInput.placeholder = 'Ajouter une note (optionnel)';
      noteInput.value = entry.note;
      noteInput.addEventListener('input', (e) => {
        data[i].note = e.target.value;
        saveData(data);
      });

      fields.appendChild(titleInput);
      fields.appendChild(noteInput);
      row.appendChild(rank);
      row.appendChild(fields);
      list.appendChild(row);
    });
  }

  resetBtn.addEventListener('click', () => {
    data = [0, 1, 2, 3, 4].map(() => ({ title: '', note: '' }));
    saveData(data);
    render();
  });

  render();
</script>
</body>
</html>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Top 5</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,400&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #241726;
    --panel: #2f1d33;
    --panel-light: #3a2540;
    --gold: #c9a24b;
    --gold-soft: #a98a4a;
    --cream: #f3eadd;
    --cream-solid: #f3eadd;
    --mauve: #a488a3;
    --mauve-dim: #6f5a71;
    --rule: rgba(243, 234, 221, 0.14);
  }

  * { box-sizing: border-box; }

  html, body {
    margin: 0;
    padding: 0;
    background: var(--ink);
    color: var(--cream-solid);
    font-family: 'Inter', sans-serif;
    min-height: 100vh;
  }

  body {
    display: flex;
    justify-content: center;
    padding: 72px 24px 100px;
    background-image:
      radial-gradient(ellipse 900px 500px at 50% -10%, rgba(201, 162, 75, 0.10), transparent);
  }

  main {
    width: 100%;
    max-width: 620px;
  }

  .masthead {
    text-align: center;
    margin-bottom: 56px;
  }

  .kicker {
    font-size: 13px;
    color: var(--mauve);
    letter-spacing: 0.02em;
    margin: 0 0 14px;
  }

  h1 {
    font-family: 'Fraunces', serif;
    font-weight: 500;
    font-size: clamp(40px, 8vw, 58px);
    line-height: 1.02;
    margin: 0 0 16px;
    color: var(--cream-solid);
  }

  .subhead {
    font-size: 15.5px;
    color: var(--mauve);
    line-height: 1.6;
    max-width: 380px;
    margin: 0 auto;
  }

  .tabs {
    margin-top: 26px;
    display: flex;
    justify-content: center;
    gap: 28px;
  }

  .tab {
    font-family: 'Inter', sans-serif;
    font-size: 13.5px;
    color: var(--gold);
    text-decoration: none;
    border-bottom: 1px solid var(--gold-soft);
    padding-bottom: 3px;
    letter-spacing: 0.01em;
    transition: opacity 0.2s ease;
  }

  .tab:hover {
    opacity: 0.72;
  }

  .list {
    border-top: 1px solid var(--rule);
  }

  .row {
    display: grid;
    grid-template-columns: 76px 1fr;
    align-items: start;
    gap: 4px 20px;
    padding: 26px 4px;
    border-bottom: 1px solid var(--rule);
    position: relative;
    transition: background 0.2s ease;
  }

  .row:hover {
    background: rgba(243, 234, 221, 0.025);
  }

  .rank {
    font-family: 'Fraunces', serif;
    font-weight: 500;
    font-style: italic;
    font-size: 48px;
    line-height: 1;
    color: var(--gold);
    padding-top: 2px;
  }

  .row-fields {
    display: flex;
    flex-direction: column;
    gap: 8px;
    padding-top: 6px;
  }

  .field-title {
    font-family: 'Fraunces', serif;
    font-size: 22px;
    font-weight: 500;
    color: var(--cream-solid);
    background: transparent;
    border: none;
    border-bottom: 1px dashed var(--mauve-dim);
    padding: 2px 0 8px;
    width: 100%;
    outline: none;
  }

  .field-title::placeholder {
    color: var(--mauve-dim);
    font-style: italic;
  }

  .field-title:focus {
    border-bottom-color: var(--gold);
  }

  .field-note {
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    color: var(--mauve);
    background: transparent;
    border: none;
    padding: 2px 0;
    width: 100%;
    outline: none;
  }

  .field-note::placeholder {
    color: var(--mauve-dim);
  }

  .footer {
    margin-top: 44px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 18px;
  }

  .save-status {
    font-size: 13px;
    color: var(--mauve-dim);
    min-width: 90px;
  }

  button.reset {
    font-family: 'Inter', sans-serif;
    font-size: 13.5px;
    color: var(--mauve);
    background: transparent;
    border: 1px solid var(--mauve-dim);
    border-radius: 3px;
    padding: 9px 18px;
    cursor: pointer;
    transition: border-color 0.2s ease, color 0.2s ease;
  }

  button.reset:hover {
    border-color: var(--gold);
    color: var(--gold);
  }

  @media (max-width: 480px) {
    .row { grid-template-columns: 52px 1fr; }
    .rank { font-size: 36px; }
    .field-title { font-size: 19px; }
  }

  @media (prefers-reduced-motion: reduce) {
    * { transition: none !important; }
  }
</style>
</head>
<body>
<main>
  <div class="masthead">
    <p class="kicker">Classement</p>
    <h1>Top 5</h1>
    <p class="subhead">Cinq emplacements, encore vides. Clique sur une ligne pour écrire un titre et, si tu veux, une courte note.</p>
    <nav class="tabs">
      <a class="tab" href="archives.html" target="_blank" rel="noopener">Archives</a>
      <a class="tab" href="photo.html">Photo</a>
    </nav>
  </div>

  <div class="list" id="list">
    <!-- rows injected by JS -->
  </div>

  <div class="footer">
    <span class="save-status" id="status">&nbsp;</span>
    <button class="reset" id="resetBtn">Réinitialiser</button>
  </div>
</main>

<script>
  const STORAGE_KEY = 'top5-ranking';
  const list = document.getElementById('list');
  const statusEl = document.getElementById('status');
  const resetBtn = document.getElementById('resetBtn');

  const romanRanks = ['I', 'II', 'III', 'IV', 'V'];

  function loadData() {
    try {
      const raw = localStorage.getItem(STORAGE_KEY);
      if (raw) return JSON.parse(raw);
    } catch (e) {}
    return [0, 1, 2, 3, 4].map(() => ({ title: '', note: '' }));
  }

  function saveData(data) {
    try {
      localStorage.setItem(STORAGE_KEY, JSON.stringify(data));
      statusEl.textContent = 'Enregistré';
      clearTimeout(saveData._t);
      saveData._t = setTimeout(() => { statusEl.textContent = ''; }, 1400);
    } catch (e) {}
  }

  let data = loadData();

  function render() {
    list.innerHTML = '';
    data.forEach((entry, i) => {
      const row = document.createElement('div');
      row.className = 'row';

      const rank = document.createElement('div');
      rank.className = 'rank';
      rank.textContent = romanRanks[i];

      const fields = document.createElement('div');
      fields.className = 'row-fields';

      const titleInput = document.createElement('input');
      titleInput.className = 'field-title';
      titleInput.type = 'text';
      titleInput.placeholder = 'À définir';
      titleInput.value = entry.title;
      titleInput.addEventListener('input', (e) => {
        data[i].title = e.target.value;
        saveData(data);
      });

      const noteInput = document.createElement('input');
      noteInput.className = 'field-note';
      noteInput.type = 'text';
      noteInput.placeholder = 'Ajouter une note (optionnel)';
      noteInput.value = entry.note;
      noteInput.addEventListener('input', (e) => {
        data[i].note = e.target.value;
        saveData(data);
      });

      fields.appendChild(titleInput);
      fields.appendChild(noteInput);
      row.appendChild(rank);
      row.appendChild(fields);
      list.appendChild(row);
    });
  }

  resetBtn.addEventListener('click', () => {
    data = [0, 1, 2, 3, 4].map(() => ({ title: '', note: '' }));
    saveData(data);
    render();
  });

  render();
</script>
</body>
</html>

    --gold-soft: #a98a4a;
    --cream: #f3eadd;
    --cream-solid: #f3eadd;
    --mauve: #a488a3;
    --mauve-dim: #6f5a71;
    --rule: rgba(243, 234, 221, 0.14);
  }

  * { box-sizing: border-box; }

  html, body {
    margin: 0;
    padding: 0;
    background: var(--ink);
    color: var(--cream-solid);
    font-family: 'Inter', sans-serif;
    min-height: 100vh;
  }

  body {
    display: flex;
    justify-content: center;
    padding: 72px 24px 100px;
    background-image:
      radial-gradient(ellipse 900px 500px at 50% -10%, rgba(201, 162, 75, 0.10), transparent);
  }

  main {
    width: 100%;
    max-width: 620px;
  }

  .masthead {
    text-align: center;
    margin-bottom: 56px;
  }

  .kicker {
    font-size: 13px;
    color: var(--mauve);
    letter-spacing: 0.02em;
    margin: 0 0 14px;
  }

  h1 {
    font-family: 'Fraunces', serif;
    font-weight: 500;
    font-size: clamp(40px, 8vw, 58px);
    line-height: 1.02;
    margin: 0 0 16px;
    color: var(--cream-solid);
  }

  .subhead {
    font-size: 15.5px;
    color: var(--mauve);
    line-height: 1.6;
    max-width: 380px;
    margin: 0 auto;
  }

  .list {
    border-top: 1px solid var(--rule);
  }

  .row {
    display: grid;
    grid-template-columns: 76px 1fr;
    align-items: start;
    gap: 4px 20px;
    padding: 26px 4px;
    border-bottom: 1px solid var(--rule);
    position: relative;
    transition: background 0.2s ease;
  }

  .row:hover {
    background: rgba(243, 234, 221, 0.025);
  }

  .rank {
    font-family: 'Fraunces', serif;
    font-weight: 500;
    font-style: italic;
    font-size: 48px;
    line-height: 1;
    color: var(--gold);
    padding-top: 2px;
  }

  .row-fields {
    display: flex;
    flex-direction: column;
    gap: 8px;
    padding-top: 6px;
  }

  .field-title {
    font-family: 'Fraunces', serif;
    font-size: 22px;
    font-weight: 500;
    color: var(--cream-solid);
    background: transparent;
    border: none;
    border-bottom: 1px dashed var(--mauve-dim);
    padding: 2px 0 8px;
    width: 100%;
    outline: none;
  }

  .field-title::placeholder {
    color: var(--mauve-dim);
    font-style: italic;
  }

  .field-title:focus {
    border-bottom-color: var(--gold);
  }

  .field-note {
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    color: var(--mauve);
    background: transparent;
    border: none;
    padding: 2px 0;
    width: 100%;
    outline: none;
  }

  .field-note::placeholder {
    color: var(--mauve-dim);
  }

  .footer {
    margin-top: 44px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 18px;
  }

  .save-status {
    font-size: 13px;
    color: var(--mauve-dim);
    min-width: 90px;
  }

  button.reset {
    font-family: 'Inter', sans-serif;
    font-size: 13.5px;
    color: var(--mauve);
    background: transparent;
    border: 1px solid var(--mauve-dim);
    border-radius: 3px;
    padding: 9px 18px;
    cursor: pointer;
    transition: border-color 0.2s ease, color 0.2s ease;
  }

  button.reset:hover {
    border-color: var(--gold);
    color: var(--gold);
  }

  @media (max-width: 480px) {
    .row { grid-template-columns: 52px 1fr; }
    .rank { font-size: 36px; }
    .field-title { font-size: 19px; }
  }

  @media (prefers-reduced-motion: reduce) {
    * { transition: none !important; }
  }
</style>
</head>
<body>
<main>
  <div class="masthead">
    <p class="kicker">Classement</p>
    <h1>Top 5</h1>
    <p class="subhead"></p>
  </div>

  <div class="list" id="list">
    <!-- rows injected by JS -->
  </div>

  <div class="footer">
    <span class="save-status" id="status">&nbsp;</span>
    <button class="reset" id="resetBtn">Réinitialiser</button>
  </div>
</main>

<script>
  const STORAGE_KEY = 'top5-ranking';
  const list = document.getElementById('list');
  const statusEl = document.getElementById('status');
  const resetBtn = document.getElementById('resetBtn');

  const romanRanks = ['I', 'II', 'III', 'IV', 'V'];

  function loadData() {
    try {
      const raw = localStorage.getItem(STORAGE_KEY);
      if (raw) return JSON.parse(raw);
    } catch (e) {}
    return [0, 1, 2, 3, 4].map(() => ({ title: '', note: '' }));
  }

  function saveData(data) {
    try {
      localStorage.setItem(STORAGE_KEY, JSON.stringify(data));
      statusEl.textContent = 'Enregistré';
      clearTimeout(saveData._t);
      saveData._t = setTimeout(() => { statusEl.textContent = ''; }, 1400);
    } catch (e) {}
  }

  let data = loadData();

  function render() {
    list.innerHTML = '';
    data.forEach((entry, i) => {
      const row = document.createElement('div');
      row.className = 'row';

      const rank = document.createElement('div');
      rank.className = 'rank';
      rank.textContent = romanRanks[i];

      const fields = document.createElement('div');
      fields.className = 'row-fields';

      const titleInput = document.createElement('input');
      titleInput.className = 'field-title';
      titleInput.type = 'text';
      titleInput.placeholder = 'À définir';
      titleInput.value = entry.title;
      titleInput.addEventListener('input', (e) => {
        data[i].title = e.target.value;
        saveData(data);
      });

      const noteInput = document.createElement('input');
      noteInput.className = 'field-note';
      noteInput.type = 'text';
      noteInput.placeholder = 'Ajouter une note (optionnel)';
      noteInput.value = entry.note;
      noteInput.addEventListener('input', (e) => {
        data[i].note = e.target.value;
        saveData(data);
      });

      fields.appendChild(titleInput);
      fields.appendChild(noteInput);
      row.appendChild(rank);
      row.appendChild(fields);
      list.appendChild(row);
    });
  }

  resetBtn.addEventListener('click', () => {
    data = [0, 1, 2, 3, 4].map(() => ({ title: '', note: '' }));
    saveData(data);
    render();
  });

  render();
</script>
</body>
</html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Archives — Top 5</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,400&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #241726;
    --panel: #2f1d33;
    --gold: #c9a24b;
    --gold-soft: #a98a4a;
    --cream-solid: #f3eadd;
    --mauve: #a488a3;
    --mauve-dim: #6f5a71;
    --rule: rgba(243, 234, 221, 0.14);
  }

  * { box-sizing: border-box; }

  html, body {
    margin: 0;
    padding: 0;
    background: var(--ink);
    color: var(--cream-solid);
    font-family: 'Inter', sans-serif;
    min-height: 100vh;
  }

  body {
    display: flex;
    justify-content: center;
    padding: 72px 24px 100px;
    background-image:
      radial-gradient(ellipse 900px 500px at 50% -10%, rgba(201, 162, 75, 0.10), transparent);
  }

  main {
    width: 100%;
    max-width: 620px;
  }

  .masthead {
    text-align: center;
    margin-bottom: 56px;
  }

  .kicker {
    font-size: 13px;
    color: var(--mauve);
    margin: 0 0 14px;
  }

  h1 {
    font-family: 'Fraunces', serif;
    font-weight: 500;
    font-size: clamp(36px, 7vw, 50px);
    line-height: 1.05;
    margin: 0 0 16px;
    color: var(--cream-solid);
  }

  .subhead {
    font-size: 15.5px;
    color: var(--mauve);
    line-height: 1.6;
    max-width: 380px;
    margin: 0 auto;
  }

  .back {
    margin-top: 26px;
    display: flex;
    justify-content: center;
  }

  .back a {
    font-size: 13.5px;
    color: var(--gold);
    text-decoration: none;
    border-bottom: 1px solid var(--gold-soft);
    padding-bottom: 3px;
  }

  .back a:hover {
    opacity: 0.72;
  }

  .empty-panel {
    border-top: 1px solid var(--rule);
    border-bottom: 1px solid var(--rule);
    padding: 60px 20px;
    text-align: center;
  }

  .empty-panel p {
    font-family: 'Fraunces', serif;
    font-style: italic;
    font-size: 19px;
    color: var(--mauve);
    margin: 0;
  }
</style>
</head>
<body>
<main>
  <div class="masthead">
    <p class="kicker">Catégorie</p>
    <h1>Archives</h1>
    <p class="subhead">Les anciens classements viendront ici au fil du temps.</p>
    <div class="back">
      <a href="index.html">Retour au classement</a>
    </div>
  </div>

  <div class="empty-panel">
    <p>Rien à afficher pour l'instant.</p>
  </div>
</main>
</body>
</html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Photo — Top 5</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,400&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #241726;
    --gold: #c9a24b;
    --gold-soft: #a98a4a;
    --cream-solid: #f3eadd;
    --mauve: #a488a3;
    --mauve-dim: #6f5a71;
    --rule: rgba(243, 234, 221, 0.14);
  }

  * { box-sizing: border-box; }

  html, body {
    margin: 0;
    padding: 0;
    background: var(--ink);
    color: var(--cream-solid);
    font-family: 'Inter', sans-serif;
    min-height: 100vh;
  }

  body {
    display: flex;
    justify-content: center;
    padding: 72px 24px 100px;
    background-image:
      radial-gradient(ellipse 900px 500px at 50% -10%, rgba(201, 162, 75, 0.10), transparent);
  }

  main {
    width: 100%;
    max-width: 620px;
  }

  .masthead {
    text-align: center;
    margin-bottom: 44px;
  }

  .kicker {
    font-size: 13px;
    color: var(--mauve);
    margin: 0 0 14px;
  }

  h1 {
    font-family: 'Fraunces', serif;
    font-weight: 500;
    font-size: clamp(36px, 7vw, 50px);
    line-height: 1.05;
    margin: 0 0 16px;
    color: var(--cream-solid);
  }

  .subhead {
    font-size: 15.5px;
    color: var(--mauve);
    line-height: 1.6;
    max-width: 400px;
    margin: 0 auto;
  }

  .back {
    margin-top: 26px;
    display: flex;
    justify-content: center;
  }

  .back a {
    font-size: 13.5px;
    color: var(--gold);
    text-decoration: none;
    border-bottom: 1px solid var(--gold-soft);
    padding-bottom: 3px;
  }

  .back a:hover {
    opacity: 0.72;
  }

  .frame {
    border: 1px solid var(--rule);
    aspect-ratio: 4 / 3;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 24px;
  }

  .frame img {
    max-width: 100%;
    max-height: 100%;
    display: block;
  }

  .frame p {
    font-family: 'Fraunces', serif;
    font-style: italic;
    font-size: 18px;
    color: var(--mauve);
    margin: 0;
    max-width: 320px;
    line-height: 1.5;
  }
</style>
</head>
<body>
<main>
  <div class="masthead">
    <p class="kicker">Photo</p>
    <h1>Photo</h1>
    <p class="subhead">Remplace le cadre ci-dessous par ta propre image.</p>
    <div class="back">
      <a href="index.html">Retour au classement</a>
    </div>
  </div>

  <div class="frame">
    <!--
      Pour ajouter ta photo :
      1. Mets ton fichier image (ex : ma-photo.jpg) à la racine de ton dépôt,
         au même niveau que ce fichier photo.html.
      2. Remplace la ligne ci-dessous par :
         <img src="ma-photo.jpg" alt="Description de la photo">
      3. Tu peux ensuite supprimer le <p> juste en dessous.
    -->
    <img src="Lionel-Messi_0.jpg" alt="Messi le GOAT">
  </div>
</main>
</body>
</html>
