<!doctype html>
<html lang="ja">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>審査・ローン相談フォーム｜住まらぼ大阪福島店</title>
  <style>
    :root {
      --orange: #f58220;
      --orange-dark: #df6d10;
      --orange-soft: #fff4e8;
      --ink: #2f2a25;
      --muted: #746b62;
      --line: #eadfd3;
      --bg: #fffaf5;
      --white: #ffffff;
      --green: #06c755;
      --shadow: 0 12px 28px rgba(120, 72, 22, 0.12);
      --radius: 8px;
    }

    * {
      box-sizing: border-box;
    }

    html {
      background: var(--bg);
    }

    body {
      margin: 0;
      color: var(--ink);
      font-family: -apple-system, BlinkMacSystemFont, "Hiragino Sans", "Yu Gothic", "Noto Sans JP", sans-serif;
      line-height: 1.7;
      letter-spacing: 0;
      background:
        linear-gradient(180deg, #fff7ef 0%, #ffffff 220px),
        var(--white);
    }

    button,
    input,
    select,
    textarea {
      font: inherit;
    }

    .page {
      width: min(100%, 520px);
      min-height: 100vh;
      margin: 0 auto;
      padding: 22px 16px 32px;
      background: var(--white);
    }

    .hero {
      padding: 10px 0 20px;
    }

    .shop {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 6px 10px;
      color: var(--orange-dark);
      font-size: 12px;
      font-weight: 700;
      background: var(--orange-soft);
      border: 1px solid #ffe0bd;
      border-radius: 999px;
    }

    .shop-mark {
      display: grid;
      place-items: center;
      width: 20px;
      height: 20px;
      color: var(--white);
      font-size: 12px;
      font-weight: 800;
      background: var(--orange);
      border-radius: 6px;
    }

    h1 {
      margin: 14px 0 8px;
      font-size: clamp(25px, 7vw, 34px);
      line-height: 1.25;
      letter-spacing: 0;
    }

    .lead {
      margin: 0;
      color: var(--muted);
      font-size: 14px;
    }

    .notice {
      margin-top: 16px;
      padding: 12px;
      color: #5f4630;
      font-size: 13px;
      background: #fff8ef;
      border: 1px solid #ffe1bd;
      border-radius: var(--radius);
    }

    .steps {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 8px;
      margin: 10px 0 18px;
    }

    .step {
      min-height: 36px;
      display: grid;
      place-items: center;
      padding: 6px;
      color: #9a8a7c;
      font-size: 12px;
      font-weight: 700;
      border: 1px solid var(--line);
      border-radius: var(--radius);
      background: #fff;
    }

    .step.is-active {
      color: var(--white);
      border-color: var(--orange);
      background: var(--orange);
    }

    .panel {
      padding: 18px 14px;
      border: 1px solid var(--line);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      background: var(--white);
    }

    .section-title {
      display: flex;
      align-items: center;
      gap: 9px;
      margin: 0 0 14px;
      font-size: 18px;
      line-height: 1.35;
    }

    .section-title::before {
      content: "";
      flex: 0 0 auto;
      width: 8px;
      height: 24px;
      background: var(--orange);
      border-radius: 99px;
    }

    .choice-grid {
      display: grid;
      gap: 10px;
    }

    .choice {
      position: relative;
    }

    .choice input {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      opacity: 0;
      cursor: pointer;
    }

    .choice span {
      display: block;
      padding: 14px 14px 14px 44px;
      color: var(--ink);
      font-weight: 700;
      border: 1px solid var(--line);
      border-radius: var(--radius);
      background: #fff;
      transition: border-color 0.2s ease, background 0.2s ease, box-shadow 0.2s ease;
    }

    .choice span::before {
      content: "";
      position: absolute;
      left: 14px;
      top: 50%;
      width: 18px;
      height: 18px;
      border: 2px solid #d7c8b8;
      border-radius: 50%;
      transform: translateY(-50%);
      background: #fff;
    }

    .choice input:checked + span {
      border-color: var(--orange);
      background: var(--orange-soft);
      box-shadow: 0 0 0 3px rgba(245, 130, 32, 0.12);
    }

    .choice input:checked + span::before {
      border-color: var(--orange);
      box-shadow: inset 0 0 0 4px #fff;
      background: var(--orange);
    }

    form {
      display: grid;
      gap: 18px;
      margin-top: 16px;
    }

    fieldset {
      display: grid;
      gap: 12px;
      margin: 0;
      padding: 0;
      border: 0;
    }

    legend {
      width: 100%;
      margin-bottom: 2px;
      padding: 10px 0 4px;
      color: var(--orange-dark);
      font-weight: 800;
    }

    .field {
      display: grid;
      gap: 6px;
    }

    label {
      color: #443c35;
      font-size: 14px;
      font-weight: 700;
    }

    .required {
      margin-left: 6px;
      color: var(--orange-dark);
      font-size: 11px;
      font-weight: 800;
    }

    input,
    select,
    textarea {
      width: 100%;
      min-height: 46px;
      padding: 11px 12px;
      color: var(--ink);
      border: 1px solid #d9cfc4;
      border-radius: var(--radius);
      background: #fff;
      outline: none;
    }

    textarea {
      min-height: 116px;
      resize: vertical;
    }

    input:focus,
    select:focus,
    textarea:focus {
      border-color: var(--orange);
      box-shadow: 0 0 0 3px rgba(245, 130, 32, 0.14);
    }

    .hint {
      color: var(--muted);
      font-size: 12px;
    }

    .actions {
      display: grid;
      gap: 10px;
      margin-top: 2px;
    }

    .button {
      min-height: 50px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      width: 100%;
      padding: 12px 16px;
      border: 0;
      border-radius: var(--radius);
      color: var(--white);
      font-weight: 800;
      background: var(--orange);
      cursor: pointer;
      box-shadow: 0 8px 18px rgba(245, 130, 32, 0.24);
    }

    .button:active {
      transform: translateY(1px);
    }

    .button.secondary {
      color: var(--orange-dark);
      border: 1px solid #ffd6a6;
      background: var(--orange-soft);
      box-shadow: none;
    }

    .button.line {
      background: var(--green);
      box-shadow: 0 8px 18px rgba(6, 199, 85, 0.18);
    }

    .screen {
      display: none;
    }

    .screen.is-active {
      display: block;
    }

    .hidden {
      display: none !important;
    }

    .summary {
      display: grid;
      gap: 10px;
      margin: 0;
    }

    .summary-row {
      padding: 10px 0;
      border-bottom: 1px solid #f0e7dd;
    }

    .summary-row dt {
      margin: 0 0 3px;
      color: var(--muted);
      font-size: 12px;
      font-weight: 700;
    }

    .summary-row dd {
      margin: 0;
      color: var(--ink);
      font-size: 15px;
      white-space: pre-wrap;
      overflow-wrap: anywhere;
    }

    .submit-status {
      min-height: 22px;
      margin: 8px 0 0;
      color: var(--orange-dark);
      font-size: 13px;
      font-weight: 700;
      text-align: center;
    }

    .complete-guide {
      margin-top: 14px;
      padding: 14px;
      color: #234431;
      font-size: 14px;
      font-weight: 800;
      text-align: center;
      border: 1px solid #bceacb;
      border-radius: var(--radius);
      background: #effcf3;
    }

    .complete-guide strong {
      display: block;
      margin-bottom: 4px;
      font-size: 16px;
    }

    .footer-note {
      margin: 18px 0 0;
      color: var(--muted);
      font-size: 12px;
      text-align: center;
    }

    @media (max-width: 360px) {
      .page {
        padding-inline: 12px;
      }

      .panel {
        padding-inline: 12px;
      }

      h1 {
        font-size: 24px;
      }

      .choice span {
        padding-right: 10px;
      }
    }
  </style>
</head>
<body>
  <main class="page">
    <header class="hero">
      <div class="shop"><span class="shop-mark">住</span>住まらぼ大阪福島店｜暮らし研究所</div>
      <h1>審査・ローン相談フォーム</h1>
      <p class="lead">LINEから開いて、そのまま相談内容を送信できます。送信後、担当者より順番にご連絡します。</p>
      <p class="notice">このフォームは相談受付用です。審査結果や融資可否を断定するものではありません。</p>
    </header>

    <nav class="steps" aria-label="入力ステップ">
      <div class="step is-active" data-step="input">入力</div>
      <div class="step" data-step="confirm">確認</div>
      <div class="step" data-step="complete">送信</div>
    </nav>

    <section class="screen is-active" id="inputScreen">
      <div class="panel">
        <h2 class="section-title">ご相談内容を選択してください</h2>
        <div class="choice-grid" role="radiogroup" aria-label="ご相談内容">
          <label class="choice">
            <input type="radio" name="consultationType" value="rent" checked>
            <span>賃貸の入居審査について</span>
          </label>
          <label class="choice">
            <input type="radio" name="consultationType" value="loan">
            <span>住宅ローンについて</span>
          </label>
          <label class="choice">
            <input type="radio" name="consultationType" value="both">
            <span>どちらも相談したい</span>
          </label>
        </div>

        <form id="consultationForm">
          <fieldset>
            <legend>基本情報</legend>
            <div class="field">
              <label for="name">お名前<span class="required">必須</span></label>
              <input id="name" name="name" type="text" autocomplete="name" required placeholder="例：山田 太郎">
            </div>
            <div class="field">
              <label for="age">年齢<span class="required">必須</span></label>
              <input id="age" name="age" type="number" inputmode="numeric" min="18" max="100" required placeholder="例：32">
            </div>
            <div class="field">
              <label for="phone">電話番号<span class="required">必須</span></label>
              <input id="phone" name="phone" type="tel" autocomplete="tel" required placeholder="例：09012345678">
            </div>
            <div class="field">
              <label for="job">ご職業<span class="required">必須</span></label>
              <input id="job" name="job" type="text" required placeholder="例：会社員、自営業、アルバイトなど">
            </div>
            <div class="field">
              <label for="employment">雇用形態<span class="required">必須</span></label>
              <select id="employment" name="employment" required>
                <option value="">選択してください</option>
                <option>正社員</option>
                <option>契約社員</option>
                <option>派遣社員</option>
                <option>アルバイト・パート</option>
                <option>自営業・個人事業主</option>
                <option>会社役員</option>
                <option>学生</option>
                <option>その他</option>
              </select>
            </div>
          </fieldset>

          <fieldset data-section="rent">
            <legend>賃貸の入居審査について</legend>
            <div class="field">
              <label for="rentIncome">月収または年収<span class="required">必須</span></label>
              <input id="rentIncome" name="rentIncome" type="text" data-required-when="rent" placeholder="例：月収25万円、年収350万円">
            </div>
            <div class="field">
              <label for="rentDebt">現在のお借入の有無<span class="required">必須</span></label>
              <select id="rentDebt" name="rentDebt" data-required-when="rent">
                <option value="">選択してください</option>
                <option>なし</option>
                <option>あり</option>
                <option>わからない・確認したい</option>
              </select>
            </div>
            <div class="field">
              <label for="screeningHistory">過去の審査落ちの有無<span class="required">必須</span></label>
              <select id="screeningHistory" name="screeningHistory" data-required-when="rent">
                <option value="">選択してください</option>
                <option>なし</option>
                <option>あり</option>
                <option>相談しながら確認したい</option>
              </select>
            </div>
            <div class="field">
              <label for="guarantor">保証人の有無<span class="required">必須</span></label>
              <select id="guarantor" name="guarantor" data-required-when="rent">
                <option value="">選択してください</option>
                <option>あり</option>
                <option>なし</option>
                <option>未定</option>
              </select>
            </div>
            <div class="field">
              <label for="rentMessage">相談内容</label>
              <textarea id="rentMessage" name="rentMessage" placeholder="気になること、不安なこと、過去の状況などをご記入ください"></textarea>
            </div>
          </fieldset>

          <fieldset data-section="loan">
            <legend>住宅ローンについて</legend>
            <div class="field">
              <label for="annualIncome">年収<span class="required">必須</span></label>
              <input id="annualIncome" name="annualIncome" type="text" data-required-when="loan" placeholder="例：年収500万円">
            </div>
            <div class="field">
              <label for="workYears">勤続年数<span class="required">必須</span></label>
              <input id="workYears" name="workYears" type="text" data-required-when="loan" placeholder="例：3年6ヶ月">
            </div>
            <div class="field">
              <label for="ownFunds">自己資金<span class="required">必須</span></label>
              <input id="ownFunds" name="ownFunds" type="text" data-required-when="loan" placeholder="例：100万円、なし、未定">
            </div>
            <div class="field">
              <label for="loanDebt">現在のお借入の有無<span class="required">必須</span></label>
              <select id="loanDebt" name="loanDebt" data-required-when="loan">
                <option value="">選択してください</option>
                <option>なし</option>
                <option>あり</option>
                <option>わからない・確認したい</option>
              </select>
            </div>
            <div class="field">
              <label for="area">購入希望エリア<span class="required">必須</span></label>
              <input id="area" name="area" type="text" data-required-when="loan" placeholder="例：大阪市福島区、北区周辺など">
            </div>
            <div class="field">
              <label for="loanMessage">相談内容</label>
              <textarea id="loanMessage" name="loanMessage" placeholder="借入希望額、物件の有無、不安な点などをご記入ください"></textarea>
            </div>
          </fieldset>

          <p class="hint">入力内容は相談受付のために使用します。送信前に確認画面が表示されます。</p>
          <div class="actions">
            <button class="button" type="submit">入力内容を確認する</button>
          </div>
        </form>
      </div>
    </section>

    <section class="screen" id="confirmScreen">
      <div class="panel">
        <h2 class="section-title">入力内容の確認</h2>
        <dl class="summary" id="summaryList"></dl>
        <div class="actions">
          <button class="button" type="button" id="submitButton">この内容で送信する</button>
          <button class="button secondary" type="button" id="backButton">入力内容を修正する</button>
        </div>
        <p class="submit-status" id="submitStatus" aria-live="polite"></p>
      </div>
    </section>

    <section class="screen" id="completeScreen">
      <div class="panel">
        <h2 class="section-title">送信を受け付けました</h2>
        <p class="lead">ご入力ありがとうございます。内容を確認のうえ、担当者よりご連絡します。</p>
        <div class="actions">
          <button class="button secondary" type="button" id="newEntryButton">別の相談を入力する</button>
        </div>
        <div class="complete-guide">
          <strong>送信済みです</strong>
          LINEでのテキスト貼り付けは不要です。
        </div>
      </div>
    </section>

    <p class="footer-note">住まらぼ大阪福島店｜暮らし研究所</p>
    <iframe class="hidden" name="submitFrame" title="送信用フレーム"></iframe>
  </main>

  <script>
    const WEB_APP_URL = "https://script.google.com/macros/s/AKfycbxlGopSuSTWgteQVecfHRYpnG5Y6xvf8Q9sPOZQ9fXaKpnyGsN2hmfWRyMq6vROUJIj/exec";
    const form = document.getElementById("consultationForm");
    const typeInputs = document.querySelectorAll('input[name="consultationType"]');
    const sections = document.querySelectorAll("[data-section]");
    const screens = {
      input: document.getElementById("inputScreen"),
      confirm: document.getElementById("confirmScreen"),
      complete: document.getElementById("completeScreen")
    };
    const steps = document.querySelectorAll("[data-step]");
    const summaryList = document.getElementById("summaryList");
    const submitButton = document.getElementById("submitButton");
    const submitStatus = document.getElementById("submitStatus");

    const fieldGroups = {
      base: [
        ["ご相談内容", "consultationLabel"],
        ["お名前", "name"],
        ["年齢", "age"],
        ["電話番号", "phone"],
        ["ご職業", "job"],
        ["雇用形態", "employment"]
      ],
      rent: [
        ["月収または年収", "rentIncome"],
        ["現在のお借入の有無", "rentDebt"],
        ["過去の審査落ちの有無", "screeningHistory"],
        ["保証人の有無", "guarantor"],
        ["相談内容", "rentMessage"]
      ],
      loan: [
        ["年収", "annualIncome"],
        ["勤続年数", "workYears"],
        ["自己資金", "ownFunds"],
        ["現在のお借入の有無", "loanDebt"],
        ["購入希望エリア", "area"],
        ["相談内容", "loanMessage"]
      ]
    };

    const typeLabels = {
      rent: "賃貸の入居審査について",
      loan: "住宅ローンについて",
      both: "どちらも相談したい"
    };

    function getSelectedType() {
      return document.querySelector('input[name="consultationType"]:checked').value;
    }

    function usesSection(type, section) {
      return type === section || type === "both";
    }

    function updateVisibleFields() {
      const type = getSelectedType();

      sections.forEach((section) => {
        const sectionName = section.dataset.section;
        const isActive = usesSection(type, sectionName);
        section.classList.toggle("hidden", !isActive);
      });

      document.querySelectorAll("[data-required-when]").forEach((field) => {
        field.required = usesSection(type, field.dataset.requiredWhen);
      });
    }

    function showScreen(name) {
      Object.entries(screens).forEach(([key, screen]) => {
        screen.classList.toggle("is-active", key === name);
      });
      steps.forEach((step) => {
        step.classList.toggle("is-active", step.dataset.step === name);
      });
      submitStatus.textContent = "";
      window.scrollTo({ top: 0, behavior: "smooth" });
    }

    function valueOf(name) {
      if (name === "consultationLabel") {
        return typeLabels[getSelectedType()];
      }

      const field = form.elements[name];
      return field && field.value.trim() ? field.value.trim() : "未入力";
    }

    function activeFields() {
      const type = getSelectedType();
      const fields = [...fieldGroups.base];

      if (usesSection(type, "rent")) {
        fields.push(["【賃貸の入居審査について】", "headingRent"], ...fieldGroups.rent);
      }

      if (usesSection(type, "loan")) {
        fields.push(["【住宅ローンについて】", "headingLoan"], ...fieldGroups.loan);
      }

      return fields;
    }

    function buildSummary() {
      summaryList.innerHTML = "";

      activeFields().forEach(([label, name]) => {
        if (name.startsWith("heading")) {
          const row = document.createElement("div");
          row.className = "summary-row";
          row.innerHTML = '<dt>' + label + '</dt><dd></dd>';
          summaryList.appendChild(row);
          return;
        }

        const row = document.createElement("div");
        row.className = "summary-row";

        const term = document.createElement("dt");
        term.textContent = label;

        const desc = document.createElement("dd");
        desc.textContent = valueOf(name);

        row.append(term, desc);
        summaryList.appendChild(row);
      });
    }

    function buildSubmissionData() {
      const data = {
        submittedAt: new Date().toISOString(),
        consultationType: typeLabels[getSelectedType()]
      };

      activeFields().forEach(([label, name]) => {
        if (!name.startsWith("heading") && name !== "consultationLabel") {
          data[name] = valueOf(name);
        }
      });

      return data;
    }

    function postToSpreadsheet(data) {
      const transportForm = document.createElement("form");
      transportForm.method = "post";
      transportForm.action = WEB_APP_URL;
      transportForm.target = "submitFrame";
      transportForm.acceptCharset = "UTF-8";
      transportForm.className = "hidden";

      const payload = document.createElement("input");
      payload.type = "hidden";
      payload.name = "payload";
      payload.value = JSON.stringify(data);

      transportForm.appendChild(payload);
      document.body.appendChild(transportForm);
      transportForm.submit();
      setTimeout(() => transportForm.remove(), 2000);
    }

    typeInputs.forEach((input) => {
      input.addEventListener("change", updateVisibleFields);
    });

    form.addEventListener("submit", (event) => {
      event.preventDefault();

      if (!form.checkValidity()) {
        form.reportValidity();
        return;
      }

      buildSummary();
      showScreen("confirm");
    });

    document.getElementById("backButton").addEventListener("click", () => {
      showScreen("input");
    });

    submitButton.addEventListener("click", () => {
      if (!WEB_APP_URL) {
        submitStatus.textContent = "送信先URLが未設定です。Google Apps ScriptのWebアプリURLを設定してください。";
        return;
      }

      submitButton.disabled = true;
      submitButton.textContent = "送信中...";
      submitStatus.textContent = "送信しています。画面を閉じずにお待ちください。";
      postToSpreadsheet(buildSubmissionData());

      setTimeout(() => {
        submitButton.disabled = false;
        submitButton.textContent = "この内容で送信する";
        form.reset();
        updateVisibleFields();
        showScreen("complete");
      }, 1200);
    });

    document.getElementById("newEntryButton").addEventListener("click", () => {
      showScreen("input");
    });

    updateVisibleFields();
  </script>
</body>
</html>
