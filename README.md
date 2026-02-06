<!doctype html>
<html lang="ru">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>MobileGems — Донат в игры быстро и безопасно</title>
  <meta name="description" content="Донат в популярные игры. Быстро, безопасно, с поддержкой в Telegram. Оформляй заявку за 1 минуту." />
  <meta name="theme-color" content="#0b1220" />
  <style>
    :root{
      --bg:#0b1220;
      --card:#111a2e;
      --card2:#0f1730;
      --text:#e9eefc;
      --muted:#a9b5d6;
      --brand:#6ee7ff;
      --brand2:#a78bfa;
      --ok:#34d399;
      --warn:#fbbf24;
      --danger:#fb7185;
      --border: rgba(255,255,255,.10);
      --shadow: 0 18px 50px rgba(0,0,0,.35);
      --radius: 18px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font: 15px/1.5 ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial;
      color:var(--text);
      background:
        radial-gradient(1200px 800px at 10% 10%, rgba(110,231,255,.14), transparent 55%),
        radial-gradient(1000px 700px at 90% 20%, rgba(167,139,250,.14), transparent 55%),
        radial-gradient(900px 700px at 50% 100%, rgba(52,211,153,.10), transparent 55%),
        var(--bg);
      overflow-x:hidden;
    }
    a{color:inherit}
    .wrap{max-width:1120px;margin:0 auto;padding:0 18px}
    .nav{
      position:sticky;top:0;z-index:50;
      backdrop-filter:saturate(180%) blur(14px);
      background: rgba(11,18,32,.65);
      border-bottom:1px solid var(--border);
    }
    .navin{
      display:flex;align-items:center;justify-content:space-between;
      padding:12px 0;
      gap:12px;
    }
    .logo{
      display:flex;align-items:center;gap:10px;
      text-decoration:none;
    }
    .mark{
      width:36px;height:36px;border-radius:12px;
      background: linear-gradient(135deg, var(--brand), var(--brand2));
      box-shadow:0 12px 30px rgba(110,231,255,.18);
    }
    .brandtxt{display:flex;flex-direction:column;line-height:1.1}
    .brandtxt b{font-size:14px;letter-spacing:.2px}
    .brandtxt span{font-size:12px;color:var(--muted)}
    .navlinks{display:flex;gap:14px;align-items:center;flex-wrap:wrap}
    .navlinks a{
      text-decoration:none;
      color:var(--muted);
      padding:8px 10px;border-radius:12px;
      border:1px solid transparent;
    }
    .navlinks a:hover{color:var(--text);border-color:var(--border);background:rgba(255,255,255,.04)}
    .btn{
      display:inline-flex;align-items:center;justify-content:center;gap:10px;
      padding:11px 14px;border-radius:14px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.05);
      color:var(--text);
      text-decoration:none;
      box-shadow: 0 10px 30px rgba(0,0,0,.15);
      cursor:pointer;
      user-select:none;
    }
    .btn:hover{transform:translateY(-1px);background: rgba(255,255,255,.08)}
    .btn.primary{
      border-color: rgba(110,231,255,.35);
      background: linear-gradient(135deg, rgba(110,231,255,.18), rgba(167,139,250,.18));
    }
    .hero{
      padding:54px 0 22px;
      display:grid;
      grid-template-columns: 1.2fr .8fr;
      gap:18px;
      align-items:stretch;
    }
    .hcard{
      background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03));
      border:1px solid var(--border);
      border-radius: var(--radius);
      padding:22px;
      box-shadow: var(--shadow);
      overflow:hidden;
      position:relative;
      min-height: 320px;
    }
    .hcard:before{
      content:"";
      position:absolute;inset:-2px;
      background:
        radial-gradient(600px 250px at 30% 0%, rgba(110,231,255,.22), transparent 60%),
        radial-gradient(600px 250px at 80% 10%, rgba(167,139,250,.20), transparent 60%);
      pointer-events:none;
      filter: blur(10px);
      opacity:.9;
    }
    .hcard > *{position:relative}
    h1{
      margin:0 0 10px;
      font-size: 38px;
      line-height:1.1;
      letter-spacing:-.4px;
    }
    .lead{color:var(--muted);max-width:52ch;margin:0 0 16px}
    .pillrow{display:flex;gap:8px;flex-wrap:wrap;margin:14px 0 18px}
    .pill{
      display:inline-flex;align-items:center;gap:8px;
      padding:8px 10px;border-radius:999px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.04);
      color:var(--muted);
      font-size:12px;
    }
    .dot{width:8px;height:8px;border-radius:99px;background:var(--ok)}
    .cta{display:flex;gap:10px;flex-wrap:wrap;margin-top:6px}
    .side{
      display:grid;
      gap:12px;
    }
    .card{
      background: rgba(17,26,46,.7);
      border:1px solid var(--border);
      border-radius: var(--radius);
      padding:16px;
      box-shadow: 0 14px 40px rgba(0,0,0,.25);
    }
    .card h3{margin:0 0 8px;font-size:15px}
    .muted{color:var(--muted)}
    .grid3{
      display:grid;grid-template-columns:repeat(3,1fr);
      gap:12px;
      margin: 14px 0 0;
    }
    .feat{
      padding:14px;border-radius:16px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
    }
    .feat b{display:block;margin-bottom:4px}
    .section{padding:26px 0}
    .title{
      display:flex;align-items:flex-end;justify-content:space-between;gap:12px;
      margin-bottom:12px;
    }
    .title h2{margin:0;font-size:22px}
    .title p{margin:0;color:var(--muted)}
    .pricing{
      display:grid;grid-template-columns:repeat(3,1fr);
      gap:12px;
    }
    .price{
      padding:16px;border-radius:18px;border:1px solid var(--border);
      background: rgba(255,255,255,.03);
    }
    .price .tag{
      display:inline-flex;gap:8px;align-items:center;
      font-size:12px;color:var(--muted);
      border:1px solid var(--border);
      padding:6px 10px;border-radius:999px;
      margin-bottom:10px;
    }
    .price h3{margin:0 0 6px;font-size:16px}
    .price .num{font-size:28px;margin:6px 0 10px}
    .list{margin:0;padding:0;list-style:none;display:grid;gap:8px}
    .list li{display:flex;gap:10px;align-items:flex-start;color:var(--muted)}
    .check{
      width:18px;height:18px;border-radius:6px;
      background: rgba(52,211,153,.14);
      border:1px solid rgba(52,211,153,.28);
      flex:0 0 18px;
      margin-top:2px;
      position:relative;
    }
    .check:after{
      content:"";
      position:absolute;left:5px;top:3px;
      width:6px;height:9px;border-right:2px solid var(--ok);border-bottom:2px solid var(--ok);
      transform:rotate(45deg);
    }
    .formgrid{
      display:grid;grid-template-columns:1fr 1fr;gap:12px;
      align-items:start;
    }
    label{display:grid;gap:6px;color:var(--muted);font-size:12px}
    input,select,textarea{
      width:100%;
      padding:12px 12px;
      border-radius:14px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      color:var(--text);
      outline:none;
    }
    textarea{min-height:110px;resize:vertical}
    input:focus,select:focus,textarea:focus{border-color: rgba(110,231,255,.35)}
    .row{display:flex;gap:10px;flex-wrap:wrap;align-items:center}
    .mini{
      font-size:12px;color:var(--muted);
      border:1px solid var(--border);
      border-radius:999px;
      padding:6px 10px;
      background: rgba(255,255,255,.03);
    }
    .faq{display:grid;grid-template-columns:1fr 1fr;gap:12px}
    details{
      border:1px solid var(--border);
      border-radius:16px;
      background: rgba(255,255,255,.03);
      padding:12px 12px;
    }
    summary{cursor:pointer;color:var(--text);font-weight:600}
    details p{margin:8px 0 0;color:var(--muted)}
    footer{
      padding:24px 0 34px;
      border-top:1px solid var(--border);
      color:var(--muted);
    }
    .footgrid{display:flex;justify-content:space-between;gap:14px;flex-wrap:wrap}
    .badges{display:flex;gap:10px;flex-wrap:wrap}
    .badge{
      display:inline-flex;align-items:center;gap:8px;
      padding:8px 10px;border-radius:999px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      font-size:12px;
    }
    .kbd{
      font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace;
      font-size: 12px;
      padding: 2px 6px;border-radius:8px;
      border:1px solid var(--border);
      background: rgba(0,0,0,.18);
      color: var(--text);
    }
    .note{
      border-left:3px solid rgba(110,231,255,.55);
      padding-left:12px;margin:10px 0 0;color:var(--muted);
    }
    .hide-sm{display:inline-flex}
    @media (max-width: 960px){
      .hero{grid-template-columns:1fr; padding-top:28px}
      .pricing{grid-template-columns:1fr}
      .grid3{grid-template-columns:1fr}
      .formgrid{grid-template-columns:1fr}
      .faq{grid-template-columns:1fr}
      .hide-sm{display:none}
      h1{font-size:32px}
    }
  </style>
