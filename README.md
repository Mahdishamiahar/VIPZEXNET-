<!DOCTYPE html>
<html dir="rtl" lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="VIPZEXNET - سرویس VPN پرسرعت با اتصال پایدار برای تمام دستگاه‌ها">
    <title>VIPZEXNET - سرویس VPN پرسرعت</title>
    <style>
        :root {
            --primary-color: #00c853;
            --primary-dark: #009624;
            --error-color: #f44336;
            --text-color: #333;
            --light-gray: #f5f5f5;
            --dark-bg: rgba(0,0,0,0.7);
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Tahoma', sans-serif;
            margin: 0;
            padding: 0;
            color: #ffffff;
            line-height: 1.7;
            background: url('background.jpg') no-repeat center center fixed;
            background-size: cover;
        }
        
        /* Header Styles */
        header {
            background-color: var(--dark-bg);
            padding: 1.5rem;
            text-align: center;
            border-bottom: 2px solid var(--primary-color);
        }
        
        header h1 {
            margin: 0;
            font-size: 1.8rem;
            color: var(--primary-color);
        }
        
        header p {
            margin: 0.5rem 0 0;
            opacity: 0.9;
        }
        
        /* Main Content Styles */
        main {
            padding: 2rem;
            max-width: 1200px;
            margin: 2rem auto;
        }
        
        /* VPN Plans Styles */
        .plans-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-bottom: 3rem;
        }
        
        .plan-card {
            background-color: rgba(0,0,0,0.6);
            padding: 1.5rem;
            border-radius: 10px;
            width: 300px;
            box-shadow: 0 0 15px rgba(0,0,0,0.3);
            border-right: 3px solid var(--primary-color);
            transition: transform 0.3s;
        }
        
        .plan-card:hover {
            transform: translateY(-5px);
        }
        
        .plan-card h2 {
            color: var(--primary-color);
            margin-top: 0;
        }
        
        .buy-btn {
            background-color: var(--primary-color);
            color: white;
            padding: 0.7rem 1.5rem;
            text-decoration: none;
            border-radius: 6px;
            display: inline-block;
            margin-top: 1rem;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .buy-btn:hover {
            background-color: var(--primary-dark);
        }
        
        /* Info Box Styles */
        .info-box {
            background-color: rgba(0,0,0,0.6);
            padding: 1.5rem;
            border-radius: 10px;
            margin-bottom: 2rem;
            border-right: 3px solid var(--primary-color);
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }
        
        /* Auth Box Styles */
        .auth-container {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 60vh;
        }
        
        .auth-box {
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 10px;
            box-shadow: 0 5px 25px rgba(0, 0, 0, 0.15);
            width: 100%;
            max-width: 400px;
            overflow: hidden;
            border-top: 5px solid var(--primary-color);
            color: var(--text-color);
        }
        
        .auth-header {
            padding: 25px;
            text-align: center;
            background-color: #fff;
        }
        
        .auth-title {
            font-size: 18px;
            color: var(--text-color);
            margin-bottom: 5px;
        }
        
        .auth-body {
            padding: 25px;
        }
        
        .form-group {
            margin-bottom: 20px;
            text-align: right;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-size: 14px;
            transition: all 0.3s;
        }
        
        .form-control:focus {
            border-color: var(--primary-color);
            outline: none;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 6px;
            width: 100%;
            font-size: 16px;
            cursor: pointer;
            transition: all 0.3s;
            text-align: center;
        }
        
        .btn:hover {
            background-color: var(--primary-dark);
        }
        
        .hidden {
            display: none;
        }
        
        .loading {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: #fff;
            animation: spin 1s ease-in-out infinite;
            margin-left: 10px;
            vertical-align: middle;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        .alert {
            padding: 12px 15px;
            border-radius: 6px;
            margin-bottom: 20px;
            font-size: 14px;
        }
        
        .alert-success {
            background-color: #e8f5e9;
            color: #2e7d32;
            border-left: 4px solid #2e7d32;
        }
        
        .alert-error {
            background-color: #ffebee;
            color: var(--error-color);
            border-left: 4px solid var(--error-color);
        }
        
        /* Social Icons */
        .social-section {
            text-align: center;
            margin: 3rem 0;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 1.5rem;
        }
        
        .social-icon {
            width: 48px;
            height: 48px;
            border-radius: 12px;
            transition: transform 0.3s;
        }
        
        .social-icon:hover {
            transform: scale(1.1);
        }
        
        /* Footer Styles */
        footer {
            background-color: var(--dark-bg);
            text-align: center;
            padding: 1.5rem;
            margin-top: 3rem;
            border-top: 2px solid var(--primary-color);
        }
        
        .footer-link {
            color: var(--primary-color);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-link:hover {
            text-decoration: underline;
        }
        
        /* Dashboard Styles (hidden by default) */
        #dashboard {
            display: none;
            padding: 2rem;
            max-width: 1200px;
            margin: auto;
            background-color: rgba(0,0,0,0.6);
            border-radius: 10px;
        }
        
        .welcome-message {
            text-align: center;
            margin-bottom: 2rem;
        }
        
        .user-email {
            color: var(--primary-color);
            font-weight: bold;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .plans-container {
                flex-direction: column;
                align-items: center;
            }
            
            .plan-card {
                width: 100%;
                max-width: 400px;
            }
            
            header h1 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Main Website Content (visible when not authenticated) -->
    <div id="main-content">
        <header>
            <h1>🔋 با VIPZEXNET بهترین سرعت VPN را تجربه کنید - بدون قطعی</h1>
            <p>اتصال پرسرعت، پایدار، بدون محدودیت و قابل استفاده در تمامی دستگاه‌ها</p>
        </header>

        <main>
            <div class="info-box">
                <p>🌍 لوکیشن‌ها: 🇩🇪 🇦🇪 🇹🇷 🇸🇪 🇫🇷 🇬🇧 🇺🇸</p>
                <p>📱 دستگاه‌ها: اندروید، iOS، ویندوز</p>
                <p>🎯 مناسب برای: اینستاگرام، یوتیوب، گیم و موارد دیگر</p>
                <p>🇮🇷 لذت یک V.P.N پرسرعت و با کیفیت را با ما تجربه کنید 🇮🇷</p>
            </div>

            <h2 style="text-align: center; color: var(--primary-color); margin-bottom: 1.5rem;">پلن‌های اشتراک VIPZEXNET</h2>
            
            <div class="plans-container">
                <div class="plan-card">
                    <h2>⭐️ نامحدود تک‌کاربر</h2>
                    <p>قیمت: ۱۰۰ هزار تومان</p>
                    <a class="buy-btn" href="#auth" onclick="showAuth()">خرید</a>
                </div>

                <div class="plan-card">
                    <h2>⭐️ نامحدود دوکاربر</h2>
                    <p>قیمت: ۵۰ هزار تومان</p>
                    <a class="buy-btn" href="#auth" onclick="showAuth()">خرید</a>
                </div>

                <div class="plan-card">
                    <h2>⭐️ نامحدود سه‌کاربر</h2>
                    <p>قیمت: ۳۰ هزار تومان</p>
                    <a class="buy-btn" href="#auth" onclick="showAuth()">خرید</a>
                </div>
            </div>

            <!-- Authentication Section -->
            <div id="auth" class="auth-container" style="display: none;">
                <div class="auth-box">
                    <div class="auth-header">
                        <div style="color: var(--primary-color); font-size: 24px; font-weight: bold;">VIPZEXNET</div>
                        <h1 class="auth-title">ورود / ثبت‌نام در سرویس VPN پرسرعت</h1>
                    </div>
                    
                    <div class="auth-body">
                        <!-- Step 1: Email Input -->
                        <div id="email-step">
                            <div id="email-alert" class="alert hidden"></div>
                            
                            <div class="form-group">
                                <input type="email" id="email" class="form-control" placeholder="ایمیل خود را وارد کنید" required>
                            </div>
                            
                            <button id="send-btn" class="btn" onclick="sendVerificationCode()">
                                ارسال کد تایید
                            </button>
                        </div>
                        
                        <!-- Step 2: Verification Code -->
                        <div id="code-step" class="hidden">
                            <div id="code-alert" class="alert hidden"></div>
                            
                            <div class="alert alert-success">
                                کد تایید به ایمیل <strong id="user-email"></strong> ارسال شد.
                            </div>
                            
                            <div class="form-group">
                                <input type="text" id="verification-code" class="form-control" placeholder="کد 6 رقمی ارسال شده" maxlength="6" required>
                            </div>
                            
                            <button id="verify-btn" class="btn" onclick="verifyCode()">
                                تایید و ورود
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <div class="social-section">
                <h2 style="color: var(--primary-color);">برای اطلاع از خبرهای VIPZEXNET ما را دنبال کنید</h2>
                <div class="social-icons">
                    <a href="https://t.me/VIPZEXNET" target="_blank" rel="noopener noreferrer">
                        <img src="https://img.icons8.com/fluency/48/telegram-app.png" alt="تلگرام" class="social-icon">
                    </a>
                    <a href="https://rubika.ir/VIPZEXNET" target="_blank" rel="noopener noreferrer">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/6/66/Rubika_app_logo.png" alt="روبیکا" class="social-icon">
                    </a>
                </div>
            </div>
        </main>

        <footer>
            <p>پشتیبانی در تلگرام: <a href="https://t.me/Mahdi_shami" class="footer-link" target="_blank" rel="noopener noreferrer">@Mahdi_shami</a></p>
            <p>کلیه حقوق این سایت متعلق به VIPZEXNET است. © 2023</p>
        </footer>
    </div>

    <!-- Dashboard Content (visible when authenticated) -->
    <div id="dashboard">
        <header>
            <h1>🔋 پنل کاربری VIPZEXNET</h1>
        </header>

        <main>
            <div class="welcome-message">
                <h2>خوش آمدید <span class="user-email" id="dashboard-email"></span></h2>
                <p>از طریق این پنل می‌توانید اشتراک‌های خود را مدیریت کنید</p>
            </div>

            <div class="info-box">
                <h2 style="color: var(--primary-color); margin-top: 0;">اشتراک فعال شما</h2>
                <p>⭐️ پلن: نامحدود تک‌کاربر</p>
                <p>📅 اعتبار تا: ۱۴۰۲/۱۰/۱۵</p>
                <p>📱 دستگاه‌های متصل: ۱ از ۱</p>
            </div>

            <div style="text-align: center; margin-top: 2rem;">
                <button class="btn" style="width: auto; padding: 10px 25px;" onclick="logout()">خروج از حساب کاربری</button>
            </div>
        </main>

        <footer>
            <p>پشتیبانی ۲۴ ساعته: <a href="https://t.me/Mahdi_shami" class="footer-link" target="_blank" rel="noopener noreferrer">@Mahdi_shami</a></p>
            <p>کلیه حقوق این سایت متعلق به VIPZEXNET است. © 2023</p>
        </footer>
    </div>

    <script>
        // Global variables
        let currentEmail = '';
        
        // Check authentication status on page load
        document.addEventListener('DOMContentLoaded', function() {
            const isAuthenticated = localStorage.getItem('vipzexnet_auth') === 'true';
            const savedEmail = localStorage.getItem('vipzexnet_email');
            
            if (isAuthenticated && savedEmail) {
                showDashboard(savedEmail);
            }
        });
        
        // Show authentication form
        function showAuth() {
            document.getElementById('auth').style.display = 'flex';
            window.scrollTo({
                top: document.getElementById('auth').offsetTop,
                behavior: 'smooth'
            });
        }
        
        // Show alert message
        function showAlert(elementId, message, type = 'error') {
            const element = document.getElementById(elementId);
            element.textContent = message;
            element.className = `alert alert-${type}`;
            element.classList.remove('hidden');
            
            // Auto hide after 5 seconds
            if (type === 'error') {
                setTimeout(() => {
                    element.classList.add('hidden');
                }, 5000);
            }
        }
        
        // Set loading state for buttons
        function setLoading(buttonId, isLoading) {
            const btn = document.getElementById(buttonId);
            btn.disabled = isLoading;
            if (isLoading) {
                btn.innerHTML = buttonId === 'send-btn' 
                    ? 'در حال ارسال کد <span class="loading"></span>'
                    : 'در حال تایید <span class="loading"></span>';
            } else {
                btn.innerHTML = buttonId === 'send-btn' ? 'ارسال کد تایید' : 'تایید و ورود';
            }
        }
        
        // Send verification code
        async function sendVerificationCode() {
            const email = document.getElementById('email').value.trim();
            currentEmail = email;
            
            // Validate email
            if (!email) {
                showAlert('email-alert', 'لطفاً ایمیل خود را وارد کنید');
                return;
            }
            
            if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)) {
                showAlert('email-alert', 'ایمیل وارد شده معتبر نیست');
                return;
            }
            
            setLoading('send-btn', true);
            
            try {
                // Call API to send verification code
                const response = await fetch(`https://api.api-code.ir/verify-code/index.php?email=${encodeURIComponent(email)}`);
                const data = await response.json();
                
                if (data.status === 'success') {
                    // Show code step
                    document.getElementById('email-step').classList.add('hidden');
                    document.getElementById('code-step').classList.remove('hidden');
                    document.getElementById('user-email').textContent = email;
                    
                    // Focus on code input
                    setTimeout(() => {
                        document.getElementById('verification-code').focus();
                    }, 300);
                } else {
                    showAlert('email-alert', data.message || 'خطا در ارسال کد تایید');
                }
            } catch (error) {
                showAlert('email-alert', 'خطا در ارتباط با سرور. لطفاً دوباره تلاش کنید.');
                console.error('Error sending verification code:', error);
            } finally {
                setLoading('send-btn', false);
            }
        }
        
        // Verify the code
        async function verifyCode() {
            const code = document.getElementById('verification-code').value.trim();
            
            // Validate code
            if (!code || code.length !== 6) {
                showAlert('code-alert', 'لطفاً کد 6 رقمی را وارد کنید');
                return;
            }
            
            setLoading('verify-btn', true);
            
            try {
                // Call API to verify code
                const response = await fetch(
                    `https://api.api-code.ir/verify-code/verify.php?email=${encodeURIComponent(currentEmail)}&code=${code}`
                );
                const data = await response.json();
                
                if (data.status === 'success' && data.verified) {
                    // Successful verification
                    showAlert('code-alert', 'احراز هویت موفق!', 'success');
                    
                    // Save authentication
                    localStorage.setItem('vipzexnet_auth', 'true');
                    localStorage.setItem('vipzexnet_email', currentEmail);
                    
                    // Show dashboard after 1 second
                    setTimeout(() => {
                        showDashboard(currentEmail);
                    }, 1000);
                } else {
                    showAlert('code-alert', data.message || 'کد تایید نامعتبر است');
                }
            } catch (error) {
                showAlert('code-alert', 'خطا در ارتباط با سرور', 'error');
                console.error('Error verifying code:', error);
            } finally {
                setLoading('verify-btn', false);
            }
        }
        
        // Show dashboard
        function showDashboard(email) {
            document.getElementById('main-content').style.display = 'none';
            document.getElementById('dashboard').style.display = 'block';
            document.getElementById('dashboard-email').textContent = email;
        }
        
        // Logout function
        function logout() {
            localStorage.removeItem('vipzexnet_auth');
            localStorage.removeItem('vipzexnet_email');
            document.getElementBy
