<svg width="1200" height="320" viewBox="0 0 1200 320" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0d1117"/>
      <stop offset="45%" stop-color="#0d1b26"/>
      <stop offset="100%" stop-color="#0d1117"/>
    </linearGradient>

    <radialGradient id="glow1" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#00d1ff" stop-opacity="0.55"/>
      <stop offset="100%" stop-color="#00d1ff" stop-opacity="0"/>
    </radialGradient>

    <radialGradient id="glow2" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#7f5af0" stop-opacity="0.45"/>
      <stop offset="100%" stop-color="#7f5af0" stop-opacity="0"/>
    </radialGradient>

    <linearGradient id="textGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00d1ff"/>
      <stop offset="50%" stop-color="#7f5af0"/>
      <stop offset="100%" stop-color="#00d1ff"/>
      <animate attributeName="x1" values="0%;100%;0%" dur="6s" repeatCount="indefinite"/>
      <animate attributeName="x2" values="100%;200%;100%" dur="6s" repeatCount="indefinite"/>
    </linearGradient>

    <filter id="softGlow" x="-60%" y="-60%" width="220%" height="220%">
      <feGaussianBlur stdDeviation="5" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <!-- background -->
  <rect width="1200" height="320" fill="url(#bg)"/>

  <!-- drifting ambient glows -->
  <circle cx="180" cy="70" r="190" fill="url(#glow1)">
    <animate attributeName="cx" values="150;340;150" dur="11s" repeatCount="indefinite"/>
    <animate attributeName="cy" values="70;120;70" dur="11s" repeatCount="indefinite"/>
  </circle>
  <circle cx="1030" cy="250" r="210" fill="url(#glow2)">
    <animate attributeName="cx" values="1030;850;1030" dur="13s" repeatCount="indefinite"/>
    <animate attributeName="cy" values="250;190;250" dur="13s" repeatCount="indefinite"/>
  </circle>

  <!-- floating particles -->
  <g fill="#00d1ff">
    <circle cx="90" cy="260" r="2.5" opacity="0.7">
      <animate attributeName="cy" values="260;40;260" dur="9s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.8;0" dur="9s" repeatCount="indefinite"/>
    </circle>
    <circle cx="240" cy="290" r="2" opacity="0.6">
      <animate attributeName="cy" values="290;30;290" dur="12s" begin="1.5s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.7;0" dur="12s" begin="1.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="980" cy="280" r="2.5" opacity="0.6">
      <animate attributeName="cy" values="280;20;280" dur="10s" begin="0.8s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.8;0" dur="10s" begin="0.8s" repeatCount="indefinite"/>
    </circle>
    <circle cx="1120" cy="250" r="2" opacity="0.5">
      <animate attributeName="cy" values="250;10;250" dur="14s" begin="2.2s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.6;0" dur="14s" begin="2.2s" repeatCount="indefinite"/>
    </circle>
    <circle cx="600" cy="300" r="2" opacity="0.5">
      <animate attributeName="cy" values="300;250;300" dur="8s" begin="0.4s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.5;0" dur="8s" begin="0.4s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- name -->
  <text x="600" y="128" font-family="'Segoe UI', Verdana, Arial, sans-serif" font-size="64" font-weight="700"
        text-anchor="middle" fill="url(#textGrad)" filter="url(#softGlow)">
    Nitya Patel
    <animate attributeName="opacity" values="0.88;1;0.88" dur="3s" repeatCount="indefinite"/>
  </text>

  <!-- subtitle -->
  <text x="600" y="168" font-family="'Segoe UI', Verdana, Arial, sans-serif" font-size="23" font-weight="600"
        text-anchor="middle" fill="#e9fbff" letter-spacing="1.5">
    FULL STACK AI DEVELOPER
  </text>

  <!-- animated underline -->
  <rect x="600" y="184" width="0" height="3" rx="1.5" fill="#00d1ff">
    <animate attributeName="width" values="0;280;280;0" keyTimes="0;0.25;0.75;1" dur="4.5s" repeatCount="indefinite"/>
    <animate attributeName="x" values="600;460;460;600" keyTimes="0;0.25;0.75;1" dur="4.5s" repeatCount="indefinite"/>
  </rect>

  <!-- cycling tagline (typewriter-style crossfade) -->
  <text x="600" y="228" font-family="'Fira Code', Consolas, monospace" font-size="18"
        text-anchor="middle" fill="#8fe3ff" opacity="0">
    Regional Qualifier — OpenAI Academy × NxtWave Buildathon
    <animate attributeName="opacity" values="0;1;1;0;0" keyTimes="0;0.03;0.30;0.34;1"
             dur="12s" repeatCount="indefinite"/>
  </text>

  <text x="600" y="228" font-family="'Fira Code', Consolas, monospace" font-size="18"
        text-anchor="middle" fill="#8fe3ff" opacity="0">
    Python • React • FastAPI • PyTorch
    <animate attributeName="opacity" values="0;0;1;1;0;0" keyTimes="0;0.34;0.37;0.63;0.67;1"
             dur="12s" repeatCount="indefinite"/>
  </text>

  <text x="600" y="228" font-family="'Fira Code', Consolas, monospace" font-size="18"
        text-anchor="middle" fill="#8fe3ff" opacity="0">
    Building Intelligent, Production-Ready Applications
    <animate attributeName="opacity" values="0;0;1;1;0" keyTimes="0;0.67;0.70;0.97;1"
             dur="12s" repeatCount="indefinite"/>
  </text>

  <!-- subtle blinking cursor -->
  <rect x="885" y="215" width="2" height="18" fill="#00d1ff">
    <animate attributeName="opacity" values="1;1;0;0;1" keyTimes="0;0.02;0.03;0.98;1" dur="1s" repeatCount="indefinite"/>
  </rect>
