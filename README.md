# hydraa

[index.html](https://github.com/user-attachments/files/33080578/index.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="theme-color" content="#05060f">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<link rel="manifest" href="manifest.webmanifest">
<link rel="apple-touch-icon" href="icon-192.png">
<meta name="apple-mobile-web-app-capable" content="yes">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns=%27http://www.w3.org/2000/svg%27 viewBox=%270 0 100 100%27%3E%3Ctext y=%27.9em%27 font-size=%2790%27%3E%F0%9F%92%A7%3C/text%3E%3C/svg%3E">
<title>Hydra — Água e Medicamentos</title>
<style>
:root{--bg:#05060f;--bg2:#0b0f24;--card:rgba(18,23,48,.72);--card2:#10152e;--text:#f4f6ff;--muted:#8e97b8;
--blue:#2f7bff;--nblue:#27c8ff;--purple:#8a5cff;--npurple:#c04bff;--ok:#38e8b0;--bad:#ff5d8f;
--grad:linear-gradient(135deg,#2f7bff,#8a5cff 60%,#c04bff);--grad2:linear-gradient(90deg,#27c8ff,#8a5cff);
--border:rgba(140,160,255,.14);--shadow:0 16px 44px rgba(0,0,0,.45)}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;min-height:100vh;color:var(--text);font-family:"Plus Jakarta Sans",Inter,system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;
background:radial-gradient(900px 500px at 85% -10%,rgba(138,92,255,.22),transparent 60%),radial-gradient(700px 500px at -10% 10%,rgba(47,123,255,.2),transparent 60%),var(--bg);background-attachment:fixed}
button,input,select,textarea{font:inherit;color:inherit}
button{cursor:pointer;border:0;background:none}
:focus-visible{outline:2px solid var(--nblue);outline-offset:2px}
.hidden{display:none!important}
main{padding:18px 16px calc(100px + env(safe-area-inset-bottom));max-width:1080px;margin:auto}
.top{display:flex;justify-content:space-between;align-items:flex-start;gap:12px;margin-bottom:16px}
h1{font-size:26px;margin:0 0 4px;letter-spacing:-.5px}
.sub{color:var(--muted);font-size:14px}
.date{color:var(--muted);font-size:12px;text-align:right;white-space:nowrap}
h2{font-size:16px;margin:0 0 12px}
.card{background:var(--card);border:1px solid var(--border);border-radius:24px;box-shadow:var(--shadow);padding:20px;backdrop-filter:blur(14px);-webkit-backdrop-filter:blur(14px)}
.grid{display:grid;gap:14px}
@media(min-width:900px){.grid.two{grid-template-columns:1.2fr 1fr}.span2{grid-column:1/-1}}
.hero{display:flex;gap:22px;align-items:center;flex-wrap:wrap}
.ring{position:relative;width:150px;height:150px;flex:none}
.ring svg{width:100%;height:100%;transform:rotate(-90deg)}
.ring .bg{stroke:rgba(255,255,255,.08)}
.ring .fg{stroke:url(#g);transition:stroke-dashoffset .9s cubic-bezier(.2,.8,.2,1);filter:drop-shadow(0 0 6px rgba(138,92,255,.7))}
.ring .c{position:absolute;inset:0;display:grid;place-content:center;text-align:center}
.pct{font-size:32px;font-weight:800}.mut{color:var(--muted);font-size:12px}
.stats{flex:1;min-width:170px}
.big{font-size:30px;font-weight:800;letter-spacing:-1px}.big small{font-size:14px;color:var(--muted);font-weight:500}
.row{display:flex;justify-content:space-between;padding:9px 0;border-bottom:1px solid var(--border);font-size:13px}.row:last-child{border:0}
.row b{font-weight:700}
.btn{padding:14px 18px;border-radius:16px;background:var(--grad);font-weight:700;color:#fff;box-shadow:0 8px 26px rgba(138,92,255,.35);transition:transform .15s,box-shadow .2s}
.btn:hover{box-shadow:0 10px 32px rgba(138,92,255,.55)}.btn:active{transform:scale(.97)}
.btn.full{width:100%}
.ghost{padding:12px 14px;border-radius:14px;border:1px solid var(--border);background:rgba(255,255,255,.03);font-weight:600;transition:.15s}
.ghost:hover{border-color:var(--nblue)}.ghost:active{transform:scale(.97)}
.ghost.ok{border-color:var(--ok);color:var(--ok)}.ghost.danger{color:var(--bad)}
.quick{display:grid;grid-template-columns:repeat(auto-fit,minmax(90px,1fr));gap:9px;margin-top:16px}
.quick .ghost{padding:14px 6px;text-align:center}
.quick small{display:block;color:var(--muted);font-weight:500;font-size:11px}
.pill{font-size:11px;padding:4px 9px;border-radius:99px;font-weight:700;display:inline-block}
.p-taken{background:rgba(56,232,176,.14);color:var(--ok)}.p-late{background:rgba(255,93,143,.14);color:var(--bad)}.p-pending{background:rgba(39,200,255,.12);color:var(--nblue)}.p-off{background:rgba(255,255,255,.08);color:var(--muted)}
.next{display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap}
.time{font-size:34px;font-weight:800;background:var(--grad2);-webkit-background-clip:text;background-clip:text;color:transparent}
.acts{display:flex;gap:8px;flex-wrap:wrap}
.kpis{display:grid;grid-template-columns:repeat(2,1fr);gap:10px}
@media(min-width:700px){.kpis.k4{grid-template-columns:repeat(4,1fr)}}
.kpi{padding:16px;border-radius:18px;background:rgba(255,255,255,.04);border:1px solid var(--border)}
.kpi b{font-size:22px;display:block}.kpi span{color:var(--muted);font-size:12px}
.chart svg{width:100%;height:auto;display:block}
.alert{display:flex;gap:10px;padding:12px 14px;border-radius:16px;background:rgba(138,92,255,.1);border:1px solid rgba(138,92,255,.25);font-size:13px;margin-bottom:8px}
.alert.warn{background:rgba(255,93,143,.1);border-color:rgba(255,93,143,.3)}
.entry{display:flex;align-items:center;gap:12px;padding:10px 0;border-bottom:1px solid var(--border)}.entry:last-child{border:0}
.thumb{width:46px;height:46px;border-radius:14px;background:var(--card2);display:grid;place-items:center;font-size:22px;object-fit:cover;flex:none}
.grow{flex:1;min-width:0}.x{color:var(--muted);font-size:20px;padding:6px 10px}.x:hover{color:var(--bad)}
.med{margin-bottom:12px}
.med-h{display:flex;justify-content:space-between;gap:10px;align-items:flex-start;margin-bottom:8px}
.slot{display:flex;align-items:center;gap:10px;justify-content:space-between;flex-wrap:wrap;padding:10px 12px;border-radius:14px;background:rgba(255,255,255,.04);margin-top:8px}
.slot.done{opacity:.75}
.empty{text-align:center;color:var(--muted);padding:26px 10px;font-size:14px}
.field{margin-bottom:13px}label{display:block;font-size:12px;color:var(--muted);margin:0 0 6px 2px}
input,select,textarea{width:100%;padding:13px 14px;border-radius:14px;border:1px solid var(--border);background:rgba(5,8,22,.7);outline:none;transition:border .2s}
input:focus,select:focus,textarea:focus{border-color:var(--purple)}
.two-c{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.days{display:flex;gap:6px;flex-wrap:wrap}.day{padding:9px 11px;border-radius:12px;border:1px solid var(--border);font-size:13px;font-weight:600;color:var(--muted)}.day.on{background:var(--grad);color:#fff;border-color:transparent}
.sw{width:50px;height:28px;border-radius:20px;background:#2a3050;padding:3px;transition:.2s;flex:none}.sw i{display:block;width:22px;height:22px;border-radius:50%;background:#fff;transition:.2s}.sw.on{background:var(--grad)}.sw.on i{transform:translateX(22px)}
.tg{display:flex;justify-content:space-between;align-items:center;gap:12px;padding:12px 0;border-bottom:1px solid var(--border)}
.avatar{width:84px;height:84px;border-radius:50%;background:var(--grad);display:grid;place-items:center;font-size:34px;overflow:hidden;flex:none;border:3px solid rgba(255,255,255,.15)}
.avatar img{width:100%;height:100%;object-fit:cover}
.modal{position:fixed;inset:0;background:rgba(2,3,10,.75);backdrop-filter:blur(4px);display:none;align-items:flex-end;justify-content:center;z-index:60;padding:10px}
.modal.show{display:flex}.modal.show .box{animation:up .25s ease}
@keyframes up{from{transform:translateY(30px);opacity:0}}
.box{width:min(100%,520px);max-height:92vh;overflow:auto;background:#0d1230;border:1px solid var(--border);border-radius:28px;padding:20px}
@media(min-width:600px){.modal{align-items:center}}
.mh{display:flex;justify-content:space-between;align-items:center;margin-bottom:14px}
.close{width:34px;height:34px;border-radius:50%;background:rgba(255,255,255,.08)}
.toast{position:fixed;left:50%;bottom:96px;transform:translate(-50%,20px);background:#fff;color:#0b0f24;padding:12px 18px;border-radius:14px;font-size:13px;font-weight:700;opacity:0;pointer-events:none;transition:.25s;z-index:100;max-width:90vw;text-align:center}
.toast.show{opacity:1;transform:translate(-50%,0)}
.note{font-size:12px;color:var(--muted);line-height:1.55;margin-top:10px}
#nav{position:fixed;bottom:0;left:0;right:0;display:grid;grid-template-columns:repeat(5,1fr);padding:8px 8px calc(8px + env(safe-area-inset-bottom));background:rgba(8,11,28,.88);backdrop-filter:blur(18px);-webkit-backdrop-filter:blur(18px);border-top:1px solid var(--border);z-index:40}
#nav .brand{display:none}
#nav button{display:flex;flex-direction:column;align-items:center;gap:3px;padding:8px 2px;border-radius:14px;color:var(--muted);font-size:11px;font-weight:600;transition:.2s}
#nav button .ic{font-size:20px}
#nav button.on{color:#fff;background:rgba(138,92,255,.18);box-shadow:inset 0 0 0 1px rgba(138,92,255,.4)}
@media(min-width:900px){
#nav{top:0;right:auto;width:230px;bottom:0;display:flex;flex-direction:column;gap:6px;padding:26px 14px;border-top:0;border-right:1px solid var(--border)}
#nav .brand{display:block;font-size:26px;font-weight:800;padding:0 12px 20px}#nav .brand span{color:var(--npurple)}
#nav button{flex-direction:row;gap:12px;font-size:14px;padding:12px 14px}
main{margin-left:230px;max-width:none;padding:30px 36px 40px}main>section{max-width:1040px}
.toast{bottom:30px}.modal{padding:20px}}
@media(prefers-reduced-motion:reduce){*{transition:none!important;animation:none!important}}

/* ===== polimento visual (efeitos) ===== */
body{-webkit-font-smoothing:antialiased;font-variant-numeric:tabular-nums}
h1,.pct,.big,.time{letter-spacing:-.03em}
.btn,.ghost,.day,#nav button,.close{position:relative;overflow:hidden;-webkit-tap-highlight-color:transparent}
.btn{background-size:170% 170%;background-position:0 50%;transition:transform .25s cubic-bezier(.2,.8,.2,1),box-shadow .3s,background-position .6s}
.btn:hover{transform:translateY(-2px);background-position:100% 50%;box-shadow:0 16px 40px rgba(138,92,255,.55),inset 0 0 0 1px rgba(255,255,255,.14)}
.btn:active{transform:translateY(0) scale(.97);box-shadow:0 6px 18px rgba(138,92,255,.4)}
.btn::after{content:"";position:absolute;inset:0;background:linear-gradient(110deg,transparent 30%,rgba(255,255,255,.38) 50%,transparent 70%);transform:translateX(-130%);transition:transform .8s}
.btn:hover::after{transform:translateX(130%)}
.ghost{transition:transform .22s cubic-bezier(.2,.8,.2,1),border-color .2s,background .2s,box-shadow .25s}
.ghost:hover{transform:translateY(-2px);border-color:var(--nblue);background:rgba(39,200,255,.07);box-shadow:0 10px 24px rgba(39,200,255,.16)}
.ghost.ok:hover{background:rgba(56,232,176,.1);box-shadow:0 10px 24px rgba(56,232,176,.18)}
.ghost.danger:hover{border-color:var(--bad);background:rgba(255,93,143,.08);box-shadow:0 10px 24px rgba(255,93,143,.16)}
.ghost:active{transform:translateY(0) scale(.97)}
#nav button:hover:not(.on){color:#fff;background:rgba(255,255,255,.05)}
.day:hover:not(.on){border-color:var(--purple);color:#fff}
.rip{position:absolute;border-radius:50%;background:rgba(255,255,255,.35);transform:scale(0);animation:rip .6s ease-out forwards;pointer-events:none}
@keyframes rip{to{transform:scale(2.6);opacity:0}}
.card{transition:transform .3s cubic-bezier(.2,.8,.2,1),border-color .3s,box-shadow .3s}
@media(hover:hover){.card:hover{border-color:rgba(138,92,255,.4);box-shadow:0 20px 50px rgba(0,0,0,.5),0 0 0 1px rgba(138,92,255,.12)}}
section.enter{animation:fadeUp .5s cubic-bezier(.2,.8,.2,1) both}
@keyframes fadeUp{from{opacity:0;transform:translateY(14px)}}
input:focus,select:focus,textarea:focus{box-shadow:0 0 0 3px rgba(138,92,255,.22)}
</style>
</head>
<body>
<nav id="nav" aria-label="Navegação principal">
  <div class="brand">hydra<span>.</span></div>
  <button data-p="home"><span class="ic">🏠</span>Início</button>
  <button data-p="water"><span class="ic">💧</span>Água</button>
  <button data-p="meds"><span class="ic">💊</span>Remédios</button>
  <button data-p="progress"><span class="ic">📊</span>Progresso</button>
  <button data-p="profile"><span class="ic">👤</span>Perfil</button>
</nav>

<main>
<svg width="0" height="0" style="position:absolute"><defs>
<linearGradient id="g" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#27c8ff"/><stop offset="55%" stop-color="#8a5cff"/><stop offset="1" stop-color="#c04bff"/></linearGradient></defs></svg>

<!-- INÍCIO -->
<section id="home">
  <div class="top"><div><h1 id="greet"></h1><div class="sub" id="greetSub"></div></div><div class="date" id="today"></div></div>
  <div class="grid two">
    <div class="card span2">
      <h2>💧 Hidratação de hoje</h2>
      <div class="hero">
        <div class="ring"><svg viewBox="0 0 120 120"><circle class="bg" cx="60" cy="60" r="52" fill="none" stroke-width="10"/><circle class="fg" id="ringFg" cx="60" cy="60" r="52" fill="none" stroke-width="10" stroke-linecap="round" stroke-dasharray="326.7" stroke-dashoffset="326.7"/></svg>
          <div class="c"><div class="pct" id="pct">0%</div><div class="mut">da meta</div></div></div>
        <div class="stats">
          <div class="big"><span id="cons">0</span> <small>/ <span id="goal">0</span> ml</small></div>
          <div class="row"><span>Restante</span><b id="rem"></b></div>
          <div class="row"><span>Meta diária</span><b id="goal2"></b></div>
          <div class="row"><span>Copos de 200 ml</span><b id="cups"></b></div>
        </div>
      </div>
      <button class="btn full" style="margin-top:16px" onclick="openWater()">+ Adicionar água</button>
      <div class="quick" style="margin-top:10px">
        <button class="ghost" onclick="addDrink(200)">+ 200 ml</button>
        <button class="ghost" onclick="addDrink(300)">+ 300 ml</button>
        <button class="ghost" onclick="addDrink(500)">+ 500 ml</button>
        <button class="ghost" onclick="openWater()">Outro…</button>
      </div>
    </div>
    <div class="card"><h2>💊 Próximo medicamento</h2><div id="nextMed"></div></div>
    <div class="card"><h2>📋 Resumo do dia</h2><div class="kpis" id="daySum"></div><div class="note" id="progMsg"></div></div>
    <div class="card chart"><h2>📊 Últimos 7 dias</h2><div id="chartHome"></div></div>
    <div class="card"><h2>🔔 Alertas</h2><div id="alerts"></div></div>
  </div>
</section>

<!-- ÁGUA -->
<section id="water" class="hidden">
  <div class="top"><div><h1>Água</h1><div class="sub">Registre cada copo ou garrafa.</div></div></div>
  <div class="card">
    <div class="quick" style="margin-top:0">
      <button class="ghost" onclick="addDrink(200)">200 ml<small>copo</small></button>
      <button class="ghost" onclick="addDrink(300)">300 ml<small>copo grande</small></button>
      <button class="ghost" onclick="addDrink(500)">500 ml<small>garrafinha</small></button>
      <button class="ghost" onclick="addDrink(750)">750 ml<small>garrafa</small></button>
      <button class="ghost" onclick="addDrink(1000)">1 L<small>garrafa</small></button>
    </div>
    <div class="two-c" style="margin-top:14px"><input id="customMl" type="number" min="1" max="5000" step="10" placeholder="Quantidade personalizada (ml)" aria-label="Quantidade em ml"><button class="btn" onclick="addCustom()">Adicionar</button></div>
    <button class="ghost full" style="width:100%;margin-top:10px" onclick="openWater()">Registrar com horário e foto</button>
  </div>
  <div class="card" style="margin-top:14px"><h2>Registros de hoje — <span id="wTotal"></span></h2><div id="entries"></div></div>
</section>

<!-- REMÉDIOS -->
<section id="meds" class="hidden">
  <div class="top"><div><h1>Meus medicamentos</h1><div class="sub">Você cadastra, o Hydra lembra.</div></div><button class="btn" onclick="openMed()">+ Novo</button></div>
  <div id="medList"></div>
  <div class="note">O Hydra apenas registra e lembra o que você cadastrar. Ele não recomenda medicamentos, doses ou horários, não verifica interações e não substitui a bula ou a orientação de um profissional de saúde.</div>
</section>

<!-- PROGRESSO -->
<section id="progress" class="hidden">
  <div class="top"><div><h1>Seu progresso</h1><div class="sub">Os últimos 7 dias, dia a dia.</div></div></div>
  <div class="kpis k4" id="histKpis"></div>
  <div class="card chart" style="margin-top:14px"><h2>Consumo de água</h2><div id="chartFull"></div></div>
  <div class="card" style="margin-top:14px"><h2>Detalhes por dia</h2><div id="histList"></div></div>
</section>

<!-- PERFIL -->
<section id="profile" class="hidden">
  <div class="top"><div><h1>Perfil</h1><div class="sub">Seus dados ficam só neste navegador.</div></div></div>
  <div class="grid two">
    <div class="card">
      <div style="display:flex;gap:16px;align-items:center;margin-bottom:16px">
        <div class="avatar" id="avatar">👤</div>
        <div><div style="font-weight:800;font-size:18px" id="pName"></div><div class="mut" id="pObj"></div>
        <label class="ghost" style="display:inline-block;margin-top:8px;cursor:pointer;padding:8px 12px">Trocar foto<input type="file" id="photoIn" accept="image/*" hidden></label></div>
      </div>
      <div class="field"><label for="name">Nome</label><input id="name" maxlength="40"></div>
      <div class="two-c">
        <div class="field"><label for="weight">Peso (kg)</label><input id="weight" type="number" step="0.1" min="1" max="400"></div>
        <div class="field"><label for="height">Altura (cm)</label><input id="height" type="number" min="50" max="250"></div>
      </div>
      <div class="two-c">
        <div class="field"><label for="age">Idade</label><input id="age" type="number" min="1" max="120"></div>
        <div class="field"><label for="manualGoal">Meta diária de água (ml)</label><input id="manualGoal" type="number" min="250" max="8000" step="50"></div>
      </div>
      <div class="field"><label for="activity">Atividade física</label><select id="activity"><option value="low">Leve (pouco exercício)</option><option value="moderate">Moderada (3 a 4x por semana)</option><option value="high">Intensa (5x ou mais, ou treino pesado)</option></select></div>
<button type="button" class="ghost full" style="width:100%;margin-bottom:10px" onclick="calcGoal()">💧 Calcular minha meta de água</button>
<div id="goalCalc" class="alert hidden" style="flex-direction:column"></div>
<div class="field"><label for="objective">Objetivo</label><input id="objective" maxlength="80" placeholder="Ex.: manter a pele hidratada"></div>
      <div class="field"><label for="extra">Outras informações (opcional)</label><textarea id="extra" rows="2" maxlength="300"></textarea></div>
      <button class="btn full" onclick="saveProfile()">Salvar perfil</button>
      <div class="note">A meta é sua: o cálculo é só uma estimativa geral e você escolhe se quer usá-la.</div>
    </div>
    <div class="grid">
      <div class="card"><h2>Meu progresso</h2><div class="kpis" id="pKpis"></div></div>
      <div class="card"><h2>⏰ Lembretes</h2>
        <div class="tg"><div><b>Lembrar de beber água</b><div class="note" style="margin:2px 0 0">Funcionam com o app aberto.</div></div><button class="sw" id="swWater" onclick="toggleRem('enabled')" aria-label="Lembretes de água"><i></i></button></div>
        <div class="tg"><div><b>Lembrar dos medicamentos</b></div><button class="sw" id="swMed" onclick="toggleRem('medEnabled')" aria-label="Lembretes de medicamentos"><i></i></button></div>
        <div class="tg"><div><b>Notificações do navegador</b></div><button class="sw" id="swNotif" onclick="toggleNotif()" aria-label="Notificações"><i></i></button></div>
<div class="tg"><div><b>Avisos com o app fechado (push)</b><div class="note" style="margin:2px 0 0">Exige o servidor configurado no Netlify.</div></div><button class="sw" id="swPush" onclick="togglePush()" aria-label="Push com app fechado"><i></i></button></div>
        <div class="tg"><div><b>Som</b></div><button class="sw" id="swSound" onclick="toggleRem('sound')" aria-label="Som"><i></i></button></div>
        <div class="two-c" style="margin-top:12px">
          <div class="field"><label for="interval">Intervalo (água)</label><select id="interval"><option value="30">30 min</option><option value="45">45 min</option><option value="60">1 hora</option><option value="90">1h30</option><option value="120">2 horas</option></select></div>
          <div class="field"><label>Próximo lembrete</label><div id="nextRem" style="padding:13px 0;font-weight:700"></div></div>
        </div>
        <div class="two-c"><div class="field"><label for="startT">Começa às</label><input id="startT" type="time"></div><div class="field"><label for="endT">Termina às</label><input id="endT" type="time"></div></div>
        <button class="ghost" style="width:100%" onclick="saveRem()">Salvar horários</button>
      </div>
      <div class="card"><h2>Dados</h2>
        <button class="ghost" style="width:100%;margin-bottom:8px" onclick="exportData()">Exportar meus dados (JSON)</button>
<button class="ghost" style="width:100%;margin-bottom:8px" onclick="exportICS()">Exportar horários para a agenda (.ics)</button>
        <button class="ghost danger" style="width:100%" onclick="clearAll()">Apagar todos os dados</button></div>
    </div>
  </div>
</section>
</main>

<!-- MODAIS -->
<div class="modal" id="mWater" role="dialog" aria-modal="true" aria-label="Adicionar água"><div class="box">
  <div class="mh"><b style="font-size:18px">Adicionar água</b><button class="close" onclick="closeModals()" aria-label="Fechar">×</button></div>
  <div class="field"><label for="wAmount">Quantidade (ml)</label><input id="wAmount" type="number" min="1" max="5000" step="10" placeholder="Ex.: 300"></div>
  <div class="field"><label for="wTime">Horário</label><input id="wTime" type="time"></div>
  <div class="field"><label for="wPhoto">Foto (opcional)</label><input id="wPhoto" type="file" accept="image/*"></div>
  <button class="btn full" onclick="saveWater()">Adicionar ao dia</button>
</div></div>

<div class="modal" id="mMed" role="dialog" aria-modal="true" aria-label="Medicamento"><div class="box">
  <div class="mh"><b style="font-size:18px" id="mMedTitle">Novo medicamento</b><button class="close" onclick="closeModals()" aria-label="Fechar">×</button></div>
  <div class="field"><label for="mName">Nome</label><input id="mName" maxlength="60" placeholder="Ex.: Vitamina D"></div>
  <div class="two-c">
    <div class="field"><label for="mDose">Dose / apresentação</label><input id="mDose" maxlength="40" placeholder="Como está na sua receita"></div>
    <div class="field"><label for="mTimes">Horários</label><input id="mTimes" placeholder="Ex.: 08:00, 20:00"></div>
  </div>
  <div class="field"><label>Dias da semana</label><div class="days" id="mDays"></div></div>
  <div class="field"><label for="mNotes">Observação</label><input id="mNotes" maxlength="120"></div>
  <div class="tg"><b>Ativo (gera lembretes)</b><button class="sw on" id="mActive" onclick="this.classList.toggle('on')" aria-label="Ativo"><i></i></button></div>
  <button class="btn full" style="margin-top:14px" onclick="saveMed()">Salvar</button>
  <button class="ghost danger hidden" id="mDel" style="width:100%;margin-top:8px" onclick="delMed()">Excluir medicamento</button>
</div></div>
<div class="toast" id="toast" role="status"></div>

<script>
const KEY='hydra_data_v1', DAYS=['Dom','Seg','Ter','Qua','Qui','Sex','Sáb'], $=id=>document.getElementById(id);
const defData=()=>({profile:{name:'',sex:'female',age:'',weight:'',height:'',activity:'moderate',goalMode:'manual',manualGoal:2500,objective:'',extra:'',photo:''},
 drinks:[],medications:[],medLogs:{},snooze:{},reminders:{enabled:false,medEnabled:true,notifications:false,sound:true,interval:60,start:'08:00',end:'22:00'}});
const uid=()=>Date.now().toString(36)+Math.random().toString(36).slice(2,7);
const pad=n=>String(n).padStart(2,'0');
let data=load(), editingMed=null, photoData='', timer=null, toastT;

function load(){
  try{
    const raw=JSON.parse(localStorage.getItem(KEY)||'null'), b=defData();
    if(!raw)return b;
    const d={...b,...raw,profile:{...b.profile,...raw.profile},reminders:{...b.reminders,...raw.reminders}};
    // migração: medicamentos do formato antigo (horários em texto) para o novo
    d.medications=(d.medications||[]).map(m=>({id:m.id||uid(),name:m.name||'Sem nome',dose:m.dose||'',
      times:Array.isArray(m.times)?m.times:(parseTimes(m.times||'').list||[]),days:m.days||[0,1,2,3,4,5,6],notes:m.notes||'',active:m.active!==false}));
    return d;
  }catch(e){return defData()}
}
function save(){syncPush();try{localStorage.setItem(KEY,JSON.stringify(data))}catch(e){toast('Sem espaço para salvar. Remova fotos antigas.')}}
const dkey=(d=new Date())=>`${d.getFullYear()}-${pad(d.getMonth()+1)}-${pad(d.getDate())}`;
const hhmm=(d=new Date())=>pad(d.getHours())+':'+pad(d.getMinutes());
const tmin=t=>{const [h,m]=t.split(':').map(Number);return h*60+m};
const nowMin=()=>tmin(hhmm());
const ml=n=>Number(n).toLocaleString('pt-BR')+' ml';
const esc=s=>String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const goal=()=>Number(data.profile.manualGoal)>0?Number(data.profile.manualGoal):2500;
const totalOn=k=>data.drinks.filter(x=>x.date===k).reduce((s,x)=>s+Number(x.amount),0);
const lastDays=n=>Array.from({length:n},(_,i)=>{const d=new Date();d.setDate(d.getDate()-(n-1-i));return d});

function toast(m){const t=$('toast');t.textContent=m;t.classList.add('show');clearTimeout(toastT);toastT=setTimeout(()=>t.classList.remove('show'),2400)}

/* navegação */
function go(p){
  if(!$(p))p='home';
  document.querySelectorAll('main>section').forEach(s=>s.classList.toggle('hidden',s.id!==p));
  document.querySelectorAll('#nav button').forEach(b=>{b.classList.toggle('on',b.dataset.p===p);b.dataset.p===p?b.setAttribute('aria-current','page'):b.removeAttribute('aria-current')});
  if(location.hash!=='#'+p)history.replaceState(null,'','#'+p);
  window.scrollTo(0,0);const sec=$(p);sec.classList.remove('enter');void sec.offsetWidth;sec.classList.add('enter');render();
}
document.querySelectorAll('#nav button').forEach(b=>b.onclick=()=>go(b.dataset.p));

/* medicamentos: doses do dia */
function slotsToday(){
  const wd=new Date().getDay(),k=dkey(),out=[];
  data.medications.filter(m=>m.active&&m.days.includes(wd)).forEach(m=>m.times.forEach(t=>{
    const key=`${k}|${m.id}|${t}`,taken=data.medLogs[key],eff=data.snooze[key]||t;
    out.push({m,t,key,taken,eff,st:taken?'taken':tmin(eff)<nowMin()?'late':'pending'});
  }));
  return out.sort((a,b)=>tmin(a.eff)-tmin(b.eff));
}
function parseTimes(s){
  const parts=s.split(/[,;\s]+/).filter(Boolean),list=[];
  for(const p of parts){const m=p.match(/^([01]?\d|2[0-3]):([0-5]\d)$/);if(!m)return{error:p};list.push(pad(m[1])+':'+m[2])}
  return{list:[...new Set(list)].sort()};
}
function takeSlot(key){
  if(data.medLogs[key])delete data.medLogs[key];else{data.medLogs[key]=hhmm();delete data.snooze[key]}
  save();render();toast(data.medLogs[key]?'Registrado como tomado ✓':'Registro desfeito.');
}
function snoozeSlot(key,t){
  const base=Math.max(nowMin(),tmin(data.snooze[key]||t))+15;
  if(base>=1440){toast('Não é possível adiar para depois da meia-noite.');return}
  data.snooze[key]=pad(Math.floor(base/60))+':'+pad(base%60);
  save();render();toast('Adiado para '+data.snooze[key]+' ⏰');
}
const pill=st=>({taken:'<span class="pill p-taken">Tomado</span>',late:'<span class="pill p-late">Atrasado</span>',pending:'<span class="pill p-pending">Pendente</span>'}[st]);

/* água */
function addDrink(amount,time,photo){
  amount=Number(amount);
  if(!(amount>=1&&amount<=5000)){toast('Informe entre 1 e 5000 ml.');return false}
  data.drinks.push({id:uid(),date:dkey(),amount,time:time||hhmm(),photo:photo||'',created:Date.now()});
  save();render();toast(`+ ${ml(amount)} registrados 💧`);return true;
}
function addCustom(){const v=$('customMl').value;if(addDrink(v))$('customMl').value=''}
function delDrink(id){if(!confirm('Remover este registro?'))return;data.drinks=data.drinks.filter(x=>x.id!==id);save();render()}
function openWater(){$('wAmount').value='';$('wTime').value=hhmm();$('wPhoto').value='';photoData='';$('mWater').classList.add('show');setTimeout(()=>$('wAmount').focus(),80)}
function saveWater(){if(addDrink($('wAmount').value,$('wTime').value,photoData))closeModals()}
function resizeImg(file,size,cb){
  const r=new FileReader();r.onload=()=>{const im=new Image();im.onload=()=>{
    const s=Math.min(1,size/Math.max(im.width,im.height)),c=document.createElement('canvas');
    c.width=im.width*s;c.height=im.height*s;c.getContext('2d').drawImage(im,0,0,c.width,c.height);cb(c.toDataURL('image/jpeg',.75))};
    im.src=r.result};r.readAsDataURL(file);
}
$('wPhoto').onchange=e=>{const f=e.target.files[0];if(f)resizeImg(f,320,d=>photoData=d)};
$('photoIn').onchange=e=>{const f=e.target.files[0];if(f)resizeImg(f,200,d=>{data.profile.photo=d;save();render();toast('Foto atualizada.')})};

/* gráfico SVG */
function chartSvg(){
  const days=lastDays(7),g=goal(),vals=days.map(d=>totalOn(dkey(d))),max=Math.max(g,...vals)*1.1;
  const W=320,H=170,bw=28,gap=(W-bw*7)/8;
  let s=`<svg viewBox="0 0 ${W} ${H}" role="img" aria-label="Consumo de água nos últimos 7 dias"><defs><linearGradient id="bg1" x1="0" y1="1" x2="0" y2="0"><stop offset="0" stop-color="#2f7bff"/><stop offset="1" stop-color="#c04bff"/></linearGradient></defs>`;
  const gy=H-24-(g/max)*(H-44);
  s+=`<line x1="0" x2="${W}" y1="${gy}" y2="${gy}" stroke="#27c8ff" stroke-dasharray="4 4" opacity=".6"/><text x="${W}" y="${gy-4}" fill="#27c8ff" font-size="9" text-anchor="end">meta</text>`;
  days.forEach((d,i)=>{
    const h=Math.max(vals[i]/max*(H-44),vals[i]?3:0),x=gap+i*(bw+gap),y=H-24-h;
    s+=`<rect x="${x}" y="${y}" width="${bw}" height="${h}" rx="8" fill="${vals[i]>=g?'url(#bg1)':'rgba(138,92,255,.45)'}"><title>${ml(vals[i])}</title></rect>`;
    s+=`<text x="${x+bw/2}" y="${H-8}" fill="#8e97b8" font-size="10" text-anchor="middle">${DAYS[d.getDay()]}</text>`;
    if(vals[i])s+=`<text x="${x+bw/2}" y="${y-4}" fill="#f4f6ff" font-size="9" text-anchor="middle">${(vals[i]/1000).toFixed(1).replace('.',',')}</text>`;
  });
  return s+'</svg>';
}
function stats(){
  const days=lastDays(7),g=goal(),tot=days.map(d=>totalOn(dkey(d)));
  let streak=0;const d=new Date();if(totalOn(dkey(d))<g)d.setDate(d.getDate()-1);
  while(totalOn(dkey(d))>=g&&streak<3650){streak++;d.setDate(d.getDate()-1)}
  const done=days.filter((x,i)=>tot[i]>=g).length;
  return{days,tot,avg:Math.round(tot.reduce((a,b)=>a+b,0)/7),best:Math.max(...tot),done,streak};
}
const kpi=(v,l)=>`<div class="kpi"><b>${v}</b><span>${l}</span></div>`;

/* renderização */
function render(){
  const g=goal(),t=totalOn(dkey()),pct=Math.min(100,Math.round(t/g*100)),name=data.profile.name,h=new Date().getHours();
  const greet=h<12?'Bom dia':h<18?'Boa tarde':'Boa noite';
  $('greet').textContent=`${greet}${name?', '+name:''} 👋`;
  $('greetSub').textContent=t>=g?'Meta de hoje batida. Parabéns! 🎉':`Você já bebeu ${(+(t/1000).toFixed(2)).toLocaleString('pt-BR')} L de ${(+(g/1000).toFixed(2)).toLocaleString('pt-BR')} L. Vamos cuidar da sua hidratação hoje.`;
  $('today').textContent=new Date().toLocaleDateString('pt-BR',{weekday:'long',day:'2-digit',month:'long'});
  $('pct').textContent=pct+'%';
  $('ringFg').style.strokeDashoffset=326.7*(1-pct/100);
  $('cons').textContent=t.toLocaleString('pt-BR');$('goal').textContent=g.toLocaleString('pt-BR');
  $('rem').textContent=ml(Math.max(g-t,0));$('goal2').textContent=ml(g);$('cups').textContent=(t/200).toFixed(1).replace('.',',').replace(',0','');
  // próximo medicamento
  const sl=slotsToday(),pend=sl.filter(s=>!s.taken),n=pend[0];
  $('nextMed').innerHTML=n?`<div class="next"><div><div class="mut">${n.st==='late'?'Atrasado desde':'Hoje às'}</div><div class="time">${n.eff}</div><b>${esc(n.m.name)}</b>${n.m.dose?` <span class="mut">${esc(n.m.dose)}</span>`:''}</div>
    <div class="acts"><button class="ghost ok" onclick="takeSlot('${n.key}')">✓ Tomei</button><button class="ghost" onclick="snoozeSlot('${n.key}','${n.t}')">⏰ Adiar</button></div></div>`
    :`<div class="empty">${sl.length?'Tudo registrado por hoje ✓':'Nenhum medicamento para hoje.<br><a href="#meds" style="color:var(--nblue)">Cadastrar medicamento</a>'}</div>`;
  const st=stats(),taken=sl.filter(s=>s.taken).length;
  $('daySum').innerHTML=kpi(ml(t),'Água hoje')+kpi(`${taken}/${sl.length}`,'Doses registradas')+kpi(st.streak+' d','Sequência da meta')+kpi(pct+'%','Meta atingida');
  $('progMsg').textContent=`Seu progresso: ${pct}% da meta de hidratação.`;
  $('chartHome').innerHTML=chartSvg();
  // alertas
  const al=[],late=sl.filter(s=>s.st==='late');
  late.forEach(s=>al.push(['warn',`💊 ${esc(s.m.name)} estava marcado para ${s.eff}.`]));
  if(t<g)al.push(['',`💧 Faltam ${ml(g-t)} para a meta de hoje.`]);
  if(!data.reminders.enabled&&!data.reminders.medEnabled)al.push(['','⏰ Os lembretes estão desligados. Ative em Perfil.']);
  else if(!data.reminders.notifications)al.push(['','🔔 Ative as notificações em Perfil para ser avisada com o app em segundo plano.']);
  $('alerts').innerHTML=al.map(a=>`<div class="alert ${a[0]}">${a[1]}</div>`).join('')||'<div class="empty">Sem alertas. Tudo em dia ✓</div>';
  // água
  $('wTotal').textContent=ml(t);
  const es=data.drinks.filter(x=>x.date===dkey()).sort((a,b)=>b.created-a.created);
  $('entries').innerHTML=es.map(x=>`<div class="entry">${x.photo?`<img class="thumb" alt="" src="${x.photo}">`:'<div class="thumb">💧</div>'}<div class="grow"><b>${ml(x.amount)}</b><div class="mut">${esc(x.time)}</div></div><button class="x" onclick="delDrink('${x.id}')" aria-label="Remover">×</button></div>`).join('')||'<div class="empty">Nenhum registro hoje. Toque em um botão acima para começar.</div>';
  // remédios
  renderMeds(sl);
  // progresso
  $('histKpis').innerHTML=kpi(ml(st.avg),'Média diária')+kpi(ml(st.best),'Melhor dia')+kpi(st.done+'/7','Dias com meta batida')+kpi(st.streak+' dias','Sequência atual');
  $('chartFull').innerHTML=chartSvg();
  $('histList').innerHTML=st.days.slice().reverse().map((d,i)=>{const v=st.tot[6-i],p=Math.min(100,v/g*100);
    return `<div style="margin-bottom:14px"><div class="row" style="border:0;padding:0 0 6px"><span>${i===0?'Hoje':d.toLocaleDateString('pt-BR',{weekday:'long',day:'2-digit',month:'2-digit'})}</span><b>${(v/1000).toFixed(1).replace('.',',')} L ${v>=g?'✓':''}</b></div><div style="height:9px;border-radius:9px;background:rgba(255,255,255,.08);overflow:hidden"><div style="height:100%;width:${p}%;background:var(--grad2);border-radius:9px;transition:width .6s"></div></div></div>`}).join('');
  // perfil
  const p=data.profile;
  $('pName').textContent=p.name||'Seu nome';$('pObj').textContent=p.objective||'Defina seu objetivo';
  $('avatar').innerHTML=p.photo?`<img alt="Foto de perfil" src="${p.photo}">`:'👤';
  $('pKpis').innerHTML=kpi(ml(t),'💧 Água hoje')+kpi(`${taken}/${sl.length}`,'💊 Remédios registrados')+kpi(st.streak,'🔥 Dias consecutivos')+kpi(ml(st.avg),'📊 Média semanal');
  renderRem();
}
function renderMeds(sl){
  const ms=data.medications;
  $('medList').innerHTML=ms.map(m=>{
    const mine=sl.filter(s=>s.m.id===m.id);
    const days=m.days.length===7?'Todos os dias':m.days.map(d=>DAYS[d]).join(', ');
    return `<div class="card med"><div class="med-h"><div><b style="font-size:17px">💊 ${esc(m.name)}</b> ${m.active?'':'<span class="pill p-off">Pausado</span>'}
      <div class="mut">${[m.dose&&esc(m.dose),days,m.notes&&esc(m.notes)].filter(Boolean).join(' · ')}</div></div>
      <button class="ghost" onclick="openMed('${m.id}')">✏️ Editar</button></div>
      ${mine.map(s=>`<div class="slot ${s.taken?'done':''}"><div><b>${s.eff}</b>${s.eff!==s.t?` <span class="mut">(adiado de ${s.t})</span>`:''} ${pill(s.st)}${s.taken?` <span class="mut">às ${s.taken}</span>`:''}</div>
        <div class="acts"><button class="ghost ${s.taken?'':'ok'}" onclick="takeSlot('${s.key}')">${s.taken?'Desfazer':'✓ Tomei'}</button>${s.taken?'':`<button class="ghost" onclick="snoozeSlot('${s.key}','${s.t}')">⏰ Adiar</button>`}</div></div>`).join('')
        ||`<div class="mut" style="padding-top:6px">${m.active?'Sem dose prevista para hoje.':'Pausado: sem lembretes.'} Horários: ${m.times.join(', ')||'—'}</div>`}</div>`;
  }).join('')||'<div class="card empty">Nenhum medicamento cadastrado.<br>Toque em “+ Novo” para começar.</div>';
}

/* medicamentos: modal */
function openMed(id){
  editingMed=id||null;const m=data.medications.find(x=>x.id===id)||{name:'',dose:'',times:[],days:[0,1,2,3,4,5,6],notes:'',active:true};
  $('mMedTitle').textContent=id?'Editar medicamento':'Novo medicamento';
  $('mName').value=m.name;$('mDose').value=m.dose;$('mTimes').value=m.times.join(', ');$('mNotes').value=m.notes;
  $('mActive').classList.toggle('on',m.active);$('mDel').classList.toggle('hidden',!id);
  $('mDays').innerHTML=DAYS.map((d,i)=>`<button type="button" class="day ${m.days.includes(i)?'on':''}" onclick="this.classList.toggle('on')" data-d="${i}">${d}</button>`).join('');
  $('mMed').classList.add('show');setTimeout(()=>$('mName').focus(),80);
}
function saveMed(){
  const name=$('mName').value.trim(),pt=parseTimes($('mTimes').value),days=[...document.querySelectorAll('#mDays .on')].map(b=>+b.dataset.d);
  if(!name)return toast('Informe o nome do medicamento.');
  if(pt.error)return toast(`Horário inválido: “${pt.error}”. Use o formato 08:00.`);
  if(!pt.list.length)return toast('Informe ao menos um horário, como 08:00.');
  if(!days.length)return toast('Escolha ao menos um dia da semana.');
  const m={id:editingMed||uid(),name,dose:$('mDose').value.trim(),times:pt.list,days,notes:$('mNotes').value.trim(),active:$('mActive').classList.contains('on')};
  const i=data.medications.findIndex(x=>x.id===editingMed);
  if(i>=0)data.medications[i]=m;else data.medications.push(m);
  save();closeModals();render();toast('Medicamento salvo.');
}
function delMed(){
  if(!confirm('Excluir este medicamento e seus lembretes?'))return;
  data.medications=data.medications.filter(m=>m.id!==editingMed);save();closeModals();render();toast('Medicamento excluído.');
}
function closeModals(){document.querySelectorAll('.modal').forEach(m=>m.classList.remove('show'))}
document.querySelectorAll('.modal').forEach(m=>m.addEventListener('click',e=>{if(e.target===m)closeModals()}));
document.addEventListener('keydown',e=>{if(e.key==='Escape')closeModals()});

/* perfil */
function fillProfile(){for(const id of ['name','weight','height','age','activity','manualGoal','objective','extra'])$(id).value=data.profile[id]??''}
function saveProfile(){
  const v=id=>$(id).value.trim(),g=Number(v('manualGoal'));
  if(g&&(g<250||g>8000))return toast('A meta deve ficar entre 250 e 8000 ml.');
  if(v('weight')&&(+v('weight')<1||+v('weight')>400))return toast('Confira o peso informado.');
  if(v('height')&&(+v('height')<50||+v('height')>250))return toast('Confira a altura informada.');
  for(const id of ['name','weight','height','age','activity','objective','extra'])data.profile[id]=v(id);
  data.profile.manualGoal=g||2500;data.profile.goalMode='manual';
  save();render();toast('Perfil salvo ✓');
  if(+v('weight')>=20&&+v('age')>=18)calcGoal(true);
}

/* cálculo da meta de água */
function calcGoal(quiet){
  const w=+$('weight').value,a=+$('age').value,act=$('activity').value,box=$('goalCalc');
  if(!(w>=20&&w<=400))return quiet||toast('Informe seu peso para calcular.');
  if(!(a>=1&&a<=120))return quiet||toast('Informe sua idade para calcular.');
  if(a<18){box.classList.remove('hidden');box.textContent='O cálculo automático é para adultos. Para menores de 18 anos, peça orientação a um profissional de saúde.';return}
  const per=a<30?40:a<=55?35:a<=65?30:25,add={low:0,moderate:350,high:700}[act]||0;
  const val=Math.min(5000,Math.max(1500,Math.round((w*per+add)/50)*50)),same=val===goal();
  box.classList.remove('hidden');
  box.innerHTML=`<div><b>Você precisa de cerca de ${(val/1000).toLocaleString('pt-BR',{minimumFractionDigits:1,maximumFractionDigits:2})} litros de água por dia</b> (${val.toLocaleString('pt-BR')} ml, ou cerca de ${Math.round(val/200)} copos de 200 ml)</div>
  <div class="mut">${w} kg × ${per} ml${add?` + ${add} ml pela atividade`:''}. Estimativa geral para adultos saudáveis, com base em peso, idade e atividade. Não substitui orientação médica: com doença renal ou cardíaca, ou restrição de líquidos, siga o que seu médico indicar.</div>
  ${same?'<div class="mut">Sua meta atual já é igual a esta estimativa. ✓</div>':`<button type="button" class="btn" onclick="applyGoal(${val})">Usar esta meta</button>`}`;
}
function applyGoal(v){$('manualGoal').value=v;saveProfile();$('goalCalc').classList.add('hidden')}

/* lembretes */
function renderRem(){
  const r=data.reminders;
  $('swWater').classList.toggle('on',r.enabled);$('swMed').classList.toggle('on',r.medEnabled);$('swSound').classList.toggle('on',r.sound);$('swPush').classList.toggle('on',!!r.push);
  $('swNotif').classList.toggle('on',r.notifications&&'Notification' in window&&Notification.permission==='granted');
  if(document.activeElement.id!=='interval')$('interval').value=r.interval;
  if(document.activeElement.id!=='startT')$('startT').value=r.start;
  if(document.activeElement.id!=='endT')$('endT').value=r.end;
  const nw=r.enabled?waterSchedule().find(t=>tmin(t)>nowMin()):null,nm=r.medEnabled?slotsToday().find(s=>!s.taken):null;
  const c=[nw&&`💧 ${nw}`,nm&&`💊 ${nm.eff}`].filter(Boolean);
  $('nextRem').textContent=c.join('  ·  ')||'—';
}
function toggleRem(k){data.reminders[k]=!data.reminders[k];save();renderRem();toast(data.reminders[k]?'Ativado.':'Desativado.')}
async function toggleNotif(){
  const r=data.reminders;
  if(r.notifications){r.notifications=false;save();renderRem();return toast('Notificações desativadas.')}
  if(!('Notification' in window))return toast('Este navegador não oferece notificações.');
  let p=Notification.permission;if(p==='default')p=await Notification.requestPermission();
  r.notifications=p==='granted';save();renderRem();
  toast(p==='granted'?'Notificações permitidas ✓':'Permissão negada. Libere nas configurações do navegador.');
}
function saveRem(){
  const s=$('startT').value,e=$('endT').value;
  if(!s||!e||tmin(e)<tmin(s))return toast('O horário final deve ser depois do inicial.');
  Object.assign(data.reminders,{interval:+$('interval').value,start:s,end:e});save();renderRem();toast('Horários salvos ✓');
}
function waterSchedule(){const r=data.reminders,out=[];for(let m=tmin(r.start);m<=tmin(r.end);m+=r.interval)out.push(pad(Math.floor(m/60))+':'+pad(m%60));return out}
function beep(){
  if(!data.reminders.sound)return;
  try{const a=new (window.AudioContext||window.webkitAudioContext)(),o=a.createOscillator(),g=a.createGain();o.connect(g);g.connect(a.destination);
    o.frequency.value=660;g.gain.setValueAtTime(.15,a.currentTime);g.gain.exponentialRampToValueAtTime(.001,a.currentTime+.5);o.start();o.stop(a.currentTime+.5)}catch(e){}
}
function notify(title,body){
  toast(title);beep();
  if(data.reminders.notifications&&'Notification' in window&&Notification.permission==='granted'){try{new Notification(title,{body})}catch(e){}}
}
function checkReminders(){
  const r=data.reminders,hm=hhmm(),k=dkey();
  let fired=JSON.parse(localStorage.getItem('hydra_fired')||'{}');if(fired.day!==k)fired={day:k,keys:[]};
  const once=id=>{if(fired.keys.includes(id))return false;fired.keys.push(id);localStorage.setItem('hydra_fired',JSON.stringify(fired));return true};
  if(r.medEnabled)slotsToday().filter(s=>!s.taken&&nowMin()-tmin(s.eff)>=0&&nowMin()-tmin(s.eff)<=5).forEach(s=>{if(once('m'+s.key+s.eff))notify('💊 Hora do seu medicamento',`${s.m.name}${s.m.dose?' — '+s.m.dose:''}`)});
  if(r.enabled&&waterSchedule().includes(hm)&&once('w'+hm))notify('💧 Está na hora de beber água','Registre no Hydra depois de beber.');
}
setInterval(checkReminders,20000);
setInterval(()=>{if(!document.hidden)render()},60000);

/* dados */
function exportData(){const u=URL.createObjectURL(new Blob([JSON.stringify(data,null,2)],{type:'application/json'})),a=document.createElement('a');a.href=u;a.download='hydra-dados.json';a.click();setTimeout(()=>URL.revokeObjectURL(u),1000)}
function clearAll(){if(!confirm('Isso apaga perfil, histórico, medicamentos e lembretes. Continuar?'))return;localStorage.removeItem(KEY);localStorage.removeItem('hydra_fired');location.reload()}

/* push (app fechado) + agenda */
const FN='/.netlify/functions/';
const b64=s=>{const r=atob((s+'='.repeat((4-s.length%4)%4)).replace(/-/g,'+').replace(/_/g,'/'));return Uint8Array.from(r,c=>c.charCodeAt(0))};
if('serviceWorker' in navigator)navigator.serviceWorker.register('sw.js').catch(()=>{});
let syncT;
function syncPush(){
  clearTimeout(syncT);
  syncT=setTimeout(async()=>{
    if(!data.reminders.push)return;
    try{
      const reg=await navigator.serviceWorker.ready,sub=await reg.pushManager.getSubscription();if(!sub)return;
      const k=dkey();
      await fetch(FN+'push-sync',{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({sub,tz:Intl.DateTimeFormat().resolvedOptions().timeZone,meds:data.medications.filter(m=>m.active),logs:Object.keys(data.medLogs).filter(x=>x.startsWith(k)),snooze:data.snooze,medEnabled:data.reminders.medEnabled})});
    }catch(e){}
  },800);
}
async function togglePush(){
  const r=data.reminders;
  if(r.push){
    try{const reg=await navigator.serviceWorker.ready,sub=await reg.pushManager.getSubscription();
      if(sub){await fetch(FN+'push-sync',{method:'DELETE',body:JSON.stringify({endpoint:sub.endpoint})});await sub.unsubscribe()}}catch(e){}
    r.push=false;save();renderRem();return toast('Push desativado.');
  }
  if(!('serviceWorker' in navigator)||!('PushManager' in window))return toast('Sem suporte a push. No iPhone, instale o app na tela inicial.');
  try{
    if(await Notification.requestPermission()!=='granted')return toast('Permissão negada.');
    const reg=await navigator.serviceWorker.ready,{key}=await (await fetch(FN+'push-key')).json();
    if(!key)throw new Error('sem chave');
    await reg.pushManager.subscribe({userVisibleOnly:true,applicationServerKey:b64(key)});
    r.push=true;save();renderRem();syncPush();toast('Push ativado ✓');
  }catch(e){toast('Não foi possível ativar o push. Confira a configuração do servidor.')}
}
function exportICS(){
  const wd=['SU','MO','TU','WE','TH','FR','SA'],stamp=new Date().toISOString().replace(/[-:]/g,'').slice(0,15)+'Z',k=dkey().replace(/-/g,''),ev=[];
  data.medications.filter(m=>m.active).forEach(m=>m.times.forEach(t=>{
    const hm=t.replace(':','')+'00';
    ev.push(['BEGIN:VEVENT',`UID:${m.id}-${hm}@hydra`,`DTSTAMP:${stamp}`,`DTSTART:${k}T${hm}`,`DTEND:${k}T${hm}`,`RRULE:FREQ=WEEKLY;BYDAY=${m.days.map(d=>wd[d]).join(',')}`,`SUMMARY:💊 ${m.name.replace(/[,;\r\n]/g,' ')}`,'BEGIN:VALARM','ACTION:DISPLAY','DESCRIPTION:Hora do medicamento','TRIGGER:PT0S','END:VALARM','END:VEVENT'].join('\r\n'));
  }));
  if(!ev.length)return toast('Nenhum medicamento ativo para exportar.');
  const txt=['BEGIN:VCALENDAR','VERSION:2.0','PRODID:-//Hydra//PT','CALSCALE:GREGORIAN',...ev,'END:VCALENDAR'].join('\r\n');
  const u=URL.createObjectURL(new Blob([txt],{type:'text/calendar'})),a=document.createElement('a');
  a.href=u;a.download='hydra-medicamentos.ics';a.click();setTimeout(()=>URL.revokeObjectURL(u),1000);
  toast('Abra o arquivo para importar na sua agenda.');
}
document.addEventListener('visibilitychange',()=>{if(!document.hidden)checkReminders()});

fillProfile();
go((location.hash||'#home').slice(1));
window.addEventListener('hashchange',()=>go(location.hash.slice(1)));

document.addEventListener('pointerdown',e=>{
  const b=e.target.closest('.btn,.ghost,.day,#nav button,.close');if(!b)return;
  const r=b.getBoundingClientRect(),d=Math.max(r.width,r.height),x=document.createElement('span');
  x.className='rip';x.style.cssText=`width:${d}px;height:${d}px;left:${e.clientX-r.left-d/2}px;top:${e.clientY-r.top-d/2}px`;
  b.appendChild(x);setTimeout(()=>x.remove(),650);
});
</script>
</body>
</html>

{"name":"Hydra — Água e Medicamentos","short_name":"Hydra","start_url":"./","scope":"./","display":"standalone","background_color":"#05060f","theme_color":"#05060f","icons":[{"src":"icon-192.png","sizes":"192x192","type":"image/png"},{"src":"icon-512.png","sizes":"512x512","type":"image/png","purpose":"any maskable"}]}


[build]
  publish = "."

[functions]
  directory = "netlify/functions"

[[headers]]
  for = "/*"
  [headers.values]
    X-Content-Type-Options = "nosniff"
    Referrer-Policy = "same-origin"

[[headers]]
  for = "/sw.js"
  [headers.values]
    Cache-Control = "no-cache"


[package.json](https://github.com/user-attachments/files/33080653/package.json)

{"name":"hydra","private":true,"type":"module","dependencies":{"@netlify/blobs":"^8.1.0","web-push":"^3.6.7"}}


[sw.js](https://github.com/user-attachments/files/33080664/sw.js)self.addEventListener('install',()=>self.skipWaiting());
self.addEventListener('activate',e=>e.waitUntil(clients.claim()));
self.addEventListener('push',e=>{
  let d={title:'Hydra',body:''};try{d=e.data.json()}catch(_){}
  e.waitUntil(self.registration.showNotification(d.title,{body:d.body,icon:'icon-192.png',badge:'icon-192.png',tag:'hydra-'+d.body,renotify:true}));
});
self.addEventListener('notificationclick',e=>{
  e.notification.close();
  e.waitUntil(clients.matchAll({type:'window'}).then(l=>l.length?l[0].focus():clients.openWindow('./#meds')));
});







