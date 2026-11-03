이 기획서대로 html css javascript가 모두 들어있는 html 파일 하나를 만들어줘. 외부 파일이나 서버 없이 브라우저에서 바로 열리게 하고, 화면 문구는 한국어로 써줘. 완성된 .html 파일로 제공해줘
나
📎
기획서.md
AI
나
이 기획서대로 html css javascript가 모두 들어있는 html 파일 하나를 만들어줘. 외부 파일이나 서버 없이 브라우저에서 바로 열리게 하고, 화면 문구는 한국어로 써줘. 완성된 .html 파일로 제공해줘
AI
좋아요! 다만 현재 대화에는 기획서 내용이 첨부되어 있지 않아서 어떤 화면/기능으로 만들어야 할지 알 수 없습니다.

아래 중 하나로 기획서를 보내주세요.

기획서 내용을 그대로 붙여넣기
이미지/문서 파일 업로드
핵심 요구사항을 간단히 정리해서 작성
예시로 이런 정보가 있으면 바로 제작할 수 있어요.

웹페이지 주제
화면 구성
버튼/입력창/메뉴 기능
색상이나 디자인 스타일
필요한 JavaScript 동작
반응형 지원 여부
기획서를 보내주시면 HTML + CSS + JavaScript가 모두 포함된 단일 .html 파일로 만들어서 다운로드 링크로 제공해드릴게요.

나
이 기획서대로 html css javascript가 모두 들어있는 html 파일 하나를 만들어줘. 외부 파일이나 서버 없이 브라우저에서 바로 열리게 하고, 화면 문구는 한국어로 써줘. 완성된 .html 파일로 제공해줘
AI
기획서 내용이 아직 대화에 첨부되지 않았어요. 😊
HTML 파일을 정확히 만들어드리려면 기획서 내용을 보내주세요.

아래 중 편한 방식으로 전달해 주세요.

기획서 파일 업로드
기획서 내용을 텍스트로 붙여넣기
핵심 요구사항만 정리해서 보내기
화면 구성
버튼/입력창 기능
색상/디자인 스타일
필요한 페이지 또는 섹션
JavaScript 동작
기획서를 보내주시면, HTML/CSS/JavaScript가 모두 포함된 단일 .html 파일로 만들어서 바로 다운로드할 수 있게 제공해드릴게요.

나
첨부 파일을 분석해주세요.
나
📎
기획서.md
AI
아래 내용을 그대로 복사해서 movie-tier-list.html 파일로 저장한 뒤, 브라우저에서 열면 바로 사용할 수 있습니다.
HTML/CSS/JavaScript가 모두 한 파일 안에 들어있고, 데이터는 브라우저 로컬스토리지에 저장됩니다.

