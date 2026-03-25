<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ENNA HRNJIC — Portfolio BTS SIO</title>
<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Rajdhani:wght@400;600;700&family=Nunito:wght@400;600;700&family=Share+Tech+Mono&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#0b0b2a;--panel:#13133a;--panel2:#191950;
  --vio:#8b5cf6;--vio2:#a78bfa;
  --cyan:#06b6d4;--cyan2:#22d3ee;
  --pink:#ec4899;--pink2:#f472b6;
  --green:#10b981;--green2:#34d399;
  --yellow:#f59e0b;
  --muted:rgba(200,200,255,0.5);
  --bv:rgba(139,92,246,0.35);
}
*{margin:0;padding:0;box-sizing:border-box;cursor:none !important;}
html{scroll-behavior:smooth;}
body{font-family:'Nunito',sans-serif;background:var(--bg);color:#f0f0ff;min-height:100vh;overflow-x:hidden;}
body::before{content:'';position:fixed;inset:0;z-index:0;pointer-events:none;
  background:radial-gradient(ellipse 80% 60% at 15% 0%,rgba(139,92,246,0.18),transparent 60%),
             radial-gradient(ellipse 60% 50% at 85% 100%,rgba(6,182,212,0.14),transparent 55%);}
body::after{content:'';position:fixed;inset:0;z-index:0;pointer-events:none;
  background-image:linear-gradient(rgba(139,92,246,0.05) 1px,transparent 1px),
                   linear-gradient(90deg,rgba(139,92,246,0.05) 1px,transparent 1px);
  background-size:50px 50px;}

/* ICONES FLOTTANTES */
.fi{position:fixed;pointer-events:none;z-index:0;opacity:0;animation:fup linear infinite;user-select:none;
    filter:drop-shadow(0 0 5px rgba(139,92,246,0.5));}
@keyframes fup{
  0%  {transform:translateY(105vh) rotate(0deg);opacity:0;}
  8%  {opacity:0.13;}
  88% {opacity:0.13;}
  100%{transform:translateY(-10vh)  rotate(360deg);opacity:0;}
}

/* CURSEUR */
#cur{position:fixed;pointer-events:none;z-index:9999;top:0;left:0;opacity:0;}
#cur svg{filter:drop-shadow(0 0 6px rgba(167,139,250,0.9));}
@keyframes adrop{
  0%  {opacity:0;transform:translateY(-8px) scale(0.7);}
  40% {opacity:1;transform:translateY(4px)  scale(1.1);}
  70% {transform:translateY(-2px) scale(1);}
  100%{opacity:0;transform:translateY(6px)  scale(0.9);}
}

/* LAYOUT */
.wrap{position:relative;z-index:1;max-width:1340px;margin:0 auto;}

/* HEADER */
header{padding:5rem 2rem 3.5rem;display:flex;flex-direction:column;align-items:center;text-align:center;width:100%;}

.badge{display:inline-flex;align-items:center;gap:.5rem;font-family:'Share Tech Mono',monospace;
  font-size:.62rem;letter-spacing:.18em;color:var(--green2);
  background:rgba(16,185,129,.06);border:1px solid rgba(52,211,153,.2);
  padding:.35rem 1rem;border-radius:3px;margin-bottom:1.8rem;opacity:.85;}
.badge .dot{width:7px;height:7px;border-radius:50%;background:var(--green2);
  box-shadow:0 0 8px var(--green2);animation:bp 1.5s ease infinite;flex-shrink:0;}
@keyframes bp{0%,100%{opacity:1;transform:scale(1);}50%{opacity:.4;transform:scale(.6);}}

.hn1{display:block;font-family:'Press Start 2P',cursive;
  font-size:clamp(1.6rem,5vw,4rem);line-height:1.2;letter-spacing:.04em;
  color:#fff;-webkit-text-stroke:3px #7c3aed;margin-bottom:1.4rem;
  text-shadow:2px 2px 0 #7c3aed,4px 4px 0 #6d28d9,6px 6px 0 #5b21b6,8px 8px 0 #4c1d95,
    0 0 25px rgba(167,139,250,1),0 0 50px rgba(139,92,246,.7),0 0 90px rgba(124,58,237,.4);}

.hn2{display:block;font-family:'Press Start 2P',cursive;
  font-size:clamp(.75rem,2vw,1.1rem);letter-spacing:.1em;
  color:#fff;-webkit-text-stroke:1px #0e7490;margin-bottom:2rem;line-height:1.8;
  text-shadow:1px 1px 0 #0e7490,2px 2px 0 #164e63,
    0 0 15px rgba(34,211,238,1),0 0 30px rgba(6,182,212,.6);}

.chips{display:flex;flex-wrap:wrap;gap:.8rem;justify-content:center;}
.chip{font-family:'Rajdhani',sans-serif;font-size:.9rem;font-weight:600;letter-spacing:.08em;padding:.4rem 1.2rem;border-radius:4px;}
.chv{background:rgba(139,92,246,.12);border:1px solid rgba(139,92,246,.4);color:var(--vio2);}
.chc{background:rgba(6,182,212,.1);border:1px solid rgba(6,182,212,.35);color:var(--cyan2);}
.chp{background:rgba(236,72,153,.1);border:1px solid rgba(236,72,153,.3);color:var(--pink2);}

/* NAV */
nav{position:sticky;top:0;z-index:100;background:rgba(11,11,42,.93);backdrop-filter:blur(20px);border-bottom:1px solid var(--bv);}
nav::after{content:'';display:block;height:1px;background:linear-gradient(90deg,transparent,var(--vio),var(--cyan2),var(--vio),transparent);box-shadow:0 0 10px var(--vio);}
.ni{display:flex;flex-wrap:wrap;justify-content:center;}
.nb{font-family:'Rajdhani',sans-serif;font-size:.82rem;font-weight:600;letter-spacing:.12em;text-transform:uppercase;
  padding:1rem 1.3rem;background:transparent;border:none;color:var(--muted);
  position:relative;transition:color .3s;display:flex;align-items:center;gap:.3rem;}
.na{color:var(--cyan2);font-size:.65rem;opacity:0;transition:opacity .3s,transform .3s;}
.nb:hover .na,.nb.on .na{opacity:1;transform:translateX(2px);}
.nb::after{content:'';position:absolute;bottom:0;left:50%;right:50%;height:2px;
  background:linear-gradient(90deg,var(--vio),var(--cyan2));
  box-shadow:0 0 8px var(--vio);transition:left .3s,right .3s;}
.nb:hover,.nb.on{color:#fff;}
.nb:hover::after,.nb.on::after{left:0;right:0;}
.nb.on{color:var(--cyan2);}

/* CONTENT */
.content{padding:4rem 2rem 6rem;}
.pane{display:none;animation:fin .4s ease;}
.pane.on{display:block;}
@keyframes fin{from{opacity:0;transform:translateY(12px);}to{opacity:1;transform:none;}}

/* SECTION TITLE */
.sh{margin-bottom:3rem;}
.sht{font-family:'Share Tech Mono',monospace;font-size:.7rem;color:var(--cyan2);letter-spacing:.2em;text-transform:uppercase;margin-bottom:.4rem;opacity:.7;}
.shh{font-family:'Rajdhani',sans-serif;font-size:clamp(2rem,4vw,3rem);font-weight:700;color:#fff;letter-spacing:.04em;}
.shh em{font-style:normal;color:var(--cyan2);text-shadow:0 0 20px rgba(34,211,238,.6);}
.shl{height:2px;margin-top:.8rem;background:linear-gradient(90deg,var(--vio),var(--cyan2),transparent);box-shadow:0 0 8px var(--vio);border-radius:1px;}

/* CARD */
.card{background:var(--panel);border:1px solid var(--bv);border-radius:10px;padding:2.5rem;
  position:relative;overflow:hidden;transition:transform .3s,box-shadow .3s,border-color .3s;}
.card::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,var(--vio),var(--cyan2),transparent);opacity:.6;}
.card:hover{transform:translateY(-4px);border-color:rgba(139,92,246,.55);box-shadow:0 16px 40px rgba(0,0,0,.5);}
.cv{border-color:rgba(139,92,246,.4);}

/* ACCUEIL */
.about{font-size:1.05rem;line-height:1.9;color:rgba(240,240,255,.85);max-width:720px;margin:0 auto;text-align:center;}
.about strong{color:var(--vio2);}
.sgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:1.2rem;margin-top:2rem;}
.sb{background:var(--panel2);border:1px solid var(--bv);border-radius:8px;padding:1.7rem;text-align:center;
  position:relative;overflow:hidden;transition:all .3s;}
.sb::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;
  background:linear-gradient(90deg,var(--vio),var(--cyan2));opacity:0;transition:opacity .3s;}
