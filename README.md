# pak-clip
AI-powered video clipping platform for Pakistan

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pak-Clip | AI Video Clipping</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      background: #080b12;
      color: #f5f7ff;
      font-family: Inter, Arial, sans-serif;
    }
    nav {
      height: 76px;
      padding: 0 7%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      border-bottom: 1px solid #202637;
    }
    .logo { font-size: 25px; font-weight: 900; }
    .logo span { color: #28d99b; }
    nav a {
      color: #aeb7c9;
      text-decoration: none;
      margin-left: 24px;
      font-size: 14px;
    }
    .btn {
      border: 0;
      border-radius: 9px;
      background: #20d69a;
      color: #06120e;
      padding: 13px 20px;
      font-weight: 800;
      cursor: pointer;
    }
    .hero {
      text-align: center;
      padding: 95px 20px 65px;
      background: radial-gradient(ellipse at top, #123d36 0%, #080b12 65%);
    }
    .tag {
      color: #37e5ac;
      border: 1px solid #236b55;
      background: #102820;
      display: inline-block;
      padding: 9px 16px;
      border-radius: 30px;
      font-size: 12px;
    }
    h1 {
      font-size: clamp(40px, 7vw, 72px);
      line-height: 1.1;
      margin: 27px 0 20px;
      font-weight: 900;
    }
    h1 span { color: #29dba0; }
    .hero p {
      color: #aab4c5;
      max-width: 590px;
      margin: auto;
      line-height: 1.8;
    }
    .hero .btn { margin-top: 30px; }
    section { padding: 65px 7%; }
    .section-title { text-align: center; margin-bottom: 35px; }
    .section-title h2 { font-size: 32px; margin-bottom: 12px; }
    .section-title p { color: #929caf; }
    .workspace {
      max-width: 850px;
      margin: auto;
      padding: 28px;
      background: #111725;
      border: 1px solid #283348;
      border-radius: 17px;
    }
    .upload {
      border: 2px dashed #3b5363;
      padding: 45px 15px;
      text-align: center;
      border-radius: 12px;
      background: #0b111d;
    }
    .upload .symbol { font-size: 42px; margin-bottom: 12px; }
    .upload p { color: #aab4c5; margin: 10px 0 20px; }
    input[type=file] { max-width: 100%; color: #aab4c5; }
    video {
      width: 100%;
      max-height: 350px;
      margin-top: 20px;
      border-radius: 10px;
      display: none;
      background: black;
    }
    .credits {
      display: flex;
      justify-content: space-between;
      gap: 10px;
      flex-wrap: wrap;
      margin-bottom: 22px;
      color: #c3ccda;
    }
    .credit-number { color: #2be0a4; font-weight: 800; }
    .plans {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      max-width: 1050px;
      margin: auto;
    }
    .plan {
      padding: 27px;
      background: #111725;
      border: 1px solid #283348;
      border-radius: 15px;
    }
    .plan.featured { border: 1px solid #27d99e; }
    .plan h3 { font-size: 21px; }
    .price { font-size: 34px; font-weight: 900; margin: 20px 0; }
    .price small { font-size: 13px; color: #929caf; }
    .plan ul { list-style: none; margin: 20px 0; }
    .plan li { color: #bac4d4; margin: 14px 0; font-size: 14px; }
    .plan li::before { content: "✓ "; color: #2be0a4; }
    .plan .btn { width: 100%; }
    .payments {
      text-align: center;
      padding: 30px;
      border: 1px solid #283348;
      background: #111725;
      border-radius: 14px;
      max-width: 850px;
      margin: auto;
    }
    .payment-methods {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 13px;
      margin-top: 22px;
    }
    .payment {
      padding: 14px 22px;
      border-radius: 9px;
      background: #202a3a;
      color: white;
      font-weight: 700;
    }
    footer {
      padding: 30px;
      text-align: center;
      border-top: 1px solid #202637;
      color: #8390a4;
      font-size: 13px;
    }
    @media(max-width: 700px) {
      nav { padding: 0 5%; }
      nav a { margin-left: 9px; font-size: 12px; }
      .plans { grid-template-columns: 1fr; }
      section { padding: 45px 5%; }
      .workspace { padding: 16px; }
    }
  </style>
</head>
<body>

<nav>
  <div class="logo">PAK<span>-CLIP</span></div>
  <div>
    <a href="#studio">Studio</a>
    <a href="#pricing">Pricing</a>
    <a href="#payments">Payments</a>
  </div>
</nav>

<header class="hero">
  <div class="tag">🇵🇰 MADE FOR PAKISTAN</div>
  <h1>Turn Videos Into<br><span>Viral Clips.</span></h1>
  <p>
    Your video clipping workspace. Upload your videos,
    create short-form content and get ready to share
    your best moments.
  </p>
  <a href="#studio"><button class="btn">Start Clipping →</button></a>
</header>

<section id="studio">
  <div class="section-title">
    <h2>Your Clipping Studio</h2>
    <p>Upload a video and get started.</p>
  </div>

  <div class="workspace">
    <div class="credits">
      <span>Free daily credits</span>
      <span class="credit-number">200 / 200 credits</span>
    </div>

    <div class="upload">
      <div class="symbol">🎬</div>
      <h3>Upload Your Video</h3>
      <p>Select a video from your device to preview it.</p>
      <input type="file" id="videoInput" accept="video/*">
      <video id="videoPreview" controls></video>
    </div>
  </div>
</section>

<section id="pricing">
  <div class="section-title">
    <h2>Simple Pricing</h2>
    <p>Choose the plan that works for you.</p>
  </div>

  <div class="plans">
    <div class="plan">
      <h3>Free</h3>
      <div class="price">Rs. 0</div>
      <p>Perfect for getting started.</p>
      <ul>
        <li>200 credits every 24 hours</li>
        <li>Video upload</li>
        <li>Basic clipping workspace</li>
      </ul>
      <button class="btn" onclick="alert('Free plan selected!')">Get Started</button>
    </div>

    <div class="plan">
      <h3>Monthly</h3>
      <div class="price">Rs. 1,499 <small>/ month</small></div>
      <p>For regular creators.</p>
      <ul>
        <li>Unlimited credits</li>
        <li>Premium workspace</li>
        <li>All clipping tools</li>
      </ul>
      <button class="btn" onclick="alert('Monthly plan selected! Payment setup coming soon.')">Choose Monthly</button>
    </div>

    <div class="plan featured">
      <h3>Yearly ⭐</h3>
      <div class="price">Rs. 2,499 <small>/ year</small></div>
      <p>For serious creators.</p>
      <ul>
        <li>Unlimited credits</li>
        <li>Premium workspace</li>
        <li>All clipping tools</li>
        <li>12-month membership</li>
      </ul>
      <button class="btn" onclick="alert('Yearly plan selected! Payment setup coming soon.')">Choose Yearly</button>
    </div>
  </div>
</section>

<section id="payments">
  <div class="section-title">
    <h2>Pakistani Payment Methods</h2>
    <p>Local payment options for your membership.</p>
  </div>
  <div class="payments">
    <h3>Choose your payment method</h3>
    <div class="payment-methods">
      <div class="payment">Easypaisa</div>
      <div class="payment">JazzCash</div>
      <div class="payment">SadaPay</div>
    </div>
    <p style="color:#929caf;margin-top:20px;font-size:13px">
      Payment integration will be connected in a later development step.
    </p>
  </div>
</section>

<footer>
  © 2026 Pak-Clip. Built for creators in Pakistan 🇵🇰
</footer>

<script>
  const input = document.getElementById("videoInput");
  const preview = document.getElementById("videoPreview");
  let currentVideoURL = null;

  input.addEventListener("change", () => {
    const file = input.files[0];
    if (!file) return;

    if (currentVideoURL) URL.revokeObjectURL(currentVideoURL);

    currentVideoURL = URL.createObjectURL(file);
    preview.src = currentVideoURL;
    preview.style.display = "block";
  });
</script>

</body>
</html>