</svg>



<div align="center">

<img src="./assets/banner.svg" width="100%"/>

<br/>

<img src="https://img.shields.io/badge/B.Sc._IT-Graduate-00d1ff?style=for-the-badge&labelColor=0D1117"/>
<img src="https://img.shields.io/badge/Role-Full_Stack_AI_Developer-00d1ff?style=for-the-badge&labelColor=0D1117"/>
<img src="https://img.shields.io/badge/Buildathon-Regional_Qualifier-00d1ff?style=for-the-badge&labelColor=0D1117"/>

<sub><b>OpenAI Academy × NxtWave Buildathon</b> — Regional Qualifier</sub>

</div>

<img src="./assets/divider.svg" width="100%"/>

## 🧠 Developer Profile

I'm a **Full Stack AI Developer** who designs and builds **AI-powered applications and scalable full-stack systems** — merging **Machine Learning pipelines** with **modern web architectures** to ship intelligent, production-ready products end to end: from model training to deployed UI.

- 🔬 Engineering ML pipelines with **PyTorch** and **Scikit-Learn**
- 🌐 Shipping full-stack apps with **React.js**, **FastAPI**, and **Firebase**
- 🏆 Regional Qualifier — **OpenAI Academy × NxtWave Buildathon**
- 📍 Always exploring the intersection of **Generative AI** and **Web Engineering**

<img src="./assets/divider.svg" width="100%"/>

## 🛠 Technical Ecosystem

