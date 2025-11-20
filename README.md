<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title> أسئلة دينية</title>
<style>
  :root{
    --bg-primary: #0a0e17;
    --bg-secondary: #121826;
    --accent-primary: #e62429; /* Red like COD */
    --accent-secondary: #ffcc00; /* Gold accent */
    --text-primary: #ffffff;
    --text-secondary: #a0a0c0;
    --panel-bg: rgba(18, 24, 38, 0.85);
    --cod-font: 'Arial', sans-serif;
    --cod-gradient: linear-gradient(90deg, #1a1a1a 0%, #0a0a0a 100%);
  }
  
  *{box-sizing:border-box; margin:0; padding:0;}
  html,body{height:100%; overflow-x:hidden;}
  body{
    margin:0;
    background: radial-gradient(circle at 10% 20%, rgba(0, 40, 80, 0.3) 0%, transparent 40%),
                radial-gradient(circle at 90% 80%, rgba(60, 20, 80, 0.2) 0%, transparent 40%),
                linear-gradient(180deg, var(--bg-primary), var(--bg-secondary));
    color: var(--text-primary);
    font-family: var(--cod-font);
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    padding: 10px;
    overflow: hidden;
    position: relative;
  }
  
  .app {
    width: 100%;
    max-width: 1200px;
    height: 90vh;
    display: flex;
    flex-direction: column;
    background: var(--panel-bg);
    border-radius: 16px;
    border: 2px solid var(--accent-primary);
    box-shadow: 0 0 40px rgba(230, 36, 41, 0.3),
                inset 0 0 20px rgba(0, 0, 0, 0.5);
    overflow: hidden;
    position: relative;
  }
  
  header {
    height: 70px;
    background: rgba(10, 14, 23, 0.9);
    border-bottom: 2px solid var(--accent-primary);
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 30px;
    position: relative;
    z-index: 10;
  }
  
  .cod-logo {
    display: flex;
    align-items: center;
    gap: 15px;
  }
  
  .cod-logo-img {
    width: 50px;
    height: 50px;
    background: var(--cod-gradient);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    font-size: 24px;
    color: var(--accent-primary);
    box-shadow: 0 0 15px rgba(230, 36, 41, 0.5);
    border: 2px solid var(--accent-primary);
    text-shadow: 0 0 10px rgba(230, 36, 41, 0.7);
  }
  
  .game-title {
    font-size: 28px;
    font-weight: 800;
    color: var(--accent-primary);
    text-shadow: 0 0 10px rgba(230, 36, 41, 0.7);
    letter-spacing: 1px;
  }
  
  .main-content {
    flex: 1;
    display: flex;
    padding: 20px;
    gap: 20px;
    position: relative;
  }
  
  .left-sidebar {
    width: 250px;
    background: rgba(26, 43, 77, 0.7);
    border-radius: 12px;
    border: 1px solid rgba(230, 36, 41, 0.3);
    padding: 15px;
    display: flex;
    flex-direction: column;
    gap: 15px;
    overflow-y: auto;
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.5);
  }
  
  .sidebar-title {
    color: var(--accent-primary);
    font-size: 18px;
    font-weight: bold;
    text-align: center;
    margin-bottom: 10px;
    text-shadow: 0 0 5px rgba(230, 36, 41, 0.5);
  }
  
  .player-card {
    background: rgba(10, 14, 23, 0.7);
    border-radius: 8px;
    padding: 12px;
    border: 1px solid rgba(230, 36, 41, 0.1);
    transition: all 0.3s ease;
  }
  
  .player-card:hover {
    border-color: var(--accent-primary);
    transform: translateX(5px);
  }
  
  .player-name {
    font-weight: bold;
    color: var(--accent-primary);
    font-size: 16px;
    margin-bottom: 5px;
  }
  
  .player-score {
    color: #4fc3f7;
    font-weight: bold;
  }
  
  .map-area {
    flex: 1;
    background: linear-gradient(135deg, #0a0e17 0%, #1a2b4d 100%);
    border-radius: 16px;
    border: 2px solid rgba(230, 36, 41, 0.3);
    overflow: hidden;
    display: flex;
    flex-direction: column;
    position: relative;
    box-shadow: 0 0 30px rgba(0, 100, 255, 0.2);
  }
  
  .map-header {
    height: 50px;
    background: rgba(10, 14, 23, 0.8);
    border-bottom: 2px solid var(--accent-primary);
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 20px;
  }
  
  .map-title {
    font-size: 20px;
    color: var(--accent-primary);
    font-weight: bold;
  }
  
  .map-content {
    flex: 1;
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
  }
  
  .map-background {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: radial-gradient(circle, rgba(10, 14, 23, 0.8) 0%, transparent 70%);
    z-index: 0;
  }
  
  .cod-btn {
    width: 260px;
    padding: 14px 18px;
    border-radius: 999px;
    border: 1px solid rgba(0,0,0,0.5);
    background: var(--cod-gradient);
    box-shadow: 0 10px 30px rgba(2,6,23,0.6), inset 0 -4px 18px rgba(0,0,0,0.25);
    color: #fff;
    font-weight: 800;
    letter-spacing: 1px;
    text-transform: uppercase;
    cursor: pointer;
    transition: transform .15s ease, box-shadow .15s ease;
  }
  
  .cod-btn:hover {
    transform: translateY(-6px) scale(1.02);
    box-shadow: 0 18px 40px rgba(230, 36, 41, 0.75);
  }
  
  .cod-btn.small {
    width: 200px;
    padding: 10px 14px;
    font-size: 0.95rem;
  }
  
  .screen {
    display: none;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0;
    transition: opacity 0.5s ease;
  }
  
  .screen.active {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    opacity: 1;
  }
  
  .countdown-display {
    font-size: 150px;
    font-weight: 900;
    color: var(--accent-secondary);
    text-shadow: 0 0 30px rgba(255, 204, 0, 0.8);
    animation: pulse 1s infinite;
  }
  
  @keyframes pulse {
    0% { transform: scale(1); opacity: 1; }
    50% { transform: scale(1.05); opacity: 0.8; }
    100% { transform: scale(1); opacity: 1; }
  }
  
  .question-card {
    background: rgba(10, 14, 23, 0.9);
    border-radius: 16px;
    border: 2px solid rgba(255, 204, 0, 0.4);
    padding: 25px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.6);
    max-width: 800px;
    margin: 0 auto;
  }
  
  .question-text {
    font-size: 24px;
    color: white;
    text-align: center;
    margin-bottom: 30px;
    line-height: 1.5;
    min-height: 120px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .options-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
  }
  
  .option {
    background: var(--cod-gradient);
    border: 2px solid rgba(230, 36, 41, 0.2);
    border-radius: 12px;
    padding: 20px;
    color: white;
    font-size: 18px;
    cursor: pointer;
    transition: all 0.3s ease;
    text-align: center;
  }
  
  .option:hover {
    border-color: var(--accent-primary);
    transform: scale(1.03);
    box-shadow: 0 8px 25px rgba(230, 36, 41, 0.4);
  }
  
  .option.correct {
    background: linear-gradient(135deg, #2ecc71 0%, #27ae60 100%);
    border-color: #2ecc71;
  }
  
  .option.incorrect {
    background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
    border-color: #e74c3c;
  }
  
  .timer-display {
    position: absolute;
    top: 20px;
    right: 20px;
    background: rgba(231, 76, 60, 0.9);
    border-radius: 50%;
    width: 60px;
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    font-size: 24px;
    color: white;
    box-shadow: 0 0 20px rgba(231, 76, 60, 0.7);
    border: 3px solid white;
    z-index: 100;
  }
  
  .player-info {
    position: absolute;
    bottom: 20px;
    left: 0;
    right: 0;
    text-align: center;
    color: var(--accent-secondary);
    font-weight: bold;
    font-size: 18px;
    text-shadow: 0 0 10px rgba(255, 204, 0, 0.5);
  }
  
  .row {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    margin-top: 8px;
  }
  
  .room-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-top: 12px;
  }
  
  .team-col {
    background: rgba(255,255,255,0.02);
    padding: 12px;
    border-radius: 10px;
    min-height: 160px;
  }
  
  .team-title {
    font-weight: 800;
    color: var(--accent-secondary);
    margin-bottom: 8px;
    display: flex;
    gap: 8px;
    align-items: center;
  }
  
  .slot {
    background: rgba(255,255,255,0.01);
    padding: 10px;
    margin-bottom: 10px;
    border-radius: 8px;
    border: 1px dashed rgba(255,255,255,0.04);
    display: flex;
    align-items: center;
    justify-content: space-between;
    cursor: grab;
  }
  
  .player-item {
    padding: 8px 10px;
    border-radius: 8px;
    background: linear-gradient(90deg, #0b1220, #12374a);
    color: var(--accent-secondary);
    font-weight: 700;
    cursor: grab;
  }
  
  .progress-wrap {
    background: rgba(255,255,255,0.04);
    height: 12px;
    border-radius: 8px;
    overflow: hidden;
    margin-top: 10px;
  }
  
  .progress-bar {
    height: 100%;
    width: 0%;
    background: linear-gradient(90deg, #ffd166, #ffcc00);
    transition: width .4s ease;
  }
  
  .badge {
    background: rgba(255,255,255,0.06);
    padding: 8px 12px;
    border-radius: 8px;
    color: rgba(255,255,255,0.9);
    margin-bottom: 5px;
  }
  
  .modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.5);
    align-items: center;
    justify-content: center;
  }
  
  .modal-content {
    background-color: rgba(10, 14, 23, 0.95);
    border-radius: 12px;
    padding: 20px;
    width: 90%;
    max-width: 800px;
    max-height: 80vh;
    overflow-y: auto;
    border: 1px solid var(--accent-primary);
    box-shadow: 0 30px 80px rgba(230, 36, 41, 0.5);
  }
  
  .close {
    color: #aaa;
    float: left;
    font-size: 28px;
    font-weight: bold;
    cursor: pointer;
  }
  
  .close:hover {
    color: var(--accent-secondary);
  }
  
  .question-item {
    padding: 10px;
    border-bottom: 1px solid rgba(255,255,255,0.05);
  }
  
  .question-item:last-child {
    border-bottom: none;
  }
  
  footer {
    height: 50px;
    background: rgba(10, 14, 23, 0.9);
    border-top: 2px solid var(--accent-primary);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--text-secondary);
    font-size: 14px;
  }
  
  @media (max-width: 1200px) {
    .left-sidebar {
      width: 220px;
    }
  }
  
  @media (max-width: 900px) {
    .main-content {
      flex-direction: column;
    }
    
    .left-sidebar {
      width: 100%;
      height: auto;
    }
    
    .options-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
</head>
<body>
  <div class="app" role="application" aria-label="Call of Duty: أسئلة دينية">
    <header>
      <div class="cod-logo">
        <div class="cod-logo-img">ديني</div>
        <div class="game-title">Call of Duty: الأسئلة الدينية</div>
      </div>
    </header>
    
    <div class="main-content">
      <div class="left-sidebar">
        <div class="sidebar-title">اللاعبون</div>
        <div class="player-card" id="player1-card">
          <div class="player-name">اللاعب 1</div>
          <div class="player-score">النقاط: 0</div>
        </div>
        <div class="player-card" id="player2-card" style="display: none;">
          <div class="player-name">اللاعب 2</div>
          <div class="player-score">النقاط: 0</div>
        </div>
        <div class="player-card" id="player3-card" style="display: none;">
          <div class="player-name">اللاعب 3</div>
          <div class="player-score">النقاط: 0</div>
        </div>
        <div class="player-card" id="player4-card" style="display: none;">
          <div class="player-name">اللاعب 4</div>
          <div class="player-score">النقاط: 0</div>
        </div>
      </div>
      
      <div class="map-area">
        <div class="map-header">
          <div class="map-title">خريطة القتال</div>
          <div class="timer-display" id="timer-display">30</div>
        </div>
        <div class="map-content">
          <div class="map-background"></div>
          
          <div id="screen-main" class="screen active">
            <h2 style="color: var(--accent-primary); text-shadow: 0 0 10px rgba(230, 36, 41, 0.7); margin-bottom: 30px; font-size: 32px;">
              CALL OF DUTY: الأسئلة الدينية
            </h2>
            <div class="row" style="flex-direction: column; gap: 10px;">
              <button id="startGame" class="cod-btn">ابدأ اللعبة</button>
              <button id="aboutBtn" class="cod-btn small">حول اللعبة</button>
              <button id="questionsListBtn" class="cod-btn small">قائمة الأسئلة</button>
            </div>
          </div>
          
          <div id="screen-mode" class="screen">
            <h2 style="color: var(--accent-primary); text-shadow: 0 0 10px rgba(230, 36, 41, 0.7); margin-bottom: 30px; font-size: 28px;">
              اختر نمط اللعب
            </h2>
            <div class="row">
              <button id="modeSolo" class="cod-btn">لكل لاعب لنفسه</button>
              <button id="modeMulti" class="cod-btn">مباراة جماعية</button>
            </div>
            <button id="backFromMode" class="cod-btn small" style="margin-top: 20px;">العودة</button>
          </div>
          
          <div id="screen-players-solo" class="screen">
            <h2 style="color: var(--accent-primary); text-shadow: 0 0 10px rgba(230, 36, 41, 0.7); margin-bottom: 30px; font-size: 28px;">
              عدد اللاعبين (1-4)
            </h2>
            <div class="row">
              <button id="soloPlayers1" class="cod-btn">1 لاعب</button>
              <button id="soloPlayers2" class="cod-btn">2 لاعبين</button>
            </div>
            <div class="row" style="margin-top: 10px;">
              <button id="soloPlayers3" class="cod-btn">3 لاعبين</button>
              <button id="soloPlayers4" class="cod-btn">4 لاعبين</button>
            </div>
            <button id="backFromPlayersSolo" class="cod-btn small" style="margin-top: 20px;">العودة</button>
          </div>
          
          <div id="screen-players-multi" class="screen">
            <h2 style="color: var(--accent-primary); text-shadow: 0 0 10px rgba(230, 36, 41, 0.7); margin-bottom: 30px; font-size: 28px;">
              عدد اللاعبين (2-4)
            </h2>
            <div class="row">
              <button id="multiPlayers2" class="cod-btn">2 لاعبين</button>
              <button id="multiPlayers3" class="cod-btn">3 لاعبين</button>
              <button id="multiPlayers4" class="cod-btn">4 لاعبين</button>
            </div>
            <button id="backFromPlayersMulti" class="cod-btn small" style="margin-top: 20px;">العودة</button>
          </div>
          
          <div id="screen-questions" class="screen">
            <h2 style="color: var(--accent-primary); text-shadow: 0 0 10px rgba(230, 36, 41, 0.7); margin-bottom: 30px; font-size: 28px;">
              عدد الأسئلة
            </h2>
            <div class="row" style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; margin: 20px 0;">
              <button id="q10" class="cod-btn small">10</button>
              <button id="q20" class="cod-btn small">20</button>
              <button id="q30" class="cod-btn small">30</button>
              <button id="q40" class="cod-btn small">40</button>
              <button id="q50" class="cod-btn small">50</button>
              <button id="q100" class="cod-btn small">100</button>
            </div>
            <button id="backFromQuestions" class="cod-btn small">العودة</button>
          </div>
          
          <div id="screen-names" class="screen">
            <h2 style="color: var(--accent-primary); text-shadow: 0 0 10px rgba(230, 36, 41, 0.7); margin-bottom: 30px; font-size: 28px;">
              أسماء اللاعبين
            </h2>
            <div id="namesInputArea" style="width: 100%; max-width: 500px; margin: 20px auto;"></div>
            <div class="row" style="margin-top: 20px;">
              <button id="startNames" class="cod-btn">تأكيد الأسماء</button>
              <button id="backFromNames" class="cod-btn small">العودة</button>
            </div>
          </div>
          
          <div id="screen-distribution" class="screen">
            <h2 style="color: var(--accent-primary); text-shadow: 0 0 10px rgba(230, 36, 41, 0.7); margin-bottom: 30px; font-size: 28px;">
              توزيع اللاعبين
            </h2>
            <div class="row">
              <button id="distRandom" class="cod-btn">توزيع عشوائي</button>
              <button id="distCustom" class="cod-btn">توزيع يدوي</button>
            </div>
            <button id="backFromDist" class="cod-btn small" style="margin-top: 20px;">العودة</button>
          </div>
          
          <div id="screen-custom" class="screen">
            <h2 style="color: var(--accent-primary); text-shadow: 0 0 10px rgba(230, 36, 41, 0.7); margin-bottom: 20px; font-size: 24px;">
              اسحب اللاعبين للفِرَق
            </h2>
            <div class="room-grid">
              <div class="team-col" id="teamA">
                <div class="team-title">الفريق الأول</div>
                <div id="slotA1" class="slot" data-slot="A1"></div>
                <div id="slotA2" class="slot" data-slot="A2"></div>
              </div>
              <div class="team-col" id="teamB">
                <div class="team-title">الفريق الثاني</div>
                <div id="slotB1" class="slot" data-slot="B1"></div>
                <div id="slotB2" class="slot" data-slot="B2"></div>
              </div>
            </div>
            <div style="margin-top:12px;">
              <h4 style="margin:0 0 8px 0;color:rgba(255,255,255,0.9); text-align: center;">اللاعبون</h4>
              <div id="playersList" style="display:flex; gap:8px; flex-wrap:wrap; justify-content: center;"></div>
            </div>
            <div class="row" style="margin-top: 20px;">
              <button id="startFromCustom" class="cod-btn">ابدأ اللعبة</button>
              <button id="backFromCustom" class="cod-btn small">العودة</button>
            </div>
          </div>
          
          <div id="screen-countdown" class="screen">
            <div class="countdown-display" id="countdown">5</div>
            <div class="player-info" id="countdownPlayerInfo">اللاعب: اللاعب 1</div>
          </div>
          
          <div id="screen-game" class="screen">
            <div class="question-card">
              <div class="question-text" id="questionText">سيظهر السؤال هنا</div>
              <div class="options-grid" id="optionsGrid">
                <!-- Options will be added dynamically -->
              </div>
              <div class="progress-wrap">
                <div class="progress-bar" id="progressBar"></div>
              </div>
            </div>
            <div class="player-info" id="currentPlayerInfo">اللاعب: اللاعب 1</div>
          </div>
          
          <div id="screen-end" class="screen">
            <h2 style="color: var(--accent-primary); text-shadow: 0 0 10px rgba(230, 36, 41, 0.7); margin-bottom: 30px; font-size: 32px;">
              نهاية اللعبة
            </h2>
            <div class="badge" style="font-size: 24px; padding: 15px; margin-bottom: 20px;">
              إجمالي النقاط: <strong id="finalScore">0</strong>
            </div>
            <div id="rankingSection" style="width: 100%; max-width: 600px; margin: 0 auto;">
              <h3 style="color: var(--accent-secondary); margin-bottom: 15px; text-align: center;">ترتيب الفرق واللاعبين</h3>
              <div id="rankingList"></div>
            </div>
            <div class="row" style="margin-top: 30px;">
              <button id="playAgain" class="cod-btn">لعب مرة أخرى</button>
              <button id="backToMain" class="cod-btn small">القائمة الرئيسية</button>
            </div>
          </div>
        </div>
      </div>
    </div>
    
    <footer>
      <span>Call of Duty Mobile Style — الإصدار 1.0</span>
    </footer>
    
    <!-- Modal for Questions List -->
    <div id="questionsModal" class="modal">
      <div class="modal-content">
        <span class="close">&times;</span>
        <h3 style="color: var(--accent-primary); text-align: center; margin-bottom: 20px;">قائمة الأسئلة</h3>
        <div id="questionsListContent"></div>
      </div>
    </div>
  </div>

<script>
// Call of Duty style game interface with all original features
const screens = {
  main: document.getElementById('screen-main'),
  mode: document.getElementById('screen-mode'),
  playersSolo: document.getElementById('screen-players-solo'),
  playersMulti: document.getElementById('screen-players-multi'),
  questions: document.getElementById('screen-questions'),
  names: document.getElementById('screen-names'),
  distribution: document.getElementById('screen-distribution'),
  custom: document.getElementById('screen-custom'),
  countdown: document.getElementById('screen-countdown'),
  game: document.getElementById('screen-game'),
  end: document.getElementById('screen-end')
};

const playerCards = {
  1: document.getElementById('player1-card'),
  2: document.getElementById('player2-card'),
  3: document.getElementById('player3-card'),
  4: document.getElementById('player4-card')
};

// Game state
let mode = 'solo'; // 'solo' or 'multi'
let numPlayers = 1;
let numQuestions = 10;
let currentPlayerIndex = 0;
let currentQuestionIndex = 0;
let scores = [0, 0, 0, 0];
let playerNames = ['اللاعب 1', 'اللاعب 2', 'اللاعب 3', 'اللاعب 4'];
let teams = [
  { id: 'A', name: 'الفريق الأول', score: 0, players: [0, 2] },
  { id: 'B', name: 'الفريق الثاني', score: 0, players: [1, 3] }
];
let currentQuestions = [];

// Original Question Bank (100 questions)
const QUESTION_BANK = [
  {"question":"من هو أول نبي خلقه الله؟","option1":"نوح","option2":"آدم","option3":"إبراهيم","option4":"موسى","correct":"آدم"},
  {"question":"كم عدد سور القرآن الكريم؟","option1":"114","option2":"99","option3":"120","option4":"1144","correct":"114"},
  {"question":"ما هي أطول سورة في القرآن؟","option1":"سورة البقرة","option2":"سورة آل عمران","option3":"سورة النساء","option4":"سورة المائدة","correct":"سورة البقرة"},
  {"question":"ما هي أقصر سورة في القرآن؟","option1":"سورة الكوثر","option2":"سورة الناس","option3":"سورة الفلق","option4":"سورة الإخلاص","correct":"سورة الكوثر"},
  {"question":"ما اسم مكة المكرمة في القرآن؟","option1":"أرض الحجاز","option2":"بكة","option3":"مكة","option4":"تهامة","correct":"بكة"},
  {"question":"ما هي القِبلة الأولى للمسلمين قبل تحويلها إلى الكعبة؟","option1":"القدس (المسجد الأقصى)","option2":"الكعبة","option3":"مسجد قباء","option4":"لا قبلة","correct":"القدس (المسجد الأقصى)"},
  {"question":"ما عدد ركعات صلاة الفجر؟","option1":"ركعتان","option2":"أربع ركعات","option3":"ثلاث ركعات","option4":"ركعة واحدة","correct":"ركعتان"},
  {"question":"كم عدد أركان الإسلام؟","option1":"3","option2":"5","option3":"6","option4":"4","correct":"5"},
  {"question":"ما هو اسم السورة التي تُسمى قلب القرآن؟","option1":"يس","option2":"الرحمن","option3":"الواقعة","option4":"القدر","correct":"يس"},
  {"question":"من هو خاتم الأنبياء؟","option1":"موسى","option2":"عيسى","option3":"محمد","option4":"إبراهيم","correct":"محمد"},
  {"question":"ما اسم سورة تُعادل ثلث القرآن في بعض الأقوال؟","option1":"الإخلاص","option2":"الفاتحة","option3":"الكوثر","option4":"الناس","correct":"الإخلاص"},
  {"question":"ما اسم ماء أعطاه الله لنبينا لإطعام القوم في بعض الروايات (الكوثر)؟","option1":"الكوثر","option2":"النيل","option3":"الفرات","option4":"الأنهار","correct":"الكوثر"},
  {"question":"من الذي بنى الكعبة؟","option1":"إبراهيم وإسماعيل","option2":"النبي محمد","option3":"قريش","option4":"آدم","correct":"إبراهيم وإسماعيل"},
  {"question":"ما هي صفة الصدقة الواجبة؟","option1":"زكاة","option2":"صدقة نافلة","option3":"هدية","option4":"زكاة واجبة","correct":"زكاة واجبة"},
  {"question":"من هو سيدنا عيسى في الإسلام؟","option1":"نبي ورسول","option2":"إله","option3":"كبير الأنبياء","option4":"ملك","correct":"نبي ورسول"},
  {"question":"كم عدد أسماء الله الحسنى المتداولة؟","option1":"99","option2":"100","option3":"85","option4":"60","correct":"99"},
  {"question":"ما اسم الليلة التي أُنزل فيها القرآن على النبي؟","option1":"ليلة القدر","option2":"ليلة الإسراء","option3":"ليلة النصف","option4":"ليلة المعراج","correct":"ليلة القدر"},
  {"question":"ما اسم الغار الذي تلقى فيه الرسول أول آيات الوحي؟","option1":"غار ثور","option2":"غار حراء","option3":"غار ثعلبة","option4":"غار بني سليم","correct":"غار حراء"},
  {"question":"من هو الصحابي الذي كان مؤذن الرسول؟","option1":"بلال بن رباح","option2":"عمر بن الخطاب","option3":"أبو بكر","option4":"علي بن أبي طالب","correct":"بلال بن رباح"},
  {"question":"ما هي الصلاة التي تُقضى في السفر؟","option1":"الظهر والعصر جمع","option2":"العصر فقط","option3":"لا توجد صلاة في السفر","option4":"تُؤجل","correct":"الظهر والعصر جمع"},
  {"question":"كم عدد ركعات صلاة العشاء بحسب المذهب الشائع؟","option1":"4","option2":"3","option3":"2","option4":"5","correct":"4"},
  {"question":"ما اسم جبريل عليه السلام بالنسبة للوحي؟","option1":"ملك الوحي","option2":"ملك الموت","option3":"ملك الجبال","option4":"ملك النار","correct":"ملك الوحي"},
  {"question":"ما اسم سورة فيها آية الكرسي؟","option1":"البقرة","option2":"الكهف","option3":"الفاتحة","option4":"الرحمن","correct":"البقرة"},
  {"question":"أي ركن من أركان الإيمان يتعلق بالإيمان باليوم الآخر؟","option1":"ركن","option2":"أركان الإيمان","option3":"ليس ركن","option4":"فرض","correct":"أركان الإيمان"},
  {"question":"ما اسم السورة التي افتتحت بـ {الحمد لله رب العالمين}؟","option1":"الفاتحة","option2":"البقرة","option3":"الأنعام","option4":"الرحمن","correct":"الفاتحة"},
  {"question":"من صاحب قول: 'إنما الأعمال بالنيات'؟","option1":"النبي محمد ﷺ","option2":"عمر بن الخطاب","option3":"أبو بكر","option4":"علي","correct":"النبي محمد ﷺ"},
  {"question":"ما هي الركن الثالث من أركان الإسلام؟","option1":"الصلاة","option2":"الزكاة","option3":"الصوم","option4":"الحج","correct":"الزكاة"},
  {"question":"كم عدد أجزاء القرآن؟","option1":"30 جزءا","option2":"10 أجزاء","option3":"20 جزءا","option4":"40 جزءا","correct":"30 جزءا"},
  {"question":"من هو الذي أسري به إلى المسجد الأقصى؟","option1":"محمد ﷺ","option2":"موسى","option3":"عيسى","option4":"إبراهيم","correct":"محمد ﷺ"},
  {"question":"ما لغة القرآن الأصلية؟","option1":"العربية","option2":"الآرامية","option3":"الفارسية","option4":"السريانية","correct":"العربية"},
  {"question":"ما معنى كلمة 'سورة'؟","option1":"آية","option2":"باب","option3":"حمل","option4":"جزء","correct":"باب/قسم من القرآن (سورة = فصل)"},
  {"question":"كم عدد الركعات في صلاة الظهر؟","option1":"4","option2":"2","option3":"3","option4":"1","correct":"4"},
  {"question":"ما هي ركن الصوم؟","option1":"النية والإمساك عن الطعام والشراب من الفجر إلى المغرب","option2":"الصلاة","option3":"الزكاة","option4":"الحج","correct":"النية والإمساك عن الطعام والشراب من الفجر إلى المغرب"},
  {"question":"ما اسم معجزة النبي محمد الكتاب المحفوظ؟","option1":"القرآن","option2":"الزبور","option3":"التوراة","option4":"الإنجيل","correct":"القرآن"},
  {"question":"من هو الصحابي المعروف بلقب 'سيف الله المسلول'؟","option1":"خالد بن الوليد","option2":"عمر بن الخطاب","option3":"أبو بكر","option4":"علي بن أبي طالب","correct":"خالد بن الوليد"},
  {"question":"ما اسم النبي الذي اشتهر بالحكمة والملك؟","option1":"سليمان","option2":"داوود","option3":"أيوب","option4":"يوسف","correct":"سليمان"},
  {"question":"كم عدد الصلوات المفروضة يومياً؟","option1":"5","option2":"3","option3":"4","option4":"6","correct":"5"},
  {"question":"ما اسم الليلة التي تُسمى 'ليلة القدر' في أي شهر؟","option1":"شهر رمضان","option2":"شوال","option3":"ذو الحجة","option4":"رجب","correct":"شهر رمضان"},
  {"question":"ما هو الركن الخامس من أركان الإسلام؟","option1":"الحج","option2":"الصيام","option3":"الزكاة","option4":"الأسرة","correct":"الحج"},
  {"question":"ما اسم السورة التي تُقرأ غالبًا في صلاة الفجر؟","option1":"الفاتحة","option2":"الكوثر","option3":"الإخلاص","option4":"الناس","correct":"الفاتحة"},
  {"question":"ما اسم أم المؤمنين التي روت الكثير من الأحاديث؟","option1":"عائشة","option2":"حفصة","option3":"أم سلمة","option4":"زيد","correct":"عائشة"},
  {"question":"من الذي ابتلعته الحوت؟","option1":"يونس","option2":"موسى","option3":"إبراهيم","option4":"عيسى","correct":"يونس"},
  {"question":"ما اسم النهر الذي سُمي في القرآن كآية؟","option1":"الكوثر","option2":"النيل","option3":"الفرات","option4":"دجلة","correct":"الكوثر"},
  {"question":"ما اسم السورة التي تحدثت عن قصة أصحاب الكهف؟","option1":"الكهف","option2":"يونس","option3":"النحل","option4":"القصص","correct":"الكهف"},
  {"question":"ما معنى كلمة 'إسلام'؟","option1":"الإذعان والانقياد لله","option2":"العمل","option3":"الصوم","option4":"الزكاة","correct":"الإذعان والانقياد لله"},
  {"question":"من نبي الله الذي تحولت عصاه إلى ثعبان؟","option1":"موسى","option2":"إبراهيم","option3":"نوح","option4":"عيسى","correct":"موسى"},
  {"question":"ما اسم مكة قبل الإسلام بكلمة مذكورة في القرآن؟","option1":"بكة","option2":"طيبة","option3":"مدين","option4":"يثرب","correct":"بكة"},
  {"question":"ما اسم المدينة التي هاجر إليها النبي؟","option1":"المدينة (يثرب)","option2":"مكة","option3":"طائف","option4":"الطائف","correct":"المدينة (يثرب)"},
  {"question":"من هو الصحابي الذي كتب الوحي للنبي؟","option1":"عبد الله بن مسعود","option2":"عمر","option3":"أبو بكر","option4":"علي","correct":"عبد الله بن مسعود"},
  {"question":"ما هي السورة التي يبدأ بها كل كتاب؟","option1":"الفاتحة","option2":"البقرة","option3":"آل عمران","option4":"الكوثر","correct":"الفاتحة"},
  {"question":"من هو النبي الذي بنى سفينة أنقذت المؤمنين؟","option1":"نوح","option2":"نوستير","option3":"يونس","option4":"إبراهيم","correct":"نوح"},
  {"question":"ما اسم أم النبي محمد؟","option1":"آمنة بنت وهب","option2":"آمنة","option3":"أميمة","option4":"خديجة","correct":"آمنة بنت وهب"},
  {"question":"من هو الذي لقب بالصديق؟","option1":"أبو بكر","option2":"عمر","option3":"عثمان","option4":"علي","correct":"أبو بكر"},
  {"question":"ما معنى كلمة 'سُنَّة'؟","option1":"طريقة النبي العملية","option2":"كتاب","option3":"حكاية","option4":"حكم قضائي","correct":"طريقة النبي العملية"},
  {"question":"ما الشيء الأول الذي سيُسأل عنه المرء يوم القيامة؟","option1":"الصلاة","option2":"الزكاة","option3":"الصدقة","option4":"السرير","correct":"الصلاة"},
  {"question":"ما الحكم في الصلاة إذا فاتت بسبب نوم؟","option1":"تُقضى","option2":"لا تُقضى","option3":"تعوض بصلاة أخرى","option4":"صلاة نافلة","correct":"تُقضى"},
  {"question":"ما اسم الجبال التي بنيت للأرض؟","option1":"الجبال","option2":"الأحجار","option3":"لا توجد","option4":"مشكلة","correct":"الجبال (خلق الله الجبال لتثبيت الأرض)"},
  {"question":"من هو خليل الله؟","option1":"إبراهيم","option2":"موسى","option3":"هارون","option4":"داوود","correct":"إبراهيم"},
  {"question":"ما اسم الملك الذي آمن بسليمان وناله علم؟","option1":"بلقيس","option2":"بلعم","option3":"بلدار","option4":"بلكس","correct":"بلقيس"},
  {"question":"ما اسم النبي الذي بيعته قومه؟","option1":"نوح","option2":"إدريس","option3":"هود","option4":"صالح","correct":"هود"},
  {"question":"كم عدد شرائح القرآن (أجزاء)؟","option1":"30","option2":"20","option3":"15","option4":"10","correct":"30"},
  {"question":"ما الاسم الآخر لسورة الفلق؟","option1":"الفلق","option2":"القدر","option3":"الناس","option4":"الفاتحة","correct":"الفلق"},
  {"question":"ما هي الصلاة التي تُؤدى قبل الظهر؟","option1":"ظهر","option2":"فجر","option3":"عصر","option4":"مغرب","correct":"فجر"},
  {"question":"من هو النبي الذي أجرى له الله معجزات عديدة منها شِفاء المرضى؟","option1":"عيسى","option2":"يونس","option3":"نوح","option4":"أيوب","correct":"عيسى"},
  {"question":"ما هي العبادات التي تُقَدَّم للصالحين؟","option1":"الصدقات","option2":"اللذات","option3":"الترفيه","option4":"الطيبات","correct":"الصدقات"},
  {"question":"ما معنى 'الزكاة'؟","option1":"طهارة المال","option2":"زيادة المال","option3":"ادخار","option4":"الإنفاق","correct":"طهارة المال"},
  {"question":"من الذي بنى مدينة يثرب؟","option1":"قبائل متعددة (يثرب تطورت تاريخيًا)","option2":"النبي","option3":"آدم","option4":"لوط","correct":"قبائل متعددة (يثرب تطورت تاريخيًا)"},
  {"question":"ما اسم السورة التي تُعرف بـ 'قلب القرآن'؟","option1":"يس","option2":"الرحمن","option3":"الواقعة","option4":"المؤمنون","correct":"يس"},
  {"question":"ما اسم آخر سورة في المصحف؟","option1":"الناس","option2":"الفاتحة","option3":"الكوثر","option4":"الهمزة","correct":"الناس"},
  {"question":"أين وُلد النبي محمد ﷺ؟","option1":"مكة","option2":"المدينة","option3":"اليمن","option4":"الشام","correct":"مكة"},
  {"question":"ما اسم السورة التي تتضمن آية الكرسي؟","option1":"البقرة","option2":"آل عمران","option3":"النور","option4":"الأنفال","correct":"البقرة"},
  {"question":"ما معنى 'حديث'؟","option1":"قول أو فعل أو تقرير للنبي","option2":"سورة","option3":"آية","option4":"شرح","correct":"قول أو فعل أو تقرير للنبي"},
  {"question":"كم عدد الأنبياء المذكورين في القرآن تقريبًا؟","option1":"نحو 25 اسمًا مذكورًا","option2":"100","option3":"10","option4":"5","correct":"نحو 25 اسمًا مذكورًا"},
  {"question":"ما اسم السورة التي تبدأ بـ {قل هو الله أحد}؟","option1":"الإخلاص","option2":"الفاتحة","option3":"النصر","option4":"الكوثر","correct":"الإخلاص"},
  {"question":"ما اسم السورة التي تُلقب ب (الرحمن)؟","option1":"الرحمن","option2":"الملك","option3":"الملك","option4":"القدر","correct":"الرحمن"},
  {"question":"من هو الذي قال: 'أنا سيد أولياء الله'؟","option1":"هذا حديث حول آراء علمية (لا يدخل هنا)","option2":"ليس نبي","option3":"خطأ","option4":"غير محدد","correct":"غير مناسب للسؤال العام"},
  {"question":"من هو الذي غُسِل النبي ﷺ عند وفاته؟","option1":"الصحابة (عائشة وغيرها)","option2":"شخص وحيد","option3":"خطباء","option4":"ملائكة","correct":"الصحابة (عرضية: عُرف أن بعض الصحابة شاركوا)"},
  {"question":"ما هي آية الدين المعروفة؟","option1":"الآية المتعلقة بالديون في البقرة","option2":"آية الكرسي","option3":"آية النور","option4":"الآية الأخيرة","correct":"الآية المتعلقة بالديون في البقرة (آية الدين)"},
  {"question":"ما اسم السورة التي تذكر قصة يوسف؟","option1":"يوسف","option2":"يونس","option3":"يونس","option4":"يوسف","correct":"يوسف"},
  {"question":"كم عدد سجود التلاوة في القرآن؟","option1":"11","option2":"14","option3":"3","option4":"7","correct":"11"},
  {"question":"من أول الخلفاء الراشدين؟","option1":"أبو بكر الصديق","option2":"عمر","option3":"عثمان","option4":"علي","correct":"أبو بكر الصديق"},
  {"question":"ما اسم المدينة التي قضاها الرسول قبل الهجرة؟","option1":"يثرب","option2":"مكة","option3":"طائف","option4":"الرفيدة","correct":"المدينة"}
];

let timer;
let timeLeft = 30;
let countdownValue = 5;
let countdownInterval = null;
const QUESTIONS_PER_LEVEL = 10;

// Modal elements
const questionsModal = document.getElementById('questionsModal');
const questionsListContent = document.getElementById('questionsListContent');
const closeModal = document.querySelector('.close');

// Show screen function
function showScreen(screenId) {
  Object.values(screens).forEach(screen => screen.classList.remove('active'));
  screens[screenId].classList.add('active');
}

// Update player displays
function updatePlayerDisplays() {
  for (let i = 1; i <= 4; i++) {
    if (i <= numPlayers) {
      playerCards[i].style.display = 'block';
      playerCards[i].querySelector('.player-name').textContent = playerNames[i-1];
      playerCards[i].querySelector('.player-score').textContent = `النقاط: ${scores[i-1]}`;
    } else {
      playerCards[i].style.display = 'none';
    }
  }
}

// Start countdown
function startCountdown() {
  showScreen('countdown');
  countdownValue = 5;
  document.getElementById('countdown').textContent = countdownValue;
  document.getElementById('countdownPlayerInfo').textContent = `اللاعب: ${playerNames[currentPlayerIndex]}`;
  
  countdownInterval = setInterval(() => {
    countdownValue--;
    document.getElementById('countdown').textContent = countdownValue;
    document.getElementById('countdownPlayerInfo').textContent = `اللاعب: ${playerNames[currentPlayerIndex]}`;
    
    if (countdownValue <= 0) {
      clearInterval(countdownInterval);
      showScreen('game');
      showQuestion();
    }
  }, 1000);
}

// Helper: shuffle array
function shuffleArray(array) {
  for (let i = array.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [array[i], array[j]] = [array[j], array[i]];
  }
  return array;
}

// Prepare questions
function prepareQuestions() {
  let pool = JSON.parse(JSON.stringify(QUESTION_BANK));
  shuffleArray(pool);
  const TOTAL_LEVELS = Math.ceil(numQuestions / QUESTIONS_PER_LEVEL);
  const QUESTIONS_TOTAL = TOTAL_LEVELS * QUESTIONS_PER_LEVEL;
  currentQuestions = pool.slice(0, QUESTIONS_TOTAL);
  shuffleArray(currentQuestions);
}

// Show question
function showQuestion() {
  if (currentQuestionIndex >= currentQuestions.length) {
    endGame();
    return;
  }
  
  const question = currentQuestions[currentQuestionIndex];
  document.getElementById('questionText').textContent = `${currentQuestionIndex + 1}. ${question.question}`;
  document.getElementById('currentPlayerInfo').textContent = `اللاعب: ${playerNames[currentPlayerIndex]}`;
  
  const optionsGrid = document.getElementById('optionsGrid');
  optionsGrid.innerHTML = '';
  
  // Shuffle options
  const options = [
    { text: question.option1, correct: question.option1 === question.correct },
    { text: question.option2, correct: question.option2 === question.correct },
    { text: question.option3, correct: question.option3 === question.correct },
    { text: question.option4, correct: question.option4 === question.correct }
  ];
  
  // Simple shuffle
  for (let i = options.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [options[i], options[j]] = [options[j], options[i]];
  }
  
  options.forEach(option => {
    const optionElement = document.createElement('div');
    optionElement.className = 'option';
    optionElement.textContent = option.text;
    optionElement.onclick = () => selectOption(option.correct);
    optionsGrid.appendChild(optionElement);
  });
  
  // Update progress bar
  const progress = (currentQuestionIndex / currentQuestions.length) * 100;
  document.getElementById('progressBar').style.width = `${progress}%`;
  
  resetTimer();
}

// Select option
function selectOption(isCorrect) {
  clearInterval(timer);
  
  const options = document.querySelectorAll('.option');
  options.forEach(option => {
    option.onclick = null;
    option.style.opacity = '0.7';
  });
  
  if (isCorrect) {
    // Award points based on remaining time
    const points = 10 + Math.floor(timeLeft / 3);
    scores[currentPlayerIndex] += points;
    
    // Update team score in multiplayer mode
    if (mode === 'multi') {
      for (const team of teams) {
        if (team.players.includes(currentPlayerIndex)) {
          team.score += points;
          break;
        }
      }
    }
    
    // Show correct animation
    options.forEach(option => {
      if (option.textContent === currentQuestions[currentQuestionIndex].correct) {
        option.style.background = 'linear-gradient(135deg, #2ecc71 0%, #27ae60 100%)';
        option.style.borderColor = '#2ecc71';
      }
    });
  } else {
    // Show incorrect animation
    options.forEach(option => {
      if (option.textContent === currentQuestions[currentQuestionIndex].correct) {
        option.style.background = 'linear-gradient(135deg, #2ecc71 0%, #27ae60 100%)';
        option.style.borderColor = '#2ecc71';
      } else if (option.textContent === event.target.textContent) {
        option.style.background = 'linear-gradient(135deg, #e74c3c 0%, #c0392b 100%)';
        option.style.borderColor = '#e74c3c';
      }
    });
  }
  
  // Update displays
  updatePlayerDisplays();
  
  // Move to next question after delay
  setTimeout(() => {
    currentQuestionIndex++;
    
    // In multiplayer mode, rotate players
    if (mode === 'multi') {
      currentPlayerIndex = (currentPlayerIndex + 1) % numPlayers;
    }
    
    showQuestion();
  }, 1500);
}

// Timer functions
function resetTimer() {
  clearInterval(timer);
  timeLeft = 30;
  document.getElementById('timer-display').textContent = timeLeft;
  
  timer = setInterval(() => {
    timeLeft--;
    document.getElementById('timer-display').textContent = timeLeft;
    
    if (timeLeft <= 0) {
      clearInterval(timer);
      // Auto-select wrong answer when time runs out
      selectOption(false);
    }
  }, 1000);
}

// End game
function endGame() {
  clearInterval(timer);
  
  // Calculate final score
  let finalScore = 0;
  if (mode === 'multi') {
    finalScore = Math.max(...teams.map(t => t.score));
  } else {
    finalScore = Math.max(...scores.slice(0, numPlayers));
  }
  
  document.getElementById('finalScore').textContent = finalScore;
  showScreen('end');
  updateRanking();
}

// Update ranking
function updateRanking() {
  const rankingList = document.getElementById('rankingList');
  rankingList.innerHTML = '';
  
  if (mode === 'multi') {
    // Team rankings
    const sortedTeams = [...teams].sort((a, b) => b.score - a.score);
    sortedTeams.forEach((team, index) => {
      const rankingItem = document.createElement('div');
      rankingItem.className = 'badge';
      rankingItem.style.padding = '12px';
      rankingItem.style.fontWeight = 'bold';
      rankingItem.style.fontSize = '18px';
      rankingItem.style.marginBottom = '10px';
      
      rankingItem.innerHTML = `
        <div style="display: flex; justify-content: space-between; align-items: center;">
          <span>${index + 1}. ${team.name}</span>
          <span style="color: var(--accent-secondary);">${team.score} نقطة</span>
        </div>
      `;
      rankingList.appendChild(rankingItem);
      
      // Add player details for this team
      team.players.slice(0, numPlayers).forEach(playerIndex => {
        if (playerIndex < numPlayers) {
          const playerItem = document.createElement('div');
          playerItem.className = 'badge';
          playerItem.style.padding = '8px 15px';
          playerItem.style.marginLeft = '30px';
          playerItem.style.fontSize = '16px';
          
          playerItem.innerHTML = `
            <div style="display: flex; justify-content: space-between;">
              <span>${playerNames[playerIndex]}</span>
              <span>${scores[playerIndex]} نقطة</span>
            </div>
          `;
          rankingList.appendChild(playerItem);
        }
      });
    });
  } else {
    // Individual player rankings
    const playerScores = playerNames.slice(0, numPlayers).map((name, index) => ({
      name,
      score: scores[index],
      index
    }));
    
    playerScores.sort((a, b) => b.score - a.score);
    
    playerScores.forEach((player, index) => {
      const rankingItem = document.createElement('div');
      rankingItem.className = 'badge';
      rankingItem.style.padding = '12px';
      rankingItem.style.fontWeight = 'bold';
      rankingItem.style.fontSize = '18px';
      rankingItem.style.marginBottom = '10px';
      
      rankingItem.innerHTML = `
        <div style="display: flex; justify-content: space-between; align-items: center;">
          <span>${index + 1}. ${player.name}</span>
          <span style="color: var(--accent-secondary);">${player.score} نقطة</span>
        </div>
      `;
      rankingList.appendChild(rankingItem);
    });
  }
}

// Setup players
function setupPlayers(n, names = []) {
  scores = [0, 0, 0, 0];
  currentPlayerIndex = 0;
  currentQuestionIndex = 0;
  
  for (let i = 0; i < n; i++) {
    playerNames[i] = names[i] || `اللاعب ${i + 1}`;
  }
  
  updatePlayerDisplays();
}

// Render names input
function renderNamesInput(n) {
  const namesInputArea = document.getElementById('namesInputArea');
  namesInputArea.innerHTML = '';
  
  for (let i = 0; i < n; i++) {
    const input = document.createElement('input');
    input.type = 'text';
    input.placeholder = `اسم اللاعب ${i + 1}`;
    input.className = 'cod-btn small';
    input.style.width = '100%';
    input.style.margin = '10px 0';
    input.value = playerNames[i] || `اللاعب ${i + 1}`;
    namesInputArea.appendChild(input);
  }
}

// Render players list for drag/drop
function renderPlayersList() {
  const playersList = document.getElementById('playersList');
  playersList.innerHTML = '';
  
  for (let i = 0; i < numPlayers; i++) {
    const div = document.createElement('div');
    div.className = 'player-item';
    div.draggable = true;
    div.id = `player-${i}`;
    div.textContent = playerNames[i];
    div.addEventListener('dragstart', dragStart);
    playersList.appendChild(div);
  }
  
  // Clear slots
  ['slotA1', 'slotA2', 'slotB1', 'slotB2'].forEach(id => {
    const slot = document.getElementById(id);
    if (slot) {
      slot.innerHTML = '';
      slot.addEventListener('dragover', dragOver);
      slot.addEventListener('drop', dropToSlot);
      slot.addEventListener('dragleave', () => slot.classList.remove('drag-over'));
    }
  });
}

// Drag & Drop handlers
function dragStart(e) {
  e.dataTransfer.setData('text/plain', e.target.id);
}

function dragOver(e) {
  e.preventDefault();
  e.currentTarget.classList.add('drag-over');
}

function dropToSlot(e) {
  e.preventDefault();
  e.currentTarget.classList.remove('drag-over');
  const pid = e.dataTransfer.getData('text/plain');
  const playerEl = document.getElementById(pid);
  if (!playerEl) return;
  
  if (e.currentTarget.firstChild) {
    document.getElementById('playersList').appendChild(e.currentTarget.firstChild);
  }
  
  e.currentTarget.appendChild(playerEl);
  
  const slotId = e.currentTarget.dataset.slot;
  if (slotId) {
    const teamId = slotId.charAt(0);
    const playerId = parseInt(pid.split('-')[1]);
    const player = {
      id: playerId,
      name: playerNames[playerId],
      score: 0,
      teamId: teamId
    };
    
    // Update team assignments
    if (teamId === 'A') {
      if (!teams[0].players.includes(playerId)) {
        teams[0].players.push(playerId);
      }
    } else if (teamId === 'B') {
      if (!teams[1].players.includes(playerId)) {
        teams[1].players.push(playerId);
      }
    }
  }
}

// Random distribution
function randomDistribution() {
  // Reset teams
  teams[0].players = [];
  teams[1].players = [];
  
  // Assign players randomly to teams
  for (let i = 0; i < numPlayers; i++) {
    if (i % 2 === 0) {
      teams[0].players.push(i);
    } else {
      teams[1].players.push(i);
    }
  }
  
  // Update UI
  renderPlayersList();
  ['slotA1', 'slotA2', 'slotB1', 'slotB2'].forEach(id => {
    const slot = document.getElementById(id);
    if (slot) slot.innerHTML = '';
  });
  
  // Fill slots based on team assignments
  teams[0].players.slice(0, 2).forEach((playerId, idx) => {
    const slot = document.getElementById(`slotA${idx + 1}`);
    if (slot) {
      const playerEl = document.getElementById(`player-${playerId}`);
      if (playerEl) slot.appendChild(playerEl.cloneNode(true));
    }
  });
  
  teams[1].players.slice(0, 2).forEach((playerId, idx) => {
    const slot = document.getElementById(`slotB${idx + 1}`);
    if (slot) {
      const playerEl = document.getElementById(`player-${playerId}`);
      if (playerEl) slot.appendChild(playerEl.cloneNode(true));
    }
  });
}

// Prepare questions list for modal
function prepareQuestionsList() {
  questionsListContent.innerHTML = '';
  QUESTION_BANK.forEach((q, index) => {
    const item = document.createElement('div');
    item.className = 'question-item';
    item.innerHTML = `<strong>السؤال ${index + 1}:</strong> ${q.question}<br>
                      <em>الإجابة الصحيحة: ${q.correct}</em>`;
    questionsListContent.appendChild(item);
  });
}

// Event listeners
document.getElementById('startGame').addEventListener('click', () => showScreen('mode'));
document.getElementById('modeSolo').addEventListener('click', () => { mode = 'solo'; showScreen('playersSolo'); });
document.getElementById('modeMulti').addEventListener('click', () => { mode = 'multi'; showScreen('playersMulti'); });
document.getElementById('backFromMode').addEventListener('click', () => showScreen('main'));

document.getElementById('soloPlayers1').addEventListener('click', () => { numPlayers = 1; showScreen('questions'); });
document.getElementById('soloPlayers2').addEventListener('click', () => { numPlayers = 2; showScreen('questions'); });
document.getElementById('soloPlayers3').addEventListener('click', () => { numPlayers = 3; showScreen('questions'); });
document.getElementById('soloPlayers4').addEventListener('click', () => { numPlayers = 4; showScreen('questions'); });
document.getElementById('backFromPlayersSolo').addEventListener('click', () => showScreen('mode'));

document.getElementById('multiPlayers2').addEventListener('click', () => { numPlayers = 2; showScreen('questions'); });
document.getElementById('multiPlayers3').addEventListener('click', () => { numPlayers = 3; showScreen('questions'); });
document.getElementById('multiPlayers4').addEventListener('click', () => { numPlayers = 4; showScreen('questions'); });
document.getElementById('backFromPlayersMulti').addEventListener('click', () => showScreen('mode'));

document.getElementById('q10').addEventListener('click', () => { numQuestions = 10; showScreen('names'); renderNamesInput(numPlayers); });
document.getElementById('q20').addEventListener('click', () => { numQuestions = 20; showScreen('names'); renderNamesInput(numPlayers); });
document.getElementById('q30').addEventListener('click', () => { numQuestions = 30; showScreen('names'); renderNamesInput(numPlayers); });
document.getElementById('q40').addEventListener('click', () => { numQuestions = 40; showScreen('names'); renderNamesInput(numPlayers); });
document.getElementById('q50').addEventListener('click', () => { numQuestions = 50; showScreen('names'); renderNamesInput(numPlayers); });
document.getElementById('q100').addEventListener('click', () => { numQuestions = 100; showScreen('names'); renderNamesInput(numPlayers); });
document.getElementById('backFromQuestions').addEventListener('click', () => {
  if (mode === 'solo') {
    showScreen('playersSolo');
  } else {
    showScreen('playersMulti');
  }
});

document.getElementById('startNames').addEventListener('click', () => {
  const inputs = document.querySelectorAll('#namesInputArea input');
  const names = Array.from(inputs).map(input => input.value.trim() || input.placeholder.split(' ')[1]);
  
  setupPlayers(numPlayers, names);
  
  if (mode === 'solo') {
    prepareQuestions();
    startCountdown();
  } else {
    showScreen('distribution');
  }
});

document.getElementById('backFromNames').addEventListener('click', () => {
  if (mode === 'solo') {
    showScreen('questions');
  } else {
    showScreen('playersMulti');
  }
});

document.getElementById('distRandom').addEventListener('click', () => {
  randomDistribution();
  prepareQuestions();
  startCountdown();
});

document.getElementById('distCustom').addEventListener('click', () => {
  renderPlayersList();
  showScreen('custom');
});

document.getElementById('backFromDist').addEventListener('click', () => showScreen('names'));

document.getElementById('startFromCustom').addEventListener('click', () => {
  prepareQuestions();
  startCountdown();
});

document.getElementById('backFromCustom').addEventListener('click', () => showScreen('distribution'));

document.getElementById('playAgain').addEventListener('click', () => {
  scores = [0, 0, 0, 0];
  teams.forEach(team => team.score = 0);
  currentPlayerIndex = 0;
  currentQuestionIndex = 0;
  prepareQuestions();
  startCountdown();
});

document.getElementById('backToMain').addEventListener('click', () => {
  clearInterval(timer);
  clearInterval(countdownInterval);
  showScreen('main');
});

document.getElementById('aboutBtn').addEventListener('click', () => {
  alert('لعبة أسئلة دينية — نسخة Call of Duty Style. اجتِب الأسئلة بأقصى سرعة واحصل على نقاط. للاعبين أو جماعي.');
});

document.getElementById('questionsListBtn').addEventListener('click', () => {
  prepareQuestionsList();
  questionsModal.style.display = 'flex';
});

closeModal.addEventListener('click', () => {
  questionsModal.style.display = 'none';
});

window.addEventListener('click', (e) => {
  if (e.target === questionsModal) {
    questionsModal.style.display = 'none';
  }
});

// Initialize
updatePlayerDisplays();
showScreen('main');
</script>
</body>
</html>
