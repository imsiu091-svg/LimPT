<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LimPT</title>
<style>
  :root{
    --orange:#FF8E32; --orange-soft:#FFB27A; --dark:#1A1918; --dark2:#252321; --dark3:#302d2a;
    --text:#F5F1EC; --muted:#A39C94; --line:#3a3633;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html,body{height:100%}
  body{font-family:"Pretendard","Apple SD Gothic Neo","Malgun Gothic",system-ui,sans-serif;background:var(--dark);color:var(--text);display:flex;flex-direction:column;overflow:hidden}

  /* 상단 바 */
  header{height:60px;display:flex;align-items:center;gap:12px;padding:0 18px;border-bottom:1px solid var(--line);background:var(--dark);flex-shrink:0}
  .logo{width:36px;height:36px;border-radius:50%;background:var(--orange);color:var(--dark);display:flex;align-items:center;justify-content:center;font-weight:900;font-size:20px;flex-shrink:0}
  .brand{font-size:22px;font-weight:800;letter-spacing:.5px}
  .brand span{color:var(--orange)}
  .menu-btn{display:none;background:none;border:none;color:var(--text);font-size:22px;cursor:pointer;margin-right:4px}
  .spacer{flex:1}
  .token-box{display:flex;align-items:center;gap:10px;background:var(--dark2);border:1px solid var(--line);border-radius:999px;padding:6px 14px 6px 10px}
  .token-icon{width:22px;height:22px;border-radius:50%;background:var(--orange);color:var(--dark);font-size:12px;font-weight:900;display:flex;align-items:center;justify-content:center}
  .token-bar{width:90px;height:8px;background:var(--dark3);border-radius:99px;overflow:hidden}
  .token-fill{height:100%;background:var(--orange);transition:width .4s}
  .token-num{font-weight:700;min-width:58px;text-align:right;font-variant-numeric:tabular-nums}
  .token-minus{color:var(--orange);font-weight:800;font-size:13px;opacity:0;transition:opacity .3s}
  .token-minus.show{opacity:1}

  /* 본문 */
  .main{flex:1;display:flex;min-height:0}
  aside{width:260px;background:var(--dark2);border-right:1px solid var(--line);display:flex;flex-direction:column;flex-shrink:0}
  .new-btn{margin:14px;padding:12px;border:none;border-radius:12px;background:var(--orange);color:var(--dark);font-weight:800;font-size:15px;cursor:pointer}
  .new-btn:hover{filter:brightness(1.07)}
  .store-title{padding:4px 18px 8px;color:var(--muted);font-size:13px;font-weight:700}
  .store{flex:1;overflow-y:auto;padding:0 10px 14px}
  .item{display:flex;align-items:center;gap:6px;padding:10px 10px;border-radius:10px;cursor:pointer;color:var(--text);font-size:14px}
  .item:hover{background:var(--dark3)}
  .item.active{background:var(--dark3);box-shadow:inset 3px 0 0 var(--orange)}
  .item .t{flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
  .item .del{background:none;border:none;color:var(--muted);cursor:pointer;font-size:15px;padding:2px 6px;border-radius:6px;opacity:0}
  .item:hover .del,.item.active .del{opacity:1}
  .item .del:hover{color:#fff;background:#c0392b}
  .empty-store{color:var(--muted);font-size:13px;padding:10px 12px}

  section.chat{flex:1;display:flex;flex-direction:column;min-width:0}
  #msgs{flex:1;overflow-y:auto;padding:26px 0}
  .wrap{max-width:780px;margin:0 auto;padding:0 20px}
  .welcome{text-align:center;margin-top:12vh}
  .welcome .big{width:84px;height:84px;margin:0 auto 18px;border-radius:50%;background:var(--orange);color:var(--dark);display:flex;align-items:center;justify-content:center;font-size:46px;font-weight:900}
  .welcome h1{font-size:28px;margin-bottom:8px}
  .welcome p{color:var(--muted)}
  .chips{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin-top:22px}
  .chip{border:1px solid var(--line);background:var(--dark2);color:var(--text);padding:9px 14px;border-radius:999px;cursor:pointer;font-size:14px}
  .chip:hover{border-color:var(--orange);color:var(--orange)}

  .row{display:flex;gap:12px;margin-bottom:22px}
  .row.user{justify-content:flex-end}
  .av{width:32px;height:32px;border-radius:50%;background:var(--orange);color:var(--dark);font-weight:900;display:flex;align-items:center;justify-content:center;flex-shrink:0}
  .bubble{max-width:85%;line-height:1.65;font-size:15.5px;word-break:break-word}
  .row.user .bubble{background:var(--orange);color:var(--dark);padding:10px 16px;border-radius:18px 18px 4px 18px;font-weight:500;white-space:pre-wrap}
  .row.ai .bubble{padding-top:4px}
  .bubble pre{background:#0f0e0d;border:1px solid var(--line);border-radius:10px;padding:12px;overflow-x:auto;margin:8px 0;font-size:13.5px}
  .bubble code{font-family:Consolas,Menlo,monospace;background:#0f0e0d;padding:1px 5px;border-radius:5px;font-size:.92em}
  .bubble pre code{background:none;padding:0}
  .bubble strong{color:var(--orange-soft)}
  .bubble ul,.bubble ol{padding-left:22px;margin:6px 0}
  .bubble h3{font-size:16.5px;margin:10px 0 4px;color:var(--orange)}
  .cost-tag{display:inline-block;margin-top:8px;font-size:12px;color:var(--muted);border:1px solid var(--line);border-radius:999px;padding:2px 10px}
  .err{color:#ff8a7a}
  .retry{margin-top:8px;background:var(--dark3);border:1px solid var(--line);color:var(--text);border-radius:8px;padding:6px 12px;cursor:pointer}
  .dots span{display:inline-block;width:7px;height:7px;margin-right:4px;border-radius:50%;background:var(--orange);animation:b 1s infinite}
  .dots span:nth-child(2){animation-delay:.15s}.dots span:nth-child(3){animation-delay:.3s}
  @keyframes b{0%,80%,100%{opacity:.25;transform:translateY(0)}40%{opacity:1;transform:translateY(-4px)}}

  /* 입력창 */
  .input-area{padding:12px 0 18px;flex-shrink:0}
  .box{display:flex;align-items:flex-end;gap:10px;background:var(--dark2);border:1.5px solid var(--line);border-radius:18px;padding:10px 10px 10px 16px}
  .box:focus-within{border-color:var(--orange)}
  textarea{flex:1;resize:none;border:none;outline:none;background:transparent;color:var(--text);font:inherit;font-size:15.5px;max-height:180px;line-height:1.5;padding:6px 0}
  textarea::placeholder{color:var(--muted)}
  .send{width:40px;height:40px;border-radius:12px;border:none;background:var(--orange);color:var(--dark);font-size:19px;font-weight:900;cursor:pointer;flex-shrink:0}
  .send:disabled{background:var(--dark3);color:var(--muted);cursor:not-allowed}
  .hint{text-align:center;color:var(--muted);font-size:12px;margin-top:8px}

  /* 토큰 0 화면 */
  .lock{display:none;text-align:center;background:var(--dark2);border:1.5px solid var(--orange);border-radius:18px;padding:18px}
  .lock.show{display:block}
  .lock b{color:var(--orange);font-size:28px;font-variant-numeric:tabular-nums;display:block;margin:6px 0}

  /* 권한 / 연결 안내 창 */
  .modal-bg{position:fixed;inset:0;background:rgba(0,0,0,.6);display:none;align-items:center;justify-content:center;z-index:50;padding:20px}
  .modal-bg.show{display:flex}
  .modal{background:var(--dark2);border:1px solid var(--line);border-radius:18px;padding:24px;max-width:420px;width:100%}
  .modal h2{font-size:19px;margin-bottom:10px;display:flex;align-items:center;gap:10px}
  .modal p{color:var(--muted);font-size:14px;line-height:1.6;margin-bottom:8px}
  .modal .btns{display:flex;gap:8px;justify-content:flex-end;margin-top:16px}
  .modal button{padding:10px 16px;border-radius:10px;border:none;font-weight:700;cursor:pointer}
  .ok{background:var(--orange);color:var(--dark)}
  .no{background:var(--dark3);color:var(--text)}

  @media (max-width:760px){
    aside{position:fixed;top:60px;bottom:0;left:0;z-index:40;transform:translateX(-100%);transition:transform .25s}
    aside.open{transform:none}
    .menu-btn{display:block}
    .token-bar{display:none}
    .brand{font-size:19px}
  }
</style>
</head>
<body>

<header>
  <button class="menu-btn" id="menuBtn" aria-label="저장소 열기">☰</button>
  <div class="logo">L</div>
  <div class="brand">Lim<span>PT</span></div>
  <div class="spacer"></div>
  <div class="token-box" title="토큰">
    <div class="token-icon">T</div>
    <div class="token-bar"><div class="token-fill" id="tokenFill"></div></div>
    <div class="token-num" id="tokenNum">100</div>
    <div class="token-minus" id="tokenMinus">-0</div>
  </div>
</header>

<div class="main">
  <aside id="side">
    <button class="new-btn" id="newBtn">＋ 새 대화</button>
    <div class="store-title">📁 대화 저장소</div>
    <div class="store" id="store"></div>
  </aside>

  <section class="chat">
    <div id="msgs"><div class="wrap" id="msgWrap"></div></div>
    <div class="input-area">
      <div class="wrap">
        <div class="box" id="inputBox">
          <textarea id="input" rows="1" placeholder="LimPT에게 무엇이든 물어보세요..."></textarea>
          <button class="send" id="sendBtn" aria-label="보내기">↑</button>
        </div>
        <div class="lock" id="lock">
          토큰을 모두 사용했어요 😴<br>
          <b id="countdown">10:00</b>
          <span style="color:var(--muted);font-size:13px">시간이 지나면 토큰 100개가 자동으로 충전돼요</span>
        </div>
        <div class="hint">대화는 자동으로 저장소에 저장돼요 · 어려운 질문일수록 토큰을 더 많이 써요</div>
      </div>
    </div>
  </section>
</div>

<!-- 인터넷 연결 허용 안내 창 -->
<div class="modal-bg" id="netModal">
  <div class="modal">
    <h2><span class="logo" style="width:28px;height:28px;font-size:15px">L</span> 인터넷 연결 허용</h2>
    <p>LimPT가 대답하려면 인터넷으로 AI 서버(Google)에 연결해야 해요.</p>
    <p>‘허용’을 누르면 연결을 시험해 볼게요. 만약 브라우저나 백신 프로그램이 따로 허용을 물어보면 그것도 ‘허용’해 주세요.</p>
    <div class="btns">
      <button class="no" id="netNo">나중에</button>
      <button class="ok" id="netOk">허용</button>
    </div>
  </div>
</div>

<script>
/* ===================== 설정 ===================== */
const API_KEY = "AQ.Ab8RN6Ji0M3guxgzv-PJGHw74zZypv-o530owbi8cJh3x4O-5Q";
// 빠른 순서대로 시도하는 모델 목록
// 이 키로 실제 시험해서 확인한 모델 (가장 빠른 것부터)
const MODELS = [
  { name:"gemini-flash-lite-latest", config:{} },
  { name:"gemini-3.1-flash-lite",    config:{} },
  { name:"gemini-3.5-flash-lite",    config:{} }
];
const MAX_TOKENS = 100;
const RECHARGE_MS = 10 * 60 * 1000; // 10분

const SYSTEM_PROMPT = `너는 "LimPT"라는 이름의 친절한 AI야. 초등학생부터 어른까지 모든 나이의 사람이 너와 대화해.
규칙:
- 사용자의 질문에 정확하고 알맞게 대답해. "강아지가 뭐야?" 같은 쉬운 질문도 절대 무시하지 말고 성실하게 대답해.
- 한국어로 질문하면 한국어로 대답해. 쉽고 친근한 말투를 써.
- 쉬운 질문은 짧게, 어려운 질문은 자세하게 대답해.
- 폭력적이거나 위험하거나 어린이에게 맞지 않는 내용은 정중하게 거절해.
- 답변의 맨 마지막 줄에는 반드시 <<COST:숫자>> 형식으로 이번 대화에 쓸 토큰 수를 적어.
  기준: 인사나 아주 쉬운 질문 1~2, 보통 질문 3~5, 길고 어려운 설명·코드·글쓰기 6~10.
  숫자는 반드시 1부터 10 사이여야 해. 예: "강아지가 뭐야?" → <<COST:1>>
  이 표시는 답변 맨 끝에 딱 한 번만 쓰고, 이 표시에 대해 따로 설명하지 마.`;

/* ===================== 저장 데이터 ===================== */
const store = {
  get(k, d){ try{ const v = localStorage.getItem(k); return v ? JSON.parse(v) : d; }catch(e){ return d; } },
  set(k, v){ try{ localStorage.setItem(k, JSON.stringify(v)); }catch(e){} }
};
let chats = store.get("limpt_chats", []);          // [{id,title,messages:[{role,text,cost}],updated}]
let tokens = store.get("limpt_tokens", MAX_TOKENS);
let emptyAt = store.get("limpt_emptyAt", null);    // 토큰이 0이 된 시각
let currentId = null;
let busy = false;
let workingModel = store.get("limpt_model", null);
let workingHost = store.get("limpt_host", null);

const $ = id => document.getElementById(id);
const msgWrap = $("msgWrap"), msgsBox = $("msgs"), input = $("input"), sendBtn = $("sendBtn");

/* ===================== 토큰 ===================== */
function renderTokens(){
  $("tokenNum").textContent = tokens + " / " + MAX_TOKENS;
  $("tokenFill").style.width = (tokens / MAX_TOKENS * 100) + "%";
  const locked = tokens <= 0;
  $("lock").classList.toggle("show", locked);
  $("inputBox").style.display = locked ? "none" : "flex";
}
function useTokens(n){
  tokens = Math.max(0, tokens - n);
  if(tokens === 0 && !emptyAt){ emptyAt = Date.now(); store.set("limpt_emptyAt", emptyAt); }
  store.set("limpt_tokens", tokens);
  const m = $("tokenMinus"); m.textContent = "-" + n; m.classList.add("show");
  setTimeout(() => m.classList.remove("show"), 1600);
  renderTokens();
}
function tickRecharge(){
  if(tokens <= 0){
    if(!emptyAt){ emptyAt = Date.now(); store.set("limpt_emptyAt", emptyAt); }
    const left = RECHARGE_MS - (Date.now() - emptyAt);
    if(left <= 0){
      tokens = MAX_TOKENS; emptyAt = null;
      store.set("limpt_tokens", tokens); store.set("limpt_emptyAt", null);
      renderTokens();
    } else {
      const s = Math.ceil(left / 1000);
      $("countdown").textContent = String(Math.floor(s/60)).padStart(2,"0") + ":" + String(s%60).padStart(2,"0");
    }
  }
}
setInterval(tickRecharge, 1000);

/* ===================== 저장소(사이드바) ===================== */
function saveChats(){ store.set("limpt_chats", chats); }
function renderStore(){
  const el = $("store"); el.innerHTML = "";
  if(!chats.length){ el.innerHTML = '<div class="empty-store">아직 저장된 대화가 없어요.<br>대화를 시작하면 자동으로 저장돼요!</div>'; return; }
  [...chats].sort((a,b) => b.updated - a.updated).forEach(c => {
    const d = document.createElement("div");
    d.className = "item" + (c.id === currentId ? " active" : "");
    d.innerHTML = '<span>💬</span><span class="t"></span><button class="del" title="삭제">🗑</button>';
    d.querySelector(".t").textContent = c.title;
    d.onclick = () => { openChat(c.id); $("side").classList.remove("open"); };
    d.querySelector(".del").onclick = e => {
      e.stopPropagation();
      if(!confirm("‘" + c.title + "’ 대화를 저장소에서 삭제할까요?")) return;
      chats = chats.filter(x => x.id !== c.id); saveChats();
      if(currentId === c.id) newChat(); else renderStore();
    };
    el.appendChild(d);
  });
}
function getChat(){ return chats.find(c => c.id === currentId); }
function newChat(){ currentId = null; renderMessages(); renderStore(); input.focus(); }
function openChat(id){ currentId = id; renderMessages(); renderStore(); }

/* ===================== 메시지 표시 ===================== */
function esc(s){ return s.replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;"); }
function md(text){
  const blocks = [];
  let s = text.replace(/```(\w*)\n?([\s\S]*?)(```|$)/g, (_, l, code) => { blocks.push(code); return "\u0000" + (blocks.length-1) + "\u0000"; });
  s = esc(s)
    .replace(/`([^`\n]+)`/g, "<code>$1</code>")
    .replace(/\*\*([^*\n]+)\*\*/g, "<strong>$1</strong>")
    .replace(/^#{1,4} (.+)$/gm, "<h3>$1</h3>")
    .replace(/^(?:[-*] .+(?:\n|$))+/gm, m => "<ul>" + m.trim().split("\n").map(l => "<li>" + l.replace(/^[-*] /,"") + "</li>").join("") + "</ul>")
    .replace(/^(?:\d+\. .+(?:\n|$))+/gm, m => "<ol>" + m.trim().split("\n").map(l => "<li>" + l.replace(/^\d+\. /,"") + "</li>").join("") + "</ol>")
    .replace(/\n/g, "<br>")
    .replace(/<\/(h3|ul|ol)><br>/g, "</$1>");
  return s.replace(/\u0000(\d+)\u0000/g, (_, i) => "<pre><code>" + esc(blocks[i]) + "</code></pre>");
}
function welcome(){
  msgWrap.innerHTML = `<div class="welcome"><div class="big">L</div><h1>안녕하세요! 저는 LimPT예요</h1>
  <p>궁금한 것을 무엇이든 물어보세요. 처음에는 토큰 100개로 시작해요.</p>
  <div class="chips">
    <button class="chip">강아지가 뭐야?</button>
    <button class="chip">무지개는 왜 생겨?</button>
    <button class="chip">재미있는 수수께끼 내줘</button>
    <button class="chip">파이썬으로 구구단 만드는 법</button>
  </div></div>`;
  msgWrap.querySelectorAll(".chip").forEach(c => c.onclick = () => { input.value = c.textContent; send(); });
}
function addRow(role, html){
  const row = document.createElement("div");
  row.className = "row " + role;
  row.innerHTML = role === "ai" ? '<div class="av">L</div><div class="bubble"></div>' : '<div class="bubble"></div>';
  row.querySelector(".bubble").innerHTML = html;
  msgWrap.appendChild(row);
  scrollDown();
  return row.querySelector(".bubble");
}
function scrollDown(){ msgsBox.scrollTop = msgsBox.scrollHeight; }
function renderMessages(){
  const c = getChat();
  if(!c || !c.messages.length){ welcome(); return; }
  msgWrap.innerHTML = "";
  c.messages.forEach(m => {
    if(m.role === "user") addRow("user", esc(m.text));
    else addRow("ai", md(m.text) + (m.cost ? `<div class="cost-tag">토큰 -${m.cost}</div>` : ""));
  });
}

/* ===================== AI 연결 ===================== */
function candidates(){
  const list = MODELS.map(m => ({
    model: m.name, config: m.config,
    url: `https://generativelanguage.googleapis.com/v1beta/models/${m.name}:streamGenerateContent?alt=sse&key=${API_KEY}`
  }));
  if(workingModel){
    const i = list.findIndex(x => x.model === workingModel);
    if(i > 0) list.unshift(list.splice(i,1)[0]);
  }
  return list;
}
// 미리보기 창(샌드박스) 안에서 열렸는지 확인
function inPreview(){
  try{ return window.self !== window.top; }catch(e){ return true; }
}

async function streamAI(history, onText){
  const contents = history.slice(-20).map(m => ({ role: m.role === "user" ? "user" : "model", parts:[{ text:m.text }] }));
  const body = {
    contents,
    systemInstruction: { parts:[{ text: SYSTEM_PROMPT }] }
  };
  let lastErr = null;
  for(const c of candidates()){
    const b = { ...body, generationConfig: { temperature: 0.7, maxOutputTokens: 2048, ...c.config } };
    let res;
    try{
      res = await fetch(c.url, { method:"POST", headers:{ "Content-Type":"application/json" }, body: JSON.stringify(b) });
    }catch(e){ lastErr = { network:true, msg:e.message }; break; }
    if(!res.ok){
      let t = ""; try{ t = await res.text(); }catch(e){}
      lastErr = { status:res.status, msg:t.slice(0,300) };
      if(res.status === 429) break; // 너무 많이 요청함 → 다른 곳 시도해도 같음
      continue;
    }
    workingModel = c.model;
    store.set("limpt_model", workingModel);

    const reader = res.body.getReader(); const dec = new TextDecoder();
    let buf = "", full = "";
    while(true){
      const { done, value } = await reader.read();
      if(done) break;
      buf += dec.decode(value, { stream:true });
      const lines = buf.split("\n"); buf = lines.pop();
      for(const line of lines){
        if(!line.startsWith("data:")) continue;
        try{
          const j = JSON.parse(line.slice(5).trim());
          const parts = j.candidates?.[0]?.content?.parts || [];
          for(const p of parts){ if(p.text && !p.thought){ full += p.text; onText(full); } }
        }catch(e){}
      }
    }
    return full;
  }
  throw lastErr || { msg:"알 수 없는 오류" };
}

function splitCost(text){
  const m = text.match(/<<\s*COST\s*:\s*(\d+)\s*>>/i);
  let cost = m ? parseInt(m[1], 10) : null;
  let clean = text.replace(/<<\s*COST[^>]*>>?/gi, "").trimEnd();
  if(!cost || isNaN(cost)){ // AI가 표시를 빠뜨리면 길이로 판단
    const len = clean.length;
    cost = len < 150 ? 1 : len < 400 ? 2 : len < 900 ? 4 : len < 1800 ? 6 : 8;
  }
  return { clean, cost: Math.min(10, Math.max(1, cost)) };
}
function visible(text){ // 스트리밍 중에는 <<COST 부분 숨기기
  const i = text.indexOf("<<"); return i >= 0 ? text.slice(0, i) : text;
}

/* ===================== 보내기 ===================== */
async function send(retryText){
  const text = (retryText ?? input.value).trim();
  if(!text || busy || tokens <= 0) return;
  if(!navigator.onLine){ $("netModal").classList.add("show"); return; }

  busy = true; sendBtn.disabled = true;
  let c = getChat();
  if(!c){
    c = { id: Date.now().toString(36), title: text.slice(0, 24) + (text.length > 24 ? "…" : ""), messages: [], updated: Date.now() };
    chats.push(c); currentId = c.id; msgWrap.innerHTML = "";
  }
  if(!retryText){ c.messages.push({ role:"user", text }); addRow("user", esc(text)); }
  c.updated = Date.now(); saveChats(); renderStore();   // 자동 저장
  input.value = ""; autoGrow();

  const bubble = addRow("ai", '<div class="dots"><span></span><span></span><span></span></div>');
  try{
    const full = await streamAI(c.messages, t => { bubble.innerHTML = md(visible(t)); scrollDown(); });
    const { clean, cost } = splitCost(full);
    if(!clean) throw { msg:"빈 답변" };
    bubble.innerHTML = md(clean) + `<div class="cost-tag">토큰 -${cost}</div>`;
    c.messages.push({ role:"ai", text: clean, cost });
    c.updated = Date.now(); saveChats(); renderStore();  // 자동 저장
    useTokens(cost);
  }catch(err){
    let why = "잠시 후 다시 시도해 주세요.";
    if(err.network && inPreview()) why = "미리보기 창에서는 인터넷을 쓸 수 없어요. 파일을 <b>다운로드</b>한 다음, 다운로드한 LimPT.html을 더블클릭해서 크롬이나 엣지에서 열어 주세요.";
    else if(err.network) why = "인터넷에 연결할 수 없어요. 와이파이를 확인하거나, 학교·백신 프로그램이 googleapis.com을 막고 있는지 확인해 주세요.";
    else if(err.status === 404) why = "AI 모델을 찾을 수 없어요. (오류 404)";
    else if(err.status === 400 || err.status === 401 || err.status === 403) why = "API 키가 올바르지 않거나 권한이 없어요. (오류 " + err.status + ")";
    else if(err.status === 429) why = "질문이 너무 빨리 많이 왔어요. 1분 정도 쉬었다가 다시 해 주세요.";
    else if(err.status) why = "AI 서버 오류 (" + err.status + ")";
    bubble.innerHTML = `<span class="err">⚠️ ${why}</span><br><button class="retry">다시 시도</button>`;
    bubble.querySelector(".retry").onclick = () => { bubble.parentElement.remove(); send(text); };
    console.warn("LimPT 오류:", err);
    if(err.network && !inPreview()) $("netModal").classList.add("show");
  }
  busy = false; sendBtn.disabled = false; input.focus();
}

/* ===================== 인터넷 허용 창 ===================== */
$("netNo").onclick = () => $("netModal").classList.remove("show");
$("netOk").onclick = async () => {
  $("netModal").classList.remove("show");
  store.set("limpt_netAllowed", true);
  try{
    await fetch("https://generativelanguage.googleapis.com/", { mode:"no-cors" });
    toast("✅ 인터넷 연결이 확인됐어요! 이제 대화할 수 있어요.");
  }catch(e){
    toast("⚠️ 아직 연결이 안 돼요. 와이파이나 백신 프로그램 설정을 확인해 주세요.");
  }
};
function toast(msg){
  const t = document.createElement("div");
  t.textContent = msg;
  t.style.cssText = "position:fixed;bottom:24px;left:50%;transform:translateX(-50%);background:#252321;border:1px solid #FF8E32;color:#F5F1EC;padding:12px 18px;border-radius:12px;z-index:60;font-size:14px";
  document.body.appendChild(t); setTimeout(() => t.remove(), 3500);
}

/* ===================== 시작 ===================== */
function autoGrow(){ input.style.height = "auto"; input.style.height = Math.min(input.scrollHeight, 180) + "px"; }
input.addEventListener("input", autoGrow);
input.addEventListener("keydown", e => { if(e.key === "Enter" && !e.shiftKey && !e.isComposing){ e.preventDefault(); send(); } });
sendBtn.onclick = () => send();
$("newBtn").onclick = () => { newChat(); $("side").classList.remove("open"); };
$("menuBtn").onclick = () => $("side").classList.toggle("open");

renderTokens(); tickRecharge(); renderStore(); welcome();
if(!store.get("limpt_netAllowed", false)) $("netModal").classList.add("show");
</script>
</body>
</html>
