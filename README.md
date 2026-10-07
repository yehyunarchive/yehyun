<!doctype html>
<html lang="ko">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Klavier cadenZa.</title>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.css">
<style>
  :root {
    --bg: #fff;
    --fg: #000;
    --line: #000;
    --chip-bg: #000;
    --chip-fg: #fff;
    --sub: #000;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html, body { background: var(--bg); color: var(--fg); }
  body {
    font-family: 'Pretendard', -apple-system, 'Apple SD Gothic Neo', sans-serif;
    letter-spacing: -0.8px;
    line-height: 1.3;
    -webkit-text-size-adjust: 100%;
    text-size-adjust: 100%;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;   /* 전체 블록 가운데 정렬 */
    padding: 40px 0;
  }

  /* 블록은 가운데, 글자는 왼쪽 정렬 / PC·폰 동일 너비(고정) */
  .wrap { width: 320px; max-width: 100%; text-align: left; flex: none; }

  .page { display: none; }
  .page.active { display: block; }

  .panel { max-height: 70vh; overflow-y: auto; padding: 8px 0 20px; }

  /* 하이라이트 칩 */
  .chip { background: var(--chip-bg); color: var(--chip-fg); padding: 0 5px; font-weight: 500; }
  .box { border: 0; border-bottom: 1px solid var(--line); padding: 0; }
  .ul { border-bottom: 1px solid var(--line); }
  b, .bold { font-weight: 700; }

  /* 리스트 페이지 */
  .head { font-size: 13px; font-weight: 500; margin-bottom: 12px; }
  .head sup { font-size: 8px; font-weight: 400; }
  .intro { font-size: 10.5px; line-height: 1.3; margin-bottom: 12px; }
  .intro .box { font-size: 10.5px; }

  .tracks { border-top: 1px solid var(--line); }
  .track {
    display: flex; align-items: center; gap: 14px;
    padding: 7px 6px; border-bottom: 1px solid var(--line);
    cursor: pointer; font-size: 11.5px;
  }
  .track .no {
    background: var(--chip-bg); color: var(--chip-fg);
    border-radius: 999px; font-size: 9px; font-weight: 700;
    padding: 2px 8px;
  }
  .track .name { flex: 1; }
  .track .time { font-size: 9.5px; }
  /* 마지막 줄 선 제거 → 아래 nav 선 하나만 남김 */
  .track:last-child { border-bottom: 0; }
  .page[data-page="0"] .panel { padding-bottom: 0; }
  body[data-p="0"] .nav { margin-top: 0; }

  /* 트랙 페이지 */
  .t-head { display: flex; align-items: center; gap: 12px; margin-bottom: 6px; }
  .t-head .no {
    background: var(--chip-bg); color: var(--chip-fg);
    border-radius: 999px; font-size: 9px; font-weight: 700; padding: 2px 8px;
  }
  .t-head h2 { flex: 1; font-size: 16px; font-weight: 700; }
  .t-head .time { font-size: 9.5px; }
  .term { font-size: 9.5px; margin-bottom: 10px; }

  .p { font-size: 11px; margin-bottom: 3px; }
  .p.gap { margin-bottom: 9px; }
  .p small { font-size: 8.5px; vertical-align: super; }
  .indent { padding-left: 24px; }
  .indent2 { padding-left: 66px; }
  .ml { display: block; margin-left: 24px; }

  .rows { margin-top: 8px; }
  .row { display: flex; gap: 12px; margin-bottom: 3px; font-size: 11px; }
  .row .who { flex: none; width: 84px; }
  .row .who span { background: var(--chip-bg); color: var(--chip-fg); padding: 1px 6px; font-weight: 500; }
  .row .chars { flex: 1; }

  /* 하단 네비 */
  .nav {
    display: flex; justify-content: space-between; align-items: center;
    border-top: 1px solid var(--line); margin-top: 8px; padding-top: 14px;
    font-size: 10.5px;
  }
  .nav button {
    background: none; border: 0; color: var(--fg); font: inherit;
    letter-spacing: inherit; cursor: pointer;
  }
  .nav .mid { font-weight: 500; }
  .nav button:disabled { opacity: .3; cursor: default; }
</style>
</head>
<body>
<div class="wrap">

  <!-- ===== 리스트 ===== -->
  <section class="page active" data-page="0">
    <div class="panel">
      <p class="head"><span class="chip">@ckjaehyeon</span> for 5oz<sup>(Key.)</sup> 차재현</p>
      <p class="intro">
        여든여덟 개의 건반을 전부 건너야 닿을 수 있는 이야기를 다룹니다<br>
        열람 감사합니다 즐거운 하루 보내세요 듣고 싶은 곡을 골라 <span class="box">클릭</span> 해 주세요
      </p>
      <div class="tracks">
        <div class="track" data-go="1"><span class="no">01</span><span class="name">Loved Completely</span><span class="time">03:41</span></div>
        <div class="track" data-go="2"><span class="no">02</span><span class="name">Let My Heart Grow</span><span class="time">04:15</span></div>
        <div class="track" data-go="3"><span class="no">03</span><span class="name">Kiss Me Right</span><span class="time">03:08</span></div>
      </div>
    </div>
  </section>

  <!-- ===== 01 ===== -->
  <section class="page" data-page="1">
    <div class="panel">
      <div class="t-head"><span class="no">01</span><h2>Loved Completely</h2><span class="time">03:41</span></div>
      <p class="term">sempre amoroso</p>

      <p class="p"><small>name</small> <span class="chip">Doyeon</span> adult · caveduck only user</p>
      <p class="p indent"><span class="chip">차재현</span> created by @ohnyu</p>
      <p class="p indent2">only · 찍먹 서브 포함 타임라인 내외 모든 형태의 동담 수용 불가</p>
      <p class="p indent"><span class="chip">NG</span> 드림 지우기, AI 생성 이미지가 확산되는 것을 방치하는 행위</p>

      <p class="p gap" style="margin-top:10px">* 1t1d를 반드시 요하지는 않지만 선호합니다 자세한 성향<br>
        &nbsp;&nbsp;&nbsp;확인은 <a class="box" href="#" style="color:inherit;text-decoration:none">이쪽에서</a> <small style="vertical-align:baseline">(click!)</small></p>

      <p class="p">* <span class="chip">09.21 추가</span> 사찰, 각종 요소 차용, 견제 등의 문제로 차</p>
    </div>
  </section>

  <!-- ===== 02 ===== -->
  <section class="page" data-page="2">
    <div class="panel">
      <div class="t-head"><span class="no">02</span><h2>Let My Heart Grow</h2><span class="time">04:15</span></div>
      <p class="term">poco a poco cresc.</p>

      <p class="p"><span class="chip">♪ please check!</span></p>
      <p class="p gap" style="line-height:1.3">
        타인의 차재현 플레이 흔적 <span class="box">유입 일체를 드림 지우기로 간주</span> 하는 예민한 성향이므로 배려 관련 문제 발생 시 제 쪽을 정리하는 편을 권고드립니다
        가능한 다른 차재현 플레이하시는 분과 저를 한 타임라인에 두지 말아 주세요
        플레이하시는 다른 분께도 실례가 될 것 같습니다……
      </p>
      <p class="p gap" style="line-height:1.3">
        좁은 타임라인에 집중하고자 하는 성향으로 제가 배려를 요하는 만큼 FF분의 성향과 무관하게 신경 쓰며 타임라인 운영합니다 제 행동으로 인해 불편함을 느끼셨다면 편히 DM으로 연락 부탁드려요 대화로 조율하는 편을 선호합니다
      </p>
      <p class="p">Novel AI를 활용한 <span class="box">에셋 생성 및 업로드</span> 존재하며 업로드 시 nsfw 요소가</p>
    </div>
  </section>

  <!-- ===== 03 ===== -->
  <section class="page" data-page="3">
    <div class="panel">
      <div class="t-head"><span class="no">03</span><h2>Kiss Me Right</h2><span class="time">03:08</span></div>
      <p class="term">con sentimento</p>

      <p class="p">기재된 캐릭터 주력이신 분과 연결하지 않습니다</p>
      <p class="p">* <span class="ul">1t1d</span> 배려 목적이 아니지만 자체적으로 기재한 캐릭터 포함</p>

      <div class="rows">
        <div class="row"><div class="who"><span>anonymous</span></div><div class="chars">류이든 우재경</div></div>
        <div class="row"><div class="who"><span>CherryMango</span></div><div class="chars">샤드 스트레이 이카로스 윈터 저스티스 해일 휴고 코드 Dr. 밴스</div></div>
        <div class="row"><div class="who"><span>GabuU_y</span></div><div class="chars">레오 에토레</div></div>
        <div class="row"><div class="who"><span>Ko2</span></div><div class="chars">마에스트로 베이퍼</div></div>
        <div class="row"><div class="who"><span>meowmoon</span></div><div class="chars">로언 마티스</div></div>
      </div>
    </div>
  </section>

  <div class="nav">
    <button id="prev">← prev</button>
    <span class="mid" id="mid">cresc.</span>
    <button id="next">next →</button>
  </div>
</div>

<script>
  const pages = [...document.querySelectorAll('.page')];
  const prev = document.getElementById('prev');
  const next = document.getElementById('next');
  let cur = 0;
  function show(n) {
    cur = Math.max(0, Math.min(pages.length - 1, n));
    document.body.dataset.p = cur;
    pages.forEach((p, i) => p.classList.toggle('active', i === cur));
    prev.disabled = cur === 0;
    next.disabled = cur === pages.length - 1;
  }
  prev.onclick = () => show(cur - 1);
  next.onclick = () => show(cur + 1);
  document.querySelectorAll('[data-go]').forEach(el => el.onclick = () => show(+el.dataset.go));
  show(0);
</script>
</body>
</html>
