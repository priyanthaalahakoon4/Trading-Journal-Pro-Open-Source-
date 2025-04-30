<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TradeJournal - Advanced PHP Trading Journal</title>
    <style>
        /* CodeCanyon Description Styles */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #333;
            line-height: 1.6;
            padding: 0;
            margin: 0;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .logo {
            max-width: 200px;
            margin-bottom: 20px;
        }
        
        h1 {
            font-size: 36px;
            color: #0e2439;
            margin-bottom: 15px;
        }
        
        .tagline {
            font-size: 20px;
            color: #4a90e2;
            margin-bottom: 30px;
        }
        
        .hero-image {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            margin-bottom: 40px;
        }
        
        .section {
            margin-bottom: 50px;
        }
        
        h2 {
            font-size: 28px;
            color: #0e2439;
            border-bottom: 2px solid #4a90e2;
            padding-bottom: 10px;
            margin-bottom: 25px;
        }
        
        .feature-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .feature-item {
            background: #f9f9f9;
            border-radius: 8px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .feature-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            color: #4a90e2;
            font-size: 36px;
            margin-bottom: 15px;
        }
        
        .feature-title {
            font-size: 20px;
            font-weight: 600;
            margin-bottom: 15px;
            color: #0e2439;
        }
        
        .feature-description {
            font-size: 16px;
            color: #666;
        }
        
        .screenshot {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 30px;
        }
        
        .screenshot-caption {
            text-align: center;
            font-size: 16px;
            color: #777;
            margin-bottom: 40px;
        }
        
        .highlight-box {
            background: linear-gradient(135deg, #4a90e2 0%, #2c3e50 100%);
            color: white;
            padding: 35px;
            border-radius: 8px;
            margin: 40px 0;
            box-shadow: 0 8px 25px rgba(74, 144, 226, 0.3);
        }
        
        .highlight-box h3 {
            font-size: 24px;
            margin-bottom: 15px;
        }
        
        .highlight-box p {
            font-size: 18px;
            margin-bottom: 20px;
        }
        
        .button {
            display: inline-block;
            background: #ffffff;
            color: #4a90e2;
            padding: 12px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        .button:hover {
            background: rgba(255, 255, 255, 0.9);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .requirements {
            background: #f4f8fb;
            padding: 30px;
            border-radius: 8px;
            margin-bottom: 40px;
        }
        
        .requirements h3 {
            font-size: 22px;
            margin-bottom: 20px;
            color: #0e2439;
        }
        
        .requirements ul {
            list-style-type: none;
            padding: 0;
        }
        
        .requirements li {
            padding: 10px 0;
            border-bottom: 1px solid #e0e9f1;
            font-size: 16px;
        }
        
        .requirements li:last-child {
            border-bottom: none;
        }
        
        .requirements li:before {
            content: "✓";
            color: #4a90e2;
            margin-right: 10px;
            font-weight: bold;
        }
        
        .accordion {
            margin-bottom: 40px;
        }
        
        .accordion-item {
            border: 1px solid #e0e9f1;
            border-radius: 8px;
            margin-bottom: 15px;
            overflow: hidden;
        }
        
        .accordion-header {
            background: #f4f8fb;
            padding: 15px 20px;
            cursor: pointer;
            font-weight: 600;
            color: #0e2439;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .accordion-header::after {
            content: "+";
            font-size: 20px;
            color: #4a90e2;
        }
        
        .accordion-content {
            padding: 20px;
            display: none;
            background: #ffffff;
        }
        
        .footer {
            text-align: center;
            padding: 30px 0;
            border-top: 1px solid #e0e9f1;
            margin-top: 50px;
        }
        
        .footer p {
            color: #777;
            font-size: 16px;
        }
        
        .theme-preview {
            display: flex;
            justify-content: space-between;
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .theme-item {
            flex: 1;
            text-align: center;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }
        
        .theme-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .theme-name {
            padding: 15px;
            background: #f4f8fb;
            font-weight: 600;
            color: #0e2439;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .feature-grid {
                grid-template-columns: 1fr;
            }
            
            .theme-preview {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header">
        <img src="images/logo.png" alt="TradeJournal Logo" class="logo">
        <h1>TradeJournal Pro</h1>
        <p class="tagline">Advanced PHP Trading Journal for Serious Traders</p>
    </div>

    <img src="images/hero-image.png" alt="TradeJournal Dashboard" class="hero-image">

    <div class="section">
        <h2>Your Ultimate Trading Companion</h2>
        <p>TradeJournal Pro is a comprehensive PHP-based trading journal application designed to help traders track, analyze, and improve their trading performance. Built with modern design principles and focusing on user experience, TradeJournal Pro gives you all the tools you need to become a better trader.</p>
        <p>Login credentials for live demo </p>
        <p>Username : test </p>
        <p>Password : test123@ </p>
        <div class="highlight-box">
            <h3>Single-User Application</h3>
            <p>TradeJournal Pro is designed as a personal trading journal with all the features you need to track your trades, analyze your performance, and improve your trading strategy.</p>
            <a href="#features" class="button">Explore Features</a>
        </div>
    </div>

    <div class="section" id="features">
        <h2>Key Features</h2>
        
        <div class="feature-grid">
            <div class="feature-item">
                <div class="feature-icon">📊</div>
                <div class="feature-title">Comprehensive Dashboard</div>
                <div class="feature-description">Get a clear overview of your trading performance with a sleek, modern dashboard displaying key metrics and recent trades.</div>
            </div>
            
            <div class="feature-item">
                <div class="feature-icon">📈</div>
                <div class="feature-title">Detailed Trade Tracking</div>
                <div class="feature-description">Log all aspects of your trades including entry/exit points, stop loss, take profit, and risk-reward ratios.</div>
            </div>
            
            <div class="feature-item">
                <div class="feature-icon">📱</div>
                <div class="feature-title">Responsive Design</div>
                <div class="feature-description">Enjoy the same great experience on desktop, tablet, or mobile with our fully responsive design.</div>
            </div>
            
            <div class="feature-item">
                <div class="feature-icon">🎨</div>
                <div class="feature-title">Modern Design</div>
                <div class="feature-description">Sleek, minimalist layout with bold typography, responsive design, and intuitive navigation for enhanced user experience.</div>
            </div>
            
            <div class="feature-item">
                <div class="feature-icon">📸</div>
                <div class="feature-title">Trade Screenshots</div>
                <div class="feature-description">Upload screenshots of your trade charts for better visual reference and analysis.</div>
            </div>
            
            <div class="feature-item">
                <div class="feature-icon">🔒</div>
                <div class="feature-title">Secure Authentication</div>
                <div class="feature-description">Keep your trading data secure with our robust authentication system and user management.</div>
            </div>
            
            <div class="feature-item">
                <div class="feature-icon">💹</div>
                <div class="feature-title">Performance Analytics</div>
                <div class="feature-description">Analyze your trading performance with detailed statistics, win rates, and profit/loss tracking.</div>
            </div>
            
            <div class="feature-item">
                <div class="feature-icon">⚙️</div>
                <div class="feature-title">Customizable Settings</div>
                <div class="feature-description">Configure currency symbols, initial capital, and other parameters to match your trading style.</div>
            </div>
            
            <div class="feature-item">
                <div class="feature-icon">🧮</div>
                <div class="feature-title">Position Calculator</div>
                <div class="feature-description">Calculate optimal position sizes based on your risk tolerance and account size.</div>
            </div>
        </div>
    </div>

    <div class="section">
        <h2>Easy Installation</h2>
        <p>TradeJournal Pro features a streamlined installation wizard that guides you through the setup process in just a few steps:</p>
        
        <img src="images/installation-screenshot.png" alt="Installation Wizard" class="screenshot">
        <p class="screenshot-caption">The intuitive installation wizard makes setup a breeze</p>
        
        <div class="requirements">
            <h3>System Requirements</h3>
            <ul>
                <li>PHP 7.4 or higher</li>
                <li>MySQL 5.7 or higher</li>
                <li>mod_rewrite enabled (for clean URLs)</li>
                <li>GD Library (for image handling)</li>
                <li>Any modern web server (Apache, Nginx, etc.)</li>
            </ul>
        </div>
    </div>

    

    <div class="section">
        <h2>Core Functionality</h2>
        
        <img src="images/dashboard-screenshot.png" alt="Dashboard Screenshot" class="screenshot">
        <p class="screenshot-caption">Comprehensive dashboard with key performance metrics</p>
        
        
        
        <img src="images/analysis-screenshot.png" alt="Performance Analysis" class="screenshot">
        <p class="screenshot-caption">Detailed performance analysis to improve your trading</p>
        
        <img src="images/calculator-screenshot.png" alt="Position Calculator" class="screenshot">
        <p class="screenshot-caption">Position calculator for optimal risk management</p>
    </div>

    <div class="section">
        <h2>Frequently Asked Questions</h2>
        
        <div class="accordion">
            <div class="accordion-item">
                <div class="accordion-header">Is TradeJournal Pro suitable for all types of trading?</div>
                <div class="accordion-content">
                    <p>Yes! TradeJournal Pro is designed to be flexible and can be used for various types of trading including stocks, forex, crypto, options, and futures. You can customize the fields and parameters to suit your specific trading style.</p>
                </div>
            </div>
            
            <div class="accordion-item">
                <div class="accordion-header">Can I install TradeJournal Pro on shared hosting?</div>
                <div class="accordion-content">
                    <p>Absolutely! TradeJournal Pro is designed to work on most shared hosting environments as long as they meet the minimum system requirements (PHP 7.4+, MySQL 5.7+).</p>
                </div>
            </div>
            
            <div class="accordion-item">
                <div class="accordion-header">Does TradeJournal Pro include updates?</div>
                <div class="accordion-content">
                    <p>Yes, your purchase includes free updates within the current major version. We regularly release updates with bug fixes, security improvements, and new features.</p>
                </div>
            </div>
            
            <div class="accordion-item">
                <div class="accordion-header">Can I customize TradeJournal Pro?</div>
                <div class="accordion-content">
                    <p>Yes, TradeJournal Pro is built with clean, modular code that makes it easy to customize. You can modify the themes, add new features, or integrate with other systems. The code is well-documented to help with customization.</p>
                </div>
            </div>
            
         

    <div class="highlight-box">
        <h3>Start Improving Your Trading Today!</h3>
        <p>TradeJournal Pro gives you all the tools you need to track, analyze, and improve your trading performance. With its modern design, comprehensive features, and ease of use, it's the perfect companion for serious traders.</p>
        <a href="#" class="button">Live Demo</a>
    </div>

</div>

<script>
    // Simple accordion functionality
    document.querySelectorAll('.accordion-header').forEach(header => {
        header.addEventListener('click', () => {
            const content = header.nextElementSibling;
            content.style.display = content.style.display === 'block' ? 'none' : 'block';
        });
    });
</script>

</body>
</html>