<table align="center">
<tr>
<th>🤖 AI & Machine Learning</th>
<th>📊 Data Engineering</th>
<th>💻 Full Stack Development</th>
</tr>
<tr>
<td align="center"><img src="https://skillicons.dev/icons?i=python" height="40"/><br/><b>Python</b></td>
<td align="center"><img src="https://img.icons8.com/color/40/000000/numpy.png"/><br/><b>NumPy</b></td>
<td align="center"><img src="https://skillicons.dev/icons?i=react" height="40"/><br/><b>React.js</b></td>
</tr>
<tr>
<td align="center"><img src="https://skillicons.dev/icons?i=pytorch" height="40"/><br/><b>PyTorch</b></td>
<td align="center"><img src="https://img.icons8.com/color/40/000000/pandas.png"/><br/><b>Pandas</b></td>
<td align="center"><img src="https://skillicons.dev/icons?i=firebase" height="40"/><br/><b>Firebase</b></td>
</tr>
<tr>
<td align="center"><img src="https://img.icons8.com/color/40/000000/scikit-learn.png"/><br/><b>Scikit-Learn</b></td>
<td align="center"><img src="https://img.icons8.com/color/40/000000/matplotlib.png"/><br/><b>Matplotlib</b></td>
<td align="center"><img src="https://skillicons.dev/icons?i=fastapi" height="40"/><br/><b>FastAPI</b></td>
</tr>
</table>

<div align="center">
<img src="https://skillicons.dev/icons?i=py,pytorch,react,firebase,fastapi,github,git,vscode,md,pnpm&theme=dark" />
</div>

<img src="./assets/divider.svg" width="100%"/>

## 🚀 Flagship Implementation

### 🧬 Med-AI — Ensemble Learning for Symptom-Based Disease Prediction

> A machine-learning-powered medical assistant that **predicts diseases from symptom inputs** using ensemble learning models, wrapped in a real-time, production-style application.

<table align="center">
<tr>
<td width="50%" valign="top">

**⚙️ System Architecture**

| Layer | Stack |
| :--- | :--- |
| 🧠 Intelligence | PyTorch + Scikit-Learn ensemble models |
| 📊 Data Processing | NumPy + Pandas pipelines |
| 🎨 Application | React.js interactive frontend |
| ☁️ Cloud & State | Firebase real-time backend |

</td>
<td width="50%" valign="top">

**✨ Highlights**

- Ensemble voting across multiple classifiers for higher prediction accuracy
- Clean, high-performance data preprocessing pipeline
- Real-time sync between frontend and backend via Firebase
- Interactive, responsive UI for symptom entry and results

</td>
</tr>
</table>

<img src="./assets/divider.svg" width="100%"/>

## 📊 Developer Analytics Dashboard

<p align="center">
<img src="https://github-readme-streak-stats.herokuapp.com?user=YOUR_USERNAME&theme=tokyonight&hide_border=true&background=0D1117&ring=00d1ff&fire=00d1ff&currStreakLabel=00d1ff" width="48%" />
<img src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00d1ff&icon_color=00d1ff&text_color=ffffff" width="48%" />
</p>

<p align="center">
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00d1ff&text_color=ffffff" width="40%" />
<img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=YOUR_USERNAME&theme=tokyonight" width="40%" />
</p>

<img src="./assets/divider.svg" width="100%"/>

## ⚡ Contribution Activity

<p align="center">
<img src="https://github-readme-activity-graph.vercel.app/graph?username=YOUR_USERNAME&theme=tokyonight&area=true&hide_border=true&bg_color=0D1117&color=00d1ff&point=00d1ff&line=00d1ff" width="100%" />
</p>

<!--
  Animated contribution snake — needs a one-time GitHub Action.
  Add .github/workflows/snake.yml (Platane/snk action) to your repo to generate this automatically.
-->
<p align="center">
<img src="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-contribution-grid-snake-dark.svg" width="100%" alt="Contribution Snake"/>
</p>

<img src="./assets/divider.svg" width="100%"/>

## 🏆 Developer Achievements

<p align="center">
<img src="https://github-profile-trophy.vercel.app/?username=YOUR_USERNAME&theme=tokyonight&no-frame=true&row=1&column=6" />
</p>

<img src="./assets/divider.svg" width="100%"/>

<div align="center">

### 📫 Let's Connect

<a href="mailto:your-email@example.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://linkedin.com/in/your-linkedin"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="https://github.com/YOUR_USERNAME"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"/></a>

<sub>⭐️ From <a href="https://github.com/YOUR_USERNAME">Nitya Patel</a> — Full Stack AI Developer</sub>

</div>
