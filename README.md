[reel.html](https://github.com/user-attachments/files/25813144/reel.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Your Highlight Reel — Rod2Reel</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>
:root {
  --gold: #F5A623;
  --gold-dark: #C4841A;
  --bg: #080808;
  --surface: #111111;
  --surface2: #1A1A1A;
  --border: #222222;
  --text: #FFFFFF;
  --muted: #666666;
  --subtle: #333333;
}

* { margin:0; padding:0; box-sizing:border-box; }

body {
  background:var(--bg);
  font-family:'DM Sans', sans-serif;
  color:var(--text);
  min-height:100vh;
  overflow-x:hidden;
}

/* HEADER */

.header {
  position:relative;
  padding:32px 24px 24px;
  text-align:center;
  background:linear-gradient(180deg,#0f0f0f 0%,var(--bg) 100%);
  border-bottom:1px solid var(--border);
  overflow:hidden;
}

.header::before {
  content:'';
  position:absolute;
  top:-60px;
  left:50%;
  transform:translateX(-50%);
  width:300px;
  height:300px;
  background:radial-gradient(circle,rgba(245,166,35,0.08) 0%,transparent 70%);
  pointer-events:none;
}

.charter-name {
  font-family:'Bebas Neue', sans-serif;
  font-size:clamp(32px,8vw,52px);
  letter-spacing:2px;
  color:var(--text);
  line-height:1;
  margin-bottom:6px;
  text-shadow:0 0 40px rgba(245,166,35,0.2);
}

.tagline {
  font-size:13px;
  color:var(--muted);
  letter-spacing:3px;
  text-transform:uppercase;
  font-weight:300;
}

.gold-line {
  width:40px;
  height:2px;
  background:var(--gold);
  margin:16px auto 0;
}

/* MAIN */

.content {
  max-width:480px;
  margin:0 auto;
  padding:24px 16px 40px;
}

/* VIDEO */

.video-wrap {
  position:relative;
  border-radius:16px;
  overflow:hidden;
  background:#000;
  margin-bottom:20px;
  box-shadow:0 20px 60px rgba(0,0,0,0.6),0 0 0 1px var(--border);
  display:none;
}

.video-wrap video {
  width:100%;
  display:block;
}

.video-badge {
  position:absolute;
  top:12px;
  left:12px;
  background:rgba(0,0,0,0.7);
  backdrop-filter:blur(8px);
  border:1px solid rgba(245,166,35,0.3);
  color:var(--gold);
  font-size:11px;
  font-weight:600;
  letter-spacing:2px;
  text-transform:uppercase;
  padding:5px 10px;
  border-radius:20px;
}

/* BUTTONS */

.btn-group {
  display:flex;
  flex-direction:column;
  gap:10px;
  margin-bottom:24px;
}

.btn {
  display:flex;
  align-items:center;
  justify-content:center;
  gap:10px;
  padding:16px 24px;
  border-radius:12px;
  font-family:'DM Sans', sans-serif;
  font-size:15px;
  font-weight:600;
  text-decoration:none;
  cursor:pointer;
  border:none;
  transition:all 0.2s ease;
  letter-spacing:0.3px;
}

.btn-review {
  background:var(--gold);
  color:#000;
}

.btn-review:hover {
  background:var(--gold-dark);
  transform:translateY(-1px);
  box-shadow:0 8px 24px rgba(245,166,35,0.3);
}

.btn-download {
  background:var(--surface2);
  color:var(--text);
  border:1px solid var(--border);
}

.btn-download:hover {
  background:var(--subtle);
  transform:translateY(-1px);
}

.btn-icon {
  font-size:18px;
}

/* SOCIAL */

.social-section {
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:16px;
  padding:20px;
  margin-bottom:20px;
  display:none;
}

.section-label {
  font-size:11px;
  font-weight:600;
  letter-spacing:3px;
  text-transform:uppercase;
  color:var(--gold);
  margin-bottom:16px;
  display:flex;
  align-items:center;
  gap:8px;
}

.section-label::after {
  content:'';
  flex:1;
  height:1px;
  background:var(--border);
}

.post-card {
  background:var(--surface2);
  border:1px solid var(--border);
  border-radius:10px;
  padding:14px;
  margin-bottom:10px;
  cursor:pointer;
  transition:all 0.2s ease;
  position:relative;
  overflow:hidden;
}

.post-card::before {
  content:'';
  position:absolute;
  left:0;
  top:0;
  bottom:0;
  width:3px;
  background:var(--gold);
  opacity:0;
  transition:opacity 0.2s ease;
}

.post-card:hover {
  border-color:var(--subtle);
  transform:translateX(3px);
}

.post-card:hover::before {
  opacity:1;
}

.post-text {
  font-size:14px;
  line-height:1.6;
  color:#CCCCCC;
  margin-bottom:8px;
}

.copy-row {
  display:flex;
  align-items:center;
  justify-content:space-between;
}

.copy-hint {
  font-size:11px;
  color:var(--muted);
  letter-spacing:1px;
  text-transform:uppercase;
}

.copy-icon {
  font-size:14px;
  opacity:0.4;
  transition:opacity 0.2s;
}

.post-card:hover .copy-icon {
  opacity:0.8;
}

/* HASHTAGS */

.hashtag-box {
  background:var(--surface2);
  border:1px dashed var(--subtle);
  border-radius:10px;
  padding:12px 14px;
  cursor:pointer;
  transition:all 0.2s ease;
  margin-top:4px;
}

.hashtag-box:hover {
  border-color:var(--gold);
  background:rgba(245,166,35,0.05);
}

.hashtag-text {
  font-size:13px;
  color:#4A9EFF;
  line-height:1.6;
  word-break:break-word;
}

.hashtag-copy-row {
  display:flex;
  align-items:center;
  justify-content:space-between;
  margin-top:8px;
}

/* LOGO */

.logo-section {
  text-align:center;
  padding:24px 0 8px;
  display:none;
  border-top:1px solid var(--border);
  margin-top:8px;
}

/* UPDATED — 35% smaller + centered */

.logo-section img {
  max-width:78px;
  max-height:39px;
  object-fit:contain;
  opacity:0.7;
  filter:brightness(1.2);
  display:block;
  margin:0 auto;
}

/* FOOTER */

.footer {
  text-align:center;
  padding:20px;
  color:var(--subtle);
  font-size:12px;
  letter-spacing:2px;
  text-transform:uppercase;
}

.footer span {
  color:var(--gold);
  opacity:0.6;
}

/* LOADING */

.loading-state {
  text-align:center;
  padding:60px 24px;
}

.fish-emoji {
  font-size:48px;
  display:block;
  margin-bottom:16px;
  animation:bob 2s ease-in-out infinite;
}

@keyframes bob {
  0%,100% { transform:translateY(0); }
  50% { transform:translateY(-8px); }
}

.loading-text {
  font-family:'Bebas Neue', sans-serif;
  font-size:24px;
  letter-spacing:3px;
  color:var(--muted);
}

/* FADE */

.fade-in {
  animation:fadeIn 0.6s ease forwards;
}

@keyframes fadeIn {
  from {opacity:0; transform:translateY(10px);}
  to {opacity:1; transform:translateY(0);}
}

/* MOBILE */

@media (max-width:480px) {
  .content {padding:20px 12px 40px;}
  .btn {padding:15px 20px;font-size:14px;}
}

</style>
</head>

<body>

<div class="header">
  <div class="charter-name" id="charterName">🎣</div>
  <div class="tagline" id="tagline">Your highlight reel is ready</div>
  <div class="gold-line"></div>
</div>

<div class="content">

<div class="loading-state" id="loadingState">
<span class="fish-emoji">🎣</span>
<div class="loading-text">Loading your reel...</div>
</div>

<div class="video-wrap" id="videoWrap">
<div class="video-badge">Your Reel</div>
<video id="mainVideo" controls playsinline preload="metadata"></video>
</div>

<div class="btn-group" id="btnGroup" style="display:none;">
<a id="reviewBtn" href="#" class="btn btn-review" style="display:none;" target="_blank">
<span class="btn-icon">⭐</span>
Leave Us a Review — 30 Seconds
</a>

<a id="downloadBtn" href="#" class="btn btn-download" download style="display:none;">
<span class="btn-icon">⬇️</span>
Download My Reel
</a>
</div>

<div class="social-section" id="socialSection">

<div class="section-label">📲 Share your catch</div>

<div class="post-card" onclick="copyPost('post1txt','toast1')">
<div class="post-text" id="post1txt"></div>
<div class="copy-row">
<span class="copy-hint" id="toast1">Tap to copy</span>
<span class="copy-icon">📋</span>
</div>
</div>

<div class="post-card" onclick="copyPost('post2txt','toast2')">
<div class="post-text" id="post2txt"></div>
<div class="copy-row">
<span class="copy-hint" id="toast2">Tap to copy</span>
<span class="copy-icon">📋</span>
</div>
</div>

<div class="post-card" onclick="copyPost('post3txt','toast3')">
<div class="post-text" id="post3txt"></div>
<div class="copy-row">
<span class="copy-hint" id="toast3">Tap to copy</span>
<span class="copy-icon">📋</span>
</div>
</div>

<div class="hashtag-box" onclick="copyPost('hashtagsTxt','toastHash')">
<div class="hashtag-text" id="hashtagsTxt"></div>
<div class="hashtag-copy-row">
<span class="copy-hint" id="toastHash">Tap to copy hashtags</span>
<span class="copy-icon">📋</span>
</div>
</div>

</div>

<div class="logo-section" id="logoSection">
<img id="charterLogo" src="" alt="Charter Logo"/>
</div>

<div class="footer">Powered by <span>Rod2Reel</span> 🎣</div>

</div>

<script>

function copyPost(textId, toastId) {

const text = document.getElementById(textId).innerText;
const toast = document.getElementById(toastId);

navigator.clipboard.writeText(text).then(function(){

toast.innerText='✓ Copied!';
toast.style.color='#F5A623';

setTimeout(function(){

toast.innerText='Tap to copy';
toast.style.color='';

},2000);

});

}

function getParam(name){

const val=new URLSearchParams(window.location.search).get(name);
return val?decodeURIComponent(val):'';

}

window.onload=function(){

const name=getParam('name');
const videoUrl=getParam('video');
const logo=getParam('logo');
const review=getParam('review');
const post1=getParam('post1');
const post2=getParam('post2');
const post3=getParam('post3');
const hashtags=getParam('hashtags');

document.getElementById('loadingState').style.display='none';

if(name){

document.getElementById('charterName').innerText=name;
document.title=name+' — Your Fishing Reel';

}else{

document.getElementById('charterName').innerText='Your Fishing Reel';

}

if(videoUrl){

document.getElementById('mainVideo').src=videoUrl;
document.getElementById('videoWrap').style.display='block';
document.getElementById('videoWrap').classList.add('fade-in');
document.getElementById('downloadBtn').href=videoUrl;
document.getElementById('downloadBtn').style.display='flex';
document.getElementById('btnGroup').style.display='flex';

}

if(review){

document.getElementById('reviewBtn').href=review;
document.getElementById('reviewBtn').style.display='flex';

}

if(post1||post2||post3){

document.getElementById('socialSection').style.display='block';
document.getElementById('socialSection').classList.add('fade-in');

document.getElementById('post1txt').innerText=post1;
document.getElementById('post2txt').innerText=post2;
document.getElementById('post3txt').innerText=post3;

if(hashtags){
document.getElementById('hashtagsTxt').innerText=hashtags;
}

}

if(logo){

document.getElementById('charterLogo').src=logo;
document.getElementById('logoSection').style.display='block';

}

}

</script>

</body>
</html>
