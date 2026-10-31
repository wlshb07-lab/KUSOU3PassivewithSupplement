<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=5">
<title>KUSO文法U3語態互動式文法練習網頁</title>
<style>
:root{
 --pumpkin:#F0781E; --pumpkin-d:#C9560B; --pink:#F4739C; --pink-l:#FFD8E4;
 --cream:#FFF6EA; --card:#FFFFFF; --ink:#4A2916; --ink2:#8A5A3C;
 --line:#F6D9BE; --green:#1E9E6A; --red:#D8452F;
 --sh:0 6px 18px -10px rgba(160,80,20,.55);
}
*{box-sizing:border-box;-webkit-tap-highlight-color:transparent}
html{scroll-behavior:smooth}
body{margin:0;color:var(--ink);font-size:16px;line-height:1.75;
 font-family:"Microsoft JhengHei","Heiti TC","Segoe UI",sans-serif;
 background:var(--cream);
 background-image:radial-gradient(circle at 12% 8%,rgba(244,115,156,.18),transparent 42%),
   radial-gradient(circle at 88% 20%,rgba(240,120,30,.18),transparent 45%),
   radial-gradient(circle at 50% 92%,rgba(255,196,87,.20),transparent 50%);
 background-attachment:fixed}
h1,h2,h3{line-height:1.35;margin:0}
.wrap{max-width:900px;margin:0 auto;padding:0 14px}

header{position:sticky;top:0;z-index:40;
 background:linear-gradient(100deg,var(--pumpkin),var(--pink));color:#fff;
 box-shadow:0 3px 14px -6px rgba(120,50,10,.6)}
.bar{max-width:900px;margin:0 auto;padding:8px 14px;display:flex;align-items:center;gap:10px}
.brand{font-size:15px;font-weight:700;flex:1;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.menuBtn{background:rgba(255,255,255,.22);color:#fff;border:1.5px solid rgba(255,255,255,.75);
 border-radius:999px;padding:7px 14px;font-size:14px;font-weight:700;cursor:pointer;
 transition:transform .18s,background .18s;font-family:inherit}
.menuBtn:hover{transform:translateY(-2px);background:rgba(255,255,255,.35)}
.menuBtn:active{transform:translateY(1px)}

#backdrop{position:fixed;inset:0;background:rgba(60,25,10,.35);z-index:38;display:none}
#backdrop.on{display:block}
#menu{position:absolute;left:0;right:0;top:100%;z-index:39;
 background:#fff;border-radius:0 0 18px 18px;box-shadow:0 16px 34px -14px rgba(120,50,10,.7);
 padding:10px;display:none;max-height:72vh;overflow:auto}
#menu.on{display:block;animation:drop .22s ease-out}
@keyframes drop{from{opacity:0;transform:translateY(-10px)}to{opacity:1;transform:none}}
.navItem{display:block;width:100%;text-align:left;font-family:inherit;font-size:15.5px;font-weight:700;
 color:var(--ink);background:var(--cream);border:1.5px solid var(--line);border-radius:12px;
 padding:11px 14px;margin:6px 0;cursor:pointer;transition:transform .16s,background .16s,color .16s}
.navItem:hover{transform:translateY(-2px);background:var(--pink-l)}
.navItem:active{transform:translateY(1px)}
.navItem.act{background:linear-gradient(100deg,var(--pumpkin),var(--pink));color:#fff;border-color:transparent}
.menuSep{height:1px;background:var(--line);margin:8px 4px}

#scorebar{display:none;margin:12px 0 0;background:#fff;border:2px dashed var(--pumpkin);
 border-radius:16px;padding:12px 16px;box-shadow:var(--sh)}
#scorebar.on{display:block;animation:drop .25s ease-out}
.scoreRow{display:flex;flex-wrap:wrap;gap:10px 18px;align-items:baseline}
.scoreNum{font-size:30px;font-weight:900;color:var(--pumpkin-d);display:inline-block}
.scoreNum.pop{animation:scorePop .5s ease}
@keyframes scorePop{0%{transform:scale(1)}45%{transform:scale(1.6)}100%{transform:scale(1)}}
.track{flex:1 1 100%;height:12px;background:var(--pink-l);border-radius:99px;overflow:hidden}
.track > i{display:block;height:100%;width:0;border-radius:99px;
 background:linear-gradient(90deg,var(--pumpkin),var(--pink));transition:width .5s ease}
.small{font-size:13.5px;color:var(--ink2)}

main{padding:16px 0 90px}
.pane{display:none} .pane.on{display:block;animation:fade .3s ease}
@keyframes fade{from{opacity:0;transform:translateY(8px)}to{opacity:1}}
h2{font-size:22px;font-weight:900;color:var(--pumpkin-d);margin:6px 0 4px}
h3{font-size:17.5px;font-weight:800;margin:26px 0 10px;padding:6px 12px;border-radius:10px;
 background:linear-gradient(100deg,rgba(240,120,30,.16),rgba(244,115,156,.16));
 border-left:6px solid var(--pumpkin)}
.sub{color:var(--ink2);font-size:14px;margin:0 0 14px}

.card{background:var(--card);border:1.5px solid var(--line);border-radius:16px;
 padding:16px 18px;margin:12px 0;box-shadow:var(--sh)}
.use{font-weight:800;color:var(--pumpkin-d);margin:0 0 4px;font-size:15px}
.en{color:var(--ink2);font-size:14px;margin:0 0 3px}
.zh{margin:0 0 10px}
ol.ex{margin:0;padding-left:20px} ol.ex li{margin-bottom:9px}
ol.ex b{color:var(--pumpkin-d)}
.note{display:block;font-size:13.5px;color:var(--ink2);border-left:4px solid var(--pink);
 background:rgba(255,216,228,.35);border-radius:0 8px 8px 0;padding:5px 10px;margin-top:6px}
