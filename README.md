<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Prezzo - Stop Undercharging. Price Every Project Profitably.</title>
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet" />
    
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
    
    <style>
        /* ============================================
           CSS VARIABLES & RESET
           ============================================ */
        :root {
            --background: #ffffff;
            --foreground: #0f172a;
            --card: #ffffff;
            --card-foreground: #0f172a;
            --popover: #ffffff;
            --popover-foreground: #0f172a;
            --primary: #2563EB;
            --primary-foreground: #ffffff;
            --primary-50: #eff6ff;
            --primary-100: #dbeafe;
            --primary-200: #bfdbfe;
            --primary-300: #93c5fd;
            --primary-400: #60a5fa;
            --primary-500: #3b82f6;
            --primary-600: #2563eb;
            --primary-700: #1d4ed8;
            --primary-800: #1e40af;
            --primary-900: #1e3a8a;
            --secondary: #f1f5f9;
            --secondary-foreground: #0f172a;
            --muted: #f1f5f9;
            --muted-foreground: #64748b;
            --accent: #f1f5f9;
            --accent-foreground: #0f172a;
            --destructive: #ef4444;
            --destructive-foreground: #ffffff;
            --border: #e2e8f0;
            --input: #e2e8f0;
            --ring: #2563eb;
            --radius: 0.5rem;
            --success: #22c55e;
            --warning: #f59e0b;
            --danger: #ef4444;
            --sidebar-width: 240px;
            --header-height: 64px;
        }

        /* Dark Mode */
        [data-theme="dark"] {
            --background: #0f172a;
            --foreground: #f8fafc;
            --card: #1e293b;
            --card-foreground: #f8fafc;
            --popover: #1e293b;
            --popover-foreground: #f8fafc;
            --secondary: #1e293b;
            --secondary-foreground: #f8fafc;
            --muted: #1e293b;
            --muted-foreground: #94a3b8;
            --accent: #1e293b;
            --accent-foreground: #f8fafc;
            --border: #1e293b;
            --input: #1e293b;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: var(--background);
            color: var(--foreground);
            line-height: 1.6;
            transition: background 0.3s, color 0.3s;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        button {
            cursor: pointer;
            font-family: inherit;
        }

        /* ============================================
           SCROLLBAR
           ============================================ */
        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        ::-webkit-scrollbar-track {
            background: transparent;
        }
        ::-webkit-scrollbar-thumb {
            background: var(--muted-foreground);
            border-radius: 4px;
            opacity: 0.3;
        }
        ::-webkit-scrollbar-thumb:hover {
            opacity: 0.5;
        }

        /* ============================================
           UTILITY CLASSES
           ============================================ */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        .flex {
            display: flex;
        }
        .flex-col {
            flex-direction: column;
        }
        .items-center {
            align-items: center;
        }
        .justify-between {
            justify-content: space-between;
        }
        .justify-center {
            justify-content: center;
        }
        .gap-2 { gap: 0.5rem; }
        .gap-3 { gap: 0.75rem; }
        .gap-4 { gap: 1rem; }
        .gap-6 { gap: 1.5rem; }
        .gap-8 { gap: 2rem; }

        .text-center { text-align: center; }
        .text-left { text-align: left; }

        .w-full { width: 100%; }
        .max-w-3xl { max-width: 48rem; }
        .max-w-5xl { max-width: 64rem; }
        .mx-auto { margin-left: auto; margin-right: auto; }

        .mt-2 { margin-top: 0.5rem; }
        .mt-4 { margin-top: 1rem; }
        .mt-6 { margin-top: 1.5rem; }
        .mt-8 { margin-top: 2rem; }
        .mt-10 { margin-top: 2.5rem; }
        .mt-16 { margin-top: 4rem; }
        .mb-2 { margin-bottom: 0.5rem; }
        .mb-4 { margin-bottom: 1rem; }
        .mb-6 { margin-bottom: 1.5rem; }
        .mb-8 { margin-bottom: 2rem; }
        .mb-16 { margin-bottom: 4rem; }

        .py-4 { padding-top: 1rem; padding-bottom: 1rem; }
        .py-8 { padding-top: 2rem; padding-bottom: 2rem; }
        .py-12 { padding-top: 3rem; padding-bottom: 3rem; }
        .py-20 { padding-top: 5rem; padding-bottom: 5rem; }
        .px-4 { padding-left: 1rem; padding-right: 1rem; }
        .px-6 { padding-left: 1.5rem; padding-right: 1.5rem; }

        .hidden { display: none; }
        .block { display: block; }

        .relative { position: relative; }
        .absolute { position: absolute; }
        .inset-0 { top: 0; right: 0; bottom: 0; left: 0; }
        .z-10 { z-index: 10; }
        .z-50 { z-index: 50; }

        /* ============================================
           BUTTONS
           ============================================ */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            padding: 0.625rem 1.25rem;
            font-size: 0.875rem;
            font-weight: 500;
            border-radius: var(--radius);
            border: 1px solid transparent;
            transition: all 0.2s;
            cursor: pointer;
            text-decoration: none;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
        }
        .btn-primary:hover {
            background: var(--primary-700);
            transform: translateY(-1px);
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.3);
        }

        .btn-outline {
            background: transparent;
            border-color: var(--border);
            color: var(--foreground);
        }
        .btn-outline:hover {
            background: var(--secondary);
        }

        .btn-ghost {
            background: transparent;
            color: var(--foreground);
        }
        .btn-ghost:hover {
            background: var(--secondary);
        }

        .btn-lg {
            padding: 0.75rem 2rem;
            font-size: 1rem;
        }

        .btn-sm {
            padding: 0.375rem 0.75rem;
            font-size: 0.75rem;
        }

        .btn-success {
            background: var(--success);
            color: white;
        }
        .btn-success:hover {
            background: #16a34a;
        }

        .btn-danger {
            background: var(--danger);
            color: white;
        }
        .btn-danger:hover {
            background: #dc2626;
        }

        /* ============================================
           CARDS
           ============================================ */
        .card {
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: var(--radius);
            overflow: hidden;
            transition: all 0.2s;
        }

        .card:hover {
            border-color: var(--primary-300);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
        }

        .card-header {
            padding: 1.5rem 1.5rem 0.5rem 1.5rem;
        }

        .card-title {
            font-size: 1.25rem;
            font-weight: 600;
            line-height: 1.4;
        }

        .card-description {
            font-size: 0.875rem;
            color: var(--muted-foreground);
            margin-top: 0.25rem;
        }

        .card-content {
            padding: 1rem 1.5rem 1.5rem 1.5rem;
        }

        .card-footer {
            padding: 1rem 1.5rem;
            border-top: 1px solid var(--border);
        }

        /* ============================================
           INPUTS
           ============================================ */
        .input-group {
            display: flex;
            flex-direction: column;
            gap: 0.25rem;
        }

        .input-group label {
            font-size: 0.875rem;
            font-weight: 500;
        }

        .input-group input,
        .input-group select {
            padding: 0.5rem 0.75rem;
            border: 1px solid var(--input);
            border-radius: var(--radius);
            background: var(--background);
            color: var(--foreground);
            font-size: 0.875rem;
            transition: border-color 0.2s;
            font-family: inherit;
        }

        .input-group input:focus,
        .input-group select:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
        }

        .input-group input:disabled {
            opacity: 0.6;
            cursor: not-allowed;
        }

        /* ============================================
           BADGE
           ============================================ */
        .badge {
            display: inline-flex;
            align-items: center;
            padding: 0.125rem 0.625rem;
            border-radius: 9999px;
            font-size: 0.75rem;
            font-weight: 600;
        }

        .badge-primary {
            background: var(--primary-100);
            color: var(--primary-700);
        }

        .badge-success {
            background: #dcfce7;
            color: #166534;
        }

        .badge-warning {
            background: #fef3c7;
            color: #92400e;
        }

        .badge-danger {
            background: #fee2e2;
            color: #991b1b;
        }

        .badge-secondary {
            background: var(--secondary);
            color: var(--secondary-foreground);
        }

        [data-theme="dark"] .badge-primary {
            background: var(--primary-900);
            color: var(--primary-200);
        }
        [data-theme="dark"] .badge-success {
            background: #14532d;
            color: #86efac;
        }
        [data-theme="dark"] .badge-warning {
            background: #78350f;
            color: #fcd34d;
        }
        [data-theme="dark"] .badge-danger {
            background: #7f1d1d;
            color: #fca5a5;
        }

        /* ============================================
           NAVBAR
           ============================================ */
        .navbar {
            position: sticky;
            top: 0;
            z-index: 50;
            background: var(--background);
            border-bottom: 1px solid var(--border);
            backdrop-filter: blur(12px);
            background: rgba(255, 255, 255, 0.8);
        }

        [data-theme="dark"] .navbar {
            background: rgba(15, 23, 42, 0.8);
        }

        .navbar .container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 64px;
        }

        .navbar-logo {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary);
        }

        .navbar-links {
            display: flex;
            align-items: center;
            gap: 2rem;
        }

        .navbar-links a {
            font-size: 0.875rem;
            color: var(--muted-foreground);
            transition: color 0.2s;
        }

        .navbar-links a:hover {
            color: var(--foreground);
        }

        .navbar-actions {
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .theme-toggle {
            padding: 0.5rem;
            border-radius: var(--radius);
            border: none;
            background: transparent;
            color: var(--foreground);
            transition: background 0.2s;
        }

        .theme-toggle:hover {
            background: var(--secondary);
        }

        .mobile-menu-btn {
            display: none;
            padding: 0.5rem;
            border: none;
            background: transparent;
            color: var(--foreground);
            font-size: 1.25rem;
        }

        .mobile-menu {
            display: none;
            padding: 1rem;
            border-top: 1px solid var(--border);
        }

        .mobile-menu a {
            display: block;
            padding: 0.5rem 0;
            color: var(--muted-foreground);
        }

        .mobile-menu .btn {
            width: 100%;
            margin-top: 0.5rem;
        }

        /* ============================================
           HERO
           ============================================ */
        .hero {
            padding: 5rem 0;
            position: relative;
            overflow: hidden;
        }

        .hero-bg {
            position: absolute;
            inset: 0;
            z-index: 0;
            background: linear-gradient(135deg, var(--primary-50) 0%, transparent 50%, transparent 100%);
            opacity: 0.5;
        }

        [data-theme="dark"] .hero-bg {
            background: linear-gradient(135deg, rgba(37, 99, 235, 0.1) 0%, transparent 50%, transparent 100%);
        }

        .hero-content {
            position: relative;
            z-index: 1;
            text-align: center;
        }

        .hero h1 {
            font-size: 3.5rem;
            font-weight: 900;
            line-height: 1.1;
            letter-spacing: -0.02em;
        }

        .hero h1 span {
            color: var(--primary);
            display: block;
        }

        .hero p {
            font-size: 1.25rem;
            color: var(--muted-foreground);
            max-width: 36rem;
            margin: 1.5rem auto 0;
        }

        .hero-actions {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-top: 2.5rem;
            flex-wrap: wrap;
        }

        .hero-social-proof {
            display: flex;
            gap: 2rem;
            justify-content: center;
            margin-top: 3rem;
            font-size: 0.875rem;
            color: var(--muted-foreground);
        }

        /* ============================================
           FEATURES
           ============================================ */
        .features {
            padding: 5rem 0;
            background: var(--secondary);
        }

        [data-theme="dark"] .features {
            background: var(--card);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature-card {
            padding: 1.5rem;
            background: var(--background);
            border-radius: var(--radius);
            border: 1px solid var(--border);
            transition: all 0.3s;
        }

        .feature-card:hover {
            border-color: var(--primary-300);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
            transform: translateY(-2px);
        }

        .feature-icon {
            width: 3rem;
            height: 3rem;
            border-radius: var(--radius);
            background: var(--primary-100);
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.25rem;
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            font-size: 1.125rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .feature-card p {
            font-size: 0.875rem;
            color: var(--muted-foreground);
        }

        /* ============================================
           HOW IT WORKS
           ============================================ */
        .how-it-works {
            padding: 5rem 0;
        }

        .steps-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
            position: relative;
        }

        .step {
            text-align: center;
        }

        .step-number {
            font-size: 3rem;
            font-weight: 900;
            color: var(--primary);
            opacity: 0.1;
            line-height: 1;
        }

        .step-icon {
            width: 3rem;
            height: 3rem;
            border-radius: 50%;
            background: var(--primary-100);
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.25rem;
            margin: 0.5rem auto;
        }

        .step h3 {
            font-size: 1.125rem;
            font-weight: 600;
            margin: 0.5rem 0;
        }

        .step p {
            font-size: 0.875rem;
            color: var(--muted-foreground);
        }

        /* ============================================
           TESTIMONIALS
           ============================================ */
        .testimonials {
            padding: 5rem 0;
            background: var(--secondary);
        }

        [data-theme="dark"] .testimonials {
            background: var(--card);
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .testimonial-card {
            padding: 1.5rem;
            background: var(--background);
            border-radius: var(--radius);
            border: 1px solid var(--border);
        }

        .testimonial-stars {
            color: var(--warning);
            margin-bottom: 0.75rem;
        }

        .testimonial-text {
            font-size: 0.875rem;
            color: var(--muted-foreground);
            margin-bottom: 1rem;
            font-style: italic;
        }

        .testimonial-author {
            font-weight: 600;
        }

        .testimonial-role {
            font-size: 0.75rem;
            color: var(--muted-foreground);
        }

        /* ============================================
           PRICING
           ============================================ */
        .pricing {
            padding: 5rem 0;
        }

        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .pricing-card {
            padding: 2rem;
            background: var(--card);
            border-radius: var(--radius);
            border: 1px solid var(--border);
            text-align: center;
            position: relative;
            transition: all 0.3s;
        }

        .pricing-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.08);
        }

        .pricing-card.popular {
            border-color: var(--primary);
            box-shadow: 0 8px 30px rgba(37, 99, 235, 0.15);
        }

        .pricing-popular {
            position: absolute;
            top: -0.75rem;
            left: 50%;
            transform: translateX(-50%);
            padding: 0.25rem 1rem;
            background: var(--primary);
            color: white;
            font-size: 0.75rem;
            font-weight: 600;
            border-radius: 9999px;
        }

        .pricing-card h3 {
            font-size: 1.25rem;
            font-weight: 600;
        }

        .pricing-price {
            font-size: 3rem;
            font-weight: 800;
            margin: 1rem 0;
        }

        .pricing-price span {
            font-size: 1rem;
            font-weight: 400;
            color: var(--muted-foreground);
        }

        .pricing-description {
            font-size: 0.875rem;
            color: var(--muted-foreground);
            margin-bottom: 1.5rem;
        }

        .pricing-features {
            list-style: none;
            text-align: left;
            margin: 1.5rem 0;
        }

        .pricing-features li {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.5rem 0;
            font-size: 0.875rem;
        }

        .pricing-features li i {
            color: var(--primary);
            font-size: 0.75rem;
        }

        .pricing-card .btn {
            width: 100%;
        }

        /* ============================================
           FAQ
           ============================================ */
        .faq {
            padding: 5rem 0;
            background: var(--secondary);
        }

        [data-theme="dark"] .faq {
            background: var(--card);
        }

        .faq-list {
            max-width: 48rem;
            margin: 3rem auto 0;
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }

        .faq-item {
            border: 1px solid var(--border);
            border-radius: var(--radius);
            overflow: hidden;
            background: var(--background);
        }

        .faq-question {
            width: 100%;
            padding: 1rem 1.5rem;
            background: none;
            border: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 1rem;
            font-weight: 500;
            color: var(--foreground);
            text-align: left;
        }

        .faq-question:hover {
            background: var(--secondary);
        }

        .faq-question i {
            transition: transform 0.2s;
        }

        .faq-question.active i {
            transform: rotate(180deg);
        }

        .faq-answer {
            padding: 0 1.5rem;
            max-height: 0;
            overflow: hidden;
            transition: all 0.3s;
            color: var(--muted-foreground);
            font-size: 0.875rem;
        }

        .faq-answer.open {
            padding: 0 1.5rem 1.5rem;
            max-height: 200px;
        }

        /* ============================================
           FOOTER
           ============================================ */
        .footer {
            padding: 3rem 0;
            border-top: 1px solid var(--border);
            background: var(--background);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 2rem;
        }

        .footer h4 {
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .footer ul {
            list-style: none;
        }

        .footer ul li {
            padding: 0.25rem 0;
        }

        .footer ul li a {
            font-size: 0.875rem;
            color: var(--muted-foreground);
            transition: color 0.2s;
        }

        .footer ul li a:hover {
            color: var(--foreground);
        }

        .footer-bottom {
            margin-top: 2rem;
            padding-top: 2rem;
            border-top: 1px solid var(--border);
            text-align: center;
            font-size: 0.875rem;
            color: var(--muted-foreground);
        }

        /* ============================================
           SIDEBAR (Dashboard)
           ============================================ */
        .dashboard-layout {
            display: flex;
            min-height: 100vh;
        }

        .sidebar {
            width: var(--sidebar-width);
            border-right: 1px solid var(--border);
            background: var(--card);
            display: flex;
            flex-direction: column;
            position: fixed;
            top: 0;
            left: 0;
            bottom: 0;
            z-index: 40;
            transition: transform 0.3s;
        }

        .sidebar-brand {
            padding: 1.5rem;
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary);
        }

        .sidebar-nav {
            flex: 1;
            padding: 0.5rem 1rem;
            overflow-y: auto;
        }

        .sidebar-nav a {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            padding: 0.625rem 0.75rem;
            border-radius: var(--radius);
            font-size: 0.875rem;
            font-weight: 500;
            color: var(--muted-foreground);
            transition: all 0.2s;
        }

        .sidebar-nav a:hover {
            background: var(--secondary);
            color: var(--foreground);
        }

        .sidebar-nav a.active {
            background: var(--primary-100);
            color: var(--primary);
        }

        [data-theme="dark"] .sidebar-nav a.active {
            background: var(--primary-900);
            color: var(--primary-300);
        }

        .sidebar-nav a i {
            width: 1.25rem;
            text-align: center;
        }

        .sidebar-footer {
            padding: 1rem;
            border-top: 1px solid var(--border);
        }

        .sidebar-footer .btn {
            width: 100%;
            justify-content: flex-start;
        }

        /* ============================================
           DASHBOARD MAIN
           ============================================ */
        .dashboard-main {
            flex: 1;
            margin-left: var(--sidebar-width);
            padding: 1.5rem;
            min-height: 100vh;
        }

        .dashboard-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
            border-bottom: 1px solid var(--border);
            margin-bottom: 1.5rem;
        }

        .dashboard-header h1 {
            font-size: 1.5rem;
            font-weight: 700;
        }

        .dashboard-header-actions {
            display: flex;
            gap: 0.5rem;
        }

        /* ============================================
           DASHBOARD CARDS
           ============================================ */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .stat-card {
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: var(--radius);
            padding: 1.25rem;
        }

        .stat-card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: var(--muted-foreground);
            font-size: 0.875rem;
            font-weight: 500;
        }

        .stat-card-header i {
            font-size: 1.25rem;
        }

        .stat-card-value {
            font-size: 2rem;
            font-weight: 700;
            margin-top: 0.5rem;
        }

        .stat-card-change {
            font-size: 0.75rem;
            color: var(--muted-foreground);
            margin-top: 0.25rem;
        }

        /* ============================================
           QUICK ACTIONS
           ============================================ */
        .quick-actions {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 1rem;
        }

        .quick-action {
            padding: 1.5rem;
            border-radius: var(--radius);
            border: 1px solid var(--border);
            background: var(--card);
            text-align: left;
            transition: all 0.2s;
        }

        .quick-action:hover {
            border-color: var(--primary-300);
            transform: translateY(-2px);
        }

        .quick-action i {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .quick-action h4 {
            font-weight: 600;
            font-size: 0.875rem;
        }

        .quick-action p {
            font-size: 0.75rem;
            color: var(--muted-foreground);
        }

        /* ============================================
           CALCULATOR PAGE
           ============================================ */
        .calculator-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .calculator-inputs {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .calculator-result {
            padding: 1rem 0;
        }

        .result-item {
            padding: 0.75rem 1rem;
            background: var(--secondary);
            border-radius: var(--radius);
            margin-bottom: 0.75rem;
        }

        .result-item .label {
            font-size: 0.75rem;
            color: var(--muted-foreground);
        }

        .result-item .value {
            font-size: 1.5rem;
            font-weight: 700;
        }

        .result-item.primary {
            background: var(--primary-100);
        }

        .result-item.primary .value {
            color: var(--primary);
        }

        .result-item.success {
            background: #dcfce7;
        }

        [data-theme="dark"] .result-item.success {
            background: #14532d;
        }

        .result-item.success .value {
            color: var(--success);
        }

        .result-item.warning {
            background: #fef3c7;
        }

        [data-theme="dark"] .result-item.warning {
            background: #78350f;
        }

        .result-item.warning .value {
            color: var(--warning);
        }

        .result-actions {
            display: flex;
            gap: 0.75rem;
            margin-top: 1rem;
        }

        .result-actions .btn {
            flex: 1;
        }

        /* ============================================
           CLIENTS TABLE
           ============================================ */
        .clients-toolbar {
            display: flex;
            gap: 1rem;
            margin-bottom: 1.5rem;
            flex-wrap: wrap;
        }

        .clients-toolbar .input-group {
            flex: 1;
            min-width: 200px;
        }

        .clients-toolbar select {
            padding: 0.5rem 0.75rem;
            border: 1px solid var(--input);
            border-radius: var(--radius);
            background: var(--background);
            color: var(--foreground);
            font-size: 0.875rem;
        }

        .client-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem;
            border: 1px solid var(--border);
            border-radius: var(--radius);
            margin-bottom: 0.75rem;
            transition: all 0.2s;
        }

        .client-item:hover {
            border-color: var(--primary-300);
        }

        .client-info h4 {
            font-weight: 600;
        }

        .client-info .details {
            font-size: 0.875rem;
            color: var(--muted-foreground);
        }

        .client-actions {
            display: flex;
            gap: 0.5rem;
        }

        /* ============================================
           SETTINGS PAGE
           ============================================ */
        .settings-section {
            max-width: 48rem;
        }

        .settings-section .card {
            margin-bottom: 1.5rem;
        }

        .settings-section .card-content {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .theme-options {
            display: flex;
            gap: 0.5rem;
        }

        .theme-options .btn {
            flex: 1;
        }

        /* ============================================
           RESPONSIVE
           ============================================ */
        @media (max-width: 1024px) {
            .features-grid,
            .testimonials-grid,
            .pricing-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .steps-grid {
                grid-template-columns: 1fr 1fr;
            }
            .footer-grid {
                grid-template-columns: 1fr 1fr;
            }
            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .quick-actions {
                grid-template-columns: repeat(2, 1fr);
            }
            .calculator-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            .hero p {
                font-size: 1rem;
            }

            .features-grid,
            .testimonials-grid,
            .pricing-grid,
            .steps-grid {
                grid-template-columns: 1fr;
            }

            .footer-grid {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .navbar-links {
                display: none;
            }
            .mobile-menu-btn {
                display: block;
            }
            .mobile-menu.open {
                display: block;
            }

            .sidebar {
                transform: translateX(-100%);
            }
            .sidebar.open {
                transform: translateX(0);
            }
            .dashboard-main {
                margin-left: 0;
            }

            .stats-grid {
                grid-template-columns: 1fr 1fr;
            }
            .quick-actions {
                grid-template-columns: 1fr 1fr;
            }

            .hero-actions {
                flex-direction: column;
                align-items: center;
            }
            .hero-actions .btn {
                width: 100%;
                max-width: 300px;
            }

            .hero-social-proof {
                flex-direction: column;
                gap: 0.5rem;
            }

            .clients-toolbar {
                flex-direction: column;
            }
            .clients-toolbar .input-group {
                min-width: unset;
            }

            .client-item {
                flex-direction: column;
                align-items: flex-start;
                gap: 0.5rem;
            }
            .client-actions {
                width: 100%;
            }
            .client-actions .btn {
                flex: 1;
            }

            .settings-section .theme-options {
                flex-direction: column;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }
            .stats-grid {
                grid-template-columns: 1fr;
            }
            .quick-actions {
                grid-template-columns: 1fr;
            }
            .result-actions {
                flex-direction: column;
            }
            .pricing-card {
                padding: 1.5rem;
            }
        }

        /* ============================================
           ANIMATIONS
           ============================================ */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .animate-in {
            animation: fadeInUp 0.5s ease-out forwards;
        }

        .delay-1 {
            animation-delay: 0.1s;
        }
        .delay-2 {
            animation-delay: 0.2s;
        }
        .delay-3 {
            animation-delay: 0.3s;
        }
        .delay-4 {
            animation-delay: 0.4s;
        }

        /* ============================================
           PAGE TRANSITIONS
           ============================================ */
        .page {
            display: none;
        }

        .page.active {
            display: block;
        }

        /* ============================================
           NOTIFICATION
           ============================================ */
        .notification {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            padding: 1rem 1.5rem;
            border-radius: var(--radius);
            background: var(--card);
            border: 1px solid var(--border);
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.15);
            z-index: 100;
            transform: translateY(100px);
            opacity: 0;
            transition: all 0.3s;
        }

        .notification.show {
            transform: translateY(0);
            opacity: 1;
        }

        .notification.success {
            border-color: var(--success);
        }

        .notification.success i {
            color: var(--success);
        }

        /* ============================================
           MOBILE OVERLAY
           ============================================ */
        .overlay {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.5);
            z-index: 35;
        }

        .overlay.show {
            display: block;
        }

        /* ============================================
           EMPTY STATE
           ============================================ */
        .empty-state {
            text-align: center;
            padding: 3rem 1rem;
        }

        .empty-state i {
            font-size: 3rem;
            color: var(--muted-foreground);
            opacity: 0.5;
            margin-bottom: 1rem;
        }

        .empty-state h3 {
            font-size: 1.125rem;
            font-weight: 600;
        }

        .empty-state p {
            color: var(--muted-foreground);
            font-size: 0.875rem;
        }
    </style>
</head>
<body>

    <!-- ============================================
    NOTIFICATION
    ============================================ -->
    <div id="notification" class="notification">
        <i class="fas fa-check-circle"></i>
        <span id="notificationMessage">Saved successfully!</span>
    </div>

    <!-- ============================================
    MOBILE OVERLAY
    ============================================ -->
    <div id="overlay" class="overlay" onclick="closeMobileMenu()"></div>

    <!-- ============================================
    NAVBAR
    ============================================ -->
    <nav class="navbar" id="navbar">
        <div class="container">
            <a href="#" class="navbar-logo" onclick="showPage('landing')">Prezzo</a>

            <div class="navbar-links" id="navLinks">
                <a href="#features" onclick="showPage('landing')">Features</a>
                <a href="#pricing" onclick="showPage('landing')">Pricing</a>
                <a href="#faq" onclick="showPage('landing')">FAQ</a>
            </div>

            <div class="navbar-actions">
                <button class="theme-toggle" onclick="toggleTheme()" aria-label="Toggle theme">
                    <i class="fas fa-moon" id="themeIcon"></i>
                </button>
                <button class="btn btn-ghost" onclick="showPage('login')" id="loginBtn">Login</button>
                <button class="btn btn-primary" onclick="showPage('signup')" id="signupBtn">Start Free</button>
                <button class="mobile-menu-btn" onclick="toggleMobileMenu()" aria-label="Toggle menu">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div class="mobile-menu" id="mobileMenu">
            <a href="#features" onclick="showPage('landing')">Features</a>
            <a href="#pricing" onclick="showPage('landing')">Pricing</a>
            <a href="#faq" onclick="showPage('landing')">FAQ</a>
            <button class="btn btn-ghost" onclick="showPage('login')">Login</button>
            <button class="btn btn-primary" onclick="showPage('signup')">Start Free</button>
        </div>
    </nav>

    <!-- ============================================
    LANDING PAGE
    ============================================ -->
    <div class="page active" id="page-landing">

        <!-- HERO -->
        <section class="hero">
            <div class="hero-bg"></div>
            <div class="container">
                <div class="hero-content animate-in">
                    <h1>
                        Stop Undercharging
                        <span>Your Clients</span>
                    </h1>
                    <p>
                        Calculate profitable project pricing, track revenue goals, manage clients,
                        and grow your freelance business with confidence.
                    </p>
                    <div class="hero-actions">
                        <button class="btn btn-primary btn-lg" onclick="showPage('signup')">
                            Start Free <i class="fas fa-arrow-right"></i>
                        </button>
                        <button class="btn btn-outline btn-lg">
                            <i class="fas fa-play"></i> Watch Demo
                        </button>
                    </div>
                    <div class="hero-social-proof">
                        <span>⭐ 4.9/5 from 2,000+ freelancers</span>
                        <span>•</span>
                        <span>🚀 10,000+ projects priced</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- FEATURES -->
        <section class="features" id="features">
            <div class="container">
                <div class="text-center max-w-3xl mx-auto">
                    <h2 style="font-size: 2.25rem; font-weight: 800; letter-spacing: -0.02em;">
                        Everything you need to price <span style="color: var(--primary);">profitably</span>
                    </h2>
                    <p style="color: var(--muted-foreground); font-size: 1.125rem; margin-top: 1rem;">
                        From calculating the perfect price to managing clients and growing your business.
                    </p>
                </div>

                <div class="features-grid">
                    <div class="feature-card animate-in delay-1">
                        <div class="feature-icon"><i class="fas fa-calculator"></i></div>
                        <h3>Pricing Calculator</h3>
                        <p>Calculate profitable project prices with buffer and premium packages.</p>
                    </div>
                    <div class="feature-card animate-in delay-2">
                        <div class="feature-icon"><i class="fas fa-clock"></i></div>
                        <h3>Hourly Rate Calculator</h3>
                        <p>Determine your ideal hourly rate based on income goals and expenses.</p>
                    </div>
                    <div class="feature-card animate-in delay-3">
                        <div class="feature-icon"><i class="fas fa-bullseye"></i></div>
                        <h3>Revenue Goal Tracker</h3>
                        <p>Set monthly targets and track your progress with daily goals.</p>
                    </div>
                    <div class="feature-card animate-in delay-2">
                        <div class="feature-icon"><i class="fas fa-file-alt"></i></div>
                        <h3>Proposal Builder</h3>
                        <p>Create beautiful, professional proposals with custom templates.</p>
                    </div>
                    <div class="feature-card animate-in delay-3">
                        <div class="feature-icon"><i class="fas fa-users"></i></div>
                        <h3>Client CRM</h3>
                        <p>Manage leads, track interactions, and never miss a follow-up.</p>
                    </div>
                    <div class="feature-card animate-in delay-4">
                        <div class="feature-icon"><i class="fas fa-chart-bar"></i></div>
                        <h3>Analytics Dashboard</h3>
                        <p>Visualize your revenue, pipeline, and conversion rates.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- HOW IT WORKS -->
        <section class="how-it-works" id="how-it-works">
            <div class="container">
                <div class="text-center max-w-3xl mx-auto">
                    <h2 style="font-size: 2.25rem; font-weight: 800; letter-spacing: -0.02em;">
                        How <span style="color: var(--primary);">Prezzo</span> Works
                    </h2>
                    <p style="color: var(--muted-foreground); font-size: 1.125rem; margin-top: 1rem;">
                        Three simple steps to start pricing your projects profitably.
                    </p>
                </div>

                <div class="steps-grid">
                    <div class="step animate-in delay-1">
                        <div class="step-number">01</div>
                        <div class="step-icon"><i class="fas fa-calculator"></i></div>
                        <h3>Calculate Your Price</h3>
                        <p>Use our pricing calculator to determine profitable project rates.</p>
                    </div>
                    <div class="step animate-in delay-2">
                        <div class="step-number">02</div>
                        <div class="step-icon"><i class="fas fa-users"></i></div>
                        <h3>Manage Your Clients</h3>
                        <p>Track leads, proposals, and client relationships in one central CRM.</p>
                    </div>
                    <div class="step animate-in delay-3">
                        <div class="step-number">03</div>
                        <div class="step-icon"><i class="fas fa-chart-line"></i></div>
                        <h3>Grow Your Revenue</h3>
                        <p>Set revenue goals, track progress, and make data-driven decisions.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- TESTIMONIALS -->
        <section class="testimonials" id="testimonials">
            <div class="container">
                <div class="text-center max-w-3xl mx-auto">
                    <h2 style="font-size: 2.25rem; font-weight: 800; letter-spacing: -0.02em;">
                        Loved by <span style="color: var(--primary);">freelancers</span> everywhere
                    </h2>
                    <p style="color: var(--muted-foreground); font-size: 1.125rem; margin-top: 1rem;">
                        See what our users have to say about Prezzo.
                    </p>
                </div>

                <div class="testimonials-grid">
                    <div class="testimonial-card animate-in delay-1">
                        <div class="testimonial-stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                        <p class="testimonial-text">"Prezzo completely transformed how I price my projects. I went from guessing to confidently charging what I'm worth."</p>
                        <div>
                            <div class="testimonial-author">Sarah Johnson</div>
                            <div class="testimonial-role">Freelance Web Developer</div>
                        </div>
                    </div>
                    <div class="testimonial-card animate-in delay-2">
                        <div class="testimonial-stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                        <p class="testimonial-text">"The revenue goal calculator helped me set clear targets. I've increased my monthly revenue by 40% in just 3 months."</p>
                        <div>
                            <div class="testimonial-author">Michael Chen</div>
                            <div class="testimonial-role">Digital Marketing Agency Owner</div>
                        </div>
                    </div>
                    <div class="testimonial-card animate-in delay-3">
                        <div class="testimonial-stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                        <p class="testimonial-text">"The proposal builder is a game-changer. My clients love the professional look, and I close deals faster."</p>
                        <div>
                            <div class="testimonial-author">Emma Rodriguez</div>
                            <div class="testimonial-role">UI/UX Designer</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- PRICING -->
        <section class="pricing" id="pricing">
            <div class="container">
                <div class="text-center max-w-3xl mx-auto">
                    <h2 style="font-size: 2.25rem; font-weight: 800; letter-spacing: -0.02em;">
                        Simple, <span style="color: var(--primary);">transparent</span> pricing
                    </h2>
                    <p style="color: var(--muted-foreground); font-size: 1.125rem; margin-top: 1rem;">
                        Choose the plan that fits your business needs.
                    </p>
                </div>

                <div class="pricing-grid">
                    <div class="pricing-card animate-in delay-1">
                        <h3>Starter</h3>
                        <div class="pricing-price">$0 <span>/ month</span></div>
                        <p class="pricing-description">Perfect for freelancers just getting started</p>
                        <ul class="pricing-features">
                            <li><i class="fas fa-check"></i> Pricing Calculator</li>
                            <li><i class="fas fa-check"></i> Hourly Rate Calculator</li>
                            <li><i class="fas fa-check"></i> Revenue Goal Tracker</li>
                            <li><i class="fas fa-check"></i> 3 Saved Calculations</li>
                            <li><i class="fas fa-check"></i> Basic Support</li>
                        </ul>
                        <button class="btn btn-outline" onclick="showPage('signup')">Start Free</button>
                    </div>

                    <div class="pricing-card popular animate-in delay-2">
                        <div class="pricing-popular">Most Popular</div>
                        <h3>Pro</h3>
                        <div class="pricing-price">$29 <span>/ month</span></div>
                        <p class="pricing-description">For serious freelancers and growing agencies</p>
                        <ul class="pricing-features">
                            <li><i class="fas fa-check"></i> Everything in Starter</li>
                            <li><i class="fas fa-check"></i> Client CRM</li>
                            <li><i class="fas fa-check"></i> Proposal Builder</li>
                            <li><i class="fas fa-check"></i> Unlimited Saved Calculations</li>
                            <li><i class="fas fa-check"></i> Analytics Dashboard</li>
                            <li><i class="fas fa-check"></i> Priority Support</li>
                        </ul>
                        <button class="btn btn-primary" onclick="showPage('signup')">Start Free Trial</button>
                    </div>

                    <div class="pricing-card animate-in delay-3">
                        <h3>Business</h3>
                        <div class="pricing-price">$79 <span>/ month</span></div>
                        <p class="pricing-description">For agencies and teams scaling their business</p>
                        <ul class="pricing-features">
                            <li><i class="fas fa-check"></i> Everything in Pro</li>
                            <li><i class="fas fa-check"></i> Team Collaboration</li>
                            <li><i class="fas fa-check"></i> Advanced Analytics</li>
                            <li><i class="fas fa-check"></i> Custom Branding</li>
                            <li><i class="fas fa-check"></i> API Access</li>
                            <li><i class="fas fa-check"></i> Dedicated Support</li>
                        </ul>
                        <button class="btn btn-outline">Contact Sales</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- FAQ -->
        <section class="faq" id="faq">
            <div class="container">
                <div class="text-center">
                    <h2 style="font-size: 2.25rem; font-weight: 800; letter-spacing: -0.02em;">
                        Frequently Asked <span style="color: var(--primary);">Questions</span>
                    </h2>
                </div>

                <div class="faq-list">
                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            What is Prezzo?
                            <i class="fas fa-chevron-down"></i>
                        </button>
                        <div class="faq-answer">
                            Prezzo is a complete business tool for freelancers and agencies that helps you calculate profitable pricing, manage clients, track revenue goals, and create professional proposals.
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            Who is Prezzo for?
                            <i class="fas fa-chevron-down"></i>
                        </button>
                        <div class="faq-answer">
                            Prezzo is designed for freelancers, agencies, consultants, social media managers, web developers, designers, and marketers who want to price their projects profitably and grow their business.
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            How does the pricing calculator work?
                            <i class="fas fa-chevron-down"></i>
                        </button>
                        <div class="faq-answer">
                            The pricing calculator takes into account your estimated hours, hourly rate, buffer percentage, and revisions to provide you with a base price, recommended price, and premium package price.
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            Can I save my calculations?
                            <i class="fas fa-chevron-down"></i>
                        </button>
                        <div class="faq-answer">
                            Yes! You can save, edit, and search all your calculations including pricing, revenue, and profit calculations.
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            Is there a free trial?
                            <i class="fas fa-chevron-down"></i>
                        </button>
                        <div class="faq-answer">
                            Yes, you can start with our free plan which includes all core features, or try Pro with a 14-day free trial.
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            Can I cancel anytime?
                            <i class="fas fa-chevron-down"></i>
                        </button>
                        <div class="faq-answer">
                            Yes, you can cancel your subscription at any time with no hidden fees or penalties.
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- FOOTER -->
        <footer class="footer">
            <div class="container">
                <div class="footer-grid">
                    <div>
                        <h3 style="font-size: 1.5rem; font-weight: 800; color: var(--primary);">Prezzo</h3>
                        <p style="color: var(--muted-foreground); font-size: 0.875rem; margin-top: 0.5rem;">
                            Stop Undercharging. Price Every Project Profitably.
                        </p>
                    </div>
                    <div>
                        <h4>Product</h4>
                        <ul>
                            <li><a href="#features">Features</a></li>
                            <li><a href="#pricing">Pricing</a></li>
                            <li><a href="#faq">FAQ</a></li>
                        </ul>
                    </div>
                    <div>
                        <h4>Company</h4>
                        <ul>
                            <li><a href="#">About</a></li>
                            <li><a href="#">Blog</a></li>
                            <li><a href="#">Contact</a></li>
                        </ul>
                    </div>
                    <div>
                        <h4>Legal</h4>
                        <ul>
                            <li><a href="#">Privacy</a></li>
                            <li><a href="#">Terms</a></li>
                        </ul>
                    </div>
                </div>
                <div class="footer-bottom">
                    &copy; 2026 Prezzo. All rights reserved.
                </div>
            </div>
        </footer>
    </div>

    <!-- ============================================
    LOGIN PAGE
    ============================================ -->
    <div class="page" id="page-login" style="min-height: 100vh; display: none; align-items: center; justify-content: center; padding: 2rem; background: var(--secondary);">
        <div class="card" style="max-width: 400px; width: 100%;">
            <div class="card-header text-center">
                <h2 class="card-title" style="font-size: 1.75rem;">Welcome Back</h2>
                <p class="card-description">Sign in to your Prezzo account</p>
            </div>
            <div class="card-content">
                <form onsubmit="handleLogin(event)" style="display: flex; flex-direction: column; gap: 1rem;">
                    <div class="input-group">
                        <label for="loginEmail">Email</label>
                        <input type="email" id="loginEmail" placeholder="you@example.com" required />
                    </div>
                    <div class="input-group">
                        <label for="loginPassword">Password</label>
                        <input type="password" id="loginPassword" placeholder="••••••••" required />
                    </div>
                    <button type="submit" class="btn btn-primary w-full">Sign In</button>
                </form>

                <div style="position: relative; margin: 1.5rem 0; text-align: center;">
                    <hr style="border: none; border-top: 1px solid var(--border);" />
                    <span style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); background: var(--card); padding: 0 0.75rem; font-size: 0.75rem; color: var(--muted-foreground); text-transform: uppercase;">Or continue with</span>
                </div>

                <button class="btn btn-outline w-full" onclick="handleGoogleLogin()">
                    <i class="fab fa-google"></i> Google
                </button>
            </div>
            <div class="card-footer" style="display: flex; justify-content: center; gap: 0.5rem; font-size: 0.875rem;">
                <a href="#" onclick="showPage('forgot-password')" style="color: var(--muted-foreground);">Forgot password?</a>
                <span style="color: var(--muted-foreground);">•</span>
                <a href="#" onclick="showPage('signup')" style="color: var(--primary);">Create account</a>
            </div>
        </div>
    </div>

    <!-- ============================================
    SIGNUP PAGE
    ============================================ -->
    <div class="page" id="page-signup" style="min-height: 100vh; display: none; align-items: center; justify-content: center; padding: 2rem; background: var(--secondary);">
        <div class="card" style="max-width: 400px; width: 100%;">
            <div class="card-header text-center">
                <h2 class="card-title" style="font-size: 1.75rem;">Create Your Account</h2>
                <p class="card-description">Start pricing your projects profitably today</p>
            </div>
            <div class="card-content">
                <form onsubmit="handleSignup(event)" style="display: flex; flex-direction: column; gap: 1rem;">
                    <div class="input-group">
                        <label for="signupName">Name</label>
                        <input type="text" id="signupName" placeholder="John Doe" required />
                    </div>
                    <div class="input-group">
                        <label for="signupEmail">Email</label>
                        <input type="email" id="signupEmail" placeholder="you@example.com" required />
                    </div>
                    <div class="input-group">
                        <label for="signupPassword">Password</label>
                        <input type="password" id="signupPassword" placeholder="••••••••" required minlength="6" />
                        <span style="font-size: 0.75rem; color: var(--muted-foreground);">Must be at least 6 characters</span>
                    </div>
                    <button type="submit" class="btn btn-primary w-full">Create Account</button>
                </form>

                <div style="position: relative; margin: 1.5rem 0; text-align: center;">
                    <hr style="border: none; border-top: 1px solid var(--border);" />
                    <span style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); background: var(--card); padding: 0 0.75rem; font-size: 0.75rem; color: var(--muted-foreground); text-transform: uppercase;">Or continue with</span>
                </div>

                <button class="btn btn-outline w-full" onclick="handleGoogleLogin()">
                    <i class="fab fa-google"></i> Google
                </button>
            </div>
            <div class="card-footer text-center">
                <p style="font-size: 0.875rem; color: var(--muted-foreground);">
                    Already have an account? <a href="#" onclick="showPage('login')" style="color: var(--primary);">Sign in</a>
                </p>
            </div>
        </div>
    </div>

    <!-- ============================================
    FORGOT PASSWORD PAGE
    ============================================ -->
    <div class="page" id="page-forgot-password" style="min-height: 100vh; display: none; align-items: center; justify-content: center; padding: 2rem; background: var(--secondary);">
        <div class="card" style="max-width: 400px; width: 100%;">
            <div class="card-header text-center">
                <h2 class="card-title" style="font-size: 1.75rem;">Reset Password</h2>
                <p class="card-description">We'll send you instructions to reset your password</p>
            </div>
            <div class="card-content">
                <form onsubmit="handleResetPassword(event)" style="display: flex; flex-direction: column; gap: 1rem;">
                    <div class="input-group">
                        <label for="resetEmail">Email</label>
                        <input type="email" id="resetEmail" placeholder="you@example.com" required />
                    </div>
                    <button type="submit" class="btn btn-primary w-full">Send Instructions</button>
                </form>
            </div>
            <div class="card-footer text-center">
                <a href="#" onclick="showPage('login')" style="color: var(--primary); font-size: 0.875rem;">Back to login</a>
            </div>
        </div>
    </div>

    <!-- ============================================
    DASHBOARD LAYOUT
    ============================================ -->
    <div class="page" id="page-dashboard" style="display: none;">
        <div class="dashboard-layout">
            <!-- Sidebar Overlay -->
            <div id="sidebarOverlay" class="overlay" onclick="closeSidebar()"></div>

            <!-- Sidebar -->
            <aside class="sidebar" id="sidebar">
                <div class="sidebar-brand">Prezzo</div>
                <nav class="sidebar-nav">
                    <a href="#" class="active" onclick="showDashboardPage('dashboard')" data-page="dashboard">
                        <i class="fas fa-th-large"></i> Dashboard
                    </a>
                    <a href="#" onclick="showDashboardPage('pricing-calculator')" data-page="pricing-calculator">
                        <i class="fas fa-calculator"></i> Pricing Calculator
                    </a>
                    <a href="#" onclick="showDashboardPage('hourly-rate')" data-page="hourly-rate">
                        <i class="fas fa-clock"></i> Hourly Rate
                    </a>
                    <a href="#" onclick="showDashboardPage('revenue-goal')" data-page="revenue-goal">
                        <i class="fas fa-bullseye"></i> Revenue Goal
                    </a>
                    <a href="#" onclick="showDashboardPage('profit-calculator')" data-page="profit-calculator">
                        <i class="fas fa-chart-line"></i> Profit Calculator
                    </a>
                    <a href="#" onclick="showDashboardPage('clients')" data-page="clients">
                        <i class="fas fa-users"></i> Client CRM
                    </a>
                    <a href="#" onclick="showDashboardPage('settings')" data-page="settings">
                        <i class="fas fa-cog"></i> Settings
                    </a>
                    <a href="#" onclick="showDashboardPage('admin')" data-page="admin">
                        <i class="fas fa-shield-alt"></i> Admin
                    </a>
                </nav>
                <div class="sidebar-footer">
                    <button class="btn btn-ghost" onclick="handleLogout()" style="justify-content: flex-start;">
                        <i class="fas fa-sign-out-alt"></i> Logout
                    </button>
                </div>
            </aside>

            <!-- Main Content -->
            <main class="dashboard-main">
                <!-- Dashboard Header -->
                <div class="dashboard-header">
                    <div>
                        <h1 id="dashboardTitle">Dashboard</h1>
                        <p style="color: var(--muted-foreground); font-size: 0.875rem;" id="dashboardSubtitle">Welcome back! Here's an overview of your business.</p>
                    </div>
                    <div class="dashboard-header-actions">
                        <button class="btn btn-ghost btn-sm" onclick="toggleSidebar()" style="display: none;" id="sidebarToggle">
                            <i class="fas fa-bars"></i>
                        </button>
                        <button class="theme-toggle" onclick="toggleTheme()">
                            <i class="fas fa-moon" id="dashboardThemeIcon"></i>
                        </button>
                    </div>
                </div>

                <!-- Dashboard Pages -->
                <div id="dashboard-content">
                    <!-- DASHBOARD HOME -->
                    <div class="dashboard-page active" id="dp-dashboard">
                        <div class="stats-grid">
                            <div class="stat-card">
                                <div class="stat-card-header">
                                    <span>Total Clients</span>
                                    <i class="fas fa-users" style="color: var(--primary);"></i>
                                </div>
                                <div class="stat-card-value" id="statClients">0</div>
                                <div class="stat-card-change">Active clients</div>
                            </div>
                            <div class="stat-card">
                                <div class="stat-card-header">
                                    <span>Active Leads</span>
                                    <i class="fas fa-user-plus" style="color: var(--warning);"></i>
                                </div>
                                <div class="stat-card-value" id="statLeads">0</div>
                                <div class="stat-card-change">In pipeline</div>
                            </div>
                            <div class="stat-card">
                                <div class="stat-card-header">
                                    <span>Revenue Goal</span>
                                    <i class="fas fa-bullseye" style="color: var(--success);"></i>
                                </div>
                                <div class="stat-card-value" id="statRevenue">$0</div>
                                <div class="stat-card-change">Monthly target</div>
                            </div>
                            <div class="stat-card">
                                <div class="stat-card-header">
                                    <span>Proposals Sent</span>
                                    <i class="fas fa-file-alt" style="color: var(--primary);"></i>
                                </div>
                                <div class="stat-card-value" id="statProposals">0</div>
                                <div class="stat-card-change">Total sent</div>
                            </div>
                        </div>

                        <div class="quick-actions">
                            <button class="quick-action" onclick="showDashboardPage('pricing-calculator')">
                                <i class="fas fa-calculator" style="color: var(--primary);"></i>
                                <h4>Price a Project</h4>
                                <p>Calculate profitable pricing</p>
                            </button>
                            <button class="quick-action" onclick="showDashboardPage('clients')">
                                <i class="fas fa-user-plus" style="color: var(--success);"></i>
                                <h4>Add Client</h4>
                                <p>Track a new lead</p>
                            </button>
                            <button class="quick-action" onclick="showDashboardPage('revenue-goal')">
                                <i class="fas fa-bullseye" style="color: var(--warning);"></i>
                                <h4>Set Revenue Goal</h4>
                                <p>Define your targets</p>
                            </button>
                            <button class="quick-action">
                                <i class="fas fa-file-alt" style="color: var(--primary);"></i>
                                <h4>Create Proposal</h4>
                                <p>Generate a proposal</p>
                            </button>
                        </div>
                    </div>

                    <!-- PRICING CALCULATOR -->
                    <div class="dashboard-page" id="dp-pricing-calculator" style="display: none;">
                        <p style="color: var(--muted-foreground); margin-bottom: 1.5rem;">Calculate profitable project pricing with buffer and premium packages.</p>
                        <div class="calculator-grid">
                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Project Details</h3>
                                </div>
                                <div class="card-content">
                                    <div class="calculator-inputs">
                                        <div class="input-group">
                                            <label>Project Type</label>
                                            <select id="pricingProjectType">
                                                <option value="website">Website Development</option>
                                                <option value="design">Design Project</option>
                                                <option value="marketing">Marketing Campaign</option>
                                                <option value="consulting">Consulting</option>
                                                <option value="software">Software Development</option>
                                                <option value="content">Content Creation</option>
                                            </select>
                                        </div>
                                        <div class="input-group">
                                            <label>Estimated Hours</label>
                                            <input type="number" id="pricingHours" value="40" min="1" />
                                        </div>
                                        <div class="input-group">
                                            <label>Hourly Rate ($)</label>
                                            <input type="number" id="pricingRate" value="75" min="0" />
                                        </div>
                                        <div class="input-group">
                                            <label>Buffer Percentage (%)</label>
                                            <input type="number" id="pricingBuffer" value="20" min="0" max="100" />
                                        </div>
                                        <div class="input-group">
                                            <label>Revisions Included</label>
                                            <input type="number" id="pricingRevisions" value="2" min="0" />
                                        </div>
                                        <button class="btn btn-primary" onclick="calculatePricing()">
                                            <i class="fas fa-calculator"></i> Calculate Price
                                        </button>
                                    </div>
                                </div>
                            </div>

                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Results</h3>
                                </div>
                                <div class="card-content" id="pricingResults">
                                    <div class="empty-state">
                                        <i class="fas fa-calculator"></i>
                                        <h3>No results yet</h3>
                                        <p>Enter your project details and click calculate</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- HOURLY RATE -->
                    <div class="dashboard-page" id="dp-hourly-rate" style="display: none;">
                        <p style="color: var(--muted-foreground); margin-bottom: 1.5rem;">Determine your ideal hourly rate based on your income goals and expenses.</p>
                        <div class="calculator-grid">
                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Your Numbers</h3>
                                </div>
                                <div class="card-content">
                                    <div class="calculator-inputs">
                                        <div class="input-group">
                                            <label>Monthly Income Goal ($)</label>
                                            <input type="number" id="hourlyGoal" value="8000" min="0" />
                                        </div>
                                        <div class="input-group">
                                            <label>Monthly Expenses ($)</label>
                                            <input type="number" id="hourlyExpenses" value="2000" min="0" />
                                        </div>
                                        <div class="input-group">
                                            <label>Working Days per Month</label>
                                            <input type="number" id="hourlyDays" value="22" min="1" max="31" />
                                        </div>
                                        <div class="input-group">
                                            <label>Billable Hours per Day</label>
                                            <input type="number" id="hourlyBillable" value="6" min="1" max="24" />
                                        </div>
                                        <button class="btn btn-primary" onclick="calculateHourly()">
                                            <i class="fas fa-clock"></i> Calculate Rate
                                        </button>
                                    </div>
                                </div>
                            </div>

                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Your Rate</h3>
                                </div>
                                <div class="card-content" id="hourlyResults">
                                    <div class="empty-state">
                                        <i class="fas fa-clock"></i>
                                        <h3>No results yet</h3>
                                        <p>Enter your numbers and click calculate</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- REVENUE GOAL -->
                    <div class="dashboard-page" id="dp-revenue-goal" style="display: none;">
                        <p style="color: var(--muted-foreground); margin-bottom: 1.5rem;">Set monthly targets and track your progress with daily and weekly goals.</p>
                        <div class="calculator-grid">
                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Set Your Goals</h3>
                                </div>
                                <div class="card-content">
                                    <div class="calculator-inputs">
                                        <div class="input-group">
                                            <label>Monthly Revenue Goal ($)</label>
                                            <input type="number" id="revenueMonthlyGoal" value="10000" min="0" />
                                        </div>
                                        <div class="input-group">
                                            <label>Average Project Value ($)</label>
                                            <input type="number" id="revenueProjectValue" value="2500" min="0" />
                                        </div>
                                        <button class="btn btn-primary" onclick="calculateRevenue()">
                                            <i class="fas fa-bullseye"></i> Calculate Targets
                                        </button>
                                    </div>
                                </div>
                            </div>

                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Your Targets</h3>
                                </div>
                                <div class="card-content" id="revenueResults">
                                    <div class="empty-state">
                                        <i class="fas fa-bullseye"></i>
                                        <h3>No results yet</h3>
                                        <p>Enter your revenue goal and average project value</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- PROFIT CALCULATOR -->
                    <div class="dashboard-page" id="dp-profit-calculator" style="display: none;">
                        <p style="color: var(--muted-foreground); margin-bottom: 1.5rem;">Track your profit margins and understand your business expenses.</p>
                        <div class="calculator-grid">
                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Revenue & Expenses</h3>
                                </div>
                                <div class="card-content">
                                    <div class="calculator-inputs">
                                        <div class="input-group">
                                            <label>Revenue ($)</label>
                                            <input type="number" id="profitRevenue" value="50000" min="0" />
                                        </div>
                                        <div class="input-group">
                                            <label>Software Costs ($)</label>
                                            <input type="number" id="profitSoftware" value="5000" min="0" />
                                        </div>
                                        <div class="input-group">
                                            <label>Marketing Costs ($)</label>
                                            <input type="number" id="profitMarketing" value="3000" min="0" />
                                        </div>
                                        <div class="input-group">
                                            <label>Team Costs ($)</label>
                                            <input type="number" id="profitTeam" value="20000" min="0" />
                                        </div>
                                        <div class="input-group">
                                            <label>Other Costs ($)</label>
                                            <input type="number" id="profitOther" value="2000" min="0" />
                                        </div>
                                        <button class="btn btn-primary" onclick="calculateProfit()">
                                            <i class="fas fa-chart-line"></i> Calculate Profit
                                        </button>
                                    </div>
                                </div>
                            </div>

                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Profit Analysis</h3>
                                </div>
                                <div class="card-content" id="profitResults">
                                    <div class="empty-state">
                                        <i class="fas fa-chart-line"></i>
                                        <h3>No results yet</h3>
                                        <p>Enter your revenue and expenses</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- CLIENTS CRM -->
                    <div class="dashboard-page" id="dp-clients" style="display: none;">
                        <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1rem; margin-bottom: 1.5rem;">
                            <p style="color: var(--muted-foreground);">Manage your clients, track interactions, and grow your relationships.</p>
                            <button class="btn btn-primary" onclick="addClient()">
                                <i class="fas fa-user-plus"></i> Add Client
                            </button>
                        </div>

                        <div class="card">
                            <div class="card-header">
                                <div class="clients-toolbar">
                                    <div class="input-group" style="flex: 1;">
                                        <input type="text" id="clientSearch" placeholder="Search clients..." oninput="filterClients()" />
                                    </div>
                                    <select id="clientFilter" onchange="filterClients()">
                                        <option value="all">All Status</option>
                                        <option value="Lead">Lead</option>
                                        <option value="Contacted">Contacted</option>
                                        <option value="Interested">Interested</option>
                                        <option value="Meeting Scheduled">Meeting Scheduled</option>
                                        <option value="Proposal Sent">Proposal Sent</option>
                                        <option value="Won">Won</option>
                                        <option value="Lost">Lost</option>
                                    </select>
                                </div>
                            </div>
                            <div class="card-content" id="clientList">
                                <div class="empty-state">
                                    <i class="fas fa-users"></i>
                                    <h3>No clients yet</h3>
                                    <p>Start adding your first client!</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- SETTINGS -->
                    <div class="dashboard-page" id="dp-settings" style="display: none;">
                        <div class="settings-section">
                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Profile</h3>
                                </div>
                                <div class="card-content">
                                    <div class="input-group">
                                        <label>Name</label>
                                        <input type="text" id="settingsName" value="John Doe" />
                                    </div>
                                    <div class="input-group">
                                        <label>Email</label>
                                        <input type="email" id="settingsEmail" value="john@example.com" disabled style="opacity: 0.6;" />
                                        <span style="font-size: 0.75rem; color: var(--muted-foreground);">Email cannot be changed</span>
                                    </div>
                                    <button class="btn btn-primary">Update Profile</button>
                                </div>
                            </div>

                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title">Preferences</h3>
                                </div>
                                <div class="card-content">
                                    <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1rem;">
                                        <div>
                                            <p style="font-weight: 500;">Theme</p>
                                            <p style="font-size: 0.875rem; color: var(--muted-foreground);">Choose your preferred theme</p>
                                        </div>
                                        <div class="theme-options">
                                            <button class="btn btn-outline btn-sm" onclick="setTheme('light')">
                                                <i class="fas fa-sun"></i> Light
                                            </button>
                                            <button class="btn btn-outline btn-sm" onclick="setTheme('dark')">
                                                <i class="fas fa-moon"></i> Dark
                                            </button>
                                            <button class="btn btn-outline btn-sm" onclick="setTheme('system')">
                                                System
                                            </button>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <div class="card">
                                <div class="card-header">
                                    <h3 class="card-title" style="color: var(--danger);">Delete Account</h3>
                                </div>
                                <div class="card-content">
                                    <p style="font-size: 0.875rem; color: var(--muted-foreground); margin-bottom: 1rem;">
                                        Permanently delete your account and all associated data. This action cannot be undone.
                                    </p>
                                    <button class="btn btn-danger" onclick="deleteAccount()">Delete Account</button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- ADMIN -->
                    <div class="dashboard-page" id="dp-admin" style="display: none;">
                        <p style="color: var(--muted-foreground); margin-bottom: 1.5rem;">Overview of your platform's performance.</p>
                        <div class="stats-grid">
                            <div class="stat-card">
                                <div class="stat-card-header">
                                    <span>Total Users</span>
                                    <i class="fas fa-users" style="color: var(--primary);"></i>
                                </div>
                                <div class="stat-card-value" id="adminUsers">0</div>
                                <div class="stat-card-change">Registered users</div>
                            </div>
                            <div class="stat-card">
                                <div class="stat-card-header">
                                    <span>Total Clients</span>
                                    <i class="fas fa-user-friends" style="color: var(--success);"></i>
                                </div>
                                <div class="stat-card-value" id="adminClients">0</div>
                                <div class="stat-card-change">All clients</div>
                            </div>
                            <div class="stat-card">
                                <div class="stat-card-header">
                                    <span>Total Proposals</span>
                                    <i class="fas fa-file-alt" style="color: var(--warning);"></i>
                                </div>
                                <div class="stat-card-value" id="adminProposals">0</div>
                                <div class="stat-card-change">Proposals created</div>
                            </div>
                            <div class="stat-card">
                                <div class="stat-card-header">
                                    <span>Total Revenue</span>
                                    <i class="fas fa-dollar-sign" style="color: var(--primary);"></i>
                                </div>
                                <div class="stat-card-value" id="adminRevenue">$0</div>
                                <div class="stat-card-change">All time</div>
                            </div>
                        </div>
                    </div>
                </div>
            </main>
        </div>
    </div>

    <!-- ============================================
    JAVASCRIPT
    ============================================ -->
    <script>
        // ============================================
        // STATE
        // ============================================
        const state = {
            theme: 'light',
            clients: [
                { id: 1, name: 'Acme Corp', email: 'contact@acme.com', company: 'Acme Corp', service: 'Web Development',
                    status: 'Won', notes: 'Signed contract' },
                { id: 2, name: 'Beta Inc', email: 'info@beta.com', company: 'Beta Inc', service: 'Marketing',
                    status: 'Lead', notes: 'Initial contact made' },
                { id: 3, name: 'Gamma LLC', email: 'hello@gamma.com', company: 'Gamma LLC', service: 'Design',
                    status: 'Proposal Sent', notes: 'Proposal sent on Friday' },
            ],
            clientIdCounter: 4,
            pricingResults: null,
            hourlyResults: null,
            revenueResults: null,
            profitResults: null,
            dashboardPage: 'dashboard',
        };

        // ============================================
        // THEME
        // ============================================
        function getPreferredTheme() {
            const saved = localStorage.getItem('prezzo-theme');
            if (saved) return saved;
            return window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light';
        }

        function applyTheme(theme) {
            state.theme = theme;
            document.documentElement.setAttribute('data-theme', theme === 'dark' ? 'dark' : '');
            localStorage.setItem('prezzo-theme', theme);

            const icon = document.getElementById('themeIcon');
            const dashIcon = document.getElementById('dashboardThemeIcon');
            if (icon) icon.className = theme === 'dark' ? 'fas fa-sun' : 'fas fa-moon';
            if (dashIcon) dashIcon.className = theme === 'dark' ? 'fas fa-sun' : 'fas fa-moon';
        }

        function toggleTheme() {
            applyTheme(state.theme === 'dark' ? 'light' : 'dark');
        }

        function setTheme(theme) {
            applyTheme(theme);
        }

        // Initialize theme
        applyTheme(getPreferredTheme());

        // ============================================
        // PAGE NAVIGATION
        // ============================================
        function showPage(page) {
            document.querySelectorAll('.page').forEach(el => el.style.display = 'none');
            const target = document.getElementById(`page-${page}`);
            if (target) {
                target.style.display = page === 'login' || page === 'signup' || page === 'forgot-password' ? 'flex' :
                'block';
                if (page === 'dashboard') {
                    target.style.display = 'block';
                    initDashboard();
                }
            }
            // Close mobile menu
            closeMobileMenu();
            // Scroll to top
            window.scrollTo(0, 0);
        }

        // ============================================
        // MOBILE MENU
        // ============================================
        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            const overlay = document.getElementById('overlay');
            menu.classList.toggle('open');
            overlay.classList.toggle('show');
        }

        function closeMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            const overlay = document.getElementById('overlay');
            menu.classList.remove('open');
            overlay.classList.remove('show');
        }

        // ============================================
        // SIDEBAR
        // ============================================
        function toggleSidebar() {
            const sidebar = document.getElementById('sidebar');
            const overlay = document.getElementById('sidebarOverlay');
            sidebar.classList.toggle('open');
            overlay.classList.toggle('show');
        }

        function closeSidebar() {
            const sidebar = document.getElementById('sidebar');
            const overlay = document.getElementById('sidebarOverlay');
            sidebar.classList.remove('open');
            overlay.classList.remove('show');
        }

        // ============================================
        // DASHBOARD
        // ============================================
        function initDashboard() {
            // Show sidebar toggle on mobile
            const toggle = document.getElementById('sidebarToggle');
            if (window.innerWidth <= 768) {
                toggle.style.display = 'block';
            } else {
                toggle.style.display = 'none';
                closeSidebar();
            }
            // Update stats
            updateStats();
            updateAdminStats();
            renderClients();
        }

        function updateStats() {
            const total = state.clients.length;
            const leads = state.clients.filter(c => c.status === 'Lead' || c.status === 'Contacted').length;
            const won = state.clients.filter(c => c.status === 'Won').length;
            const proposals = state.clients.filter(c => c.status === 'Proposal Sent').length;

            document.getElementById('statClients').textContent = total;
            document.getElementById('statLeads').textContent = leads;
            document.getElementById('statRevenue').textContent = `$${Math.round(total * 2500).toLocaleString()}`;
            document.getElementById('statProposals').textContent = proposals;
        }

        function updateAdminStats() {
            const total = state.clients.length;
            document.getElementById('adminUsers').textContent = '1';
            document.getElementById('adminClients').textContent = total;
            document.getElementById('adminProposals').textContent = total;
            document.getElementById('adminRevenue').textContent = `$${(total * 2500).toLocaleString()}`;
        }

        function showDashboardPage(page) {
            state.dashboardPage = page;

            // Update sidebar
            document.querySelectorAll('.sidebar-nav a').forEach(el => el.classList.remove('active'));
            document.querySelector(`.sidebar-nav a[data-page="${page}"]`)?.classList.add('active');

            // Update content
            document.querySelectorAll('.dashboard-page').forEach(el => el.style.display = 'none');
            const target = document.getElementById(`dp-${page}`);
            if (target) target.style.display = 'block';

            // Update header
            const titles = {
                'dashboard': ['Dashboard', 'Welcome back! Here\'s an overview of your business.'],
                'pricing-calculator': ['Pricing Calculator',
                    'Calculate profitable project pricing with buffer and premium packages.'
                ],
                'hourly-rate': ['Hourly Rate', 'Determine your ideal hourly rate based on your income goals and expenses.'],
                'revenue-goal': ['Revenue Goal', 'Set monthly targets and track your progress with daily and weekly goals.'],
                'profit-calculator': ['Profit Calculator', 'Track your profit margins and understand your business expenses.'],
                'clients': ['Client CRM', 'Manage your clients, track interactions, and grow your relationships.'],
                'settings': ['Settings', 'Manage your account settings and preferences.'],
                'admin': ['Admin Panel', 'Overview of your platform\'s performance.'],
            };
            const [title, subtitle] = titles[page] || ['Page', ''];
            document.getElementById('dashboardTitle').textContent = title;
            document.getElementById('dashboardSubtitle').textContent = subtitle;

            // Close sidebar on mobile
            if (window.innerWidth <= 768) closeSidebar();

            // Scroll to top
            document.querySelector('.dashboard-main').scrollTop = 0;
        }

        // ============================================
        // PRICING CALCULATOR
        // ============================================
        function calculatePricing() {
            const hours = parseFloat(document.getElementById('pricingHours').value) || 0;
            const rate = parseFloat(document.getElementById('pricingRate').value) || 0;
            const buffer = parseFloat(document.getElementById('pricingBuffer').value) || 0;
            const revisions = parseInt(document.getElementById('pricingRevisions').value) || 0;

            const basePrice = hours * rate;
            const bufferCost = basePrice * (buffer / 100);
            const recommendedPrice = basePrice + bufferCost;
            const premiumPrice = recommendedPrice * 1.25;

            state.pricingResults = { basePrice, bufferCost, recommendedPrice, premiumPrice };

            const container = document.getElementById('pricingResults');
            container.innerHTML = `
                        <div class="calculator-result">
                            <div class="result-item">
                                <div class="label">Base Price</div>
                                <div class="value">$${basePrice.toLocaleString()}</div>
                            </div>
                            <div class="result-item warning">
                                <div class="label">Buffer Cost (${buffer}%)</div>
                                <div class="value">$${bufferCost.toLocaleString()}</div>
                            </div>
                            <div class="result-item primary">
                                <div class="label">Recommended Price</div>
                                <div class="value">$${recommendedPrice.toLocaleString()}</div>
                            </div>
                            <div class="result-item success">
                                <div class="label">Premium Package</div>
                                <div class="value">$${premiumPrice.toLocaleString()}</div>
                                <div style="font-size: 0.75rem; color: var(--muted-foreground);">Includes express delivery and additional revisions</div>
                            </div>
                            <div class="result-actions">
                                <button class="btn btn-outline" onclick="saveCalculation('pricing')">
                                    <i class="fas fa-save"></i> Save
                                </button>
                                <button class="btn btn-outline">
                                    <i class="fas fa-download"></i> Export
                                </button>
                            </div>
                        </div>
                    `;
        }

        // ============================================
        // HOURLY RATE CALCULATOR
        // ============================================
        function calculateHourly() {
            const goal = parseFloat(document.getElementById('hourlyGoal').value) || 0;
            const expenses = parseFloat(document.getElementById('hourlyExpenses').value) || 0;
            const days = parseFloat(document.getElementById('hourlyDays').value) || 1;
            const billable = parseFloat(document.getElementById('hourlyBillable').value) || 1;

            const hourlyRate = (goal + expenses) / (days * billable);
            const monthlyCapacity = days * billable * hourlyRate;
            const annualProjection = monthlyCapacity * 12;

            state.hourlyResults = { hourlyRate, monthlyCapacity, annualProjection };

            const container = document.getElementById('hourlyResults');
            container.innerHTML = `
                        <div class="calculator-result">
                            <div class="result-item primary">
                                <div class="label">Recommended Hourly Rate</div>
                                <div class="value">$${hourlyRate.toFixed(2)}</div>
                            </div>
                            <div class="result-item">
                                <div class="label">Monthly Capacity</div>
                                <div class="value">$${Math.round(monthlyCapacity).toLocaleString()}</div>
                            </div>
                            <div class="result-item success">
                                <div class="label">Annual Projection</div>
                                <div class="value">$${Math.round(annualProjection).toLocaleString()}</div>
                            </div>
                            <div class="result-actions">
                                <button class="btn btn-outline" onclick="saveCalculation('hourly')">
                                    <i class="fas fa-save"></i> Save
                                </button>
                            </div>
                        </div>
                    `;
        }

        // ============================================
        // REVENUE GOAL CALCULATOR
        // ============================================
        function calculateRevenue() {
            const monthlyGoal = parseFloat(document.getElementById('revenueMonthlyGoal').value) || 0;
            const projectValue = parseFloat(document.getElementById('revenueProjectValue').value) || 1;

            const projectsNeeded = Math.ceil(monthlyGoal / projectValue);
            const weeklyTarget = monthlyGoal / 4;
            const dailyTarget = monthlyGoal / 20;

            state.revenueResults = { projectsNeeded, weeklyTarget, dailyTarget };

            const container = document.getElementById('revenueResults');
            container.innerHTML = `
                        <div class="calculator-result">
                            <div class="result-item primary">
                                <div class="label">Projects Needed</div>
                                <div class="value">${projectsNeeded}</div>
                                <div style="font-size: 0.75rem; color: var(--muted-foreground);">projects per month to reach your goal</div>
                            </div>
                            <div class="result-item warning">
                                <div class="label">Weekly Target</div>
                                <div class="value">$${Math.round(weeklyTarget).toLocaleString()}</div>
                            </div>
                            <div class="result-item success">
                                <div class="label">Daily Target</div>
                                <div class="value">$${Math.round(dailyTarget).toLocaleString()}</div>
                            </div>
                            <div class="result-actions">
                                <button class="btn btn-outline" onclick="saveCalculation('revenue')">
                                    <i class="fas fa-save"></i> Save Goal
                                </button>
                            </div>
                        </div>
                    `;
        }

        // ============================================
        // PROFIT CALCULATOR
        // ============================================
        function calculateProfit() {
            const revenue = parseFloat(document.getElementById('profitRevenue').value) || 0;
            const software = parseFloat(document.getElementById('profitSoftware').value) || 0;
            const marketing = parseFloat(document.getElementById('profitMarketing').value) || 0;
            const team = parseFloat(document.getElementById('profitTeam').value) || 0;
            const other = parseFloat(document.getElementById('profitOther').value) || 0;

            const totalExpenses = software + marketing + team + other;
            const profit = revenue - totalExpenses;
            const profitMargin = revenue > 0 ? (profit / revenue) * 100 : 0;

            state.profitResults = { totalExpenses, profit, profitMargin };

            const container = document.getElementById('profitResults');
            const isProfit = profit >= 0;
            container.innerHTML = `
                        <div class="calculator-result">
                            <div class="result-item">
                                <div class="label">Total Expenses</div>
                                <div class="value">$${totalExpenses.toLocaleString()}</div>
                            </div>
                            <div class="result-item ${isProfit ? 'success' : 'warning'}" style="${!isProfit ? 'background: #fee2e2;' : ''}">
                                <div class="label">Profit</div>
                                <div class="value" style="color: ${isProfit ? 'var(--success)' : 'var(--danger)'};">$${profit.toLocaleString()}</div>
                            </div>
                            <div class="result-item primary">
                                <div class="label">Profit Margin</div>
                                <div class="value">${profitMargin.toFixed(1)}%</div>
                                <div style="font-size: 0.75rem; color: var(--muted-foreground);">
                                    ${profitMargin >= 30 ? 'Healthy margin! 🎉' : profitMargin >= 20 ? 'Good margin 💪' : 'Consider optimizing costs 💡'}
                                </div>
                            </div>
                            <div class="result-actions">
                                <button class="btn btn-outline" onclick="saveCalculation('profit')">
                                    <i class="fas fa-save"></i> Save
                                </button>
                            </div>
                        </div>
                    `;
        }

        // ============================================
        // SAVE CALCULATION
        // ============================================
        function saveCalculation(type) {
            let name = '';
            let data = {};

            switch (type) {
                case 'pricing':
                    name = 'Pricing Calculation';
                    data = state.pricingResults;
                    break;
                case 'hourly':
                    name = 'Hourly Rate Calculation';
                    data = state.hourlyResults;
                    break;
                case 'revenue':
                    name = 'Revenue Goal';
                    data = state.revenueResults;
                    break;
                case 'profit':
                    name = 'Profit Calculation';
                    data = state.profitResults;
                    break;
            }

            showNotification(`${name} saved successfully! ✅`);
        }

        // ============================================
        // CLIENTS CRM
        // ============================================
        function renderClients() {
            const search = document.getElementById('clientSearch')?.value?.toLowerCase() || '';
            const filter = document.getElementById('clientFilter')?.value || 'all';

            let filtered = state.clients.filter(c => {
                const matchSearch = c.name.toLowerCase().includes(search) ||
                    c.email.toLowerCase().includes(search) ||
                    c.company.toLowerCase().includes(search);
                const matchFilter = filter === 'all' || c.status === filter;
                return matchSearch && matchFilter;
            });

            const container = document.getElementById('clientList');
            if (filtered.length === 0) {
                container.innerHTML = `
                            <div class="empty-state">
                                <i class="fas fa-users"></i>
                                <h3>No clients found</h3>
                                <p>${search ? 'Try adjusting your search' : 'Start adding your first client!'}</p>
                            </div>
                        `;
                return;
            }

            container.innerHTML = filtered.map(c => `
                        <div class="client-item">
                            <div class="client-info">
                                <h4>${c.name}</h4>
                                <div class="details">
                                    ${c.email} • ${c.company} • ${c.service}
                                </div>
                                <div style="margin-top: 0.25rem;">
                                    <span class="badge ${getStatusBadge(c.status)}">${c.status}</span>
                                    ${c.notes ? `<span style="font-size: 0.75rem; color: var(--muted-foreground); margin-left: 0.5rem;">${c.notes}</span>` : ''}
                                </div>
                            </div>
                            <div class="client-actions">
                                <button class="btn btn-ghost btn-sm" onclick="editClient(${c.id})">
                                    <i class="fas fa-edit"></i>
                                </button>
                                <button class="btn btn-ghost btn-sm" style="color: var(--danger);" onclick="deleteClient(${c.id})">
                                    <i class="fas fa-trash"></i>
                                </button>
                            </div>
                        </div>
                    `).join('');
        }

        function getStatusBadge(status) {
            const map = {
                'Lead': 'badge-secondary',
                'Contacted': 'badge-warning',
                'Interested': 'badge-primary',
                'Meeting Scheduled': 'badge-primary',
                'Proposal Sent': 'badge-primary',
                'Won': 'badge-success',
                'Lost': 'badge-danger',
            };
            return map[status] || 'badge-secondary';
        }

        function filterClients() {
            renderClients();
        }

        function addClient() {
            const name = prompt('Client name:');
            if (!name) return;
            const email = prompt('Email:') || '';
            const company = prompt('Company:') || '';
            const service = prompt('Service:') || '';
            const status = prompt('Status (Lead/Contacted/Interested/Meeting Scheduled/Proposal Sent/Won/Lost):') || 'Lead';

            state.clients.push({
                id: state.clientIdCounter++,
                name,
                email,
                company,
                service,
                status,
                notes: '',
            });

            renderClients();
            updateStats();
            updateAdminStats();
            showNotification('Client added successfully! ✅');
        }

        function deleteClient(id) {
            if (!confirm('Are you sure you want to delete this client?')) return;
            state.clients = state.clients.filter(c => c.id !== id);
            renderClients();
            updateStats();
            updateAdminStats();
            showNotification('Client deleted.');
        }

        function editClient(id) {
            const client = state.clients.find(c => c.id === id);
            if (!client) return;
            const name = prompt('Name:', client.name);
            if (name) client.name = name;
            const status = prompt('Status (Lead/Contacted/Interested/Meeting Scheduled/Proposal Sent/Won/Lost):', client.status);
            if (status) client.status = status;
            renderClients();
            updateStats();
        }

        // ============================================
        // AUTH HANDLERS
        // ============================================
        function handleLogin(e) {
            e.preventDefault();
            const email = document.getElementById('loginEmail').value;
            const password = document.getElementById('loginPassword').value;

            if (email && password.length >= 6) {
                showNotification('Login successful! Welcome back! 🎉');
                showPage('dashboard');
            } else {
                showNotification('Please enter valid credentials.', 'error');
            }
        }

        function handleSignup(e) {
            e.preventDefault();
            const name = document.getElementById('signupName').value;
            const email = document.getElementById('signupEmail').value;
            const password = document.getElementById('signupPassword').value;

            if (name && email && password.length >= 6) {
                showNotification('Account created successfully! 🎉');
                showPage('dashboard');
            } else {
                showNotification('Please fill in all fields correctly.', 'error');
            }
        }

        function handleResetPassword(e) {
            e.preventDefault();
            const email = document.getElementById('resetEmail').value;
            if (email) {
                showNotification('Password reset instructions sent to your email! 📧');
                showPage('login');
            }
        }

        function handleGoogleLogin() {
            showNotification('Google authentication coming soon! 🔜');
        }

        function handleLogout() {
            if (confirm('Are you sure you want to logout?')) {
                showNotification('Logged out successfully.');
                showPage('landing');
            }
        }

        function deleteAccount() {
            if (confirm('Are you sure you want to delete your account? This action cannot be undone.')) {
                showNotification('Account deleted.');
                showPage('landing');
            }
        }

        // ============================================
        // FAQ
        // ============================================
        function toggleFAQ(button) {
            const answer = button.nextElementSibling;
            const isOpen = answer.classList.contains('open');

            // Close all
            document.querySelectorAll('.faq-answer').forEach(el => el.classList.remove('open'));
            document.querySelectorAll('.faq-question').forEach(el => el.classList.remove('active'));

            if (!isOpen) {
                answer.classList.add('open');
                button.classList.add('active');
            }
        }

        // ============================================
        // NOTIFICATIONS
        // ============================================
        function showNotification(message, type = 'success') {
            const notification = document.getElementById('notification');
            const messageEl = document.getElementById('notificationMessage');
            messageEl.textContent = message;
            notification.className = `notification ${type}`;
            notification.classList.add('show');

            setTimeout(() => {
                notification.classList.remove('show');
            }, 3000);
        }

        // ============================================
        // WINDOW RESIZE HANDLER
        // ============================================
        window.addEventListener('resize', () => {
            const toggle = document.getElementById('sidebarToggle');
            if (window.innerWidth <= 768) {
                toggle.style.display = 'block';
            } else {
                toggle.style.display = 'none';
                closeSidebar();
            }
        });

        // ============================================
        // KEYBOARD SHORTCUTS
        // ============================================
        document.addEventListener('keydown', (e) => {
            // Escape to close modals/menus
            if (e.key === 'Escape') {
                closeMobileMenu();
                closeSidebar();
            }
        });

        // ============================================
        // INITIALIZATION
        // ============================================
        console.log('🚀 Prezzo loaded successfully!');
        console.log('📊 ' + state.clients.length + ' clients loaded');
    </script>

</body>
</html>
