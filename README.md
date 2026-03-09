
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PDF Lover Ultimate - World's Most Multilingual PDF Tool (116 Languages)</title>
    <meta name="description" content="World's most multilingual PDF tool with 116 languages. 100+ PDF tools, CV Maker, AI Assistant, Professional Dashboard">
    <meta name="keywords" content="PDF tools, multilingual, document converter, CV maker, AI assistant, 116 languages">
    <meta name="author" content="PDF Lover Enterprise">
    
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Chart.js for Dashboard -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>
    
    <!-- Google Translate API -->
    <script src="https://translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
    
    <!-- PDF Libraries -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf-lib/1.17.1/pdf-lib.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.9.179/pdf.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/tesseract.js@4.0.2/dist/tesseract.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mammoth/1.4.14/mammoth.browser.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/PptxGenJS/3.10.0/pptxgen.bundle.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/fabric.js/5.3.0/fabric.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js"></script>
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --primary-light: #3b82f6;
            --secondary: #7c3aed;
            --success: #10b981;
            --warning: #f59e0b;
            --danger: #ef4444;
            --dark: #0f172a;
            --light: #f8fafc;
            --gray-50: #f9fafb;
            --gray-100: #f3f4f6;
            --gray-200: #e5e7eb;
            --gray-300: #d1d5db;
            --gray-400: #9ca3af;
            --gray-500: #6b7280;
            --gray-600: #4b5563;
            --gray-700: #374151;
            --gray-800: #1f2937;
            --gray-900: #111827;
            
            --sidebar-width: 280px;
            --header-height: 70px;
            --card-shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .dark-mode {
            --primary: #3b82f6;
            --primary-dark: #2563eb;
            --primary-light: #60a5fa;
            --dark: #f8fafc;
            --light: #0f172a;
            --gray-50: #1f2937;
            --gray-100: #374151;
            --gray-200: #4b5563;
            --gray-300: #6b7280;
            --gray-400: #9ca3af;
            --gray-500: #d1d5db;
            --gray-600: #e5e7eb;
            --gray-700: #f3f4f6;
            --gray-800: #f9fafb;
            --gray-900: #ffffff;
            background: #0f172a;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--gray-50);
            color: var(--gray-900);
            transition: var(--transition);
            overflow-x: hidden;
        }

        /* App Container */
        .app-container {
            display: flex;
            min-height: 100vh;
        }

        /* Sidebar */
        .sidebar {
            width: var(--sidebar-width);
            background: white;
            box-shadow: 4px 0 20px rgba(0, 0, 0, 0.02);
            position: fixed;
            height: 100vh;
            overflow-y: auto;
            transition: var(--transition);
            z-index: 50;
        }

        .dark-mode .sidebar {
            background: var(--gray-800);
            border-right: 1px solid var(--gray-700);
        }

        .sidebar-header {
            padding: 1.5rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            border-bottom: 1px solid var(--gray-200);
        }

        .sidebar-header .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .sidebar-header .logo i {
            font-size: 2rem;
        }

        .sidebar-menu {
            padding: 1.5rem 0;
        }

        .menu-item {
            padding: 0.8rem 1.5rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            color: var(--gray-600);
            text-decoration: none;
            transition: var(--transition);
            margin: 0.2rem 0;
            border-left: 3px solid transparent;
        }

        .menu-item:hover {
            background: var(--gray-100);
            color: var(--primary);
            border-left-color: var(--primary);
        }

        .menu-item.active {
            background: var(--primary);
            color: white;
            border-left-color: white;
        }

        .menu-item i {
            width: 24px;
            font-size: 1.2rem;
        }

        .menu-category {
            padding: 1rem 1.5rem 0.5rem;
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            color: var(--gray-400);
            font-weight: 600;
        }

        /* Main Content */
        .main-content {
            flex: 1;
            margin-left: var(--sidebar-width);
            min-height: 100vh;
            transition: var(--transition);
        }

        /* Header */
        .header {
            height: var(--header-height);
            background: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.02);
            position: sticky;
            top: 0;
            z-index: 40;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 2rem;
        }

        .dark-mode .header {
            background: var(--gray-800);
            border-bottom: 1px solid var(--gray-700);
        }

        .header-left {
            display: flex;
            align-items: center;
            gap: 2rem;
        }

        .header-left h2 {
            font-size: 1.2rem;
            font-weight: 600;
            color: var(--gray-800);
        }

        .dark-mode .header-left h2 {
            color: white;
        }

        .header-right {
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }

        .language-selector {
            position: relative;
        }

        .language-btn {
            background: var(--gray-100);
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 8px;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            cursor: pointer;
            font-size: 0.9rem;
            color: var(--gray-700);
            transition: var(--transition);
        }

        .language-btn:hover {
            background: var(--gray-200);
        }

        .language-dropdown {
            position: absolute;
            top: 120%;
            right: 0;
            width: 300px;
            max-height: 400px;
            overflow-y: auto;
            background: white;
            border-radius: 12px;
            box-shadow: var(--card-shadow);
            display: none;
            z-index: 100;
            padding: 0.5rem;
        }

        .dark-mode .language-dropdown {
            background: var(--gray-800);
            border: 1px solid var(--gray-700);
        }

        .language-selector:hover .language-dropdown {
            display: block;
        }

        .language-item {
            padding: 0.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            cursor: pointer;
            border-radius: 6px;
            transition: var(--transition);
        }

        .language-item:hover {
            background: var(--gray-100);
        }

        .dark-mode .language-item:hover {
            background: var(--gray-700);
        }

        .theme-toggle {
            width: 40px;
            height: 40px;
            border-radius: 8px;
            background: var(--gray-100);
            border: none;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gray-700);
            font-size: 1.2rem;
            transition: var(--transition);
        }

        .theme-toggle:hover {
            background: var(--gray-200);
        }

        .user-profile {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 0.5rem 1rem;
            background: var(--gray-100);
            border-radius: 8px;
            cursor: pointer;
        }

        .user-profile img {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            object-fit: cover;
        }

        /* Dashboard */
        .dashboard {
            padding: 2rem;
        }

        /* Stats Grid */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .stat-card {
            background: white;
            border-radius: 16px;
            padding: 1.5rem;
            box-shadow: var(--card-shadow);
            display: flex;
            align-items: center;
            justify-content: space-between;
            transition: var(--transition);
            border: 1px solid var(--gray-200);
        }

        .dark-mode .stat-card {
            background: var(--gray-800);
            border-color: var(--gray-700);
        }

        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
        }

        .stat-info h3 {
            font-size: 0.9rem;
            color: var(--gray-500);
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .stat-info .stat-number {
            font-size: 2rem;
            font-weight: 700;
            color: var(--gray-900);
            margin-bottom: 0.2rem;
        }

        .dark-mode .stat-info .stat-number {
            color: white;
        }

        .stat-info .stat-trend {
            font-size: 0.8rem;
            color: var(--success);
        }

        .stat-icon {
            width: 60px;
            height: 60px;
            border-radius: 12px;
            background: var(--primary-light);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.8rem;
            opacity: 0.9;
        }

        /* Charts Row */
        .charts-row {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .chart-card {
            background: white;
            border-radius: 16px;
            padding: 1.5rem;
            box-shadow: var(--card-shadow);
            border: 1px solid var(--gray-200);
        }

        .dark-mode .chart-card {
            background: var(--gray-800);
            border-color: var(--gray-700);
        }

        .chart-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 1.5rem;
        }

        .chart-header h3 {
            font-size: 1rem;
            font-weight: 600;
            color: var(--gray-700);
        }

        .chart-header select {
            padding: 0.3rem 1rem;
            border-radius: 6px;
            border: 1px solid var(--gray-200);
            background: white;
            font-size: 0.9rem;
        }

        .dark-mode .chart-header select {
            background: var(--gray-700);
            color: white;
            border-color: var(--gray-600);
        }

        .chart-container {
            height: 300px;
            position: relative;
        }

        /* Tools Section */
        .tools-section {
            background: white;
            border-radius: 16px;
            padding: 1.5rem;
            margin-bottom: 2rem;
            border: 1px solid var(--gray-200);
        }

        .dark-mode .tools-section {
            background: var(--gray-800);
            border-color: var(--gray-700);
        }

        .section-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 1.5rem;
        }

        .section-header h3 {
            font-size: 1.2rem;
            font-weight: 600;
        }

        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 1rem;
        }

        .tool-item {
            padding: 1.2rem;
            background: var(--gray-50);
            border-radius: 12px;
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
            border: 2px solid transparent;
            position: relative;
        }

        .dark-mode .tool-item {
            background: var(--gray-900);
        }

        .tool-item:hover {
            border-color: var(--primary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .tool-item i {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .tool-item h4 {
            font-size: 0.95rem;
            font-weight: 600;
            margin-bottom: 0.3rem;
        }

        .tool-item p {
            font-size: 0.8rem;
            color: var(--gray-500);
        }

        .new-badge {
            position: absolute;
            top: 5px;
            right: 5px;
            background: var(--danger);
            color: white;
            font-size: 0.7rem;
            padding: 0.2rem 0.4rem;
            border-radius: 4px;
        }

        /* Recent Activity */
        .activity-section {
            background: white;
            border-radius: 16px;
            padding: 1.5rem;
            border: 1px solid var(--gray-200);
        }

        .dark-mode .activity-section {
            background: var(--gray-800);
            border-color: var(--gray-700);
        }

        .activity-list {
            margin-top: 1rem;
        }

        .activity-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem 0;
            border-bottom: 1px solid var(--gray-200);
        }

        .activity-item:last-child {
            border-bottom: none;
        }

        .activity-icon {
            width: 40px;
            height: 40px;
            border-radius: 10px;
            background: var(--primary-light);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
        }

        .activity-details {
            flex: 1;
        }

        .activity-details p {
            font-weight: 500;
            margin-bottom: 0.2rem;
        }

        .activity-time {
            font-size: 0.8rem;
            color: var(--gray-500);
        }

        .activity-status {
            padding: 0.2rem 1rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 500;
        }

        .status-success {
            background: #d1fae5;
            color: #065f46;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(5px);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            background: white;
            width: 90%;
            max-width: 500px;
            padding: 2rem;
            border-radius: 24px;
            position: relative;
            animation: slideUp 0.3s ease;
        }

        .dark-mode .modal-content {
            background: var(--gray-800);
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .modal-close {
            position: absolute;
            top: 1rem;
            right: 1rem;
            cursor: pointer;
            font-size: 1.2rem;
            color: var(--gray-400);
            transition: var(--transition);
        }

        .modal-close:hover {
            color: var(--danger);
            transform: rotate(90deg);
        }

        .modal h2 {
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .modal input,
        .modal select,
        .modal textarea {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 1rem;
            border: 2px solid var(--gray-200);
            border-radius: 10px;
            font-size: 0.95rem;
            transition: var(--transition);
        }

        .modal input:focus,
        .modal select:focus,
        .modal textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        .modal button {
            width: 100%;
            padding: 1rem;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
        }

        .modal button:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
        }

        .progress-bar {
            width: 100%;
            height: 6px;
            background: var(--gray-200);
            border-radius: 10px;
            margin: 1rem 0;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: var(--primary);
            width: 0%;
            transition: width 0.3s ease;
        }

        /* AI Assistant */
        #ai-assistant {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 60px;
            height: 60px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(37, 99, 235, 0.4);
            transition: var(--transition);
            z-index: 100;
            animation: pulse 2s infinite;
        }

        #ai-assistant:hover {
            transform: scale(1.1);
        }

        #ai-chat {
            display: none;
            position: fixed;
            bottom: 5rem;
            right: 2rem;
            width: 350px;
            height: 500px;
            background: white;
            border-radius: 20px;
            box-shadow: var(--card-shadow);
            z-index: 100;
            overflow: hidden;
            animation: slideIn 0.3s ease;
        }

        .dark-mode #ai-chat {
            background: var(--gray-800);
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .chat-header {
            background: var(--primary);
            color: white;
            padding: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .chat-header i {
            font-size: 1.5rem;
        }

        .chat-messages {
            height: 350px;
            overflow-y: auto;
            padding: 1rem;
        }

        .message {
            margin-bottom: 1rem;
            max-width: 80%;
        }

        .message.user {
            margin-left: auto;
        }

        .message-content {
            padding: 0.8rem;
            border-radius: 15px;
            font-size: 0.9rem;
        }

        .message.bot .message-content {
            background: var(--gray-100);
            border-radius: 15px 15px 15px 0;
        }

        .message.user .message-content {
            background: var(--primary);
            color: white;
            border-radius: 15px 15px 0 15px;
        }

        .chat-input {
            padding: 1rem;
            border-top: 1px solid var(--gray-200);
            display: flex;
            gap: 0.5rem;
        }

        .chat-input input {
            flex: 1;
            padding: 0.6rem;
            border: 2px solid var(--gray-200);
            border-radius: 25px;
            font-size: 0.9rem;
        }

        .chat-input button {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--primary);
            color: white;
            border: none;
            cursor: pointer;
            transition: var(--transition);
        }

        .chat-input button:hover {
            transform: scale(1.1);
        }

        /* Footer */
        .footer {
            background: white;
            padding: 2rem;
            border-radius: 16px;
            margin-top: 2rem;
            border: 1px solid var(--gray-200);
        }

        .dark-mode .footer {
            background: var(--gray-800);
            border-color: var(--gray-700);
        }

        .footer-content {
            text-align: center;
            color: var(--gray-500);
            font-size: 0.9rem;
        }

        .footer-content i {
            color: var(--danger);
        }

        /* Responsive */
        @media (max-width: 1024px) {
            .sidebar {
                transform: translateX(-100%);
            }
            
            .sidebar.active {
                transform: translateX(0);
            }
            
            .main-content {
                margin-left: 0;
            }
            
            .charts-row {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .header {
                padding: 0 1rem;
            }
            
            .header-left h2 {
                display: none;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .tools-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
            
            #ai-chat {
                width: 300px;
                right: 1rem;
            }
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>
    <div class="app-container">
        <!-- Sidebar -->
        <aside class="sidebar" id="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <i class="fas fa-file-pdf"></i>
                    <span>PDF Lover</span>
                </div>
            </div>
            
            <div class="sidebar-menu">
                <div class="menu-category">Main</div>
                <a href="#" class="menu-item active">
                    <i class="fas fa-chart-pie"></i>
                    <span>Dashboard</span>
                </a>
                <a href="#" class="menu-item">
                    <i class="fas fa-file-pdf"></i>
                    <span>PDF Tools</span>
                </a>
                <a href="#" class="menu-item">
                    <i class="fas fa-id-card"></i>
                    <span>CV Maker</span>
                </a>
                <a href="#" class="menu-item">
                    <i class="fas fa-diagram-project"></i>
                    <span>Project Builder</span>
                </a>
                
                <div class="menu-category">Analytics</div>
                <a href="#" class="menu-item">
                    <i class="fas fa-chart-line"></i>
                    <span>Usage Stats</span>
                </a>
                <a href="#" class="menu-item">
                    <i class="fas fa-users"></i>
                    <span>Team Activity</span>
                </a>
                
                <div class="menu-category">Settings</div>
                <a href="#" class="menu-item">
                    <i class="fas fa-cog"></i>
                    <span>Preferences</span>
                </a>
                <a href="#" class="menu-item">
                    <i class="fas fa-shield-alt"></i>
                    <span>Security</span>
                </a>
                <a href="#" class="menu-item">
                    <i class="fas fa-headset"></i>
                    <span>Support</span>
                </a>
            </div>
        </aside>

        <!-- Main Content -->
        <main class="main-content">
            <!-- Header -->
            <header class="header">
                <div class="header-left">
                    <i class="fas fa-bars" style="font-size: 1.5rem; cursor: pointer;" onclick="toggleSidebar()"></i>
                    <h2>Dashboard Overview</h2>
                </div>
                
                <div class="header-right">
                    <div class="language-selector">
                        <button class="language-btn">
                            <i class="fas fa-globe"></i>
                            <span id="current-lang">116 Languages</span>
                            <i class="fas fa-chevron-down"></i>
                        </button>
                        <div class="language-dropdown" id="languageDropdown"></div>
                    </div>
                    
                    <button class="theme-toggle" onclick="toggleTheme()">
                        <i class="fas fa-moon"></i>
                    </button>
                    
                    <div class="user-profile">
                        <img src="https://ui-avatars.com/api/?name=PDF+Lover&background=2563eb&color=fff&size=32" alt="User">
                        <span>Admin</span>
                    </div>
                </div>
            </header>

            <!-- Dashboard Content -->
            <div class="dashboard">
                <!-- Stats Cards -->
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-info">
                            <h3>Total Conversions</h3>
                            <div class="stat-number">1,24,563</div>
                            <div class="stat-trend">
                                <i class="fas fa-arrow-up"></i> +12.5% this week
                            </div>
                        </div>
                        <div class="stat-icon">
                            <i class="fas fa-file-pdf"></i>
                        </div>
                    </div>
                    
                    <div class="stat-card">
                        <div class="stat-info">
                            <h3>Active Users</h3>
                            <div class="stat-number">45,892</div>
                            <div class="stat-trend">
                                <i class="fas fa-arrow-up"></i> +8.2% this week
                            </div>
                        </div>
                        <div class="stat-icon">
                            <i class="fas fa-users"></i>
                        </div>
                    </div>
                    
                    <div class="stat-card">
                        <div class="stat-info">
                            <h3>Languages</h3>
                            <div class="stat-number">116</div>
                            <div class="stat-trend">
                                <i class="fas fa-globe"></i> Global coverage
                            </div>
                        </div>
                        <div class="stat-icon">
                            <i class="fas fa-language"></i>
                        </div>
                    </div>
                    
                    <div class="stat-card">
                        <div class="stat-info">
                            <h3>Response Time</h3>
                            <div class="stat-number">0.3s</div>
                            <div class="stat-trend">
                                <i class="fas fa-bolt"></i> Lightning fast
                            </div>
                        </div>
                        <div class="stat-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                    </div>
                </div>

                <!-- Charts Row -->
                <div class="charts-row">
                    <div class="chart-card">
                        <div class="chart-header">
                            <h3>Usage Analytics (Last 7 Days)</h3>
                            <select>
                                <option>Weekly</option>
                                <option>Monthly</option>
                                <option>Yearly</option>
                            </select>
                        </div>
                        <div class="chart-container">
                            <canvas id="usageChart"></canvas>
                        </div>
                    </div>
                    
                    <div class="chart-card">
                        <div class="chart-header">
                            <h3>Language Distribution</h3>
                            <select>
                                <option>Top 10</option>
                                <option>All</option>
                            </select>
                        </div>
                        <div class="chart-container">
                            <canvas id="languageChart"></canvas>
                        </div>
                    </div>
                </div>

                <!-- Tools Section -->
                <div class="tools-section">
                    <div class="section-header">
                        <h3><i class="fas fa-bolt"></i> Quick Access Tools</h3>
                        <a href="#" style="color: var(--primary);">View All <i class="fas fa-arrow-right"></i></a>
                    </div>
                    
                    <div class="tools-grid" id="toolsGrid"></div>
                </div>

                <!-- Recent Activity -->
                <div class="activity-section">
                    <div class="section-header">
                        <h3><i class="fas fa-history"></i> Recent Activity</h3>
                        <a href="#" style="color: var(--primary);">View All</a>
                    </div>
                    
                    <div class="activity-list" id="activityList"></div>
                </div>

                <!-- Footer -->
                <div class="footer">
                    <div class="footer-content">
                        <p><i class="fas fa-heart"></i> PDF Lover Ultimate - World's Most Multilingual PDF Tool (116 Languages)</p>
                        <p style="margin-top: 0.5rem;">© 2026 | 100% Client-Side | Privacy First</p>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <!-- Hidden Google Translate -->
    <div id="google_translate_element" style="display: none;"></div>

    <!-- Modal -->
    <div class="modal" id="toolModal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal()">&times;</span>
            <h2 id="modalTitle">Tool Name</h2>
            <input type="file" id="fileUpload" multiple>
            <select id="toolOptions">
                <option>Basic Settings</option>
                <option>Advanced Settings</option>
                <option>Batch Processing</option>
            </select>
            <textarea id="toolInput" placeholder="Additional options..." rows="3"></textarea>
            <button onclick="processTool()">
                <i class="fas fa-play"></i> Process Now
            </button>
            <div class="progress-bar">
                <div class="progress-fill" id="progressFill"></div>
            </div>
            <div id="progress"></div>
            <a id="downloadLink" href="#" download style="display:none; text-align: center; margin-top: 1rem; color: var(--primary);">
                <i class="fas fa-download"></i> Download Result
            </a>
        </div>
    </div>

    <!-- AI Assistant -->
    <div id="ai-assistant" onclick="toggleAI()">
        <i class="fas fa-robot"></i>
    </div>
    
    <div id="ai-chat">
        <div class="chat-header">
            <i class="fas fa-robot"></i>
            <span>AI Assistant (116 Languages)</span>
        </div>
        <div class="chat-messages" id="chatMessages">
            <div class="message bot">
                <div class="message-content">
                    <i class="fas fa-smile"></i> Hello! I can help you in 116 languages. How can I assist you today?
                </div>
            </div>
        </div>
        <div class="chat-input">
            <input type="text" id="chatInput" placeholder="Type your question...">
            <button onclick="sendMessage()"><i class="fas fa-paper-plane"></i></button>
        </div>
    </div>

    <script>
        // Languages Data (116)
        const languages = [
            { code: 'mr', name: 'मराठी', flag: '🇮🇳' },
            { code: 'hi', name: 'हिंदी', flag: '🇮🇳' },
            { code: 'bn', name: 'বাংলা', flag: '🇧🇩' },
            { code: 'te', name: 'తెలుగు', flag: '🇮🇳' },
            { code: 'ta', name: 'தமிழ்', flag: '🇮🇳' },
            { code: 'gu', name: 'ગુજરાતી', flag: '🇮🇳' },
            { code: 'kn', name: 'ಕನ್ನಡ', flag: '🇮🇳' },
            { code: 'ml', name: 'മലയാളം', flag: '🇮🇳' },
            { code: 'or', name: 'ଓଡ଼ିଆ', flag: '🇮🇳' },
            { code: 'pa', name: 'ਪੰਜਾਬੀ', flag: '🇮🇳' },
            { code: 'as', name: 'অসমীয়া', flag: '🇮🇳' },
            { code: 'ur', name: 'اردو', flag: '🇵🇰' },
            { code: 'sa', name: 'संस्कृत', flag: '🇮🇳' },
            { code: 'sd', name: 'سنڌي', flag: '🇵🇰' },
            { code: 'kok', name: 'कोंकणी', flag: '🇮🇳' },
            { code: 'mai', name: 'मैथिली', flag: '🇮🇳' },
            { code: 'doi', name: 'डोगरी', flag: '🇮🇳' },
            { code: 'ks', name: 'कॉशुर', flag: '🇮🇳' },
            { code: 'ne', name: 'नेपाली', flag: '🇳🇵' },
            { code: 'brx', name: 'बर', flag: '🇮🇳' },
            { code: 'sat', name: 'ᱥᱟᱱᱛᱟᱲᱤ', flag: '🇮🇳' },
            { code: 'mni', name: 'মৈতৈ', flag: '🇮🇳' },
            { code: 'en', name: 'English', flag: '🇬🇧' },
            { code: 'es', name: 'Español', flag: '🇪🇸' },
            { code: 'fr', name: 'Français', flag: '🇫🇷' },
            { code: 'de', name: 'Deutsch', flag: '🇩🇪' },
            { code: 'it', name: 'Italiano', flag: '🇮🇹' },
            { code: 'pt', name: 'Português', flag: '🇵🇹' },
            { code: 'ru', name: 'Русский', flag: '🇷🇺' },
            { code: 'zh', name: '中文', flag: '🇨🇳' },
            { code: 'ja', name: '日本語', flag: '🇯🇵' },
            { code: 'ko', name: '한국어', flag: '🇰🇷' },
            { code: 'ar', name: 'العربية', flag: '🇸🇦' },
            { code: 'tr', name: 'Türkçe', flag: '🇹🇷' },
            { code: 'nl', name: 'Nederlands', flag: '🇳🇱' },
            { code: 'sv', name: 'Svenska', flag: '🇸🇪' },
            { code: 'da', name: 'Dansk', flag: '🇩🇰' },
            { code: 'fi', name: 'Suomi', flag: '🇫🇮' },
            { code: 'no', name: 'Norsk', flag: '🇳🇴' },
            { code: 'pl', name: 'Polski', flag: '🇵🇱' },
            { code: 'cs', name: 'Čeština', flag: '🇨🇿' },
            { code: 'sk', name: 'Slovenčina', flag: '🇸🇰' },
            { code: 'hu', name: 'Magyar', flag: '🇭🇺' },
            { code: 'ro', name: 'Română', flag: '🇷🇴' },
            { code: 'bg', name: 'Български', flag: '🇧🇬' },
            { code: 'sr', name: 'Српски', flag: '🇷🇸' },
            { code: 'hr', name: 'Hrvatski', flag: '🇭🇷' },
            { code: 'bs', name: 'Bosanski', flag: '🇧🇦' },
            { code: 'sq', name: 'Shqip', flag: '🇦🇱' },
            { code: 'el', name: 'Ελληνικά', flag: '🇬🇷' },
            { code: 'uk', name: 'Українська', flag: '🇺🇦' },
            { code: 'be', name: 'Беларуская', flag: '🇧🇾' },
            { code: 'lt', name: 'Lietuvių', flag: '🇱🇹' },
            { code: 'lv', name: 'Latviešu', flag: '🇱🇻' },
            { code: 'et', name: 'Eesti', flag: '🇪🇪' },
            { code: 'is', name: 'Íslenska', flag: '🇮🇸' },
            { code: 'ga', name: 'Gaeilge', flag: '🇮🇪' },
            { code: 'gd', name: 'Gàidhlig', flag: '🏴󠁧󠁢󠁳󠁣󠁴󠁿' },
            { code: 'cy', name: 'Cymraeg', flag: '🏴󠁧󠁢󠁷󠁬󠁳󠁿' },
            { code: 'kw', name: 'Kernewek', flag: '🏴󠁧󠁢󠁥󠁮󠁧󠁿' },
            { code: 'th', name: 'ไทย', flag: '🇹🇭' },
            { code: 'vi', name: 'Tiếng Việt', flag: '🇻🇳' },
            { code: 'id', name: 'Bahasa Indonesia', flag: '🇮🇩' },
            { code: 'ms', name: 'Bahasa Melayu', flag: '🇲🇾' },
            { code: 'fil', name: 'Filipino', flag: '🇵🇭' },
            { code: 'km', name: 'ភាសាខ្មែរ', flag: '🇰🇭' },
            { code: 'lo', name: 'ພາສາລາວ', flag: '🇱🇦' },
            { code: 'my', name: 'မြန်မာစာ', flag: '🇲🇲' },
            { code: 'si', name: 'සිංහල', flag: '🇱🇰' },
            { code: 'bo', name: 'བོད་སྐད', flag: '🇨🇳' },
            { code: 'mn', name: 'Монгол', flag: '🇲🇳' },
            { code: 'uz', name: 'Oʻzbek', flag: '🇺🇿' },
            { code: 'kk', name: 'Қазақ', flag: '🇰🇿' },
            { code: 'tg', name: 'Тоҷикӣ', flag: '🇹🇯' },
            { code: 'ky', name: 'Кыргыз', flag: '🇰🇬' },
            { code: 'tk', name: 'Türkmen', flag: '🇹🇲' },
            { code: 'az', name: 'Azərbaycan', flag: '🇦🇿' },
            { code: 'ka', name: 'ქართული', flag: '🇬🇪' },
            { code: 'hy', name: 'Հայերեն', flag: '🇦🇲' },
            { code: 'he', name: 'עברית', flag: '🇮🇱' },
            { code: 'ps', name: 'پښتو', flag: '🇦🇫' },
            { code: 'prs', name: 'دری', flag: '🇦🇫' },
            { code: 'ku', name: 'Kurdî', flag: '🇹🇷' },
            { code: 'ckb', name: 'سۆرانی', flag: '🇮🇶' },
            { code: 'sw', name: 'Kiswahili', flag: '🇰🇪' },
            { code: 'yo', name: 'Yorùbá', flag: '🇳🇬' },
            { code: 'ig', name: 'Igbo', flag: '🇳🇬' },
            { code: 'ha', name: 'Hausa', flag: '🇳🇬' },
            { code: 'am', name: 'አማርኛ', flag: '🇪🇹' },
            { code: 'so', name: 'Soomaali', flag: '🇸🇴' },
            { code: 'zu', name: 'isiZulu', flag: '🇿🇦' },
            { code: 'xh', name: 'isiXhosa', flag: '🇿🇦' },
            { code: 'sn', name: 'chiShona', flag: '🇿🇼' },
            { code: 'ny', name: 'Chichewa', flag: '🇲🇼' },
            { code: 'mg', name: 'Malagasy', flag: '🇲🇬' },
            { code: 'st', name: 'Sesotho', flag: '🇱🇸' },
            { code: 'tn', name: 'Setswana', flag: '🇧🇼' },
            { code: 'af', name: 'Afrikaans', flag: '🇿🇦' },
            { code: 'ti', name: 'ትግርኛ', flag: '🇪🇷' },
            { code: 'qu', name: 'Runa Simi', flag: '🇵🇪' },
            { code: 'ay', name: 'Aymar', flag: '🇧🇴' },
            { code: 'gn', name: 'Avañeẽ', flag: '🇵🇾' },
            { code: 'nah', name: 'Nāhuatl', flag: '🇲🇽' },
            { code: 'yua', name: 'Maaya tʼaan', flag: '🇲🇽' },
            { code: 'haw', name: 'Ōlelo Hawaiʻi', flag: '🇺🇸' },
            { code: 'mi', name: 'Te Reo Māori', flag: '🇳🇿' },
            { code: 'sm', name: 'Gagana Sāmoa', flag: '🇼🇸' },
            { code: 'ty', name: 'Reo Tahiti', flag: '🇵🇫' },
            { code: 'fj', name: 'Vosa Vakaviti', flag: '🇫🇯' },
            { code: 'la', name: 'Latina', flag: '🇻🇦' },
            { code: 'grc', name: 'Ἑλληνική', flag: '🇬🇷' },
            { code: 'ae', name: '𐬎𐬞𐬀𐬯𐬙𐬀', flag: '🇮🇷' },
            { code: 'egy', name: '𓂋𓏤𓈖𓆎𓅓', flag: '🇪🇬' },
            { code: 'eo', name: 'Esperanto', flag: '🌍' }
        ];

        // Tools Data
        const tools = [
            { name: 'Merge PDF', icon: 'fa-object-group', desc: 'Combine PDFs', color: '#2563eb' },
            { name: 'Split PDF', icon: 'fa-cut', desc: 'Extract pages', color: '#7c3aed' },
            { name: 'Compress', icon: 'fa-compress', desc: 'Reduce size', color: '#10b981' },
            { name: 'PDF to Word', icon: 'fa-file-word', desc: 'Convert to DOCX', color: '#2563eb' },
            { name: 'PDF to Excel', icon: 'fa-file-excel', desc: 'Extract tables', color: '#10b981' },
            { name: 'PDF to PPT', icon: 'fa-file-powerpoint', desc: 'To presentation', color: '#f59e0b' },
            { name: 'JPG to PDF', icon: 'fa-file-image', desc: 'Images to PDF', color: '#ef4444' },
            { name: 'CV Maker', icon: 'fa-id-card', desc: 'Create resume', color: '#7c3aed', new: true },
            { name: 'Project Maker', icon: 'fa-diagram-project', desc: 'Build project', color: '#2563eb', new: true },
            { name: 'Protect PDF', icon: 'fa-lock', desc: 'Add password', color: '#f59e0b' },
            { name: 'Unlock PDF', icon: 'fa-unlock', desc: 'Remove password', color: '#10b981' },
            { name: 'Rotate PDF', icon: 'fa-rotate-right', desc: 'Change orientation', color: '#7c3aed' },
            { name: 'Watermark', icon: 'fa-droplet', desc: 'Add watermark', color: '#2563eb' },
            { name: 'Sign PDF', icon: 'fa-pen', desc: 'Add signature', color: '#ef4444' },
            { name: 'OCR PDF', icon: 'fa-eye', desc: 'Text recognition', color: '#7c3aed' },
            { name: 'HTML to PDF', icon: 'fa-code', desc: 'Webpage to PDF', color: '#10b981' }
        ];

        // Activity Data
        const activities = [
            { user: 'John Doe', action: 'Merged 5 PDFs', time: '2 minutes ago', status: 'success' },
            { user: 'Maria Garcia', action: 'Created CV', time: '15 minutes ago', status: 'success' },
            { user: 'Raj Kumar', action: 'Converted PDF to Word', time: '1 hour ago', status: 'success' },
            { user: 'Li Wei', action: 'Compressed PDF', time: '3 hours ago', status: 'success' },
            { user: 'Sarah Johnson', action: 'Added watermark', time: '5 hours ago', status: 'success' },
            { user: 'Ahmed Hassan', action: 'Split PDF into 3 files', time: '1 day ago', status: 'success' }
        ];

        // Initialize Languages
        function initLanguages() {
            const dropdown = document.getElementById('languageDropdown');
            languages.forEach(lang => {
                const item = document.createElement('div');
                item.className = 'language-item';
                item.onclick = () => changeLanguage(lang.code);
                item.innerHTML = `${lang.flag} ${lang.name}`;
                dropdown.appendChild(item);
            });
        }

        // Initialize Tools Grid
        function initTools() {
            const grid = document.getElementById('toolsGrid');
            tools.forEach(tool => {
                const item = document.createElement('div');
                item.className = 'tool-item';
                item.onclick = () => openModal(tool.name);
                item.innerHTML = `
                    <i class="fas ${tool.icon}" style="color: ${tool.color};"></i>
                    <h4>${tool.name}</h4>
                    <p>${tool.desc}</p>
                    ${tool.new ? '<span class="new-badge">NEW</span>' : ''}
                `;
                grid.appendChild(item);
            });
        }

        // Initialize Activity List
        function initActivities() {
            const list = document.getElementById('activityList');
            activities.forEach(activity => {
                const item = document.createElement('div');
                item.className = 'activity-item';
                item.innerHTML = `
                    <div class="activity-icon">
                        <i class="fas fa-file-pdf"></i>
                    </div>
                    <div class="activity-details">
                        <p>${activity.user} - ${activity.action}</p>
                        <span class="activity-time">${activity.time}</span>
                    </div>
                    <span class="activity-status status-success">Completed</span>
                `;
                list.appendChild(item);
            });
        }

        // Initialize Charts
        function initCharts() {
            // Usage Chart
            const usageCtx = document.getElementById('usageChart').getContext('2d');
            new Chart(usageCtx, {
                type: 'line',
                data: {
                    labels: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
                    datasets: [{
                        label: 'PDF Conversions',
                        data: [12500, 19200, 18300, 24500, 28900, 32400, 29800],
                        borderColor: '#2563eb',
                        backgroundColor: 'rgba(37, 99, 235, 0.1)',
                        tension: 0.4,
                        fill: true
                    }, {
                        label: 'CV Creations',
                        data: [5200, 6800, 7200, 8900, 10200, 11500, 9800],
                        borderColor: '#7c3aed',
                        backgroundColor: 'rgba(124, 58, 237, 0.1)',
                        tension: 0.4,
                        fill: true
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: true,
                            position: 'bottom'
                        }
                    }
                }
            });

            // Language Chart
            const langCtx = document.getElementById('languageChart').getContext('2d');
            new Chart(langCtx, {
                type: 'doughnut',
                data: {
                    labels: ['Marathi', 'Hindi', 'English', 'Spanish', 'Bengali', 'Others'],
                    datasets: [{
                        data: [25, 20, 15, 10, 8, 22],
                        backgroundColor: [
                            '#2563eb',
                            '#7c3aed',
                            '#10b981',
                            '#f59e0b',
                            '#ef4444',
                            '#6b7280'
                        ]
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            position: 'bottom'
                        }
                    }
                }
            });
        }

        // Google Translate
        function googleTranslateElementInit() {
            new google.translate.TranslateElement({
                pageLanguage: 'en',
                includedLanguages: languages.map(l => l.code).join(','),
                layout: google.translate.TranslateElement.InlineLayout.SIMPLE,
                autoDisplay: false
            }, 'google_translate_element');
        }

        // Change Language
        function changeLanguage(langCode) {
            const lang = languages.find(l => l.code === langCode);
            if(lang) {
                document.getElementById('current-lang').innerHTML = `${lang.flag} ${lang.name}`;
                
                const select = document.querySelector('select.goog-te-combo');
                if(select) {
                    select.value = langCode;
                    select.dispatchEvent(new Event('change'));
                }
            }
        }

        // Theme Toggle
        function toggleTheme() {
            document.body.classList.toggle('dark-mode');
            const btn = document.querySelector('.theme-toggle i');
            if(document.body.classList.contains('dark-mode')) {
                btn.className = 'fas fa-sun';
            } else {
                btn.className = 'fas fa-moon';
            }
        }

        // Sidebar Toggle
        function toggleSidebar() {
            document.getElementById('sidebar').classList.toggle('active');
        }

        // Modal Functions
        function openModal(toolName) {
            document.getElementById('toolModal').style.display = 'flex';
            document.getElementById('modalTitle').innerText = toolName;
        }

        function closeModal() {
            document.getElementById('toolModal').style.display = 'none';
        }

        // Process Tool
        function processTool() {
            const progressFill = document.getElementById('progressFill');
            const progress = document.getElementById('progress');
            let width = 0;
            
            progress.innerHTML = 'Processing...';
            
            const interval = setInterval(() => {
                if(width >= 100) {
                    clearInterval(interval);
                    progress.innerHTML = '✅ Process Complete!';
                    document.getElementById('downloadLink').style.display = 'block';
                } else {
                    width += 10;
                    progressFill.style.width = width + '%';
                    progress.innerHTML = `Processing... ${width}%`;
                }
            }, 200);
        }

        // AI Chat
        function toggleAI() {
            const chat = document.getElementById('ai-chat');
            chat.style.display = chat.style.display === 'none' ? 'block' : 'none';
        }

        function sendMessage() {
            const input = document.getElementById('chatInput');
            const msg = input.value.trim();
            if(!msg) return;
            
            const messages = document.getElementById('chatMessages');
            
            messages.innerHTML += `
                <div class="message user">
                    <div class="message-content">${msg}</div>
                </div>
            `;
            
            input.value = '';
            
            setTimeout(() => {
                messages.innerHTML += `
                    <div class="message bot">
                        <div class="message-content">
                            <i class="fas fa-robot"></i> I'm processing your request in your selected language. Please wait...
                        </div>
                    </div>
                `;
                messages.scrollTop = messages.scrollHeight;
            }, 1000);
        }

        // Initialize on Load
        document.addEventListener('DOMContentLoaded', function() {
            initLanguages();
            initTools();
            initActivities();
            initCharts();
            
            // Close modal on outside click
            window.onclick = function(e) {
                const modal = document.getElementById('toolModal');
                if(e.target === modal) closeModal();
            };
            
            // Enter key in chat
            document.getElementById('chatInput').addEventListener('keypress', function(e) {
                if(e.key === 'Enter') sendMessage();
            });
        });
    </script>
</body>
</html>