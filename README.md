<h1 align="center">Hi, I'm Kabelo ⭐</h1>





<div align="center">

![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&pause=1000&color=1E90FF&background=FFFFFF&width=820&lines=AI+-+Front-End+Developer+%26+UX%2FUI+Product+Designer)

</div>


---

<section style="font-family: 'Inter', sans-serif; direction: rtl; text-align: right; line-height: 1.7; color: #555555; max-width: 700px; margin: 0 auto;">
  <h2 style="color: #111111; font-size: 26px; margin-bottom: 16px;">👨‍💻 About Me</h2>
  <p>I'm a <strong style="color: #1E90FF;">Front-End Developer</strong> & <strong style="color: #1E90FF;">UX/UI Designer</strong> from <em>Johannesburg, South Africa</em>.</p>
  <p>I build <strong>responsive, user-friendly apps</strong> with <strong>HTML, CSS, JavaScript, React</strong>, and <strong>Figma</strong>.</p>
  <p>With <strong>10+ years of experience</strong>, I create <strong>intuitive digital experiences</strong> and thrive in collaborative teams.</p>
  <p>Currently exploring <strong>Ethereum Blockchain Development</strong> and working on freelance projects.</p>
  <p style="color: #1E90FF; background-color: #ffffff; font-family: 'Inter', sans-serif; padding: 8px; border-radius: 4px;">
  ✨ Passionate about <strong>design + code + strategy</strong> to craft meaningful experiences.
</p>

  <!-- Portfolio Button -->
  <p>
    <a href="https://www.behance.net/kabelomaitisa1" target="_blank" 
       style="display: inline-block; background-color: #1E90FF; color: #ffffff; padding: 12px 24px; border-radius: 8px; text-decoration: none; font-weight: 600; transition: background-color 0.3s;">
      View Portfolio
    </a>
  </p>
</section>


---

