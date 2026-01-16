```html
<!doctype html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />index.html.txtindex.html
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>AIx 企業変革 Lite FocusCamp | Aoba-BBT</title>

    <!-- Google Fonts: Noto Sans JP -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700;800&display=swap"
      rel="stylesheet"
    />

    <!-- Tailwind CSS (CDN) -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
      tailwind.config = {
        theme: {
          extend: {
            fontFamily: {
              sans: ['"Noto Sans JP"', "ui-sans-serif", "system-ui"],
            },
            colors: {
              brand: {
                cyan: "#00C2FF", // main
                orange: "#FFA500", // accent
                ink: "#0B1220",
                slate: "#5B6476",
              },
            },
            boxShadow: {
              soft: "0 10px 30px rgba(2, 132, 199, 0.12)",
              glow: "0 0 0 6px rgba(0, 194, 255, 0.15)",
            },
            backgroundImage: {
              "grid-faint":
                "radial-gradient(circle at 1px 1px, rgba(0,194,255,0.18) 1px, rgba(255,255,255,0) 0)",
            },
          },
        },
      };
    </script>

    <!-- FontAwesome -->
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
      referrerpolicy="no-referrer"
    />

    <style>
      html {
        scroll-behavior: smooth;
      }
      /* nicer focus ring */
      :focus-visible {
        outline: none;
        box-shadow: 0 0 0 6px rgba(0, 194, 255, 0.18);
        border-radius: 12px;
      }
    </style>
  </head>

  <body class="font-sans bg-white text-brand-ink antialiased">
    <!-- Top announcement / subtle bar (optional but nice for "speed") -->
    <div class="bg-brand-ink text-white">
      <div class="mx-auto max-w-6xl px-4 py-2 text-xs sm:text-sm flex items-center justify-between gap-3">
        <div class="flex items-center gap-2">
          <i class="fa-solid fa-bolt text-brand-cyan"></i>
          <span class="opacity-95">4週間で「現場の自走力」を実装する FocusCamp</span>
        </div>
        <a href="#apply" class="hidden sm:inline-flex items-center gap-2 text-white/90 hover:text-white transition">
          <span>今すぐ申し込む</span><i class="fa-solid fa-arrow-right text-xs"></i>
        </a>
      </div>
    </div>

    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white/80 backdrop-blur border-b border-slate-200/70">
      <div class="mx-auto max-w-6xl px-4">
        <div class="flex h-16 items-center justify-between gap-3">
          <!-- Logo (text) -->
          <a href="#" class="flex items-center gap-3">
            <div class="h-10 w-10 rounded-2xl bg-brand-cyan/10 border border-brand-cyan/20 flex items-center justify-center">
              <i class="fa-solid fa-layer-group text-brand-cyan"></i>
            </div>
            <div class="leading-tight">
              <p class="text-sm font-semibold text-brand-ink">Aoba-BBT AIx FocusCamp</p>
              <p class="text-xs text-brand-slate">DX人材育成プログラム</p>
            </div>
          </a>

          <!-- Nav (desktop) -->
          <nav class="hidden md:flex items-center gap-6 text-sm text-brand-slate">
            <a href="#problem" class="hover:text-brand-ink transition">課題</a>
            <a href="#solution" class="hover:text-brand-ink transition">解決策</a>
            <a href="#curriculum" class="hover:text-brand-ink transition">カリキュラム</a>
            <a href="#instructor" class="hover:text-brand-ink transition">講師</a>
            <a href="#overview" class="hover:text-brand-ink transition">概要</a>
          </nav>

          <!-- CTA -->
          <div class="flex items-center gap-2">
            <a
              href="#apply"
              class="inline-flex items-center gap-2 rounded-2xl bg-brand-orange px-4 py-2 text-sm font-bold text-white shadow-soft hover:brightness-105 active:brightness-95 transition"
            >
              <i class="fa-solid fa-pen-to-square"></i>
              今すぐ申し込む
            </a>

            <!-- Mobile menu button (simple anchor list below) -->
            <a
              href="#mobile-nav"
              class="md:hidden inline-flex h-10 w-10 items-center justify-center rounded-2xl border border-slate-200 text-brand-ink hover:bg-slate-50 transition"
              aria-label="メニューを開く"
            >
              <i class="fa-solid fa-bars"></i>
            </a>
          </div>
        </div>

        <!-- Mobile nav (simple, no JS; shown when jumped) -->
        <div id="mobile-nav" class="md:hidden pb-4">
          <div class="grid grid-cols-2 gap-2 text-sm">
            <a href="#problem" class="rounded-xl border border-slate-200 px-3 py-2 hover:bg-slate-50 transition">課題</a>
            <a href="#solution" class="rounded-xl border border-slate-200 px-3 py-2 hover:bg-slate-50 transition">解決策</a>
            <a href="#curriculum" class="rounded-xl border border-slate-200 px-3 py-2 hover:bg-slate-50 transition">カリキュラム</a>
            <a href="#instructor" class="rounded-xl border border-slate-200 px-3 py-2 hover:bg-slate-50 transition">講師</a>
            <a href="#overview" class="rounded-xl border border-slate-200 px-3 py-2 hover:bg-slate-50 transition">概要</a>
            <a href="#apply" class="rounded-xl bg-brand-orange px-3 py-2 font-bold text-white hover:brightness-105 transition">申込</a>
          </div>
        </div>
      </div>
    </header>

    <!-- Hero -->
    <section class="relative overflow-hidden">
      <!-- Background decoration -->
      <div class="absolute inset-0 bg-grid-faint [background-size:18px_18px] opacity-60"></div>
      <div class="absolute -top-24 -right-24 h-72 w-72 rounded-full bg-brand-cyan/20 blur-3xl"></div>
      <div class="absolute -bottom-24 -left-24 h-72 w-72 rounded-full bg-brand-orange/15 blur-3xl"></div>

      <div class="relative mx-auto max-w-6xl px-4 py-14 sm:py-20">
        <div class="grid gap-10 lg:grid-cols-2 lg:items-center">
          <!-- Copy -->
          <div>
            <div class="inline-flex items-center gap-2 rounded-full border border-brand-cyan/25 bg-white/70 px-4 py-2 text-xs font-semibold text-brand-ink">
              <i class="fa-solid fa-wand-magic-sparkles text-brand-cyan"></i>
              <span>AIx 企業変革 Lite FocusCamp</span>
              <span class="text-brand-slate font-medium">｜全4回（2月開始予定）</span>
            </div>

            <h1 class="mt-5 text-3xl sm:text-4xl lg:text-5xl font-extrabold leading-tight tracking-tight">
              「学習性無力感」を破壊し、<br class="hidden sm:block" />
              現場の自走力を実装する4週間
            </h1>

            <p class="mt-4 text-base sm:text-lg text-brand-slate leading-relaxed">
              Replit × AI Agentを活用し、インフラ構築不要で現場だけで完結する開発環境を提供。<br />
              “作れる現場”を、最短で立ち上げます。
            </p>

            <div class="mt-7 flex flex-col sm:flex-row gap-3">
              <a
                href="#apply"
                class="inline-flex items-center justify-center gap-2 rounded-2xl bg-brand-orange px-6 py-3 text-base font-extrabold text-white shadow-soft hover:brightness-105 active:brightness-95 transition"
              >
                <i class="fa-solid fa-rocket"></i>
                今すぐ申し込む
              </a>
              <a
                href="#overview"
                class="inline-flex items-center justify-center gap-2 rounded-2xl border border-slate-200 bg-white px-6 py-3 text-base font-bold text-brand-ink hover:bg-slate-50 transition"
              >
                <i class="fa-regular fa-circle-play text-brand-cyan"></i>
                概要を見る
              </a>
            </div>

            <!-- Trust badges -->
            <div class="mt-8 grid grid-cols-1 sm:grid-cols-3 gap-3">
              <div class="rounded-2xl border border-slate-200 bg-white/70 p-4">
                <div class="flex items-center gap-3">
                  <div class="h-10 w-10 rounded-2xl bg-brand-cyan/10 flex items-center justify-center">
                    <i class="fa-solid fa-stopwatch text-brand-cyan"></i>
                  </div>
                  <div>
                    <p class="text-sm font-bold">環境構築0秒</p>
                    <p class="text-xs text-brand-slate">Replitで即スタート</p>
                  </div>
                </div>
              </div>
              <div class="rounded-2xl border border-slate-200 bg-white/70 p-4">
                <div class="flex items-center gap-3">
                  <div class="h-10 w-10 rounded-2xl bg-brand-orange/15 flex items-center justify-center">
                    <i class="fa-solid fa-code text-brand-orange"></i>
                  </div>
                  <div>
                    <p class="text-sm font-bold">コーディング不要</p>
                    <p class="text-xs text-brand-slate">自然言語でVibe Coding</p>
                  </div>
                </div>
              </div>
              <div class="rounded-2xl border border-slate-200 bg-white/70 p-4">
                <div class="flex items-center gap-3">
                  <div class="h-10 w-10 rounded-2xl bg-brand-cyan/10 flex items-center justify-center">
                    <i class="fa-solid fa-shield-halved text-brand-cyan"></i>
                  </div>
                  <div>
                    <p class="text-sm font-bold">信頼できる設計</p>
                    <p class="text-xs text-brand-slate">現場運用まで落とす</p>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Visual -->
          <div class="relative">
            <div class="rounded-3xl border border-slate-200 bg-white shadow-soft overflow-hidden">
              <div class="p-5 sm:p-6 border-b border-slate-200">
                <p class="text-sm font-bold flex items-center gap-2">
                  <i class="fa-solid fa-diagram-project text-brand-cyan"></i>
                  FocusCampのイメージ
                </p>
                <p class="text-xs text-brand-slate mt-1">スピード感 / テック感 / 変革 / 信頼</p>
              </div>

              <div class="p-6 sm:p-8">
                <div class="aspect-[4/3] rounded-2xl border border-dashed border-slate-300 bg-slate-50 flex items-center justify-center text-brand-slate">
                  画像プレースホルダー
                </div>

                <div class="mt-6 grid grid-cols-2 gap-3">
                  <div class="rounded-2xl bg-brand-ink text-white p-4">
                    <p class="text-xs text-white/70">アウトプット</p>
                    <p class="mt-1 font-extrabold">MVP × 1本</p>
                    <p class="mt-1 text-xs text-white/70">最終週で発表</p>
                  </div>
                  <div class="rounded-2xl bg-white border border-slate-200 p-4">
                    <p class="text-xs text-brand-slate">プロセス</p>
                    <p class="mt-1 font-extrabold text-brand-ink">Sprint開発</p>
                    <p class="mt-1 text-xs text-brand-slate">週ごとに積み上げ</p>
                  </div>
                </div>
              </div>
            </div>

            <div class="absolute -z-10 -bottom-8 -right-8 h-40 w-40 rounded-full bg-brand-cyan/15 blur-2xl"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- Problem -->
    <section id="problem" class="mx-auto max-w-6xl px-4 py-14 sm:py-18">
      <div class="grid gap-10 lg:grid-cols-2 lg:items-start">
        <div>
          <p class="text-xs font-extrabold tracking-widest text-brand-cyan">PROBLEM</p>
          <h2 class="mt-2 text-2xl sm:text-3xl font-extrabold">なぜDXは停滞するのか？</h2>
          <p class="mt-4 text-brand-slate leading-relaxed">
            現場のDXが止まる理由は、ツール不足でも、やる気不足でもありません。<br />
            「どうせ無理だ」という諦め——つまり <span class="font-bold text-brand-ink">学習性無力感</span> が組織に染み込んでいるからです。
          </p>

          <div class="mt-6 space-y-3">
            <div class="flex gap-3 rounded-2xl border border-slate-200 bg-white p-4">
              <div class="mt-0.5 h-10 w-10 shrink-0 rounded-2xl bg-brand-cyan/10 flex items-center justify-center">
                <i class="fa-solid fa-briefcase text-brand-cyan"></i>
              </div>
              <div>
                <p class="font-bold">忙しいから無理</p>
                <p class="text-sm text-brand-slate">現場改善が「いつかやる」になり、永遠に来ない。</p>
              </div>
            </div>

            <div class="flex gap-3 rounded-2xl border border-slate-200 bg-white p-4">
              <div class="mt-0.5 h-10 w-10 shrink-0 rounded-2xl bg-brand-orange/15 flex items-center justify-center">
                <i class="fa-solid fa-hourglass-half text-brand-orange"></i>
              </div>
              <div>
                <p class="font-bold">頼んでも半年待ち</p>
                <p class="text-sm text-brand-slate">情報システムや開発部門がボトルネック化する。</p>
              </div>
            </div>

            <div class="flex gap-3 rounded-2xl border border-slate-200 bg-white p-4">
              <div class="mt-0.5 h-10 w-10 shrink-0 rounded-2xl bg-brand-cyan/10 flex items-center justify-center">
                <i class="fa-solid fa-handshake text-brand-cyan"></i>
              </div>
              <div>
                <p class="font-bold">外部ベンダーへの丸投げ</p>
                <p class="text-sm text-brand-slate">内製の筋力が育たず、変化の速度で負け続ける。</p>
              </div>
            </div>
          </div>
        </div>

        <div class="rounded-3xl border border-slate-200 bg-white shadow-soft overflow-hidden">
          <div class="p-6 sm:p-8">
            <p class="text-sm font-bold flex items-center gap-2">
              <i class="fa-solid fa-triangle-exclamation text-brand-orange"></i>
              停滞の正体
            </p>
            <p class="mt-3 text-brand-slate leading-relaxed">
              DXは「プロジェクト」ではなく「文化」です。<br />
              文化は、現場が自力で “小さく作って回す” 経験を積まない限り変わりません。
            </p>
            <div class="mt-6 aspect-[16/10] rounded-2xl border border-dashed border-slate-300 bg-slate-50 flex items-center justify-center text-brand-slate">
              画像プレースホルダー
            </div>

            <div class="mt-6 rounded-2xl bg-brand-ink p-5 text-white">
              <p class="text-xs text-white/70">FocusCampが狙うこと</p>
              <p class="mt-2 text-lg font-extrabold leading-snug">
                “できない前提” を捨て、<br />
                “作って検証する前提” に組織を切り替える。
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Solution -->
    <section id="solution" class="bg-slate-50">
      <div class="mx-auto max-w-6xl px-4 py-14 sm:py-18">
        <div class="max-w-2xl">
          <p class="text-xs font-extrabold tracking-widest text-brand-cyan">SOLUTION</p>
          <h2 class="mt-2 text-2xl sm:text-3xl font-extrabold">Vibe Codingで「即時実装」する文化へ</h2>
          <p class="mt-4 text-brand-slate leading-relaxed">
            自然言語でAIと対話し、コーディング不要でアプリを作る。<br />
            Replitなら環境構築0秒。現場が “思いついたら作る” を実行できる状態をつくります。
          </p>
        </div>

        <div class="mt-10 grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
          <div class="rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
            <div class="h-12 w-12 rounded-2xl bg-brand-cyan/10 flex items-center justify-center">
              <i class="fa-solid fa-comments text-brand-cyan"></i>
            </div>
            <h3 class="mt-4 font-extrabold text-lg">自然言語で開発</h3>
            <p class="mt-2 text-sm text-brand-slate leading-relaxed">
              仕様を会話で詰め、AIと一緒に実装。現場が主役の開発へ。
            </p>
          </div>

          <div class="rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
            <div class="h-12 w-12 rounded-2xl bg-brand-orange/15 flex items-center justify-center">
              <i class="fa-solid fa-plug-circle-bolt text-brand-orange"></i>
            </div>
            <h3 class="mt-4 font-extrabold text-lg">即スタート環境</h3>
            <p class="mt-2 text-sm text-brand-slate leading-relaxed">
              Replitで “環境構築0秒”。インフラやセットアップで止まらない。
            </p>
          </div>

          <div class="rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
            <div class="h-12 w-12 rounded-2xl bg-brand-cyan/10 flex items-center justify-center">
              <i class="fa-solid fa-rotate text-brand-cyan"></i>
            </div>
            <h3 class="mt-4 font-extrabold text-lg">Sprintで積み上げ</h3>
            <p class="mt-2 text-sm text-brand-slate leading-relaxed">
              小さく作って、回して、改善する。変革に必要な“実装筋”を鍛える。
            </p>
          </div>
        </div>

        <div class="mt-10 rounded-3xl border border-slate-200 bg-white overflow-hidden shadow-soft">
          <div class="grid lg:grid-cols-2">
            <div class="p-6 sm:p-8">
              <p class="text-sm font-bold flex items-center gap-2">
                <i class="fa-solid fa-flag-checkered text-brand-cyan"></i>
                ゴール
              </p>
              <p class="mt-3 text-brand-slate leading-relaxed">
                4週間で、社内のリアル課題を題材に <span class="font-bold text-brand-ink">MVP</span> を作り、現場に戻して回す。<br />
                学びではなく、<span class="font-bold text-brand-ink">実装</span> が成果になります。
              </p>

              <ul class="mt-6 space-y-3 text-sm">
                <li class="flex gap-3">
                  <span class="mt-0.5 inline-flex h-6 w-6 items-center justify-center rounded-lg bg-brand-cyan/10">
                    <i class="fa-solid fa-check text-brand-cyan text-xs"></i>
                  </span>
                  <span class="text-brand-slate"><span class="font-bold text-brand-ink">ITスキル不問</span>：現場リーダーが主役</span>
                </li>
                <li class="flex gap-3">
                  <span class="mt-0.5 inline-flex h-6 w-6 items-center justify-center rounded-lg bg-brand-orange/15">
                    <i class="fa-solid fa-check text-brand-orange text-xs"></i>
                  </span>
                  <span class="text-brand-slate">OCR / RAGなど<span class="font-bold text-brand-ink">実務に効く構成</span></span>
                </li>
                <li class="flex gap-3">
                  <span class="mt-0.5 inline-flex h-6 w-6 items-center justify-center rounded-lg bg-brand-cyan/10">
                    <i class="fa-solid fa-check text-brand-cyan text-xs"></i>
                  </span>
                  <span class="text-brand-slate">成果物は <span class="font-bold text-brand-ink">社内共有できるMVP</span></span>
                </li>
              </ul>
            </div>

            <div class="bg-slate-50 p-6 sm:p-8">
              <div class="aspect-[16/10] rounded-2xl border border-dashed border-slate-300 bg-white flex items-center justify-center text-brand-slate">
                画像プレースホルダー
              </div>
              <div class="mt-5 rounded-2xl bg-brand-ink p-5 text-white">
                <p class="text-xs text-white/70">合言葉</p>
                <p class="mt-2 text-lg font-extrabold leading-snug">
                  「待つな。現場で作れ。」<br />
                  変革の速度を、組織に実装する。
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Curriculum -->
    <section id="curriculum" class="mx-auto max-w-6xl px-4 py-14 sm:py-18">
      <div class="max-w-2xl">
        <p class="text-xs font-extrabold tracking-widest text-brand-cyan">CURRICULUM</p>
        <h2 class="mt-2 text-2xl sm:text-3xl font-extrabold">4週間の工程</h2>
        <p class="mt-4 text-brand-slate leading-relaxed">
          “理解”ではなく、“実装”で進める4週間。毎週、目に見える成果物を積み上げます。
        </p>
      </div>

      <div class="mt-10 grid gap-4 lg:grid-cols-2">
        <!-- Week 1 -->
        <div class="rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
          <div class="flex items-start justify-between gap-4">
            <div>
              <p class="text-xs font-extrabold text-brand-cyan">WEEK 1</p>
              <h3 class="mt-1 text-lg font-extrabold">Kickoff &amp; Initiation（1Day集中）</h3>
              <p class="mt-2 text-sm text-brand-slate leading-relaxed">
                自社課題の選定／成功条件の定義／Sprint設計。AI Agentの基本運用もここで固めます。
              </p>
            </div>
            <div class="h-12 w-12 rounded-2xl bg-brand-cyan/10 flex items-center justify-center">
              <i class="fa-solid fa-play text-brand-cyan"></i>
            </div>
          </div>
          <div class="mt-5 aspect-[16/9] rounded-2xl border border-dashed border-slate-300 bg-slate-50 flex items-center justify-center text-brand-slate">
            画像プレースホルダー
          </div>
        </div>

        <!-- Week 2 -->
        <div class="rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
          <div class="flex items-start justify-between gap-4">
            <div>
              <p class="text-xs font-extrabold text-brand-cyan">WEEK 2</p>
              <h3 class="mt-1 text-lg font-extrabold">Sprint-1 名刺画像読み取りアプリ開発（OCR連携）</h3>
              <p class="mt-2 text-sm text-brand-slate leading-relaxed">
                画像→テキスト→データ化の一連を実装。現場の“面倒”を一発で削る体験をつくります。
              </p>
            </div>
            <div class="h-12 w-12 rounded-2xl bg-brand-orange/15 flex items-center justify-center">
              <i class="fa-solid fa-id-card text-brand-orange"></i>
            </div>
          </div>
          <div class="mt-5 aspect-[16/9] rounded-2xl border border-dashed border-slate-300 bg-slate-50 flex items-center justify-center text-brand-slate">
            画像プレースホルダー
          </div>
        </div>

        <!-- Week 3 -->
        <div class="rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
          <div class="flex items-start justify-between gap-4">
            <div>
              <p class="text-xs font-extrabold text-brand-cyan">WEEK 3</p>
              <h3 class="mt-1 text-lg font-extrabold">Sprint-2 社内FAQボット開発（RAG構築）</h3>
              <p class="mt-2 text-sm text-brand-slate leading-relaxed">
                社内ナレッジを“検索”から“対話”へ。業務の問い合わせ対応を加速させます。
              </p>
            </div>
            <div class="h-12 w-12 rounded-2xl bg-brand-cyan/10 flex items-center justify-center">
              <i class="fa-solid fa-robot text-brand-cyan"></i>
            </div>
          </div>
          <div class="mt-5 aspect-[16/9] rounded-2xl border border-dashed border-slate-300 bg-slate-50 flex items-center justify-center text-brand-slate">
            画像プレースホルダー
          </div>
        </div>

        <!-- Week 4 -->
        <div class="rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
          <div class="flex items-start justify-between gap-4">
            <div>
              <p class="text-xs font-extrabold text-brand-cyan">WEEK 4</p>
              <h3 class="mt-1 text-lg font-extrabold">Final Pitch 自社課題解決MVP発表</h3>
              <p class="mt-2 text-sm text-brand-slate leading-relaxed">
                作ったMVPを“現場に戻す”ための提案。運用・展開まで含めて勝ち筋を設計します。
              </p>
            </div>
            <div class="h-12 w-12 rounded-2xl bg-brand-orange/15 flex items-center justify-center">
              <i class="fa-solid fa-trophy text-brand-orange"></i>
            </div>
          </div>
          <div class="mt-5 aspect-[16/9] rounded-2xl border border-dashed border-slate-300 bg-slate-50 flex items-center justify-center text-brand-slate">
            画像プレースホルダー
          </div>
        </div>
      </div>
    </section>

    <!-- Instructor -->
    <section id="instructor" class="bg-slate-50">
      <div class="mx-auto max-w-6xl px-4 py-14 sm:py-18">
        <div class="grid gap-10 lg:grid-cols-2 lg:items-center">
          <div>
            <p class="text-xs font-extrabold tracking-widest text-brand-cyan">INSTRUCTOR</p>
            <h2 class="mt-2 text-2xl sm:text-3xl font-extrabold">講師</h2>
            <p class="mt-4 text-brand-slate leading-relaxed">
              “使い方”ではなく、“実装の勝ち筋”を教える。現場で回る設計まで導きます。
            </p>

            <div class="mt-6 rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
              <div class="flex items-start gap-4">
                <div class="h-14 w-14 rounded-3xl bg-brand-cyan/10 border border-brand-cyan/20 flex items-center justify-center">
                  <i class="fa-solid fa-user-astronaut text-brand-cyan text-xl"></i>
                </div>
                <div>
                  <p class="text-lg font-extrabold">佐藤 亮</p>
                  <p class="text-sm text-brand-slate">株式会社パールライト 代表</p>

                  <ul class="mt-4 space-y-2 text-sm text-brand-slate">
                    <li class="flex gap-2">
                      <i class="fa-solid fa-star text-brand-orange mt-0.5"></i>
                      <span>Replit 日本第一人者</span>
                    </li>
                    <li class="flex gap-2">
                      <i class="fa-solid fa-award text-brand-orange mt-0.5"></i>
                      <span>Replit公式ハッカソン最優秀賞</span>
                    </li>
                  </ul>
                </div>
              </div>

              <div class="mt-6 aspect-[16/10] rounded-2xl border border-dashed border-slate-300 bg-slate-50 flex items-center justify-center text-brand-slate">
                画像プレースホルダー
              </div>
            </div>
          </div>

          <div class="rounded-3xl border border-slate-200 bg-white shadow-soft overflow-hidden">
            <div class="p-6 sm:p-8 border-b border-slate-200">
              <p class="text-sm font-bold flex items-center gap-2">
                <i class="fa-solid fa-quote-left text-brand-cyan"></i>
                メッセージ
              </p>
              <p class="mt-3 text-brand-slate leading-relaxed">
                現場が変わるのは、「理解した時」ではなく「作れた時」です。<br />
                FocusCampは、“最短で作る経験”を組織に埋め込みます。
              </p>
            </div>
            <div class="p-6 sm:p-8">
              <div class="grid gap-3 sm:grid-cols-2">
                <div class="rounded-2xl bg-slate-50 p-4">
                  <p class="text-xs text-brand-slate">強み</p>
                  <p class="mt-1 font-extrabold">実装の高速化</p>
                </div>
                <div class="rounded-2xl bg-slate-50 p-4">
                  <p class="text-xs text-brand-slate">提供価値</p>
                  <p class="mt-1 font-extrabold">現場の自走力</p>
                </div>
                <div class="rounded-2xl bg-slate-50 p-4">
                  <p class="text-xs text-brand-slate">方法論</p>
                  <p class="mt-1 font-extrabold">Vibe Coding</p>
                </div>
                <div class="rounded-2xl bg-slate-50 p-4">
                  <p class="text-xs text-brand-slate">環境</p>
                  <p class="mt-1 font-extrabold">Replit × AI Agent</p>
                </div>
              </div>

              <div class="mt-6 rounded-2xl bg-brand-ink p-5 text-white">
                <p class="text-xs text-white/70">FocusCampは</p>
                <p class="mt-2 text-lg font-extrabold leading-snug">
                  “作れない組織”を、<br />
                  “作って回す組織”へ変えるためのブートキャンプです。
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Overview -->
    <section id="overview" class="mx-auto max-w-6xl px-4 py-14 sm:py-18">
      <div class="max-w-2xl">
        <p class="text-xs font-extrabold tracking-widest text-brand-cyan">OVERVIEW</p>
        <h2 class="mt-2 text-2xl sm:text-3xl font-extrabold">概要</h2>
        <p class="mt-4 text-brand-slate leading-relaxed">
          必要なのは “知識” ではなく “実装経験”。短期で成果を出す設計に絞りました。
        </p>
      </div>

      <div class="mt-10 grid gap-4 lg:grid-cols-3">
        <div class="rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
          <div class="h-12 w-12 rounded-2xl bg-brand-cyan/10 flex items-center justify-center">
            <i class="fa-regular fa-calendar text-brand-cyan"></i>
          </div>
          <p class="mt-4 text-sm text-brand-slate">期間</p>
          <p class="mt-1 text-lg font-extrabold">全4回 / 2月開始予定</p>
        </div>

        <div class="rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
          <div class="h-12 w-12 rounded-2xl bg-brand-orange/15 flex items-center justify-center">
            <i class="fa-solid fa-yen-sign text-brand-orange"></i>
          </div>
          <p class="mt-4 text-sm text-brand-slate">費用</p>
          <p class="mt-1 text-lg font-extrabold">98,000円（税別）/ 人</p>
        </div>

        <div class="rounded-3xl border border-slate-200 bg-white p-6 shadow-soft">
          <div class="h-12 w-12 rounded-2xl bg-brand-cyan/10 flex items-center justify-center">
            <i class="fa-solid fa-users text-brand-cyan"></i>
          </div>
          <p class="mt-4 text-sm text-brand-slate">対象</p>
          <p class="mt-1 text-lg font-extrabold">現場リーダー / DX推進担当者</p>
          <p class="mt-2 text-sm text-brand-slate">ITスキル不問</p>
        </div>
      </div>

      <!-- Apply -->
      <div id="apply" class="mt-10 rounded-3xl border border-slate-200 bg-white shadow-soft overflow-hidden">
        <div class="grid lg:grid-cols-2">
          <div class="p-6 sm:p-8">
            <p class="text-xs font-extrabold tracking-widest text-brand-cyan">APPLY</p>
            <h3 class="mt-2 text-xl sm:text-2xl font-extrabold">参加申し込み</h3>
            <p class="mt-4 text-brand-slate leading-relaxed">
              まずは必要情報を送信してください。折り返し、事務局よりご案内します。<br />
              <span class="text-xs">(ここは実運用に合わせてフォーム連携に差し替え可能)</span>
            </p>

            <form class="mt-6 space-y-4">
              <div>
                <label class="text-sm font-bold">お名前</label>
                <input
                  type="text"
                  placeholder="例）山田 太郎"
                  class="mt-2 w-full rounded-2xl border border-slate-200 bg-white px-4 py-3 text-sm focus:border-brand-cyan"
                />
              </div>

              <div>
                <label class="text-sm font-bold">メールアドレス</label>
                <input
                  type="email"
                  placeholder="example@company.com"
                  class="mt-2 w-full rounded-2xl border border-slate-200 bg-white px-4 py-3 text-sm focus:border-brand-cyan"
                />
              </div>

              <div>
                <label class="text-sm font-bold">所属 / 役職</label>
                <input
                  type="text"
                  placeholder="例）◯◯部 部長 / DX推進担当"
                  class="mt-2 w-full rounded-2xl border border-slate-200 bg-white px-4 py-3 text-sm focus:border-brand-cyan"
                />
              </div>

              <div>
                <label class="text-sm font-bold">解決したい課題（任意）</label>
                <textarea
                  rows="4"
                  placeholder="例）問い合わせ対応の削減、名刺入力の自動化、社内ナレッジ検索の改善 など"
                  class="mt-2 w-full rounded-2xl border border-slate-200 bg-white px-4 py-3 text-sm focus:border-brand-cyan"
                ></textarea>
              </div>

              <button
                type="button"
                class="w-full inline-flex items-center justify-center gap-2 rounded-2xl bg-brand-orange px-6 py-3 text-base font-extrabold text-white shadow-soft hover:brightness-105 active:brightness-95 transition"
              >
                <i class="fa-solid fa-paper-plane"></i>
                申し込み内容を送信
              </button>

              <p class="text-xs text-brand-slate">
                ※送信ボタンはデモです。実運用ではGoogleフォーム / Typeform / HubSpot等に接続してください。
              </p>
            </form>
          </div>

          <div class="bg-slate-50 p-6 sm:p-8">
            <div class="aspect-[16/10] rounded-2xl border border-dashed border-slate-300 bg-white flex items-center justify-center text-brand-slate">
              画像プレースホルダー
            </div>

            <div class="mt-6 rounded-2xl bg-brand-ink p-6 text-white">
              <p class="text-xs text-white/70">このプログラムで得られること</p>
              <ul class="mt-3 space-y-3 text-sm">
                <li class="flex gap-3">
                  <span class="mt-0.5 inline-flex h-6 w-6 items-center justify-center rounded-lg bg-white/10">
                    <i class="fa-solid fa-check text-brand-cyan text-xs"></i>
                  </span>
                  <span>現場主導で作る “実装体験”</span>
                </li>
                <li class="flex gap-3">
                  <span class="mt-0.5 inline-flex h-6 w-6 items-center justify-center rounded-lg bg-white/10">
                    <i class="fa-solid fa-check text-brand-cyan text-xs"></i>
                  </span>
                  <span>OCR / RAG を使った即戦力MVP</span>
                </li>
                <li class="flex gap-3">
                  <span class="mt-0.5 inline-flex h-6 w-6 items-center justify-center rounded-lg bg-white/10">
                    <i class="fa-solid fa-check text-brand-cyan text-xs"></i>
                  </span>
                  <span>“待つ組織”から “回す組織” への転換</span>
                </li>
              </ul>

              <div class="mt-6 rounded-2xl bg-white/10 p-4">
                <p class="text-xs text-white/70">ひとこと</p>
                <p class="mt-2 text-lg font-extrabold leading-snug">
                  変革は、会議では起きない。<br />
                  現場で “作れた瞬間” に始まる。
                </p>
              </div>
            </div>

            <div class="mt-6 grid gap-3 sm:grid-cols-2">
              <div class="rounded-2xl bg-white border border-slate-200 p-4">
                <p class="text-xs text-brand-slate">主な対象</p>
                <p class="mt-1 font-extrabold">現場リーダー</p>
              </div>
              <div class="rounded-2xl bg-white border border-slate-200 p-4">
                <p class="text-xs text-brand-slate">開発環境</p>
                <p class="mt-1 font-extrabold">Replit</p>
              </div>
              <div class="rounded-2xl bg-white border border-slate-200 p-4">
                <p class="text-xs text-brand-slate">開発スタイル</p>
                <p class="mt-1 font-extrabold">Vibe Coding</p>
              </div>
              <div class="rounded-2xl bg-white border border-slate-200 p-4">
                <p class="text-xs text-brand-slate">ゴール</p>
                <p class="mt-1 font-extrabold">MVP発表</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="border-t border-slate-200 bg-white">
      <div class="mx-auto max-w-6xl px-4 py-10">
        <div class="flex flex-col sm:flex-row items-start sm:items-center justify-between gap-6">
          <div class="flex items-center gap-3">
            <div class="h-10 w-10 rounded-2xl bg-brand-cyan/10 border border-brand-cyan/20 flex items-center justify-center">
              <i class="fa-solid fa-layer-group text-brand-cyan"></i>
            </div>
            <div>
              <p class="text-sm font-bold">Aoba-BBT AIx FocusCamp</p>
              <p class="text-xs text-brand-slate">AIx 企業変革 Lite FocusCamp</p>
            </div>
          </div>

          <div class="text-xs text-brand-slate">
            © Aoba-BBT Learning Hub
          </div>
        </div>

        <div class="mt-6 text-xs text-brand-slate leading-relaxed">
          ※本ページはLPテンプレートです。記載内容（開催日程、詳細条件、申込導線、注意事項等）は運用に合わせて編集してください。
        </div>
      </div>
    </footer>
  </body>
</html>
```