</head>
<body>
  <header class="nav">
    <div class="wrap navin">
      <a class="logo" href="#top">
        <div class="mark" aria-hidden="true"></div>
        <div class="brandtxt">
          <b>MobileGems</b>
          <span>Донат-сервис в игры</span>
        </div>
      </a>
      <nav class="navlinks">
        <a href="#how">Как это работает</a>
        <a href="#prices">Тарифы</a>
        <a href="#order">Оформить</a>
        <a href="#faq">FAQ</a>
        <a class="btn primary" href="https://t.me/mobilegemss" target="_blank" rel="noopener">
          Перейти в Telegram <span class="hide-sm">→</span>
        </a>
      </nav>
    </div>
  </header>

  <main id="top" class="wrap">
    <section class="hero">
      <div class="hcard">
        <h1>Донат в игры — быстро, прозрачно, с поддержкой в Telegram</h1>
        <p class="lead">
          Оформляй заявку за 1 минуту. Подскажем по стоимости, срокам и способу входа.
          Работаем через безопасный сценарий и фиксируем детали перед оплатой.
        </p>

        <div class="pillrow">
          <div class="pill"><span class="dot"></span> Онлайн поддержка</div>
          <div class="pill">⚡ Быстрые сроки</div>
          <div class="pill">🧾 Чек/подтверждение</div>
          <div class="pill">🔒 Конфиденциально</div>
        </div>

        <div class="cta">
          <a class="btn primary" href="#order">Оформить заявку</a>
          <a class="btn" href="https://t.me/mobilegemss" target="_blank" rel="noopener">Написать в Telegram</a>
          <a class="btn" href="#prices">Смотреть тарифы</a>
        </div>

        <p class="note">
          Важно: для некоторых игр требуется регион/платформа. Уточним в чате, чтобы всё прошло без сюрпризов.
        </p>
      </div>

      <div class="side">
        <div class="card">
          <h3>Калькулятор стоимости</h3>
          <p class="muted" style="margin:0 0 10px">Выбери игру и сумму — получишь ориентир и текст заявки.</p>

          <label>
            Игра
            <select id="game">
              <option value="PUBG Mobile">PUBG Mobile</option>
              <option value="Mobile Legends">Mobile Legends</option>
              <option value="Genshin Impact">Genshin Impact</option>
              <option value="Brawl Stars">Brawl Stars</option>
              <option value="Другая">Другая</option>
            </select>
          </label>

          <div class="row" style="margin-top:10px">
            <label style="flex:1">
              Сумма пополнения (в валюте игры/магазина)
              <input id="amount" type="number" min="1" step="1" placeholder="Напр. 500" />
            </label>
          </div>

          <div class="row" style="margin-top:10px">
            <span class="mini">Комиссия сервиса: <b id="fee">5%</b></span>
            <span class="mini">Оценка к оплате: <b id="total">—</b></span>
          </div>

          <div class="row" style="margin-top:12px">
            <button class="btn primary" id="copyText" type="button">Скопировать текст заявки</button>
            <a class="btn" href="https://t.me/mobilegemss" target="_blank" rel="noopener">Открыть Telegram</a>
          </div>

          <p class="muted" style="margin:10px 0 0;font-size:12px">
            * Это ориентир. Финальная сумма зависит от региона/платформы/курса и выбранного способа оплаты.
          </p>
        </div>

        <div class="card">
          <h3>Что нужно от тебя</h3>
          <ul class="list">
            <li><span class="check"></span><span>Игра + платформа (Android/iOS/PC/консоль)</span></li>
            <li><span class="check"></span><span>ID/ник/сервер (по игре)</span></li>
            <li><span class="check"></span><span>Сумма/пакет доната</span></li>
            <li><span class="check"></span><span>Способ связи: Telegram</span></li>
          </ul>
        </div>
      </div>
    </section>

    <section id="how" class="section">
      <div class="title">
        <div>
          <h2>Как это работает</h2>
          <p>Простой процесс без лишних шагов.</p>
        </div>
      </div>

      <div class="grid3">
        <div class="feat">
          <b>1) Оставляешь заявку</b>
          <span class="muted">На сайте или в Telegram: игра, ID, сумма, регион/платформа.</span>
        </div>
        <div class="feat">
          <b>2) Подтверждаем детали</b>
          <span class="muted">Согласуем цену, срок, способ пополнения и формат подтверждения.</span>
        </div>
        <div class="feat">
          <b>3) Выполняем донат</b>
          <span class="muted">После оплаты выполняем пополнение и присылаем результат/скрин/чек.</span>
        </div>
      </div>
    </section>

    <section id="prices" class="section">
      <div class="title">
        <div>
          <h2>Тарифы</h2>
          <p>Выбери подходящий формат. Цены — пример, замени под себя.</p>
        </div>
        <div class="badges">
          <span class="badge">⚡ Среднее время: 5–30 мин</span>
          <span class="badge">🛡️ Поддержка: 7/7</span>
        </div>
      </div>

      <div class="pricing">
        <div class="price">
          <div class="tag">Старт</div>
          <h3>Разовые пополнения</h3>
          <div class="num">Комиссия 5%</div>
          <ul class="list">
            <li><span class="check"></span><span>Подходит для большинства игр</span></li>
            <li><span class="check"></span><span>Подтверждение после выполнения</span></li>
            <li><span class="check"></span><span>Поддержка в Telegram</span></li>
          </ul>
          <div style="margin-top:12px" class="row">
            <a class="btn primary" href="#order">Оформить</a>
          </div>
        </div>

        <div class="price" style="border-color: rgba(110,231,255,.28); background: linear-gradient(180deg, rgba(110,231,255,.10), rgba(255,255,255,.03));">
          <div class="tag">Популярно</div>
          <h3>Быстрый приоритет</h3>
          <div class="num">Комиссия 7%</div>
          <ul class="list">
            <li><span class="check"></span><span>Приоритет в очереди</span></li>
            <li><span class="check"></span><span>Уточнение по региону/платформе</span></li>
            <li><span class="check"></span><span>Статусы выполнения</span></li>
          </ul>
          <div style="margin-top:12px" class="row">
            <a class="btn primary" href="#order">Оформить</a>
          </div>
        </div>

        <div class="price">
          <div class="tag">Премиум</div>
          <h3>Регулярный донат</h3>
          <div class="num">Индивидуально</div>
          <ul class="list">
            <li><span class="check"></span><span>Скидка от объёма</span></li>
            <li><span class="check"></span><span>Персональный менеджер</span></li>
            <li><span class="check"></span><span>Гибкие способы оплаты</span></li>
          </ul>
          <div style="margin-top:12px" class="row">
            <a class="btn primary" href="https://t.me/mobilegemss" target="_blank" rel="noopener">Написать</a>
          </div>
        </div>
      </div>

      <p class="muted" style="margin:12px 0 0;font-size:12px">
        Совет: если принимаешь оплаты, добавь реквизиты/провайдера и короткое “Условия/Возвраты/Риски” под свою модель работы.
      </p>
    </section>

    <section id="order" class="section">
      <div class="title">
        <div>
          <h2>Оформить заявку</h2>
          <p>Заполни форму — мы подготовим ответ в Telegram.</p>
        </div>
      </div>

      <div class="card">
        <div class="formgrid">
          <div>
            <label>
              Игра
              <input id="f_game" placeholder="Напр. PUBG Mobile" />
            </label>
          </div>
          <div>
            <label>
              Платформа
              <select id="f_platform">
                <option>Android</option>
                <option>iOS</option>
                <option>PC</option>
                <option>Другое</option>
              </select>
            </label>
          </div>

          <div>
            <label>
              ID / Ник / Сервер
              <input id="f_id" placeholder="Напр. ID 123456789 / Сервер EU" />
            </label>
          </div>
          <div>
            <label>
              Сумма / Пакет
              <input id="f_pack" placeholder="Напр. 500 UC / 1090 алмазов" />
            </label>
          </div>

          <div style="grid-column:1/-1">
            <label>
              Комментарий (регион, способ входа, сроки)
              <textarea id="f_comment" placeholder="Напр. регион UA, нужно сегодня, без входа в аккаунт (если возможно)"></textarea>
            </label>
          </div>

          <div class="row" style="grid-column:1/-1">
            <button class="btn primary" id="sendTg" type="button">Отправить в Telegram</button>
            <button class="btn" id="copyOrder" type="button">Скопировать заявку</button>
            <span class="mini">Telegram: <span class="kbd">@mobilegemss</span></span>
          </div>

          <p class="muted" style="grid-column:1/-1;margin:6px 0 0;font-size:12px">
            Нажимая “Отправить”, откроется Telegram с готовым текстом (ты просто отправляешь его менеджеру).
          </p>
        </div>
      </div>
    </section>

    <section id="faq" class="section">
      <div class="title">
        <div>
          <h2>FAQ</h2>
          <p>Коротко о частых вопросах.</p>
        </div>
      </div>

      <div class="faq">
        <details>
          <summary>Сколько по времени занимает донат?</summary>
          <p>Обычно 5–30 минут после подтверждения оплаты. В редких случаях дольше из-за очередей/проверок платформы.</p>
        </details>
        <details>
          <summary>Нужны ли логин/пароль?</summary>
          <p>Зависит от игры и метода. По возможности используйте пополнение по ID. Если вход нужен — заранее согласуйте безопасный сценарий.</p>
        </details>
        <details>
          <summary>Какие способы оплаты доступны?</summary>
          <p>Добавь сюда свои методы: карта, перевод, крипто, платёжный провайдер. Лучше указать комиссии и валюту.</p>
        </details>
        <details>
          <summary>Есть ли гарантии?</summary>
          <p>Фиксируем детали заказа в чате. После выполнения присылаем подтверждение (скрин/чек/статус в игре, если применимо).</p>
        </details>
      </div>
    </section>
  </main>

  <footer>
    <div class="wrap footgrid">
      <div>
        <div style="display:flex;align-items:center;gap:10px">
          <div class="mark" aria-hidden="true" style="width:28px;height:28px;border-radius:10px"></div>
          <div>
            <div><b>MobileGems</b></div>
            <div class="muted" style="font-size:12px">Донат-сервис • Поддержка в Telegram</div>
          </div>
        </div>
        <div class="muted" style="margin-top:10px;font-size:12px;max-width:70ch">
          © <span id="y"></span> MobileGems. Все торговые марки принадлежат их владельцам.
          Этот сайт — информационная страница сервиса.
        </div>
      </div>
      <div class="badges">
        <a class="badge" href="https://t.me/mobilegemss" target="_blank" rel="noopener">
          :contentReference[oaicite:0]{index=0}: @mobilegemss
        </a>
        <span class="badge">🧾 Подтверждение заказа</span>
        <span class="badge">🔒 Конфиденциально</span>
      </div>
    </div>
  </footer>

  <script>
    // ====== Calculator ======
    const feeEl = document.getElementById('fee');
    const totalEl = document.getElementById('total');
    const amountEl = document.getElementById('amount');
    const gameEl = document.getElementById('game');
    const copyTextBtn = document.getElementById('copyText');

    // Простая логика комиссии (пример): базово 5%, но для "Другая" 7%
    function currentFee(){
      return (gameEl.value === 'Другая') ? 0.07 : 0.05;
    }
    function formatMoney(n){
      if (!isFinite(n)) return '—';
      return (Math.round(n * 100) / 100).toString();
    }
    function updateCalc(){
      const fee = currentFee();
      feeEl.textContent = Math.round(fee * 100) + '%';
      const a = Number(amountEl.value);
      if (!a || a <= 0){ totalEl.textContent = '—'; return; }
      const total = a * (1 + fee);
      totalEl.textContent = formatMoney(total);
    }
    amountEl.addEventListener('input', updateCalc);
    gameEl.addEventListener('change', updateCalc);
    updateCalc();

    function buildCalcText(){
      const fee = Math.round(currentFee() * 100);
      const a = Number(amountEl.value || 0);
      const t = a ? formatMoney(a * (1 + currentFee())) : '—';
      return `Заявка на донат:\nИгра: ${gameEl.value}\nСумма пополнения: ${a || '—'}\nКомиссия сервиса: ${fee}%\nОценка к оплате: ${t}\n\nНужно уточнить: регион/платформа/ID.`;
    }

    copyTextBtn.addEventListener('click', async () => {
      try{
        await navigator.clipboard.writeText(buildCalcText());
        copyTextBtn.textContent = 'Скопировано ✓';
        setTimeout(()=>copyTextBtn.textContent='Скопировать текст заявки', 1200);
      }catch(e){
        alert('Не удалось скопировать. Скопируй вручную:\n\n' + buildCalcText());
      }
    });

    // ====== Order form -> Telegram deep link ======
    const fGame = document.getElementById('f_game');
    const fPlatform = document.getElementById('f_platform');
    const fId = document.getElementById('f_id');
    const fPack = document.getElementById('f_pack');
    const fComment = document.getElementById('f_comment');
    const sendTg = document.getElementById('sendTg');
    const copyOrder = document.getElementById('copyOrder');

    // Подставим выбранную игру из калькулятора в форму
    fGame.value = gameEl.value;
    gameEl.addEventListener('change', ()=> fGame.value = gameEl.value);

    function buildOrderText(){
      const lines = [
        'Привет! Хочу оформить донат:',
        `Игра: ${fGame.value || '—'}`,
        `Платформа: ${fPlatform.value || '—'}`,
        `ID/Ник/Сервер: ${fId.value || '—'}`,
        `Сумма/Пакет: ${fPack.value || '—'}`,
        `Комментарий: ${fComment.value || '—'}`
      ];
      return lines.join('\n');
    }

    function tgLink(text){
      // Вставь сюда, если используешь бота: https://t.me/<botname>?start=...
      const username = 'mobilegemss';
      const url = `https://t.me/${username}?text=${encodeURIComponent(text)}`;
      return url;
    }

    sendTg.addEventListener('click', () => {
      const url = tgLink(buildOrderText());
      window.open(url, '_blank', 'noopener');
    });

    copyOrder.addEventListener('click', async () => {
      const text = buildOrderText();
      try{
        await navigator.clipboard.writeText(text);
        copyOrder.textContent = 'Скопировано ✓';
        setTimeout(()=>copyOrder.textContent='Скопировать заявку', 1200);
      }catch(e){
        alert('Не удалось скопировать. Скопируй вручную:\n\n' + text);
      }
    });

    document.getElementById('y').textContent = new Date().getFullYear();
  </script>
</body>
</html>

