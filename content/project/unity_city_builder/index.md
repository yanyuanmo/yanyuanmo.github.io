---
title: Mobile Game Development Project — Archiventure
summary: Mobile Game Development Project — Archiventure
tags:
  - Andriod
  - Mobile Development
  - Unity
  - Game Development
date: '2024-12-16T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  focal_point: Smart

# links:
#   - icon: Github
#     icon_pack: fab
#     name: Repo Page
#     url: https://github.com/Yanko96/Path-Link-Graph-Nerural-Network-for-IP-Performance-Prediction
url_code: 'https://github.com/yanyuanmo/Archiventure'
url_pdf: ''
url_slides: ''
url_video: ''
styles: |
  .article-container {
    max-width: 1400px !important;
  }

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

<style>
.article-container {
  max-width: 100% !important;
  padding: 0;
}

#unity-container {
  width: 100%;
  height: 80vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

#unity-canvas {
  width: 100%;
  height: 100%;
  background: #231F20;
}
</style>

<div id="unity-container">
  <canvas id="unity-canvas" tabindex="-1"></canvas>
</div>

<script src="/apps/Archiventure/Build/build.loader.js"></script>
<script>
  var canvas = document.querySelector("#unity-canvas");
  
  function resizeCanvas() {
    var container = document.querySelector("#unity-container");
    var aspectRatio = 600/400;
    
    var maxWidth = container.clientWidth;
    var maxHeight = container.clientHeight;
    
    var newWidth = maxWidth;
    var newHeight = newWidth / aspectRatio;
    
    if (newHeight > maxHeight) {
      newHeight = maxHeight;
      newWidth = newHeight * aspectRatio;
    }
    
    canvas.style.width = newWidth + 'px';
    canvas.style.height = newHeight + 'px';
  }

  window.addEventListener('resize', resizeCanvas);
  resizeCanvas();

  createUnityInstance(canvas, {
    arguments: [],
    dataUrl: "/apps/Archiventure/Build/build.data",
    frameworkUrl: "/apps/Archiventure/Build/build.framework.js",
    codeUrl: "/apps/Archiventure/Build/build.wasm",
    streamingAssetsUrl: "/apps/Archiventure/StreamingAssets",
    companyName: "DefaultCompany",
    productName: "Archiventure",
    productVersion: "1.0",
    matchWebGLToCanvasSize: true,
  });
</script>

This project served as the final project of course 
CS 5520 Mobile Application Development. The code is available [here](https://github.com/yanyuanmo/Archiventure)

Archiventure is a cultural city builder mobile game built in Unity with PlayFab backend integration. The game features an innovative isometric grid system with custom coordinate mapping for intuitive building placement, complemented by unique upgrade progression trees for each building type. Implemented comprehensive gameplay systems including resource management, achievement tracking, and an in-game economy. Enhanced player experience through a hybrid save system combining PlayFab cloud storage and local serialization, enabling seamless cross-device progression while maintaining offline gameplay capability.