.pumpkin{background:linear-gradient(120deg,#FFE7C9,#FFD8E4);border:1.5px solid var(--line);
 border-radius:16px;padding:14px 16px;margin:12px 0;box-shadow:var(--sh)}
.pumpkin.alt{background:linear-gradient(120deg,#FFD8E4,#FFE7C9)}
.pumpkin p{margin:4px 0;font-size:15px} .pumpkin b{color:var(--pumpkin-d)}
.arrow{color:var(--pink);font-weight:900}

.scroll{overflow-x:auto;margin:12px 0;-webkit-overflow-scrolling:touch}
table{border-collapse:collapse;width:100%;min-width:560px;background:#fff;font-size:14px;
 border-radius:12px;overflow:hidden;box-shadow:var(--sh)}
th,td{border:1px solid var(--line);padding:9px 11px;text-align:left;vertical-align:top}
thead th{background:linear-gradient(100deg,var(--pumpkin),var(--pink));color:#fff}
tbody th{background:#FFF1E0;white-space:nowrap}
td b{color:var(--pumpkin-d)}

.q{background:#fff;border:1.5px solid var(--line);border-left:7px solid var(--pink);
 border-radius:14px;padding:14px 16px;margin:12px 0;box-shadow:var(--sh);scroll-margin-top:70px}
.q.ok{border-left-color:var(--green)} .q.no{border-left-color:var(--red)}
.qn{font-weight:900;color:var(--pumpkin-d);margin-right:6px}
.stem{margin:0 0 6px} .zhq{color:var(--ink2);font-size:14px;margin:0 0 10px}
.btnRow{display:flex;flex-wrap:wrap;gap:8px;align-items:center}
.reveal,.spk{font-family:inherit;font-size:14px;font-weight:700;cursor:pointer;
 border-radius:999px;padding:9px 15px;transition:transform .16s,box-shadow .16s,background .16s}
.reveal{background:#fff;color:var(--pumpkin-d);border:2px solid var(--pumpkin)}
.reveal:hover{transform:translateY(-2px);background:var(--pumpkin);color:#fff}
.reveal:active{transform:translateY(1px)}
.spk{background:var(--pink-l);color:var(--ink);border:2px solid var(--pink)}
.spk:hover{transform:translateY(-2px)} .spk:active{transform:translateY(1px)}
.spk.mini{padding:3px 9px;font-size:12.5px;border-width:1.5px;vertical-align:middle;margin-left:4px}
.ans{display:none;margin-top:12px;background:linear-gradient(120deg,#FFF3E2,#FFE9F0);
 border:2px dashed var(--pumpkin);border-radius:12px;padding:12px 14px}
.ans.on{display:block;animation:drop .22s ease-out}
.ans .key{font-weight:900;color:var(--pumpkin-d);font-size:16px;margin:0 0 6px}
.ans .full{margin:0 0 6px;font-size:15px}
.ans .why{margin:0;font-size:14px}
.ans .why:before{content:"詳解｜";font-weight:800;color:var(--pink)}

select.blank{font-family:inherit;font-size:15px;font-weight:700;color:var(--pumpkin-d);
 background:#FFE7C9;border:2px dashed var(--pumpkin);border-radius:10px;padding:3px 6px;
 margin:2px 2px;cursor:pointer;max-width:100%;transition:transform .15s}
select.blank:hover{transform:translateY(-2px)}
select.blank.ok{background:#DFF6EA;border-color:var(--green);border-style:solid;color:#14664a}
select.blank.no{background:#FFE0DA;border-color:var(--red);border-style:solid;color:#8f2213}
.fb{display:none;margin-top:10px;border-radius:12px;padding:11px 13px;font-size:14.5px}
.fb.on{display:block;animation:drop .22s ease-out}
.fb.ok{background:#DFF6EA;border:2px solid var(--green)}
.fb.no{background:#FFE6E0;border:2px solid var(--red)}
.fb b{color:var(--pumpkin-d)}

.fcGrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:14px;margin:12px 0}
.fc{perspective:1200px;min-height:200px;cursor:pointer}
.fcIn{position:relative;width:100%;height:100%;min-height:200px;
 transition:transform .6s cubic-bezier(.35,.05,.2,1);transform-style:preserve-3d}
.fc.on .fcIn{transform:rotateY(180deg)}
.fcF,.fcB{position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;
 border-radius:16px;padding:15px 16px;border:1.5px solid var(--line);box-shadow:var(--sh);
 display:flex;flex-direction:column;gap:7px;justify-content:center}
.fcF{background:linear-gradient(130deg,#FFE7C9,#FFD8E4)}
.fcB{background:linear-gradient(130deg,#FFF6EA,#FFE0EC);transform:rotateY(180deg)}
.fcT{font-weight:900;color:var(--pumpkin-d);font-size:15px}
.fcE{margin:0;font-size:14.5px;line-height:1.6}
.fcB p{margin:0;font-size:14px}
.fcHint{font-size:12.5px;color:var(--ink2)}
.fcB .spk{align-self:flex-start;padding:7px 13px;font-size:13px}

.dlg{background:linear-gradient(120deg,#FFF6EA,#FFE9F0);border:1.5px solid var(--line);
 border-radius:12px;padding:10px 13px;margin:2px 0 4px}
.dlg .ln{margin:0 0 4px;font-size:15px;line-height:1.65}
.dlg .ln:last-child{margin-bottom:0}
.dlg .sp{display:inline-block;min-width:36px;color:var(--pink);font-weight:900}
.dlg .zhl{color:var(--ink2);font-size:14px}

.tin{font-family:inherit;font-size:15.5px;color:var(--ink);background:#FFF9F1;
 border:2px dashed var(--pumpkin);border-radius:10px;padding:8px 11px;width:100%;max-width:440px;
 margin:2px 0 8px;transition:border-color .2s,background .2s}
.tin:focus{outline:none;border-style:solid;border-color:var(--pink);background:#fff}
.tin.ok{border-style:solid;border-color:var(--green);background:#EFFBF5}
.ta{min-height:92px;max-width:100%;line-height:1.6;resize:vertical}
.sendBtn{font-family:inherit;font-size:14px;font-weight:700;cursor:pointer;border-radius:999px;
 padding:9px 16px;background:linear-gradient(100deg,var(--pumpkin),var(--pink));color:#fff;border:none;
 transition:transform .16s,filter .16s}
.sendBtn:hover{transform:translateY(-2px);filter:brightness(1.06)}
.sendBtn:active{transform:translateY(1px)}

.subBox{background:linear-gradient(130deg,#FFF3E2,#FFE0EC);border:2px solid var(--pumpkin);
 border-radius:16px;padding:15px 17px;margin:22px 0 8px;box-shadow:var(--sh)}
.subH{margin:0 0 8px;font-size:16.5px;background:none;border:none;padding:0;color:var(--pumpkin-d)}
.subList{margin:0 0 12px;padding-left:20px;font-size:14.5px}
.subList li{margin-bottom:5px}
.subRow{display:flex;flex-wrap:wrap;gap:8px;align-items:center}
.tin.sm{max-width:190px;margin:0}
.subNote{margin:10px 0 0;font-size:13px;color:var(--ink2)}

#printOverlay{display:none;position:fixed;inset:0;z-index:70;background:rgba(60,25,10,.45);overflow:auto;padding:18px}
.poInner{max-width:820px;margin:0 auto;background:#fff;border-radius:16px;padding:20px 22px;box-shadow:0 20px 44px -18px rgba(80,35,10,.8)}
.poInner h1{font-size:20px;border-bottom:3px solid var(--pumpkin);padding-bottom:6px}
.poInner h2{font-size:16px;background:#FFE7C9;padding:5px 9px;border-radius:6px;margin-top:18px;border:none}
.poInner table{min-width:0;font-size:13px}
.poBtns{display:flex;gap:8px;flex-wrap:wrap;margin-top:16px}
@media print{
  body.printing > *:not(#printOverlay){display:none !important}
  #printOverlay{position:static;background:#fff;padding:0;overflow:visible}
  .poInner{box-shadow:none;border-radius:0;padding:0;max-width:none}
  .poBtns{display:none !important}
  @page{margin:14mm}
}

#fw{position:fixed;inset:0;pointer-events:none;z-index:50}
#toast{position:fixed;left:50%;bottom:24px;transform:translate(-50%,20px);z-index:60;
 background:rgba(45,20,8,.94);color:#fff;padding:11px 20px;border-radius:999px;font-size:14.5px;
 font-weight:700;opacity:0;transition:opacity .3s,transform .3s;pointer-events:none;max-width:90vw;text-align:center}
#toast.on{opacity:1;transform:translate(-50%,0)}

@media(max-width:480px){
 body{font-size:15.5px} .brand{font-size:13px} h2{font-size:19px} h3{font-size:16px}
 .card,.q{padding:13px 13px} .scoreNum{font-size:26px}
}
@media (prefers-reduced-motion: reduce){*{animation:none !important;transition:none !important}}
</style>
</head>
<body>

<canvas id="fw"></canvas>
<div id="backdrop"></div>

<header>
 <div class="bar">
  <div class="brand">🎃 KUSO文法 U3 語態互動練習</div>
  <button class="menuBtn" id="mBtn">☰ 選單</button>
 </div>
 <div id="menu">
  <button class="navItem" data-t="t0">🎃 語態總覽與基本規則</button>
  <button class="navItem" data-t="tf">🃏 語態閃卡自學</button>
  <button class="navItem" data-t="t1">🍊 POINT 1 被動語態的各種時式</button>
  <button class="navItem" data-t="t2">🍂 POINT 2 被動語態的其他用法</button>
  <button class="navItem" data-t="t3">🌻 客觀說法句型三種變化結構與互換</button>
  <button class="navItem" data-t="t4">📐 文法選擇 25 題</button>
  <button class="navItem" data-t="t5">🧩 填空與引導式翻譯</button>
  <button class="navItem" data-t="t6">🏅 歷屆試題</button>
  <button class="navItem" data-t="t7">📚 重點回顧總複習</button>

  <div class="menuSep"></div>
  <button class="navItem" id="scoreToggle">🏆 顯示／隱藏計分列</button>
 </div>
</header>

<div class="wrap">
 <div id="scorebar">
  <div class="scoreRow">
   <div>累計總分：<span class="scoreNum" id="total">0</span> 分</div>
   <div class="small">本輪：<span id="round">0</span>/<span id="roundMax">0</span></div>
   <div class="track"><i id="bar"></i></div>
  </div>
 </div>
</div>

<main class="wrap">
<section class="pane" id="t0"><h2>語態 Voice｜總覽與基本規則</h2><p class='sub'>主動語態說「誰做了什麼」，被動語態說「什麼被怎麼了」。同一件事，換一個焦點，就換一種語態。</p>
<div class="pumpkin">
<p>🐻 小熊："Mom, where is my money?"<button class="spk mini" data-say="Mom, where is my money?">🔊</button></p>
<p>👩 媽媽："Don't worry! It is locked up in the safe."<button class="spk mini" data-say="Don't worry! It is locked up in the safe.">🔊</button></p>
<p>例句：All the money <b>is locked up</b> in the safe.（所有的錢都鎖在保險箱裡。）<button class="spk mini" data-say="All the money is locked up in the safe.">🔊</button></p>
<p class="small">解析：是誰把錢鎖在保險箱裡不重要，重要的是錢鎖在保險箱中。Who locked the money in the safe is unimportant; what matters is that the money is locked inside the safe.</p>
</div>

<div class="card">
<p class="use">文法大特寫｜什麼時候要用被動語態？</p>
<p class="en">In English, voice is divided into "active voice" and "passive voice." When a sentence carries a "passive" meaning, the verb structure used is "be-V + past participle (p.p.)". But when should the passive voice be used? The passive voice is often used when the doer of the action is unclear or unimportant. Furthermore, the passive voice is frequently used in formal documents or academic writing to maintain an objective and impartial tone.</p>
<p class="zh">在英文中，語態分為「主動語態」與「被動語態」。如果句子含有「被動」的意思時，動詞使用「be-V + 過去分詞 (p.p.)」。但到底什麼時候該使用被動語態呢？當執行動作者身份不明確，或根本不重要時，常使用被動語態。而且被動語態多用於正式文件或學術寫作中，以求論述客觀公正。</p>
</div>

<h3>POINT 1 的核心規則：主動改被動</h3>
<div class="pumpkin alt">
<p>主動句 <span class="arrow">➔</span> 主詞 + 及物動詞 + 受詞</p>
<p>被動句 <span class="arrow">➔</span> 主詞 + be-V + p.p.（過去分詞） + by + 受詞</p>
<p>Dr. Owl punished Monkey.（Dr. 奧懲罰了小猴。）<span class="arrow">➔</span> Monkey <b>was punished</b> by Dr. Owl.（小猴被 Dr. 奧處罰。）<button class="spk mini" data-say="Dr. Owl punished Monkey. Monkey was punished by Dr. Owl.">🔊</button></p>
</div>

<h3>POINT 2 被動語態的八種時式總表</h3>
<p class="sub">英文的十二種時式中，能構成被動語態的有八種。Of the twelve tenses in English, eight can form the passive voice.</p>
<div class="scroll"><table>
<thead><tr><th>時式</th><th>動詞型態</th><th>例句</th></tr></thead>
<tbody>
<tr><th>現在簡單式</th><td>is / am / are + p.p.</td><td>The house is cleaned every day.（這間房子每天都有人打掃。） <button class="spk mini" data-say="The house is cleaned every day.">🔊</button></td></tr><tr><th>過去簡單式</th><td>was / were + p.p.</td><td>Cinderella was punished yesterday.（Cinderella 昨天被處罰了。） <button class="spk mini" data-say="Cinderella was punished yesterday.">🔊</button></td></tr><tr><th>未來簡單式</th><td>will + be-V + p.p.</td><td>A ball will be held next week.（下星期將舉辦一場舞會。） <button class="spk mini" data-say="A ball will be held next week.">🔊</button></td></tr><tr><th>現在進行式</th><td>is / am / are + being + p.p.</td><td>The proposal is being discussed at the meeting.（該提案正在會議中討論。） <button class="spk mini" data-say="The proposal is being discussed at the meeting.">🔊</button></td></tr><tr><th>過去進行式</th><td>was / were + being + p.p.</td><td>All the computers were being used when I went to the computer room.（我到電腦教室時，所有的電腦都有人在使用。） <button class="spk mini" data-say="All the computers were being used when I went to the computer room.">🔊</button></td></tr><tr><th>現在完成式</th><td>has / have + been + p.p.</td><td>Their pretty evening gowns have been made by the best seamstress.（她們漂亮的禮服已經由最好的裁縫師縫製好了。） <button class="spk mini" data-say="Their pretty evening gowns have been made by the best seamstress.">🔊</button></td></tr><tr><th>過去完成式</th><td>had + been + p.p.</td><td>The housework had been done when her stepmother returned.（當她繼母回到家時，家事已經完成了。） <button class="spk mini" data-say="The housework had been done when her stepmother returned.">🔊</button></td></tr><tr><th>未來完成式</th><td>will + have been + p.p.</td><td>The computer will have been fixed by the time you come home.（你回到家時，電腦將已經修好了。） <button class="spk mini" data-say="The computer will have been fixed by the time you come home.">🔊</button></td></tr>
</tbody></table></div>
<div class="card">
<p class="use">Dr. 奧開講｜引言</p>
<p class="en">After students have a basic concept, let Dr. Owl explain the various tenses of the passive voice in detail to everyone!</p>
<p class="zh">同學們有了基本概念後，現在就讓 Dr. 奧為同學仔細說明各種被動語態的時式吧！</p>
</div>
</section>
<section class="pane" id="tf"><h2>語態閃卡自學</h2><p class='sub'>正面是例句，點一下卡片翻到背面看用法重點，再按 🔊 聽發音。</p><div class="fcGrid"><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">現在簡單式被動 Present Simple</span><p class="fcE">The house is cleaned every day.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>am / are / is + p.p.。這間房子每天都有人打掃。表現在的事實或習慣。</p><button class="spk" data-say="The house is cleaned every day.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">過去簡單式被動 Past Simple</span><p class="fcE">Cinderella was punished yesterday.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>was / were + p.p.。Cinderella 昨天被處罰了。配過去時間副詞。</p><button class="spk" data-say="Cinderella was punished yesterday.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">未來簡單式被動 Future Simple</span><p class="fcE">A ball will be held next week.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>will + be + p.p.（亦可 be going to + be + p.p.）。下星期將舉辦一場舞會。</p><button class="spk" data-say="A ball will be held next week.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">現在進行式被動 Present Continuous</span><p class="fcE">The proposal is being discussed at the meeting.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>am / are / is + being + p.p.。該提案正在會議中討論。</p><button class="spk" data-say="The proposal is being discussed at the meeting.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">過去進行式被動 Past Continuous</span><p class="fcE">All the computers were being used when I went to the computer room.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>was / were + being + p.p.。我到電腦教室時，所有的電腦都有人在使用。</p><button class="spk" data-say="All the computers were being used when I went to the computer room.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">現在完成式被動 Present Perfect</span><p class="fcE">Their pretty evening gowns have been made by the best seamstress.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>has / have + been + p.p.。她們漂亮的禮服已經由最好的裁縫師縫製好了。</p><button class="spk" data-say="Their pretty evening gowns have been made by the best seamstress.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">過去完成式被動 Past Perfect</span><p class="fcE">The housework had been done when her stepmother returned.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>had + been + p.p.。當她繼母回到家時，家事已經完成了。</p><button class="spk" data-say="The housework had been done when her stepmother returned.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">未來完成式被動 Future Perfect</span><p class="fcE">The computer will have been fixed by the time you come home.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>will + have been + p.p.。你回到家時，電腦將已經修好了。</p><button class="spk" data-say="The computer will have been fixed by the time you come home.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">助動詞被動 Modal + be + p.p.</span><p class="fcE">The problem must be handled right away.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>must / should / ought to / can / could + be + p.p.。這個問題必須馬上處理。</p><button class="spk" data-say="The problem must be handled right away.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">感官與使役動詞被動 Perception &amp; Causative</span><p class="fcE">John was heard to sing a love song to his wife.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>S + be + seen／heard + to VR（整個過程）或 V-ing（當下）；make 改被動後接 to VR。</p><button class="spk" data-say="John was heard to sing a love song to his wife.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">動名詞與不定詞被動 Gerund &amp; Infinitive</span><p class="fcE">Gina enjoys being invited to parties.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>動名詞被動 being + p.p.；不定詞被動 to be + p.p.。Gina 喜歡受邀參加派對。</p><button class="spk" data-say="Gina enjoys being invited to parties.">🔊 朗讀例句</button></div></div></div><div class="fc"><div class="fcIn"><div class="fcF"><span class="fcT">客觀說法 Impersonal Passive</span><p class="fcE">It is said that he two-timed his girlfriend.</p><span class="fcHint">👆 點卡片翻面看用法</span></div><div class="fcB"><span class="fcT">用法重點</span><p>It is + believed／reported／said／thought／rumored… + that S + V。據說他劈腿。</p><button class="spk" data-say="It is said that he two-timed his girlfriend.">🔊 朗讀例句</button></div></div></div></div></section>
<section class="pane" id="t1"><h2>POINT 1　被動語態的各種時式</h2><p class='sub'>八種時式的被動形式，差別只在 be 動詞怎麼變；p.p. 永遠不動。</p>
<h3>（一）簡單式 Simple Tense</h3>
<div class="scroll"><table>
<thead><tr><th>時式</th><th>動詞型態</th></tr></thead>
<tbody>
<tr><th>現在簡單式 Present Simple</th><td>am / are / is + p.p.</td></tr>
<tr><th>過去簡單式 Past Simple</th><td>was / were + p.p.</td></tr>
<tr><th>未來簡單式 Future Simple</th><td>will + be + p.p. ／ be going to + be + p.p.</td></tr>
</tbody></table></div>
<div class="card"><p class="use">USAGE｜簡單式被動的三個例句</p><p class="en">In passive sentences, the doer behind (them) is unimportant, so by them can be omitted.</p><p class="zh">在被動句中，後面的行為者（them）不重要，所以可將 by them 省略。</p><ol class="ex"><li>They store vegetables in the refrigerator. <span class='arrow'>➔</span> <b>Vegetables are stored in the refrigerator.</b>（他們把蔬菜存在冰箱裡。<span class='arrow'>➔</span> 蔬菜冰在冰箱裡。）<span class="note">在被動句中，後面的行為者（them）不重要，所以可將 by them 省略。</span> <button class="spk mini" data-say="They store vegetables in the refrigerator. becomes Vegetables are stored in the refrigerator.">🔊</button></li><li>Jason's girlfriend dumped him last week. <span class='arrow'>➔</span> <b>Jason was dumped by his girlfriend last week.</b>（Jason 上星期被他女朋友甩了。） <button class="spk mini" data-say="Jason&#x27;s girlfriend dumped him last week. becomes Jason was dumped by his girlfriend last week.">🔊</button></li><li>Someone will tell you how to use this machine. <span class='arrow'>➔</span> <b>You will be told how to use this machine.</b>（有人會告訴你如何使用這臺機器。） <button class="spk mini" data-say="Someone will tell you how to use this machine. becomes You will be told how to use this machine.">🔊</button></li></ol></div>
<h3>（二）進行式 Continuous Tense</h3>
<div class="scroll"><table>
<thead><tr><th>時式</th><th>動詞型態</th></tr></thead>
<tbody>
<tr><th>現在進行式 Present Continuous</th><td>am / are / is + being + p.p.</td></tr>
<tr><th>過去進行式 Past Continuous</th><td>was / were + being + p.p.</td></tr>
</tbody></table></div>
<div class="card"><p class="use">USAGE｜進行式被動的兩個例句</p><p class="en">In this sentence, who used the computer is unimportant, so by someone can be omitted. Also, in Chinese translation, it is recommended to use "Someone..." as the subject rather than translating it literally.</p><p class="zh">在本句中，電腦被誰使用並不重要，所以可將 by someone 省略。</p><ol class="ex"><li>The teacher is scolding the naughty boy now. <span class='arrow'>➔</span> <b>The naughty boy is being scolded by the teacher now.</b>（那個調皮的男孩現在正被老師責罵。） <button class="spk mini" data-say="The teacher is scolding the naughty boy now. becomes The naughty boy is being scolded by the teacher now.">🔊</button></li><li>When I went to the office, someone was using the computer. <span class='arrow'>➔</span> <b>When I went to the office, the computer was being used.</b>（當我去辦公室時，有人正在用那臺電腦。<span class='arrow'>➔</span> 當我去辦公室時，電腦正在被使用。）<span class="note">中譯時建議以「有人……」當主詞，不要翻成「電腦正在被使用著」，這樣中文句子會充滿英文的陰影。</span> <button class="spk mini" data-say="When I went to the office, someone was using the computer. becomes When I went to the office, the computer was being used.">🔊</button></li></ol></div>
<h3>（三）完成式 Perfect Tense</h3>
<div class="scroll"><table>
<thead><tr><th>時式</th><th>動詞型態</th></tr></thead>
<tbody>
<tr><th>現在完成式 Present Perfect</th><td>has / have + been + p.p.</td></tr>
<tr><th>過去完成式 Past Perfect</th><td>had + been + p.p.</td></tr>
<tr><th>未來完成式 Future Perfect</th><td>will + have been + p.p.</td></tr>
</tbody></table></div>
<div class="card"><p class="use">USAGE｜完成式被動的三個例句</p><p class="en">The passive highlights the event itself rather than who performed it, so the doer can be omitted.</p><p class="zh">被動語態中可將行為者省略，因為重點是事情本身，而不是「誰」做了這件事。</p><ol class="ex"><li>The dentist has pulled out the crocodile's tooth. <span class='arrow'>➔</span> <b>The crocodile's tooth has been pulled out (by the dentist).</b>（牙醫已經把鱷魚的牙齒拔出來了。<span class='arrow'>➔</span> 鱷魚的牙齒已經被拔出來了。）<span class="note">被動語態中可將 by the dentist 省略，因為重點是「牙齒被拔出來了」這件事情，而不是「誰」拔了鱷魚的牙齒。</span> <button class="spk mini" data-say="The dentist has pulled out the crocodile&#x27;s tooth. becomes The crocodile&#x27;s tooth has been pulled out .">🔊</button></li><li>The police had towed away my car before I returned. <span class='arrow'>➔</span> <b>My car had been towed away (by the police) before I returned.</b>（在我回來之前，警察已經把我的車拖走了。<span class='arrow'>➔</span> 當我回來時，車子已經被拖吊了。）<span class="note">改為被動時，強調的是「車子已經被拖吊」這件事情，故 by the police 可省略。</span> <button class="spk mini" data-say="The police had towed away my car before I returned. becomes My car had been towed away before I returned.">🔊</button></li><li>By the time you come back, I will have cooked dinner. <span class='arrow'>➔</span> <b>By the time you come back, dinner will have been cooked.</b>（等你回來的時候，我將已經煮好晚餐了。<span class='arrow'>➔</span> 等你回來的時候，晚餐將已經煮好了。）<span class="note">by me 可省略，因為重點是「晚餐到時已經煮好了」。</span> <button class="spk mini" data-say="By the time you come back, I will have cooked dinner. becomes By the time you come back, dinner will have been cooked.">🔊</button></li></ol></div><h3>🎯 隨堂練習｜被動的時式</h3><p class='sub'>先自己判斷，再按【📖 參考解答】對答案。</p><div class="q"><p class="stem"><span class="qn">1.</span> The Eiffel Tower ________ in 1889.（(A) is built　(B) has built　(C) had been built　(D) was built）</p><p class="zhq">艾菲爾鐵塔於 1889 年建造。</p><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">(D) was built</p><p class="full">The Eiffel Tower was built in 1889.</p><p class="why">有過去特定時間點 1889，且鐵塔是「被建造」，故用過去簡單式被動 was + p.p.。</p></div></div>
<div class="q"><p class="stem"><span class="qn">2.</span> Nowadays, hip hop ________ mostly by young people.（(A) is enjoyed　(B) has enjoyed　(C) enjoyed　(D) has been enjoying）</p><p class="zhq">現今，嘻哈音樂大多受到年輕人的喜愛。</p><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">(A) is enjoyed</p><p class="full">Nowadays, hip hop is enjoyed mostly by young people.</p><p class="why">Nowadays 表示現今的普遍事實，且嘻哈音樂是「被喜愛」，故用現在簡單式被動 is + p.p.。</p></div></div>
<div class="q"><p class="stem"><span class="qn">3.</span> By the time you return, the house ________.（(A) had been remodeled　(B) will have been remodeled　(C) will remodel　(D) has been remodeled）</p><p class="zhq">等你回來時，這棟房子將已經改建完成了。</p><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">(B) will have been remodeled</p><p class="full">By the time you return, the house will have been remodeled.</p><p class="why">By the time + 現在式（return）代替未來式，主句表「到未來某時將已完成」，且房子是「被改建」，故用未來完成式被動 will have been + p.p.。</p></div></div></section>
<section class="pane" id="t2"><h2>POINT 2　被動語態的其他用法</h2><p class='sub'>助動詞、感官與使役動詞、雙受詞、受詞補語、動名詞與不定詞、動詞片語、客觀說法、省略 by。</p><div class="card"><p class="use">（一）助動詞 Modal Verbs｜助動詞 + be + p.p.</p><p class="en">must + be + p.p. (must be...) / should, ought to + be + p.p. (should be...) / can, could + be + p.p. (can be...)</p><p class="zh">must + be + p.p. ➔ 必須被……／should、ought to + be + p.p. ➔ 應該被……／can、could + be + p.p. ➔ 可以被……</p><ol class="ex"><li>The problem <b>must be handled</b> right away.（這個問題必須馬上處理。） <button class="spk mini" data-say="The problem must be handled right away.">🔊</button></li><li>The program <b>should be banned</b>.（這個節目應該被禁播。） <button class="spk mini" data-say="The program should be banned.">🔊</button></li><li>The project <b>can be completed</b> within a week.（這個企劃一個星期內可以完成。） <button class="spk mini" data-say="The project can be completed within a week.">🔊</button></li></ol></div>
<div class="card">
<p class="use">（二）感官動詞及使役動詞 Verbs of Perception and Causative Verbs</p>
<div class="pumpkin alt">
<p><b>感官動詞被動句型</b></p>
<p>主動句：S + see / hear… + O + { VR / V-ing }</p>
<p class="small">VR 表示看到／聽到整個行動過程；V-ing 表示看到／聽到動作發生的當下。</p>
<p>被動句：S + be + { seen / heard… } + { to VR / V-ing }</p>
<p class="small">to VR 表示整個行動過程被看見／聽見（被動時原形動詞須還原加上 to）；V-ing 表示動作發生的當下被看到／聽到。</p>
<p><b>使役動詞 make 被動句型</b></p>
<p>主動句：S + make + O + VR　<span class="arrow">➔</span>　被動句：S + be + made + to VR</p>
</div>
<p class="zh">補充說明：感官動詞除了 see, hear 外，還有 listen to, feel, watch, look at, notice, observe, witness 等。</p>
<p class="zh">說明：主動語態中，若感官動詞後的動詞為 VR，改成被動句時感官動詞後接 to VR（例 1）。若感官動詞後的動詞為 V-ing，改成被動句時感官動詞後接 V-ing（例 2）。使役動詞 make 改被動句時，後接 to VR（例 3）。</p>
<ol class="ex">
<li>Everyone heard John sing a love song to his wife. <span class="arrow">➔</span> <b>John was heard to sing a love song to his wife.</b>（大家都聽到 John 對他的老婆唱歌。<span class="arrow">➔</span> John 被聽到唱歌給他老婆聽。）<button class="spk mini" data-say="Everyone heard John sing a love song to his wife. John was heard to sing a love song to his wife.">🔊</button></li>
<li>Someone saw him crying in the corner just now. <span class="arrow">➔</span> <b>He was seen crying in the corner just now.</b>（有人剛看到他在角落哭泣。<span class="arrow">➔</span> 他剛才被看到在角落哭泣。）<button class="spk mini" data-say="Someone saw him crying in the corner just now. He was seen crying in the corner just now.">🔊</button></li>
<li>Betty's mother made Betty eat vegetables. <span class="arrow">➔</span> <b>Betty was made to eat vegetables (by her mother).</b>（Betty 的媽媽逼 Betty 吃蔬菜。<span class="arrow">➔</span> Betty 被迫吃蔬菜。）<span class="note">以上三句的行為者並不重要，因此改成被動語態時可省略行為者。</span><button class="spk mini" data-say="Betty's mother made Betty eat vegetables. Betty was made to eat vegetables by her mother.">🔊</button></li>
</ol>
</div>

<div class="card">
<p class="use">（三）有兩個受詞的動詞（授與動詞） Verbs with Two Objects</p>
<p class="en">Verbs that take two objects, such as give, can use either the person or the thing as the subject when changed into the passive voice.</p>
<p class="zh">有兩個受詞的動詞，如 give，改成被動時，可以人或物當主詞。提醒：常見有兩個受詞的動詞包括 send, offer, show, pay, teach, promise, tell, lend 和 write。（詳見第一章 S + V + IO + DO 的句型）</p>
<ol class="ex">
<li>I paid Jim one thousand dollars for his painting.<br>
以人當被動句的主詞：<span class="arrow">➔</span> <b>Jim was paid one thousand dollars for his painting.</b>（Jim 被付了一千元買他的畫作。）<br>
以物當被動句的主詞：<span class="arrow">➔</span> <b>One thousand dollars was paid to Jim for his painting.</b>（一千元被付給 Jim 作為買他畫作的錢。）<button class="spk mini" data-say="Jim was paid one thousand dollars for his painting. One thousand dollars was paid to Jim for his painting.">🔊</button></li>
<li>Monkey offered Piggy hush money to keep a secret.<br>
以人當被動句的主詞：<span class="arrow">➔</span> <b>Piggy was offered hush money to keep a secret.</b>（小豬被給予封口費以保持祕密。）<br>
以物當被動句的主詞：<span class="arrow">➔</span> <b>Hush money was offered to Piggy to keep a secret.</b>（封口費被給予小豬以保持祕密。）<span class="note">以上兩個例句改為被動態後可將原本的主詞（I 和 Monkey）省略，使執行動作的主詞的重要性大幅減低。</span><button class="spk mini" data-say="Piggy was offered hush money to keep a secret. Hush money was offered to Piggy to keep a secret.">🔊</button></li>
</ol>
</div>
<div class="card"><p class="use">（四）主詞有受詞補語的被動態 Passive of S + V + O + OC</p><p class="en">Common verbs taking an object complement include believe, think, call, name, elect, choose, consider, and appoint. When changed into the passive, the object becomes the subject.</p><p class="zh">常見有受詞補語的動詞有 believe, think, call, name, elect, choose, consider, appoint（指派）。改為被動時，要以受詞為主詞。</p><ol class="ex"><li>We elected Tim our class leader. <span class='arrow'>➔</span> <b>Tim was elected our class leader.</b>（Tim 被選為我們班的班長。） <button class="spk mini" data-say="We elected Tim our class leader. becomes Tim was elected our class leader.">🔊</button></li><li>Many people consider Mt. Ali a must-see tourist attraction. <span class='arrow'>➔</span> <b>Mt. Ali is considered a must-see tourist attraction.</b>（阿里山被視為是必遊景點。） <button class="spk mini" data-say="Many people consider Mt. Ali a must-see tourist attraction. becomes Mt. Ali is considered a must-see tourist attraction.">🔊</button></li></ol></div><div class="card"><p class="use">（五）動名詞與不定詞的被動 Passive of Gerunds and Infinitives</p><p class="en">Gerund passive: being + p.p. Infinitive passive: to be + p.p.</p><p class="zh">動名詞的被動：being + p.p.；不定詞的被動：to be + p.p.。補充說明：介系詞及某些動詞（例：enjoy, escape, mind, finish, practice 等）後的動詞，一定要加 V-ing，故改被動態時變成 being + p.p.；有些動詞後面（例：want, wish, expect, desired 等）必須加 to V。</p><ol class="ex"><li>Gina enjoys <b>being invited</b> to parties.（Gina 喜歡受邀參加派對。） <button class="spk mini" data-say="Gina enjoys being invited to parties.">🔊</button></li><li>Angela is afraid of <b>being bullied</b> at school.（Angela 怕在學校被霸凌。） <button class="spk mini" data-say="Angela is afraid of being bullied at school.">🔊</button></li><li>The book is going <b>to be sold</b> next week.（那本書將於下週開賣。） <button class="spk mini" data-say="The book is going to be sold next week.">🔊</button></li></ol></div><div class="card"><p class="use">（六）動詞片語改被動 Passive of Phrasal Verbs</p><p class="en">S + be + phrasal verb (p.p.) + (by…). Never drop the preposition when changing a phrasal verb into the passive.</p><p class="zh">句型：S + be + 動詞片語（p.p.） + (by…)。常用動詞片語：laugh at ➔ laughed at（嘲笑）、put off ➔ put off（延期）、rely on ➔ relied on（依賴）、take care of ➔ taken care of（照顧）、look down on ➔ looked down on（看不起）。重要提醒：動詞片語改為被動時，千萬千萬不要漏掉了介系詞！</p><ol class="ex"><li>We can rely on James. <span class='arrow'>➔</span> <b>James can be relied on (by us).</b>（James 值得信賴。） <button class="spk mini" data-say="We can rely on James. becomes James can be relied on .">🔊</button></li><li>The mother took good care of the children. <span class='arrow'>➔</span> <b>The children were taken good care of (by the mother).</b>（那些孩子被照顧得很好。） <button class="spk mini" data-say="The mother took good care of the children. becomes The children were taken good care of .">🔊</button></li><li>Mary laughed at me. <span class='arrow'>➔</span> <b>I was laughed at by Mary.</b>（瑪莉嘲笑我。） <button class="spk mini" data-say="Mary laughed at me. becomes I was laughed at by Mary.">🔊</button></li><li>She took care of the children. <span class='arrow'>➔</span> <b>The children were taken care of by her.</b>（她照顧這些孩子。） <button class="spk mini" data-say="She took care of the children. becomes The children were taken care of by her.">🔊</button></li></ol></div><div class="card"><p class="use">（七）客觀說法 Impersonal Passive</p><p class="en">It is + { believed / reported / hoped / known / said / thought / rumored / expected / estimated } + that S + V…</p><p class="zh">句型：It is + { believed／reported／hoped／known／said／thought／rumored／expected／estimated } + that S + V…。說明：表示客觀的說法或主詞不明確時，常以「It is p.p. that……」句型來表達。</p><ol class="ex"><li><b>It is said that</b> he two-timed his girlfriend.（據說他劈腿。） <button class="spk mini" data-say="It is said that he two-timed his girlfriend.">🔊</button></li><li><b>It is rumored that</b> Harry is bankrupt.（謠傳 Harry 破產了。） <button class="spk mini" data-say="It is rumored that Harry is bankrupt.">🔊</button></li><li><b>It is hoped that</b> he will recover soon.（希望他能很快康復。） <button class="spk mini" data-say="It is hoped that he will recover soon.">🔊</button></li></ol></div><div class="card"><p class="use">（八）省略 by Omission of "by"</p><p class="en">When the subject of the active sentence is a vague general reference such as People, They, You, We, or Somebody, "by + someone" is usually omitted in the passive.</p><p class="zh">主動語態的主詞為 People, They, You, We, Somebody 等含糊地表示一般的人，變為被動語態時，常將「by + 某人」省略。</p><ol class="ex"><li>Somebody stole the money on the desk. <span class='arrow'>➔</span> <b>The money on the desk was stolen.</b>（桌上的那筆錢被偷了。） <button class="spk mini" data-say="Somebody stole the money on the desk. becomes The money on the desk was stolen.">🔊</button></li><li>We elected Bob leader of the team. <span class='arrow'>➔</span> <b>Bob was elected leader of the team.</b>（鮑伯被選為隊長。） <button class="spk mini" data-say="We elected Bob leader of the team. becomes Bob was elected leader of the team.">🔊</button></li></ol></div><h3>🎯 隨堂練習｜其他用法</h3><div class="q"><p class="stem"><span class="qn">1.</span> The concert ________ in the Taipei Arena（臺北小巨蛋）next month.（(A) will hold　(B) is being held　(C) will be held　(D) will be holding）</p><p class="zhq">演唱會將於下個月在臺北小巨蛋舉行。</p><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">(C) will be held</p><p class="full">The concert will be held in the Taipei Arena next month.</p><p class="why">next month 為未來特定時間，且演唱會是「被舉行」，故用未來簡單式被動 will be held。</p></div></div>
<div class="q"><p class="stem"><span class="qn">2.</span> Look! The cat ________ by the dog.（(A) is chasing　(B) is chased　(C) is being chased　(D) chases）</p><p class="zhq">看！貓咪正在被狗追。</p><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">(C) is being chased</p><p class="full">Look! The cat is being chased by the dog.</p><p class="why">Look! 提示動作此刻正在進行，且貓是「被追」，故用現在進行式被動 is being + p.p.。</p></div></div></section>
<section class="pane" id="t3"><h2>KUSO文法U3之客觀說法的句型三種變化結構與如何互換</h2>
<p class="sub">People say that… ／ It is said that… ／ S is said to V ／ to have p.p. ／ S was said to have p.p.　高一英文｜被動語態進階｜學測與 EMI 課程銜接教材</p>

<h3>一、先看懂一個核心概念</h3>
<div class="card">
<p class="zh">「客觀說法」就是：不說出「是誰說的」，只說「大家這樣說」。因為說話的人不重要，所以英文把 People say 改成被動的 It is said，再進一步把真正的主角搬到句首。</p>
<p class="use" style="margin-top:10px">判斷句型只要看兩個時間點</p>
<ol class="ex">
<li><b>時間點 A</b>：這個說法「什麼時候被說出來」<span class="arrow">→</span> 決定主句的 be 動詞是 is / are 還是 was / were。</li>
<li><b>時間點 B</b>：被談論的事情「什麼時候發生」<span class="arrow">→</span> 決定不定詞是 to V 還是 to have p.p.。</li>
</ol>
<p class="note">兩個時間一樣早 <span class="arrow">→</span> to V；事情比說法更早 <span class="arrow">→</span> to have p.p.</p>
</div>

<h3>二、三種句型結構變化全攻略</h3>
<div class="card"><p class="use">【句型 1】主動：主詞是 People 或 They</p><p class="en">People / They + say / believe / rumor / expect / hope + (that) + S + V.</p><div class="dlg"><p class="ln">People say that our school has the best basketball team in the city. <button class="spk mini" data-say="People say that our school has the best basketball team in the city.">🔊</button></p><p class="ln zhl">中譯：大家說我們學校有全市最強的籃球隊。</p></div><ol class="ex"><li>重點：People 只是「大家」，不是特定的人，所以不重要；that 可以省略不寫。</li><li>小提醒：hope 只能用在句型 1 和句型 2，沒有後面三種變化。</li></ol></div><div class="card"><p class="use">【句型 2】被動：用假主詞 It 開頭</p><p class="en">It is said / believed / suggested / rumored / advised / estimated / reported + that + S + V.</p><div class="dlg"><p class="ln">It is believed that eating breakfast helps students concentrate in class. <button class="spk mini" data-say="It is believed that eating breakfast helps students concentrate in class.">🔊</button></p><p class="ln zhl">中譯：一般相信吃早餐能幫助學生在課堂上專心。</p></div><ol class="ex"><li>重點：It 是「假主詞」，沒有意思，只是先站在主詞的位置；真正的主詞是後面整個 that 子句。</li><li>注意：這個 that 不能省略，省略了句子就沒有主詞了。</li></ol></div><div class="card"><p class="use">【句型 3-1】把主角搬到句首 + to V（說法和事情都在現在）</p><p class="en">S + is / am / are + said / believed / suggested / rumored / advised / estimated / reported + (not) + to + V.</p><div class="dlg"><p class="ln">Night markets are said to be the best place to taste real Taiwanese food. <button class="spk mini" data-say="Night markets are said to be the best place to taste real Taiwanese food.">🔊</button></p><p class="ln zhl">中譯：據說夜市是品嘗道地台灣美食最好的地方。</p></div><ol class="ex"><li>重點：說法是現在，事情也是現在（夜市現在就是這樣），兩個時間一樣，所以用最簡單的 to V。</li><li>對照：It is said that night markets are the best place… 兩句意思相同。</li></ol></div><div class="card"><p class="use">【句型 3-2】主角搬到句首 + to have p.p.（說法在現在，事情在過去）</p><p class="en">S + is / am / are + said / believed / suggested / rumored / advised / estimated / reported + (not) + to have + p.p.</p><div class="dlg"><p class="ln">The singer is reported to have written this song when she was only fifteen. <button class="spk mini" data-say="The singer is reported to have written this song when she was only fifteen.">🔊</button></p><p class="ln zhl">中譯：據報導這位歌手在她只有十五歲時就寫下了這首歌。</p></div><ol class="ex"><li>重點：報導是現在，但寫歌是十五歲時的事，事情比說法早，所以不定詞要「往前一格」，寫成 to have written。</li><li>對照：It is reported that the singer wrote this song when she was only fifteen.</li></ol></div>
<div class="card">
<p class="use">【句型 3-3】主角搬到句首 + was / were … to have p.p.（說法在過去，事情比說法更早）</p>
<p class="en">S + was / were + said / believed / suggested / rumored / advised / estimated / reported + (not) + to have + p.p.</p>
<p class="zh">例句（本單元指定例句）：</p>
<div class="dlg">
<p class="ln">Before modern technology unraveled its secrets and revealed the sheer power of human labor, <b>it was rumored that</b> the Great Pyramid <b>had been</b> the work of extraterrestrials.<button class="spk mini" data-say="Before modern technology unraveled its secrets and revealed the sheer power of human labor, it was rumored that the Great Pyramid had been the work of extraterrestrials.">🔊</button></p>
<p class="ln zhl">中譯：在現代科技解開金字塔的祕密、揭示人力的驚人力量之前，曾有謠傳說大金字塔是外星人的作品。</p>
<p class="ln">改成主角開頭：The Great Pyramid <b>was rumored to have been</b> the work of extraterrestrials before modern technology unraveled its secrets and revealed the sheer power of human labor.<button class="spk mini" data-say="The Great Pyramid was rumored to have been the work of extraterrestrials before modern technology unraveled its secrets and revealed the sheer power of human labor.">🔊</button></p>
</div>
<ol class="ex">
<li>重點一：句首的 Before… 告訴我們「這個謠傳是以前的事」，所以主句用過去式 was rumored。</li>
<li>重點二：that 子句用 had been，表示「金字塔是外星人蓋的」這件事被認定發生在謠傳之前，所以不定詞用 to have been。</li>
<li>重點三：不能改成 is rumored，因為科技已經解開祕密，現在沒有人這樣謠傳了。</li>
</ol>
<p class="note">關鍵區辨：句型 4 和句型 5 的不定詞長得一模一樣（to have p.p.），差別只在前面的 be 動詞。is／are 就是句型 4，was／were 就是句型 5。</p>
</div>

<div class="card">
<p class="use">【句型 3-4】It is expected / hoped / estimated / projected that S will / can + V（說法在現在，事情在未來）</p>
<p class="zh">that 子句有 will <span class="arrow">→</span> 不定詞用 to V，will 消失；有 can <span class="arrow">→</span> 改成 to be able to V。</p>
<ol class="ex">
<li>It is expected that the typhoon will hit Taiwan tomorrow. <span class="arrow">→</span> <b>The typhoon is expected to hit Taiwan tomorrow.</b>（✗ to will hit）<button class="spk mini" data-say="It is expected that the typhoon will hit Taiwan tomorrow. The typhoon is expected to hit Taiwan tomorrow.">🔊</button></li>
</ol>
</div>
<h3>三、三種不同句型結構代換或互換時要注意的位置變化（九大要點）</h3><div class="card"><p class="use">變化 1：主角要搬家（主詞提升）</p><p class="zh">句型 1 <span class='arrow'>→</span> 句型 2：主詞 People 或 They 整個不見了（因為「誰說的」不重要），that 子句整句搬到 It 的後面。句型 2 <span class='arrow'>→</span> 句型 3、4、5：that 子句裡的小主詞被搬到整句最前面，變成新主詞；原來的 It 和 that 同時消失。</p><ol class="ex"><li>People say that my uncle owns three restaurants. <span class='arrow'>→</span> It is said that my uncle owns three restaurants. <span class='arrow'>→</span> My uncle is said to own three restaurants. <button class="spk mini" data-say="People say that my uncle owns three restaurants. becomes It is said that my uncle owns three restaurants. becomes My uncle is said to own three restaurants.">🔊</button></li></ol></div><div class="card"><p class="use">變化 2：be 動詞要跟著新主詞改，時態不可以自己亂換</p><p class="zh">句型 2 的 It 固定用單數；搬家之後，be 動詞要看新主詞是單數還是複數。主句原來是 is／are，搬家後還是 is／are，所以是句型 3 或句型 4；主句原來是 was／were，搬家後還是 was／were，所以是句型 5。</p><ol class="ex"><li>It is said that the twins play the violin. <span class='arrow'>→</span> The twins are said to play the violin.（不可寫 The twins is） <button class="spk mini" data-say="It is said that the twins play the violin. becomes The twins are said to play the violin.">🔊</button></li></ol></div><div class="card"><p class="use">變化 3：that 子句的動詞變成不定詞，由不定詞負責表達時間差</p><p class="zh">動詞搬進不定詞之後就沒有時態了，所以要用不定詞的形式來表示「跟說法比起來，誰先誰後」。(1) 事情和說法同時 → to V。(2) 事情比說法早 → to have p.p.。(3) 事情是「正在進行」→ to be V-ing（同時）／to have been V-ing（更早）。(4) 事情是「被動」→ to be p.p.（同時）／to have been p.p.（更早）。</p><ol class="ex"><li>It is believed that the temple was built in 1890. <span class='arrow'>→</span> The temple is believed to have been built in 1890. <button class="spk mini" data-say="It is believed that the temple was built in 1890. becomes The temple is believed to have been built in 1890.">🔊</button></li></ol></div><div class="card"><p class="use">變化 4：not 要移到 to 的前面</p><p class="zh">句型 2 的 not 放在 that 子句的動詞前面；搬家之後，not 必須放在 to 的前面，寫成 not to V 或 not to have p.p.。常見錯誤：寫成 He is not said to eat meat.，意思會變成「沒有人說他吃肉」，跟原意不一樣。never 的處理方式跟 not 一樣，也要放在 to 前面：is said never to eat meat。</p><ol class="ex"><li>It is said that he does not eat meat. <span class='arrow'>→</span> He is said not to eat meat. <button class="spk mini" data-say="It is said that he does not eat meat. becomes He is said not to eat meat.">🔊</button></li></ol></div><div class="card"><p class="use">變化 5：時間副詞要跟事情配對</p><p class="zh">表過去的時間副詞（last year、in 2010、two days ago、before…）只能配 to have p.p.；表現在或未來的（now、next week、tomorrow）只能配 to V。</p><ol class="ex"><li>The team is said to have won the championship last year.（✗ is said to win … last year） <button class="spk mini" data-say="The team is said to have won the championship last year.">🔊</button></li></ol></div><div class="card"><p class="use">變化 6：will 和 can 的處理</p><p class="zh">that 子句有 will <span class='arrow'>→</span> 不定詞用 to V，will 消失；有 can <span class='arrow'>→</span> 改成 to be able to V。</p><ol class="ex"><li>It is expected that the typhoon will hit Taiwan tomorrow. <span class='arrow'>→</span> The typhoon is expected to hit Taiwan tomorrow.（✗ to will hit） <button class="spk mini" data-say="It is expected that the typhoon will hit Taiwan tomorrow. becomes The typhoon is expected to hit Taiwan tomorrow.">🔊</button></li></ol></div><div class="card"><p class="use">變化 7：不是每個動詞五種句型都能用</p><p class="zh">(1) hope 只有句型 1 和句型 2，沒有搬家句（✗ He is hoped to come.）。(2) happen、take place、belong to、consist of 這些動詞本身沒有被動式。主詞可以搬家，但動詞絕對不能改成被動。(3) that 子句主詞是 there 時，搬家後寫成 There is said to be… 或 There was said to have been…。</p><ol class="ex"><li>The accident is said to have happened at midnight.（✗ to have been happened） <button class="spk mini" data-say="The accident is said to have happened at midnight.">🔊</button></li></ol></div><div class="card"><p class="use">變化 8：that 什麼時候可以省略</p><p class="zh">句型 1 的 that 可以省略；句型 2 的 that 不可以省略，因為它帶著整個真主詞。</p><ol class="ex"><li>People say (that) Mike is sick. ✓　／　It is said Mike is sick. ✗ <button class="spk mini" data-say="People say Mike is sick. ✓ ／ It is said Mike is sick. ✗">🔊</button></li></ol></div><div class="card"><p class="use">變化 9：把 is 改成 was，意思會變</p><p class="zh">is said 表示「現在大家還這樣說」；was said 表示「以前這樣說，現在不一定了」。指定例句用 was rumored，就是因為科技已經推翻了那個謠傳。</p><ol class="ex"><li>It is rumored that the Great Pyramid is the work of extraterrestrials.（現在仍有人這樣說）　／　It was rumored that the Great Pyramid had been the work of extraterrestrials.（以前有人這樣說，現在沒有了） <button class="spk mini" data-say="It is rumored that the Great Pyramid is the work of extraterrestrials. ／ It was rumored that the Great Pyramid had been the work of extraterrestrials.">🔊</button></li></ol></div><h3>四、三種不同句型結構互換實例五則</h3><div class="q"><p class="stem"><span class="qn">★</span> <b>實例 1（句型 3：說法和事情都在現在 → to V）</b></p><div class="dlg"><p class="ln">句型 1：People say that this night market opens until two in the morning. <button class="spk mini" data-say="句型 1：People say that this night market opens until two in the morning.">🔊</button></p><p class="ln">句型 2：It is said that this night market opens until two in the morning. <button class="spk mini" data-say="句型 2：It is said that this night market opens until two in the morning.">🔊</button></p><p class="ln">主角開頭句：This night market is said to open until two in the morning. <button class="spk mini" data-say="主角開頭句：This night market is said to open until two in the morning.">🔊</button></p></div><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">中譯：據說這個夜市營業到凌晨兩點。</p><p class="why">位置變化：opens 是現在式，和 is said 同時，所以用最簡單的 to open，動詞回原形不加 s。</p></div></div><div class="q"><p class="stem"><span class="qn">★</span> <b>實例 2（句型 4：說法在現在，事情在過去 → to have p.p.）</b></p><div class="dlg"><p class="ln">句型 1：People believe that the old bridge survived three big earthquakes. <button class="spk mini" data-say="句型 1：People believe that the old bridge survived three big earthquakes.">🔊</button></p><p class="ln">句型 2：It is believed that the old bridge survived three big earthquakes. <button class="spk mini" data-say="句型 2：It is believed that the old bridge survived three big earthquakes.">🔊</button></p><p class="ln">主角開頭句：The old bridge is believed to have survived three big earthquakes. <button class="spk mini" data-say="主角開頭句：The old bridge is believed to have survived three big earthquakes.">🔊</button></p></div><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">中譯：一般相信這座老橋撐過了三次大地震。</p><p class="why">位置變化：survived 是過去式，比 is believed 早，所以不定詞往前一格，用 to have survived。</p></div></div><div class="q"><p class="stem"><span class="qn">★</span> <b>實例 3（句型 4 + 複數主詞 + 否定）</b></p><div class="dlg"><p class="ln">句型 1：People say that the two players did not break the rules. <button class="spk mini" data-say="句型 1：People say that the two players did not break the rules.">🔊</button></p><p class="ln">句型 2：It is said that the two players did not break the rules. <button class="spk mini" data-say="句型 2：It is said that the two players did not break the rules.">🔊</button></p><p class="ln">主角開頭句：The two players are said not to have broken the rules. <button class="spk mini" data-say="主角開頭句：The two players are said not to have broken the rules.">🔊</button></p></div><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">中譯：據說那兩位球員並沒有違規。</p><p class="why">位置變化：主詞是複數 players，be 動詞用 are；not 要放在 to 前面；事情在過去，所以用 to have broken。</p></div></div><div class="q"><p class="stem"><span class="qn">★</span> <b>實例 4（句型 5：指定例句，說法在過去，事情更早）</b></p><div class="dlg"><p class="ln">句型 1：Before modern technology unraveled its secrets and revealed the sheer power of human labor, people rumored that the Great Pyramid had been the work of extraterrestrials. <button class="spk mini" data-say="句型 1：Before modern technology unraveled its secrets and revealed the sheer power of human labor, people rumored that the Great Pyramid had been the work of extraterrestrials.">🔊</button></p><p class="ln">句型 2：Before modern technology unraveled its secrets and revealed the sheer power of human labor, it was rumored that the Great Pyramid had been the work of extraterrestrials. <button class="spk mini" data-say="句型 2：Before modern technology unraveled its secrets and revealed the sheer power of human labor, it was rumored that the Great Pyramid had been the work of extraterrestrials.">🔊</button></p><p class="ln">主角開頭句：Before modern technology unraveled its secrets and revealed the sheer power of human labor, the Great Pyramid was rumored to have been the work of extraterrestrials. <button class="spk mini" data-say="主角開頭句：Before modern technology unraveled its secrets and revealed the sheer power of human labor, the Great Pyramid was rumored to have been the work of extraterrestrials.">🔊</button></p></div><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">中譯：在現代科技解開金字塔的祕密、揭示人力的驚人力量之前，曾有謠傳說大金字塔是外星人的作品。</p><p class="why">位置變化：句首的 Before 子句把說法鎖在過去，所以主句用 was rumored；that 子句的 had been 比謠傳更早，所以不定詞用 to have been。不能改成 is rumored，因為現在已經沒有人這樣謠傳了。</p></div></div><div class="q"><p class="stem"><span class="qn">★</span> <b>實例 5（句型 3 的未來用法：will 消失）</b></p><div class="dlg"><p class="ln">句型 1：People expect that the new MRT line will open next summer. <button class="spk mini" data-say="句型 1：People expect that the new MRT line will open next summer.">🔊</button></p><p class="ln">句型 2：It is expected that the new MRT line will open next summer. <button class="spk mini" data-say="句型 2：It is expected that the new MRT line will open next summer.">🔊</button></p><p class="ln">主角開頭句：The new MRT line is expected to open next summer. <button class="spk mini" data-say="主角開頭句：The new MRT line is expected to open next summer.">🔊</button></p></div><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">中譯：一般預期新的捷運線將在明年夏天通車。</p><p class="why">位置變化：will open 是未來，但不定詞還是用最簡單的 to open，will 不見了，不可以寫 to will open。</p></div></div><h3>五、練習一：句型轉換填空（五題．打字作答）</h3><p class="sub">說明：依提示完成句型轉換，把整格答案打進去（可含多字，以空格分隔），按【✅ 送出答案】或 Enter 送出。</p><div id="convBox"></div><h3>六、練習二：句型填空（五題．打字作答）</h3><p class="sub">說明：依中文語意完成英文句子。</p><div id="objBox"></div><h3>七、練習三：引導式翻譯（五題．打字作答）</h3><p class="sub">說明：依中文語意把空格處應填的字一起打進去。</p><div id="objtBox"></div>
<h3>八、重點速查</h3>
<div class="card">
<p class="use">客觀說法常用的過去分詞</p>
<p class="zh">said（據說）／believed（大家相信）／suggested（有人建議）／rumored（謠傳）／advised（有人建議）／estimated（據估計）／reported（據報導）／expected（大家預期）／thought（大家認為）</p>
<p class="use" style="margin-top:10px">hope 的限制</p>
<p class="zh">hope 只能寫 People hope that… 和 It is hoped that…，沒有「主角開頭」的句子，所以沒有句型 3、4、5。</p>
<p class="use" style="margin-top:10px">沒有被動式的動詞與片語</p>
<p class="zh">happen（發生）／occur（發生）／take place（舉行、發生）／belong to（屬於）／break out（爆發）／consist of（由……組成）；另外 cost、take、last、resemble、have 也沒有被動式；連綴動詞 look、feel、taste、smell、remain 同樣沒有被動式。</p>
<p class="use" style="margin-top:10px">為什麼句型 1 的 People 會不見</p>
<p class="zh">因為主詞是 People、They、Someone 這種「泛指一般人」的字，改成被動時 by people 通常省略不寫，所以句型 2 就看不到 People 了。</p>
</div>
<div class="scroll"><table>
<thead><tr><th>不定詞形式對照總表</th><th>形式</th></tr></thead>
<tbody>
<tr><th>事情和說法同時</th><td>to V ／ to be V-ing ／ to be p.p.</td></tr>
<tr><th>事情比說法早</th><td>to have p.p. ／ to have been V-ing ／ to have been p.p.</td></tr>
<tr><th>說法在現在（is／are）</th><td>句型 3 或句型 4</td></tr>
<tr><th>說法在過去（was／were）</th><td>句型 5</td></tr>
</tbody></table></div>
<div class="subBox">
<h3 class="subH">📤 練習成果繳交步驟</h3>
<ol class="subList">
<li>把這個部分的題目<b>做到最後一題</b>，讓系統記錄你的每一題作答。</li>
<li>填入下方的<b>班級座號</b>與<b>姓名</b>。</li>
<li>按【📄 下載成果單 PDF】會開啟列印視窗，把印表機選成「<b>另存為 PDF</b>」或「Save as PDF」後儲存；若列印視窗打不開，改按【🌐 下載成果單 網頁檔】，檔案會直接存到你的「下載」資料夾，用瀏覽器打開後一樣可以另存 PDF 或直接上傳。</li>
<li>打開 <b>Google Classroom</b>，進入 Kristie 老師指定的作業繳交區。</li>
<li>點「新增或建立 → 檔案」，上傳剛才存好的檔案，最後按「<b>繳交</b>」。</li>
</ol>
<div class="subRow">
<input class="tin sm sClass" type="text" placeholder="班級座號，例如 101-25">
<input class="tin sm sName" type="text" placeholder="姓名">
</div>
<div class="subRow" style="margin-top:8px">
<button class="sendBtn pdfBtn">📄 下載成果單 PDF</button>
<button class="sendBtn htmBtn">🌐 下載成果單 網頁檔</button>
</div>
<p class="subNote">小提醒：各個練習區（文法選擇、填空、引導式翻譯、句型轉換、歷屆試題）的作答會一起收錄在同一份成果單裡，做完全部再下載最完整。手機若無法列印，用【🌐 網頁檔】一樣可以繳交。</p>
</div></section>
<section class="pane" id="t4"><h2>文法選擇｜25 題</h2><p class='sub'>按一下句中的橘色空格，會跳出四個選項的下拉選單。</p><div id='mcBox'></div><div class="subBox">
<h3 class="subH">📤 練習成果繳交步驟</h3>
<ol class="subList">
<li>把這個部分的題目<b>做到最後一題</b>，讓系統記錄你的每一題作答。</li>
<li>填入下方的<b>班級座號</b>與<b>姓名</b>。</li>
<li>按【📄 下載成果單 PDF】會開啟列印視窗，把印表機選成「<b>另存為 PDF</b>」或「Save as PDF」後儲存；若列印視窗打不開，改按【🌐 下載成果單 網頁檔】，檔案會直接存到你的「下載」資料夾，用瀏覽器打開後一樣可以另存 PDF 或直接上傳。</li>
<li>打開 <b>Google Classroom</b>，進入 Kristie 老師指定的作業繳交區。</li>
<li>點「新增或建立 → 檔案」，上傳剛才存好的檔案，最後按「<b>繳交</b>」。</li>
</ol>
<div class="subRow">
<input class="tin sm sClass" type="text" placeholder="班級座號，例如 101-25">
<input class="tin sm sName" type="text" placeholder="姓名">
</div>
<div class="subRow" style="margin-top:8px">
<button class="sendBtn pdfBtn">📄 下載成果單 PDF</button>
<button class="sendBtn htmBtn">🌐 下載成果單 網頁檔</button>
</div>
<p class="subNote">小提醒：各個練習區（文法選擇、填空、引導式翻譯、句型轉換、歷屆試題）的作答會一起收錄在同一份成果單裡，做完全部再下載最完整。手機若無法列印，用【🌐 網頁檔】一樣可以繳交。</p>
</div></section>
<section class="pane" id="t5"><h2>填空｜每格不限一字（共 16 格）</h2><p class='sub'>直接把答案打進格子裡，按【✅ 送出答案】或 Enter 送出。</p><div id='fillBox'></div><h2>引導式翻譯｜共 5 題</h2><p class='sub'>把空格處應填的字打進去；若有多格，以空格分隔一起打。</p><div id='transBox'></div><div class="subBox">
<h3 class="subH">📤 練習成果繳交步驟</h3>
<ol class="subList">
<li>把這個部分的題目<b>做到最後一題</b>，讓系統記錄你的每一題作答。</li>
<li>填入下方的<b>班級座號</b>與<b>姓名</b>。</li>
<li>按【📄 下載成果單 PDF】會開啟列印視窗，把印表機選成「<b>另存為 PDF</b>」或「Save as PDF」後儲存；若列印視窗打不開，改按【🌐 下載成果單 網頁檔】，檔案會直接存到你的「下載」資料夾，用瀏覽器打開後一樣可以另存 PDF 或直接上傳。</li>
<li>打開 <b>Google Classroom</b>，進入 Kristie 老師指定的作業繳交區。</li>
<li>點「新增或建立 → 檔案」，上傳剛才存好的檔案，最後按「<b>繳交</b>」。</li>
</ol>
<div class="subRow">
<input class="tin sm sClass" type="text" placeholder="班級座號，例如 101-25">
<input class="tin sm sName" type="text" placeholder="姓名">
</div>
<div class="subRow" style="margin-top:8px">
<button class="sendBtn pdfBtn">📄 下載成果單 PDF</button>
<button class="sendBtn htmBtn">🌐 下載成果單 網頁檔</button>
</div>
<p class="subNote">小提醒：各個練習區（文法選擇、填空、引導式翻譯、句型轉換、歷屆試題）的作答會一起收錄在同一份成果單裡，做完全部再下載最完整。手機若無法列印，用【🌐 網頁檔】一樣可以繳交。</p>
</div></section>
<section class="pane" id="t6"><h2>歷屆試題</h2><p class='sub'>學測真題：同樣的判斷邏輯，換成長句與學術語境。</p><div id='examBox'></div><h3>★ 加碼挑戰</h3><div class="q"><p class="stem"><span class="qn">1.</span> 挑戰句｜下面這句話哪裡怪怪的？請試著改寫成正確、自然的英文。<br>原句：An accident was happened here a week ago.</p><p class="zhq">一個星期前在這裡發生了車禍。</p><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">An accident happened here a week ago.</p><p class="why">happen 是不及物動詞，沒有受詞，因此根本不可能改成被動式。被動語態的成立前提是「及物動詞 + 受詞」，受詞才能被提到句首當主詞。同理，take place、occur、belong to、break out、consist of 也都不可寫成被動。若要用被動表達「舉行」，必須換成及物動詞 hold：The meeting will be held next Monday.</p></div></div>
<div class="q"><p class="stem"><span class="qn">2.</span> 挑戰句｜下面這句話哪裡怪怪的？請試著改寫成正確、自然的英文。<br>原句：The children were taken good care by the mother.</p><p class="zhq">那些孩子被照顧得很好。</p><button class="reveal">📖 參考解答</button><div class="ans"><p class="key">The children were taken good care of by the mother.</p><p class="why">動詞片語 take care of 改為被動時，介系詞 of 必須一起搬過來，絕對不可以漏掉。相同情形還有 laugh at ➔ be laughed at、rely on ➔ be relied on、look down on ➔ be looked down on、pay attention to ➔ be paid attention to。</p></div></div><div class="subBox">
<h3 class="subH">📤 練習成果繳交步驟</h3>
<ol class="subList">
<li>把這個部分的題目<b>做到最後一題</b>，讓系統記錄你的每一題作答。</li>
<li>填入下方的<b>班級座號</b>與<b>姓名</b>。</li>
<li>按【📄 下載成果單 PDF】會開啟列印視窗，把印表機選成「<b>另存為 PDF</b>」或「Save as PDF」後儲存；若列印視窗打不開，改按【🌐 下載成果單 網頁檔】，檔案會直接存到你的「下載」資料夾，用瀏覽器打開後一樣可以另存 PDF 或直接上傳。</li>
<li>打開 <b>Google Classroom</b>，進入 Kristie 老師指定的作業繳交區。</li>
<li>點「新增或建立 → 檔案」，上傳剛才存好的檔案，最後按「<b>繳交</b>」。</li>
</ol>
<div class="subRow">
<input class="tin sm sClass" type="text" placeholder="班級座號，例如 101-25">
<input class="tin sm sName" type="text" placeholder="姓名">
</div>
<div class="subRow" style="margin-top:8px">
<button class="sendBtn pdfBtn">📄 下載成果單 PDF</button>
<button class="sendBtn htmBtn">🌐 下載成果單 網頁檔</button>
</div>
<p class="subNote">小提醒：各個練習區（文法選擇、填空、引導式翻譯、句型轉換、歷屆試題）的作答會一起收錄在同一份成果單裡，做完全部再下載最完整。手機若無法列印，用【🌐 網頁檔】一樣可以繳交。</p>
</div></section>
<section class="pane" id="t7"><h2>重點回顧總複習</h2><p class='sub'>情緒動詞、慣用片語、不能被動的動詞、介系詞搭配、客觀說法速查，一次收齊。</p>
<h3>一、英文寫作常用被動語態的三種情形</h3>
<div class="card">
<p class="use">1. 主使者不明</p>
<ol class="ex">
<li>His father <b>was killed</b> in the war.（他父親在戰爭中喪生了。）</li>
<li>English <b>is spoken</b> in more than 100 countries.（有一百多個國家使用英語。）</li>
</ol>
<p class="use" style="margin-top:10px">2. 避免主觀或武斷，而用「It is + p.p.」的句型</p>
<ol class="ex">
<li><b>It is suggested that</b> we postpone the meeting until tomorrow.（我們建議把會議延到明天。）</li>
<li><b>It is said that</b> she was a beauty when she was young.（據說她年輕時，是個美女。）</li>
</ol>
<p class="use" style="margin-top:10px">3. 說話的重點在接受動作者，不在主動者</p>
<ol class="ex">
<li>The man <b>was hit</b> by a speeding car.（這個人被一輛超速的車子撞上。）</li>
<li>The book <b>was written</b> by Dr. Lee.（這本書是李博士寫的。）</li>
</ol>
</div>

<h3>二、情緒動詞 Emotional Verbs</h3>
<div class="scroll"><table>
<thead><tr><th>分類</th><th>常用情緒動詞與搭配介系詞</th></tr></thead>
<tbody>
<tr><th>表高興、滿意</th><td>amused (with / at)、delighted (with / at)、excited (about)、interested (in)、pleased (with)、satisfied (with)</td></tr>
<tr><th>表驚訝</th><td>amazed (at)、astonished (at)、startled (at)、surprised (at)、shocked (at)、stunned (by)、frightened (at / about)</td></tr>
<tr><th>其他／負面／疲憊</th><td>annoyed (by / with)（苦惱）、bored (with)（厭煩）、disappointed (at / with)（失望）、disgusted (with / by)（厭惡）、embarrassed (at / with / about)（困窘）、tired / exhausted / fatigued (by / with / from)（疲倦）；補充：be tired of… ／ be tired from / with…</td></tr>
</tbody></table></div>
<div class="card">
<p class="zh">文法說明：(1) 所謂「情緒動詞」是指可以表達各種「心理感受」（如：「高興」、「滿意」、「驚訝」等）的動詞。(2) 上述動詞，若主詞是「人」的話，常用「被動」形式表達，其句型是：「人 + be V + 情緒動詞的過去分詞」➔ 表示「某人感到……」。</p>
<ol class="ex">
<li>Alice <b>is interested in</b> studying English literature.（愛麗絲對研究英國文學有興趣。）</li>
<li>Joe <b>was delighted</b> to meet you.（喬很高興見到你。）</li>
<li>I <b>was surprised</b> to hear the news.（我聽到這消息甚為驚訝。）</li>
<li>We <b>were disappointed at</b> learning the truth.（我們了解真相之後很失望。）</li>
</ol>
</div>

<h3>三、具被動形式但無被動意義的慣用片語</h3>
<div class="scroll"><table>
<thead><tr><th>左欄片語</th><th>右欄片語</th></tr></thead>
<tbody>
<tr><td>be used to + N（習慣於）</td><td>be accustomed to + N（習慣於）</td></tr>
<tr><td>be devoted to + N（獻身於）</td><td>be dedicated to + N（致力於）</td></tr>
<tr><td>be absorbed in（專心於）</td><td>be engaged in（從事於）</td></tr>
<tr><td>be acquainted with（熟悉）</td><td>be concerned about（關心）</td></tr>
<tr><td>be opposed to + N（反對）</td><td>be supposed to + V（應該要）</td></tr>
<tr><td>be exposed to + V / N（暴露於）</td><td>be well-known for（以……著名）</td></tr>
<tr><td>be made up of / consist of（由……組成）</td><td>be inclined to + V（傾向於）</td></tr>
<tr><td>be wounded / be injured（受傷）</td><td>be seated (on the…)（就座）</td></tr>
<tr><td>be located / situated / sited（位於）</td><td>be dressed in / with（穿著）</td></tr>
<tr><td></td><td>be available（可用／購得）</td></tr>
</tbody></table></div>
<div class="card">
<p class="zh">1. 建築物 + be located（＝ be situated）（位於……）<br>
2. 人 + be dressed（＝ dress oneself）（穿著）<br>
3. 整體 + be made up of + 元素（＝ be composed of）（由……組成）＝ consist of</p>
</div>

<h3>四、不能用被動式的動詞與片語</h3>
<div class="card">
<p class="zh">take place（發生）／happen（發生）／occur（發生）／belong to（屬於）／break out（爆發）／consist of（由……組成）皆為不及物動詞，沒有被動式。</p>
<ol class="ex">
<li>一個星期前在這裡發生了車禍。<br>［正］<b>An accident happened here a week ago.</b><br>［誤］An accident was happened here a week ago.</li>
<li>這棟房子現在屬於我。<br>［正］<b>This house belongs to me now.</b><br>［誤］This house is belonged to me now.</li>
</ol>
<p class="zh" style="margin-top:10px">1. 「take place」做「舉行」解時，要注意其用法：下星期一將舉行會議。<br>
We will hold the meeting next Monday.＝ The meeting will be held next Monday.＝ The meeting will take place next Monday.</p>
<p class="zh">2. 「連綴動詞」（如 look, feel, taste, smell, remain 等）沒有被動形式：這杯咖啡嚐起來有一點苦。<br>
［正］The coffee tastes a little bitter.　［誤］The coffee is tasted a little bitter.</p>
<p class="zh">3. 並非所有及物動詞都有被動形式，如：cost（花費）、take（花費）、last（持續）、resemble（像）、have（有）等沒有被動形式：這枝筆要十元。<br>
［正］The pen cost ten dollars.　［誤］The pen is cost ten dollars.</p>
</div>

<h3>五、以動名詞或不定詞表被動語態</h3>
<div class="card">
<p class="zh">下列動詞看似主動，但其實含有被動的意義：<br>
1. be worth + V-ing（值得……）　補充筆記：be worthy of N / to V / of being p.p. / to be p.p.<br>
2. need / want / require + V-ing（需要……）　補充筆記：need to be p.p.<br>
3. to let（出租）、to blame（該受責備）</p>
<ol class="ex">
<li>The book <b>is worth reading</b>.（這本書值得一讀。）＝ The book is worthy to be read.＝ The book is worthy of being read.</li>
<li>My car <b>needs checking</b>.（我的車子需要檢查。）＝ My car needs to be checked.</li>
<li>The house <b>is to let</b>.（此屋出租。）</li>
<li>You <b>are to blame</b>.（你應受責備。）</li>
</ol>
</div>

<h3>六、用其他介系詞代替 by</h3>
<p class="sub">在被動語態中，表示行為者的介系詞通常用 by；但有些動詞不用 by 而要用其他的介系詞（如 to, in, at, with…）。</p>
<div class="scroll"><table>
<thead><tr><th>介系詞</th><th>常見搭配</th></tr></thead>
<tbody>
<tr><th>with</th><td>be acquainted（認識）、be covered（覆蓋）、be equipped（裝備）、be pleased（高興）、be satisfied（滿意）、be crowded / packed（擠滿）、be filled（充滿）<br>範例：The train is packed / crowded with passengers.</td></tr>
<tr><th>at</th><td>be amazed / astonished（驚訝）、be startled / surprised / shocked（震驚）、be disappointed（失望）、be frightened（驚嚇）</td></tr>
<tr><th>in</th><td>be dressed（穿～衣服）、be interested（感興趣）、be absorbed（專心於）、be engaged（從事於）、be caught（遇到）</td></tr>
<tr><th>to 及其他</th><td>be accustomed / used（習慣於）、be devoted / dedicated（致力於）、be known（為～所知）、be married（結婚）、be obliged（感激）、be engaged（訂婚）</td></tr>
</tbody></table></div>
<div class="card">
<ol class="ex">
<li>The mountain <b>is covered with</b> snow.（山被雪所覆蓋。）</li>
<li>Tony <b>is pleased with</b> his new job.（東尼對新工作很滿意。）</li>
<li>I <b>was surprised at</b> the news.（這消息使我吃驚。）</li>
<li>Lily <b>is interested in</b> music.（莉莉對音樂感興趣。）</li>
<li>Mother Teresa <b>was devoted to</b> helping the poor.（德蕾莎修女奉獻一生幫助窮人。）</li>
<li>I <b>was caught in</b> a shower on my way home.（我在回家途中遇到陣雨。）</li>
</ol>
</div>

<h3>七、被動語態與介系詞的選擇：with 工具 ／ by 行為者</h3>
<div class="card">
<p class="zh">句型結構：被動式 + { with + 工具 ／ by + 行為者 }</p>
<ol class="ex">
<li>This photo <b>was taken with</b> a cell phone.（這張照片是用手機拍的。）</li>
<li>He wrote the note <b>with</b> a pen.（他用筆寫下這張字條。）</li>
<li>The mailman <b>was bitten by</b> a dog a few days ago.（那郵差幾天前被狗咬到。）</li>
</ol>
</div>

<h3>八、be known 的不同搭配用法</h3>
<div class="card">
<p class="zh">句型結構：be known + { to + 名詞（廣為……所知／對象）／ as + 身份（以……身份而著名）／ by（藉著～而被知道／口碑 word of mouth）}</p>
<ol class="ex">
<li>As <b>is known to</b> us, Michael Jordan is the best basketball player of all time.（誠如我們所知，麥克·喬登是有史以來最棒的籃球選手。）</li>
<li>Louis <b>is known as</b> a rock singer.（路易斯以搖滾歌手而著名。）</li>
<li>A man <b>is known by</b> the company he keeps.（觀其友，而知其人。）</li>
</ol>
</div>

<h3>九、客觀說法重點速查｜五種時態對應</h3>
<div class="card">
<p class="zh">表「客觀說法」的常見過去分詞：believed（大家相信）／expected（大家期待）／reported（據報導）／rumored（謠傳）／said（據說）／suggested（有人建議）／thought（大家認為）／advised（有人建議）／estimated（據估計）。基本句型：It is [p.p.] that S + V…</p>
<p class="note">判斷關鍵：主句的 be 動詞決定「說法何時被說出」，不定詞的形式決定「事情何時發生」。</p>
</div>

<div class="card">
<p class="use">【時態 3-1：現在對現在】說法在現在，事情也在現在 <span class="arrow">➔</span> to V</p>
<ol class="ex">
<li>They say that Mike is sick in bed.（據說麥克臥病在床。）<span class="arrow">➔</span> It is said that Mike is sick in bed. <span class="arrow">➔</span> <b>Mike is said to be sick in bed.</b><button class="spk mini" data-say="They say that Mike is sick in bed. It is said that Mike is sick in bed. Mike is said to be sick in bed.">🔊</button></li>
<li>It is thought that dogs are man's best friend.（我們都認為狗是人類最好的朋友。）<span class="arrow">➔</span> <b>Dogs are thought to be man's best friend.</b><button class="spk mini" data-say="It is thought that dogs are man's best friend. Dogs are thought to be man's best friend.">🔊</button></li>
</ol>
</div>

<div class="card">
<p class="use">【時態 3-2：現在對過去】說法在現在，事情在過去 <span class="arrow">➔</span> to have p.p.</p>
<ol class="ex">
<li>People believe that he was rich.（大家相信他以前很有錢。）<span class="arrow">➔</span> It is believed that he was rich. <span class="arrow">➔</span> <b>He is believed to have been rich.</b><button class="spk mini" data-say="People believe that he was rich. It is believed that he was rich. He is believed to have been rich.">🔊</button></li>
<li>It is rumored that the famous singer got married in France.（據傳這位著名的歌手已經在法國結婚了。）<span class="arrow">➔</span> <b>The famous singer is rumored to have got married in France.</b><button class="spk mini" data-say="It is rumored that the famous singer got married in France. The famous singer is rumored to have got married in France.">🔊</button></li>
</ol>
</div>

<div class="card">
<p class="use">【時態 3-3：過去對過去】說法在過去，事情與說法同時 <span class="arrow">➔</span> was／were + p.p. + to V</p>
<div class="dlg">
<p class="ln">People in the 20th century believed that smallpox and polio were incurable diseases. Thanks to concerted global efforts by governments, they have now become extremely rare.<button class="spk mini" data-say="People in the twentieth century believed that smallpox and polio were incurable diseases. Thanks to concerted global efforts by governments, they have now become extremely rare.">🔊</button></p>
<p class="ln zhl">中譯：在 20 世紀時人們認為天花和小兒麻痺是不治之症。由於各國政府的共同努力，如今這兩種疾病已極為罕見。</p>
<p class="ln"><span class="arrow">➔</span> It was believed that smallpox and polio were incurable diseases in the 20th century. Thanks to concerted global efforts by governments, they have now become extremely rare.<button class="spk mini" data-say="It was believed that smallpox and polio were incurable diseases in the twentieth century.">🔊</button></p>
<p class="ln"><span class="arrow">➔</span> <b>Smallpox and polio were believed to be incurable diseases in the 20th century.</b> Thanks to concerted global efforts by governments, they have now become extremely rare.<button class="spk mini" data-say="Smallpox and polio were believed to be incurable diseases in the twentieth century.">🔊</button></p>
</div>
<span class="note">說法鎖在 20 世紀，而「是不治之症」在當時也同時成立，兩個時間一樣早，所以主句用 were believed，不定詞仍用最簡單的 to be。</span>
</div>

<div class="card">
<p class="use">【時態 3-4：過去對更早的過去】說法在過去，事情比說法更早 <span class="arrow">➔</span> was／were + p.p. + to have p.p.</p>
<div class="dlg">
<p class="ln">Before modern technology unraveled its secrets and revealed the sheer power of human labor, people rumored that the Great Pyramid had been the work of extraterrestrials.<button class="spk mini" data-say="Before modern technology unraveled its secrets and revealed the sheer power of human labor, people rumored that the Great Pyramid had been the work of extraterrestrials.">🔊</button></p>
<p class="ln zhl">中譯：在現代科技揭開金字塔的祕密並展現人類勞動的巨大力量之前，曾有傳言大金字塔是由外星人一手打造。</p>
<p class="ln"><span class="arrow">➔</span> Before modern technology unraveled its secrets and revealed the sheer power of human labor, it was rumored that the Great Pyramid had been the work of extraterrestrials.<button class="spk mini" data-say="Before modern technology unraveled its secrets and revealed the sheer power of human labor, it was rumored that the Great Pyramid had been the work of extraterrestrials.">🔊</button></p>
<p class="ln"><span class="arrow">➔</span> Before modern technology unraveled its secrets and revealed the sheer power of human labor, <b>the Great Pyramid was rumored to have been the work of extraterrestrials.</b><button class="spk mini" data-say="Before modern technology unraveled its secrets and revealed the sheer power of human labor, the Great Pyramid was rumored to have been the work of extraterrestrials.">🔊</button></p>
</div>
<span class="note">Before 子句把謠傳鎖在過去，而 that 子句的 had been 比謠傳更早，所以主句用 was rumored，不定詞往前推一格，用 to have been。</span>
</div>

<div class="card">
<p class="use">【句型 3-5】It is expected／estimated／projected that S will／can + V（說法在現在，事情在未來）</p>
<p class="zh">說明 1：expect（預料、預計、期待）／estimate（估計、估算）／project（預計、推算）這類的動詞本身就是表達預期、預計、期待未來事件的發生。</p>
<p class="zh">說明 2：hope（希望、盼望）只能用 It is hoped that S will…，沒有主詞提升句（✗ The typhoon is hoped to hit Taiwan tomorrow）。</p>
<p class="zh">說明 4：that 子句有 will <span class="arrow">➔</span> 不定詞用 to V，will 消失；有 can <span class="arrow">➔</span> 改成 to be able to V。</p>
<ol class="ex">
<li>It is expected that the typhoon will hit Taiwan tomorrow. <span class="arrow">➔</span> <b>The typhoon is expected to hit Taiwan tomorrow.</b>（✗ to will hit）<button class="spk mini" data-say="It is expected that the typhoon will hit Taiwan tomorrow. The typhoon is expected to hit Taiwan tomorrow.">🔊</button></li>
</ol>
</div>

<div class="card">
<p class="zh">省略 by 的時機：主動語態主詞為 People、They、You、We、Somebody 等泛指一般人時，改被動後通常省略 by + 某人，這正是句型 1 轉句型 2 時 People 消失的原因。</p>
</div>
</section>

</main>

<div id="toast"></div>

<script>
const DATA = {"mc": [{"s": "The Eiffel Tower @ in 1889.", "zh": "艾菲爾鐵塔於 1889 年建造。", "o": ["is built", "has built", "had been built", "was built"], "k": 3, "e": "有過去特定時間點 1889，且鐵塔是被建造，故用過去簡單式被動 was + p.p.。"}, {"s": "Nowadays, hip hop @ mostly by young people.", "zh": "現今，嘻哈音樂大多受到年輕人的喜愛。", "o": ["is enjoyed", "has enjoyed", "enjoyed", "has been enjoying"], "k": 0, "e": "Nowadays 表示現今的普遍事實，嘻哈音樂是被喜愛，故用現在簡單式被動。"}, {"s": "By the time you return, the house @.", "zh": "等你回來時，這棟房子將已經改建完成了。", "o": ["had been remodeled", "will have been remodeled", "will remodel", "has been remodeled"], "k": 1, "e": "By the time + 現在式代替未來式，主句表到未來某時將已完成，且房子是被改建，故用未來完成式被動。"}, {"s": "The concert @ in the Taipei Arena（臺北小巨蛋）next month.", "zh": "演唱會將於下個月在臺北小巨蛋舉行。", "o": ["will hold", "is being held", "will be held", "will be holding"], "k": 2, "e": "next month 為未來特定時間，演唱會是被舉行，故用未來簡單式被動 will be held。"}, {"s": "Look! The cat @ by the dog.", "zh": "看！貓咪正在被狗追。", "o": ["is chasing", "is chased", "is being chased", "chases"], "k": 2, "e": "Look! 提示動作此刻正在進行，貓是被追，故用現在進行式被動 is being chased。"}, {"s": "His voice was so loud that it @ all over the office.", "zh": "他的聲音是如此之大，以至於在整個辦公室都聽得到。", "o": ["could be heard", "could hear", "could have heard", "could be hearing"], "k": 0, "e": "主詞 it 指代聲音，聲音是被聽見的，助動詞 could 後接原形被動 be + p.p.。"}, {"s": "He @ many job offers since he graduated.", "zh": "自從他畢業以來，他已經獲得了許多工作機會。", "o": ["is given", "has been given", "was given", "has been giving"], "k": 1, "e": "搭配 since he graduated 應用現在完成式，且他是被給予工作機會，故用現在完成式被動 has been given。"}, {"s": "A decision must @ today.", "zh": "今天必須做出決定。", "o": ["make", "have been made", "be made", "to make"], "k": 2, "e": "助動詞 must 後接原形被動 be + p.p.，故選 be made。"}, {"s": "We were made @ for hours before the game.", "zh": "比賽前我們被逼得等了好幾個小時。", "o": ["wait", "waiting", "waited", "to wait"], "k": 3, "e": "使役動詞 make 改為被動語態時，原形動詞 VR 須還原加上 to，故選 to wait。"}, {"s": "The beautiful deer was seen @ on the grass in the field.", "zh": "那隻美麗的鹿被看到正在田野的草地上吃草。", "o": ["feed", "feeding", "fed", "for feeding"], "k": 1, "e": "感官動詞 see 改為被動語態時，若強調動作正在發生，後方可接 V-ing，故選 feeding。"}, {"s": "After his parents died, he @ by his grandmother.", "zh": "父母去世後，他由祖母照顧。", "o": ["took care of", "has taken care of", "was taken care of", "will take care of"], "k": 2, "e": "動詞片語 take care of 改被動為 be taken care of，且事情發生在過去，故用過去簡單式被動，介系詞 of 不可漏。"}, {"s": "The project should @ by Friday.", "zh": "該專案應該在星期五前完成。", "o": ["complete", "be completed", "be completing", "have completed"], "k": 1, "e": "助動詞 should 後接原形被動 be + p.p.，專案是被完成，故選 be completed。"}, {"s": "Taipei 101 @ in 2004.", "zh": "臺北 101 於 2004 年完工。", "o": ["was completed", "had been completed", "completed", "was being completed"], "k": 0, "e": "in 2004 為明確的過去時間點，大樓是被完成，故用過去簡單式被動。"}, {"s": "He hates @ an idiot.", "zh": "他討厭被叫作白癡。", "o": ["calling", "being called", "called", "to call"], "k": 1, "e": "hate 後接動名詞，且他是被叫，動名詞的被動為 being + p.p.，故選 being called。"}, {"s": "He was heard @ a love song to his girlfriend.", "zh": "他被聽到正在對女友唱情歌。", "o": ["to singing", "sing", "sang", "singing"], "k": 3, "e": "感官動詞 hear 改被動後可接 to VR 或 V-ing；此處強調動作當下正在發生，故選 singing。"}, {"s": "The man who ran through the red light was made @ his driver's license（駕照）.", "zh": "那個闖紅燈的人被逼著出示駕照。", "o": ["to show", "show", "showing", "shown"], "k": 0, "e": "使役動詞 make 改為被動時，原形動詞須還原加上 to，故選 to show。"}, {"s": "He doesn't like the feeling of @.", "zh": "他不喜歡被嘲笑的感覺。", "o": ["laughed at", "being laughed at", "laughed", "laughing at"], "k": 1, "e": "介系詞 of 後須接動名詞，且他是被嘲笑，故用動名詞被動 being laughed at，介系詞 at 不可漏。"}, {"s": "The patient had to @ to the hospital immediately.", "zh": "病人必須立刻被送到醫院。", "o": ["send", "being sent", "have been sent", "be sent"], "k": 3, "e": "had to 後接原形動詞，病人是被送，故用原形被動 be sent。"}, {"s": "All the windows and doors ought to @ before you go to bed.", "zh": "睡覺前所有的門窗都應該上鎖。", "o": ["locked", "be locked", "have locked", "be locking"], "k": 1, "e": "ought to 後接原形被動 be + p.p.，門窗是被鎖，故選 be locked。"}, {"s": "I have to stay at my friend's place because my apartment @ now.", "zh": "我必須待在朋友家，因為我的公寓現在正在改建。", "o": ["remodeled", "is being remodeled", "remodeling", "has been remodeled"], "k": 1, "e": "now 表此刻正在進行，公寓是被改建，故用現在進行式被動 is being remodeled。"}, {"s": "The mailman found out that the letter @ delivered to the wrong address.", "zh": "郵差發現那封信已經被寄送到錯誤的地址。", "o": ["is", "had", "has been", "had been"], "k": 3, "e": "信件被寄錯發生在 found out 這個過去動作之前，屬於過去的過去，且為被動，故用 had been + p.p.。"}, {"s": "If you don't work hard, you will certainly @ by your boss.", "zh": "如果你不努力工作，你一定會被老闆開除。", "o": ["fire", "being fired", "be fired", "to fire"], "k": 2, "e": "will 後接原形被動 be + p.p.，你是被開除，故選 be fired。"}, {"s": "Johnson is very responsible and honest, so he can @.", "zh": "Johnson 非常負責且誠實，所以他是值得信賴的。", "o": ["rely on", "be relied on", "be relied", "be relying on"], "k": 1, "e": "動詞片語 rely on 改被動為 be relied on，助動詞 can 後接原形，介系詞 on 絕不可漏。"}, {"s": "Everyone heard John @ a love song to his wife.（改為被動：John was heard ______ a love song to his wife.）", "zh": "大家都聽到 John 對他的老婆唱歌。被動：John 被聽到唱歌給他老婆聽。", "o": ["to sing", "sing", "sung", "to singing"], "k": 0, "e": "主動時感官動詞後接原形 sing；改為被動時，原形動詞須還原加上 to，故被動句用 to sing。"}, {"s": "My car needs @.（＝ My car needs to be checked.）", "zh": "我的車子需要檢查。", "o": ["checking", "to check", "checked", "being checked"], "k": 0, "e": "need / want / require + V-ing 看似主動，實含被動意義，等於 need to be checked，故選 checking。"}], "exam": [{"s": "Apples have been grown for thousands of years in Asia and Europe, and @ to North America by European colonists in the 17th century.［104 學測］", "zh": "蘋果在亞洲和歐洲種植了數千年，並在 17 世紀由歐洲殖民者帶到北美。", "o": ["bring", "have brought", "were brought", "have been brought"], "k": 2, "e": "主詞 apples 與 bring 為被動關係，且發生在過去特定時間 17th century，故用過去簡單式被動 were brought。"}, {"s": "Later, as steel wire became more common, inventors began to notice its elastic feature. With this feature, it could @ into various clip-like objects.［104 學測改］", "zh": "當鋼線變得更普遍，發明家注意到它的彈性特徵。利用此特徵，它能被拉伸並被扭曲成各種夾子狀的物品。", "o": ["be stretched; twisted", "stretch; twist", "be stretching; twisting", "have stretched; twisted"], "k": 0, "e": "could 後接原形被動 be + p.p.，and 連接對等的被動語態 be stretched 和 twisted。"}, {"s": "The familiar looped design was invented by Gem Manufacturing Ltd. in England. This clip is therefore sometimes @ as the Gem clip.［104 學測改］", "zh": "熟悉的環形設計由英國 Gem Manufacturing Ltd. 發明。因此這個夾子有時被稱為 Gem 夾。", "o": ["being known", "known", "knowing", "having known"], "k": 1, "e": "be known as… 為被動固定片語，表「以……而聞名、被稱為」，故選過去分詞 known。"}, {"s": "People may choose a name because they are strongly @ to a character in a book or a television series; they may also adopt names of famous people or their favorite actors and actresses.［104 學測改］", "zh": "人們可能會選擇一個名字，因為他們強烈地被書中或電視劇中的角色所吸引。", "o": ["drawing", "being drawn", "drawn", "having drawn"], "k": 2, "e": "be drawn to… 表示「被……所吸引」，故用過去分詞 drawn 構成被動。"}, {"s": "The art of using paste from the henna plant to create temporary henna tattoos goes back to ancient Egypt. Over the centuries, these tattoos @ in celebrations because they are thought to carry blessings from the gods.［104 學測改］", "zh": "使用指甲花植物製成暫時性刺青的藝術可追溯到古埃及。幾個世紀以來，這些刺青一直被用於慶祝活動中。", "o": ["have been used", "were used", "are being used", "had used"], "k": 0, "e": "搭配 Over the centuries（幾世紀以來）表示從過去持續到現在，且刺青是被使用，故用現在完成式被動 have been used。"}], "fill": [{"s": "He enjoys ________ (admire) by his fans.", "zh": "他喜歡被他的粉絲們仰慕。", "key": "being admired", "acc": ["being admired"], "e": "enjoy 後接動名詞，且他是「被仰慕」，動名詞的被動為 being + p.p.。"}, {"s": "The naughty students were ________ (make, clean) the classroom.", "zh": "調皮的學生們被逼著打掃教室。", "key": "made to clean", "acc": ["made to clean"], "e": "使役動詞 make 改為被動時，後面的原形動詞須還原加上 to，故為 were made to clean。"}, {"s": "Listen! My favorite song ________ (sing) by the street performer（街頭藝人）.", "zh": "聽！我最喜歡的歌正被那位街頭藝人演唱。", "key": "is being sung", "acc": ["is being sung"], "e": "Listen! 表示此刻正在進行，歌曲是被演唱，故用現在進行式被動 is being + p.p.。"}, {"s": "He was seen ________ (cry) in the corner.", "zh": "他被看到在角落哭泣。", "key": "crying", "acc": ["crying", "to cry"], "e": "感官動詞 see 改被動後，若強調動作發生的當下，接 V-ing，故用 crying。"}, {"s": "What the teacher says should ________ (pay attention to).", "zh": "老師所說的話應該被注意。", "key": "be paid attention to", "acc": ["be paid attention to"], "e": "助動詞 should 後接原形被動；動詞片語 pay attention to 改被動時介系詞 to 絕不可漏。"}, {"s": "His album ________ (release) last week.", "zh": "他的專輯上星期發行了。", "key": "was released", "acc": ["was released"], "e": "last week 為過去時間，專輯是被發行，故用過去簡單式被動。"}, {"s": "This course ________ (teach) by Mr. Wang for the past five years.", "zh": "這門課程過去五年一直由王先生授課。", "key": "has been taught", "acc": ["has been taught", "has been being taught"], "e": "for the past five years 表從過去持續到現在，課程是被教授，故用現在完成式被動 has been taught。"}, {"s": "English ________ (speak) in countries like America, Britain, New Zealand, and Australia.", "zh": "英語在美國、英國、紐西蘭和澳洲等國家被說。", "key": "is spoken", "acc": ["is spoken"], "e": "敘述現在的普遍事實，英語是被說，故用現在簡單式被動 is spoken。"}, {"s": "The bridge ________ (repair) now, so we have to take a detour（繞道）.", "zh": "這座橋現在正在修繕，所以我們必須繞道。", "key": "is being repaired", "acc": ["is being repaired"], "e": "now 表此刻正在進行，橋是被修繕，故用現在進行式被動 is being repaired。"}, {"s": "He is believed to ________ (be) rich when he was young.", "zh": "據信他年輕時很有錢。", "key": "have been", "acc": ["have been"], "e": "when he was young 為過去的事實，比主句 is believed 更早，故不定詞往前推一格，用完成式不定詞 to have been。"}, {"s": "It ________ (estimate) that the project will take one year to complete.", "zh": "據估計該專案將需要一年時間完成。", "key": "is estimated", "acc": ["is estimated"], "e": "客觀說法句型 It is + p.p. + that S + V，故用 is estimated。"}, {"s": "By the time I got home, all the food ________ (eat) up.", "zh": "等我回到家時，所有的食物都已經被吃光了。", "key": "had been eaten", "acc": ["had been eaten"], "e": "By the time + 過去式，主句表更早完成，且食物是被吃光，故用過去完成式被動 had been eaten。"}, {"s": "The tickets to the musical Cats ________ (sell) out before I knew it.", "zh": "音樂劇《貓》的票在我不知不覺中就賣光了。", "key": "were sold（亦可 had been sold）", "acc": ["were sold", "had been sold"], "e": "票是被賣光，before I knew it 指過去，故用過去簡單式被動；若強調比「我知道」更早，亦可用過去完成式被動。"}, {"s": "The actor is reported to ________ (die) of heart attack.", "zh": "據報導該演員死於心臟病發作。", "key": "have died", "acc": ["have died"], "e": "死亡發生在報導之前，故用完成式不定詞 to have died；die 為不及物動詞，絕不可寫成 to have been died。"}, {"s": "The teacher said that the homework should ________ (hand in) on time.", "zh": "老師說作業應該準時交。", "key": "be handed in", "acc": ["be handed in"], "e": "should 後接原形被動，動詞片語 hand in 改被動為 be handed in，介系詞 in 不可漏。"}, {"s": "Such success was never ________ (dream of).", "zh": "這樣的成功從未被夢想過（從未料到）。", "key": "dreamed of（亦可 dreamt of）", "acc": ["dreamed of", "dreamt of"], "e": "動詞片語 dream of 改為被動時寫成 be dreamed of，介系詞 of 絕不可漏。"}], "trans": [{"s": "We should protect the environment from ________.", "zh": "我們應該保護環境使其免於被污染。", "key": "being polluted", "acc": ["being polluted"], "e": "介系詞 from 後須接動名詞，環境是被污染，故用動名詞的被動 being + p.p.。"}, {"s": "Barack Obama ________ President of the United States in 2008, becoming the first African-American U.S. president.", "zh": "歐巴馬在二○○八年當選美國總統，成為第一位美國黑人總統。", "key": "was elected", "acc": ["was elected"], "e": "elect 為有受詞補語的動詞，改被動時以受詞為主詞；in 2008 為過去時間，故用過去簡單式被動 was elected。"}, {"s": "It is rumored ________ he ________.（兩格請一起打，以空格分隔）", "zh": "謠傳他是被謀殺的。", "key": "that ／ was murdered", "acc": ["that was murdered", "that he was murdered"], "e": "客觀說法句型 It is rumored that S + V，that 不可省略；他是被謀殺，故用過去簡單式被動 was murdered。"}, {"s": "Yesterday's game ________ because of the rain.（提示：p 開頭的動詞）", "zh": "昨天的比賽因雨延期了。", "key": "was postponed", "acc": ["was postponed"], "e": "比賽是被延期，昨天為過去時間，故用過去簡單式被動 was postponed。"}, {"s": "I ________ by any teacher.", "zh": "我從未被任何老師處罰過。", "key": "have never been punished", "acc": ["have never been punished", "never have been punished"], "e": "「從未被處罰過」表從過去到現在的經驗，故用現在完成式被動，never 置於 have 與 been 之間。"}], "conv": [{"s": "People say that my grandmother makes the best beef noodles in town. <span class='arrow'>→</span> My grandmother ________ the best beef noodles in town.（四格請一起打，以空格分隔）", "zh": "大家說我奶奶做全鎮最好吃的牛肉麵。", "key": "is said to make", "acc": ["is said to make"], "e": "主詞 my grandmother 搬到句首，單數所以用 is；makes 是現在式，和說法同時，所以用 to make，動詞回原形不加 s。這是句型 3。"}, {"s": "It is believed that the writer finished the novel in only three months. <span class='arrow'>→</span> The writer is believed ________ the novel in only three months.（三格請一起打）", "zh": "一般相信這位作家只花三個月就完成了這本小說。", "key": "to have finished", "acc": ["to have finished"], "e": "finished 是過去式，比 is believed 早，所以不定詞往前一格，用 to have finished。這是句型 4。"}, {"s": "It was rumored that the Great Pyramid had been the work of extraterrestrials. <span class='arrow'>→</span> The Great Pyramid ________ the work of extraterrestrials.（五格請一起打）", "zh": "曾有謠傳說大金字塔是外星人的作品。", "key": "was rumored to have been", "acc": ["was rumored to have been"], "e": "主句原本是過去式 was rumored，搬家後要保留過去式；that 子句的 had been 比謠傳更早，所以用 to have been。這是句型 5。"}, {"s": "It is said that the shy boy does not talk to strangers. <span class='arrow'>→</span> The shy boy is said ________ to strangers.（三格請一起打）", "zh": "據說這個害羞的男孩不跟陌生人說話。", "key": "not to talk", "acc": ["not to talk"], "e": "not 要移到 to 的前面。如果寫成 is not said to talk，意思會變成「沒有人這樣說」，和原意不同。"}, {"s": "People expect that the museum will reopen next month. <span class='arrow'>→</span> The museum ________ next month.（四格請一起打）", "zh": "大家預期這間博物館下個月將重新開放。", "key": "is expected to reopen", "acc": ["is expected to reopen"], "e": "主句是現在式，用 is expected；will reopen 是未來，但不定詞仍用 to reopen，will 消失，不可寫 to will reopen。這是句型 3。"}], "obj": [{"s": "The bridge is said ________ more than three hundred years ago.（四格請一起打，以空格分隔）", "zh": "據說這座橋是三百多年前建造的。", "key": "to have been built", "acc": ["to have been built"], "e": "three hundred years ago 是過去的時間，而且橋是「被建造」的，所以完成式和被動一起用，寫成 to have been built。這是句型 4。"}, {"s": "Exercise ________ helpful in reducing stress.（四格請一起打）", "zh": "一般認為運動有助於減輕壓力。", "key": "is believed to be", "acc": ["is believed to be"], "e": "exercise 是不可數名詞，當單數用 is believed；「有助於」是現在的事實，和說法同時，所以用 to be。這是句型 3。"}, {"s": "Before the fire, the photos ________.（六格請一起打）", "zh": "在那場大火之前，大家都相信這些照片早就不見了。", "key": "were believed to have been lost", "acc": ["were believed to have been lost"], "e": "Before the fire 把說法鎖在過去，主詞是複數，所以用 were believed；「早就不見了」比當時的相信更早，照片是「被遺失」，所以用 to have been lost。這是句型 5。"}, {"s": "The fire ________ millions of dollars in damage.（五格請一起打）", "zh": "據估計這場大火造成了上百萬元的損失。", "key": "is estimated to have caused ／ was estimated to cause ／ was estimated to have caused", "acc": ["is estimated to have caused", "was estimated to cause", "was estimated to have caused"], "e": "情況 (1) the fire（這場大火）是已經發生的過去事件，比事後估計損失（is estimated）發生得早，故用 to have caused；而主詞 the fire 是單數，用 is。　情況 (2) the fire（這場大火）是已經發生的過去事件，據估計也是發生在過去，【過去的估計損失對過去的事件，用不定詞 to VR】來表達事件與估計損失都發生在過去，故填入 was estimated to cause。　情況 (3) the fire（這場大火）是已經發生的過去事件，估計損失雖是大火發生或撲滅後才進行，但估計損失仍發生在過去，【過去估計更早之前發生的大火所造成的損失】，故用 was estimated（事後估計）to have caused（這場大火之前所造成的損失）。"}, {"s": "The old man is said ________ to anyone.（三格請一起打）", "zh": "據說這位老人從不向任何人抱怨。", "key": "never to complain", "acc": ["never to complain"], "e": "never 和 not 一樣要放在 to 前面，寫成 never to complain；complain 後面要加介系詞 to。這是句型 3 的否定形式。"}], "objt": [{"s": "Before modern technology unraveled its secrets, the Great Pyramid ________ the work of extraterrestrials.（五格請一起打，以空格分隔）", "zh": "在現代科技解開祕密之前，大金字塔一直被謠傳是外星人的作品。", "key": "was rumored to have been", "acc": ["was rumored to have been"], "e": "完整句：Before modern technology unraveled its secrets, the Great Pyramid was rumored to have been the work of extraterrestrials.　Before 子句把說法鎖在過去，主句用 was rumored；事情比謠傳更早，所以用 to have been。這是句型 5。"}, {"s": "The bookstore ________ for more than sixty years.（五格請一起打）", "zh": "據說這間書店已經開了超過六十年。", "key": "is said to have been open", "acc": ["is said to have been open"], "e": "完整句：The bookstore is said to have been open for more than sixty years.　說法在現在，用 is said；「已經開了六十年」是從過去延續到現在，比說法早，所以用 to have been。這是句型 4。"}, {"s": "The scientist ________ in the experiment.（六格請一起打）", "zh": "大家相信那位科學家並沒有參加這項實驗。", "key": "is believed not to have joined", "acc": ["is believed not to have joined"], "e": "完整句：The scientist is believed not to have joined in the experiment.　not 要放在 to 前面；「沒有參加」是過去的事，所以用 to have joined。這是句型 4 的否定形式。"}, {"s": "The car accident ________ at around three in the morning.（五格請一起打）", "zh": "據報導這場車禍發生在凌晨三點左右。", "key": "is reported to have happened", "acc": ["is reported to have happened"], "e": "完整句：The car accident is reported to have happened at around three in the morning.　happen 沒有被動式，絕對不能寫 to have been happened；事情在過去，所以用 to have happened。這是句型 4。"}, {"s": "The two companies ________ any contract.（六格請一起打）", "zh": "當時謠傳那兩家公司從來沒有簽過任何合約。", "key": "were rumored never to have signed", "acc": ["were rumored never to have signed"], "e": "完整句：The two companies were rumored never to have signed any contract.　「當時謠傳」表示說法在過去，主詞是複數，所以用 were rumored；never 放在 to 前面；「從來沒簽過」比謠傳更早，所以用 to have signed。這是句型 5。"}]};

/* ---------- 選單 ---------- */
const menu=document.getElementById('menu'), mBtn=document.getElementById('mBtn'),
      bd=document.getElementById('backdrop');
function openMenu(){menu.classList.add('on');bd.classList.add('on');mBtn.textContent='✕ 關閉';}
function closeMenu(){menu.classList.remove('on');bd.classList.remove('on');mBtn.textContent='☰ 選單';}
mBtn.addEventListener('click',e=>{e.stopPropagation();menu.classList.contains('on')?closeMenu():openMenu();});
bd.addEventListener('click',closeMenu);
document.addEventListener('click',e=>{if(menu.classList.contains('on')&&!menu.contains(e.target)&&e.target!==mBtn)closeMenu();});
window.addEventListener('scroll',()=>{if(window.scrollY>150&&menu.classList.contains('on'))closeMenu();},{passive:true});

/* ---------- 分頁 ---------- */
const panes=[...document.querySelectorAll('.pane')], items=[...document.querySelectorAll('.navItem[data-t]')];
function show(id){
  panes.forEach(p=>p.classList.toggle('on',p.id===id));
  items.forEach(b=>b.classList.toggle('act',b.dataset.t===id));
  window.scrollTo({top:0,behavior:'smooth'});
}
items.forEach(b=>b.addEventListener('click',()=>{show(b.dataset.t);closeMenu();}));
show('t0');

/* ---------- 計分列 ---------- */
const sb=document.getElementById('scorebar');
document.getElementById('scoreToggle').addEventListener('click',()=>{sb.classList.toggle('on');closeMenu();});
let total=0, round=0;
const elT=document.getElementById('total'), elR=document.getElementById('round'),
      elMax=document.getElementById('roundMax'), elBar=document.getElementById('bar');
function setMax(n){elMax.textContent=n;elBar.style.width=Math.min(100,round/n*100)+'%';}
function addScore(ok,max){
  total=Math.max(0,total+(ok?200:-50));
  if(ok) round+=200;
  elT.textContent=total; elR.textContent=round;
  elBar.style.width=Math.min(100,round/max*100)+'%';
  elT.classList.remove('pop'); void elT.offsetWidth; elT.classList.add('pop');
}

/* ---------- Toast ---------- */
let tTimer;
const toast=document.getElementById('toast');
function say(msg){toast.textContent=msg;toast.classList.add('on');clearTimeout(tTimer);
  tTimer=setTimeout(()=>toast.classList.remove('on'),3500);}

/* ---------- 煙火 ---------- */
const cv=document.getElementById('fw'), ctx=cv.getContext('2d');
let parts=[], raf=null;
function fit(){cv.width=innerWidth;cv.height=innerHeight;}
fit(); addEventListener('resize',fit);
function boom(){
  const cx=Math.random()*innerWidth*.6+innerWidth*.2, cy=Math.random()*innerHeight*.4+innerHeight*.15;
  const cols=['#F0781E','#F4739C','#FFC457','#FF9A3C','#FFD8E4','#C9560B'];
  for(let i=0;i<70;i++){const a=Math.random()*Math.PI*2,s=Math.random()*5+1.5;
    parts.push({x:cx,y:cy,vx:Math.cos(a)*s,vy:Math.sin(a)*s,l:1,c:cols[i%cols.length]});}
  if(!raf) raf=requestAnimationFrame(loop);
}
function loop(){
  ctx.clearRect(0,0,cv.width,cv.height);
  parts=parts.filter(p=>p.l>0);
  parts.forEach(p=>{p.x+=p.vx;p.y+=p.vy;p.vy+=.06;p.vx*=.99;p.l-=.014;
    ctx.globalAlpha=Math.max(p.l,0);ctx.fillStyle=p.c;
    ctx.beginPath();ctx.arc(p.x,p.y,2.6,0,7);ctx.fill();});
  ctx.globalAlpha=1;
  if(parts.length) raf=requestAnimationFrame(loop); else {raf=null;ctx.clearRect(0,0,cv.width,cv.height);}
}

/* ---------- 朗讀 ---------- */
function speak(txt){
  if(!('speechSynthesis' in window)){say('此裝置不支援語音朗讀');return;}
  speechSynthesis.cancel();
  const u=new SpeechSynthesisUtterance(txt.replace(/[（(][^）)]*[）)]/g,' '));
  u.lang='en-US'; u.rate=0.9; speechSynthesis.speak(u);
}

/* ---------- 下拉式選擇題（三次機會、前兩次不給提示也不給正解） ---------- */
const L=['A','B','C','D'];
function buildMC(box, list, prefix, label, max){
  const wrap=document.getElementById(box);
  list.forEach((it,i)=>{
    const d=document.createElement('div'); d.className='q'; d.id=prefix+i;
    const opts=it.o.map((o,j)=>'<option value="'+j+'">('+L[j]+') '+o+'</option>').join('');
    const stem=it.s.replace('@','<select class="blank"><option value="-1">▼ 請選擇</option>'+opts+'</select>');
    d.innerHTML='<p class="stem"><span class="qn">'+(i+1)+'.</span> '+stem+'</p>'+
      '<p class="zhq">'+it.zh+'</p><div class="fb"></div>';
    const sel=d.querySelector('select'), fb=d.querySelector('.fb');
    let tries=0, done=false;
    sel.addEventListener('change',()=>{
      const v=+sel.value; if(v<0||done) return;
      tries++;
      const ok=v===it.k;
      if(ok){
        done=true; sel.disabled=true; sel.classList.remove('no'); sel.classList.add('ok');
        d.classList.remove('no'); d.classList.add('ok');
        fb.className='fb on ok';
        fb.innerHTML='🎉 <b>答對了！</b><br>正確答案：('+L[it.k]+') '+it.o[it.k]+'<br>詳解｜'+it.e;
        REC.push({sec:label,n:i+1,q:it.s.replace('@','________'),
          my:'('+L[v]+') '+it.o[v],ans:'('+L[it.k]+') '+it.o[it.k],ok:true});
        addScore(true,max); boom(); say('🎃 答對了！');
      } else if(tries<3){
        sel.classList.add('no'); d.classList.add('no');
        fb.className='fb on no';
        fb.innerHTML='💪 <b>再想一想，換一個選項試試看！</b>';
        sel.value='-1';
        addScore(false,max); say('再想一想！');
      } else {
        done=true; sel.disabled=true; sel.classList.add('no'); d.classList.add('no');
        fb.className='fb on no';
        fb.innerHTML='📖 <b>我們一起看解答</b><br>正確答案：('+L[it.k]+') '+it.o[it.k]+'<br>詳解｜'+it.e;
        REC.push({sec:label,n:i+1,q:it.s.replace('@','________'),
          my:'('+L[v]+') '+it.o[v],ans:'('+L[it.k]+') '+it.o[it.k],ok:false});
        addScore(false,max); say('沒關係，把詳解讀懂就賺到了');
      }
      setTimeout(()=>fb.scrollIntoView({behavior:'smooth',block:'center'}),120);
    });
    wrap.appendChild(d);
  });
}

/* ---------- 打字作答（三次機會、前兩次不給提示也不給正解） ---------- */
function norm(t){return t.toLowerCase().replace(/[.,!?;:"'’“”]/g,'').replace(/\s+/g,' ').trim();}
function buildTyped(box, list, label, max, multiline){
  const wrap=document.getElementById(box);
  list.forEach((it,i)=>{
    const d=document.createElement('div'); d.className='q';
    const field=multiline
      ? '<textarea class="tin ta" placeholder="請在此輸入你的答案…"></textarea>'
      : '<input class="tin" type="text" placeholder="請在此輸入你的答案…">';
    d.innerHTML='<p class="stem"><span class="qn">'+(i+1)+'.</span> '+it.s+'</p>'+
      '<p class="zhq">'+it.zh+'</p>'+field+
      '<div class="btnRow"><button class="sendBtn">✅ 送出答案</button></div><div class="fb"></div>';
    const inp=d.querySelector('.tin'), btn=d.querySelector('.sendBtn'), fb=d.querySelector('.fb');
    let done=false, n=0;
    function grade(){
      if(done) return;
      const v=norm(inp.value);
      if(!v){say('先把答案打進格子裡喔');return;}
      const ok=it.acc.some(a=>norm(a)===v);
      if(ok){
        done=true; inp.classList.add('ok'); inp.readOnly=true;
        fb.className='fb on ok';
        fb.innerHTML='🎉 <b>完全正確！</b><br>參考答案：'+it.key+'<br>詳解｜'+it.e;
        REC.push({sec:label,n:i+1,q:it.s,my:inp.value.trim(),ans:it.key,ok:true});
        addScore(true,max); boom(); say('🎃 打字全對！');
      } else {
        n++;
        if(n<3){
          fb.className='fb on no';
          fb.innerHTML='💪 <b>差一點，再試一次！</b>';
          say('再試一次！'); inp.focus();
          if(inp.select) inp.select();
        } else {
          done=true; inp.readOnly=true;
          fb.className='fb on no';
          fb.innerHTML='📖 <b>我們一起看解答</b><br>參考答案：'+it.key+'<br>詳解｜'+it.e;
          REC.push({sec:label,n:i+1,q:it.s,my:inp.value.trim(),ans:it.key,ok:false});
          say('把詳解讀懂就賺到了');
        }
      }
      setTimeout(()=>fb.scrollIntoView({behavior:'smooth',block:'center'}),120);
    }
    btn.addEventListener('click',grade);
    if(!multiline) inp.addEventListener('keydown',e=>{if(e.key==='Enter'){e.preventDefault();grade();}});
    wrap.appendChild(d);
  });
}

/* ---------- 練習成果輸出 ---------- */
const REC=[];
function meta(){
  const pick=c=>{let v='';document.querySelectorAll('.'+c).forEach(el=>{if(el.value.trim())v=el.value.trim();});return v;};
  const nm=pick('sName'), cl=pick('sClass');
  document.querySelectorAll('.sName').forEach(el=>el.value=nm);
  document.querySelectorAll('.sClass').forEach(el=>el.value=cl);
  return {nm:nm, cl:cl, now:new Date().toLocaleString('zh-TW'),
    okN:REC.filter(r=>r.ok).length, fn:('KUSO文法U3語態_練習成果_'+(cl||'班級座號')+'_'+(nm||'姓名'))};
}
const SECS=['文法選擇','歷屆試題','填空','引導式翻譯','句型轉換','句型填空','客觀說法翻譯'];
function esc(t){return String(t).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');}
function plain(t){return String(t).replace(/<[^>]+>/g,'');}
function reportHTML(){
  const m=meta();
  let rows='';
  SECS.forEach(sc=>{
    const list=REC.filter(r=>r.sec===sc); if(!list.length) return;
    rows+='<h2>'+sc+'</h2><table><tr><th>題號</th><th>題目</th><th>我的作答</th><th>參考答案</th><th>結果</th></tr>';
    list.forEach(r=>{
      rows+='<tr><td>'+r.n+'</td><td>'+esc(plain(r.q))+'</td><td>'+esc(r.my||'（未作答）')+
        '</td><td>'+esc(plain(r.ans))+'</td><td>'+(r.ok?'✔ 答對':'✘ 待加強')+'</td></tr>';
    });
    rows+='</table>';
  });
  return {m:m, html:'<!DOCTYPE html><html lang="zh-TW"><head><meta charset="utf-8">'+
   '<meta name="viewport" content="width=device-width,initial-scale=1"><title>'+esc(m.fn)+'</title><style>'+
   'body{font-family:"Microsoft JhengHei","Heiti TC","Segoe UI",sans-serif;color:#3a2010;padding:22px;line-height:1.6}'+
   'h1{font-size:20px;border-bottom:3px solid #F0781E;padding-bottom:6px}'+
   'h2{font-size:16px;background:#FFE7C9;padding:5px 9px;border-radius:6px;margin-top:18px}'+
   '.meta{font-size:13.5px;margin:8px 0 4px}'+
   'table{border-collapse:collapse;width:100%;font-size:12.5px;margin-top:6px}'+
   'th,td{border:1px solid #E5C6A6;padding:5px 7px;vertical-align:top;text-align:left}'+
   'th{background:#FFF1E0} @page{margin:14mm}'+
   '</style></head><body>'+
   '<h1>🎃 KUSO 文法 U3 語態｜練習成果單</h1>'+
   '<p class="meta">班級座號：'+esc(m.cl||'____________')+'　　姓名：'+esc(m.nm||'____________')+'　　完成時間：'+m.now+'</p>'+
   '<p class="meta">作答題數：'+REC.length+' 題　　答對：'+m.okN+' 題　　累計總分：'+total+' 分</p>'+
   rows+
   '<p class="meta" style="margin-top:18px">※ 請將本頁另存為 PDF 或直接上傳，繳交至 Kristie 老師的 Google Classroom 作業繳交區。</p>'+
   '</body></html>'};
}
function saveFile(name, text, mime){
  try{
    const blob=new Blob(['﻿'+text], {type:mime+';charset=utf-8'});
    if(window.navigator && window.navigator.msSaveOrOpenBlob){
      window.navigator.msSaveOrOpenBlob(blob,name); say('已下載：'+name); return true;
    }
    const url=URL.createObjectURL(blob);
    const a=document.createElement('a');
    a.href=url; a.download=name; a.rel='noopener';
    document.body.appendChild(a); a.click();
    setTimeout(()=>{URL.revokeObjectURL(url);a.remove();},1500);
    say('已下載：'+name+'（請到「下載」資料夾找檔案）');
    return true;
  }catch(err){
    showReport(); say('無法直接下載，已在畫面上開啟成果單，請按列印或長按複製');
    return false;
  }
}
function needRec(){ if(!REC.length){say('先完成至少一題再下載喔');return false;} return true; }
function dlHTML(){ if(!needRec()) return; const r=reportHTML(); saveFile(r.m.fn+'.html', r.html, 'text/html'); }
function showReport(){
  const r=reportHTML();
  const body=r.html.slice(r.html.indexOf('<body>')+6, r.html.indexOf('</body>'));
  let ov=document.getElementById('printOverlay');
  if(!ov){ov=document.createElement('div');ov.id='printOverlay';document.body.appendChild(ov);}
  ov.innerHTML='<div class="poInner">'+body+
    '<div class="poBtns"><button class="sendBtn" id="poPrint">🖨️ 列印／另存為 PDF</button>'+
    '<button class="sendBtn" id="poHtm">🌐 下載網頁檔</button>'+
    '<button class="reveal" id="poClose">✕ 關閉</button></div></div>';
  ov.style.display='block';
  document.body.classList.add('printing');
  document.getElementById('poPrint').onclick=()=>window.print();
  document.getElementById('poHtm').onclick=dlHTML;
  document.getElementById('poClose').onclick=()=>{ov.style.display='none';document.body.classList.remove('printing');};
  ov.scrollTop=0;
}
function dlPDF(){
  if(!needRec()) return;
  showReport();
  setTimeout(()=>{
    try{ window.print(); say('列印視窗中請把印表機選成「另存為 PDF」'); }
    catch(err){ say('列印被瀏覽器擋住了，請改按「🌐 下載成果單 網頁檔」'); }
  },400);
}
document.addEventListener('click',e=>{
  if(e.target.closest('.pdfBtn')) dlPDF();
  else if(e.target.closest('.htmBtn')) dlHTML();
});

/* ---------- 建立所有練習 ---------- */
const MAXR=(DATA.mc.length+DATA.exam.length+DATA.fill.length+DATA.trans.length
           +DATA.conv.length+DATA.obj.length+DATA.objt.length)*200;
setMax(MAXR);
buildMC('mcBox',DATA.mc,'mc','文法選擇',MAXR);
buildMC('examBox',DATA.exam,'ex','歷屆試題',MAXR);
buildTyped('fillBox',DATA.fill,'填空',MAXR,false);
buildTyped('transBox',DATA.trans,'引導式翻譯',MAXR,false);
buildTyped('convBox',DATA.conv,'句型轉換',MAXR,false);
buildTyped('objBox',DATA.obj,'句型填空',MAXR,false);
buildTyped('objtBox',DATA.objt,'客觀說法翻譯',MAXR,false);

/* ---------- 3D 翻卡與朗讀 ---------- */
document.addEventListener('click',e=>{
  const sp=e.target.closest('.spk[data-say]');
  if(sp){e.stopPropagation();speak(sp.dataset.say);return;}
  const c=e.target.closest('.fc'); if(c) c.classList.toggle('on');
});

/* ---------- 參考解答（點擊才顯示） ---------- */
document.addEventListener('click',e=>{
  const b=e.target.closest('.reveal'); if(!b) return;
  const box=b.nextElementSibling;
  const on=box.classList.toggle('on');
  b.textContent=on?'📕 收起解答':'📖 參考解答';
  if(on) setTimeout(()=>box.scrollIntoView({behavior:'smooth',block:'center'}),120);
});
say('🎃 歡迎！按右上角「☰ 選單」切換單元與計分列');
</script>
</body>
</html>