.sb:hover{border-color:rgba(139,92,246,.5);transform:translateY(-4px);}
.sb:hover::before{opacity:1;}
.sbi{font-size:2rem;margin-bottom:.8rem;}
.sbl{font-family:'Share Tech Mono',monospace;font-size:.62rem;color:var(--cyan2);letter-spacing:.18em;text-transform:uppercase;margin-bottom:.4rem;}
.sbv{font-family:'Rajdhani',sans-serif;font-size:1rem;font-weight:600;color:#fff;}

/* PARCOURS */
.tl{position:relative;padding-left:2.8rem;}
.tl::before{content:'';position:absolute;left:0;top:0;bottom:0;width:2px;
  background:linear-gradient(180deg,var(--vio),var(--cyan2),transparent);box-shadow:0 0 12px var(--vio);}
.tli{position:relative;margin-bottom:2rem;}
.tld{position:absolute;left:-3.15rem;top:1.8rem;width:14px;height:14px;border-radius:50%;
  background:var(--vio);border:2px solid var(--bg);
  box-shadow:0 0 0 3px rgba(139,92,246,.25),0 0 16px var(--vio);}
.tld.now{background:var(--cyan2);box-shadow:0 0 0 3px rgba(34,211,238,.25),0 0 16px var(--cyan2);}
.tlc{background:var(--panel);border:1px solid var(--bv);border-radius:8px;padding:2rem;
  position:relative;overflow:hidden;transition:all .3s;}
.tlc::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,rgba(139,92,246,.5),transparent);}
.tlc:hover{border-color:rgba(139,92,246,.5);transform:translateX(5px);}
.tcb{font-family:'Share Tech Mono',monospace;font-size:.68rem;letter-spacing:.1em;padding:.3rem .9rem;
  border-radius:3px;display:inline-block;margin-bottom:.8rem;}
.bp{background:rgba(236,72,153,.08);border:1px solid rgba(236,72,153,.25);color:var(--pink2);}
.bn{background:rgba(16,185,129,.08);border:1px solid rgba(16,185,129,.25);color:var(--green2);}
.tcs{font-family:'Rajdhani',sans-serif;font-size:1.2rem;font-weight:700;color:#fff;margin-bottom:.2rem;}
.tcd{font-size:.88rem;color:var(--cyan2);font-weight:600;margin-bottom:.8rem;}
.tct{font-size:.95rem;color:rgba(200,200,255,.75);line-height:1.75;}

/* PROJETS */
.pgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(270px,1fr));gap:1.5rem;}
.pc{background:var(--panel);border:1px solid var(--bv);border-radius:10px;padding:2rem;
  position:relative;overflow:hidden;transition:all .4s;}
.pc::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,var(--vio),var(--cyan2),transparent);}
.pc::after{content:'';position:absolute;top:12px;right:12px;width:14px;height:14px;
  border-top:2px solid var(--cyan2);border-right:2px solid var(--cyan2);opacity:.3;transition:opacity .3s;}
.pc:hover::after{opacity:1;}
.pc:hover{border-color:rgba(139,92,246,.6);transform:translateY(-7px);box-shadow:0 20px 45px rgba(0,0,0,.5);}
.pnum{font-family:'Rajdhani',sans-serif;font-size:3rem;font-weight:700;color:rgba(139,92,246,.07);
  position:absolute;top:.5rem;right:1rem;line-height:1;}
.pico{width:52px;height:52px;border-radius:10px;display:flex;align-items:center;justify-content:center;
  font-size:1.5rem;background:linear-gradient(135deg,rgba(139,92,246,.18),rgba(6,182,212,.12));
  border:1px solid rgba(139,92,246,.3);margin-bottom:1.2rem;}
.pc h3{font-family:'Rajdhani',sans-serif;font-size:1.15rem;font-weight:700;color:#fff;margin-bottom:.4rem;letter-spacing:.04em;}
.pc > p{font-size:.9rem;color:var(--muted);line-height:1.6;}
.parr{position:absolute;bottom:1.5rem;right:1.5rem;width:30px;height:30px;border-radius:50%;
  background:rgba(139,92,246,.1);border:1px solid rgba(139,92,246,.3);
  display:flex;align-items:center;justify-content:center;font-size:.85rem;color:var(--vio2);transition:all .3s;}
.pc:hover .parr{background:rgba(139,92,246,.3);transform:rotate(45deg);}

/* CERTIFICATIONS */
.cgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:1.5rem;}
.ccard{background:var(--panel);border:1px solid var(--bv);border-radius:10px;padding:2rem;
  text-align:center;position:relative;overflow:hidden;transition:all .4s;}
.ccard::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,var(--vio),var(--cyan2),transparent);}
.ccard:hover{border-color:rgba(139,92,246,.6);transform:translateY(-5px);box-shadow:0 16px 40px rgba(0,0,0,.5);}
.cico{width:64px;height:64px;border-radius:14px;margin:0 auto 1.2rem;display:flex;align-items:center;justify-content:center;
  font-size:2rem;background:linear-gradient(135deg,rgba(139,92,246,.2),rgba(6,182,212,.12));
  border:1px solid rgba(139,92,246,.3);transition:all .3s;}
.ccard:hover .cico{box-shadow:0 0 25px rgba(139,92,246,.3);border-color:rgba(139,92,246,.6);}
.ccard h3{font-family:'Rajdhani',sans-serif;font-size:1rem;font-weight:700;color:#fff;margin-bottom:.3rem;}
.ciss{font-size:.82rem;color:var(--vio2);margin-bottom:1rem;font-weight:600;}
.cst{font-family:'Share Tech Mono',monospace;font-size:.65rem;font-weight:700;letter-spacing:.12em;
  text-transform:uppercase;padding:.35rem 1rem;border-radius:3px;display:inline-block;}
.cok{background:rgba(16,185,129,.08);border:1px solid rgba(16,185,129,.3);color:var(--green2);}
.cpr{background:rgba(245,158,11,.08);border:1px solid rgba(245,158,11,.3);color:var(--yellow);}

/* INFRA */
.itxt{font-size:1rem;color:rgba(200,200,255,.85);line-height:1.85;}
.itxt strong{color:var(--vio2);}
.ttags{display:flex;flex-wrap:wrap;gap:.7rem;margin-top:1.5rem;}
.tt{font-family:'Rajdhani',sans-serif;font-size:.85rem;font-weight:600;letter-spacing:.08em;padding:.35rem 1rem;border-radius:4px;}
.ttv{background:rgba(139,92,246,.1);border:1px solid rgba(139,92,246,.3);color:var(--vio2);}
.ttc{background:rgba(6,182,212,.08);border:1px solid rgba(6,182,212,.25);color:var(--cyan2);}
.diag{background:rgba(0,0,0,.4);border:1px solid rgba(139,92,246,.3);border-radius:10px;
  padding:2rem;margin:2rem 0;position:relative;overflow:hidden;}
.diag::before{content:'';position:absolute;inset:0;
  background-image:linear-gradient(rgba(139,92,246,.03) 1px,transparent 1px),
                   linear-gradient(90deg,rgba(139,92,246,.03) 1px,transparent 1px);
  background-size:28px 28px;pointer-events:none;}
.dh{font-family:'Share Tech Mono',monospace;font-size:.65rem;color:var(--cyan2);letter-spacing:.2em;
  margin-bottom:1.5rem;display:flex;align-items:center;gap:.8rem;}
.dh::before{content:'// ';}
.dh::after{content:'';flex:1;height:1px;background:linear-gradient(90deg,rgba(34,211,238,.4),transparent);}

/* TOOLTIP */
#ntt{position:fixed;background:rgba(11,11,42,.97);border:1px solid rgba(139,92,246,.5);border-radius:8px;
  padding:1rem 1.2rem;font-family:'Nunito',sans-serif;font-size:.82rem;color:#fff;
  pointer-events:none;z-index:500;display:none;max-width:250px;box-shadow:0 0 25px rgba(139,92,246,.3);}
#ntt.on{display:block;}
#ntt h4{font-family:'Rajdhani',sans-serif;color:var(--cyan2);font-size:1rem;font-weight:700;margin-bottom:.3rem;}
.tip-i{color:var(--green2);font-family:'Share Tech Mono',monospace;font-size:.75rem;margin-bottom:.2rem;}
.tip-r{color:var(--vio2);font-size:.8rem;font-weight:600;margin-bottom:.3rem;}
.tip-d{color:rgba(200,200,255,.65);font-size:.78rem;line-height:1.5;}

/* SERVEURS */
.srvgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:1.3rem;margin-top:2rem;}
.srv{background:var(--panel);border-radius:10px;padding:1.8rem;position:relative;
  overflow:hidden;transition:all .4s;animation:svin .5s ease forwards;opacity:0;}
