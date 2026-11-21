<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>贪吃蛇 · 元素周期表记忆动画</title>
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      min-height: 100vh;
      background: linear-gradient(145deg, #0b1a2e 0%, #1a2f3f 100%);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Segoe UI', 'Roboto', system-ui, sans-serif;
      padding: 16px;
    }
    .game-container {
      background: #0f1c2b;
      border-radius: 2.5rem;
      padding: 24px 24px 30px;
      box-shadow: 0 25px 40px rgba(0, 0, 0, 0.7), inset 0 0 8px rgba(100, 200, 255, 0.3);
      border: 2px solid #3e6d7a;
    }
    .header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 8px 18px 8px;
    }
    .title {
      color: #b5e6ff;
      font-weight: 600;
      font-size: 1.6rem;
      letter-spacing: 3px;
      text-shadow: 0 0 10px #2d9cdb;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .title span {
      font-size: 2rem;
    }
    .score-box {
      background: #07111b;
      color: #8ae2ff;
      font-weight: bold;
      font-size: 1.8rem;
      padding: 8px 24px;
      border-radius: 60px;
      box-shadow: inset 0 0 12px #1e4d66, 0 4px 0 #0a121c;
      border: 1px solid #2d8fb0;
      font-variant-numeric: tabular-nums;
    }
    canvas {
      display: block;
      margin: 0 auto;
      background: #0a141f;
      border-radius: 28px;
      box-shadow: inset 0 0 40px #00000066, 0 12px 25px black;
      border: 3px solid #1c485a;
      width: 100%;
      max-width: 700px;
      height: auto;
      aspect-ratio: 1 / 1;
      cursor: pointer;
    }
    .info-panel {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-top: 20px;
      padding: 0 10px;
      color: #a0d0e0;
    }
    .current-element {
      background: #0d1e2c;
      padding: 8px 18px;
      border-radius: 50px;
      font-size: 1.2rem;
      font-weight: 500;
      border-left: 6px solid #5fd1ff;
      box-shadow: 0 0 12px #1d5b77;
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .current-element .symbol {
      font-size: 2rem;
      font-weight: 800;
      color: #f0e68c;
      text-shadow: 0 0 10px #f0b34b;
    }
    .controls {
      display: flex;
      gap: 14px;
    }
    .btn {
      background: #1f3e4e;
      border: none;
      color: #d0f0ff;
      font-size: 1.2rem;
      padding: 8px 18px;
      border-radius: 40px;
      font-weight: 600;
      box-shadow: 0 6px 0 #0b1922, 0 6px 12px black;
      transition: all 0.05s ease;
      cursor: pointer;
      border: 1px solid #418aa0;
      display: flex;
      align-items: center;
      gap: 6px;
    }
    .btn:active {
      transform: translateY(5px);
      box-shadow: 0 1px 0 #0b1922, 0 6px 12px black;
    }
    .btn:disabled {
      opacity: 0.5;
      transform: translateY(3px);
      box-shadow: 0 3px 0 #0b1922;
      pointer-events: none;
    }
    .hint {
      font-size: 0.9rem;
      color: #7ba3b3;
      text-align: center;
      margin-top: 12px;
    }
  </style>
</head>
<body>
<div class="game-container">
  <div class="header">
    <div class="title">
      <span>🐍</span> 元素贪吃蛇
    </div>
    <div class="score-box" id="scoreDisplay">0</div>
  </div>

  <canvas id="gameCanvas" width="600" height="600"></canvas>

  <div class="info-panel">
    <div class="current-element">
      <span class="symbol" id="currentSymbol">H</span>
      <span id="currentName">氢 (1)</span>
    </div>
    <div class="controls">
      <button class="btn" id="restartBtn">↻ 重来</button>
    </div>
  </div>
  <div class="hint">
    ⬆⬇⬅➡ 方向键 / 点击画面控制方向 · 每吃一个元素，蛇身变长，记住符号与原子序数！
  </div>
</div>

<script>
  (function() {
    // ---------- 元素周期表数据 (前20号元素，方便记忆) ----------
    const elements = [
      { symbol: "H",  name: "氢",  atomic: 1  },
      { symbol: "He", name: "氦",  atomic: 2  },
      { symbol: "Li", name: "锂",  atomic: 3  },
      { symbol: "Be", name: "铍",  atomic: 4  },
      { symbol: "B",  name: "硼",  atomic: 5  },
      { symbol: "C",  name: "碳",  atomic: 6  },
      { symbol: "N",  name: "氮",  atomic: 7  },
      { symbol: "O",  name: "氧",  atomic: 8  },
      { symbol: "F",  name: "氟",  atomic: 9  },
      { symbol: "Ne", name: "氖",  atomic: 10 },
      { symbol: "Na", name: "钠",  atomic: 11 },
      { symbol: "Mg", name: "镁",  atomic: 12 },
      { symbol: "Al", name: "铝",  atomic: 13 },
      { symbol: "Si", name: "硅",  atomic: 14 },
      { symbol: "P",  name: "磷",  atomic: 15 },
      { symbol: "S",  name: "硫",  atomic: 16 },
      { symbol: "Cl", name: "氯",  atomic: 17 },
      { symbol: "Ar", name: "氩",  atomic: 18 },
      { symbol: "K",  name: "钾",  atomic: 19 },
      { symbol: "Ca", name: "钙",  atomic: 20 }
    ];

    // ---------- 游戏配置 ----------
    const GRID_SIZE = 20;          // 20x20 网格
    const CELL_SIZE = 30;          // 600px / 20 = 30px
    const TICK_INTERVAL_MS = 160;  // 移动速度

    const canvas = document.getElementById('gameCanvas');
    const ctx = canvas.getContext('2d');
    const scoreDisplay = document.getElementById('scoreDisplay');
    const currentSymbol = document.getElementById('currentSymbol');
    const currentName = document.getElementById('currentName');

    // ---------- 状态变量 ----------
    let snake = [];                // 坐标数组 {x, y}
    let direction = { dx: 1, dy: 0 };    // 当前移动方向
    let nextDirection = { dx: 1, dy: 0 };
    let food = { x: 8, y: 10 };     // 食物坐标
    let foodElement = elements[0];  // 当前食物对应的元素
    let score = 0;
    let gameOver = false;
    let winFlag = false;
    let gameInterval = null;
    let isPaused = false;

    // 元素索引，每吃一个就按顺序轮换 (循环)
    let elementCycleIndex = 0;      // 决定下一个食物元素 (按顺序)

    // ---------- 初始化 ----------
    function initGame() {
      // 清除旧定时器
      if (gameInterval) {
        clearInterval(gameInterval);
        gameInterval = null;
      }

      // 蛇: 长度3，水平放置
      snake = [
        { x: 8, y: 10 },  // 头
        { x: 7, y: 10 },
        { x: 6, y: 10 }
      ];
      // 初始方向向右
      direction = { dx: 1, dy: 0 };
      nextDirection = { dx: 1, dy: 0 };
      score = 0;
      gameOver = false;
      winFlag = false;
      isPaused = false;
      elementCycleIndex = 0;

      // 重置元素循环索引，让食物从第一个元素开始
      // 但是为了初始食物不是蛇身，放置一个安全位置
      generateFood();

      updateScoreAndUI();
      draw();

      // 启动游戏循环
      gameInterval = setInterval(gameTick, TICK_INTERVAL_MS);
    }

    // 更新分数显示 & 当前元素显示
    function updateScoreAndUI() {
      scoreDisplay.textContent = score;
      // 当前食物元素信息展示
      currentSymbol.textContent = foodElement.symbol;
      currentName.textContent = `${foodElement.name} (${foodElement.atomic})`;
    }

    // ---------- 生成新食物 (不与蛇重叠) ----------
    function generateFood() {
      const maxAttempts = 500;
      let attempts = 0;
      let newFood = null;
      let freeCells = [];

      // 如果蛇已经占满网格 → 胜利
      if (snake.length >= GRID_SIZE * GRID_SIZE) {
        winGame();
        return;
      }

      // 收集所有空闲格子 (更高效)
      const snakeSet = new Set(snake.map(seg => `${seg.x},${seg.y}`));
      for (let y = 0; y < GRID_SIZE; y++) {
        for (let x = 0; x < GRID_SIZE; x++) {
          if (!snakeSet.has(`${x},${y}`)) {
            freeCells.push({ x, y });
          }
        }
      }

      if (freeCells.length === 0) {
        // 没有空闲格子, 胜利
        winGame();
        return;
      }

      // 随机选择一个空闲格子
      const randomIndex = Math.floor(Math.random() * freeCells.length);
      newFood = freeCells[randomIndex];

      food = newFood;

      // 根据 elementCycleIndex 选取元素，然后递增循环
      const elemIndex = elementCycleIndex % elements.length;
      foodElement = elements[elemIndex];
      // 下一个食物使用下一个元素 (顺序循环)
      elementCycleIndex = (elemIndex + 1) % elements.length;

      // 更新 UI
      updateScoreAndUI();
    }

    // 胜利处理
    function winGame() {
      if (gameOver) return;
      gameOver = true;
      winFlag = true;
      if (gameInterval) {
        clearInterval(gameInterval);
        gameInterval = null;
      }
      draw(); // 绘制胜利信息
    }

    // ---------- 游戏失败 ----------
    function loseGame() {
      if (gameOver) return;
      gameOver = true;
      winFlag = false;
      if (gameInterval) {
        clearInterval(gameInterval);
        gameInterval = null;
      }
      draw(); // 绘制失败信息
    }

    // ---------- 移动逻辑 ----------
    function moveSnake() {
      if (gameOver || isPaused) return false;

      // 正式采用缓存的方向
      direction = { ...nextDirection };

      // 计算新头部
      const head = snake[0];
      const newHead = {
        x: head.x + direction.dx,
        y: head.y + direction.dy
      };

      // 检查是否吃到食物 (在移动前判断, 因为食物位置不变)
      const willEat = (newHead.x === food.x && newHead.y === food.y);

      // 执行移动: 先在头部插入新坐标
      snake.unshift(newHead);

      if (!willEat) {
        // 没吃到食物: 移除尾部
        snake.pop();
      } else {
        // 吃到食物: 蛇变长 (不pop), 增加分数
        score++;
        scoreDisplay.textContent = score;

        // 检查胜利条件 (蛇长达到400)
        if (snake.length >= GRID_SIZE * GRID_SIZE) {
          winGame();
          return true;
        }

        // 生成新食物 (并更新食物元素)
        generateFood();

        // 如果生成食物时触发了胜利 (没有空闲格子)
        if (gameOver && winFlag) {
          return true;
        }
      }

      // 碰撞检测 (边界 & 自身)
      const headPos = snake[0];
      // 边界
      if (headPos.x < 0 || headPos.x >= GRID_SIZE || headPos.y < 0 || headPos.y >= GRID_SIZE) {
        loseGame();
        return true;
      }
      // 自身碰撞 (从索引1开始检查，因为头部是新插入的)
      for (let i = 1; i < snake.length; i++) {
        if (snake[i].x === headPos.x && snake[i].y === headPos.y) {
          loseGame();
          return true;
        }
      }

      return true;
    }

    // ---------- 定时器驱动 ----------
    function gameTick() {
      if (gameOver || isPaused) return;
      moveSnake();
      draw();
    }

    // ---------- 绘制 ----------
    function draw() {
      ctx.clearRect(0, 0, 600, 600);

      // 绘制网格线 (暗线)
      ctx.strokeStyle = '#1e3b4b';
      ctx.lineWidth = 0.6;
      for (let i = 0; i <= GRID_SIZE; i++) {
        ctx.beginPath();
        ctx.moveTo(i * CELL_SIZE, 0);
        ctx.lineTo(i * CELL_SIZE, canvas.height);
        ctx.strokeStyle = '#1e3b4b';
        ctx.stroke();

        ctx.beginPath();
        ctx.moveTo(0, i * CELL_SIZE);
        ctx.lineTo(canvas.width, i * CELL_SIZE);
        ctx.stroke();
      }

      // 绘制蛇 (带渐变和发光)
      for (let i = 0; i < snake.length; i++) {
        const seg = snake[i];
        const x = seg.x * CELL_SIZE;
        const y = seg.y * CELL_SIZE;
        const padding = i === 0 ? 2 : 4; // 头部稍大
        const radius = 7;

        // 头部颜色更亮，身体渐变
        if (i === 0) {
          ctx.shadowColor = '#5fd1ff';
          ctx.shadowBlur = 16;
          ctx.fillStyle = '#a8e4ff';
        } else {
          // 身体渐变: 从青到绿
          const ratio = i / snake.length;
          const r = 50 + 80 * (1 - ratio);
          const g = 180 + 50 * (1 - ratio);
          const b = 180 + 40 * ratio;
          ctx.shadowColor = '#2a9d8f';
          ctx.shadowBlur = 10;
          ctx.fillStyle = `rgb(${Math.floor(r)}, ${Math.floor(g)}, ${Math.floor(b)})`;
        }

        // 圆角矩形
        ctx.beginPath();
        ctx.roundRect(x + padding/2, y + padding/2, CELL_SIZE - padding, CELL_SIZE - padding, radius);
        ctx.fill();
      }
      // 关闭阴影避免影响食物绘制
      ctx.shadowBlur = 0;
      ctx.shadowColor = 'transparent';

      // 绘制食物 (元素块) —— 用高亮边框 + 元素符号
      if (food) {
        const fx = food.x * CELL_SIZE;
        const fy = food.y * CELL_SIZE;

        // 食物背景发光
        ctx.shadowColor = '#f0e68c';
        ctx.shadowBlur = 24;

        // 圆角背景
        ctx.fillStyle = '#ffe066';
        ctx.beginPath();
        ctx.roundRect(fx + 2, fy + 2, CELL_SIZE - 4, CELL_SIZE - 4, 8);
        ctx.fill();

        // 边框
        ctx.shadowBlur = 18;
        ctx.strokeStyle = '#fff9c4';
        ctx.lineWidth = 2.5;
        ctx.stroke();

        // 重置阴影
        ctx.shadowBlur = 0;

        // 绘制元素符号 (白色加粗)
        ctx.font = 'bold 18px "Segoe UI", "Roboto", system-ui, sans-serif';
        ctx.textAlign = 'center';
        ctx.textBaseline = 'middle';
        ctx.fillStyle = '#1f2e3a';
        ctx.fillText(foodElement.symbol, fx + CELL_SIZE/2, fy + CELL_SIZE/2 - 2);

        // 小号原子序数显示在右下角
        ctx.font = 'bold 10px "Segoe UI", "Roboto", sans-serif';
        ctx.fillStyle = '#2c3e4e';
        ctx.textAlign = 'right';
        ctx.textBaseline = 'bottom';
        ctx.fillText(foodElement.atomic, fx + CELL_SIZE - 5, fy + CELL_SIZE - 4);
      }

      // 游戏结束或胜利覆盖层
      if (gameOver) {
        ctx.fillStyle = 'rgba(0, 0, 0, 0.75)';
        ctx.fillRect(0, 0, 600, 600);

        ctx.textAlign = 'center';
        ctx.textBaseline = 'middle';
        ctx.shadowBlur = 28;
        ctx.shadowColor = winFlag ? '#6fcf97' : '#e76f51';

        if (winFlag) {
          ctx.font = 'bold 46px "Segoe UI", "Roboto", sans-serif';
          ctx.fillStyle = '#b7f0b1';
          ctx.fillText('🏆 元素大师！', 300, 270);
          ctx.font = '30px "Segoe UI", sans-serif';
          ctx.fillStyle = '#d4f7d4';
          ctx.fillText('你记住了所有元素！', 300, 350);
        } else {
          ctx.font = 'bold 48px "Segoe UI", "Roboto", sans-serif';
          ctx.fillStyle = '#ffb4a2';
          ctx.fillText('💥 游戏结束', 300, 270);
          ctx.font = '28px "Segoe UI", sans-serif';
          ctx.fillStyle = '#ffd9cc';
          ctx.fillText('点击「重来」再试一次', 300, 350);
        }

        ctx.shadowBlur = 0;
      }
    }

    // 扩展canvas上下文绘制圆角矩形
    CanvasRenderingContext2D.prototype.roundRect = function (x, y, w, h, r) {
      if (w < 2 * r) r = w / 2;
      if (h < 2 * r) r = h / 2;
      this.moveTo(x + r, y);
      this.lineTo(x + w - r, y);
      this.quadraticCurveTo(x + w, y, x + w, y + r);
      this.lineTo(x + w, y + h - r);
      this.quadraticCurveTo(x + w, y + h, x + w - r, y + h);
      this.lineTo(x + r, y + h);
      this.quadraticCurveTo(x, y + h, x, y + h - r);
      this.lineTo(x, y + r);
      this.quadraticCurveTo(x, y, x + r, y);
      return this;
    };

    // ---------- 方向控制 ----------
    function setDirection(dx, dy) {
      if (gameOver || isPaused) return;
      // 禁止原地掉头（不能与当前方向相反）
      if (direction.dx === -dx && direction.dy === -dy) return;
      // 使用nextDirection作为缓冲，避免快速连续按键导致自碰
      nextDirection = { dx, dy };
    }

    // 键盘事件
    function handleKeydown(e) {
      const key = e.key;
      e.preventDefault();  // 防止页面滚动

      if (key === 'ArrowUp') setDirection(0, -1);
      else if (key === 'ArrowDown') setDirection(0, 1);
      else if (key === 'ArrowLeft') setDirection(-1, 0);
      else if (key === 'ArrowRight') setDirection(1, 0);
      else if (key === ' ' || key === 'Space') {
        // 空格暂停/继续 (可选)
        e.preventDefault();
        if (gameOver) return;
        isPaused = !isPaused;
        if (!isPaused && !gameInterval) {
          // 如果因为暂停没有定时器，重启
          gameInterval = setInterval(gameTick, TICK_INTERVAL_MS);
        }
      }
    }

    // 触摸/点击控制 (滑动检测简化版：点击canvas四角或使用滑动？为了简单用键盘提示)
    // 增加鼠标点击 Canvas 上下左右区域移动 (适合触屏)
    function handleCanvasClick(e) {
      if (gameOver) return;

      const rect = canvas.getBoundingClientRect();
      const scaleX = canvas.width / rect.width;
      const scaleY = canvas.height / rect.height;

      const mouseX = (e.clientX - rect.left) * scaleX;
      const mouseY = (e.clientY - rect.top) * scaleY;

      // 相对于中心的方向
      const centerX = 300;
      const centerY = 300;
      const dx = mouseX - centerX;
      const dy = mouseY - centerY;

      if (Math.abs(dx) > Math.abs(dy)) {
        // 左右
        if (dx > 0) setDirection(1, 0);
        else setDirection(-1, 0);
      } else {
        // 上下
        if (dy > 0) setDirection(0, 1);
        else setDirection(0, -1);
      }
    }

    // 重置游戏
    function restartGame() {
      if (gameInterval) {
        clearInterval(gameInterval);
        gameInterval = null;
      }
      initGame();
    }

    // ---------- 事件绑定 ----------
    window.addEventListener('keydown', (e) => {
      if (e.key.startsWith('Arrow') || e.key === ' ' || e.key === 'Space') {
        e.preventDefault();
      }
      handleKeydown(e);
    });

    canvas.addEventListener('click', handleCanvasClick);

    document.getElementById('restartBtn').addEventListener('click', restartGame);

    // 防止页面方向键滚动
    window.addEventListener('keydown', function(e) {
      if (e.key === 'ArrowUp' || e.key === 'ArrowDown' || e.key === 'ArrowLeft' || e.key === 'ArrowRight') {
        e.preventDefault();
      }
    }, { passive: false });

    // 启动游戏
    initGame();
  })();
</script>
</body>
</html>