## 🛠️ Skills
![HTML](https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 🧑‍🚀 What I'm working on:

- Delivering freelance projects for clients
- Creating and managing content on Pinterest and YouTube
- Learning and experimenting with AI & Machine Learning technologies
- Developing decentralized applications (dApps) on the Ethereum blockchain

---

## 🌱 I’m currently learning:
- Web3 & Blockchain Development (Ethereum, Solidity, Smart Contracts)
- AI & Machine Learning applications

---
 
## 🤖 Interested in
- Crafting intuitive and engaging UI/UX designs
- Building responsive and interactive web applications
- Exploring AI, Web3, and emerging front-end technologies

---

## 📈 GitHub Stats
![Kabelo's GitHub Stats](https://github-readme-stats.vercel.app/api?username=KabeloM13&show_icons=true&bg_color=ffffff)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=KabeloM13&layout=compact&bg_color=ffffff)

---

## 📫 How to reach me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kabelo-m-9a0555128/)
[![Behance](https://img.shields.io/badge/Behance-1769FF?style=for-the-badge&logo=behance&logoColor=white)](https://www.behance.net/kabelomaitisa1)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kabelodesigns777@gmail.com)

---

## ⚡ Fun Facts
- Coffee fuels my coding sessions ☕
- I love spending time in nature 🌿🌞

---

<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Pac-Man Demo (Canvas)</title>
<style>
  html,body { height:100%; margin:0; background:#fff; display:flex; align-items:center; justify-content:center; }
  canvas { background: #ffffff; box-shadow: 0 6px 20px rgba(0,0,0,0.2); image-rendering: pixelated; }
  .hint { position:fixed; top:12px; left:12px; font-family:system-ui,Arial; color:#222; }
</style>
</head>
<body>
<div class="hint">Use ← → ↑ ↓ or A D W S to move • Press R to reset</div>
<canvas id="game" width="720" height="720"></canvas>

<script>
/*
 Simple Pac-Man-like demo.
 - Grid-based maze (21x21)
 - Walls, pellets, power pellets
 - Pac-Man with keyboard movement
*/

const canvas = document.getElementById('game');
const ctx = canvas.getContext('2d');

// Grid params
const COLS = 21;
const ROWS = 21;
const TILE = Math.floor(canvas.width / COLS);
const PELLET_RADIUS = Math.max(2, TILE * 0.06);
const POWER_RADIUS = Math.max(5, TILE * 0.18);

// Colors
const WALL_COLOR = '#8AA0FF';   // pale blue lines
const BG_COLOR = '#FFFFFF';     // white background
const PELLET_COLOR = '#F7E7F0';
const POWER_COLOR = '#F0C6D6';
const PAC_COLOR = '#FFD300';

// Maze layout (21x21). 0=empty,1=wall,2=pellet,3=power-pellet
// A stylized symmetric maze — feel free to edit rows to change layout.
let L = [
"111111111111111111111",
"100000200000100000001",
"101110101011101011101",
"102000101000001010201",
"101110101011101011101",
"100000000000000000001",
"101110101111101011101",
"100000101000001000001",
"111110101011101011111",
"000000000000000000000",
"111110101011101011111",
"100000101000001000001",
"101110101111101011101",
"100000000000000000001",
"101110101011101011101",
"102000101000001010201",
"101110101011101011101",
"100000200000100000001",
"111111111111111111111",
"000000000000000000000",
"111111111111111111111"
];

// Convert to numeric grid (pad/truncate to ROWS x COLS)
let grid = [];
for (let r = 0; r < ROWS; r++){
  const line = (L[r] || "0".repeat(COLS)).slice(0,COLS);
  grid[r] = [];
  for (let c = 0; c < COLS; c++) {
    const ch = line[c] || "0";
    // Convert: '1'->wall, '2'->pellet, '3'->power (we used '2' in layout as pellet/power marks)
    grid[r][c] = (ch === '1') ? 1 : (ch === '2') ? 2 : (ch === '3') ? 3 : 0;
  }
}

// helper to determine walkable
function isWall(r,c){
  if (r<0||c<0||r>=ROWS||c>=COLS) return true;
  return grid[r][c] === 1;
}

// Pac-Man state (start near center-left)
let pac = {
  row: 10, col: 9,
  x: 9 * TILE + TILE/2, y: 10 * TILE + TILE/2,
  dir: {x:0,y:0}, // current moving direction in tiles: x:-1/0/1, y:-1/0/1
  desired: {x:0,y:0},
  speed: TILE * 0.14, // pixels per frame
  mouth: 0 // mouth openness (0..1)
};

let score = 0;
let pelletsTotal = 0;

// Initialize pellets count (convert zeros to pellets where not wall)
function initPellets(){
  pelletsTotal = 0;
  for (let r=0;r<ROWS;r++){
    for (let c=0;c<COLS;c++){
      // If grid cell is 0 and not boundary, set pellet; keep existing 2 as pellet/power
      if (grid[r][c] === 0) {
        // place pellet but avoid outer walls by checking immediate adjacency to walls (optional)
        grid[r][c] = 2; // pellet
        pelletsTotal++;
      } else if (grid[r][c] === 2) pelletsTotal++;
    }
  }
  // carve corridors: ensure cells that are walls remain 1 and not pellets
  for (let r=0;r<ROWS;r++){
    for (let c=0;c<COLS;c++){
      if (L[r] && L[r][c] === '1') grid[r][c] = 1;
    }
  }
  // Add a few power pellets in corners
  const corners = [[1,1],[1,COLS-2],[ROWS-2,1],[ROWS-2,COLS-2]];
  corners.forEach(([r,c]) => { if (!isWall(r,c)) { grid[r][c] = 3; pelletsTotal--; }});
}

initPellets();

// Draw wall as rounded path
function drawMaze(){
  // clear
  ctx.fillStyle = BG_COLOR;
  ctx.fillRect(0,0,canvas.width,canvas.height);

  // Draw pellets first
  for (let r=0;r<ROWS;r++){
    for (let c=0;c<COLS;c++){
      const cellX = c * TILE + TILE/2;
      const cellY = r * TILE + TILE/2;
      if (grid[r][c] === 2) {
        ctx.fillStyle = PELLET_COLOR;
        ctx.beginPath();
        ctx.arc(cellX, cellY, PELLET_RADIUS, 0, Math.PI*2);
        ctx.fill();
      } else if (grid[r][c] === 3) {
        ctx.fillStyle = POWER_COLOR;
        ctx.beginPath();
        ctx.arc(cellX, cellY, POWER_RADIUS, 0, Math.PI*2);
        ctx.fill();
      }
    }
  }

  // Draw smooth walls: stroke rectangles for each 1
  ctx.lineWidth = Math.max(2, TILE * 0.14);
  ctx.strokeStyle = WALL_COLOR;
  ctx.lineJoin = "round";
  for (let r=0;r<ROWS;r++){
    for (let c=0;c<COLS;c++){
      if (grid[r][c] === 1) {
        const x = c * TILE + ctx.lineWidth/2;
        const y = r * TILE + ctx.lineWidth/2;
        const w = TILE - ctx.lineWidth;
        const h = TILE - ctx.lineWidth;
        ctx.strokeRect(x,y,w,h);
      }
    }
  }

  // Optionally draw a center "ghost house" rectangle
  // ctx.strokeStyle = '#C39BFF'; ctx.strokeRect(canvas.width/2 - TILE*2, canvas.height/2 - TILE, TILE*4, TILE*2);
}

// Draw Pac-Man head with mouth facing current direction
function drawPac(){
  const px = pac.x, py = pac.y;
  const dir = pac.dir;
  // compute angle from direction
  let angle = 0;
  if (dir.x === 1) angle = 0;
  else if (dir.x === -1) angle = Math.PI;
  else if (dir.y === 1) angle = Math.PI/2;
  else if (dir.y === -1) angle = -Math.PI/2;
  // mouth oscillation
  const mouthOpen = 0.15 + 0.55 * Math.abs(Math.sin(pac.mouth));
  ctx.fillStyle = PAC_COLOR;
  ctx.beginPath();
  ctx.moveTo(px, py);
  ctx.arc(px, py, TILE*0.45, angle + mouthOpen, angle - mouthOpen, false);
  ctx.closePath();
  ctx.fill();
}

// Utility: canMove to tile center from current tile towards given direction
function canMoveToTile(r, c, dirX, dirY){
  const nr = r + dirY;
  const nc = c + dirX;
  return !isWall(nr, nc);
}

// Convert current pixel pos to tile indices (rounded)
function pixToTile(px, py){
  return {r: Math.floor(py / TILE), c: Math.floor(px / TILE)};
}

// Game loop
function update(){
  // try to change direction if desired available
  const center = pixToTile(pac.x, pac.y);
  // Allow direction change only when near tile center to prevent clipping
  const centerX = center.c * TILE + TILE/2;
  const centerY = center.r * TILE + TILE/2;
  const dxCenter = Math.abs(pac.x - centerX);
  const dyCenter = Math.abs(pac.y - centerY);
  const nearCenter = (dxCenter < pac.speed + 0.5 && dyCenter < pac.speed + 0.5);

  if (nearCenter) {
    // snap to center
    pac.x = centerX;
    pac.y = centerY;
    // If desired direction is possible, flip to it
    if ((pac.desired.x !== pac.dir.x || pac.desired.y !== pac.dir.y) &&
        canMoveToTile(center.r, center.c, pac.desired.x, pac.desired.y)) {
      pac.dir.x = pac.desired.x; pac.dir.y = pac.desired.y;
    }
    // If current direction blocked, stop
    if (!canMoveToTile(center.r, center.c, pac.dir.x, pac.dir.y)) {
      pac.dir.x = 0; pac.dir.y = 0;
    }
    // Collect pellet at this tile
    if (grid[center.r][center.c] === 2) {
      grid[center.r][center.c] = 0; score++;
    } else if (grid[center.r][center.c] === 3) {
      grid[center.r][center.c] = 0; score += 5;
    }
  }

  // Move in dir if possible
  if (pac.dir.x !== 0 || pac.dir.y !== 0) {
    // Before moving, check immediate next tile if about to collide (pre-check)
    const nextX = pac.x + pac.dir.x * pac.speed;
    const nextY = pac.y + pac.dir.y * pac.speed;
    // compute proposed tile
    const nextTile = pixToTile(nextX, nextY);
    if (isWall(nextTile.r, nextTile.c)) {
      // stop at center (or do nothing)
      // do nothing -> will be aligned next frame
    } else {
      pac.x = nextX; pac.y = nextY;
    }
  }

  // animate mouth
  pac.mouth += 0.3;

  // redraw
  drawMaze();
  drawPac();

  // HUD: score
  ctx.fillStyle = '#222';
  ctx.font = `${Math.max(12, TILE*0.5)}px Arial`;
  ctx.fillText('Score: ' + score, 8, canvas.height - 8);

  requestAnimationFrame(update);
}

// Keys
const keyMap = {
  'ArrowLeft': {x:-1,y:0}, 'ArrowRight': {x:1,y:0}, 'ArrowUp': {x:0,y:-1}, 'ArrowDown': {x:0,y:1},
  'a': {x:-1,y:0}, 'd': {x:1,y:0}, 'w': {x:0,y:-1}, 's': {x:0,y:1}
};

window.addEventListener('keydown', e => {
  const k = e.key;
  if (k === 'r' || k === 'R') { reset(); return; }
  const m = keyMap[k];
  if (m) {
    pac.desired.x = m.x; pac.desired.y = m.y;
    e.preventDefault();
  }
});

// Basic reset
function reset(){
  pac.row = 10; pac.col = 9;
  pac.x = pac.col * TILE + TILE/2; pac.y = pac.row * TILE + TILE/2;
  pac.dir = {x:0,y:0}; pac.desired = {x:0,y:0}; pac.mouth = 0; score = 0;
  // restore pellets (simple regen)
  initPellets();
}

// Initial placement / start
reset();
requestAnimationFrame(update);
</script>
</body>
</html>