@keyframes svin{from{opacity:0;transform:translateY(12px);}to{opacity:1;transform:none;}}
.srv::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,var(--vio),transparent);opacity:.5;}
.srv:hover{transform:translateY(-4px);}
.srv:nth-child(1){animation-delay:.05s}.srv:nth-child(2){animation-delay:.1s}
.srv:nth-child(3){animation-delay:.15s}.srv:nth-child(4){animation-delay:.2s}
.srv:nth-child(5){animation-delay:.25s}.srv:nth-child(6){animation-delay:.3s}
.srv:nth-child(7){animation-delay:.35s}.srv:nth-child(8){animation-delay:.4s}
.srv:nth-child(9){animation-delay:.45s}
.srv.sv{border:1px solid rgba(139,92,246,.35);}.srv.sv:hover{border-color:rgba(139,92,246,.65);}
.srv.sc{border:1px solid rgba(6,182,212,.3);}.srv.sc:hover{border-color:rgba(6,182,212,.6);}
.srv.sp{border:1px solid rgba(236,72,153,.25);}.srv.sp:hover{border-color:rgba(236,72,153,.55);}
.srv.sg{border:1px solid rgba(16,185,129,.25);}.srv.sg:hover{border-color:rgba(16,185,129,.55);}
.srh{display:flex;align-items:center;gap:.9rem;margin-bottom:.8rem;}
.sri{font-size:1.8rem;}
.srn{font-family:'Rajdhani',sans-serif;font-size:1rem;font-weight:700;color:#fff;}
.srip{font-family:'Share Tech Mono',monospace;font-size:.7rem;color:var(--green2);}
.ztag{font-family:'Share Tech Mono',monospace;font-size:.62rem;font-weight:700;letter-spacing:.1em;
  text-transform:uppercase;padding:.25rem .7rem;border-radius:3px;display:inline-block;margin-bottom:.7rem;}
.zi{background:rgba(16,185,129,.08);border:1px solid rgba(16,185,129,.25);color:var(--green2);}
.zd{background:rgba(245,158,11,.08);border:1px solid rgba(245,158,11,.2);color:var(--yellow);}
.ze{background:rgba(236,72,153,.08);border:1px solid rgba(236,72,153,.2);color:var(--pink2);}
.srd{font-size:.88rem;color:rgba(200,200,255,.7);line-height:1.6;margin-bottom:.8rem;}
.srtags{display:flex;flex-wrap:wrap;gap:.3rem;}
.stag{font-family:'Rajdhani',sans-serif;font-size:.75rem;font-weight:600;padding:.2rem .6rem;border-radius:3px;
  background:rgba(139,92,246,.08);border:1px solid rgba(139,92,246,.18);color:rgba(196,181,253,.7);}
.pdot{width:7px;height:7px;border-radius:50%;display:inline-block;background:var(--green2);
  box-shadow:0 0 8px var(--green2);animation:pd 2s infinite;margin-left:5px;vertical-align:middle;}
@keyframes pd{0%,100%{opacity:1;transform:scale(1);}50%{opacity:.4;transform:scale(.6);}}
.synthg{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:1.2rem;margin:2rem 0;}
.syb{background:rgba(139,92,246,.06);border:1px solid rgba(139,92,246,.2);border-radius:8px;
  padding:1.5rem;text-align:center;transition:all .3s;}
.syb:hover{border-color:rgba(139,92,246,.45);transform:translateY(-4px);}
.syi{font-size:2rem;display:block;margin-bottom:.7rem;}
.syb h5{font-family:'Rajdhani',sans-serif;font-size:.88rem;font-weight:700;color:#fff;
  text-transform:uppercase;letter-spacing:.08em;margin-bottom:.4rem;}
.syb p{font-size:.85rem;color:var(--muted);line-height:1.5;}
.refl{background:linear-gradient(135deg,rgba(139,92,246,.07),rgba(6,182,212,.04));
  border:1px solid rgba(139,92,246,.2);border-radius:8px;padding:2rem;margin-top:2rem;}
.refl h4{font-family:'Rajdhani',sans-serif;font-size:1.1rem;font-weight:700;color:var(--vio2);margin-bottom:.9rem;}
.refl p{font-size:.95rem;color:rgba(200,200,255,.8);line-height:1.85;}
.refl strong{color:var(--cyan2);}

/* VEILLE */
.vq{background:linear-gradient(135deg,rgba(139,92,246,.09),rgba(6,182,212,.04));
  border:1px solid rgba(139,92,246,.25);border-radius:10px;padding:2.5rem;margin-bottom:3rem;
  position:relative;overflow:hidden;}
.vql{font-family:'Share Tech Mono',monospace;font-size:.65rem;color:var(--cyan2);
  letter-spacing:.2em;text-transform:uppercase;margin-bottom:.8rem;}
.vq p{font-family:'Rajdhani',sans-serif;font-size:1.2rem;font-weight:600;
  color:rgba(240,240,255,.92);line-height:1.7;font-style:italic;}
.agrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(270px,1fr));gap:1.5rem;}
.acard{display:block;text-decoration:none;color:inherit;background:var(--panel);border:1px solid var(--bv);
  border-radius:10px;padding:2rem;transition:all .4s;position:relative;overflow:hidden;}
.acard::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,var(--vio),var(--cyan2),transparent);}
.acard:hover{border-color:rgba(139,92,246,.55);transform:translateY(-5px);box-shadow:0 16px 40px rgba(0,0,0,.5);}
.aico{font-size:1.6rem;margin-bottom:1rem;}
.acard h4{font-family:'Rajdhani',sans-serif;font-size:1rem;font-weight:700;color:#fff;margin-bottom:.3rem;}
.adate{font-family:'Share Tech Mono',monospace;font-size:.65rem;color:var(--muted);letter-spacing:.08em;margin-bottom:.8rem;}
.acard p{font-size:.88rem;color:var(--muted);line-height:1.6;}
.concl{background:rgba(16,185,129,.05);border:1px solid rgba(16,185,129,.2);border-radius:10px;padding:2.5rem;margin-top:2rem;}
.concl h3{font-family:'Rajdhani',sans-serif;font-size:1.1rem;font-weight:700;color:var(--green2);
  letter-spacing:.06em;margin-bottom:1rem;}
.concl p{font-size:.95rem;color:rgba(200,200,255,.82);line-height:1.85;}

/* CONTACT */
.ctgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:1.5rem;}
.ctcard{background:var(--panel);border:1px solid var(--bv);border-radius:10px;padding:2.5rem;
  text-align:center;position:relative;overflow:hidden;transition:all .4s;}
.ctcard::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,var(--vio),var(--cyan2),transparent);}
.ctcard:hover{border-color:rgba(139,92,246,.55);transform:translateY(-5px);box-shadow:0 16px 40px rgba(0,0,0,.5);}
.ctico{width:60px;height:60px;border-radius:12px;margin:0 auto 1.3rem;display:flex;align-items:center;
  justify-content:center;font-size:1.8rem;background:linear-gradient(135deg,rgba(139,92,246,.18),rgba(6,182,212,.1));
  border:1px solid rgba(139,92,246,.3);}
.ctlbl{font-family:'Share Tech Mono',monospace;font-size:.62rem;letter-spacing:.18em;
  text-transform:uppercase;color:var(--cyan2);margin-bottom:.6rem;}
.ctcard a{color:#fff;text-decoration:none;font-size:.95rem;font-weight:600;transition:color .3s;}
.ctcard a:hover{color:var(--vio2);}

/* GRILLES */
.ph{text-align:center;padding:5rem 2rem;}
.phi{font-size:3rem;display:block;margin-bottom:1rem;}
.ph p{color:var(--muted);}

/* MODAL */
.modal{display:none;position:fixed;z-index:1000;inset:0;background:rgba(0,0,0,.85);
  backdrop-filter:blur(15px);overflow-y:auto;}
.mbox{background:var(--panel2);border:1px solid rgba(139,92,246,.4);border-radius:12px;
  margin:3% auto;padding:3rem;width:90%;max-width:790px;position:relative;
  box-shadow:0 40px 100px rgba(0,0,0,.7);animation:mopen .4s ease;}
.mbox::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;
  background:linear-gradient(90deg,var(--vio),var(--cyan2),var(--pink),var(--vio));
  box-shadow:0 0 12px var(--vio);}
@keyframes mopen{from{opacity:0;transform:scale(.96) translateY(18px);}to{opacity:1;transform:none;}}
.mcl{position:absolute;top:1.5rem;right:1.5rem;width:34px;height:34px;border-radius:6px;
  background:rgba(255,255,255,.04);border:1px solid var(--bv);display:flex;align-items:center;
  justify-content:center;font-size:1rem;color:var(--muted);transition:all .3s;}