html
📋 복사
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>영화 티어리스트</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: "Pretendard", "Noto Sans KR", Arial, sans-serif;
      background: #111827;
      color: #f9fafb;
    }

    header {
      padding: 28px 32px 18px;
      background: linear-gradient(135deg, #1f2937, #111827);
      border-bottom: 1px solid #374151;
    }

    header h1 {
      margin: 0;
      font-size: 32px;
    }

    header p {
      margin: 8px 0 0;
      color: #d1d5db;
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 24px 24px 48px;
    }

    .toolbar {
      display: flex;
      gap: 10px;
      align-items: center;
      margin-bottom: 20px;
      padding: 16px;
      background: #1f2937;
      border: 1px solid #374151;
      border-radius: 14px;
    }

    .toolbar input {
      flex: 1;
      padding: 12px 14px;
      border: 1px solid #4b5563;
      border-radius: 10px;
      background: #111827;
      color: #f9fafb;
      font-size: 15px;
      outline: none;
    }

    .toolbar input:focus {
      border-color: #60a5fa;
    }

    button {
      border: none;
      cursor: pointer;
      border-radius: 9px;
      font-weight: 700;
      transition: 0.15s;
    }

    button:hover {
      transform: translateY(-1px);
      opacity: 0.92;
    }

    .add-btn {
      padding: 12px 18px;
      background: #2563eb;
      color: white;
      font-size: 15px;
    }

    .reset-btn {
      padding: 12px 18px;
      background: #4b5563;
      color: white;
      font-size: 15px;
    }

    .notice {
      margin-bottom: 18px;
      padding: 12px 14px;
      background: #0f172a;
      border: 1px solid #334155;
      border-radius: 12px;
      color: #cbd5e1;
      font-size: 14px;
      line-height: 1.5;
    }

    .tier-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .tier-row {
      display: grid;
      grid-template-columns: 100px 1fr;
      min-height: 170px;
      border: 1px solid #374151;
      border-radius: 14px;
      overflow: hidden;
      background: #1f2937;
    }

    .tier-label {
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 38px;
      font-weight: 900;
      color: #111827;
      text-shadow: 0 1px 0 rgba(255,255,255,0.35);
    }

    .tier-s { background: #f87171; }
    .tier-a { background: #fb923c; }
    .tier-b { background: #facc15; }
    .tier-c { background: #4ade80; }
    .tier-u { background: #93c5fd; font-size: 22px; text-align: center; }

    .drop-zone {
      padding: 14px;
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      align-content: flex-start;
      min-height: 170px;
      background: #111827;
      transition: 0.15s;
    }

    .drop-zone.drag-over {
      background: #172554;
      outline: 2px dashed #60a5fa;
      outline-offset: -8px;
    }

    .movie-card {
      width: 132px;
      background: #f9fafb;
      color: #111827;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 8px 18px rgba(0,0,0,0.28);
      cursor: grab;
      user-select: none;
      border: 2px solid transparent;
    }

    .movie-card:active {
      cursor: grabbing;
    }

    .movie-card.dragging {
      opacity: 0.45;
      border-color: #60a5fa;
    }

    .poster {
      width: 100%;
      height: 180px;
      background: linear-gradient(135deg, #e5e7eb, #9ca3af);
      display: flex;
      justify-content: center;
      align-items: center;
      color: #374151;
      font-size: 13px;
      text-align: center;
      padding: 10px;
      overflow: hidden;
    }

    .poster img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .movie-title {
      min-height: 44px;
      padding: 8px;
      font-size: 14px;
      font-weight: 800;
      line-height: 1.25;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      word-break: keep-all;
    }

    .card-actions {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 4px;
      padding: 7px;
      background: #e5e7eb;
    }

    .card-actions button,
    .upload-label {
      padding: 6px 4px;
      font-size: 12px;
      border-radius: 7px;
      text-align: center;
      color: white;
      font-weight: 700;
      cursor: pointer;
    }

    .upload-label {
      background: #2563eb;
    }

    .edit-btn {
      background: #059669;
      color: white;
    }

    .delete-btn {
      background: #dc2626;
      color: white;
    }

    .hidden-file {
      display: none;
    }

    .empty-text {
      color: #64748b;
      font-size: 15px;
      padding: 12px;
    }

    footer {
      margin-top: 24px;
      color: #9ca3af;
      font-size: 13px;
      line-height: 1.5;
    }

    @media (max-width: 800px) {
      .tier-row {
        grid-template-columns: 72px 1fr;
      }

      .tier-label {
        font-size: 28px;
      }

      .tier-u {
        font-size: 16px;
      }

      .movie-card {
        width: 118px;
      }

      .poster {
        height: 160px;
      }

      .toolbar {
        flex-direction: column;
        align-items: stretch;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>영화 티어리스트</h1>
    <p>내가 본 영화를 S / A / B / C 등급으로 정리해 보세요.</p>
  </header>

  <main class="container">
    <section class="toolbar">
      <input id="newMovieInput" type="text" placeholder="추가할 영화 제목을 입력하세요" />
      <button class="add-btn" id="addMovieBtn">영화 추가</button>
      <button class="reset-btn" id="resetBtn">초기화</button>
    </section>

    <section class="notice">
      영화 카드를 드래그해서 원하는 등급 칸에 놓으세요.  
      각 영화의 <strong>사진</strong> 버튼으로 포스터 이미지를 업로드할 수 있으며,
      제목과 등급 정보는 브라우저에 자동 저장됩니다.
    </section>

    <section class="tier-list" id="tierList"></section>

    <footer>
      ※ 이 페이지는 외부 서버 없이 동작합니다. 업로드한 이미지는 현재 브라우저의 로컬스토리지에 저장됩니다.
    </footer>
  </main>

  <script>
    const STORAGE_KEY = "movieTierListData_v1";

    const tiers = [
      { id: "S", label: "S", className: "tier-s" },
      { id: "A", label: "A", className: "tier-a" },
      { id: "B", label: "B", className: "tier-b" },
      { id: "C", label: "C", className: "tier-c" },
      { id: "UNRATED", label: "미분류", className: "tier-u" }
    ];

    const initialMovies = [
      "귀를 기울이면",
      "모노노케 히메",
      "센과 치히로의 행방불명",
      "마녀 배달부 키키",
      "이웃집 토토로",
      "하울의 움직이는 성",
      "바람계곡의 나우시카",
      "천공의 성 라퓨타"
    ].map(title => ({
      id: createId(),
      title,
      image: "",
      tier: "UNRATED"
    }));

    let movies = loadMovies();
    let draggedMovieId = null;

    const tierList = document.getElementById("tierList");
    const newMovieInput = document.getElementById("newMovieInput");
    const addMovieBtn = document.getElementById("addMovieBtn");
    const resetBtn = document.getElementById("resetBtn");

    render();

    addMovieBtn.addEventListener("click", addMovie);

    newMovieInput.addEventListener("keydown", event => {
      if (event.key === "Enter") {
        addMovie();
      }
    });

    resetBtn.addEventListener("click", () => {
      const ok = confirm("모든 변경사항을 지우고 처음 상태로 되돌릴까요?");
      if (!ok) return;

      movies = initialMovies.map(movie => ({
        ...movie,
        id: createId()
      }));

      saveMovies();
      render();
    });

    function createId() {
      return "movie_" + Date.now() + "_" + Math.random().toString(16).slice(2);
    }

    function loadMovies() {
      const saved = localStorage.getItem(STORAGE_KEY);

      if (!saved) {
        return initialMovies;
      }

      try {
        const parsed = JSON.parse(saved);
        if (Array.isArray(parsed)) {
          return parsed;
        }
        return initialMovies;
      } catch {
        return initialMovies;
      }
    }

    function saveMovies() {
      localStorage.setItem(STORAGE_KEY, JSON.stringify(movies));
    }

    function render() {
      tierList.innerHTML = "";

      tiers.forEach(tier => {
        const row = document.createElement("div");
        row.className = "tier-row";

        const label = document.createElement("div");
        label.className = `tier-label ${tier.className}`;
        label.textContent = tier.label;

        const dropZone = document.createElement("div");
        dropZone.className = "drop-zone";
        dropZone.dataset.tier = tier.id;

        dropZone.addEventListener("dragover", event => {
          event.preventDefault();
          dropZone.classList.add("drag-over");
        });

        dropZone.addEventListener("dragleave", () => {
          dropZone.classList.remove("drag-over");
        });

        dropZone.addEventListener("drop", event => {
          event.preventDefault();
          dropZone.classList.remove("drag-over");

          if (!draggedMovieId) return;

          const movie = movies.find(item => item.id === draggedMovieId);
          if (movie) {
            movie.tier = tier.id;
            saveMovies();
            render();
          }
        });

        const moviesInTier = movies.filter(movie => movie.tier === tier.id);

        if (moviesInTier.length === 0) {
          const emptyText = document.createElement("div");
          emptyText.className = "empty-text";
          emptyText.textContent = "이 칸에 영화를 드래그해 넣으세요.";
          dropZone.appendChild(emptyText);
        } else {
          moviesInTier.forEach(movie => {
            dropZone.appendChild(createMovieCard(movie));
          });
        }

        row.appendChild(label);
        row.appendChild(dropZone);
        tierList.appendChild(row);
      });
    }

    function createMovieCard(movie) {
      const card = document.createElement("article");
      card.className = "movie-card";
      card.draggable = true;
      card.dataset.id = movie.id;

      card.addEventListener("dragstart", () => {
        draggedMovieId = movie.id;
        card.classList.add("dragging");
      });

      card.addEventListener("dragend", () => {
        draggedMovieId = null;
        card.classList.remove("dragging");
      });

      const poster = document.createElement("div");
      poster.className = "poster";

      if (movie.image) {
        const img = document.createElement("img");
        img.src = movie.image;
        img.alt = `${movie.title} 포스터`;
        poster.appendChild(img);
      } else {
        poster.textContent = "포스터 없음";
      }

      const title = document.createElement("div");
      title.className = "movie-title";
      title.textContent = movie.title;

      const actions = document.createElement("div");
      actions.className = "card-actions";

      const fileInput = document.createElement("input");
      fileInput.type = "file";
      fileInput.accept = "image/*";
      fileInput.className = "hidden-file";
      fileInput.id = `file_${movie.id}`;

      fileInput.addEventListener("change", event => {
        const file = event.target.files[0];
        if (!file) return;

        resizeImage(file, 500, dataUrl => {
          movie.image = dataUrl;
          saveMovies();
          render();
        });
      });

      const uploadLabel = document.createElement("label");
      uploadLabel.className = "upload-label";
      uploadLabel.htmlFor = fileInput.id;
      uploadLabel.textContent = "사진";

      const editBtn = document.createElement("button");
      editBtn.className = "edit-btn";
      editBtn.type = "button";
      editBtn.textContent = "수정";
      editBtn.addEventListener("click", () => {
        const newTitle = prompt("영화 제목을 수정하세요.", movie.title);
        if (newTitle === null) return;

        const trimmed = newTitle.trim();
        if (!trimmed) {
          alert("영화 제목은 비워둘 수 없습니다.");
          return;
        }

        movie.title = trimmed;
        saveMovies();
        render();
      });

      const deleteBtn = document.createElement("button");
      deleteBtn.className = "delete-btn";
      deleteBtn.type = "button";
      deleteBtn.textContent = "삭제";
      deleteBtn.addEventListener("click", () => {
        const ok = confirm(`"${movie.title}" 영화를 삭제할까요?`);
        if (!ok) return;

        movies = movies.filter(item => item.id !== movie.id);
        saveMovies();
        render();
      });

      actions.appendChild(fileInput);
      actions.appendChild(uploadLabel);
      actions.appendChild(editBtn);
      actions.appendChild(deleteBtn);

      card.appendChild(poster);
      card.appendChild(title);
      card.appendChild(actions);

      return card;
    }

    function addMovie() {
      const title = newMovieInput.value.trim();

      if (!title) {
        alert("추가할 영화 제목을 입력하세요.");
        newMovieInput.focus();
        return;
      }

      movies.push({
        id: createId(),
        title,
        image: "",
        tier: "UNRATED"
      });

      newMovieInput.value = "";
      saveMovies();
      render();
    }

    function resizeImage(file, maxWidth, callback) {
      const reader = new FileReader();

      reader.onload
나
뒤에 잘린 거 아니지?
AI
맞아요, 이전 답변은 뒤쪽 JavaScript 코드가 잘렸습니다.
아래에 완성된 단일 HTML 파일 전체 코드를 다시 드릴게요. 그대로 복사해서 movie-tier-list.html로 저장하면 됩니다. 😊

html
📋 복사
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>영화 티어리스트</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, "Noto Sans KR", sans-serif;
      background: #111827;
      color: #f9fafb;
    }

    header {
      padding: 28px 32px;
      background: linear-gradient(135deg, #1f2937, #111827);
      border-bottom: 1px solid #374151;
    }

    header h1 {
      margin: 0;
      font-size: 32px;
    }

    header p {
      margin: 8px 0 0;
      color: #d1d5db;
    }

    main {
      max-width: 1280px;
      margin: 0 auto;
      padding: 24px;
    }

    .toolbar {
      display: flex;
      gap: 10px;
      margin-bottom: 16px;
      padding: 16px;
      background: #1f2937;
      border: 1px solid #374151;
      border-radius: 14px;
    }

    .toolbar input {
      flex: 1;
      padding: 12px 14px;
      border: 1px solid #4b5563;
      border-radius: 10px;
      background: #111827;
      color: #f9fafb;
      font-size: 15px;
      outline: none;
    }

    .toolbar input:focus {
      border-color: #60a5fa;
    }

    button {
      border: none;
      cursor: pointer;
      border-radius: 9px;
      font-weight: bold;
      transition: 0.15s;
    }

    button:hover {
      opacity: 0.9;
      transform: translateY(-1px);
    }

    .add-btn {
      padding: 12px 18px;
      background: #2563eb;
      color: white;
    }

    .reset-btn {
      padding: 12px 18px;
      background: #4b5563;
      color: white;
    }

    .notice {
      margin-bottom: 18px;
      padding: 14px;
      background: #0f172a;
      border: 1px solid #334155;
      border-radius: 12px;
      color: #cbd5e1;
      line-height: 1.5;
      font-size: 14px;
    }

    .tier-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .tier-row {
      display: grid;
      grid-template-columns: 110px 1fr;
      min-height: 178px;
      border: 1px solid #374151;
      border-radius: 14px;
      overflow: hidden;
      background: #1f2937;
    }

    .tier-label {
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 40px;
      font-weight: 900;
      color: #111827;
      text-align: center;
    }

    .tier-s { background: #f87171; }
    .tier-a { background: #fb923c; }
    .tier-b { background: #facc15; }
    .tier-c { background: #4ade80; }
    .tier-u {
      background: #93c5fd;
      font-size: 22px;
    }

    .drop-zone {
      min-height: 178px;
      padding: 14px;
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      align-content: flex-start;
      background: #111827;
      transition: 0.15s;
    }

    .drop-zone.drag-over {
      background: #172554;
      outline: 2px dashed #60a5fa;
      outline-offset: -8px;
    }

    .empty-text {
      color: #64748b;
      padding: 12px;
      font-size: 15px;
    }

    .movie-card {
      width: 132px;
      background: #f9fafb;
      color: #111827;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 8px 18px rgba(0, 0, 0, 0.28);
      cursor: grab;
      user-select: none;
      border: 2px solid transparent;
    }

    .movie-card:active {
      cursor: grabbing;
    }

    .movie-card.dragging {
      opacity: 0.45;
      border-color: #60a5fa;
    }

    .poster {
      width: 100%;
      height: 180px;
      background: linear-gradient(135deg, #e5e7eb, #9ca3af);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #374151;
      font-size: 13px;
      text-align: center;
      padding: 10px;
      overflow: hidden;
    }

    .poster img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .movie-title {
      min-height: 46px;
      padding: 8px;
      font-size: 14px;
      font-weight: 800;
      line-height: 1.25;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      word-break: keep-all;
    }

    .card-actions {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 4px;
      padding: 7px;
      background: #e5e7eb;
    }

    .card-actions button,
    .upload-label {
      padding: 6px 4px;
      font-size: 12px;
      border-radius: 7px;
      text-align: center;
      color: white;
      font-weight: bold;
      cursor: pointer;
    }

    .upload-label {
      background: #2563eb;
    }

    .edit-btn {
      background: #059669;
      color: white;
    }

    .delete-btn {
      background: #dc2626;
      color: white;
    }

    .hidden-file {
      display: none;
    }

    footer {
      margin-top: 24px;
      color: #9ca3af;
      font-size: 13px;
      line-height: 1.5;
    }

    @media (max-width: 800px) {
      .toolbar {
        flex-direction: column;
      }

      .tier-row {
        grid-template-columns: 76px 1fr;
      }

      .tier-label {
        font-size: 28px;
      }

      .tier-u {
        font-size: 16px;
      }

      .movie-card {
        width: 118px;
      }

      .poster {
        height: 160px;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>영화 티어리스트</h1>
    <p>내가 본 영화를 S / A / B / C 등급으로 정리해 보세요.</p>
  </header>

  <main>
    <section class="toolbar">
      <input id="newMovieInput" type="text" placeholder="추가할 영화 제목을 입력하세요" />
      <button class="add-btn" id="addMovieBtn">영화 추가</button>
      <button class="reset-btn" id="resetBtn">초기화</button>
    </section>

    <section class="notice">
      영화 카드를 드래그해서 원하는 등급 칸에 놓으세요.
      각 영화의 <strong>사진</strong> 버튼으로 포스터를 업로드할 수 있습니다.
      등급, 제목, 포스터 이미지는 브라우저 로컬스토리지에 자동 저장됩니다.
    </section>

    <section class="tier-list" id="tierList"></section>

    <footer>
      ※ 외부 서버 없이 브라우저에서 바로 실행됩니다.  
      ※ 업로드한 이미지는 현재 브라우저의 로컬스토리지에 저장됩니다.
    </footer>
  </main>

  <script>
    const STORAGE_KEY = "movieTierListData_v1";

    const tiers = [
      { id: "S", label: "S", className: "tier-s" },
      { id: "A", label: "A", className: "tier-a" },
      { id: "B", label: "B", className: "tier-b" },
      { id: "C", label: "C", className: "tier-c" },
      { id: "UNRATED", label: "미분류", className: "tier-u" }
    ];

    const defaultTitles = [
      "귀를 기울이면",
      "모노노케 히메",
      "센과 치히로의 행방불명",
      "마녀 배달부 키키",
      "이웃집 토토로",
      "하울의 움직이는 성",
      "바람계곡의 나우시카",
      "천공의 성 라퓨타"
    ];

    let movies = loadMovies();
    let draggedMovieId = null;

    const tierList = document.getElementById("tierList");
    const newMovieInput = document.getElementById("newMovieInput");
    const addMovieBtn = document.getElementById("addMovieBtn");
    const resetBtn = document.getElementById("resetBtn");

    render();

    addMovieBtn.addEventListener("click", addMovie);

    newMovieInput.addEventListener("keydown", function (event) {
      if (event.key === "Enter") {
        addMovie();
      }
    });

    resetBtn.addEventListener("click", function () {
      const ok = confirm("모든 변경사항을 지우고 처음 상태로 되돌릴까요?");
      if (!ok) return;

      movies = createDefaultMovies();
      saveMovies();
      render();
    });

    function createId() {
      return "movie_" + Date.now() + "_" + Math.random().toString(16).slice(2);
    }

    function createDefaultMovies() {
      return defaultTitles.map(function (title) {
        return {
          id: createId(),
          title: title,
          image: "",
          tier: "UNRATED"
        };
      });
    }

    function loadMovies() {
      const saved = localStorage.getItem(STORAGE_KEY);

      if (!saved) {
        return createDefaultMovies();
      }

      try {
        const parsed = JSON.parse(saved);

        if (Array.isArray(parsed)) {
          return parsed;
        }

        return createDefaultMovies();
      } catch (error) {
        return createDefaultMovies();
      }
    }

    function saveMovies() {
      try {
        localStorage.setItem(STORAGE_KEY, JSON.stringify(movies));
      } catch (error) {
        alert("저장 공간이 부족할 수 있습니다. 더 작은 이미지를 사용해 주세요.");
      }
    }

    function render() {
      tierList.innerHTML = "";

      tiers.forEach(function (tier) {
        const row = document.createElement("div");
        row.className = "tier-row";

        const label = document.createElement("div");
        label.className = "tier-label " + tier.className;
        label.textContent = tier.label;

        const dropZone = document.createElement("div");
        dropZone.className = "drop-zone";
        dropZone.dataset.tier = tier.id;

        dropZone.addEventListener("dragover", function (event) {
          event.preventDefault();
          dropZone.classList.add("drag-over");
        });

        dropZone.addEventListener("dragleave", function () {
          dropZone.classList.remove("drag-over");
        });

        dropZone.addEventListener("drop", function (event) {
          event.preventDefault();
          dropZone.classList.remove("drag-over");

          if (!draggedMovieId) return;

          const movie = movies.find(function (item) {
            return item.id === draggedMovieId;
          });

          if (movie) {
            movie.tier = tier.id;
            saveMovies();
            render();
          }
        });

        const moviesInTier = movies.filter(function (movie) {
          return movie.tier === tier.id;
        });

        if (moviesInTier.length === 0) {
          const emptyText = document.createElement("div");
          emptyText.className = "empty-text";
          emptyText.textContent = "이 칸에 영화를 드래그해 넣으세요.";
          dropZone.appendChild(emptyText);
        } else {
          moviesInTier.forEach(function (movie) {
            dropZone.appendChild(createMovieCard(movie));
          });
        }

        row.appendChild(label);
        row.appendChild(dropZone);
        tierList.appendChild(row);
      });
    }

    function createMovieCard(movie) {
      const card = document.createElement("article");
      card.className = "movie-card";
      card.draggable = true;
      card.dataset.id = movie.id;

      card.addEventListener("dragstart", function (event) {
        draggedMovieId = movie.id;
        card.classList.add("dragging");
        event.dataTransfer.setData("text/plain", movie.id);
      });

      card.addEventListener("dragend", function () {
        draggedMovieId = null;
        card.classList.remove("dragging");
      });

      const poster = document.createElement("div");
      poster.className = "poster";

      if (movie.image) {
        const img = document.createElement("img");
        img.src = movie.image;
        img.alt = movie.title + " 포스터";
        poster.appendChild(img);
      } else {
        poster.textContent = "포스터 없음";
      }

      const title = document.createElement("div");
      title.className = "movie-title";
      title.textContent = movie.title;

      const actions = document.createElement("div");
      actions.className = "card-actions";

      const fileInput = document.createElement("input");
      fileInput.type = "file";
      fileInput.accept = "image/*";
      fileInput.className = "hidden-file";
      fileInput.id = "file_" + movie.id;

      fileInput.addEventListener("change", function (event) {
        const file = event.target.files[0];
        if (!file) return;

        resizeImage(file, 600, function (dataUrl) {
          movie.image = dataUrl;
          saveMovies();
          render();
        });
      });

      const uploadLabel = document.createElement("label");
      uploadLabel.className = "upload-label";
      uploadLabel.htmlFor = fileInput.id;
      uploadLabel.textContent = "사진";

      const editBtn = document.createElement("button");
      editBtn.className = "edit-btn";
      editBtn.type = "button";
      editBtn.textContent = "수정";

      editBtn.addEventListener("click", function () {
        const newTitle = prompt("영화 제목을 수정하세요.", movie.title);

        if (newTitle === null) return;

        const trimmed = newTitle.trim();

        if (!trimmed) {
          alert("영화 제목은 비워둘 수 없습니다.");
          return;
        }

        movie.title = trimmed;
        saveMovies();
        render();
      });

      const deleteBtn = document.createElement("button");
      deleteBtn.className = "delete-btn";
      deleteBtn.type = "button";
      deleteBtn.textContent = "삭제";

      deleteBtn.addEventListener("click", function () {
        const ok = confirm('"' + movie.title + '" 영화를 삭제할까요?');
        if (!ok) return;

        movies = movies.filter(function (item) {
          return item.id !== movie.id;
        });

        saveMovies();
        render();
      });

      actions.appendChild(fileInput);
      actions.appendChild(uploadLabel);
      actions.appendChild(editBtn);
      actions.appendChild(deleteBtn);

      card.appendChild(poster);
      card.appendChild(title);
      card.appendChild(actions);

      return card;
    }

    function addMovie() {
      const title = newMovieInput.value.trim();

      if (!title) {
        alert("추가할 영화 제목을 입력하세요.");
        newMovieInput.focus();
        return;
      }

      movies.push({
        id: createId(),
        title: title,
        image: "",
        tier: "UNRATED
나
이것도 잘린 것 같아. 세 파트로 나눠서 보내줘.
AI
좋아요. 아래 Part 1 → Part 2 → Part 3 순서대로 전부 이어 붙여서 하나의 파일로 저장하면 됩니다.

파일 이름 예시: movie-tier-list.html

Part 1 / 3
html
📋 복사
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>영화 티어리스트</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, "Noto Sans KR", sans-serif;
      background: #111827;
      color: #f9fafb;
    }

    header {
      padding: 28px 32px;
      background: linear-gradient(135deg, #1f2937, #111827);
      border-bottom: 1px solid #374151;
    }

    header h1 {
      margin: 0;
      font-size: 32px;
    }

    header p {
      margin: 8px 0 0;
      color: #d1d5db;
    }

    main {
      max-width: 1280px;
      margin: 0 auto;
      padding: 24px;
    }

    .toolbar {
      display: flex;
      gap: 10px;
      margin-bottom: 16px;
      padding: 16px;
      background: #1f2937;
      border: 1px solid #374151;
      border-radius: 14px;
    }

    .toolbar input {
      flex: 1;
      padding: 12px 14px;
      border: 1px solid #4b5563;
      border-radius: 10px;
      background: #111827;
      color: #f9fafb;
      font-size: 15px;
      outline: none;
    }

    .toolbar input:focus {
      border-color: #60a5fa;
    }

    button {
      border: none;
      cursor: pointer;
      border-radius: 9px;
      font-weight: bold;
      transition: 0.15s;
    }

    button:hover {
      opacity: 0.9;
      transform: translateY(-1px);
    }

    .add-btn {
      padding: 12px 18px;
      background: #2563eb;
      color: white;
    }

    .reset-btn {
      padding: 12px 18px;
      background: #4b5563;
      color: white;
    }

    .notice {
      margin-bottom: 18px;
      padding: 14px;
      background: #0f172a;
      border: 1px solid #334155;
      border-radius: 12px;
      color: #cbd5e1;
      line-height: 1.5;
      font-size: 14px;
    }

    .tier-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .tier-row {
      display: grid;
      grid-template-columns: 110px 1fr;
      min-height: 178px;
      border: 1px solid #374151;
      border-radius: 14px;
      overflow: hidden;
      background: #1f2937;
    }

    .tier-label {
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 40px;
      font-weight: 900;
      color: #111827;
      text-align: center;
    }

    .tier-s {
      background: #f87171;
    }

    .tier-a {
      background: #fb923c;
    }

    .tier-b {
      background: #facc15;
    }

    .tier-c {
      background: #4ade80;
    }

    .tier-u {
      background: #93c5fd;
      font-size: 22px;
    }

    .drop-zone {
      min-height: 178px;
      padding: 14px;
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      align-content: flex-start;
      background: #111827;
      transition: 0.15s;
    }

    .drop-zone.drag-over {
      background: #172554;
      outline: 2px dashed #60a5fa;
      outline-offset: -8px;
    }

    .empty-text {
      color: #64748b;
      padding: 12px;
      font-size: 15px;
    }

    .movie-card {
      width: 132px;
      background: #f9fafb;
      color: #111827;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 8px 18px rgba(0, 0, 0, 0.28);
      cursor: grab;
      user-select: none;
      border: 2px solid transparent;
    }

    .movie-card:active {
      cursor: grabbing;
    }

    .movie-card.dragging {
      opacity: 0.45;
      border-color: #60a5fa;
    }

    .poster {
      width: 100%;
      height: 180px;
      background: linear-gradient(135deg, #e5e7eb, #9ca3af);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #374151;
      font-size: 13px;
      text-align: center;
      padding: 10px;
      overflow: hidden;
    }

    .poster img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .movie-title {
      min-height: 46px;
      padding: 8px;
      font-size: 14px;
      font-weight: 800;
      line-height: 1.25;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      word-break: keep-all;
    }

    .card-actions {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 4px;
      padding: 7px;
      background: #e5e7eb;
    }

    .card-actions button,
    .upload-label {
      padding: 6px 4px;
      font-size: 12px;
      border-radius: 7px;
      text-align: center;
      color: white;
      font-weight: bold;
      cursor: pointer;
    }

    .upload-label {
      background: #2563eb;
    }

    .edit-btn {
      background: #059669;
      color: white;
    }

    .delete-btn {
      background: #dc2626;
      color: white;
    }

    .hidden-file {
      display: none;
    }

    footer {
      margin-top: 24px;
      color: #9ca3af;
      font-size: 13px;
      line-height: 1.5;
    }

    @media (max-width: 800px) {
      .toolbar {
        flex-direction: column;
      }

      .tier-row {
        grid-template-columns: 76px 1fr;
      }

      .tier-label {
        font-size: 28px;
      }

      .tier-u {
        font-size: 16px;
      }

      .movie-card {
        width: 118px;
      }

      .poster {
        height: 160px;
      }
    }
  </style>
</head>
Part 2 / 3
html
📋 복사
<body>
  <header>
    <h1>영화 티어리스트</h1>
    <p>내가 본 영화를 S / A / B / C 등급으로 정리해 보세요.</p>
  </header>

  <main>
    <section class="toolbar">
      <input id="newMovieInput" type="text" placeholder="추가할 영화 제목을 입력하세요" />
      <button class="add-btn" id="addMovieBtn">영화 추가</button>
      <button class="reset-btn" id="resetBtn">초기화</button>
    </section>

    <section class="notice">
      영화 카드를 드래그해서 원하는 등급 칸에 놓으세요.
      각 영화의 <strong>사진</strong> 버튼으로 포스터를 업로드할 수 있습니다.
      등급, 제목, 포스터 이미지는 브라우저 로컬스토리지에 자동 저장됩니다.
    </section>

    <section class="tier-list" id="tierList"></section>

    <footer>
      ※ 외부 서버 없이 브라우저에서 바로 실행됩니다.<br />
      ※ 업로드한 이미지는 현재 브라우저의 로컬스토리지에 저장됩니다.
    </footer>
  </main>

  <script>
    const STORAGE_KEY = "movieTierListData_v1";

    const tiers = [
      { id: "S", label: "S", className: "tier-s" },
      { id: "A", label: "A", className: "tier-a" },
      { id: "B", label: "B", className: "tier-b" },
      { id: "C", label: "C", className: "tier-c" },
      { id: "UNRATED", label: "미분류", className: "tier-u" }
    ];

    const defaultTitles = [
      "귀를 기울이면",
      "모노노케 히메",
      "센과 치히로의 행방불명",
      "마녀 배달부 키키",
      "이웃집 토토로",
      "하울의 움직이는 성",
      "바람계곡의 나우시카",
      "천공의 성 라퓨타"
    ];

    let movies = loadMovies();
    let draggedMovieId = null;

    const tierList = document.getElementById("tierList");
    const newMovieInput = document.getElementById("newMovieInput");
    const addMovieBtn = document.getElementById("addMovieBtn");
    const resetBtn = document.getElementById("resetBtn");

    render();

    addMovieBtn.addEventListener("click", addMovie);

    newMovieInput.addEventListener("keydown", function (event) {
      if (event.key === "Enter") {
        addMovie();
      }
    });

    resetBtn.addEventListener("click", function () {
      const ok = confirm("모든 변경사항을 지우고 처음 상태로 되돌릴까요?");
      if (!ok) return;

      movies = createDefaultMovies();
      saveMovies();
      render();
    });

    function createId() {
      return "movie_" + Date.now() + "_" + Math.random().toString(16).slice(2);
    }

    function createDefaultMovies() {
      return defaultTitles.map(function (title) {
        return {
          id: createId(),
          title: title,
          image: "",
          tier: "UNRATED"
        };
      });
    }

    function loadMovies() {
      const saved = localStorage.getItem(STORAGE_KEY);

      if (!saved) {
        return createDefaultMovies();
      }

      try {
        const parsed = JSON.parse(saved);

        if (Array.isArray(parsed)) {
          return parsed;
        }

        return createDefaultMovies();
      } catch (error) {
        return createDefaultMovies();
      }
    }

    function saveMovies() {
      try {
        localStorage.setItem(STORAGE_KEY, JSON.stringify(movies));
      } catch (error) {
        alert("저장 공간이 부족할 수 있습니다. 더 작은 이미지를 사용해 주세요.");
      }
    }

    function render() {
      tierList.innerHTML = "";

      tiers.forEach(function (tier) {
        const row = document.createElement("div");
        row.className = "tier-row";

        const label = document.createElement("div");
        label.className = "tier-label " + tier.className;
        label.textContent = tier.label;

        const dropZone = document.createElement("div");
        dropZone.className = "drop-zone";
        dropZone.dataset.tier = tier.id;

        dropZone.addEventListener("dragover", function (event) {
          event.preventDefault();
          dropZone.classList.add("drag-over");
        });

        dropZone.addEventListener("dragleave", function () {
          dropZone.classList.remove("drag-over");
        });

        dropZone.addEventListener("drop", function (event) {
          event.preventDefault();
          dropZone.classList.remove("drag-over");

          if (!draggedMovieId) return;

          const movie = movies.find(function (item) {
            return item.id === draggedMovieId;
          });

          if (movie) {
            movie.tier = tier.id;
            saveMovies();
            render();
          }
        });

        const moviesInTier = movies.filter(function (movie) {
          return movie.tier === tier.id;
        });

        if (moviesInTier.length === 0) {
          const emptyText = document.createElement("div");
          emptyText.className = "empty-text";
          emptyText.textContent = "이 칸에 영화를 드래그해 넣으세요.";
          dropZone.appendChild(emptyText);
        } else {
          moviesInTier.forEach(function (movie) {
            dropZone.appendChild(createMovieCard(movie));
          });
        }

        row.appendChild(label);
        row.appendChild(dropZone);
        tierList.appendChild(row);
      });
    }
Part 3 / 3
html
📋 복사
    function createMovieCard(movie) {
      const card = document.createElement("article");
      card.className = "movie-card";
      card.draggable = true;
      card.dataset.id = movie.id;

      card.addEventListener("dragstart", function (event) {
        draggedMovieId = movie.id;
        card.classList.add("dragging");
        event.dataTransfer.setData("text/plain", movie.id);
      });

      card.addEventListener("dragend", function () {
        draggedMovieId = null;
        card
나
Part 3이 잘린 것 같아
AI
맞아요. Part 3이 중간에서 잘렸습니다.
아래는 Part 3 / 3 전체입니다. 이전에 받은 Part 1 + Part 2 뒤에 그대로 이어 붙이면 됩니다. 👍

Part 3 / 3
html
📋 복사
    function createMovieCard(movie) {
      const card = document.createElement("article");
      card.className = "movie-card";
      card.draggable = true;
      card.dataset.id = movie.id;

      card.addEventListener("dragstart", function (event) {
        draggedMovieId = movie.id;
        card.classList.add("dragging");
        event.dataTransfer.setData("text/plain", movie.id);
      });

      card.addEventListener("dragend", function () {
        draggedMovieId = null;
        card.classList.remove("dragging");
      });

      const poster = document.createElement("div");
      poster.className = "poster";

      if (movie.image) {
        const img = document.createElement("img");
        img.src = movie.image;
        img.alt = movie.title + " 포스터";
        poster.appendChild(img);
      } else {
        poster.textContent = "포스터 없음";
      }

      const title = document.createElement("div");
      title.className = "movie-title";
      title.textContent = movie.title;

      const actions = document.createElement("div");
      actions.className = "card-actions";

      const fileInput = document.createElement("input");
      fileInput.type = "file";
      fileInput.accept = "image/*";
      fileInput.className = "hidden-file";
      fileInput.id = "file_" + movie.id;

      fileInput.addEventListener("change", function (event) {
        const file = event.target.files[0];
        if (!file) return;

        resizeImage(file, 600, function (dataUrl) {
          movie.image = dataUrl;
          saveMovies();
          render();
        });
      });

      const uploadLabel = document.createElement("label");
      uploadLabel.className = "upload-label";
      uploadLabel.htmlFor = fileInput.id;
      uploadLabel.textContent = "사진";

      const editBtn = document.createElement("button");
      editBtn.className = "edit-btn";
      editBtn.type = "button";
      editBtn.textContent = "수정";

      editBtn.addEventListener("click", function () {
        const newTitle = prompt("영화 제목을 수정하세요.", movie.title);

        if (newTitle === null) return;

        const trimmed = newTitle.trim();

        if (!trimmed) {
          alert("영화 제목은 비워둘 수 없습니다.");
          return;
        }

        movie.title = trimmed;
        saveMovies();
        render();
      });

      const deleteBtn = document.createElement("button");
      deleteBtn.className = "delete-btn";
      deleteBtn.type = "button";
      deleteBtn.textContent = "삭제";

      deleteBtn.addEventListener("click", function () {
        const ok = confirm('"' + movie.title + '" 영화를 삭제할까요?');
        if (!ok) return;

        movies = movies.filter(function (item) {
          return item.id !== movie.id;
        });

        saveMovies();
        render();
      });

      actions.appendChild(fileInput);
      actions.appendChild(uploadLabel);
      actions.appendChild(editBtn);
      actions.appendChild(deleteBtn);

      card.appendChild(poster);
      card.appendChild(title);
      card.appendChild(actions);

      return card;
    }

    function addMovie() {
      const title = newMovieInput.value.trim();

      if (!title) {
        alert("추가할 영화 제목을 입력하세요.");
        newMovieInput.focus();
        return;
      }

      movies.push({
        id: createId(),
        title: title,
        image: "",
        tier: "UNRATED"
      });

      newMovieInput.value = "";
      saveMovies();
      render();
    }

    function resizeImage(file, maxWidth, callback) {
      const reader = new FileReader();

      reader.onload = function (event) {
        const img = new Image();

        img.onload = function () {
          let width = img.width;
          let height = img.height;

          if (width > maxWidth) {
            height = Math.round((height * maxWidth) / width);
            width = maxWidth;
          }

          const canvas = document.createElement("canvas");
          canvas.width = width;
          canvas.height = height;

          const context = canvas.getContext("2d");
          context.drawImage(img, 0, 0, width, height);

          const dataUrl = canvas.toDataURL("image/jpeg", 0.82);
          callback(dataUrl);
        };

        img.src = event.target.result;
      };

      reader.readAsDataURL(file);
    }
  </script>
</body>
</html>
이제 구조는 이렇게 붙이면 됩니다.

text
📋 복사
Part 1
Part 2
Part 3
저장 후 브라우저에서 열면 정상 실행될 거예요. 잘하고 있어요!