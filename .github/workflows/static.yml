<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Reviva — Mycie Kostki Brukowej | Zblewo i okolice</title>
  <meta name="description" content="Profesjonalne mycie i czyszczenie kostki brukowej. Obsługujemy Zblewo i okolice w promieniu 20 km. Bezpłatna wycena."/>
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;700;800&family=Literata:ital,wght@0,300;0,400;1,300&display=swap" rel="stylesheet"/>

  <style>
/* ════════════════════════════════════════════════
   TOKENS & RESET
════════════════════════════════════════════════ */
:root{
  --navy:#080f1e; --blue:#112c60; --sky:#1d58c0;
  --ice:#9ec3f5;  --gold:#f5c800; --amber:#e09800;
  --cream:#f6f1e6; --white:#fff;
  --muted:rgba(158,195,245,.6);
  --border:rgba(245,200,0,.14);
  --ff-h:'Syne',sans-serif; --ff-b:'Literata',serif;
  --ease:cubic-bezier(.4,0,.2,1);
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html,body{scroll-behavior:auto;font-size:16px;margin:0!important;padding:0!important;min-height:0}
body{background:var(--navy);color:var(--cream);font-family:var(--ff-b);line-height:1.72;overflow-x:hidden;margin:0!important;padding:0!important}
@media(pointer:fine){body{cursor:none}}

/* ════════════════════════════════════════════════
   CURSOR
════════════════════════════════════════════════ */
#cursor,#cursor-dot{display:none}
@media(pointer:fine){
  #cursor{display:block;width:20px;height:20px;border:2px solid var(--gold);border-radius:50%;position:fixed;pointer-events:none;z-index:9999;transform:translate(-50%,-50%);transition:width .22s,height .22s,background .22s;will-change:left,top}
  #cursor.big{width:52px;height:52px;background:rgba(245,200,0,.1)}
  #cursor-dot{display:block;width:5px;height:5px;background:var(--gold);border-radius:50%;position:fixed;pointer-events:none;z-index:9999;transform:translate(-50%,-50%)}
}

/* ════════════════════════════════════════════════
   PROGRESS
════════════════════════════════════════════════ */
#progress{position:fixed;top:0;left:0;height:3px;width:0%;background:linear-gradient(90deg,var(--sky),var(--gold));z-index:300;transition:width .08s linear}

/* ════════════════════════════════════════════════
   NAV
════════════════════════════════════════════════ */
nav#nav{position:fixed;top:0;left:0;right:0;display:flex;align-items:center;justify-content:space-between;padding:1.3rem 4rem;z-index:200;transition:background .4s,padding .4s,border-color .4s;border-bottom:1px solid transparent}
nav#nav.scrolled{background:rgba(8,15,30,.95);backdrop-filter:blur(20px);padding:.8rem 4rem;border-color:var(--border)}
.nav-logo{display:flex;align-items:center;text-decoration:none;height:44px}
.nav-logo-text{font-family:var(--ff-h);font-size:1.7rem;font-weight:800;letter-spacing:.04em;color:var(--white)}
.nav-logo-text span{color:var(--gold)}
.nav-logo-img{height:52px;width:auto;max-width:180px;object-fit:contain;display:none}
.nav-links{display:flex;gap:2.5rem}
.nav-links a{font-family:var(--ff-h);font-size:.7rem;font-weight:700;letter-spacing:.2em;text-transform:uppercase;color:var(--muted);text-decoration:none;transition:color .2s;position:relative}
.nav-links a::after{content:'';position:absolute;bottom:-3px;left:0;right:0;height:1px;background:var(--gold);transform:scaleX(0);transform-origin:left;transition:transform .25s}
.nav-links a:hover{color:var(--gold)}
.nav-links a:hover::after{transform:scaleX(1)}
.nav-tel{font-family:var(--ff-h);font-size:.78rem;font-weight:700;color:var(--gold);letter-spacing:.06em;text-decoration:none;border:1px solid rgba(245,200,0,.35);padding:.5rem 1.2rem;display:flex;align-items:center;gap:.5rem;transition:background .2s;white-space:nowrap}
.nav-tel:hover{background:rgba(245,200,0,.1)}
.nav-tel svg{width:14px;height:14px;fill:var(--gold);flex-shrink:0}
.nav-burger{display:none;flex-direction:column;gap:5px;cursor:pointer;padding:.4rem;background:none;border:none}
.nav-burger span{display:block;width:24px;height:2px;background:var(--cream);transition:transform .3s,opacity .3s}
.nav-burger.open span:nth-child(1){transform:translateY(7px) rotate(45deg)}
.nav-burger.open span:nth-child(2){opacity:0}
.nav-burger.open span:nth-child(3){transform:translateY(-7px) rotate(-45deg)}
.nav-drawer{display:none;position:fixed;inset:0;background:rgba(8,15,30,.98);backdrop-filter:blur(24px);z-index:190;flex-direction:column;align-items:center;justify-content:center;gap:2.5rem;opacity:0;pointer-events:none;transition:opacity .35s}
.nav-drawer.open{opacity:1;pointer-events:auto}
.nav-drawer a{font-family:var(--ff-h);font-size:2rem;font-weight:800;color:var(--cream);text-decoration:none;transition:color .2s}
.nav-drawer a:hover{color:var(--gold)}

/* ════════════════════════════════════════════════
   UTILITIES
════════════════════════════════════════════════ */
.section-eyebrow{font-family:var(--ff-h);font-size:.68rem;font-weight:700;letter-spacing:.28em;text-transform:uppercase;color:var(--gold);margin-bottom:1.1rem;display:flex;align-items:center;gap:.7rem}
.section-eyebrow::before{content:'';display:block;width:28px;height:1px;background:var(--gold);flex-shrink:0}
.section-h2{font-family:var(--ff-h);font-weight:800;font-size:clamp(2.4rem,4.5vw,4rem);line-height:.9;letter-spacing:-.01em;color:var(--white);margin-bottom:1.4rem}
.section-lead{font-size:1rem;font-weight:300;font-style:italic;color:var(--muted);max-width:52ch;line-height:1.75;margin:0 auto}
.btn-gold{display:inline-flex;align-items:center;gap:.6rem;background:var(--gold);color:var(--navy);font-family:var(--ff-h);font-weight:700;font-size:.78rem;letter-spacing:.14em;text-transform:uppercase;padding:1rem 2.2rem;text-decoration:none;transition:background .2s,transform .15s}
.btn-gold:hover{background:#ffd93d;transform:translateY(-2px)}
.btn-outline{display:inline-flex;align-items:center;gap:.6rem;border:1px solid rgba(158,195,245,.3);color:var(--ice);font-family:var(--ff-h);font-weight:700;font-size:.78rem;letter-spacing:.14em;text-transform:uppercase;padding:1rem 2.2rem;text-decoration:none;transition:border-color .2s,color .2s}
.btn-outline:hover{border-color:var(--gold);color:var(--gold)}
.reveal,.reveal-l,.reveal-r{opacity:0;transition:opacity .85s var(--ease),transform .85s var(--ease)}
.reveal{transform:translateY(40px)}
.reveal-l{transform:translateX(-50px)}
.reveal-r{transform:translateX(50px)}
.reveal.vis,.reveal-l.vis,.reveal-r.vis{opacity:1;transform:none}
.chapter-mark{position:absolute;right:3rem;bottom:2.5rem;font-family:var(--ff-h);font-size:.58rem;font-weight:700;letter-spacing:.3em;text-transform:uppercase;color:rgba(245,200,0,.15);user-select:none;pointer-events:none}

/* ════════════════════════════════════════════════
   SECTION 1 — HERO
════════════════════════════════════════════════ */
#hero{min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;position:relative;overflow:hidden;background:var(--navy)}
#hero-canvas{position:absolute;inset:0;width:100%;height:100%;opacity:.2}
#hero::after{content:'';position:absolute;inset:0;background:radial-gradient(ellipse 60% 55% at 50% 58%,rgba(29,88,192,.3),transparent 70%);pointer-events:none}
.hero-particles{position:absolute;inset:0;pointer-events:none}
.hprt{position:absolute;border-radius:50%;background:var(--gold);opacity:0;animation:hprtDrift linear infinite}
@keyframes hprtDrift{0%{opacity:0;transform:translateY(0) scale(.5)}8%{opacity:.7}92%{opacity:.35}100%{opacity:0;transform:translateY(-90vh) scale(1.3)}}
.hero-content{position:relative;z-index:3;padding:5rem 2rem 8rem;max-width:100%;width:100%;overflow:hidden}
.hero-eyebrow{display:inline-flex;align-items:center;gap:.45rem;font-family:var(--ff-h);font-size:.6rem;font-weight:700;letter-spacing:.18em;text-transform:uppercase;color:var(--gold);border:1px solid rgba(245,200,0,.22);padding:.28rem .9rem;margin-bottom:1.6rem;opacity:.85}
.hero-eyebrow svg{width:13px;height:13px;flex-shrink:0}
.hero-h1{font-family:var(--ff-h);font-weight:800;font-size:clamp(3rem,8vw,8.5rem);line-height:.88;letter-spacing:-.03em;color:var(--white);margin-bottom:1.4rem;white-space:nowrap}
.hero-h1 .gold{color:var(--gold)}
.hero-h1 .hollow{-webkit-text-stroke:2px var(--ice);color:transparent}
.hero-sub{font-size:1.1rem;font-weight:300;font-style:italic;color:var(--ice);max-width:60ch;margin:0 auto 2.8rem}
.hero-ctas{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;}
.scroll-cue{position:absolute;bottom:2rem;left:50%;transform:translateX(-50%);display:flex;flex-direction:column;align-items:center;gap:.4rem;z-index:3;}
.scroll-cue-label{font-family:var(--ff-h);font-size:.6rem;letter-spacing:.25em;text-transform:uppercase;color:rgba(158,195,245,.5)}
.scroll-cue-line{width:1px;height:50px;background:linear-gradient(var(--gold),transparent);animation:scuePulse 2s ease-in-out infinite}
@keyframes scuePulse{0%,100%{opacity:.25;transform:scaleY(1)}50%{opacity:1;transform:scaleY(.55)}}

/* Hero strip — clean stats (no fake numbers) */
.hero-strip{position:absolute;bottom:0;left:0;right:0;background:rgba(8,15,30,.75);backdrop-filter:blur(16px);border-top:1px solid var(--border);display:flex;justify-content:center;z-index:1}
.hero-stat{padding:1.1rem 2.5rem;border-right:1px solid var(--border);text-align:center;flex:1;min-width:120px}
.hero-stat:last-child{border-right:none}
.hero-stat-num{font-family:var(--ff-h);font-size:1.8rem;font-weight:800;color:var(--gold);line-height:1}
.hero-stat-label{font-family:var(--ff-h);font-size:.58rem;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:var(--muted);margin-top:.2rem}

/* ════════════════════════════════════════════════
   SECTION 2 — PROBLEM
════════════════════════════════════════════════ */
#s-problem{padding:9rem 4rem;position:relative;overflow:hidden;background:var(--navy)}
#s-problem::before{content:'';position:absolute;top:-200px;right:-200px;width:600px;height:600px;background:radial-gradient(circle,rgba(29,88,192,.15),transparent 65%);pointer-events:none}
.problem-grid{display:grid;grid-template-columns:1.15fr .85fr;gap:4rem;align-items:center;max-width:1300px;margin:0 auto;text-align:left}
.problem-text p{font-size:1rem;font-weight:300;color:rgba(246,241,230,.68);margin-bottom:1rem;max-width:54ch}
.problem-text p strong{color:var(--ice);font-weight:400}
.problem-icons{display:flex;flex-direction:column;gap:1.1rem;margin-top:2rem}
.problem-icon-row{display:flex;align-items:flex-start;gap:1rem}
.problem-icon-row svg{flex-shrink:0;width:22px;height:22px;stroke:var(--gold);fill:none;stroke-width:1.5;margin-top:.15rem}
.problem-icon-row div strong{font-family:var(--ff-h);font-size:.74rem;letter-spacing:.1em;text-transform:uppercase;color:var(--white);display:block;margin-bottom:.15rem}
.problem-icon-row div span{font-size:.88rem;color:var(--muted);font-weight:300}
.pave-visual{position:relative;display:flex;align-items:center;justify-content:center}
.pave-3d-wrap{transform:perspective(700px) rotateX(18deg) rotateY(-10deg);filter:drop-shadow(0 40px 80px rgba(0,0,0,.6));transition:transform .6s}
.pave-3d-wrap:hover{transform:perspective(700px) rotateX(12deg) rotateY(-5deg)}
#paveGrid{display:grid;grid-template-columns:repeat(7,1fr);gap:6px;width:min(460px,92vw)}
.pave-tile{aspect-ratio:1.45;border-radius:2px;transition:background 1.8s var(--ease)}
.pave-glow{position:absolute;width:min(440px,90vw);height:min(440px,90vw);background:radial-gradient(circle,rgba(29,88,192,.28),transparent 70%);top:50%;left:50%;transform:translate(-50%,-50%);pointer-events:none;animation:glowPulse 3.5s ease-in-out infinite}
@keyframes glowPulse{0%,100%{opacity:.6}50%{opacity:1}}
.wipe-bar{position:absolute;top:0;left:0;bottom:0;width:3px;background:linear-gradient(rgba(158,195,245,0),rgba(158,195,245,.9),rgba(158,195,245,0));pointer-events:none;opacity:0;transition:opacity .3s}
.pave-visual.cleaning .wipe-bar{opacity:1}

/* ════════════════════════════════════════════════
   SECTION 3 — 3D SCROLLYTELLING PROCESS
════════════════════════════════════════════════ */
#s-process{position:relative;background:var(--navy)}
.process-sticky-outer{height:280vh;position:relative}
.process-sticky-inner{position:sticky;top:0;height:100vh;overflow:hidden;display:flex;align-items:stretch}

/* Left text panel */
.process-left{width:38%;flex-shrink:0;display:flex;flex-direction:column;justify-content:center;padding:3rem 2.5rem 3rem 3rem;position:relative;z-index:2;background:rgba(8,15,30,.85);backdrop-filter:blur(8px);border-right:1px solid var(--border)}
.step-progress-track{position:relative;width:3px;background:rgba(245,200,0,.1);border-radius:2px;height:80px;margin:.6rem 0 1rem 0}
.step-progress-fill{position:absolute;top:0;left:0;right:0;background:linear-gradient(var(--sky),var(--gold));height:0%;border-radius:2px;transition:height .5s var(--ease)}
.process-step-list{display:flex;flex-direction:column;gap:0}
.pstep{padding:1.1rem 0;border-bottom:1px solid rgba(245,200,0,.06);transition:padding-left .3s}
.pstep:first-child{padding-top:0}
.pstep.active{padding-left:.8rem;border-bottom-color:var(--border)}
.pstep-num{font-family:var(--ff-h);font-size:.58rem;font-weight:700;letter-spacing:.22em;text-transform:uppercase;color:rgba(245,200,0,.3);margin-bottom:.2rem;transition:color .3s}
.pstep.active .pstep-num{color:var(--gold)}
.pstep-title{font-family:var(--ff-h);font-size:1rem;font-weight:700;color:rgba(246,241,230,.3);transition:color .3s,font-size .3s}
.pstep.active .pstep-title{color:var(--white);font-size:1.2rem}
.pstep-desc{font-size:.86rem;font-weight:300;color:var(--muted);max-height:0;overflow:hidden;opacity:0;margin-top:0;transition:max-height .4s,opacity .4s,margin-top .3s}
.pstep.active .pstep-desc{max-height:80px;opacity:1;margin-top:.4rem}

/* Right visual panel */
.process-right{flex:1;position:relative;overflow:hidden;background:linear-gradient(135deg,#060f1e 0%,#0a1628 100%);display:flex;align-items:center;justify-content:center}
.process-visual{position:relative;width:100%;height:100%;display:flex;align-items:center;justify-content:center;overflow:hidden}

/* Each step scene */
.pscene{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;opacity:0;transition:opacity .7s var(--ease);pointer-events:none;padding:.5rem}
.pscene.active{opacity:1;pointer-events:auto}

/* Big step number watermark */
.pscene-num{position:absolute;right:2.5rem;bottom:2rem;font-family:var(--ff-h);font-size:clamp(5rem,12vw,9rem);font-weight:800;-webkit-text-stroke:1px rgba(245,200,0,.12);color:transparent;line-height:1;user-select:none}

/* Step dots */
.step-dots{position:absolute;right:2rem;top:50%;transform:translateY(-50%);display:flex;flex-direction:column;gap:.9rem;z-index:10}
.sdot{width:7px;height:7px;border-radius:50%;background:rgba(245,200,0,.2);transition:background .3s,transform .3s;cursor:pointer}
.sdot.active{background:var(--gold);transform:scale(1.6)}

/* ── SCENE 0: Usuwanie chwastów ── */
.scene0-wrap{position:relative;width:min(300px,88vw);height:min(190px,30vh);display:flex;align-items:center;justify-content:center;perspective:600px}
.scene0-grid{display:grid;grid-template-columns:repeat(5,1fr);gap:7px;transform:perspective(600px) rotateX(20deg) rotateY(-6deg);filter:drop-shadow(0 30px 60px rgba(0,0,0,.7));position:relative;z-index:1}
.s0tile{width:62px;height:46px;border-radius:3px;position:relative;overflow:hidden;transition:background 1s}
.s0tile::after{content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(255,255,255,.06),transparent)}
/* weeds on tiles */
.weed{position:absolute;bottom:100%;width:3px;background:linear-gradient(#2d5a1b,#4a8a2a);border-radius:2px 2px 0 0;transform-origin:bottom center;animation:weedSway 2s ease-in-out infinite}
@keyframes weedSway{0%,100%{transform:rotate(-8deg)}50%{transform:rotate(8deg)}}
/* tool sweeping */
.s0-tool{position:absolute;bottom:50%;left:0;width:44px;height:44px;animation:toolSweep 3.5s ease-in-out infinite;z-index:5;filter:drop-shadow(0 4px 8px rgba(0,0,0,.5));transform:translateY(50%)}
@keyframes toolSweep{0%{transform:translate(0px,0px) rotate(-15deg);opacity:0}8%{opacity:1}33%{transform:translate(90px,-5px) rotate(10deg)}66%{transform:translate(180px,0px) rotate(-8deg)}92%{opacity:1}100%{transform:translate(270px,0px) rotate(15deg);opacity:0}}
.s0-dust{position:absolute;border-radius:50%;background:rgba(120,90,50,.5);animation:dustPuff ease-out infinite}
@keyframes dustPuff{0%{transform:scale(0);opacity:.7}100%{transform:scale(3);opacity:0}}

/* ── SCENE 1: Płukanie wysokociśnieniowe ── */
.scene1-wrap{position:relative;width:min(320px,88vw);height:min(200px,32vh);display:flex;flex-direction:column;justify-content:center;align-items:center}
/* Płukanie — woda spływa po siatce kostki */
.scene1-wrap{overflow:hidden}
/* Siatka kostki (brudna) */
.s1-grid{display:grid;grid-template-columns:repeat(6,1fr);gap:5px;position:absolute;bottom:0;left:0;right:0;padding:0 4px 4px;height:120px;align-content:end}
.s1-tile{border-radius:2px;background:#1e2c14;height:32px;position:relative;overflow:hidden;transition:background .4s}
.s1-tile.clean{background:#c8c0b4}
/* Linia wody spływająca od góry — gradient przesuwający się w dół */
.s1-water-curtain{position:absolute;left:0;right:0;height:100%;top:-100%;background:linear-gradient(180deg,transparent 0%,rgba(158,195,245,.12) 40%,rgba(158,195,245,.35) 55%,rgba(158,195,245,.12) 70%,transparent 100%);animation:waterFall 2.8s ease-in-out infinite;pointer-events:none;z-index:3}
@keyframes waterFall{0%{top:-100%;opacity:0}15%{opacity:1}85%{opacity:1}100%{top:100%;opacity:0}}
/* Krople spływające */
.s1-drop{position:absolute;width:3px;border-radius:0 0 50% 50%;background:linear-gradient(rgba(158,195,245,.9),rgba(158,195,245,.2));animation:dropSlide linear infinite}
@keyframes dropSlide{0%{top:-20px;opacity:0}10%{opacity:.9}90%{opacity:.7}100%{top:110%;opacity:0}}
/* Kałuże przy dole */
.s1-puddle{position:absolute;bottom:0;height:4px;background:rgba(158,195,245,.3);border-radius:50%;animation:puddleGrow 2.8s ease-in-out infinite}
@keyframes puddleGrow{0%,100%{width:20px;opacity:.4}50%{width:60px;opacity:.7}}
/* Refleks słońca na mokrej powierzchni */
.s1-glint{position:absolute;width:30px;height:4px;background:linear-gradient(90deg,transparent,rgba(255,255,255,.4),transparent);border-radius:50%;animation:glintMove 1.4s ease-in-out infinite alternate}
@keyframes glintMove{from{left:10%;opacity:.5}to{left:60%;opacity:1}}
/* Ukryj stare elementy */
.s1-nozzle{display:none}
.s1-washer{display:none}
.s1-jet{display:none}
.s1-spray-ring{display:none}
.s1-cone{display:none}
.s1-splash{display:none}
@keyframes nozzle1Osc{0%,100%{left:25%}50%{left:75%}}
@keyframes conePulse{0%,100%{left:25%}50%{left:75%}}
/* spray cone */
.s1-cone{position:absolute;top:100px;left:50%;transform:translateX(-50%);border-left:30px solid transparent;border-right:30px solid transparent;border-top:80px solid rgba(158,195,245,.15);animation:conePulse 1.8s ease-in-out infinite;filter:blur(2px)}
@keyframes conePulse{0%,100%{left:25%}50%{left:75%}}
/* water drops scatter */
.s1-splash{position:absolute;border-radius:50%;background:var(--ice);animation:splashOut linear infinite}
@keyframes splashOut{0%{transform:translate(0,0) scale(1);opacity:.8}100%{transform:translate(var(--sx),var(--sy)) scale(.2);opacity:0}}
/* dirty surface before */
.s1-surface{position:absolute;bottom:0;left:0;right:0;height:50px;border-radius:3px;overflow:hidden;background:linear-gradient(180deg,#1e2c12,#243018)}
.s1-surface::after{content:'';position:absolute;inset:0;background:repeating-linear-gradient(90deg,rgba(8,15,30,.4) 0,rgba(8,15,30,.4) 1px,transparent 1px,transparent 44px),repeating-linear-gradient(0deg,rgba(8,15,30,.4) 0,rgba(8,15,30,.4) 1px,transparent 1px,transparent 30px)}
/* clean sweep over surface */
.s1-clean{position:absolute;bottom:0;left:0;height:70px;background:linear-gradient(180deg,#d0c8bc,#c4bcb0);border-radius:4px;animation:cleanPass 3.6s ease-in-out infinite}
@keyframes cleanPass{0%,100%{width:0}45%,55%{width:100%}}

/* ── SCENE 2: Szorowanie ── */
.scene2-wrap{position:relative;width:min(320px,88vw);height:min(200px,32vh);display:flex;align-items:center;justify-content:center;overflow:visible}
/* rotating brush */
.s2-brush-wrap{position:absolute;top:20px;left:20%;animation:brushSweep 2.2s ease-in-out infinite}
@keyframes brushSweep{0%,100%{left:20%;transform:translateX(-50%)}50%{left:80%;transform:translateX(-50%)}}
.s2-brush{width:70px;height:70px;border-radius:50%;border:4px solid #888;background:radial-gradient(circle,#555 30%,#333 100%);position:relative;animation:brushSpin 0.4s linear infinite;box-shadow:0 6px 24px rgba(0,0,0,.5)}
@keyframes brushSpin{from{transform:rotate(0deg)}to{transform:rotate(360deg)}}
.s2-bristle{position:absolute;width:3px;height:30px;background:linear-gradient(var(--gold),#888);border-radius:2px;top:50%;left:50%;transform-origin:bottom center}
/* foam bubbles */
.s2-foam{position:absolute;border-radius:50%;border:1px solid rgba(158,195,245,.5);background:rgba(158,195,245,.06);animation:foamFloat ease-in-out infinite}
@keyframes foamFloat{0%{transform:translate(0,0) scale(1);opacity:.7}100%{transform:translate(var(--fx),var(--fy)) scale(.3);opacity:0}}
/* dirty/clean surface */
.s2-surface{position:absolute;bottom:0;left:0;right:0;height:50px;border-radius:3px;overflow:hidden;background:#2a2218}
.s2-surface::after{content:'';position:absolute;inset:0;background:repeating-linear-gradient(90deg,rgba(0,0,0,.25) 0,rgba(0,0,0,.25) 1px,transparent 1px,transparent 40px),repeating-linear-gradient(0deg,rgba(0,0,0,.25) 0,rgba(0,0,0,.25) 1px,transparent 1px,transparent 28px)}
.s2-clean-bar{position:absolute;bottom:0;left:0;height:80px;background:linear-gradient(180deg,#ccc4b8,#beb6aa);border-right:2px solid rgba(158,195,245,.7);animation:s2Sweep 2.2s ease-in-out infinite}
@keyframes s2Sweep{0%,100%{width:0;left:0}45%,55%{width:80%;left:0}}
/* scratch marks foam */
.s2-scratch{position:absolute;bottom:85px;height:2px;background:rgba(255,255,255,.15);border-radius:1px;animation:scratchMove 2.2s ease-in-out infinite}
@keyframes scratchMove{0%,100%{left:5%;width:10%}45%,55%{left:5%;width:75%}}

/* ── SCENE 3: Impregnation — shield glow ── */
.scene3-wrap{position:relative;width:min(300px,88vw);height:min(200px,32vh);display:flex;align-items:center;justify-content:center}
.shield-hex{position:relative;width:140px;height:160px}
.shield-hex svg{width:100%;height:100%;filter:drop-shadow(0 0 30px rgba(245,200,0,.4));animation:shieldPulse 2.5s ease-in-out infinite}
@keyframes shieldPulse{0%,100%{filter:drop-shadow(0 0 20px rgba(245,200,0,.3))}50%{filter:drop-shadow(0 0 50px rgba(245,200,0,.7))}}
.orbit{position:absolute;top:50%;left:50%;border-radius:50%;border:1px solid rgba(245,200,0,.2);transform:translate(-50%,-50%)}
.orbit-1{width:200px;height:200px;animation:orbitSpin 6s linear infinite}
.orbit-2{width:270px;height:270px;animation:orbitSpin 10s linear infinite reverse;border-color:rgba(158,195,245,.15)}
.orbit-3{width:330px;height:330px;animation:orbitSpin 15s linear infinite;border-color:rgba(245,200,0,.08)}
@keyframes orbitSpin{from{transform:translate(-50%,-50%) rotate(0deg)}to{transform:translate(-50%,-50%) rotate(360deg)}}
.orbit-dot{position:absolute;width:8px;height:8px;border-radius:50%;top:-4px;left:50%;margin-left:-4px}
.orbit-1 .orbit-dot{background:var(--gold);box-shadow:0 0 10px var(--gold)}
.orbit-2 .orbit-dot{background:var(--ice);box-shadow:0 0 8px var(--ice);top:auto;bottom:-4px}
.orbit-3 .orbit-dot{background:rgba(245,200,0,.5)}
.clean-tiles-sm{position:absolute;bottom:-20px;left:50%;transform:translateX(-50%);display:grid;grid-template-columns:repeat(5,1fr);gap:4px;opacity:.6}
.cts{width:36px;height:26px;border-radius:2px;background:#c8c0b4;animation:tileShine 2s ease-in-out infinite}
.cts:nth-child(2){animation-delay:.15s}.cts:nth-child(3){animation-delay:.3s}.cts:nth-child(4){animation-delay:.45s}.cts:nth-child(5){animation-delay:.6s}
@keyframes tileShine{0%,100%{background:#c8c0b4}50%{background:#e0d8cc;box-shadow:0 0 8px rgba(245,200,0,.3)}}

/* ── SCENE 4: Piaskowanie — dysza pneumatyczna ── */
.scene4-wrap{position:relative;width:min(320px,88vw);height:min(200px,32vh);display:flex;align-items:center;justify-content:center;overflow:hidden}

/* Dysza pistoletu sandblastingowego */
.s4-gun{position:absolute;left:16px;top:50%;transform:translateY(-50%);width:110px;height:44px;animation:gunOsc 2s ease-in-out infinite}
@keyframes gunOsc{0%,100%{top:46%}50%{top:54%}}
.s4-gun-body{position:absolute;top:10px;left:0;width:80px;height:24px;background:linear-gradient(180deg,#666,#444,#333);border-radius:5px;box-shadow:0 4px 16px rgba(0,0,0,.5)}
.s4-gun-handle{position:absolute;top:20px;left:25px;width:16px;height:30px;background:linear-gradient(180deg,#555,#333);border-radius:2px 2px 5px 5px}
.s4-gun-barrel{position:absolute;top:14px;left:78px;width:32px;height:16px;background:linear-gradient(180deg,#888,#555);border-radius:0 4px 4px 0}
.s4-gun-hose{position:absolute;top:22px;left:0;width:8px;height:8px;background:#888;border-radius:50%}

/* Strumień piasku z dyszy — stożkowy wachlarz */
.s4-jet-wrap{position:absolute;left:120px;top:50%;transform:translateY(-50%);animation:gunOsc 2s ease-in-out infinite;width:180px;height:120px;overflow:visible}
.s4-jet-line{position:absolute;left:0;top:50%;height:3px;border-radius:2px;transform-origin:left center;background:linear-gradient(90deg,rgba(200,175,100,.9),rgba(200,175,100,.1))}

/* Cząstki piasku */
.s4-grain{position:absolute;border-radius:50%;animation:grainFall linear infinite}
@keyframes grainFall{0%{opacity:0;transform:translate(0,0) scale(1)}12%{opacity:.9}88%{opacity:.6}100%{opacity:0;transform:translate(var(--gx),var(--gy)) scale(.2)}}

/* Obłok pyłu przy uderzeniu */
.s4-impact-cloud{position:absolute;right:30px;top:50%;transform:translateY(-50%);animation:gunOsc 2s ease-in-out infinite}
.s4-dust-puff{position:absolute;border-radius:50%;background:rgba(200,175,100,.18);filter:blur(5px);animation:dustPuff ease-out infinite}
@keyframes dustPuff{0%{transform:scale(.3) translate(0,0);opacity:.7}100%{transform:scale(2.5) translate(var(--px),var(--py));opacity:0}}
.s4-spark{position:absolute;width:3px;height:3px;border-radius:50%;background:rgba(245,200,0,.8);animation:sparkFly linear infinite}
@keyframes sparkFly{0%{opacity:.9;transform:translate(0,0)}100%{opacity:0;transform:translate(var(--sx),var(--sy))}}

/* Powierzchnia kostki */
.s4-surface{position:absolute;bottom:0;left:0;right:0;height:70px;border-radius:4px;overflow:hidden;background:#2a2218}
.s4-surface::after{content:'';position:absolute;inset:0;background:repeating-linear-gradient(90deg,rgba(0,0,0,.3) 0,rgba(0,0,0,.3) 1px,transparent 1px,transparent 42px),repeating-linear-gradient(0deg,rgba(0,0,0,.3) 0,rgba(0,0,0,.3) 1px,transparent 1px,transparent 28px)}
.s4-clean{position:absolute;bottom:0;right:0;height:70px;background:linear-gradient(180deg,#d0c8bc,#c4bcb0);animation:s4CleanSweep 2s ease-in-out infinite}
@keyframes s4CleanSweep{0%,100%{width:40px}50%{width:90px}}
.s4-impact{position:absolute;bottom:77px;right:42px;width:50px;height:22px;background:radial-gradient(ellipse,rgba(245,200,0,.25),transparent 70%);animation:impactPulse .35s ease-in-out infinite alternate;border-radius:50%}
@keyframes impactPulse{from{transform:scaleX(.6);opacity:.3}to{transform:scaleX(1.3);opacity:.9}}

/* stare animacje (używane gdzie indziej) */
.s4-pile{position:absolute;bottom:77px;left:50%;transform:translateX(-50%);width:0;height:0;border-left:44px solid transparent;border-right:44px solid transparent;border-bottom:22px solid #b8902a;animation:pileGrow 3s ease-in-out infinite;filter:drop-shadow(0 3px 8px rgba(0,0,0,.4))}
@keyframes pileGrow{0%,100%{border-left-width:40px;border-right-width:40px;border-bottom-width:22px;opacity:.7}50%{border-left-width:60px;border-right-width:60px;border-bottom-width:32px;opacity:1}}
.s4-dust-cloud{position:absolute;bottom:76px;left:50%;transform:translateX(-50%);width:70px;height:30px;background:radial-gradient(ellipse,rgba(180,150,80,.25),transparent 70%);animation:dustCloud 1.5s ease-in-out infinite alternate;border-radius:50%;filter:blur(4px)}
@keyframes dustCloud{from{transform:translateX(-50%) scale(.8);opacity:.4}to{transform:translateX(-50%) scale(1.3);opacity:.8}}
/* Dziura w worku + strumień piasku */
/* Grain particles from bag */
.s4-grain{position:absolute;border-radius:50%;animation:grainFall linear infinite}
@keyframes streamWiden{0%,100%{clip-path:polygon(20% 0,80% 0,90% 100%,10% 100%)}50%{clip-path:polygon(15% 0,85% 0,95% 100%,5% 100%)}}
@keyframes grainFall{0%{opacity:0;transform:translate(0,0) scale(1)}12%{opacity:.9}88%{opacity:.6}100%{opacity:0;transform:translate(var(--gx),var(--gy)) scale(.25)}}
/* Pile of sand building up */
.s4-pile{position:absolute;bottom:77px;left:50%;transform:translateX(-50%);width:0;height:0;border-left:44px solid transparent;border-right:44px solid transparent;border-bottom:22px solid #b8902a;animation:pileGrow 3s ease-in-out infinite;filter:drop-shadow(0 3px 8px rgba(0,0,0,.4))}
@keyframes pileGrow{0%,100%{border-left-width:40px;border-right-width:40px;border-bottom-width:22px;opacity:.7}50%{border-left-width:60px;border-right-width:60px;border-bottom-width:32px;opacity:1}}
.s4-pile::after{content:'';position:absolute;top:2px;left:-52px;width:104px;height:10px;background:rgba(200,165,60,.4);border-radius:50%;filter:blur(3px)}
/* surface being sandblasted */
.s4-surface{position:absolute;bottom:0;left:0;right:0;height:74px;border-radius:4px;overflow:hidden;background:#2a2218}
.s4-surface::after{content:'';position:absolute;inset:0;background:repeating-linear-gradient(90deg,rgba(0,0,0,.3) 0,rgba(0,0,0,.3) 1px,transparent 1px,transparent 42px),repeating-linear-gradient(0deg,rgba(0,0,0,.3) 0,rgba(0,0,0,.3) 1px,transparent 1px,transparent 28px)}
.s4-clean{position:absolute;bottom:0;left:50%;width:100px;height:74px;margin-left:-50px;background:linear-gradient(180deg,#d0c8bc,#c4bcb0);border-radius:2px;animation:s4CleanGrow 3s ease-in-out infinite}
@keyframes s4CleanGrow{0%,100%{width:60px;margin-left:-30px}50%{width:120px;margin-left:-60px}}
/* dust cloud */
.s4-dust-cloud{position:absolute;bottom:76px;left:50%;transform:translateX(-50%);width:70px;height:30px;background:radial-gradient(ellipse,rgba(180,150,80,.25),transparent 70%);animation:dustCloud 1.5s ease-in-out infinite alternate;border-radius:50%;filter:blur(4px)}
@keyframes dustCloud{from{transform:translateX(-50%) scale(.8);opacity:.4}to{transform:translateX(-50%) scale(1.3);opacity:.8}}
/* impact flash */
.s4-impact{position:absolute;bottom:72px;left:50%;transform:translateX(-50%);width:50px;height:20px;background:radial-gradient(ellipse,rgba(245,200,0,.2),transparent 70%);animation:impactPulse .4s ease-in-out infinite alternate}
@keyframes impactPulse{from{transform:translateX(-50%) scaleX(.6);opacity:.4}to{transform:translateX(-50%) scaleX(1.2);opacity:.9}}


/* Mobile process fallback */
.mobile-steps{display:none;padding:4rem 1.6rem;background:var(--navy)}
.mobile-step{margin-bottom:2.5rem;padding-bottom:2.5rem;border-bottom:1px solid var(--border)}
.mobile-step:last-child{border-bottom:none}
.mobile-step-head{display:flex;align-items:center;gap:1rem;margin-bottom:.7rem}
.mobile-step-num{font-family:var(--ff-h);font-size:3rem;font-weight:800;color:rgba(245,200,0,.15);line-height:1}
.mobile-step-title{font-family:var(--ff-h);font-size:1.2rem;color:var(--white)}
.mobile-step p{font-size:.92rem;color:var(--muted);font-weight:300}

/* ════════════════════════════════════════════════
   SECTION 4 — GALLERY
════════════════════════════════════════════════ */
#s-gallery{padding:9rem 0 6rem;position:relative;overflow:hidden;background:linear-gradient(170deg,#0a1628 0%,#071020 100%)}
.gallery-header{max-width:1200px;margin:0 auto 3rem;padding:0 4rem;display:flex;flex-direction:column;align-items:flex-start;gap:1.2rem}
.gallery-intro{max-width:800px}
.gallery-heading{white-space:nowrap}
.mob-br{display:none}
.gallery-strip{position:relative;display:flex;padding:2rem 4rem 5rem;overflow-x:auto;scrollbar-width:none;justify-content:center;overflow-y:hidden}
.gallery-strip::-webkit-scrollbar{display:none}
.gallery-card{position:relative;flex-shrink:0;width:300px;height:420px;margin-right:-55px;transition:transform .45s var(--ease),z-index 0s}
.gallery-card:last-child{margin-right:0}
.gallery-card:nth-child(even){transform:translateY(38px) rotate(1.1deg)}
.gallery-card:nth-child(odd){transform:translateY(-18px) rotate(-.7deg)}
.gallery-card:hover{transform:translateY(-28px) rotate(0deg) scale(1.04)!important;z-index:10}
.gallery-img-placeholder{width:100%;height:100%;position:relative;overflow:hidden}
.gallery-img-placeholder img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .6s var(--ease)}
.gallery-card:hover .gallery-img-placeholder img{transform:scale(1.06)}
.gallery-img-placeholder .img-empty{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:.8rem;color:rgba(158,195,245,.2);font-family:var(--ff-h);font-size:.58rem;letter-spacing:.12em;text-transform:uppercase;border:1px dashed rgba(158,195,245,.1);cursor:default}
.gallery-img-placeholder .img-empty svg{width:32px;height:32px;stroke:rgba(158,195,245,.35);fill:none;stroke-width:1.5}
.gallery-img-placeholder .img-empty:hover{border-color:rgba(158,195,245,.15);color:rgba(158,195,245,.35)}
.gallery-card-label{position:absolute;bottom:0;left:0;right:0;background:linear-gradient(transparent,rgba(8,15,30,.95));padding:2.5rem 1.3rem 1.1rem;transform:translateY(100%);transition:transform .35s}
.gallery-card:hover .gallery-card-label{transform:translateY(0)}
.gallery-card-label strong{font-family:var(--ff-h);font-size:.72rem;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:var(--gold);display:block;margin-bottom:.2rem}
.gallery-card-label span{font-size:.8rem;color:var(--ice);font-weight:300}
.gallery-note{text-align:center;padding:.8rem 1.4rem 0;font-size:.76rem;color:rgba(158,195,245,.28);font-weight:300;font-style:italic}
/* gallery swipe hint */
@keyframes galleryHint{
  0%{transform:translateX(0)}
  15%{transform:translateX(-28px)}
  30%{transform:translateX(12px)}
  45%{transform:translateX(-18px)}
  60%{transform:translateX(8px)}
  75%{transform:translateX(-6px)}
  88%{transform:translateX(3px)}
  100%{transform:translateX(0)}
}
.gallery-strip.hint-play{animation:galleryHint .9s cubic-bezier(.4,0,.2,1) both}
/* swipe indicator arrow */
.gallery-swipe-hint{position:absolute;bottom:1rem;left:50%;transform:translateX(-50%);display:none;align-items:center;gap:.5rem;font-family:var(--ff-h);font-size:.58rem;font-weight:700;letter-spacing:.18em;text-transform:uppercase;color:rgba(158,195,245,.5);pointer-events:none;animation:swipeHintFade 2.5s ease-out forwards}
@keyframes swipeHintFade{0%,30%{opacity:1;transform:translateX(-50%)}80%{opacity:0;transform:translateX(-40%)}100%{opacity:0;transform:translateX(-40%)}}
.gallery-swipe-hint svg{width:22px;height:14px;stroke:rgba(158,195,245,.5);fill:none;animation:arrowSlide 1s ease-in-out infinite}
@keyframes arrowSlide{0%,100%{transform:translateX(0)}50%{transform:translateX(6px)}}

/* ════════════════════════════════════════════════
   SECTION 5 — TESTIMONIALS
════════════════════════════════════════════════ */
#s-testi{padding:9rem 0;background:var(--navy);overflow:hidden}
.testi-header{max-width:1200px;margin:0 auto 4rem;padding:0 4rem}
.testi-track-outer{position:relative;overflow:hidden}
.testi-track-outer::before,.testi-track-outer::after{content:'';position:absolute;top:0;bottom:0;width:130px;z-index:2;pointer-events:none}
.testi-track-outer::before{left:0;background:linear-gradient(90deg,var(--navy),transparent)}
.testi-track-outer::after{right:0;background:linear-gradient(-90deg,var(--navy),transparent)}
.testi-track{display:flex;gap:2rem;animation:tscroll 32s linear infinite;width:max-content}
.testi-track:hover{animation-play-state:paused}
@keyframes tscroll{from{transform:translateX(0)}to{transform:translateX(-50%)}}
.tcard{width:320px;flex-shrink:0;background:rgba(17,44,96,.35);border:1px solid rgba(245,200,0,.1);padding:2rem 1.7rem;transition:border-color .3s,background .3s}
.tcard:hover{border-color:rgba(245,200,0,.3);background:rgba(17,44,96,.55)}
.tcard-stars{display:flex;gap:3px;margin-bottom:1rem}
.tcard-stars svg{width:14px;height:14px;fill:var(--gold)}
.tcard-q{font-size:.92rem;font-weight:300;font-style:italic;color:var(--cream);line-height:1.7;margin-bottom:1.2rem}
.tcard-q::before{content:'\201C';color:var(--gold)}
.tcard-q::after{content:'\201D';color:var(--gold)}
.tcard-who{font-family:var(--ff-h);font-size:.67rem;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:var(--ice)}
.tcard-loc{font-size:.76rem;color:rgba(158,195,245,.4);font-weight:300;margin-top:.12rem}

/* ════════════════════════════════════════════════
   SECTION 6 — MAP
════════════════════════════════════════════════ */
#s-map{padding:9rem 4rem;position:relative;overflow:hidden;background:var(--navy)}
#s-map::after{content:'';position:absolute;bottom:-150px;left:-150px;width:480px;height:480px;background:radial-gradient(circle,rgba(29,88,192,.12),transparent 65%);pointer-events:none}
.map-grid{display:grid;grid-template-columns:1.1fr 1fr;gap:5rem;align-items:center;max-width:1200px;margin:0 auto}
.map-text p{font-size:1rem;font-weight:300;color:rgba(246,241,230,.68);margin-bottom:1rem}
.map-text p strong{color:var(--ice);font-weight:400}
.map-stats{display:grid;grid-template-columns:1fr 1fr;gap:1px;margin-top:2rem;background:var(--border);max-width:320px}
.map-stat{padding:1.3rem 1.5rem;background:var(--navy)}
.map-stat-n{font-family:var(--ff-h);font-size:2rem;font-weight:800;color:var(--gold);line-height:1}
.map-stat-l{font-family:var(--ff-h);font-size:.58rem;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:var(--muted);margin-top:.2rem}
.town-chips{display:flex;flex-wrap:wrap;gap:.45rem;margin-top:1.8rem}
.tchip{font-family:var(--ff-h);font-size:.6rem;font-weight:700;letter-spacing:.1em;text-transform:uppercase;background:rgba(29,88,192,.2);border:1px solid rgba(29,88,192,.35);color:var(--ice);padding:.3rem .85rem;transition:background .2s,border-color .2s,color .2s;cursor:default}
.tchip:hover{background:rgba(245,200,0,.12);border-color:rgba(245,200,0,.4);color:var(--gold)}

/* Map SVG — fixed positioning */
.map-visual{position:relative;display:flex;justify-content:center;align-items:center}
.map-svg-outer{position:relative;width:100%;max-width:440px}
.map-svg-outer svg{display:block;width:100%;height:auto}
/* all map overlays use % based positioning relative to the SVG viewBox 460x460 */
.map-overlay{position:absolute;top:0;left:0;width:100%;height:100%;pointer-events:none}
.map-pulse-ring{position:absolute;border-radius:50%;background:rgba(245,200,0,.2);animation:mpr 2.6s ease-out infinite;transform:translate(-50%,-50%)}
@keyframes mpr{0%{transform:translate(-50%,-50%) scale(.5);opacity:.9}100%{transform:translate(-50%,-50%) scale(4);opacity:0}}
.map-centre{position:absolute;width:3%;height:0;padding-bottom:3%;background:var(--gold);border-radius:50%;border:2px solid var(--white);box-shadow:0 0 0 4px rgba(245,200,0,.22);transform:translate(-50%,-50%);z-index:4}
.map-town-dot{position:absolute;width:1.6%;height:0;padding-bottom:1.6%;background:var(--sky);border-radius:50%;border:1.5px solid var(--ice);transform:translate(-50%,-50%);z-index:3}
.map-town-name{position:absolute;transform:translate(-50%,calc(-50% + 12px));font-family:var(--ff-h);font-size:clamp(.45rem,.9vw,.65rem);font-weight:700;letter-spacing:.06em;text-transform:uppercase;color:var(--ice);white-space:nowrap;z-index:3}
.map-centre-name{position:absolute;transform:translate(-50%,calc(-50% + 14px));font-family:var(--ff-h);font-size:clamp(.5rem,.9vw,.65rem);font-weight:800;letter-spacing:.06em;text-transform:uppercase;color:var(--gold);white-space:nowrap;z-index:5}

/* ════════════════════════════════════════════════
   SECTION 7 — CONTACT
════════════════════════════════════════════════ */
#s-contact{padding:9rem 4rem;position:relative;overflow:hidden;background:linear-gradient(145deg,#0c1e40 0%,var(--navy) 60%)}
#s-contact::before{content:'';position:absolute;top:-100px;right:-100px;width:600px;height:600px;background:radial-gradient(circle,rgba(245,200,0,.06),transparent 65%);pointer-events:none}
.contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:start;max-width:1200px;margin:0 auto}
.contact-info-blocks{display:flex;flex-direction:row;flex-wrap:wrap;gap:1.2rem;margin-top:2rem}
.cib{display:flex;align-items:flex-start;gap:1rem;padding:1rem 1.2rem;border:1px solid rgba(245,200,0,.1);background:rgba(29,88,192,.07);transition:border-color .25s,background .25s;flex:1;min-width:180px}
.cib:hover{border-color:rgba(245,200,0,.28);background:rgba(29,88,192,.14)}
.cib-icon{flex-shrink:0;width:34px;height:34px;background:rgba(245,200,0,.1);border-radius:2px;display:flex;align-items:center;justify-content:center}
.cib-icon svg{width:17px;height:17px;stroke:var(--gold);fill:none;stroke-width:1.5}
.cib-text strong{font-family:var(--ff-h);font-size:.66rem;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:var(--gold);display:block;margin-bottom:.15rem}
.cib-text span{font-size:.9rem;color:var(--ice);font-weight:300}
.contact-form-title{font-family:var(--ff-h);font-size:1.05rem;font-weight:700;color:var(--white);margin-bottom:1.5rem;letter-spacing:.02em}
.form-body{display:flex;flex-direction:column;gap:1rem}
.form-2col{display:grid;grid-template-columns:1fr 1fr;gap:1rem}
.fg{display:flex;flex-direction:column;gap:.35rem}
.fg label{font-family:var(--ff-h);font-size:.6rem;font-weight:700;letter-spacing:.2em;text-transform:uppercase;color:rgba(158,195,245,.55)}
.fg label .req{color:var(--gold);margin-left:2px}
.fg input,.fg textarea,.fg select{background:rgba(255,255,255,.05);border:1px solid rgba(158,195,245,.14);color:var(--white);padding:.88rem 1rem;font-family:var(--ff-b);font-size:.9rem;outline:none;transition:border-color .2s,background .2s,box-shadow .2s;resize:none;-webkit-appearance:none}
.fg input:focus,.fg textarea:focus,.fg select:focus{border-color:var(--gold);background:rgba(245,200,0,.04);box-shadow:0 0 0 3px rgba(245,200,0,.08)}
.fg input::placeholder,.fg textarea::placeholder{color:rgba(158,195,245,.25)}
.fg select option{background:#0d1f3e}
.fg textarea{height:115px}
.fg .err-msg{font-family:var(--ff-h);font-size:.58rem;letter-spacing:.14em;text-transform:uppercase;color:#f56060;display:none;margin-top:.15rem}
.fg.invalid .err-msg{display:block}
.fg.invalid input,.fg.invalid textarea,.fg.invalid select{border-color:rgba(245,96,96,.5)}
.fg.valid input,.fg.valid textarea,.fg.valid select{border-color:rgba(29,188,100,.45)}
.form-check{display:flex;align-items:flex-start;gap:.8rem}
.form-check input[type=checkbox]{width:16px;height:16px;margin-top:3px;accent-color:var(--gold);flex-shrink:0}
.form-check label{font-size:.82rem;color:var(--muted);font-weight:300;font-family:var(--ff-b)}
.form-submit{width:100%;padding:1.1rem;background:var(--gold);color:var(--navy);font-family:var(--ff-h);font-weight:700;font-size:.8rem;letter-spacing:.16em;text-transform:uppercase;border:none;display:flex;align-items:center;justify-content:center;gap:.7rem;transition:background .2s,transform .15s;position:relative;overflow:hidden}
@media(pointer:fine){.form-submit{cursor:none}}
.form-submit::before{content:'';position:absolute;top:0;left:-100%;width:100%;height:100%;background:linear-gradient(90deg,transparent,rgba(255,255,255,.22),transparent);transition:left .5s}
.form-submit:hover{background:#ffd93d;transform:translateY(-2px)}
.form-submit:hover::before{left:100%}
.form-submit svg{width:17px;height:17px;stroke:var(--navy);fill:none;stroke-width:2.5}
.form-success{display:none;flex-direction:column;align-items:center;justify-content:center;padding:3rem 2rem;text-align:center;gap:1rem;border:1px solid rgba(245,200,0,.2);background:rgba(29,88,192,.1)}
.form-success.show{display:flex}
.form-success svg{width:50px;height:50px;stroke:var(--gold);fill:none;stroke-width:1.5}
.form-success h3{font-family:var(--ff-h);font-size:1.4rem;color:var(--white)}
.form-success p{font-size:.9rem;color:var(--muted);font-weight:300}

/* ════════════════════════════════════════════════
   FOOTER
════════════════════════════════════════════════ */
footer{background:#03070f;padding:2.2rem 4rem;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:1rem;border-top:1px solid rgba(245,200,0,.07);margin:0;padding-bottom:2.2rem}
.footer-logo{display:flex;align-items:center;height:136px}
.footer-logo img{height:126px;width:auto;max-width:380px;object-fit:contain;display:block}
.footer-copy{font-size:.74rem;color:rgba(158,195,245,.3);font-weight:300}
.footer-links{display:flex;gap:1.8rem}
.footer-links a{font-family:var(--ff-h);font-size:.62rem;font-weight:700;letter-spacing:.15em;text-transform:uppercase;color:rgba(158,195,245,.35);text-decoration:none;transition:color .2s}
.footer-links a:hover{color:var(--gold)}
.footer-social{display:flex;gap:1rem;align-items:center}
.footer-social a{display:flex;align-items:center;justify-content:center;width:38px;height:38px;border:1px solid rgba(158,195,245,.15);border-radius:50%;color:rgba(158,195,245,.45);text-decoration:none;transition:border-color .25s,color .25s,background .25s}
.footer-social a:hover{border-color:var(--gold);color:var(--gold);background:rgba(245,200,0,.08)}
.footer-social a svg{width:16px;height:16px;fill:currentColor}

/* ════════════════════════════════════════════════
   RESPONSIVE — MOBILE
════════════════════════════════════════════════ */

.mob-step-overlay{display:none}
@media(max-width:900px){
  /* NAV */
  nav#nav{padding:1rem 1.4rem}
  nav#nav.scrolled{padding:.75rem 1.4rem}
  .nav-logo{margin:0 auto 0 0;padding-left:.4rem}
  .nav-logo-text{display:none}
  .nav-logo-img{display:block;height:78px;width:auto;max-width:200px}
  .nav-links,.nav-tel{display:none}
  .nav-burger{display:flex}
  .nav-drawer{display:flex}

  /* HERO — prevent eyebrow overlapping h1 */
  .hero-content{padding:7rem 1.2rem 6rem}
  .hero-eyebrow{font-size:.58rem;letter-spacing:.15em;padding:.28rem .75rem;margin-bottom:1rem}
  .hero-h1{font-size:clamp(2.8rem,11vw,4.8rem);white-space:normal}
  .hero-sub{font-size:.92rem}
  .hero-strip{position:static;border-top:none;border-bottom:1px solid var(--border);flex-wrap:wrap}
  .hero-stat{padding:.85rem 1rem;min-width:50%;max-width:50%;border-right:none;border-bottom:1px solid var(--border)}
  .hero-stat:nth-child(odd){border-right:1px solid var(--border)}
  .hero-stat:nth-last-child(-n+2){border-bottom:none}
  .hero-stat-num{font-size:1.5rem}
  .scroll-cue{display:none}

  /* PROBLEM */
  #s-problem{padding:5rem 1.4rem;text-align:center}
  .problem-grid{grid-template-columns:1fr;gap:2rem;overflow:visible}
  .problem-text .section-eyebrow{justify-content:center}
  .problem-text .section-h2{text-align:center}
  .problem-text>p{text-align:center}
  .problem-icons{text-align:left}
  #paveGrid{width:min(280px,82vw);margin:0 auto;gap:4px}
  .pave-3d-wrap{transform:perspective(380px) rotateX(10deg) rotateY(-4deg);filter:drop-shadow(0 12px 28px rgba(0,0,0,.5));overflow:visible}
  .pave-visual{min-height:auto;margin-top:1.5rem;overflow:visible;display:flex;justify-content:center}
  .pave-glow{width:min(280px,78vw)!important;height:min(280px,78vw)!important}
  .problem-grid{overflow:visible}

  /* PROCESS — mobile sticky scrollytelling */
  .process-sticky-outer{height:380vh}
  .process-sticky-inner{display:grid;grid-template-rows:auto 1fr;height:100svh;min-height:100dvh;overflow:hidden}
  .mobile-steps{display:none}
  .chapter-mark{display:none}
  /* Lewa kolumna: tylko nagłówek, bez listy i progress */
  .process-left{display:flex;flex-direction:column;justify-content:center;padding:.8rem 1.4rem .5rem;border-right:none;border-bottom:1px solid var(--border);backdrop-filter:blur(8px);background:rgba(8,15,30,.92);width:100%}
  .process-left{text-align:center}
  .process-left-top .section-eyebrow{font-size:.58rem;margin-bottom:.3rem;justify-content:center}
  .process-left-top .section-h2{font-size:clamp(1.35rem,5.5vw,1.8rem)!important;line-height:.98;margin-bottom:0;text-align:center}
  .step-progress-track{display:none}
  .process-step-list{display:none}
  /* Prawa kolumna: scena na pełną pozostałą wysokość */
  .process-right{width:100%;height:100%;position:relative;overflow:hidden}
  .pscene{padding-bottom:150px}
  .scene4-wrap{height:min(180px,28vh)}
  .s4-bag-wrap{top:-10px!important}
  .s4-surface{height:55px}
  .s4-pile{bottom:62px!important;border-left-width:35px!important;border-right-width:35px!important;border-bottom-width:18px!important}
  .s4-dust-cloud{bottom:60px!important;width:55px!important;height:22px!important}
  /* Overlay: opis etapu na dole sceny */
  .mob-step-overlay{display:block;position:absolute;bottom:0;left:0;right:0;z-index:20;background:linear-gradient(transparent 0%,rgba(8,15,30,.95) 25%,rgba(8,15,30,1) 100%);padding:1.2rem 1.4rem .9rem;pointer-events:none}
  .mob-step-progress{position:absolute;top:0;left:0;height:2px;background:linear-gradient(90deg,var(--sky),var(--gold));transition:width .4s;z-index:21;border-radius:0 2px 2px 0}
  .mob-step-overlay-eyebrow{font-family:var(--ff-h);font-size:.54rem;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:rgba(245,200,0,.65);margin-bottom:.18rem;margin-top:.25rem}
  .mob-step-overlay-title{font-family:var(--ff-h);font-size:1.05rem;font-weight:800;color:var(--white);line-height:1.05;margin-bottom:.2rem}
  .mob-step-overlay-desc{font-size:.74rem;font-weight:300;color:var(--muted);line-height:1.4;margin-bottom:.5rem;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}
  .mob-step-overlay-dots{display:flex;gap:.5rem;align-items:center}
  .mob-step-overlay-dot{width:5px;height:5px;border-radius:50%;background:rgba(245,200,0,.2);transition:background .3s,transform .3s}
  .mob-step-overlay-dot.active{background:var(--gold);transform:scale(1.5)}
  /* Scene preview dimensions on mobile */
  .mobile-scene-preview{width:100%;height:200px;background:linear-gradient(135deg,#060f1e,#0a1628);border-radius:6px;margin-bottom:1rem;position:relative;overflow:hidden;display:flex;align-items:center;justify-content:center}

  /* GALLERY */
  #s-gallery{padding:5rem 0 3rem}
  .gallery-header{padding:0 1.4rem;flex-direction:column;align-items:center;text-align:center;overflow:hidden}
  .gallery-intro{width:100%;text-align:center}
  .gallery-intro .section-eyebrow{justify-content:center}
  .gallery-intro .btn-gold{display:inline-flex;margin:0 auto}
  .gallery-heading{white-space:normal!important;font-size:clamp(1.5rem,6vw,2.2rem)!important;letter-spacing:-.02em}
  .mob-br{display:none}
  .gallery-strip{padding:1.2rem 0 2.5rem;gap:.8rem;overflow-x:scroll;overflow-y:hidden;align-items:flex-start;justify-content:flex-start;scroll-snap-type:x mandatory;-webkit-overflow-scrolling:touch;padding-left:10vw;display:flex}
  .gallery-card{width:80vw;height:240px;min-height:240px;max-height:240px;margin-right:0;overflow:hidden;flex-shrink:0;scroll-snap-align:center;transform:none!important}
  @keyframes cardBounceIn{0%{opacity:0;transform:scale(.92) translateY(20px)}60%{transform:scale(1.02) translateY(-4px)}100%{opacity:1;transform:scale(1) translateY(0)}}
  .gallery-card.mob-entered{animation:cardBounceIn .5s cubic-bezier(.34,1.56,.64,1) both}
  .gallery-card:last-child{margin-right:10vw}
  .gallery-strip{cursor:grab}
  .gallery-strip:active{cursor:grabbing}
  .gallery-swipe-hint{display:flex}
  .gallery-card-label{transform:translateY(0)!important}
  .gallery-card:nth-child(n){transform:none}
  .gallery-card:hover{transform:scale(1.02)!important}
  .gallery-note{padding:.8rem 1.4rem 0}

  /* TESTIMONIALS */
  #s-testi{padding:5rem 0;overflow:hidden}
  .testi-header{padding:0 1.4rem}
  .tcard{width:78vw;max-width:78vw;padding:1.4rem 1.2rem}
  .tcard-q{font-size:.82rem}
  .testi-track-outer{overflow:hidden;max-width:100vw}

  /* MAP — fixed for mobile */
  #s-map{padding:5rem 1.4rem;text-align:center}
  .map-grid{grid-template-columns:1fr;gap:3rem}
  .map-text{text-align:center}
  .map-text .section-eyebrow{justify-content:center}
  .map-text p{text-align:center}
  .map-stats{margin:1.5rem auto 0;max-width:280px}
  .town-chips{justify-content:center}
  .map-visual{justify-content:center;margin:0 auto;max-width:360px;width:100%}
  .map-svg-outer{max-width:100%}
  .map-stats{grid-template-columns:1fr 1fr}
  /* Map town labels — smaller on mobile */
  .map-town-name{font-size:.5rem}
  .map-centre-name{font-size:.52rem}

  /* CONTACT */
  #s-contact{padding:5rem 1.4rem}
  .contact-grid{grid-template-columns:1fr;gap:3rem}
  .contact-info-blocks{flex-direction:column}
  .cib{min-width:0;width:100%;box-sizing:border-box}
  .contact-text{order:1}
  .contact-form-wrap{order:2}
  .form-2col{grid-template-columns:1fr}

  /* FOOTER */
  footer{padding:1.8rem 1.4rem;flex-direction:column;text-align:center}
  .footer-links{justify-content:center}
  .footer-social{justify-content:center}
}

/* ════════════════════════════════════════════════
   SECTION — CENNIK
════════════════════════════════════════════════ */
#s-pricing{padding:9rem 4rem;position:relative;overflow:hidden;background:linear-gradient(160deg,#070e1e 0%,#0b1830 60%,#070e1e 100%)}
#s-pricing::before{content:'';position:absolute;top:-200px;right:-100px;width:500px;height:500px;background:radial-gradient(circle,rgba(245,200,0,.05),transparent 65%);pointer-events:none}
.pricing-header{text-align:center;margin-bottom:4rem}
.pricing-grid{display:grid;grid-template-columns:1fr 1fr;gap:2rem;max-width:960px;margin:0 auto}
.pricing-card{background:rgba(17,44,96,.25);border:1px solid rgba(245,200,0,.12);padding:2.8rem 2.2rem;position:relative;transition:border-color .3s,transform .3s,box-shadow .3s}
.pricing-card:hover{border-color:rgba(245,200,0,.35);transform:translateY(-6px);box-shadow:0 24px 60px rgba(0,0,0,.4)}
.pricing-card.featured{border-color:rgba(245,200,0,.4);background:rgba(29,88,192,.2)}
.pricing-card.featured::before{content:'POLECAMY';position:absolute;top:-1px;right:2rem;background:var(--gold);color:var(--navy);font-family:var(--ff-h);font-size:.55rem;font-weight:800;letter-spacing:.2em;padding:.28rem .9rem}
.pricing-badge{font-family:var(--ff-h);font-size:.62rem;font-weight:700;letter-spacing:.22em;text-transform:uppercase;color:var(--gold);margin-bottom:.8rem;display:flex;align-items:center;gap:.5rem}
.pricing-badge::before{content:'';width:20px;height:1px;background:var(--gold)}
.pricing-name{font-family:var(--ff-h);font-size:2.4rem;font-weight:800;color:var(--white);line-height:1;margin-bottom:.4rem}
.pricing-name span{color:var(--gold)}
.pricing-tagline{font-size:.85rem;color:var(--muted);font-weight:300;font-style:italic;margin-bottom:2rem;padding-bottom:1.8rem;border-bottom:1px solid rgba(245,200,0,.1)}
.pricing-items{list-style:none;display:flex;flex-direction:column;gap:.85rem;margin-bottom:2.2rem}
.pricing-items li{display:flex;align-items:flex-start;gap:.8rem;font-size:.9rem;color:rgba(246,241,230,.8);font-weight:300}
.pricing-items li svg{flex-shrink:0;width:16px;height:16px;stroke:#4ade80;fill:none;stroke-width:2.5;margin-top:.15rem}
.pricing-items li.extra{color:rgba(74,222,128,.75)}
.pricing-items li.extra svg{stroke:#4ade80}
.pricing-cta{display:block;width:100%;padding:1rem;text-align:center;font-family:var(--ff-h);font-weight:700;font-size:.78rem;letter-spacing:.14em;text-transform:uppercase;text-decoration:none;transition:background .2s,transform .15s;border:none;cursor:pointer}
.pricing-card:not(.featured) .pricing-cta{background:rgba(245,200,0,.12);color:var(--gold);border:1px solid rgba(245,200,0,.3)}
.pricing-card:not(.featured) .pricing-cta:hover{background:rgba(245,200,0,.22)}
.pricing-card.featured .pricing-cta{background:var(--gold);color:var(--navy)}
.pricing-card.featured .pricing-cta:hover{background:#ffd93d;transform:translateY(-2px)}
.pricing-note{text-align:center;margin-top:2.2rem;font-size:.8rem;color:rgba(158,195,245,.35);font-weight:300;font-style:italic}
/* Ceny i promocja */
.pricing-price-wrap{margin:1.4rem 0 1.8rem;display:flex;align-items:flex-end;gap:1rem;flex-wrap:wrap}
.pricing-price-old{font-family:var(--ff-h);font-size:1.4rem;font-weight:700;color:#ff2222;text-decoration:line-through;text-decoration-color:#ff2222;text-decoration-thickness:3px;line-height:1}
.pricing-price-new{font-family:var(--ff-h);font-size:2.8rem;font-weight:800;color:#00ff7f;line-height:1;text-shadow:0 0 20px rgba(0,255,127,.35)}
.pricing-price-unit{font-family:var(--ff-h);font-size:.72rem;font-weight:700;color:rgba(74,222,128,.7);letter-spacing:.1em;margin-bottom:.3rem}
.pricing-savings{font-family:var(--ff-h);font-size:.72rem;font-weight:800;letter-spacing:.1em;text-transform:uppercase;color:#00ff7f;margin-left:.5rem;align-self:center;text-shadow:0 0 12px rgba(0,255,127,.4)}
@media(max-width:900px){
  #s-pricing{padding:5rem 1.4rem}
  .pricing-grid{grid-template-columns:1fr;gap:1.5rem}
  .pricing-card{padding:2rem 1.5rem}
}
</style>
</head>
<body>

<div id="cursor"></div>
<div id="cursor-dot"></div>
<div id="progress"></div>

<!-- ══════════ NAV ══════════ -->
<nav id="nav">
  <a href="#hero" class="nav-logo" id="navLogo">
    <!-- Desktop: napis Reviva -->
    <div class="nav-logo-text">Re<span>viva</span></div>
    <!-- ╔══════════════════════════════════════════════╗
         ║  LOGO MOBILE — wklej URL swojego logo      ║
         ║  Zmień src="" na adres ze Shopify:          ║
         ║  src="https://cdn.shopify.com/logo.png"    ║
         ╚══════════════════════════════════════════════╝ -->
    <img
      src="https://cdn.shopify.com/s/files/1/1044/5173/5882/files/Gemini_Generated_Image_yuei3wyuei3wyuei_18b18d9a-403c-4db8-b4d9-66856d8fd2a8.png?v=1779522368"
      alt="Logo firmy"
      class="nav-logo-img"
      id="navLogoImg"
    />
  </a>
  <div class="nav-links">
    <a href="#s-problem">Problem</a>
    <a href="#s-process">Proces</a>
    <a href="#s-gallery">Realizacje</a>
    
    <a href="#s-testi">Opinie</a>
    <a href="#s-pricing">Cennik</a>
    <a href="#s-map">Zasięg</a>
    <a href="#s-contact">Kontakt</a>
  </div>
  <a href="tel:+48579892966" class="nav-tel">
    <svg viewBox="0 0 24 24"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.36 12a19.79 19.79 0 0 1-3.07-8.67 2 2 0 0 1 2-2.18h3a2 2 0 0 1 2 1.72c.13.96.36 1.9.7 2.81a2 2 0 0 1-.45 2.11L7.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45c.9.34 1.85.57 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
    +48 579 892 966
  </a>
  <button class="nav-burger" id="burger" aria-label="Menu"><span></span><span></span><span></span></button>
</nav>

<div class="nav-drawer" id="drawer">
  <a href="#s-problem" class="drawer-link">Problem</a>
  <a href="#s-process" class="drawer-link">Proces</a>
  <a href="#s-gallery" class="drawer-link">Realizacje</a>
  <a href="#s-pricing" class="drawer-link">Cennik</a>
  <a href="#s-map" class="drawer-link">Zasięg</a>
  <a href="#s-contact" class="drawer-link">Kontakt</a>
  <a href="tel:+48579892966" class="drawer-link" style="color:var(--gold);font-size:1.3rem;letter-spacing:.05em;font-weight:700">+48 579 892 966</a>
</div>

<!-- ══════════ SECTION 1 — HERO ══════════ -->
<section id="hero">
  <canvas id="hero-canvas"></canvas>
  <div class="hero-particles" id="hParticles"></div>

  <div class="hero-content">
    <div class="hero-eyebrow">
      <svg viewBox="0 0 24 24" fill="none" stroke="var(--gold)" stroke-width="1.5" stroke-linecap="round" xmlns="http://www.w3.org/2000/svg"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
      Zblewo &amp; okolice &middot; 20 km zasięgu
    </div>
    <h1 class="hero-h1">
      Twoja kostka<br/>
      <span class="hollow">zasługuje</span><br/>
      na <span class="gold">blask</span>
    </h1>
    <p class="hero-sub">Profesjonalne mycie i czyszczenie kostki brukowej — usuwamy mech, glony i zabrudzenia, przywracając pierwotny wygląd nawierzchni.</p>
    <div class="hero-ctas">
      <a href="#s-contact" class="btn-gold">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
        Bezpłatna wycena
      </a>
      <a href="#s-process" class="btn-outline">Jak działamy?</a>
    </div>
  </div>

  <div class="hero-strip">
    <div class="hero-stat">
      <div class="hero-stat-num">100<span style="color:var(--amber)">%</span></div>
      <div class="hero-stat-label">Zadowolonych klientów</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-num">20 km</div>
      <div class="hero-stat-label">Zasięg działania</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-num">szybki</div>
      <div class="hero-stat-label">Czas realizacji</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-num">100<span style="color:var(--amber)">%</span></div>
      <div class="hero-stat-label">Topowe preparaty</div>
    </div>
  </div>

  <div class="scroll-cue">
    <div class="scroll-cue-line"></div>
    <span class="scroll-cue-label"></span>
  </div>
</section>

<!-- ══════════ SECTION 2 — PROBLEM ══════════ -->
<section id="s-problem">
  <div class="chapter-mark">Rozdział 01</div>
  <div class="problem-grid">
    <div class="problem-text reveal-l">
      <div class="section-eyebrow">Problem</div>
      <h2 class="section-h2">Mech, glony<br/>i czas robią<br/><span style="color:var(--ice)">swoje</span></h2>
      <p>Woda z węża i środki z marketu usuwają brud tylko powierzchownie, przez co problem wraca już po kilku dniach. Nasz sprzęt ciśnieniowy i specjalistyczne preparaty usuwają zabrudzenia dogłębnie.<strong> Przywróć kostce czysty wygląd i zadbaj o bezpieczeństwo przed domem.</strong></p>
      <p></p>
      <div class="problem-icons">
        <div class="problem-icon-row">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
          <div><strong>Zagrożenie bezpieczeństwa</strong><span>Mech i glony zwiększają ryzyko poślizgnięcia do 4-krotnie.</span></div>
        </div>
        <div class="problem-icon-row">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
          <div><strong>Trwałe zniszczenia</strong><span>Zabrudzenia biologiczne wnikają w strukturę kamienia i cegły.</span></div>
        </div>
        <div class="problem-icon-row">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" stroke-linecap="round" stroke-linejoin="round"><line x1="12" y1="1" x2="12" y2="23"/><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/></svg>
          <div><strong>Utrata wartości nieruchomości</strong><span>Zaniedbane podjazdy i tarasy obniżają wartość posesji.</span></div>
        </div>
      </div>
    </div>
    <div class="pave-visual reveal-r" id="paveVisual">
      <div class="pave-glow"></div>
      <div class="pave-3d-wrap"><div id="paveGrid"></div></div>
      <div class="wipe-bar" id="wipeBar"></div>
    </div>
  </div>
</section>

<!-- ══════════ SECTION 4 — GALLERY ══════════ -->
<section id="s-gallery">
  <div class="gallery-header">
    <div class="gallery-intro reveal-l">
      <div class="section-eyebrow">Realizacje</div>
      <h2 class="section-h2 gallery-heading">Nasze najlepsze<br class="mob-br"/> prace</h2>
      <p class="section-lead" style="margin:1rem 0 1.4rem;max-width:52ch">Twoja kostka z dużą szansą znajdzie się tu rownież!</p>
      <div style="display:flex;align-items:center;gap:1.4rem;flex-wrap:wrap">
        <a href="#s-pricing" class="btn-gold" style="font-size:.72rem;padding:.85rem 1.8rem">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2z"/><path d="M12 6v6l4 2"/></svg>
          Sprawdź cenę
        </a>

      </div>
    </div>
  </div>
    <div class="gallery-strip" id="galleryStrip">
    <div class="gallery-swipe-hint" id="galleryHintEl"><svg viewBox="0 0 22 14"><polyline points="1 7 15 7"/><polyline points="10 2 15 7 10 12"/><polyline points="16 7 22 7" opacity=".4"/></svg>przesuń</div>
    <!--
    ╔═══════════════════════════════════════════════════════╗
    ║  ZDJĘCIE 1: Podjazd · Starogard Gd.                ║
    ║  Wklej adres URL swojego zdjęcia w src="" poniżej:   ║
    ║  src="https://cdn.shopify.com/s/.../twoje-zdjecie.jpg"║
    ╚═══════════════════════════════════════════════════════╝
    -->
    <div class="gallery-card reveal">
      <div class="gallery-img-placeholder" id="gcard-0">
        <img
          id="gimg-0"
          src="https://cdn.shopify.com/s/files/1/1044/5173/5882/files/pobrane_1.jpg?v=1780134088"
          alt="Podjazd · Starogard Gd."
          onerror="this.style.display='none';document.getElementById('gph-0').style.display='flex'"
          onload="this.style.display='block';this.style.objectFit='cover';this.style.width='100%';this.style.height='100%';document.getElementById('gph-0').style.display='none'"
        />
        <div class="img-empty" id="gph-0" style="pointer-events:none;cursor:default">
          <svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          
        </div>
      </div>
      <div class="gallery-card-label"><strong>Wokół domu · Zblewo</strong><span> 130 m²</span></div>
    </div>
    <!--
    ╔═══════════════════════════════════════════════════════╗
    ║  ZDJĘCIE 2: Taras · Zblewo                         ║
    ║  Wklej adres URL swojego zdjęcia w src="" poniżej:   ║
    ║  src="https://cdn.shopify.com/s/.../twoje-zdjecie.jpg"║
    ╚═══════════════════════════════════════════════════════╝
    -->
    <div class="gallery-card reveal">
      <div class="gallery-img-placeholder" id="gcard-1">
        <img
          id="gimg-1"
          src="https://cdn.shopify.com/s/files/1/1044/5173/5882/files/Gemini_Generated_Image_gpab8kgpab8kgpab.png?v=1780134091"
          alt="Taras · Zblewo"
          onerror="this.style.display='none';document.getElementById('gph-1').style.display='flex'"
          onload="this.style.display='block';this.style.objectFit='cover';this.style.width='100%';this.style.height='100%';document.getElementById('gph-1').style.display='none'"
        />
        <div class="img-empty" id="gph-1" style="pointer-events:none;cursor:default">
          <svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          
        </div>
      </div>
      <div class="gallery-card-label"><strong>Wjazd · Zblewo</strong><span> 52 m²</span></div>
    </div>
    <!--
    ╔═══════════════════════════════════════════════════════╗
    ║  ZDJĘCIE 3: Chodnik · Skarszewy                    ║
    ║  Wklej adres URL swojego zdjęcia w src="" poniżej:   ║
    ║  src="https://cdn.shopify.com/s/.../twoje-zdjecie.jpg"║
    ╚═══════════════════════════════════════════════════════╝
    -->
    <div class="gallery-card reveal">
      <div class="gallery-img-placeholder" id="gcard-2">
        <img
          id="gimg-2"
          src="https://cdn.shopify.com/s/files/1/1044/5173/5882/files/Gemini_Generated_Image_52xya52xya52xya5.png?v=1780134090"
          alt="Chodnik · Skarszewy"
          onerror="this.style.display='none';document.getElementById('gph-2').style.display='flex'"
          onload="this.style.display='block';this.style.objectFit='cover';this.style.width='100%';this.style.height='100%';document.getElementById('gph-2').style.display='none'"
        />
        <div class="img-empty" id="gph-2" style="pointer-events:none;cursor:default">
          <svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          
        </div>
      </div>
      <div class="gallery-card-label"><strong>Podjazd · Skarszewy</strong><span> 120 m²</span></div>
    </div>
    <!--
    ╔═══════════════════════════════════════════════════════╗
    ║  ZDJĘCIE 4: Taras · Gniew                          ║
    ║  Wklej adres URL swojego zdjęcia w src="" poniżej:   ║
    ║  src="https://cdn.shopify.com/s/.../twoje-zdjecie.jpg"║
    ╚═══════════════════════════════════════════════════════╝
    -->
    <div class="gallery-card reveal">
      <div class="gallery-img-placeholder" id="gcard-3">
        <img
          id="gimg-3"
          src="https://cdn.shopify.com/s/files/1/1044/5173/5882/files/Gemini_Generated_Image_3qhlzz3qhlzz3qhl.png?v=1780134091"
          alt="Taras · Gniew"
          onerror="this.style.display='none';document.getElementById('gph-3').style.display='flex'"
          onload="this.style.display='block';this.style.objectFit='cover';this.style.width='100%';this.style.height='100%';document.getElementById('gph-3').style.display='none'"
        />
        <div class="img-empty" id="gph-3" style="pointer-events:none;cursor:default">
          <svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          
        </div>
      </div>
      <div class="gallery-card-label"><strong>Chodnik · Zblewo</strong><span> 52 m²</span></div>
    </div>
    <!--
    ╔═══════════════════════════════════════════════════════╗
    ║  ZDJĘCIE 5: Alejka · Pelplin                       ║
    ║  Wklej adres URL swojego zdjęcia w src="" poniżej:   ║
    ║  src="https://cdn.shopify.com/s/.../twoje-zdjecie.jpg"║
    ╚═══════════════════════════════════════════════════════╝
    -->
    <div class="gallery-card reveal">
      <div class="gallery-img-placeholder" id="gcard-4">
        <img
          id="gimg-4"
          src="https://cdn.shopify.com/s/files/1/1044/5173/5882/files/atena-z-kruszywem-safari-gladio-kostka-brukowa-ogrodzenia_s00.jpg?v=1780134088"
          alt="Alejka · Pelplin"
          onerror="this.style.display='none';document.getElementById('gph-4').style.display='flex'"
          onload="this.style.display='block';this.style.objectFit='cover';this.style.width='100%';this.style.height='100%';document.getElementById('gph-4').style.display='none'"
        />
        <div class="img-empty" id="gph-4" style="pointer-events:none;cursor:default">
          <svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          
        </div>
      </div>
      <div class="gallery-card-label"><strong>Chodnik · Starogard.Gd</strong><span> 68 m²</span></div>
    </div>
    </div>
    <p class="gallery-note"></p>
</section>

<!-- ══════════ SECTION 3 — 3D SCROLLYTELLING ══════════ -->
<section id="s-process">
  <div class="process-sticky-outer" id="processOuter">
    <div class="process-sticky-inner">

      <div class="process-left">
        <div class="process-left-top">
          <div class="section-eyebrow">Proces</div>
          <div class="step-progress-track"><div class="step-progress-fill" id="stepFill"></div></div>
          <h2 class="section-h2" style="font-size:clamp(1.8rem,2.8vw,3rem)">5 etapów do<br/><span style="color:var(--gold)">czystej</span><br/>nawierzchni</h2>
        </div>
        <div class="process-step-list" id="pstepList">
          <div class="pstep active" data-step="0">
            <div class="pstep-num">01</div>
            <div class="pstep-title">Usuwanie chwastów</div>
            <div class="pstep-desc">Mechaniczne i chemiczne usunięcie mchu, chwastów i glonów ze spoin i powierzchni.</div>
          </div>
          <div class="pstep" data-step="1">
            <div class="pstep-num">02</div>
            <div class="pstep-title">Płukanie wysokociśnieniowe</div>
            <div class="pstep-desc">Strumień wody pod wysokim ciśnieniem zrywa zabrudzenia i wypłukuje pozostałości.</div>
          </div>
          <div class="pstep" data-step="2">
            <div class="pstep-num">03</div>
            <div class="pstep-title">Szorowanie</div>
            <div class="pstep-desc">Rotacyjne szczotki docierają do struktury i usuwają uparty brud, tłuszcz i przebarwienia.</div>
          </div>
          <div class="pstep" data-step="3">
            <div class="pstep-num">04</div>
            <div class="pstep-title">Impregnacja <span style="font-size:.62rem;color:#4ade80;font-weight:700;letter-spacing:.04em">(opcja płatna)</span></div>
            <div class="pstep-desc">Powłoka ochronna blokuje wilgoć i porosty. Dostępna jako usługa dodatkowa — wycena indywidualna.</div>
          </div>
          <div class="pstep" data-step="4">
            <div class="pstep-num">05</div>
            <div class="pstep-title">Piaskowanie <span style="font-size:.58rem;color:#4ade80;font-weight:700;letter-spacing:.04em"></span></div>
            <div class="pstep-desc">Precyzyjne piaskowanie usuwa możliwość zapadnięcia i odświeża wytrwałość. <span style="color:#4ade80;font-weight:600">Gratis w ramach naszych usług.</span></div>
          </div>
        </div>
      </div>

      <div class="process-right">
        <div class="process-visual">

          <!-- SCENE 0: Usuwanie chwastów -->
          <div class="pscene active" id="pscene-0">
            <div class="scene0-wrap">
              <div class="scene0-grid" id="scene0grid"></div>
              <div class="s0-tool" id="s0tool">
                <svg viewBox="0 0 44 44" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <rect x="18" y="2" width="8" height="28" rx="3" fill="var(--gold)" opacity=".9"/>
                  <rect x="8" y="28" width="28" height="8" rx="3" fill="#888"/>
                  <line x1="10" y1="36" x2="10" y2="42" stroke="#888" stroke-width="2.5" stroke-linecap="round"/>
                  <line x1="22" y1="36" x2="22" y2="42" stroke="#888" stroke-width="2.5" stroke-linecap="round"/>
                  <line x1="34" y1="36" x2="34" y2="42" stroke="#888" stroke-width="2.5" stroke-linecap="round"/>
                </svg>
              </div>
              <div class="s0-dust" style="width:40px;height:40px;top:50%;left:40%;animation-duration:1.2s;animation-delay:0s"></div>
              <div class="s0-dust" style="width:28px;height:28px;top:55%;left:60%;animation-duration:1.5s;animation-delay:.4s"></div>
            </div>
            <div class="pscene-num">01</div>
          </div>

          <!-- SCENE 1: Płukanie wysokociśnieniowe -->
          <div class="pscene" id="pscene-1">
            <div class="scene1-wrap">
              <!-- Kurtyna wody -->
              <div class="s1-water-curtain"></div>
              <!-- Krople -->
              <div class="s1-drop" style="left:15%;height:40px;animation-duration:1.1s;animation-delay:0s"></div>
              <div class="s1-drop" style="left:28%;height:55px;animation-duration:.95s;animation-delay:.3s"></div>
              <div class="s1-drop" style="left:42%;height:35px;animation-duration:1.2s;animation-delay:.1s"></div>
              <div class="s1-drop" style="left:57%;height:48px;animation-duration:.9s;animation-delay:.5s"></div>
              <div class="s1-drop" style="left:71%;height:42px;animation-duration:1.05s;animation-delay:.2s"></div>
              <div class="s1-drop" style="left:85%;height:38px;animation-duration:1.15s;animation-delay:.4s"></div>
              <!-- Siatka kostki -->
              <div class="s1-grid" id="s1grid"></div>
              <!-- Kałuże -->
              <div class="s1-puddle" style="left:20%;animation-delay:.3s"></div>
              <div class="s1-puddle" style="left:55%;animation-delay:.8s;width:30px"></div>
              <!-- Refleks -->
              <div class="s1-glint" style="bottom:6px"></div>
            </div>
            <div class="pscene-num">02</div>
          </div>

          <!-- SCENE 2: Szorowanie -->
          <div class="pscene" id="pscene-2">
            <div class="scene2-wrap">
              <div class="s2-brush-wrap">
                <div class="s2-brush" id="s2brush"></div>
              </div>
              <div id="s2foams"></div>
              <div class="s2-surface"><div class="s2-clean-bar"></div></div>
              <div class="s2-scratch"></div>
              <div class="s2-scratch" style="bottom:90px;animation-delay:.6s;opacity:.08"></div>
            </div>
            <div class="pscene-num">03</div>
          </div>

          <!-- SCENE 3: Impregnacja -->
          <div class="pscene" id="pscene-3">
            <div class="scene3-wrap">
              <div class="orbit orbit-1"><div class="orbit-dot"></div></div>
              <div class="orbit orbit-2"><div class="orbit-dot"></div></div>
              <div class="orbit orbit-3"><div class="orbit-dot"></div></div>
              <div class="shield-hex">
                <svg viewBox="0 0 100 115" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M50 5 L90 25 L90 65 Q90 95 50 110 Q10 95 10 65 L10 25 Z" stroke="var(--gold)" stroke-width="2" fill="rgba(245,200,0,.06)"/>
                  <path d="M50 20 L78 34 L78 62 Q78 84 50 96 Q22 84 22 62 L22 34 Z" stroke="rgba(245,200,0,.4)" stroke-width="1" fill="rgba(245,200,0,.04)"/>
                  <path d="M36 57 L46 67 L66 47" stroke="var(--gold)" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </div>
              <div class="clean-tiles-sm" id="cleanTiles"></div>
            </div>
            <div class="pscene-num">04</div>
          </div>


          <!-- SCENE 4: Piaskowanie -->
          <div class="pscene" id="pscene-4">
            <div class="scene4-wrap">
              <!-- Worek z piaskiem SVG -->
              <div class="s4-bag-wrap">
                <svg width="90" height="120" viewBox="0 0 90 120" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <!-- linka zawieszenia -->
                  <line x1="45" y1="0" x2="45" y2="12" stroke="#aaa" stroke-width="3" stroke-linecap="round"/>
                  <!-- węzeł/zaciśnięcie górne -->
                  <ellipse cx="45" cy="18" rx="9" ry="6" fill="#8a6820" stroke="#6a4e10" stroke-width="1.5"/>
                  <!-- ciało worka — jutowy kształt -->
                  <path d="M22 24 Q14 38 14 62 Q14 90 45 95 Q76 90 76 62 Q76 38 68 24 Z"
                        fill="url(#bagGrad)" stroke="#7a5a18" stroke-width="1.5"/>
                  <!-- poziome szwy na worku -->
                  <path d="M20 42 Q45 46 70 42" stroke="rgba(0,0,0,.25)" stroke-width="1.2" fill="none" stroke-linecap="round"/>
                  <path d="M17 58 Q45 63 73 58" stroke="rgba(0,0,0,.2)" stroke-width="1.2" fill="none" stroke-linecap="round"/>
                  <path d="M18 74 Q45 79 72 74" stroke="rgba(0,0,0,.2)" stroke-width="1.2" fill="none" stroke-linecap="round"/>
                  <!-- pionowe szwy -->
                  <path d="M30 25 Q29 60 32 93" stroke="rgba(0,0,0,.15)" stroke-width="1" fill="none"/>
                  <path d="M60 25 Q61 60 58 93" stroke="rgba(0,0,0,.15)" stroke-width="1" fill="none"/>
                  <!-- napis SAND na worku -->
                  <text x="45" y="66" text-anchor="middle" font-family="sans-serif" font-size="9" font-weight="700"
                        fill="rgba(0,0,0,.3)" letter-spacing="3">SAND</text>
                  <!-- podświetlenie -->
                  <path d="M28 28 Q22 50 24 72" stroke="rgba(255,255,255,.18)" stroke-width="5" fill="none" stroke-linecap="round"/>
                  <!-- dziurka na dole skąd sypie się piasek -->
                  <ellipse cx="45" cy="95" rx="5" ry="3" fill="#3a2205"/>
                  <defs>
                    <linearGradient id="bagGrad" x1="14" y1="24" x2="76" y2="95" gradientUnits="userSpaceOnUse">
                      <stop offset="0%" stop-color="#d4a84a"/>
                      <stop offset="40%" stop-color="#b07828"/>
                      <stop offset="100%" stop-color="#8a5e18"/>
                    </linearGradient>
                  </defs>
                </svg>
              </div>
              <!-- Strumień piasku z dziurki -->
              <div style="position:absolute;top:126px;left:50%;transform:translateX(-50%);width:10px;height:50px;background:linear-gradient(180deg,rgba(200,165,80,.88),rgba(200,165,80,.15));border-radius:0 0 6px 6px;animation:streamWiden 3s ease-in-out infinite"></div>
              <!-- Sand grains -->
              <div id="s4grains"></div>
              <!-- Pile & impact -->
              <div class="s4-pile"></div>
              <div class="s4-dust-cloud"></div>
              <div class="s4-impact"></div>
              <!-- Surface -->
              <div class="s4-surface"><div class="s4-clean"></div></div>
            </div>
            <div class="pscene-num">05</div>
          </div>

        </div>
        <div class="step-dots" id="stepDots">
          <div class="sdot active"></div>
          <div class="sdot"></div>
          <div class="sdot"></div>
          <div class="sdot"></div>
          <div class="sdot"></div>
        </div>
        <!-- Mobile sticky overlay — opis etapu -->
        <div class="mob-step-overlay" id="mobStepOverlay">
          <div class="mob-step-progress" id="mobStepProgress" style="width:20%"></div>
          <div class="mob-step-overlay-eyebrow" id="mobStepNum">Etap 01 / 05</div>
          <div class="mob-step-overlay-title" id="mobStepTitle">Usuwanie chwastów</div>
          <div class="mob-step-overlay-desc" id="mobStepDesc">Mechaniczne i chemiczne usunięcie mchu, chwastów i glonów ze spoin i nawierzchni.</div>
          <div class="mob-step-overlay-dots" id="mobStepDots">
            <div class="mob-step-overlay-dot active"></div>
            <div class="mob-step-overlay-dot"></div>
            <div class="mob-step-overlay-dot"></div>
            <div class="mob-step-overlay-dot"></div>
            <div class="mob-step-overlay-dot"></div>
          </div>
        </div>
      </div>

    </div>
  </div>



<!-- ══════════ CENNIK ══════════ -->
<section id="s-pricing">
  <div class="pricing-header reveal">
    <div class="section-eyebrow" style="justify-content:center">Cennik</div>
    <h2 class="section-h2">Wybierz swój<br/><span style="color:var(--gold)">pakiet</span></h2>
    <p class="section-lead" style="margin:1rem auto 0">Wszystkie ceny ustalane indywidualnie — poniżej orientacyjny zakres usług w każdym pakiecie. Wycena bezpłatna.</p>
  </div>

  <div class="pricing-grid">

    <!-- PAKIET PRO -->
    <div class="pricing-card reveal-l">
      <div class="pricing-badge">Pakiet podstawowy</div>
      <div class="pricing-name">PRO<span>.</span></div>
      <div class="pricing-price-wrap">
        <div>
          <div class="pricing-price-old">20 zł/m²</div>
          <div class="pricing-price-new">10 zł<span class="pricing-price-unit">/m²</span></div>
        </div>
        <div class="pricing-savings">−50%</div>
      </div>
      <div class="pricing-tagline">Kompleksowe oczyszczanie nawierzchni — idealne na start.</div>
      <ul class="pricing-items">
        <li>
          <svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>
          Wyrwanie zielska i usunięcie mchu
        </li>
        <li>
          <svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>
          Płukanie wysokociśnieniowe
        </li>
        <li>
          <svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>
          Szorowanie rotacyjne spoin i powierzchni
        </li>
        <li>
          <svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>
          Piaskowanie — <span style="color:#4ade80;font-weight:600">gratis w ramach usługi</span>
        </li>
      </ul>
      <a href="#s-contact" class="pricing-cta">Zamów wycenę</a>
    </div>

    <!-- PAKIET DELUXE -->
    <div class="pricing-card featured reveal-r">
      <div class="pricing-badge">Pakiet premium</div>
      <div class="pricing-name">DE<span>LUXE</span></div>
      <div class="pricing-price-wrap">
        <div>
          <div class="pricing-price-old">32 zł/m²</div>
          <div class="pricing-price-new">16 zł<span class="pricing-price-unit">/m²</span></div>
        </div>
        <div class="pricing-savings">−50%</div>
      </div>
      <div class="pricing-tagline">Wszystko z PRO + ochrona długoterminowa. Efekt nawet na lata.</div>
      <ul class="pricing-items">
        <li>
          <svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>
          Wyrwanie zielska i usunięcie mchu
        </li>
        <li>
          <svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>
          Płukanie wysokociśnieniowe
        </li>
        <li>
          <svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>
          Szorowanie rotacyjne spoin i powierzchni
        </li>
        <li>
          <svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>
          Piaskowanie — <span style="color:#4ade80;font-weight:600">gratis w ramach usługi</span>
        </li>
        <li class="extra">
          <svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>
          <strong>Impregnacja ochronna</strong> — powłoka blokująca wilgoć i glony
        </li>
      </ul>
      <a href="#s-contact" class="pricing-cta">Zamów wycenę</a>
    </div>

  </div>
  <p class="pricing-note">Ceny zależą od rodzaju nawierzchni, powierzchni i stopnia zabrudzenia. Dojazd w promieniu 20 km od Zblewa — zawsze gratis.</p>
</section>

<!-- ══════════ SECTION 6 — MAP ══════════ -->
<section id="s-map">
  <div class="chapter-mark">Rozdział 04</div>
  <div class="map-grid">
    <div class="map-text reveal-l">
      <div class="section-eyebrow">Zasięg działania</div>
      <h2 class="section-h2">Zblewo<br/>i okolice<br/><span style="color:var(--gold)">+20 km</span></h2>
      <p>Obsługujemy cały region w promieniu 20 km od Zblewa. <strong>Dojazd jest bezpłatny</strong> — żadnych ukrytych kosztów transportu.</p>
      <p>Jesteś poza zasięgiem? Zadzwoń — przy większych zleceniach wyjeżdżamy dalej.</p>
      <div class="map-stats">
        <div class="map-stat"><div class="map-stat-n">20 km</div><div class="map-stat-l">Zasięg dojazdu</div></div>
        <div class="map-stat"><div class="map-stat-n">0 zł</div><div class="map-stat-l">Koszt dojazdu</div></div>
      </div>
      <div class="town-chips">
        <span class="tchip">Zblewo</span>
        <span class="tchip">Starogard Gdański</span>
        <span class="tchip">Skarszewy</span>
        <span class="tchip">Pinczyn</span>
        <span class="tchip">Semlin</span>
        <span class="tchip">Kaliska</span>
        <span class="tchip">Stara kiszewa</span>
        <span class="tchip">Lubichowo</span>
      </div>
    </div>

    <!-- SVG map — all towns positioned as % of 460x460 viewBox -->
    <div class="map-visual reveal-r">
      <div class="map-svg-outer" id="mapOuter">
        <svg viewBox="0 0 460 460" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <radialGradient id="mapGlow" cx="50%" cy="50%" r="50%">
              <stop offset="0%" stop-color="rgba(29,88,192,.15)"/>
              <stop offset="100%" stop-color="transparent"/>
            </radialGradient>
          </defs>
          <rect width="460" height="460" fill="rgba(8,15,30,.75)" rx="4"/>
          <circle cx="230" cy="230" r="170" fill="rgba(29,88,192,.07)" stroke="rgba(245,200,0,.22)" stroke-width="1.5" stroke-dasharray="9 5"/>
          <circle cx="230" cy="230" r="90"  fill="rgba(29,88,192,.05)" stroke="rgba(245,200,0,.1)"  stroke-width="1"   stroke-dasharray="5 4"/>
          <circle cx="230" cy="230" r="170" fill="url(#mapGlow)"/>
          <line x1="60"  y1="230" x2="400" y2="230" stroke="rgba(158,195,245,.07)" stroke-width="1.5"/>
          <line x1="230" y1="60"  x2="230" y2="400" stroke="rgba(158,195,245,.07)" stroke-width="1.5"/>
          <!-- Wierzyca stylised -->
          <path d="M200 60 Q215 110 205 155 Q193 200 208 230 Q222 260 210 310 Q198 355 215 400" fill="none" stroke="rgba(29,88,192,.4)" stroke-width="3" stroke-linecap="round"/>
          <!-- Scale -->
          <line x1="330" y1="425" x2="410" y2="425" stroke="rgba(158,195,245,.25)" stroke-width="1.5"/>
          <line x1="330" y1="420" x2="330" y2="430" stroke="rgba(158,195,245,.25)" stroke-width="1.5"/>
          <line x1="410" y1="420" x2="410" y2="430" stroke="rgba(158,195,245,.25)" stroke-width="1.5"/>
          <text x="370" y="418" text-anchor="middle" fill="rgba(158,195,245,.35)" font-size="9" font-family="Syne" letter-spacing="2">20 KM</text>
        </svg>

        <!-- Overlay elements positioned as % of 460px -->
        <div class="map-overlay">
          <!-- ZBLEWO — centrum mapy -->
          <div class="map-pulse-ring" style="left:50%;top:50%;width:38px;height:38px;"></div>
          <div class="map-pulse-ring" style="left:50%;top:50%;width:38px;height:38px;animation-delay:.9s"></div>
          <div class="map-centre" style="left:50%;top:50%;"></div>
          <div class="map-centre-name" style="left:50%;top:calc(50% + 3px)">Zblewo</div>

          <!-- Smętowo Graniczne — 5km N (tuż nad Zblewem) -->
          <div class="map-town-dot" style="left:52%;top:35%;padding-bottom:1.2%;width:1.2%"></div>
          <div class="map-town-name" style="left:52%;top:calc(35% + 2px);font-size:clamp(.4rem,.75vw,.54rem)">Pinczyn</div>

          <!-- Jabłowo — 4km SE -->
          <div class="map-town-dot" style="left:60%;top:58%;padding-bottom:1.2%;width:1.2%"></div>
          <div class="map-town-name" style="left:60%;top:calc(58% + 2px);font-size:clamp(.4rem,.75vw,.54rem)">Semlin</div>

          <!-- Pinczyn — 6km W -->
          <div class="map-town-dot" style="left:36%;top:49%;padding-bottom:1.2%;width:1.2%"></div>
          <div class="map-town-name" style="left:36%;top:calc(49% + 2px);font-size:clamp(.4rem,.75vw,.54rem)">Bytonia</div>

          <!-- Starogard Gdański — 8km E -->
          <div class="map-town-dot" style="left:74%;top:46%"></div>
          <div class="map-town-name" style="left:74%;top:calc(46% + 2px)">Starogard Gd.</div>

          <!-- Czarna Woda — 12km N -->
          <div class="map-town-dot" style="left:42%;top:22%"></div>
          <div class="map-town-name" style="left:42%;top:calc(22% + 2px)">Skarszewy</div>

          <!-- Bobowo — 10km SE -->
          <div class="map-town-dot" style="left:67%;top:65%"></div>
          <div class="map-town-name" style="left:67%;top:calc(65% + 2px)">Lubichowo</div>

          <!-- Skarszewy — 14km SW -->
          <div class="map-town-dot" style="left:24%;top:70%"></div>
          <div class="map-town-name" style="left:24%;top:calc(70% + 2px)">Kaliska</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════ SECTION 7 — CONTACT ══════════ -->
<section id="s-contact">
  <div class="chapter-mark">Rozdział 05</div>
  <div class="contact-grid">
    <div class="contact-text reveal-l">
      <div class="section-eyebrow">Kontakt</div>
      <h2 class="section-h2">Zamów<br/><span style="color:var(--gold)">bezpłatną</span><br/>wycenę</h2>
      <p class="section-lead">Odpiszemy lub oddzwonimy jeszcze dziś. Dojazd gratis w promieniu 20 km od Zblewa.</p>
      <div class="contact-info-blocks">
        <div class="cib" onclick="copyToClipboard('+48579892966','Numer skopiowany!')" style="cursor:pointer" title="Kliknij aby skopiować numer">
          <div class="cib-icon"><svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.36 12a19.79 19.79 0 0 1-3.07-8.67 2 2 0 0 1 2-2.18h3a2 2 0 0 1 2 1.72c.13.96.36 1.9.7 2.81a2 2 0 0 1-.45 2.11L7.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45c.9.34 1.85.57 2.81.7A2 2 0 0 1 22 16.92z"/></svg></div>
          <div class="cib-text"><strong>Telefon <span id="telCopied" style="color:#4ade80;font-size:.6rem;opacity:0;transition:opacity .3s;font-weight:700;letter-spacing:.08em"> ✓ skopiowano</span></strong><span>+48 579 892 966<br/>Pon–Sob 7:00–20:00</span></div>
        </div>
        <div class="cib" onclick="copyToClipboard('Revivaa@wp.pl','E-mail skopiowany!')" style="cursor:pointer" title="Kliknij aby skopiować e-mail">
          <div class="cib-icon"><svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg></div>
          <div class="cib-text"><strong>E-mail <span id="emailCopied" style="color:#4ade80;font-size:.6rem;opacity:0;transition:opacity .3s;font-weight:700;letter-spacing:.08em"> ✓ skopiowano</span></strong><span>Revivaa@wp.pl<br/>Odpiszemy błyskawicznie!</span></div>
        </div>

      </div>
    </div>

    <div class="contact-form-wrap reveal-r" style="align-self:start">
      <div class="contact-form-title">Wyślij zapytanie — odpiszemy dziś!</div>
      <div class="form-body" id="formBody">
        <div class="form-2col">
          <div class="fg" id="fg-name">
            <label for="f-name">Imię i nazwisko <span class="req">*</span></label>
            <input id="f-name" type="text" placeholder="Jan Kowalski" autocomplete="name"/>
            <span class="err-msg">Proszę podać imię i nazwisko</span>
          </div>
          <div class="fg" id="fg-phone">
            <label for="f-phone">Telefon <span class="req">*</span></label>
            <input id="f-phone" type="tel" placeholder="+48 500 000 000" autocomplete="tel"/>
            <span class="err-msg">Podaj poprawny numer telefonu</span>
          </div>
        </div>
        <div class="fg" id="fg-email">
          <label for="f-email">Adres e-mail <span class="req">*</span></label>
          <input id="f-email" type="email" placeholder="jan@email.com" autocomplete="email"/>
          <span class="err-msg">Podaj poprawny adres e-mail</span>
        </div>
        <div class="fg" id="fg-city">
          <label for="f-city">Miejscowość</label>
          <input id="f-city" type="text" placeholder="np. Starogard Gdański, Skarszewy…"/>
        </div>
        <div class="fg" id="fg-service">
          <label for="f-service">Rodzaj usługi</label>
          <select id="f-service">
            <option value="">— Wybierz usługę —</option>
            <option>Pakiet PRO (Zielsko,Płukanie,Szorowanie,Piaskowanie)</option>
            <option>Pakiet DELUXE (Zielsko,Płukanie,Szorowanie,Piaskowanie,Impregnacja)</option>
            <option>Inne</option> 
          </select>
        </div>
        <div class="fg" id="fg-msg">
          <label for="f-msg">Opis zlecenia</label>
          <textarea id="f-msg" placeholder="Rodzaj nawierzchni, przybliżona powierzchnia w m², aktualny stan…"></textarea>
        </div>
        <div class="form-check">
          <input type="checkbox" id="f-agree"/>
          <label for="f-agree">Wyrażam zgodę na przetwarzanie moich danych osobowych w celu odpowiedzi na zapytanie (RODO). <span class="req">*</span></label>
        </div>
        <div id="agree-err" style="display:none;font-family:var(--ff-h);font-size:.58rem;letter-spacing:.14em;text-transform:uppercase;color:#f56060;margin-top:-.3rem">Zgoda jest wymagana</div>
        <div class="form-submit-wrap">
          <button class="form-submit" id="formBtn" type="button" onclick="submitForm()">
            <svg viewBox="0 0 24 24"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></svg>
            Wyślij zapytanie
          </button>
        </div>
      </div>
      <div class="form-success" id="formSuccess">
        <svg viewBox="0 0 24 24"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><polyline points="22 4 12 14.01 9 11.01"/></svg>
        <h3>Zapytanie wysłane!</h3>
        <p>Odezwiemy się w ciągu 2 godzin roboczych. Dziękujemy za zaufanie.</p>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <!-- ╔══════════════════════════════════════════════╗
       ║  LOGO STOPKA — wklej URL swojego logo      ║
       ║  Zmień src="" poniżej na adres ze Shopify  ║
       ╚══════════════════════════════════════════════╝ -->
  <div class="footer-logo">
    <img
      src="https://cdn.shopify.com/s/files/1/1044/5173/5882/files/Gemini_Generated_Image_yuei3wyuei3wyuei_18b18d9a-403c-4db8-b4d9-66856d8fd2a8.png?v=1779522368"
      alt="Logo firmy"
      id="footerLogoImg"
    />
  </div>
  <div class="footer-copy">© 2026 Reviva · Zblewo · Wszelkie prawa zastrzeżone</div>
  <div class="footer-social">
    <!-- Facebook -->
    <a href="https://www.facebook.com/profile.php?id=61590141381966" target="_blank" rel="noopener" title="Facebook">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
    </a>
    <!-- Instagram -->
    <a href="https://www.instagram.com/reviva_pomorskie/" target="_blank" rel="noopener" title="Instagram">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><rect x="2" y="2" width="20" height="20" rx="5" ry="5" fill="none" stroke="currentColor" stroke-width="2"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z" fill="none" stroke="currentColor" stroke-width="2"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5" stroke="currentColor" stroke-width="2" stroke-linecap="round"/></svg>
    </a>
    <!-- TikTok -->
    <a href="https://www.tiktok.com/@reviva_pomorskie" target="_blank" rel="noopener" title="TikTok">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 0 1-2.88 2.5 2.89 2.89 0 0 1-2.89-2.89 2.89 2.89 0 0 1 2.89-2.89c.28 0 .54.04.79.1V9.01a6.34 6.34 0 0 0-.79-.05 6.34 6.34 0 0 0-6.34 6.34 6.34 6.34 0 0 0 6.34 6.34 6.34 6.34 0 0 0 6.34-6.34V8.69a8.18 8.18 0 0 0 4.79 1.54V6.78a4.85 4.85 0 0 1-1.03-.09z"/></svg>
    </a>
    <!-- LinkedIn -->
    <a href="#" target="_blank" rel="noopener" title="LinkedIn">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
    </a>
    <!-- Google -->
    <a href="https://www.google.com/maps/place/Reviva/@53.9514268,18.287398,11.67z/data=!4m6!3m5!1s0xa1b06a1e0e89f5a9:0x6f689c85eaceddd7!8m2!3d53.9376484!4d18.3217305!16s%2Fg%2F11z7swtpfp?entry=ttu&g_ep=EgoyMDI2MDUyNy4wIKXMDSoASAFQAw%3D%3D" target="_blank" rel="noopener" title="Google">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z" fill="currentColor"/><path d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z" fill="currentColor"/><path d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z" fill="currentColor"/><path d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z" fill="currentColor"/></svg>
    </a>
  </div>
  <div class="footer-links">
    <a href="#hero">Start</a>
    <a href="#s-map">Zasięg</a>
    <a href="#s-contact">Kontakt</a>
  </div>
</footer>

<!-- ══════════════════════════════════════════════
     JAVASCRIPT
══════════════════════════════════════════════ -->
<script>
/* ── CURSOR ── */
if(window.matchMedia('(pointer:fine)').matches){
  const cur=document.getElementById('cursor'),cdot=document.getElementById('cursor-dot');
  let mx=0,my=0,cx=0,cy=0;
  document.addEventListener('mousemove',function(e){mx=e.clientX;my=e.clientY;cdot.style.left=mx+'px';cdot.style.top=my+'px'});
  (function loop(){cx+=(mx-cx)*.16;cy+=(my-cy)*.16;cur.style.left=cx+'px';cur.style.top=cy+'px';requestAnimationFrame(loop)})();
  document.querySelectorAll('a,button,.cib,.tchip,.gallery-card,.tcard').forEach(function(el2){
    el2.addEventListener('mouseenter',function(){cur.classList.add('big')});
    el2.addEventListener('mouseleave',function(){cur.classList.remove('big')});
  });
}

/* ── PROGRESS ── */
var progBar=document.getElementById('progress');
window.addEventListener('scroll',function(){
  var sc=document.documentElement.scrollTop,ht=document.documentElement.scrollHeight-window.innerHeight;
  progBar.style.width=(sc/ht*100)+'%';
},{passive:true});

/* ── NAV ── */
var navEl=document.getElementById('nav');
window.addEventListener('scroll',function(){navEl.classList.toggle('scrolled',window.scrollY>80)},{passive:true});
var burger=document.getElementById('burger'),drawer=document.getElementById('drawer');
burger.addEventListener('click',function(){burger.classList.toggle('open');drawer.classList.toggle('open')});
document.querySelectorAll('.drawer-link').forEach(function(a){a.addEventListener('click',function(){burger.classList.remove('open');drawer.classList.remove('open')})});

/* ── HERO CANVAS ── */
(function(){
  var hc=document.getElementById('hero-canvas');
  if(!hc)return;
  var ctx=hc.getContext('2d');
  var W,H,cols,rows;
  function resize(){W=hc.width=hc.offsetWidth;H=hc.height=hc.offsetHeight;cols=Math.ceil(W/64)+1;rows=Math.ceil(H/44)+1}
  resize();window.addEventListener('resize',resize,{passive:true});
  function draw(){
    ctx.clearRect(0,0,W,H);
    var t2=Date.now()*.0004;
    for(var rr=0;rr<rows;rr++)for(var cc=0;cc<cols;cc++){
      var x=cc*64+(rr%2)*32,y=rr*44;
      var b=.1+.05*Math.sin(t2+cc*.3+rr*.5);
      ctx.fillStyle='rgba(37,99,196,'+b+')';
      ctx.strokeStyle='rgba(168,200,248,.07)';ctx.lineWidth=.5;
      ctx.beginPath();ctx.rect(x+1,y+1,61,41);ctx.fill();ctx.stroke();
    }
    requestAnimationFrame(draw);
  }
  draw();
})();

/* ── HERO PARTICLES ── */
(function(){
  var pc=document.getElementById('hParticles');
  if(!pc)return;
  for(var pi=0;pi<22;pi++){
    var pp=document.createElement('div');pp.className='hprt';
    var ps=Math.random()*5+2;
    pp.style.cssText='width:'+ps+'px;height:'+ps+'px;left:'+Math.random()*100+'%;bottom:0;animation-duration:'+(Math.random()*9+7)+'s;animation-delay:'+Math.random()*10+'s';
    pc.appendChild(pp);
  }
})();


/* ── TESTIMONIALS ── */
(function(){
  var testimonials=[
    {q:'Podjazd wyglądał jak nowy po ich wizycie. Mech, który rósł przez lata — znikł w ciągu kilku godzin.',who:'Marek W.',loc:'Starogard Gdański'},
    {q:'Ekipa punktualna, sprzęt profesjonalny, efekt rewelacyjny. W cenie mieściła się też impregnacja.',who:'Anna K.',loc:'Zblewo'},
    {q:'Panowie idealnie dobrali ciśnienie do piaskowca — kamień wygląda jak za pierwszych lat.',who:'Tomasz R.',loc:'Skarszewy'},
    {q:'Szybki kontakt, szybki dojazd, świetny wynik. Koszt niższy niż u konkurencji, jakość dużo wyższa.',who:'Beata L.',loc:'Bobowo'},
    {q:'Kostka po 10 latach wyglądała okropnie — zielona od glonów. Wróciła jej oryginalna barwa!',who:'Piotr M.',loc:'Pelplin'},
  ];
  var track=document.getElementById('testiTrack');if(!track)return;
  var star='<svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2" fill="var(--gold)"/></svg>';
  var stars='<div class="tcard-stars">'+star.repeat(5)+'</div>';
  var all=testimonials.concat(testimonials);
  all.forEach(function(t){
    var cc=document.createElement('div');cc.className='tcard';
    cc.innerHTML=stars+'<div class="tcard-q">'+t.q+'</div><div class="tcard-who">'+t.who+'</div><div class="tcard-loc">'+t.loc+'</div>';
    track.appendChild(cc);
  });
})();


/* ── SCROLL REVEAL + GALLERY HINT ── */
(function(){
  var obs=new IntersectionObserver(function(entries){entries.forEach(function(e){if(e.isIntersecting)e.target.classList.add('vis')})},{threshold:.1});
  document.querySelectorAll('.reveal,.reveal-l,.reveal-r').forEach(function(el3){obs.observe(el3)});

  /* Gallery mobile — auto-show label of visible card */
  var galleryStripEl = document.getElementById('galleryStrip');
  if(galleryStripEl && window.innerWidth <= 900){
    galleryStripEl.addEventListener('scroll', function(){
      var cards = galleryStripEl.querySelectorAll('.gallery-card');
      var stripRect = galleryStripEl.getBoundingClientRect();
      var stripCenter = stripRect.left + stripRect.width/2;
      cards.forEach(function(card){
        var r = card.getBoundingClientRect();
        var cardCenter = r.left + r.width/2;
        var label = card.querySelector('.gallery-card-label');
        if(!label) return;
        if(Math.abs(cardCenter - stripCenter) < r.width * 0.6){
          label.style.transform = 'translateY(0)';
        } else {
          label.style.transform = 'translateY(100%)';
        }
      });
    }, {passive:true});
  }

  /* Gallery entrance hint — jednorazowe "szarpnięcie" kart gdy sekcja wchodzi w viewport */
  var gallerySection = document.getElementById('s-gallery');
  var galleryStrip   = document.getElementById('galleryStrip');
  var galleryHintEl  = document.getElementById('galleryHintEl');
  var hintPlayed = false;

  if(gallerySection && galleryStrip){
    var galleryObs = new IntersectionObserver(function(entries){
      if(entries[0].isIntersecting && !hintPlayed){
        hintPlayed = true;
        /* Opóźnienie żeby strona się załadowała wizualnie */
        setTimeout(function(){
          /* Animacja kart — każda lekko "skacze" po kolei */
          var cards = galleryStrip.querySelectorAll('.gallery-card');
          cards.forEach(function(card, i){
            setTimeout(function(){
              card.style.transition = 'transform .25s cubic-bezier(.4,0,.2,1)';
              card.style.transform  = (i%2===0 ? 'translateX(-14px)' : 'translateX(14px)') +
                                       (card.classList.contains('reveal') ? '' : '');
              setTimeout(function(){
                card.style.transform = '';
                setTimeout(function(){
                  card.style.transition = '';
                }, 280);
              }, 200);
            }, i * 80);
          });
          /* Pokaż wskaźnik "przesuń" na mobile */
          if(galleryHintEl){
            galleryHintEl.style.opacity = '1';
            setTimeout(function(){ galleryHintEl.style.opacity = '0'; }, 2800);
          }
        }, 400);
        galleryObs.disconnect();
      }
    }, {threshold: 0.25});
    galleryObs.observe(gallerySection);
  }
})();


/* ── COPY TO CLIPBOARD ── */
window.copyToClipboard = function(text, label){
  navigator.clipboard.writeText(text).then(function(){
    var feedbackId = text.includes('@') ? 'emailCopied' : 'telCopied';
    var el = document.getElementById(feedbackId);
    if(el){ el.style.opacity='1'; setTimeout(function(){ el.style.opacity='0'; }, 2200); }
  }).catch(function(){
    var ta = document.createElement('textarea');
    ta.value = text; ta.style.position='fixed'; ta.style.opacity='0';
    document.body.appendChild(ta); ta.select();
    document.execCommand('copy'); document.body.removeChild(ta);
    var feedbackId = text.includes('@') ? 'emailCopied' : 'telCopied';
    var el = document.getElementById(feedbackId);
    if(el){ el.style.opacity='1'; setTimeout(function(){ el.style.opacity='0'; }, 2200); }
  });
};


/* ── GALLERY URL SETTER (Shopify) ── */
/* ── GALLERY — zdjęcia ustawiane w kodzie HTML (src="...") ── */


/* ── FORM VALIDATION + FORMSPREE ── */
function validateField(id,testFn,errMsg){
  var fg=document.getElementById('fg-'+id);
  var inp=document.getElementById('f-'+id);
  if(!fg||!inp)return true;
  var ok=testFn(inp.value.trim());
  fg.classList.toggle('invalid',!ok);fg.classList.toggle('valid',ok);
  var em=fg.querySelector('.err-msg');if(em)em.textContent=errMsg;
  return ok;
}
window.submitForm=function(){
  var okName =validateField('name', function(v){return v.length>=2},'Proszę podać imię i nazwisko');
  var okPhone=validateField('phone',function(v){return /[\d\s\+\-]{7,}/.test(v)},'Podaj poprawny numer telefonu');
  var okEmail=validateField('email',function(v){return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(v)},'Podaj poprawny adres e-mail');
  var agree=document.getElementById('f-agree');
  var agreeErr=document.getElementById('agree-err');
  var okAgree=agree&&agree.checked;
  if(agreeErr)agreeErr.style.display=okAgree?'none':'block';
  if(!okName||!okPhone||!okEmail||!okAgree)return;
  var btn=document.getElementById('formBtn');
  btn.textContent='Wysyłanie…';btn.disabled=true;
  fetch('https://formspree.io/f/xkoeoyoa',{
    method:'POST',
    headers:{'Content-Type':'application/json','Accept':'application/json'},
    body:JSON.stringify({
      name:   document.getElementById('f-name').value.trim(),
      phone:  document.getElementById('f-phone').value.trim(),
      email:  document.getElementById('f-email').value.trim(),
      city:   document.getElementById('f-city').value.trim(),
      service:document.getElementById('f-service').value,
      message:document.getElementById('f-msg').value.trim(),
    })
  }).then(function(res){
    if(res.ok){
      document.getElementById('formBody').style.display='none';
      document.getElementById('formSuccess').classList.add('show');
    }else{btn.textContent='Błąd — spróbuj ponownie';btn.disabled=false}
  }).catch(function(){btn.textContent='Błąd sieci — spróbuj ponownie';btn.disabled=false});
};
['name','phone','email'].forEach(function(id){
  var inp2=document.getElementById('f-'+id);
  if(inp2)inp2.addEventListener('blur',function(){
    if(id==='name') validateField('name', function(v){return v.length>=2},'Proszę podać imię i nazwisko');
    if(id==='phone')validateField('phone',function(v){return /[\d\s\+\-]{7,}/.test(v)},'Podaj poprawny numer telefonu');
    if(id==='email')validateField('email',function(v){return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(v)},'Podaj poprawny adres e-mail');
  });
});

/* ── PAVE ANIMATION — repeating every 8s ── */
(function(){
  var grid = document.getElementById('paveGrid');
  if(!grid) return;
  var dirty = ['#1e2e14','#243418','#182a10','#1c3016','#284022'];
  var clean = ['#c8c0b4','#d0c8bc','#beb6aa','#ccc4b8','#c4bcb0'];
  for(var i=0;i<35;i++){
    var t=document.createElement('div');t.className='pave-tile';
    t.style.background=dirty[i%dirty.length];
    t.dataset.clean=clean[i%clean.length];
    t.dataset.dirty=dirty[i%dirty.length];
    grid.appendChild(t);
  }
  function runClean(){
    var tiles=grid.querySelectorAll('.pave-tile');
    document.getElementById('paveVisual').classList.add('cleaning');
    tiles.forEach(function(tt,i){setTimeout(function(){tt.style.background=tt.dataset.clean},i*55)});
    setTimeout(function(){
      document.getElementById('paveVisual').classList.remove('cleaning');
      // After pause, go dirty again then repeat
      setTimeout(function(){
        tiles.forEach(function(tt,i){setTimeout(function(){tt.style.background=tt.dataset.dirty},i*30)});
        setTimeout(runClean, 35*30+1500);
      }, 2000);
    }, 35*55+400);
  }
  // Start when visible
  var started=false;
  new IntersectionObserver(function(entries){
    if(entries[0].isIntersecting&&!started){started=true;runClean();}
  },{threshold:.3}).observe(grid);
})();


/* ── PROCESS SCROLLYTELLING ── */
(function(){
  window._bwg=function(el,c2,r2,tw2,th2){buildWeedGrid(el,c2||5,r2||4,tw2||62,th2||46);};
function buildWeedGrid(el,cols,rows,tw,th){
    if(!el)return;
    /* Na mobile zmniejsz kafelki */
    var isMob = window.innerWidth <= 900;
    if(isMob){ tw = Math.min(tw, Math.floor((window.innerWidth*0.85)/cols - 6)); th = Math.floor(tw/1.45); }
    el.style.gridTemplateColumns='repeat('+cols+',1fr)';
    var dc=['#1e2e14','#243418','#182a10','#1c3016','#284022'];
    for(var i=0;i<cols*rows;i++){
      var t=document.createElement('div');
      t.style.cssText='width:'+tw+'px;height:'+th+'px;border-radius:3px;background:'+dc[i%dc.length]+';position:relative;overflow:hidden;flex-shrink:0';
      if(Math.random()>.45){
        var wh=Math.random()*13+6;
        var w1=document.createElement('div');w1.className='weed';
        w1.style.cssText='height:'+wh+'px;left:'+(18+Math.random()*55)+'%;animation-delay:'+Math.random()*2+'s';
        t.appendChild(w1);
        if(Math.random()>.5){var w2=document.createElement('div');w2.className='weed';w2.style.cssText='height:'+(wh*.65)+'px;left:'+(38+Math.random()*35)+'%;animation-delay:'+Math.random()*2+'s;background:linear-gradient(#3d7a22,#5aaa32)';t.appendChild(w2);}
      }
      el.appendChild(t);
    }
  }
  window._bsp=buildSplashes;
function buildSplashes(el){
    if(!el)return;
    el.style.cssText='position:absolute;top:60px;left:0;right:0;height:110px;pointer-events:none';
    for(var p=0;p<14;p++){
      var sp=document.createElement('div');sp.className='s1-splash';
      var sx=(Math.random()-.5)*65,sy=Math.random()*32+14;
      sp.style.cssText='width:'+(Math.random()*4+2)+'px;height:'+(Math.random()*4+2)+'px;--sx:'+sx+'px;--sy:'+sy+'px;left:'+(25+Math.random()*50)+'%;top:'+(Math.random()*55)+'px;animation-duration:'+(Math.random()*.5+.3)+'s;animation-delay:'+Math.random()*1.8+'s';
      el.appendChild(sp);
    }
  }
  window._bbr=buildBrush;
function buildBrush(el,sz){
    if(!el)return;
    if(sz){el.style.width=sz;el.style.height=sz;}
    for(var b=0;b<8;b++){var br=document.createElement('div');br.className='s2-bristle';br.style.transform='rotate('+(b*45)+'deg)';el.appendChild(br);}
  }
  window._bfm=buildFoam;
function buildFoam(el){
    if(!el)return;
    el.style.cssText='position:absolute;top:60px;left:0;right:0;height:125px;pointer-events:none';
    for(var f=0;f<12;f++){
      var fm=document.createElement('div');fm.className='s2-foam';
      var fw=Math.random()*10+4,fx=(Math.random()-.5)*50,fy=-(Math.random()*36+14);
      fm.style.cssText='width:'+fw+'px;height:'+fw+'px;--fx:'+fx+'px;--fy:'+fy+'px;left:'+(20+Math.random()*60)+'%;top:'+(Math.random()*70+15)+'px;animation-duration:'+(Math.random()*.8+.5)+'s;animation-delay:'+Math.random()*2+'s';
      el.appendChild(fm);
    }
  }
  window._bgr=buildGrains;
function buildGrains(el,topPx){
    if(!el)return;
    /* Grains fly horizontally from gun barrel, fan out on impact */
    el.style.cssText='position:absolute;top:50%;left:110px;transform:translateY(-50%);width:220px;height:80px;pointer-events:none;animation:gunOsc 2s ease-in-out infinite';
    for(var g=0;g<28;g++){
      var gr=document.createElement('div');gr.className='s4-grain';
      var dist=Math.random()*160+40;
      var spread=(Math.random()-.5)*60;
      var gs=Math.random()*2.5+1;
      gr.style.cssText='width:'+gs+'px;height:'+gs+'px;background:rgba('
        +(185+Math.floor(Math.random()*40))+','
        +(155+Math.floor(Math.random()*35))+','
        +(65+Math.floor(Math.random()*30))+','
        +(Math.random()*.5+.4)+');'
        +'--gx:'+dist+'px;--gy:'+spread+'px;'
        +'left:'+(Math.random()*20)+'%;top:'+(30+Math.random()*40)+'%;'
        +'animation-duration:'+(Math.random()*.5+.25)+'s;'
        +'animation-delay:'+Math.random()*1.2+'s';
      el.appendChild(gr);
    }
  }
  window._bjt=buildJets;
function buildJets(el){
    if(!el)return;
    var angles=[-18,-10,-4,0,4,10,18];
    angles.forEach(function(a){
      var jl=document.createElement('div');jl.className='s4-jet-line';
      var len=Math.random()*40+120;
      jl.style.cssText='width:'+len+'px;transform-origin:left center;transform:rotate('+a+'deg);top:calc(50% - 1.5px);left:0;opacity:'+(0.9-Math.abs(a)/30)+';animation:gunOsc 2s ease-in-out infinite';
      el.appendChild(jl);
    });
  }
  window._bic=buildImpactCloud;
function buildImpactCloud(el){
    if(!el)return;
    for(var i=0;i<6;i++){
      var d=document.createElement('div');d.className='s4-dust-puff';
      var sz=Math.random()*30+15;
      var px=(Math.random()-.5)*50,py=(Math.random()-.5)*50;
      d.style.cssText='width:'+sz+'px;height:'+sz+'px;--px:'+px+'px;--py:'+py+'px;left:'+(Math.random()*30-15)+'px;top:'+(Math.random()*30-15)+'px;animation-duration:'+(Math.random()*.6+.5)+'s;animation-delay:'+Math.random()*1+'s';
      el.appendChild(d);
      /* sparks */
      var sp=document.createElement('div');sp.className='s4-spark';
      var sx=(Math.random()-.5)*40,sy=(Math.random()-.5)*40;
      sp.style.cssText='--sx:'+sx+'px;--sy:'+sy+'px;left:0;top:0;animation-duration:'+(Math.random()*.3+.2)+'s;animation-delay:'+Math.random()*.8+'s';
      el.appendChild(sp);
    }
  }

  /* Desktop scenes */
  var g0=document.getElementById('scene0grid');
  if(g0){g0.style.cssText=(g0.style.cssText||'')+';display:grid;grid-template-columns:repeat(5,1fr);gap:7px';buildWeedGrid(g0,5,4,62,46);}
  buildSplashes(document.getElementById('s1splashes'));
  buildBrush(document.getElementById('s2brush'),'70px');
  buildFoam(document.getElementById('s2foams'));
  var ct=document.getElementById('cleanTiles');
  if(ct){for(var ti=0;ti<5;ti++){var ts=document.createElement('div');ts.className='cts';ct.appendChild(ts);}}
  buildGrains(document.getElementById('s4grains'));
  buildJets(document.getElementById('s4jets'));
  buildImpactCloud(document.getElementById('s4cloud'));

  /* Mobile scenes */
  var mg=document.getElementById('mob-grid-0');
  if(mg){mg.style.cssText=(mg.style.cssText||'')+';display:grid;grid-template-columns:repeat(5,1fr);gap:4px';buildWeedGrid(mg,5,3,44,32);}
  buildSplashes(document.getElementById('mob-s1sp'));
  buildBrush(document.getElementById('mob-brush'),'55px');
  buildFoam(document.getElementById('mob-s2foam'));
  buildGrains(document.getElementById('mob-s4gr'),105);

  /* Scroll-driven step switching — desktop only */
  var outer=document.getElementById('processOuter');
  var psteps=document.querySelectorAll('.pstep');
  var scenes=document.querySelectorAll('.pscene');
  var dots=document.querySelectorAll('.sdot');
  var stepFillEl=document.getElementById('stepFill');
  var currentStep=0;
  var totalSteps=5;

  function setStep(idx){
    if(idx===currentStep)return;
    currentStep=idx;
    psteps.forEach(function(s,i){s.classList.toggle('active',i===idx)});
    scenes.forEach(function(s,i){s.classList.toggle('active',i===idx)});
    dots.forEach(function(d,i){d.classList.toggle('active',i===idx)});
    if(stepFillEl)stepFillEl.style.height=((idx/(totalSteps-1))*100)+'%';
  }

  if(outer && window.innerWidth>900){
    window.addEventListener('scroll',function(){
      var rect=outer.getBoundingClientRect();
      var total=outer.offsetHeight-window.innerHeight;
      var scrolled=Math.max(0,-rect.top);
      setStep(Math.min(totalSteps-1,Math.floor(Math.min(.9999,scrolled/total)*totalSteps)));
    },{passive:true});
  }

  dots.forEach(function(d,i){
    d.addEventListener('click',function(){
      if(!outer||window.innerWidth<=900)return;
      window.scrollTo({top:outer.offsetTop+(i/(totalSteps-1))*(outer.offsetHeight-window.innerHeight),behavior:'smooth'});
    });
  });
})();


/* ── MOBILE PROCESS — STICKY SCROLLYTELLING ── */
(function(){
  if(window.innerWidth > 900) return;

  var stepData = [
    {num:'01',title:'Usuwanie chwastów',    desc:'Mechaniczne i chemiczne usunięcie mchu, chwastów i glonów ze spoin i nawierzchni.'},
    {num:'02',title:'Płukanie ciśnieniowe', desc:'Strumień pod wysokim ciśnieniem zrywa zabrudzenia i wypłukuje pozostałości biologiczne.'},
    {num:'03',title:'Szorowanie',           desc:'Rotacyjne szczotki docierają do spoin i usuwają uparty brud, tłuszcz i przebarwienia.'},
    {num:'04',title:'Impregnacja',          desc:'Powłoka ochronna blokuje wilgoć i biologię. Opcja płatna — wycena indywidualna.'},
    {num:'05',title:'Piaskowanie — gratis', desc:'Precyzyjne piaskowanie usuwa głębokie przebarwienia. Gratis w ramach usług!'},
  ];

  var outer    = document.getElementById('processOuter');
  var numEl    = document.getElementById('mobStepNum');
  var titleEl  = document.getElementById('mobStepTitle');
  var descEl   = document.getElementById('mobStepDesc');
  var progEl   = document.getElementById('mobStepProgress');
  var dotsEl   = document.getElementById('mobStepDots');
  var scenes   = document.querySelectorAll('.pscene');
  var psteps   = document.querySelectorAll('.pstep');
  var sdots    = document.querySelectorAll('.sdot');
  var stepFill = document.getElementById('stepFill');

  if(!outer || !numEl) return;

  var curMob = -1;

  function setMobStep(idx){
    if(idx === curMob) return;
    curMob = idx;
    var d = stepData[idx];
    if(numEl)   numEl.textContent   = 'Etap '+d.num+' / 05';
    if(titleEl) titleEl.textContent = d.title;
    if(descEl)  descEl.textContent  = d.desc;
    if(progEl)  progEl.style.width  = ((idx+1)/5*100)+'%';
    if(dotsEl){
      var ds = dotsEl.querySelectorAll('.mob-step-overlay-dot');
      ds.forEach(function(dot,i){ dot.classList.toggle('active', i===idx); });
    }
    scenes.forEach(function(s,i){ s.classList.toggle('active', i===idx); });
    psteps.forEach(function(s,i){ s.classList.toggle('active', i===idx); });
    sdots.forEach(function(d2,i){ d2.classList.toggle('active', i===idx); });
    if(stepFill) stepFill.style.height = ((idx/4)*100)+'%';
    /* Lazy init scene animations — funkcje dostępne z window po process IIFE */
    if(idx===0 && !window._ms0){window._ms0=1;
      var g=document.getElementById('scene0grid');
      if(g&&g.children.length===0 && window._bwg){window._bwg(g,5,4);}
    }
    if(idx===1 && !window._ms1){window._ms1=1; if(window._bsp)window._bsp(document.getElementById('s1splashes'));}
    if(idx===2 && !window._ms2){window._ms2=1; if(window._bbr){window._bbr(document.getElementById('s2brush'),'70px'); window._bfm(document.getElementById('s2foams'));}}
    if(idx===4 && !window._ms4){window._ms4=1; if(window._bgr){window._bgr(document.getElementById('s4grains')); window._bjt(document.getElementById('s4jets')); window._bic(document.getElementById('s4cloud'));}}
  }

  function onScrollMob(){
    if(!outer) return;
    var rect  = outer.getBoundingClientRect();
    var total = outer.offsetHeight - window.innerHeight;
    var scrolled = Math.max(0, -rect.top);
    setStep(Math.min(4, Math.floor(Math.min(.9999, scrolled/total)*5)));
  }
  function setStep(i){ setMobStep(i); }

  window.addEventListener('scroll', onScrollMob, {passive:true});
  setTimeout(function(){ setMobStep(0); }, 150);
})();

/* ── GALLERY MOBILE BOUNCE ENTRY ── */



</script>
</body>
</html>