.mcl:hover{background:rgba(236,72,153,.12);color:#fff;}
.mbox h2{font-family:'Rajdhani',sans-serif;font-size:1.6rem;font-weight:700;color:#fff;
  margin-bottom:2rem;padding-right:3rem;letter-spacing:.03em;}
.mbox h3{font-family:'Share Tech Mono',monospace;font-size:.65rem;letter-spacing:.18em;
  text-transform:uppercase;color:var(--cyan2);margin:2rem 0 .7rem;display:flex;align-items:center;gap:.5rem;}
.mbox h3::before{content:'▶';color:var(--vio);font-size:.6rem;}
.mbox p,.mbox li{font-size:.93rem;color:rgba(200,200,255,.82);line-height:1.8;margin-bottom:.5rem;}
.mbox ul{margin-left:1.5rem;}
.mbox strong{color:var(--vio2);}

/* FOOTER */
footer{text-align:center;padding:2rem;border-top:1px solid var(--bv);font-family:'Share Tech Mono',monospace;
  font-size:.65rem;color:var(--muted);letter-spacing:.15em;position:relative;z-index:1;}
footer em{color:var(--vio2);font-style:normal;}

@media(max-width:768px){
  header{padding:3rem 1.2rem;}
  .content{padding:2rem 1rem;}
  .tl{padding-left:2rem;}.tld{left:-2.3rem;}
  .mbox{padding:1.8rem;margin:5% auto;}
  .hn1{-webkit-text-stroke:2px #7c3aed;}
  .hn2{font-size:.65rem;}
}
</style>
</head>
<body>

<div id="cur"><svg width="22" height="28" viewBox="0 0 22 28" fill="none"><path d="M2 2L2 22L7.5 16.5L11.5 25L14.5 23.5L10.5 14.5H18L2 2Z" fill="white" stroke="#a78bfa" stroke-width="1.8" stroke-linejoin="round"/></svg></div>
<div id="ntt"></div>

<div class="wrap">

<header>
  <div class="badge"><span class="dot"></span>DISPONIBLE ALTERNANCE 2026–2027</div>
  <span class="hn1">ENNA HRNJIC</span>
  <span class="hn2">BTS SIO · SISR</span>
  <div class="chips">
    <span class="chip chv">⟶ Administration Système</span>
    <span class="chip chc">⟶ Cybersécurité</span>
    <span class="chip chp">⟶ Infrastructure Réseau</span>
  </div>
</header>

<nav>
  <div class="ni">
    <button class="nb on"  onclick="showTab('accueil',this)"><span class="na">▶</span>Accueil</button>
    <button class="nb"     onclick="showTab('parcours',this)"><span class="na">▶</span>Parcours</button>
    <button class="nb"     onclick="showTab('situations',this)"><span class="na">▶</span>Situations Pro</button>
    <button class="nb"     onclick="showTab('infra',this)"><span class="na">▶</span>Infrastructure</button>
    <button class="nb"     onclick="showTab('certifications',this)"><span class="na">▶</span>Certifications</button>
    <button class="nb"     onclick="showTab('veille',this)"><span class="na">▶</span>Veille Techno</button>
    <button class="nb"     onclick="showTab('grilles',this)"><span class="na">▶</span>Grilles</button>
    <button class="nb"     onclick="showTab('contact',this)"><span class="na">▶</span>Contact</button>
  </div>
</nav>

<div class="content">

<!-- ACCUEIL -->
<div id="accueil" class="pane on">
  <div class="sh"><div class="sht">// accueil</div><h2 class="shh">Bienvenue sur mon <em>Portfolio</em></h2><div class="shl"></div></div>
  <div class="card cv" style="text-align:center;margin-bottom:2rem;">
    <p class="about">Je m'appelle <strong>Enna</strong>, actuellement en <strong>BTS SIO option SISR</strong>, spécialisée dans les infrastructures réseaux et systèmes informatiques. Sérieuse, curieuse et motivée, je cherche à développer constamment mes compétences en informatique.</p>
  </div>
  <div class="sgrid">
    <div class="sb"><div class="sbi">🎯</div><div class="sbl">Spécialité</div><div class="sbv">Option SISR</div></div>
    <div class="sb"><div class="sbi">🏫</div><div class="sbl">Formation</div><div class="sbv">Lycée Jacques Brel</div></div>
    <div class="sb"><div class="sbi">🔒</div><div class="sbl">Focus</div><div class="sbv">Réseaux & Sécurité</div></div>
    <div class="sb"><div class="sbi">💼</div><div class="sbl">Objectif</div><div class="sbv">Alternance 2026–2027</div></div>
  </div>
</div>

<!-- PARCOURS -->
<div id="parcours" class="pane">
  <div class="sh"><div class="sht">// parcours scolaire</div><h2 class="shh">Mon <em>Parcours</em></h2><div class="shl"></div></div>
  <div class="card" style="text-align:center;margin-bottom:2.5rem;">
    <p style="font-style:italic;color:var(--muted);line-height:1.8;">D'un parcours en STMG à l'univers de l'informatique, mon chemin académique reflète une évolution guidée par la découverte de ma véritable passion.</p>
  </div>
  <div class="tl">
    <div class="tli">
      <div class="tld"></div>
      <div class="tlc">
        <div class="tcb bp">2021 – 2024</div>
        <div class="tcs">Lycée Jacques Brel</div>
        <div class="tcd">Bac STMG – Spécialité Mercatique</div>
        <p class="tct">En 2021–2022, j'étais en seconde générale. De 2022 à 2024, j'ai suivi la voie STMG spécialité Mercatique. J'ai obtenu mon bac avec mention Bien.</p>
      </div>
    </div>
    <div class="tli">
      <div class="tld now"></div>
      <div class="tlc">
        <div class="tcb bn">2024 – Aujourd'hui</div>
        <div class="tcs">Lycée Jacques Brel</div>
        <div class="tcd">BTS SIO – Option SISR</div>
        <p class="tct">Depuis septembre 2024, je poursuis un BTS Services Informatiques aux Organisations option SISR. Je me forme à l'administration des réseaux, la cybersécurité, le déploiement de serveurs et la maintenance informatique.</p>
      </div>
    </div>
  </div>
</div>

<!-- SITUATIONS PRO -->
<div id="situations" class="pane">
  <div class="sh"><div class="sht">// projets professionnels</div><h2 class="shh">Situations <em>Professionnelles</em></h2><div class="shl"></div></div>
  <div class="card" style="text-align:center;margin-bottom:2.5rem;">
    <!-- MODIF 2 : nouvelle phrase intro projets -->
    <p style="color:var(--muted);">Chaque projet m'a confrontée à un environnement ou un outil que je ne maîtrisais pas encore — l'occasion de sortir de ma zone de confort, de m'adapter rapidement et de transformer l'inconnu en compétence concrète.</p>
  </div>
  <div class="pgrid">
    <div class="pc" onclick="openModal('p1')"><div class="pnum">01</div><div class="pico">🔍</div><h3>Analyse de Trames Réseau</h3><p>Wireshark & Protocoles TCP/IP</p><div class="parr">↗</div></div>
    <div class="pc" onclick="openModal('p2')"><div class="pnum">02</div><div class="pico">🔧</div><h3>Configuration Switch Dell</h3><p>Segmentation VLAN</p><div class="parr">↗</div></div>
    <div class="pc" onclick="openModal('p3')"><div class="pnum">03</div><div class="pico">📊</div><h3>Supervision avec Centreon</h3><p>Monitoring Infrastructure</p><div class="parr">↗</div></div>
    <div class="pc" onclick="openModal('p4')"><div class="pnum">04</div><div class="pico">🤖</div><h3>Migration Agent SIMON</h3><p>Automatisation Tanium</p><div class="parr">↗</div></div>
  </div>
</div>

<!-- INFRASTRUCTURE -->
<div id="infra" class="pane">
  <div class="sh"><div class="sht">// network topology</div><h2 class="shh">Infrastructure <em>Réseau</em></h2><div class="shl"></div></div>
  <div class="card cv" style="margin-bottom:2.5rem;">
    <p class="itxt">Dans le cadre de ma formation BTS SIO, j'ai travaillé sur une <strong>infrastructure réseau complète et segmentée</strong>. Elle comprend une zone interne sécurisée avec <strong>deux contrôleurs Active Directory</strong>, une DMZ et une zone externe, le tout contrôlé par un pare-feu centralisé unique point de sortie vers Internet.</p>
    <div class="ttags">
      <span class="tt ttv">🔥 Pare-feu central</span><span class="tt ttc">🖧 Segmentation réseau</span>
      <span class="tt ttv">📊 Supervision Centreon</span><span class="tt ttc">🪟 Active Directory ×2</span>
      <span class="tt ttv">🛡️ SIEM Wazuh</span><span class="tt ttc">💾 NAS TrueNAS</span>
    </div>
  </div>

  <div class="diag">
    <div class="dh">SCHÉMA RÉSEAU INTERACTIF — survole les équipements</div>
    <div style="overflow-x:auto;">
    <!-- Schéma réseau corrigé -->
    <svg viewBox="0 0 960 640" style="width:100%;max-width:940px;display:block;margin:0 auto;">
      <defs>
        <filter id="gv"><feGaussianBlur stdDeviation="4" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
        <filter id="gc"><feGaussianBlur stdDeviation="3" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
        <filter id="go"><feGaussianBlur stdDeviation="3" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
        <marker id="mv" markerWidth="8" markerHeight="8" refX="4" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#a78bfa"/></marker>
        <marker id="mc" markerWidth="8" markerHeight="8" refX="4" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#22d3ee"/></marker>
        <marker id="mo" markerWidth="8" markerHeight="8" refX="4" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#f59e0b"/></marker>
        <marker id="mb" markerWidth="8" markerHeight="8" refX="4" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#818cf8"/></marker>
        <style>.lv{stroke-dasharray:8 4;animation:ld 2s linear infinite}.lc{stroke-dasharray:6 3;animation:ld 2.5s linear infinite}.ls{stroke-dasharray:5 5;animation:ld 4s linear infinite}@keyframes ld{to{stroke-dashoffset:-24}}.zp{animation:zpu 3s ease-in-out infinite}@keyframes zpu{0%,100%{opacity:.1}50%{opacity:.22}}</style>
      </defs>

      <!-- Zone Interne -->
      <rect x="18" y="22" width="430" height="290" rx="14" fill="rgba(16,185,129,.05)" stroke="#10b981" stroke-width="1.5" stroke-dasharray="6 3" class="zp"/>
      <text x="35" y="48" font-family="'Share Tech Mono',monospace" font-size="11" fill="#34d399" letter-spacing="2">◈ ZONE INTERNE</text>

      <!-- DMZ -->
      <rect x="620" y="22" width="200" height="150" rx="14" fill="rgba(245,158,11,.05)" stroke="#f59e0b" stroke-width="1.5" stroke-dasharray="6 3" class="zp"/>
      <text x="638" y="48" font-family="'Share Tech Mono',monospace" font-size="11" fill="#f59e0b" letter-spacing="2">◈ DMZ</text>

      <!-- Zone Externe — normale, DNS + DCB uniquement -->
      <rect x="18" y="400" width="310" height="175" rx="14" fill="rgba(236,72,153,.04)" stroke="#ec4899" stroke-width="1.5" stroke-dasharray="6 3" class="zp"/>
      <text x="35" y="426" font-family="'Share Tech Mono',monospace" font-size="10" fill="#f472b6" letter-spacing="2">◈ ZONE EXTERNE</text>

      <!-- Firewall -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()"
         data-n="PARE-FEU CENTRAL" data-i="10.0.211.17 / 10.0.211.1 / 172.28.211.1"
         data-r="Sécurité inter-zones" data-d="Seul point de sortie vers Internet. Filtrage strict du trafic entrant/sortant.">
        <rect x="450" y="268" width="115" height="90" rx="10" fill="#0b0b2a" stroke="#f59e0b" stroke-width="2.5" filter="url(#go)"/>
        <text x="507" y="304" font-size="26" text-anchor="middle">🔥</text>
        <text x="507" y="328" font-size="10" fill="#f59e0b" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">FIREWALL</text>
        <text x="507" y="344" font-size="9"  fill="#fbbf24" text-anchor="middle" font-family="'Share Tech Mono',monospace">CENTRAL</text>
      </g>

      <!-- Zone interne → FW -->
      <line x1="448" y1="313" x2="420" y2="313" stroke="#34d399" stroke-width="2" class="lv" marker-end="url(#mv)" opacity=".7"/>

      <!-- FW → DMZ -->
      <line x1="620" y1="98" x2="565" y2="290" stroke="#f59e0b" stroke-width="1.8" class="lc" marker-end="url(#mo)" opacity=".65"/>

      <!-- FW → Zone externe (vers DNS/DCB) -->
      <line x1="507" y1="358" x2="214" y2="440" stroke="#f472b6" stroke-width="1.8" class="lc" marker-end="url(#mo)" opacity=".6"/>
      <text x="320" y="400" font-size="9" fill="#f472b6" font-family="'Share Tech Mono',monospace">172.28.211.1</text>

      <!-- Zone Externe → Internet (flèche WAN depuis le bord droit de la zone externe) -->
      <line x1="328" y1="490" x2="790" y2="490" stroke="#818cf8" stroke-width="1.8" class="ls" marker-end="url(#mb)" opacity=".8"/>
      <text x="500" y="483" font-size="9" fill="#818cf8" font-family="'Share Tech Mono',monospace" text-anchor="middle">WAN</text>

      <!-- AD-01 -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()" data-n="AD-01 — Contrôleur Primaire" data-i="10.0.211.66" data-r="Contrôleur de domaine principal" data-d="Rôles FSMO, authentification Kerberos, GPO et annuaire d'entreprise.">
        <rect x="28" y="60" width="98" height="76" rx="8" fill="#060b12" stroke="#10b981" stroke-width="1.8" filter="url(#gc)"/>
        <text x="77" y="89" font-size="20" text-anchor="middle">🏢</text>
        <text x="77" y="109" font-size="9" fill="#34d399" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">AD-01</text>
        <text x="77" y="123" font-size="8" fill="#065f46" text-anchor="middle" font-family="'Share Tech Mono',monospace">10.0.211.66</text>
      </g>
      <!-- AD-02 -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()" data-n="AD-02 — Contrôleur Secondaire" data-i="10.0.211.69" data-r="Contrôleur de domaine secondaire" data-d="Réplication avec AD-01. Haute disponibilité en cas de panne.">
        <rect x="142" y="60" width="98" height="76" rx="8" fill="#060b12" stroke="#10b981" stroke-width="1.8" filter="url(#gc)"/>
        <text x="191" y="89" font-size="20" text-anchor="middle">🏛️</text>
        <text x="191" y="109" font-size="9" fill="#34d399" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">AD-02</text>
        <text x="191" y="123" font-size="8" fill="#065f46" text-anchor="middle" font-family="'Share Tech Mono',monospace">10.0.211.69</text>
      </g>
      <!-- SRV-FIC -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()" data-n="SRV-FIC" data-i="10.0.211.67" data-r="Serveur de fichiers" data-d="Stockage centralisé avec gestion fine des droits ACL liés aux groupes AD.">
        <rect x="255" y="60" width="98" height="76" rx="8" fill="#060b12" stroke="#10b981" stroke-width="1.8" filter="url(#gc)"/>
        <text x="304" y="89" font-size="20" text-anchor="middle">🗂️</text>
        <text x="304" y="109" font-size="9" fill="#34d399" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">SRV-FIC</text>
        <text x="304" y="123" font-size="8" fill="#065f46" text-anchor="middle" font-family="'Share Tech Mono',monospace">10.0.211.67</text>
      </g>
      <!-- TRUENAS -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()" data-n="SRV-TRUENAS" data-i="10.0.211.68" data-r="NAS / Stockage ZFS" data-d="NAS TrueNAS haute capacité. Sauvegardes et redondance via ZFS.">
        <rect x="365" y="60" width="98" height="76" rx="8" fill="#060b12" stroke="#10b981" stroke-width="1.8" filter="url(#gc)"/>
        <text x="414" y="89" font-size="20" text-anchor="middle">💾</text>
        <text x="414" y="109" font-size="9" fill="#34d399" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">TRUENAS</text>
        <text x="414" y="123" font-size="8" fill="#065f46" text-anchor="middle" font-family="'Share Tech Mono',monospace">10.0.211.68</text>
      </g>
      <!-- CENTREON -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()" data-n="SRV-CENTREON" data-i="10.0.211.64" data-r="Supervision / Monitoring" data-d="Monitoring temps réel via SNMP et NRPE. Alertes et tableaux de bord.">
        <rect x="28" y="185" width="108" height="76" rx="8" fill="#080820" stroke="#8b5cf6" stroke-width="1.8" filter="url(#gv)"/>
        <text x="82" y="214" font-size="20" text-anchor="middle">📊</text>
        <text x="82" y="234" font-size="9" fill="#a78bfa" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">CENTREON</text>
        <text x="82" y="248" font-size="8" fill="#4c1d95" text-anchor="middle" font-family="'Share Tech Mono',monospace">10.0.211.64</text>
      </g>
      <!-- WAZUH -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()" data-n="SRV-WAZUH" data-i="10.0.211.63" data-r="SIEM / Sécurité" data-d="IDS, centralisation des logs de sécurité et réponse aux incidents.">
        <rect x="155" y="185" width="98" height="76" rx="8" fill="#080820" stroke="#8b5cf6" stroke-width="1.8" filter="url(#gv)"/>
        <text x="204" y="214" font-size="20" text-anchor="middle">🛡️</text>
        <text x="204" y="234" font-size="9" fill="#a78bfa" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">WAZUH</text>
        <text x="204" y="248" font-size="8" fill="#4c1d95" text-anchor="middle" font-family="'Share Tech Mono',monospace">10.0.211.63</text>
      </g>
      <!-- W11 CLIENT -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()" data-n="W11 CLIENT" data-i="10.0.211.70" data-r="Poste utilisateur" data-d="Poste Windows 11 rattaché au domaine Active Directory.">
        <rect x="270" y="185" width="102" height="76" rx="8" fill="#080820" stroke="#06b6d4" stroke-width="1.8" filter="url(#gv)"/>
        <text x="321" y="214" font-size="20" text-anchor="middle">💻</text>
        <text x="321" y="234" font-size="9" fill="#22d3ee" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">W11 CLIENT</text>
        <text x="321" y="248" font-size="8" fill="#164e63" text-anchor="middle" font-family="'Share Tech Mono',monospace">10.0.211.70</text>
      </g>
      <!-- SRV-LAMP DMZ -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()" data-n="SRV-LAMP" data-i="10.0.211.10" data-r="Serveur Web (DMZ)" data-d="LAMP Linux/Apache/MySQL/PHP. Accessible depuis l'extérieur via le pare-feu.">
        <rect x="635" y="58" width="98" height="76" rx="8" fill="#130a00" stroke="#f59e0b" stroke-width="1.8" filter="url(#go)"/>
        <text x="684" y="87" font-size="20" text-anchor="middle">🌐</text>
        <text x="684" y="107" font-size="9" fill="#fbbf24" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">SRV-LAMP</text>
        <text x="684" y="121" font-size="8" fill="#92400e" text-anchor="middle" font-family="'Share Tech Mono',monospace">10.0.211.10</text>
      </g>
      <!-- SRV-DNS — zone externe -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()" data-n="SRV-DNS" data-i="10.0.211.65" data-r="Résolution DNS" data-d="Résolution des noms internes + redirection vers DNS publics.">
        <rect x="165" y="450" width="98" height="76" rx="8" fill="#130010" stroke="#ec4899" stroke-width="1.8" filter="url(#go)"/>
        <text x="214" y="479" font-size="20" text-anchor="middle">🔍</text>
        <text x="214" y="499" font-size="9" fill="#f472b6" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">SRV-DNS</text>
        <text x="214" y="513" font-size="8" fill="#831843" text-anchor="middle" font-family="'Share Tech Mono',monospace">10.0.211.65</text>
      </g>
      <!-- DCB CLIENT — zone externe -->
      <g onmouseenter="ns(event,this)" onmouseleave="nh()" data-n="DCB CLIENT" data-i="172.28.211.220" data-r="Client zone externe" data-d="Accès depuis réseau externe peu fiable. Trafic via pare-feu obligatoire.">
        <rect x="30" y="450" width="108" height="76" rx="8" fill="#130010" stroke="#ec4899" stroke-width="1.8" filter="url(#go)"/>
        <text x="84" y="479" font-size="20" text-anchor="middle">🖥️</text>
        <text x="84" y="499" font-size="9" fill="#f472b6" text-anchor="middle" font-family="'Rajdhani',sans-serif" font-weight="700">DCB CLIENT</text>
        <text x="84" y="513" font-size="7.5" fill="#831843" text-anchor="middle" font-family="'Share Tech Mono',monospace">172.28.211.220</text>
      </g>
      <!-- Internet — hors de toute zone, à droite -->
      <text x="850" y="465" font-size="44" text-anchor="middle" opacity=".8">☁️</text>
      <text x="850" y="503" font-size="10" fill="#818cf8" text-anchor="middle" font-family="'Share Tech Mono',monospace" letter-spacing="2">INTERNET</text>

      <!-- Légende — bas droite, sous la DMZ, hors de tout élément -->
      <rect x="620" y="195" width="330" height="165" rx="10" fill="rgba(0,0,0,.65)" stroke="rgba(139,92,246,.2)" stroke-width="1.5"/>
      <text x="640" y="220" font-size="10" fill="#a78bfa" font-family="'Share Tech Mono',monospace" letter-spacing="3">// LÉGENDE</text>
      <rect x="640" y="232" width="12" height="7" rx="1" fill="rgba(16,185,129,.2)" stroke="#10b981"/>
      <text x="658" y="241" font-size="10" fill="#34d399" font-family="'Share Tech Mono',monospace">Zone Interne — AD×2, FIC, NAS</text>
      <rect x="640" y="252" width="12" height="7" rx="1" fill="rgba(245,158,11,.15)" stroke="#f59e0b"/>
      <text x="658" y="261" font-size="10" fill="#f59e0b" font-family="'Share Tech Mono',monospace">DMZ — Services web exposés</text>
      <rect x="640" y="272" width="12" height="7" rx="1" fill="rgba(236,72,153,.12)" stroke="#ec4899"/>
      <text x="658" y="281" font-size="10" fill="#f472b6" font-family="'Share Tech Mono',monospace">Zone Externe — DNS, DCB</text>
      <line x1="640" y1="294" x2="652" y2="294" stroke="#818cf8" stroke-width="1.5" stroke-dasharray="4 2"/>
      <text x="658" y="299" font-size="10" fill="#818cf8" font-family="'Share Tech Mono',monospace">WAN → Internet (hors zones)</text>
      <text x="640" y="348" font-size="9" fill="rgba(139,92,246,.4)" font-family="'Share Tech Mono',monospace">Survole les nœuds pour détails</text>
    </svg>
    </div>
  </div>

  <div class="sh" style="margin-top:3rem;"><div class="sht">// server details</div><h2 class="shh">Détail des <em>Serveurs</em></h2><div class="shl"></div></div>
  <div class="srvgrid">
    <div class="srv sg"><div class="srh"><span class="sri">🏢</span><div><div class="srn">AD-01 Primaire <span class="pdot"></span></div><div class="srip">10.0.211.66</div></div></div><span class="ztag zi">◈ Zone Interne</span><p class="srd">Contrôleur de domaine <strong style="color:var(--vio2)">primaire</strong>. Rôles FSMO, authentification Kerberos, GPO et annuaire d'entreprise.</p><div class="srtags"><span class="stag">Windows Server</span><span class="stag">LDAP</span><span class="stag">GPO</span><span class="stag">Kerberos</span></div></div>
    <div class="srv sg"><div class="srh"><span class="sri">🏛️</span><div><div class="srn">AD-02 Secondaire <span class="pdot"></span></div><div class="srip">10.0.211.69</div></div></div><span class="ztag zi">◈ Zone Interne</span><p class="srd">Contrôleur de domaine <strong style="color:var(--vio2)">secondaire</strong>. Réplication automatique avec AD-01 pour la haute disponibilité.</p><div class="srtags"><span class="stag">Windows Server</span><span class="stag">Réplication AD</span><span class="stag">Failover</span></div></div>
    <div class="srv sv"><div class="srh"><span class="sri">🗂️</span><div><div class="srn">SRV-FIC <span class="pdot"></span></div><div class="srip">10.0.211.67</div></div></div><span class="ztag zi">◈ Zone Interne</span><p class="srd">Serveur de fichiers partagés avec gestion fine des droits ACL par utilisateur et groupe AD.</p><div class="srtags"><span class="stag">SMB</span><span class="stag">ACL</span><span class="stag">Partage réseau</span></div></div>
    <div class="srv sc"><div class="srh"><span class="sri">💾</span><div><div class="srn">SRV-TRUENAS <span class="pdot"></span></div><div class="srip">10.0.211.68</div></div></div><span class="ztag zi">◈ Zone Interne</span><p class="srd">NAS TrueNAS haute capacité pour sauvegardes et redondance des données via ZFS.</p><div class="srtags"><span class="stag">TrueNAS</span><span class="stag">ZFS</span><span class="stag">Sauvegarde</span></div></div>
    <div class="srv sv"><div class="srh"><span class="sri">📊</span><div><div class="srn">SRV-CENTREON <span class="pdot"></span></div><div class="srip">10.0.211.64</div></div></div><span class="ztag zi">◈ Zone Interne</span><p class="srd">Supervision temps réel des services réseau via SNMP et NRPE. Alertes automatiques.</p><div class="srtags"><span class="stag">Centreon</span><span class="stag">SNMP</span><span class="stag">NRPE</span></div></div>
    <div class="srv sp"><div class="srh"><span class="sri">🛡️</span><div><div class="srn">SRV-WAZUH <span class="pdot"></span></div><div class="srip">10.0.211.63</div></div></div><span class="ztag zi">◈ Zone Interne</span><p class="srd">SIEM Wazuh — détection d'intrusions, centralisation des logs et réponse aux incidents.</p><div class="srtags"><span class="stag">SIEM</span><span class="stag">IDS</span><span class="stag">Wazuh</span></div></div>
    <div class="srv sc"><div class="srh"><span class="sri">🌐</span><div><div class="srn">SRV-LAMP <span class="pdot"></span></div><div class="srip">10.0.211.10</div></div></div><span class="ztag zd">◈ DMZ</span><p class="srd">Serveur LAMP (Linux/Apache/MySQL/PHP) accessible depuis l'extérieur via le pare-feu.</p><div class="srtags"><span class="stag">Apache</span><span class="stag">PHP</span><span class="stag">MySQL</span></div></div>
    <div class="srv sp"><div class="srh"><span class="sri">🔍</span><div><div class="srn">SRV-DNS <span class="pdot"></span></div><div class="srip">10.0.211.65</div></div></div><span class="ztag ze">◈ Zone Externe</span><p class="srd">Résolution des noms de domaine internes + redirection vers résolveurs DNS publics.</p><div class="srtags"><span class="stag">DNS</span><span class="stag">BIND</span><span class="stag">Résolution</span></div></div>
    <div class="srv sc"><div class="srh"><span class="sri">🖥️</span><div><div class="srn">DCB CLIENT <span class="pdot"></span></div><div class="srip">172.28.211.220</div></div></div><span class="ztag ze">◈ Zone Externe</span><p class="srd">Client zone externe simulant un accès depuis un réseau peu fiable. Trafic via pare-feu obligatoire.</p><div class="srtags"><span class="stag">Client</span><span class="stag">172.28.x.x</span></div></div>
  </div>

  <div class="card cv" style="margin-top:3rem;">
    <div class="synthg">
      <div class="syb"><span class="syi">🔥</span><h5>Pare-feu</h5><p>Seul point de sortie vers Internet</p></div>
      <div class="syb"><span class="syi">🏢</span><h5>Double AD</h5><p>Redondance et haute disponibilité</p></div>
      <div class="syb"><span class="syi">📊</span><h5>Supervision</h5><p>Centreon + Wazuh</p></div>
      <div class="syb"><span class="syi">🌐</span><h5>DMZ isolée</h5><p>Services web contrôlés</p></div>
    </div>
    <!-- MODIF 3 : nouvelle réflexion "Ce que j'ai appris" -->
    <div class="refl">
      <h4>▶ Ce que j'ai appris</h4>
      <p>Ce projet m'a appris que <strong>construire une infrastructure, c'est avant tout apprendre à anticiper</strong>. Chaque choix de segmentation, chaque règle de pare-feu, chaque service placé en DMZ répond à une logique que j'ai dû comprendre avant de pouvoir l'appliquer. J'ai découvert que la sécurité ne se greffe pas sur une architecture — <strong>elle se conçoit avec elle, dès le départ</strong>. Ce travail m'a donné le goût de la rigueur technique et m'a montré que la maîtrise vient toujours de la curiosité qu'on met à comprendre pourquoi, pas seulement comment.</p>
    </div>
  </div>
</div>

<!-- CERTIFICATIONS -->
<div id="certifications" class="pane">
  <div class="sh"><div class="sht">// certifications</div><h2 class="shh">Mes <em>Certifications</em></h2><div class="shl"></div></div>
  <div class="card" style="text-align:center;margin-bottom:2.5rem;">
    <p style="color:var(--muted);">Des certifications attestant de mes compétences techniques et de mon engagement continu.</p>
  </div>
  <div class="cgrid">
    <div class="ccard"><div class="cico">🌐</div><h3>Cisco Networking Basics</h3><p class="ciss">Cisco</p><span class="cst cok">✓ Obtenue</span></div>
    <div class="ccard"><div class="cico">⚙️</div><h3>Devices and Initial Configuration</h3><p class="ciss">Cisco</p><span class="cst cok">✓ Obtenue</span></div>
    <div class="ccard"><div class="cico">🔒</div><h3>Introduction to Cybersecurity</h3><p class="ciss">Cisco</p><span class="cst cok">✓ Obtenue</span></div>
    <div class="ccard"><div class="cico">🛡️</div><h3>SecNum</h3><p class="ciss">ANSSI</p><span class="cst cok">✓ Obtenue</span></div>
    <div class="ccard"><div class="cico">🎯</div><h3>Root-Me</h3><p class="ciss">300 points</p><span class="cst cok">✓ Actif</span></div>
    <div class="ccard"><div class="cico">☁️</div><h3>AWS Cloud Practitioner</h3><p class="ciss">Amazon Web Services</p><span class="cst cpr">⟳ En préparation</span></div>
  </div>
</div>

<!-- VEILLE -->
<div id="veille" class="pane">
  <div class="sh"><div class="sht">// veille technologique</div><h2 class="shh">Veille <em>Technologique</em></h2><div class="shl"></div></div>
  <div class="vq">
    <div class="vql">// problématique</div>
    <p>Comment les nouvelles technologies, censées faciliter le quotidien, peuvent-elles également représenter une menace pour la sécurité, la vie privée et les libertés individuelles ?</p>
  </div>
  <div class="agrid">
    <a href="https://www.tf1info.fr/high-tech/verif-videos-flipper-zero-piratage-hackers-feux-tricolores-flippers-carte-bancaire-telephone-portable-2343480.html" target="_blank" class="acard"><div class="aico">🔓</div><h4>Que peut vraiment faire le Flipper Zero…</h4><p class="adate">TF1info · 8 janvier 2025</p><p>Le Flipper Zero peut reproduire des signaux électroniques utilisés par des badges d'accès, révélant des failles exploitables dans les systèmes IoT.</p></a>
    <a href="https://www.lemonde.fr/pixels/article/2025/08/18/la-discrete-montee-en-puissance-de-la-reconnaissance-faciale-dans-le-monde_6631500_4408996.html" target="_blank" class="acard"><div class="aico">👁️</div><h4>La montée en puissance de la reconnaissance faciale</h4><p class="adate">Le Monde · 18 août 2025</p><p>La reconnaissance faciale suscite des inquiétudes quant à l'identification et au suivi des individus sans leur consentement.</p></a>
    <a href="https://www.lemonde.fr/international/article/2025/07/17/une-nouvelle-identite-numerique-pour-controler-encore-davantage-l-internet-chinois_6621732_3210.html" target="_blank" class="acard"><div class="aico">🆔</div><h4>Une nouvelle identité numérique en Chine</h4><p class="adate">Le Monde · 17 juillet 2025</p><p>La Chine a lancé un système d'identité numérique centralisé renforçant le contrôle de l'État sur Internet.</p></a>
    <a href="https://fr.wikipedia.org/wiki/Syst%C3%A8me_de_cr%C3%A9dit_social" target="_blank" class="acard"><div class="aico">📊</div><h4>Système de crédit social</h4><p class="adate">Wikipédia · Consulté en 2025</p><p>Mécanismes d'évaluation du comportement des citoyens en Chine — exemple type de surveillance systématique à grande échelle.</p></a>
  </div>
  <div class="concl">
    <h3>▶ Conclusion</h3>
    <p>Pour répondre à la problématique, les nouvelles technologies sont initialement conçues pour simplifier notre quotidien : elles permettent de communiquer instantanément, de sécuriser nos logements grâce aux objets connectés, ou encore d'effectuer des démarches administratives en ligne plus rapidement. Cependant, ces mêmes technologies, lorsqu'elles sont mal sécurisées ou utilisées sans encadrement, peuvent devenir des outils d'intrusion ou de surveillance, comme le montrent les failles des objets connectés ou certains systèmes de contrôle numérique à grande échelle. Il est donc essentiel de trouver un équilibre entre innovation, sécurité et respect des libertés individuelles, afin que la technologie reste un outil au service de l'humain et non un moyen de restriction.</p>
  </div>
</div>

<!-- GRILLES -->
<div id="grilles" class="pane">
  <div class="sh"><div class="sht">// grilles compétences</div><h2 class="shh">Grilles des <em>Compétences</em></h2><div class="shl"></div></div>
  <div class="card"><div class="ph"><span class="phi">🔮</span><p>Contenu à venir...</p></div></div>
</div>

<!-- CONTACT -->
<div id="contact" class="pane">
  <div class="sh"><div class="sht">// contact</div><h2 class="shh">Me <em>Contacter</em></h2><div class="shl"></div></div>
  <div class="ctgrid">
    <div class="ctcard"><div class="ctico">📧</div><div class="ctlbl">Email</div><a href="mailto:hrnjicenna@gmail.com">hrnjicenna@gmail.com</a></div>
    <div class="ctcard"><div class="ctico">💼</div><div class="ctlbl">LinkedIn</div><a href="https://www.linkedin.com/in/enna-hrnjic" target="_blank">Enna Hrnjic</a></div>
    <div class="ctcard"><div class="ctico">📱</div><div class="ctlbl">Téléphone</div><a href="tel:0772321290">07.72.32.12.90</a></div>
  </div>
</div>

</div></div>

<footer><em>ENNA HRNJIC</em> · BTS SIO SISR · <em>2025</em></footer>

<!-- MODALS -->
<div id="p1" class="modal"><div class="mbox">
  <div class="mcl" onclick="closeModal('p1')">✕</div>
  <h2>Analyse de Trames Réseau avec Wireshark</h2>
  <h3>Contexte</h3><p>TP d'analyse de trames réseau dans un environnement virtualisé VMware.</p>
  <h3>Environnement technique</h3><ul><li><strong>POSTE-1</strong> : génération de trafic réseau</li><li><strong>POSTE-2</strong> : FTP, messagerie (hMailServer), web (XAMPP)</li><li><strong>POSTE-3</strong> : capture Wireshark</li></ul>
  <h3>Réalisation</h3><p>Configuration du serveur, génération de trafic : DNS, ping, DHCP, HTTP, emails. Capture et analyse sur la machine sniffeur.</p>
  <h3>Compétences développées</h3><ul><li>Analyse des protocoles TCP, UDP, HTTP, FTP</li><li>Utilisation de Wireshark</li><li>Compréhension des couches OSI</li><li>Diagnostic de problèmes réseau</li></ul>
  <h3>Bilan</h3><p>Observation de trames ARP, ICMP, DNS, FTP, HTTP, SMTP, DHCP. Compréhension des enjeux de sécurité des protocoles non chiffrés.</p>
</div></div>

<div id="p2" class="modal"><div class="mbox">
  <div class="mcl" onclick="closeModal('p2')">✕</div>
  <h2>Configuration Switch Dell – Segmentation VLAN</h2>
  <h3>Contexte</h3><p>Configuration d'un switch Dell pour un commissariat de police à Saint-Fons.</p>
  <h3>Problématique</h3><p>Tous les équipements étaient sur un seul VLAN. Il fallait segmenter, sécuriser et permettre une administration centralisée.</p>
  <h3>Réalisation</h3><p>Attribution d'IP fixe, suppression du VLAN 1, création du VLAN de management (VLAN 999), puis configuration de plus de 30 VLANs.</p>
  <h3>Compétences développées</h3><ul><li>Configuration de switches Dell</li><li>Gestion et création de VLANs</li><li>Routage inter-VLAN</li><li>Administration à distance SSH</li></ul>
  <h3>Bilan</h3><p>Manipulation d'un équipement réseau réel. Compréhension de la segmentation pour améliorer sécurité et fiabilité.</p>
</div></div>

<div id="p3" class="modal"><div class="mbox">
  <div class="mcl" onclick="closeModal('p3')">✕</div>
  <h2>Supervision avec Centreon</h2>
  <h3>Contexte</h3><p>Mise en place d'une solution de supervision pour une infrastructure Linux, Windows et équipements réseau.</p>
  <h3>Environnement</h3><ul><li>VM Debian 12 + Centreon</li><li>Protocoles SNMPv3 et HTTPS</li><li>Machines Linux et Windows supervisées</li></ul>
  <h3>Réalisation</h3><p>Installation Centreon sur VM Debian 12, sécurisation MariaDB/HTTPS/SNMPv3. Ajout des hôtes, configuration des connecteurs, tests d'alertes.</p>
  <h3>Compétences développées</h3><ul><li>Installation et configuration de Centreon</li><li>Administration système Linux</li><li>Sécurisation d'infrastructure</li><li>Supervision mixte Linux/Windows</li></ul>
  <h3>Bilan</h3><p>Démarche complète : installation → sécurisation → configuration → tests.</p>
</div></div>

<div id="p4" class="modal"><div class="mbox">
  <div class="mcl" onclick="closeModal('p4')">✕</div>
  <h2>Migration et automatisation d'un agent SIMON</h2>
  <h3>Contexte</h3><p>Remplacement de l'agent <strong>SIMON</strong> devenu obsolète sur l'ensemble des serveurs de l'entreprise.</p>
  <h3>Environnement</h3><ul><li>Serveurs Windows web et applicatifs</li><li>Outil de supervision : <strong>SIMON</strong></li><li>Outil de déploiement : <strong>Tanium</strong></li></ul>
  <h3>Réalisation</h3><p>Migration manuelle sur 5 serveurs pilotes pour valider la procédure, puis automatisation via le module Deploy de Tanium.</p>
  <h3>Compétences développées</h3><ul><li>Gestion d'une migration technique</li><li>Déploiement automatisé avec Tanium</li><li>Administration de serveurs Windows</li><li>Gestion de projet avec phase pilote</li></ul>
  <h3>Bilan</h3><p>Compréhension de la gestion d'une migration en limitant les risques grâce à une phase pilote.</p>
</div></div>

<script>
// CURSEUR
var cur = document.getElementById('cur');
cur.style.opacity = '0';
document.addEventListener('mousemove', function(e) {
  cur.style.opacity = '1';
  cur.style.left = e.clientX + 'px';
  cur.style.top  = e.clientY + 'px';
});

// ONGLETS
function showTab(id, btn) {
  var panes = document.getElementsByClassName('pane');
  for (var i = 0; i < panes.length; i++) { panes[i].classList.remove('on'); }
  var btns = document.getElementsByClassName('nb');
  for (var i = 0; i < btns.length; i++) { btns[i].classList.remove('on'); }
  document.getElementById(id).classList.add('on');
  btn.classList.add('on');
  var r = btn.getBoundingClientRect();
  var a = document.createElement('div');
  a.style.cssText = 'position:fixed;left:' + (r.left + r.width/2 - 11) + 'px;top:' + (r.bottom + 5) + 'px;z-index:9999;pointer-events:none;animation:adrop 0.65s cubic-bezier(.22,.68,0,1.2) forwards;';
  a.innerHTML = '<svg width="22" height="28" viewBox="0 0 22 28" fill="none"><path d="M2 2L2 22L7.5 16.5L11.5 25L14.5 23.5L10.5 14.5H18L2 2Z" fill="white" stroke="#a78bfa" stroke-width="1.8" stroke-linejoin="round"/></svg>';
  document.body.appendChild(a);
  setTimeout(function() { if (a.parentNode) a.parentNode.removeChild(a); }, 700);
}

// MODALS
function openModal(id) { document.getElementById(id).style.display = 'block'; document.body.style.overflow = 'hidden'; }
function closeModal(id) { document.getElementById(id).style.display = 'none'; document.body.style.overflow = ''; }
window.addEventListener('click', function(e) {
  if (e.target.classList.contains('modal')) { e.target.style.display = 'none'; document.body.style.overflow = ''; }
});

// TOOLTIP RÉSEAU
var ntt = document.getElementById('ntt');
function ns(e, el) {
  ntt.innerHTML = '<h4>' + (el.dataset.n || '') + '</h4>' +
    '<p class="tip-i">◈ ' + (el.dataset.i || '') + '</p>' +
    '<p class="tip-r">' + (el.dataset.r || '') + '</p>' +
    '<p class="tip-d">' + (el.dataset.d || '') + '</p>';
  ntt.classList.add('on');
  nm(e);
}
function nh() { ntt.classList.remove('on'); }
function nm(e) {
  ntt.style.left = Math.min(e.clientX + 16, window.innerWidth - 265) + 'px';
  ntt.style.top  = Math.min(e.clientY + 16, window.innerHeight - 185) + 'px';
}
var svgNodes = document.querySelectorAll('[onmouseenter]');
for (var i = 0; i < svgNodes.length; i++) { svgNodes[i].addEventListener('mousemove', nm); }

// TILT 3D
var tiltEls = document.querySelectorAll('.card,.pc,.ccard,.ctcard,.srv,.sb,.tlc');
for (var i = 0; i < tiltEls.length; i++) {
  (function(c) {
    c.addEventListener('mousemove', function(e) {
      var r = c.getBoundingClientRect();
      var x = (e.clientX - r.left) / r.width  - 0.5;
      var y = (e.clientY - r.top)  / r.height - 0.5;
      c.style.transform = 'translateY(-4px) rotateX(' + (-y * 6) + 'deg) rotateY(' + (x * 6) + 'deg)';
    });
    c.addEventListener('mouseleave', function() { c.style.transform = ''; });
  })(tiltEls[i]);
}

// ICONES FLOTTANTES
(function() {
  var icons = ['💻','🖥️','🖱️','⌨️','📡','🔒','🛡️','⚙️','🌐','📶','🔐','💾','🖨️','📟','🔧','🔌','📲','🗄️','🕹️','📊'];
  for (var i = 0; i < 32; i++) {
    var el = document.createElement('div');
    el.className = 'fi';
    el.textContent = icons[Math.floor(Math.random() * icons.length)];
    el.style.left = Math.random() * 100 + 'vw';
    el.style.fontSize = (1 + Math.random() * 1.2) + 'rem';
    el.style.animationDuration = (13 + Math.random() * 22) + 's';
    el.style.animationDelay = (-Math.random() * 35) + 's';
    document.body.appendChild(el);
  }
})();
</script>
</body>
</html>

