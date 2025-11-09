<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fuel Corner - Fuel Delivery Service in India</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <style>
        /* Global Styles */
        :root {
            --primary: #FF6B35;
            --secondary: #004E89;
            --accent: #FFC800;
            --light: #F8F9FA;
            --dark: #212529;
            --gray: #6C757D;
            --success: #28A745;
            --white: #FFFFFF;
            --black: #000000;
            --text-dark: #1A1A1A;
            --text-light: #666666;
            --background: #F7F7F7;
            --card-shadow: 0 8px 30px rgba(0, 0, 0, 0.08);
            --hover-shadow: 0 15px 40px rgba(0, 0, 0, 0.12);
            --gradient-primary: linear-gradient(135deg, var(--primary), #e55a2b);
            --gradient-secondary: linear-gradient(135deg, var(--secondary), #003d6d);
            --gradient-accent: linear-gradient(135deg, var(--accent), #e6b400);
            --ease-out-quad: cubic-bezier(0.25, 0.46, 0.45, 0.94);
            --ease-out-expo: cubic-bezier(0.19, 1, 0.22, 1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            line-height: 1.6;
            color: var(--text-dark);
            background-color: var(--white);
            overflow-x: hidden;
            font-weight: 500;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 14px 28px;
            background: var(--gradient-primary);
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.4s var(--ease-out-quad);
            box-shadow: 0 4px 15px rgba(255, 107, 53, 0.3);
            font-size: 16px;
            gap: 8px;
            position: relative;
            overflow: hidden;
            transform: translateY(0);
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: left 0.5s;
        }
        
        .btn:hover::before {
            left: 100%;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 107, 53, 0.4);
        }
        
        .btn-secondary {
            background: var(--gradient-secondary);
            box-shadow: 0 4px 15px rgba(0, 78, 137, 0.3);
        }
        
        .btn-secondary:hover {
            box-shadow: 0 8px 25px rgba(0, 78, 137, 0.4);
        }
        
        .btn-accent {
            background: var(--gradient-accent);
            color: var(--dark);
            box-shadow: 0 4px 15px rgba(255, 200, 0, 0.3);
        }
        
        .btn-accent:hover {
            box-shadow: 0 8px 25px rgba(255, 200, 0, 0.4);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
            box-shadow: none;
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: white;
        }
        
        section {
            padding: 100px 0;
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s var(--ease-out-expo);
        }
        
        section.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        h1, h2, h3, h4 {
            margin-bottom: 1rem;
            line-height: 1.2;
            font-weight: 800;
        }
        
        h1 {
            font-size: 3.5rem;
            font-weight: 900;
        }
        
        h2 {
            font-size: 2.8rem;
            font-weight: 800;
        }
        
        h3 {
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        h4 {
            font-size: 1.4rem;
            font-weight: 700;
        }
        
        p {
            font-size: 1.1rem;
            color: var(--text-light);
            margin-bottom: 1.5rem;
            font-weight: 500;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 70px;
        }
        
        .section-title h2 {
            font-size: 2.8rem;
            color: var(--text-dark);
            position: relative;
            display: inline-block;
            font-weight: 800;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--gradient-primary);
            border-radius: 2px;
        }
        
        .section-title p {
            max-width: 700px;
            margin: 30px auto 0;
            font-size: 1.2rem;
            font-weight: 500;
        }
        
        /* Apple-style Glow Media Wrapper */
        .glow-media-wrapper {
            position: relative;
            overflow: hidden;
            border-radius: 20px;
            margin: 60px 0;
        }
        
        .glow-media-container {
            position: relative;
            border-radius: 18px;
            overflow: hidden;
            background: var(--white);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.08);
        }
        
        .glow-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, 
                rgba(255, 107, 53, 0.1) 0%, 
                rgba(0, 78, 137, 0.15) 50%, 
                rgba(255, 200, 0, 0.1) 100%);
            opacity: 0;
            transition: opacity 1.2s var(--ease-out-expo);
            z-index: 1;
        }
        
        .glow-media-container.visible .glow-background {
            opacity: 1;
        }
        
        .glow-content {
            position: relative;
            z-index: 2;
            padding: 60px;
            text-align: center;
        }
        
        /* Enhanced section with glow effect */
        .glow-section {
            position: relative;
            overflow: hidden;
        }
        
        .glow-section::before {
            content: '';
            position: absolute;
            top: -100px;
            left: -100px;
            right: -100px;
            height: 300px;
            background: linear-gradient(135deg, 
                rgba(255, 107, 53, 0.03) 0%, 
                rgba(0, 78, 137, 0.05) 50%, 
                rgba(255, 200, 0, 0.03) 100%);
            filter: blur(60px);
            opacity: 0;
            transition: opacity 1.5s var(--ease-out-expo);
            z-index: 0;
        }
        
        .glow-section.visible::before {
            opacity: 1;
        }
        
        /* Header Styles */
        header {
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.08);
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            transition: all 0.6s var(--ease-out-expo);
            transform: translateY(0);
        }
        
        header.scrolled {
            padding: 5px 0;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            background-color: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(30px);
            -webkit-backdrop-filter: blur(30px);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
            min-height: 80px;
            transition: all 0.3s ease;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .logo-icon {
            width: 45px;
            height: 45px;
            background: var(--gradient-primary);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.3rem;
            box-shadow: 0 4px 10px rgba(255, 107, 53, 0.3);
        }
        
        .logo-text {
            display: flex;
            flex-direction: column;
        }
        
        .logo-text h1 {
            font-size: 1.8rem;
            color: var(--text-dark);
            margin-bottom: 0;
            font-weight: 900;
        }
        
        .logo-text span {
            background: var(--gradient-primary);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .tagline {
            font-size: 0.8rem;
            color: var(--gray);
            margin-top: -5px;
            font-weight: 500;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            align-items: center;
            gap: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            transition: color 0.3s ease;
            position: relative;
            font-size: 1rem;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--gradient-primary);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--secondary);
            z-index: 1001;
        }
        
        /* Page Content Styles */
        .page {
            display: none;
            animation: fadeIn 0.5s ease-in;
        }
        
        .page.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Vector Image Containers */
        .vector-container {
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .vector-image {
            max-width: 100%;
            height: auto;
            filter: drop-shadow(0 10px 20px rgba(0,0,0,0.1));
            transition: all 0.6s var(--ease-out-quad);
        }
        
        .vector-image:hover {
            transform: scale(1.05);
        }
        
        /* Hero Vector */
        .hero-vector {
            position: absolute;
            right: 10%;
            bottom: 0;
            width: 500px;
            height: 400px;
            opacity: 0.9;
        }
        
        /* Service Vectors */
        .service-vector {
            width: 120px;
            height: 120px;
            margin-bottom: 20px;
        }
        
        /* Feature Vectors */
        .feature-vector {
            width: 200px;
            height: 200px;
            margin: 0 auto 30px;
        }
        
        /* App Vector */
        .app-vector {
            width: 300px;
            height: 300px;
            margin: 0 auto;
        }
        
        /* Calculator Vector */
        .calculator-vector {
            width: 250px;
            height: 250px;
            margin: 0 auto 30px;
        }
        
        /* Team Vectors */
        .team-vector {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin-bottom: 20px;
        }
        
        /* Updated Hero Section for Vector */
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: left;
            position: relative;
            z-index: 2;
        }
        
        /* Vector Animation */
        @keyframes float {
            0%, 100% { 
                transform: translateY(0px) rotate(0deg); 
            }
            50% { 
                transform: translateY(-20px) rotate(2deg); 
            }
        }
        
        .floating {
            animation: float 6s var(--ease-out-quad) infinite;
        }
        
        /* Updated Service Icons to use Vectors */
        .service-icon {
            height: 200px;
            background: transparent;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: visible;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, rgba(0,78,137,0.85), rgba(255,107,53,0.85)), url('https://images.unsplash.com/photo-1563720223485-854d2637f6e1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            padding: 180px 0 120px;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 100px;
            background: linear-gradient(to top, var(--white), transparent);
        }
        
        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            font-weight: 900;
            text-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }
        
        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 2.5rem;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 500;
        }
        
        .hero-buttons {
            display: flex;
            justify-content: flex-start;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        /* Services Section */
        .services {
            background-color: var(--white);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background-color: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            transition: all 0.5s var(--ease-out-quad);
            position: relative;
            height: 100%;
            display: flex;
            flex-direction: column;
            transform: translateY(0) scale(1);
            opacity: 1;
            animation: fadeInUp 0.8s var(--ease-out-expo) both;
        }
        
        .service-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: var(--hover-shadow);
        }
        
        .service-card:hover .vector-image {
            transform: scale(1.1) rotate(5deg);
        }
        
        .service-card:nth-child(1) { animation-delay: 0.1s; }
        .service-card:nth-child(2) { animation-delay: 0.2s; }
        .service-card:nth-child(3) { animation-delay: 0.3s; }
        .service-card:nth-child(4) { animation-delay: 0.4s; }
        .service-card:nth-child(5) { animation-delay: 0.5s; }
        .service-card:nth-child(6) { animation-delay: 0.6s; }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .service-content {
            padding: 30px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
        
        .service-content h3 {
            color: var(--text-dark);
            margin-bottom: 15px;
            font-size: 1.5rem;
            font-weight: 700;
        }
        
        .service-features {
            list-style: none;
            margin: 15px 0;
            flex-grow: 1;
        }
        
        .service-features li {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            font-weight: 500;
        }
        
        .service-features i {
            color: var(--success);
            margin-right: 10px;
            font-size: 0.9rem;
        }
        
        .service-card .btn {
            margin-top: auto;
            align-self: flex-start;
        }
        
        /* How It Works */
        .how-it-works {
            background-color: var(--background);
            position: relative;
        }
        
        .how-it-works::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1558618047-3c8c76ca7d13?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
            opacity: 0.05;
            z-index: 0;
        }
        
        .how-it-works .container {
            position: relative;
            z-index: 1;
        }
        
        .steps {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-top: 50px;
        }
        
        .step {
            flex: 1;
            min-width: 220px;
            text-align: center;
            padding: 0 20px;
            margin-bottom: 30px;
            position: relative;
        }
        
        .step:not(:last-child)::after {
            content: '';
            position: absolute;
            top: 40px;
            right: 0;
            width: 50%;
            height: 2px;
            background: linear-gradient(to right, var(--primary), transparent);
            z-index: 1;
        }
        
        .step-number {
            width: 80px;
            height: 80px;
            background: var(--gradient-primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            font-weight: 800;
            margin: 0 auto 25px;
            position: relative;
            z-index: 2;
            box-shadow: 0 8px 20px rgba(255, 107, 53, 0.3);
        }
        
        .step h3 {
            color: var(--text-dark);
            margin-bottom: 15px;
            font-size: 1.3rem;
            font-weight: 700;
        }
        
        .step p {
            font-size: 1rem;
            font-weight: 500;
        }
        
        /* App Download */
        .app-download {
            background: var(--gradient-secondary);
            color: white;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .app-download::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
            opacity: 0.1;
            z-index: 0;
        }
        
        .app-download .container {
            position: relative;
            z-index: 1;
        }
        
        .app-download h2 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            font-weight: 800;
        }
        
        .app-download p {
            max-width: 600px;
            margin: 0 auto 30px;
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 500;
        }
        
        .app-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .app-btn {
            display: flex;
            align-items: center;
            background-color: white;
            color: var(--dark);
            padding: 15px 25px;
            border-radius: 12px;
            text-decoration: none;
            font-weight: 700;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }
        
        .app-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
        }
        
        .app-btn i {
            font-size: 2rem;
            margin-right: 12px;
        }
        
        /* Enhanced Fuel Calculator */
        .calculator {
            background-color: var(--white);
        }
        
        .calculator-container {
            max-width: 900px;
            margin: 0 auto;
            background-color: var(--white);
            padding: 40px;
            border-radius: 20px;
            box-shadow: var(--card-shadow);
        }
        
        .calculator-header {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .calculator-header h3 {
            font-size: 1.8rem;
            color: var(--text-dark);
            font-weight: 700;
        }
        
        .calculator-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 30px;
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 600;
            color: var(--text-dark);
        }
        
        .form-control {
            width: 100%;
            padding: 15px;
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            font-size: 1rem;
            transition: border 0.3s ease, box-shadow 0.3s ease;
            font-weight: 500;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(255, 107, 53, 0.2);
        }
        
        .calculator-results {
            background: var(--gradient-secondary);
            color: white;
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
            margin-top: 30px;
            display: none;
        }
        
        .result-item {
            display: flex;
            justify-content: space-between;
            padding: 12px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
            font-weight: 500;
        }
        
        .result-item.total {
            font-weight: 700;
            font-size: 1.3rem;
            color: var(--accent);
            border-bottom: none;
            margin-top: 10px;
        }
        
        /* Original Calculator */
        .original-calculator {
            background-color: var(--background);
            margin-top: 50px;
        }
        
        .original-calculator-container {
            max-width: 600px;
            margin: 0 auto;
            background-color: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: var(--card-shadow);
        }
        
        .result {
            margin-top: 20px;
            padding: 20px;
            background: var(--gradient-secondary);
            color: white;
            border-radius: 12px;
            text-align: center;
            display: none;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }
        
        /* Live Service Status */
        .live-status {
            background-color: var(--white);
        }
        
        .status-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }
        
        .status-card {
            background: white;
            padding: 30px;
            border-radius: 16px;
            box-shadow: var(--card-shadow);
            text-align: center;
            position: relative;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .status-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--hover-shadow);
        }
        
        .status-indicator {
            width: 14px;
            height: 14px;
            border-radius: 50%;
            position: absolute;
            top: 20px;
            right: 20px;
        }
        
        .status-card.online .status-indicator {
            background-color: var(--success);
            box-shadow: 0 0 10px var(--success);
        }
        
        .status-card.busy .status-indicator {
            background-color: var(--accent);
            box-shadow: 0 0 10px var(--accent);
        }
        
        .wait-time {
            display: inline-block;
            margin-top: 15px;
            padding: 8px 16px;
            background: var(--light);
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
        }
        
        /* Trust Badges */
        .trust-badges {
            background: var(--gradient-secondary);
            color: white;
            padding: 80px 0;
            position: relative;
            overflow: hidden;
        }
        
        .trust-badges::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1558618047-3c8c76ca7d13?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
            opacity: 0.05;
            z-index: 0;
        }
        
        .trust-badges .container {
            position: relative;
            z-index: 1;
        }
        
        .badges-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 40px;
        }
        
        .badge {
            text-align: center;
            padding: 20px;
        }
        
        .badge i {
            font-size: 3rem;
            margin-bottom: 20px;
            color: var(--accent);
        }
        
        .badge span {
            display: block;
            font-weight: 700;
            font-size: 1.1rem;
        }
        
        /* Enhanced Testimonials */
        .testimonials {
            background-color: var(--white);
        }
        
        .testimonial-carousel {
            position: relative;
            max-width: 900px;
            margin: 0 auto;
            overflow: hidden;
        }
        
        .testimonial-slide {
            display: none;
            padding: 30px;
        }
        
        .testimonial-slide.active {
            display: block;
            animation: fadeIn 0.5s ease-in;
        }
        
        .testimonial-content {
            background: var(--white);
            padding: 40px;
            border-radius: 20px;
            text-align: center;
            position: relative;
            box-shadow: var(--card-shadow);
        }
        
        .testimonial-content::before {
            content: '"';
            position: absolute;
            top: 10px;
            left: 20px;
            font-size: 5rem;
            color: var(--primary);
            opacity: 0.2;
            font-family: Georgia, serif;
        }
        
        .rating {
            color: var(--accent);
            font-size: 1.3rem;
            margin-bottom: 20px;
        }
        
        .customer-info {
            margin-top: 25px;
        }
        
        .customer-info strong {
            display: block;
            color: var(--secondary);
            font-size: 1.1rem;
            font-weight: 700;
        }
        
        .customer-info span {
            font-weight: 500;
        }
        
        .carousel-controls {
            display: flex;
            justify-content: center;
            margin-top: 30px;
            gap: 10px;
        }
        
        .carousel-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #ddd;
            cursor: pointer;
            transition: background 0.3s ease, transform 0.3s ease;
        }
        
        .carousel-dot.active {
            background: var(--primary);
            transform: scale(1.2);
        }
        
        /* Coverage */
        .coverage {
            background-color: var(--background);
        }
        
        .cities {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 40px;
        }
        
        .city {
            background-color: white;
            padding: 12px 24px;
            border-radius: 30px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
            font-weight: 600;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .city:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.12);
        }
        
        /* About Page Styles */
        .about-hero {
            background: linear-gradient(135deg, rgba(0,78,137,0.9), rgba(255,107,53,0.9)), url('https://images.unsplash.com/photo-1558618047-3c8c76ca7d13?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            text-align: center;
            padding: 150px 0 100px;
        }
        
        .mission-vision {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }
        
        .mission-card, .vision-card {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: var(--card-shadow);
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .mission-card:hover, .vision-card:hover {
            transform: translateY(-5px);
        }
        
        .mission-card i, .vision-card i {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .team-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .team-card:hover {
            transform: translateY(-5px);
        }
        
        .team-info {
            padding: 25px;
        }
        
        /* Pricing Page Styles */
        .pricing-hero {
            background: linear-gradient(135deg, rgba(255,107,53,0.9), rgba(255,200,0,0.9)), url('https://images.unsplash.com/photo-1563720223485-854d2637f6e1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            text-align: center;
            padding: 150px 0 100px;
        }
        
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .pricing-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            text-align: center;
            position: relative;
            transition: transform 0.3s ease;
        }
        
        .pricing-card:hover {
            transform: translateY(-10px);
        }
        
        .pricing-header {
            background: var(--gradient-primary);
            color: white;
            padding: 30px;
        }
        
        .pricing-price {
            font-size: 2.5rem;
            font-weight: 800;
            margin: 10px 0;
        }
        
        .pricing-features {
            padding: 30px;
            list-style: none;
        }
        
        .pricing-features li {
            padding: 10px 0;
            border-bottom: 1px solid #eee;
            font-weight: 500;
        }
        
        .pricing-features li:last-child {
            border-bottom: none;
        }
        
        /* Blog Page Styles */
        .blog-hero {
            background: linear-gradient(135deg, rgba(0,78,137,0.9), rgba(255,200,0,0.9)), url('https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            text-align: center;
            padding: 150px 0 100px;
        }
        
        .blog-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .blog-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            transition: transform 0.3s ease;
        }
        
        .blog-card:hover {
            transform: translateY(-5px);
        }
        
        .blog-content {
            padding: 25px;
        }
        
        .blog-meta {
            color: var(--gray);
            font-size: 0.9rem;
            margin-bottom: 15px;
            font-weight: 500;
        }
        
        /* Careers Page Styles */
        .careers-hero {
            background: linear-gradient(135deg, rgba(255,107,53,0.9), rgba(0,78,137,0.9)), url('https://images.unsplash.com/photo-1551434678-e076c223a692?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            text-align: center;
            padding: 150px 0 100px;
        }
        
        .jobs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .job-card {
            background: white;
            border-radius: 20px;
            padding: 30px;
            box-shadow: var(--card-shadow);
            transition: transform 0.3s ease;
        }
        
        .job-card:hover {
            transform: translateY(-5px);
        }
        
        .job-tags {
            display: flex;
            gap: 10px;
            margin: 15px 0;
            flex-wrap: wrap;
        }
        
        .job-tag {
            background: var(--light);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            color: var(--secondary);
            font-weight: 600;
        }
        
        /* Contact Page Styles */
        .contact-hero {
            background: linear-gradient(135deg, rgba(0,78,137,0.9), rgba(255,200,0,0.9)), url('https://images.unsplash.com/photo-1557804506-669a67965ba0?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            text-align: center;
            padding: 150px 0 100px;
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }
        
        .contact-info {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: var(--card-shadow);
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
        }
        
        .contact-item i {
            width: 50px;
            height: 50px;
            background: var(--gradient-primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-size: 1.2rem;
        }
        
        .contact-form {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: var(--card-shadow);
        }
        
        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.8);
            justify-content: center;
            align-items: center;
            z-index: 10000;
        }
        
        .modal-content {
            background: white;
            padding: 40px;
            border-radius: 20px;
            max-width: 500px;
            width: 90%;
            text-align: center;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
        }
        
        /* Footer */
        footer {
            background: var(--gradient-secondary);
            color: white;
            padding: 80px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 50px;
            margin-bottom: 50px;
        }
        
        .footer-column h3 {
            color: var(--accent);
            margin-bottom: 25px;
            font-size: 1.4rem;
            font-weight: 700;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s ease;
            font-weight: 500;
        }
        
        .footer-links a:hover {
            color: var(--accent);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 25px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background 0.3s ease, transform 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #aaa;
            font-weight: 500;
        }
        
        /* Back to Top Button */
        .back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background: var(--gradient-primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(255, 107, 53, 0.3);
            z-index: 999;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }
        
        .back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }
        
        .back-to-top:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255, 107, 53, 0.4);
        }
        
        /* Text Reveal Animations */
        .text-reveal {
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.8s var(--ease-out-expo);
        }
        
        .text-reveal.revealed {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Responsive Styles */
        @media (max-width: 1024px) {
            h1 {
                font-size: 3rem;
            }
            
            h2 {
                font-size: 2.2rem;
            }
            
            .hero h2 {
                font-size: 2.8rem;
            }
            
            .section-title h2 {
                font-size: 2.4rem;
            }
            
            .hero-vector {
                width: 400px;
                height: 320px;
                right: 5%;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 80px;
                left: 0;
                width: 100%;
                background-color: white;
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
                gap: 15px;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-links li {
                margin: 0;
            }
            
            .mobile-menu {
                display: block;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .steps {
                flex-direction: column;
            }
            
            .step:not(:last-child)::after {
                display: none;
            }
            
            section {
                padding: 70px 0;
            }
            
            .calculator-container {
                padding: 25px;
            }
            
            .hero-vector {
                display: none;
            }
            
            .hero-content {
                text-align: center;
            }
            
            .hero-buttons {
                justify-content: center;
            }
            
            .glow-content {
                padding: 40px 20px;
            }
        }
        
        @media (max-width: 480px) {
            h1 {
                font-size: 2.5rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .services-grid {
                grid-template-columns: 1fr;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .app-buttons {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <div class="logo-icon">
                    <i class="fas fa-gas-pump"></i>
                </div>
                <div class="logo-text">
                    <h1>Fuel <span>Corner</span></h1>
                    <div class="tagline">Fuel to Every Corner of India</div>
                </div>
            </div>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
            <ul class="nav-links">
                <li><a href="#" class="nav-link" data-page="home">Home</a></li>
                <li><a href="#" class="nav-link" data-page="about">About</a></li>
                <li><a href="#" class="nav-link" data-page="services">Services</a></li>
                <li><a href="#" class="nav-link" data-page="pricing">Pricing</a></li>
                <li><a href="#" class="nav-link" data-page="blog">Blog</a></li>
                <li><a href="#" class="nav-link" data-page="careers">Careers</a></li>
                <li><a href="#" class="nav-link" data-page="contact">Contact</a></li>
                <li><a href="#" class="btn download-app-btn">Download App</a></li>
            </ul>
        </div>
    </header>

    <!-- Back to Top Button -->
    <div class="back-to-top" id="backToTop">
        <i class="fas fa-chevron-up"></i>
    </div>

    <!-- Home Page -->
    <div id="home" class="page active">
        <!-- Hero Section with Vector -->
        <section class="hero">
            <div class="container">
                <div class="hero-content">
                    <h2 class="text-reveal">Fuel Delivered to Every Corner of India</h2>
                    <p class="text-reveal">India's most trusted on-demand fuel delivery service. Order petrol or diesel through our app and get it delivered safely to your location, no matter where you are.</p>
                    <div class="hero-buttons">
                        <a href="#" class="btn order-fuel-btn">
                            <i class="fas fa-bolt"></i>
                            Order Fuel Now
                        </a>
                        <a href="#" class="btn btn-secondary download-app-btn">
                            <i class="fas fa-mobile-alt"></i>
                            Download App
                        </a>
                    </div>
                </div>
                <!-- Hero Vector -->
                <div class="hero-vector floating">
                    <svg viewBox="0 0 500 400" class="vector-image">
                        <defs>
                            <linearGradient id="heroGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#FF6B35"/>
                                <stop offset="100%" stop-color="#004E89"/>
                            </linearGradient>
                        </defs>
                        <!-- Delivery Truck -->
                        <rect x="100" y="250" width="300" height="80" rx="10" fill="url(#heroGradient)" opacity="0.9"/>
                        <rect x="120" y="200" width="120" height="50" rx="8" fill="url(#heroGradient)" opacity="0.8"/>
                        <circle cx="150" cy="330" r="30" fill="#2C3E50"/>
                        <circle cx="350" cy="330" r="30" fill="#2C3E50"/>
                        <circle cx="150" cy="330" r="15" fill="#ECF0F1"/>
                        <circle cx="350" cy="330" r="15" fill="#ECF0F1"/>
                        
                        <!-- Fuel Pump -->
                        <rect x="350" y="150" width="40" height="120" fill="#34495E"/>
                        <rect x="340" y="140" width="60" height="20" fill="#2C3E50"/>
                        <rect x="355" y="100" width="30" height="40" fill="#E74C3C"/>
                        
                        <!-- Road -->
                        <rect x="0" y="360" width="500" height="40" fill="#7F8C8D"/>
                        <line x1="0" y1="380" x2="500" y2="380" stroke="#ECF0F1" stroke-width="4" stroke-dasharray="10,10"/>
                    </svg>
                </div>
            </div>
        </section>

        <!-- Services Section with Vector Icons -->
        <section class="services">
            <div class="container">
                <div class="section-title">
                    <h2 class="text-reveal">Our Services</h2>
                    <p class="text-reveal">We deliver quality fuel right to your doorstep across India</p>
                </div>
                <div class="services-grid">
                    <!-- Petrol Delivery -->
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="petrolGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#FF6B35"/>
                                            <stop offset="100%" stop-color="#FFC800"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Fuel Pump -->
                                    <rect x="30" y="20" width="60" height="80" rx="5" fill="url(#petrolGradient)"/>
                                    <rect x="40" y="10" width="40" height="15" rx="3" fill="#34495E"/>
                                    <rect x="50" y="25" width="20" height="50" fill="#2C3E50"/>
                                    <circle cx="60" cy="90" r="8" fill="#E74C3C"/>
                                    <!-- Drops -->
                                    <circle cx="45" cy="45" r="3" fill="#3498DB"/>
                                    <circle cx="65" cy="35" r="2" fill="#3498DB"/>
                                    <circle cx="75" cy="55" r="2.5" fill="#3498DB"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>Petrol Delivery</h3>
                            <p>Get high-quality petrol delivered directly to your vehicle at your preferred location and time.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> Available 24/7</li>
                                <li><i class="fas fa-check"></i> Certified quality fuel</li>
                                <li><i class="fas fa-check"></i> Safe delivery process</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">Order Now</a>
                        </div>
                    </div>

                    <!-- Diesel Delivery -->
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="dieselGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#004E89"/>
                                            <stop offset="100%" stop-color="#0066CC"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Truck -->
                                    <rect x="20" y="60" width="80" height="30" rx="5" fill="url(#dieselGradient)"/>
                                    <rect x="30" y="40" width="40" height="20" rx="3" fill="url(#dieselGradient)" opacity="0.8"/>
                                    <circle cx="40" cy="90" r="8" fill="#2C3E50"/>
                                    <circle cx="80" cy="90" r="8" fill="#2C3E50"/>
                                    <!-- Container -->
                                    <rect x="25" y="45" width="70" height="25" fill="#34495E" opacity="0.7"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>Diesel Delivery</h3>
                            <p>We deliver diesel for your commercial vehicles, generators, and equipment with safety measures.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> Bulk delivery options</li>
                                <li><i class="fas fa-check"></i> Scheduled deliveries</li>
                                <li><i class="fas fa-check"></i> Fleet management</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">Order Now</a>
                        </div>
                    </div>

                    <!-- Bulk Fuel Delivery -->
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="bulkGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#FFC800"/>
                                            <stop offset="100%" stop-color="#004E89"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Industrial Tank -->
                                    <rect x="30" y="40" width="60" height="50" rx="5" fill="url(#bulkGradient)"/>
                                    <rect x="25" y="35" width="70" height="10" rx="5" fill="#34495E"/>
                                    <rect x="50" y="20" width="20" height="20" fill="#2C3E50"/>
                                    <!-- Pipes -->
                                    <rect x="40" y="70" width="10" height="30" fill="#7F8C8D"/>
                                    <rect x="70" y="70" width="10" height="30" fill="#7F8C8D"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>Bulk Fuel Delivery</h3>
                            <p>Specialized service for industries, construction sites, and fleet operators requiring bulk fuel.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> Custom delivery schedules</li>
                                <li><i class="fas fa-check"></i> Volume discounts</li>
                                <li><i class="fas fa-check"></i> Dedicated account manager</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">Order Now</a>
                        </div>
                    </div>

                    <!-- Towing Service -->
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="towingGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#FFC800"/>
                                            <stop offset="100%" stop-color="#FF6B35"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Tow Truck -->
                                    <rect x="25" y="60" width="70" height="25" rx="5" fill="url(#towingGradient)"/>
                                    <rect x="35" y="45" width="30" height="15" rx="3" fill="url(#towingGradient)" opacity="0.8"/>
                                    <circle cx="45" cy="85" r="7" fill="#2C3E50"/>
                                    <circle cx="75" cy="85" r="7" fill="#2C3E50"/>
                                    <!-- Hook -->
                                    <path d="M 15,65 Q 25,55 25,65" stroke="#E74C3C" stroke-width="3" fill="none"/>
                                    <circle cx="15" cy="65" r="4" fill="#E74C3C"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>Vehicle Towing Service</h3>
                            <p>Professional vehicle towing service for breakdowns, accidents, or transportation needs across India.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> 24/7 Emergency towing</li>
                                <li><i class="fas fa-check"></i> All vehicle types covered</li>
                                <li><i class="fas fa-check"></i> GPS tracked service</li>
                                <li><i class="fas fa-check"></i> Insurance assistance</li>
                                <li><i class="fas fa-check"></i> Safe & secure transport</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">Request Tow</a>
                        </div>
                    </div>

                    <!-- Mechanic Service -->
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="mechanicGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#004E89"/>
                                            <stop offset="100%" stop-color="#FF6B35"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Car -->
                                    <rect x="25" y="60" width="70" height="25" rx="5" fill="url(#mechanicGradient)"/>
                                    <rect x="35" y="45" width="40" height="15" rx="3" fill="url(#mechanicGradient)" opacity="0.8"/>
                                    <circle cx="45" cy="85" r="7" fill="#2C3E50"/>
                                    <circle cx="75" cy="85" r="7" fill="#2C3E50"/>
                                    <!-- Tools -->
                                    <rect x="80" y="30" width="5" height="20" rx="2" fill="#34495E"/>
                                    <rect x="75" y="35" width="15" height="3" rx="1" fill="#E74C3C"/>
                                    <rect x="35" y="30" width="15" height="3" rx="1" fill="#E74C3C" transform="rotate(45 35 30)"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>On-Site Mechanic Service</h3>
                            <p>Certified mechanics available for emergency repairs, maintenance, and diagnostics at your location.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> Emergency roadside assistance</li>
                                <li><i class="fas fa-check"></i> Battery jump-start service</li>
                                <li><i class="fas fa-check"></i> Tire replacement & repair</li>
                                <li><i class="fas fa-check"></i> Basic diagnostics & repairs</li>
                                <li><i class="fas fa-check"></i> Certified professionals</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">Call Mechanic</a>
                        </div>
                    </div>

                    <!-- Assistance Package -->
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="packageGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#FF6B35"/>
                                            <stop offset="100%" stop-color="#004E89"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Shield -->
                                    <path d="M 60,20 L 90,30 L 90,70 Q 90,90 75,100 Q 60,110 45,100 Q 30,90 30,70 L 30,30 Z" fill="url(#packageGradient)"/>
                                    <!-- Checkmarks -->
                                    <path d="M 45,55 L 55,65 L 75,45" stroke="#FFFFFF" stroke-width="4" fill="none" stroke-linecap="round"/>
                                    <path d="M 45,70 L 55,80 L 75,60" stroke="#FFFFFF" stroke-width="4" fill="none" stroke-linecap="round"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>Vehicle Assistance Package</h3>
                            <p>Complete vehicle care package including fuel, towing, and mechanic services at special bundled rates.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> Priority service access</li>
                                <li><i class="fas fa-check"></i> Discounted bundle pricing</li>
                                <li><i class="fas fa-check"></i> Monthly subscription plans</li>
                                <li><i class="fas fa-check"></i> Corporate fleet packages</li>
                                <li><i class="fas fa-check"></i> 24/7 customer support</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">View Plans</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- How It Works with Vectors -->
        <section class="how-it-works glow-section">
            <div class="container">
                <div class="section-title">
                    <h2 class="text-reveal">How It Works</h2>
                    <p class="text-reveal">Getting fuel delivered is as easy as 1-2-3-4</p>
                </div>
                <div class="glow-media-wrapper">
                    <div class="glow-media-container">
                        <div class="glow-background"></div>
                        <div class="glow-content">
                            <div class="steps">
                                <div class="step">
                                    <div class="step-number">1</div>
                                    <div class="feature-vector">
                                        <svg viewBox="0 0 200 200" class="vector-image">
                                            <defs>
                                                <linearGradient id="step1Gradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                                    <stop offset="0%" stop-color="#FF6B35"/>
                                                    <stop offset="100%" stop-color="#004E89"/>
                                                </linearGradient>
                                            </defs>
                                            <!-- Phone -->
                                            <rect x="60" y="40" width="80" height="120" rx="15" fill="url(#step1Gradient)"/>
                                            <rect x="70" y="50" width="60" height="40" rx="5" fill="#ECF0F1"/>
                                            <circle cx="100" cy="110" r="15" fill="#2C3E50"/>
                                            <rect x="85" y="130" width="30" height="5" rx="2" fill="#34495E"/>
                                            <!-- App Icon -->
                                            <rect x="75" y="60" width="50" height="50" rx="10" fill="#FF6B35"/>
                                            <circle cx="100" cy="75" r="8" fill="#FFFFFF"/>
                                            <rect x="90" y="90" width="20" height="5" rx="2" fill="#FFFFFF"/>
                                        </svg>
                                    </div>
                                    <h3>Download & Order</h3>
                                    <p>Download our app, register your account, and place your fuel order with your location.</p>
                                </div>
                                <div class="step">
                                    <div class="step-number">2</div>
                                    <div class="feature-vector">
                                        <svg viewBox="0 0 200 200" class="vector-image">
                                            <defs>
                                                <linearGradient id="step2Gradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                                    <stop offset="0%" stop-color="#004E89"/>
                                                    <stop offset="100%" stop-color="#FFC800"/>
                                                </linearGradient>
                                            </defs>
                                            <!-- Map with Pin -->
                                            <rect x="50" y="50" width="100" height="100" rx="10" fill="url(#step2Gradient)"/>
                                            <circle cx="100" cy="80" r="20" fill="#E74C3C"/>
                                            <path d="M 100,80 L 100,120 L 90,130 L 100,120 L 110,130 Z" fill="#E74C3C"/>
                                            <!-- Moving Vehicle -->
                                            <rect x="70" y="90" width="20" height="10" rx="2" fill="#2C3E50"/>
                                            <circle cx="75" cy="100" r="3" fill="#ECF0F1"/>
                                            <circle cx="85" cy="100" r="3" fill="#ECF0F1"/>
                                            <!-- Road Lines -->
                                            <line x1="60" y1="100" x2="140" y2="100" stroke="#ECF0F1" stroke-width="3"/>
                                            <line x1="80" y1="120" x2="120" y2="120" stroke="#ECF0F1" stroke-width="3"/>
                                        </svg>
                                    </div>
                                    <h3>Track Delivery</h3>
                                    <p>Track our fuel delivery vehicle in real-time as it makes its way to your location.</p>
                                </div>
                                <div class="step">
                                    <div class="step-number">3</div>
                                    <div class="feature-vector">
                                        <svg viewBox="0 0 200 200" class="vector-image">
                                            <defs>
                                                <linearGradient id="step3Gradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                                    <stop offset="0%" stop-color="#FFC800"/>
                                                    <stop offset="100%" stop-color="#FF6B35"/>
                                                </linearGradient>
                                            </defs>
                                            <!-- Car being refueled -->
                                            <rect x="60" y="100" width="80" height="30" rx="5" fill="url(#step3Gradient)"/>
                                            <rect x="70" y="80" width="40" height="20" rx="3" fill="url(#step3Gradient)" opacity="0.8"/>
                                            <circle cx="80" cy="130" r="8" fill="#2C3E50"/>
                                            <circle cx="120" cy="130" r="8" fill="#2C3E50"/>
                                            <!-- Fuel Nozzle -->
                                            <rect x="130" y="60" width="10" height="40" fill="#34495E"/>
                                            <rect x="125" y="50" width="20" height="10" rx="2" fill="#E74C3C"/>
                                            <!-- Fuel Drops -->
                                            <circle cx="135" cy="105" r="3" fill="#3498DB"/>
                                            <circle cx="140" cy="100" r="2" fill="#3498DB"/>
                                        </svg>
                                    </div>
                                    <h3>Safe Refueling</h3>
                                    <p>Our trained professional will safely refuel your vehicle following all safety protocols.</p>
                                </div>
                                <div class="step">
                                    <div class="step-number">4</div>
                                    <div class="feature-vector">
                                        <svg viewBox="0 0 200 200" class="vector-image">
                                            <defs>
                                                <linearGradient id="step4Gradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                                    <stop offset="0%" stop-color="#FF6B35"/>
                                                    <stop offset="100%" stop-color="#004E89"/>
                                                </linearGradient>
                                            </defs>
                                            <!-- Payment Success -->
                                            <rect x="60" y="60" width="80" height="80" rx="10" fill="url(#step4Gradient)"/>
                                            <circle cx="100" cy="90" r="25" fill="#FFFFFF"/>
                                            <path d="M 90,90 L 95,95 L 110,80" stroke="#27AE60" stroke-width="5" fill="none" stroke-linecap="round"/>
                                            <!-- Payment Icons -->
                                            <circle cx="80" cy="130" r="5" fill="#3498DB"/>
                                            <rect x="95" cy="125" width="10" height="10" rx="2" fill="#F39C12"/>
                                            <path d="M 115,125 L 120,130 L 115,135 Z" fill="#9B59B6"/>
                                        </svg>
                                    </div>
                                    <h3>Digital Payment</h3>
                                    <p>Pay securely through our app using UPI, credit/debit cards, or digital wallets.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Live Service Status -->
        <section class="live-status">
            <div class="container">
                <div class="section-title">
                    <h2 class="text-reveal">Live Service Status</h2>
                    <p class="text-reveal">Real-time updates from across our service areas</p>
                </div>
                <div class="status-grid">
                    <div class="status-card online">
                        <div class="status-indicator"></div>
                        <h4>Mumbai</h4>
                        <p>15 delivery vehicles active</p>
                        <span class="wait-time">~20 min delivery</span>
                    </div>
                    <div class="status-card busy">
                        <div class="status-indicator"></div>
                        <h4>Delhi</h4>
                        <p>22 delivery vehicles active</p>
                        <span class="wait-time">~35 min delivery</span>
                    </div>
                    <div class="status-card online">
                        <div class="status-indicator"></div>
                        <h4>Bangalore</h4>
                        <p>18 delivery vehicles active</p>
                        <span class="wait-time">~25 min delivery</span>
                    </div>
                    <div class="status-card online">
                        <div class="status-indicator"></div>
                        <h4>Hyderabad</h4>
                        <p>12 delivery vehicles active</p>
                        <span class="wait-time">~30 min delivery</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Trust Badges -->
        <section class="trust-badges">
            <div class="container">
                <div class="badges-grid">
                    <div class="badge">
                        <i class="fas fa-shield-alt"></i>
                        <span>ISO 9001 Certified</span>
                    </div>
                    <div class="badge">
                        <i class="fas fa-lock"></i>
                        <span>SSL Secured Payments</span>
                    </div>
                    <div class="badge">
                        <i class="fas fa-truck"></i>
                        <span>5000+ Deliveries</span>
                    </div>
                    <div class="badge">
                        <i class="fas fa-heart"></i>
                        <span>98% Customer Satisfaction</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- App Download with Vector -->
        <section class="app-download glow-section">
            <div class="container">
                <div class="app-vector floating">
                    <svg viewBox="0 0 300 300" class="vector-image">
                        <defs>
                            <linearGradient id="appGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#FFFFFF"/>
                                <stop offset="100%" stop-color="#F8F9FA"/>
                            </linearGradient>
                        </defs>
                        <!-- Phone -->
                        <rect x="50" y="30" width="200" height="240" rx="25" fill="url(#appGradient)"/>
                        <rect x="70" y="50" width="160" height="180" rx="10" fill="#004E89"/>
                        
                        <!-- App Interface -->
                        <rect x="80" y="60" width="140" height="30" rx="5" fill="#FF6B35"/>
                        <circle cx="95" cy="75" r="3" fill="#FFFFFF"/>
                        <rect x="105" y="72" width="100" height="6" rx="3" fill="#FFFFFF" opacity="0.8"/>
                        
                        <!-- Fuel Icon in App -->
                        <rect x="100" y="110" width="100" height="60" rx="10" fill="#FFC800"/>
                        <rect x="120" y="120" width="20" height="40" fill="#34495E"/>
                        <rect x="125" y="100" width="10" height="20" fill="#E74C3C"/>
                        
                        <!-- Location Pin -->
                        <circle cx="200" cy="150" r="8" fill="#E74C3C"/>
                        <circle cx="200" cy="150" r="4" fill="#FFFFFF"/>
                        
                        <!-- Action Buttons -->
                        <rect x="100" y="190" width="40" height="15" rx="7" fill="#27AE60"/>
                        <rect x="160" y="190" width="40" height="15" rx="7" fill="#E74C3C"/>
                    </svg>
                </div>
                <h2 class="text-reveal">Download Fuel Corner App</h2>
                <p class="text-reveal">Get the app now and experience the convenience of fuel delivery at your fingertips. Available on both Android and iOS.</p>
                <div class="app-buttons">
                    <a href="https://play.google.com/store/apps/details?id=com.fuelcorner.app" class="app-btn" target="_blank">
                        <i class="fab fa-google-play"></i>
                        <div>
                            <small>GET IT ON</small>
                            <div>Google Play</div>
                        </div>
                    </a>
                    <a href="https://apps.apple.com/app/fuel-corner/id123456789" class="app-btn" target="_blank">
                        <i class="fab fa-apple"></i>
                        <div>
                            <small>Download on the</small>
                            <div>App Store</div>
                        </div>
                    </a>
                </div>
            </div>
        </section>

        <!-- Enhanced Fuel Calculator -->
        <section class="calculator">
            <div class="container">
                <div class="section-title">
                    <h2 class="text-reveal">Smart Fuel Calculator</h2>
                    <p class="text-reveal">Calculate your fuel expenses for any journey across India</p>
                </div>
                <div class="calculator-vector">
                    <svg viewBox="0 0 250 250" class="vector-image">
                        <defs>
                            <linearGradient id="calcGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#FF6B35"/>
                                <stop offset="100%" stop-color="#004E89"/>
                            </linearGradient>
                        </defs>
                        <!-- Calculator -->
                        <rect x="50" y="50" width="150" height="150" rx="10" fill="url(#calcGradient)"/>
                        <rect x="60" y="60" width="130" height="40" rx="5" fill="#ECF0F1"/>
                        <rect x="70" y="110" width="30" height="30" rx="3" fill="#34495E"/>
                        <rect x="110" y="110" width="30" height="30" rx="3" fill="#34495E"/>
                        <rect x="150" y="110" width="30" height="30" rx="3" fill="#34495E"/>
                        <rect x="70" y="150" width="30" height="30" rx="3" fill="#FFC800"/>
                        <rect x="110" y="150" width="30" height="30" rx="3" fill="#FFC800"/>
                        <rect x="150" y="150" width="30" height="30" rx="3" fill="#FFC800"/>
                        
                        <!-- Fuel Symbol -->
                        <rect x="180" y="70" width="40" height="60" rx="5" fill="#E74C3C" opacity="0.8"/>
                        <rect x="185" y="75" width="30" height="20" fill="#FFFFFF" opacity="0.3"/>
                        
                        <!-- Calculation Symbols -->
                        <text x="85" y="130" font-family="Arial" font-size="14" fill="#ECF0F1">+</text>
                        <text x="125" y="130" font-family="Arial" font-size="14" fill="#ECF0F1">-</text>
                        <text x="165" y="130" font-family="Arial" font-size="14" fill="#ECF0F1">×</text>
                        <text x="85" y="170" font-family="Arial" font-size="14" fill="#2C3E50">=</text>
                        <text x="125" y="170" font-family="Arial" font-size="14" fill="#2C3E50">%</text>
                        <text x="165" y="170" font-family="Arial" font-size="14" fill="#2C3E50">₹</text>
                    </svg>
                </div>
                <div class="calculator-container">
                    <div class="calculator-header">
                        <h3>Plan Your Journey</h3>
                        <p>Get precise cost estimates for your trip</p>
                    </div>
                    
                    <div class="calculator-grid">
                        <div class="form-group">
                            <label for="from-city">From City</label>
                            <select id="from-city" class="form-control">
                                <option value="">Select City</option>
                                <option value="mumbai">Mumbai</option>
                                <option value="delhi">Delhi</option>
                                <option value="bangalore">Bangalore</option>
                                <option value="hyderabad">Hyderabad</option>
                                <option value="chennai">Chennai</option>
                                <option value="kolkata">Kolkata</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="to-city">To City</label>
                            <select id="to-city" class="form-control">
                                <option value="">Select City</option>
                                <option value="mumbai">Mumbai</option>
                                <option value="delhi">Delhi</option>
                                <option value="bangalore">Bangalore</option>
                                <option value="hyderabad">Hyderabad</option>
                                <option value="chennai">Chennai</option>
                                <option value="kolkata">Kolkata</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="vehicle-type">Vehicle Type</label>
                            <select id="vehicle-type" class="form-control">
                                <option value="">Select Vehicle</option>
                                <option value="hatchback">Hatchback (15-20 kmpl)</option>
                                <option value="sedan">Sedan (12-18 kmpl)</option>
                                <option value="suv">SUV (10-15 kmpl)</option>
                                <option value="bike">Motorcycle (35-50 kmpl)</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="fuel-type">Fuel Type</label>
                            <select id="fuel-type" class="form-control">
                                <option value="petrol">Petrol</option>
                                <option value="diesel">Diesel</option>
                            </select>
                        </div>
                    </div>
                    
                    <button id="calculate-btn" class="btn">Calculate Fuel Cost</button>
                    
                    <div id="calculator-results" class="calculator-results">
                        <div class="result-item">
                            <span>Distance:</span>
                            <span id="distance-result">-- km</span>
                        </div>
                        <div class="result-item">
                            <span>Fuel Needed:</span>
                            <span id="fuel-result">-- liters</span>
                        </div>
                        <div class="result-item total">
                            <span>Total Cost:</span>
                            <span id="total-cost">₹ --</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Original Calculator -->
        <section class="calculator original-calculator glow-section">
            <div class="container">
                <div class="section-title">
                    <h2 class="text-reveal">Simple Fuel Calculator</h2>
                    <p class="text-reveal">Quick calculation based on distance and mileage</p>
                </div>
                <div class="glow-media-wrapper">
                    <div class="glow-media-container">
                        <div class="glow-background"></div>
                        <div class="glow-content">
                            <div class="original-calculator-container">
                                <div class="form-group">
                                    <label for="distance">Distance (in km)</label>
                                    <input type="number" id="distance" class="form-control" placeholder="Enter distance">
                                </div>
                                <div class="form-group">
                                    <label for="mileage">Vehicle Mileage (km/l)</label>
                                    <input type="number" id="mileage" class="form-control" placeholder="Enter mileage">
                                </div>
                                <div class="form-group">
                                    <label for="simple-fuel-type">Fuel Type</label>
                                    <select id="simple-fuel-type" class="form-control">
                                        <option value="petrol">Petrol</option>
                                        <option value="diesel">Diesel</option>
                                    </select>
                                </div>
                                <button id="simple-calculate-btn" class="btn">Calculate Fuel Cost</button>
                                <div id="simple-result" class="result"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Coverage -->
        <section class="coverage">
            <div class="container">
                <div class="section-title">
                    <h2 class="text-reveal">We Serve Every Corner of India</h2>
                    <p class="text-reveal">Fuel Corner is rapidly expanding across India. Currently serving these major cities with more locations being added regularly.</p>
                </div>
                <div class="cities">
                    <div class="city">Mumbai</div>
                    <div class="city">Delhi</div>
                    <div class="city">Bangalore</div>
                    <div class="city">Hyderabad</div>
                    <div class="city">Chennai</div>
                    <div class="city">Kolkata</div>
                    <div class="city">Pune</div>
                    <div class="city">Ahmedabad</div>
                    <div class="city">Jaipur</div>
                    <div class="city">Lucknow</div>
                    <div class="city">Chandigarh</div>
                    <div class="city">Kochi</div>
                    <div class="city">Bhopal</div>
                    <div class="city">Indore</div>
                    <div class="city">Patna</div>
                    <div class="city">Guwahati</div>
                </div>
            </div>
        </section>

        <!-- Enhanced Testimonials -->
        <section class="testimonials glow-section">
            <div class="container">
                <div class="section-title">
                    <h2 class="text-reveal">What Our Customers Say</h2>
                    <p class="text-reveal">Hear from our satisfied customers across India</p>
                </div>
                <div class="glow-media-wrapper">
                    <div class="glow-media-container">
                        <div class="glow-background"></div>
                        <div class="glow-content">
                            <div class="testimonial-carousel">
                                <div class="testimonial-slide active">
                                    <div class="testimonial-content">
                                        <div class="rating">★★★★★</div>
                                        <p>Fuel Corner has been a lifesaver for my logistics business. No more downtime for refueling our fleet. The service is reliable and the fuel quality is excellent.</p>
                                        <div class="customer-info">
                                            <strong>Rajesh Kumar</strong>
                                            <span>Logistics Business Owner, Delhi</span>
                                        </div>
                                    </div>
                                </div>
                                <div class="testimonial-slide">
                                    <div class="testimonial-content">
                                        <div class="rating">★★★★★</div>
                                        <p>As a working professional in Bangalore traffic, Fuel Corner saves me so much time. I get fuel delivered to my office parking while I'm working. Highly recommended!</p>
                                        <div class="customer-info">
                                            <strong>Priya Menon</strong>
                                            <span>IT Professional, Bangalore</span>
                                        </div>
                                    </div>
                                </div>
                                <div class="testimonial-slide">
                                    <div class="testimonial-content">
                                        <div class="rating">★★★★★</div>
                                        <p>The convenience of getting diesel delivered to our construction site in Pune has improved our productivity significantly. The bulk delivery option is perfect for our needs.</p>
                                        <div class="customer-info">
                                            <strong>Anil Sharma</strong>
                                            <span>Construction Manager, Pune</span>
                                        </div>
                                    </div>
                                </div>
                                <div class="testimonial-slide">
                                    <div class="testimonial-content">
                                        <div class="rating">★★★★★</div>
                                        <p>I was skeptical at first, but Fuel Corner proved me wrong. The service is prompt, professional, and the fuel quality is certified. Will definitely use again!</p>
                                        <div class="customer-info">
                                            <strong>Sanjay Patel</strong>
                                            <span>Business Owner, Ahmedabad</span>
                                        </div>
                                    </div>
                                </div>
                                <div class="testimonial-slide">
                                    <div class="testimonial-content">
                                        <div class="rating">★★★★★</div>
                                        <p>Emergency fuel delivery at 2 AM! I was stranded on the highway and Fuel Corner rescued me. Their 24/7 service is truly amazing.</p>
                                        <div class="customer-info">
                                            <strong>Rohit Verma</strong>
                                            <span>Sales Executive, Chennai</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="carousel-controls">
                                <div class="carousel-dot active" data-slide="0"></div>
                                <div class="carousel-dot" data-slide="1"></div>
                                <div class="carousel-dot" data-slide="2"></div>
                                <div class="carousel-dot" data-slide="3"></div>
                                <div class="carousel-dot" data-slide="4"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- About Page -->
    <div id="about" class="page">
        <section class="about-hero">
            <div class="container">
                <h2>About Fuel Corner</h2>
                <p>Revolutionizing fuel delivery across India, one corner at a time</p>
            </div>
        </section>

        <section class="services">
            <div class="container">
                <div class="section-title">
                    <h2>Our Story</h2>
                </div>
                <div class="mission-vision">
                    <div class="mission-card">
                        <i class="fas fa-bullseye"></i>
                        <h3>Our Mission</h3>
                        <p>To make fuel accessible to every corner of India through safe, reliable, and convenient delivery services that save time and enhance productivity for individuals and businesses alike.</p>
                    </div>
                    <div class="vision-card">
                        <i class="fas fa-eye"></i>
                        <h3>Our Vision</h3>
                        <p>To become India's most trusted fuel delivery partner, transforming the way people and businesses access energy while maintaining the highest standards of safety and service quality.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="how-it-works">
            <div class="container">
                <div class="section-title">
                    <h2>Our Values</h2>
                </div>
                <div class="steps">
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <h3>Safety First</h3>
                        <p>We prioritize safety in every aspect of our operations, from handling to delivery.</p>
                    </div>
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-users"></i>
                        </div>
                        <h3>Customer Focus</h3>
                        <p>Our customers are at the heart of everything we do, driving our innovation and service improvements.</p>
                    </div>
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-bolt"></i>
                        </div>
                        <h3>Innovation</h3>
                        <p>We continuously innovate to provide better, faster, and more efficient fuel delivery solutions.</p>
                    </div>
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-handshake"></i>
                        </div>
                        <h3>Integrity</h3>
                        <p>We conduct our business with honesty, transparency, and ethical practices.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="testimonials">
            <div class="container">
                <div class="section-title">
                    <h2>Leadership Team</h2>
                </div>
                <div class="team-grid">
                    <div class="team-card">
                        <div class="team-vector">
                            <svg viewBox="0 0 150 150" class="vector-image">
                                <defs>
                                    <linearGradient id="ceoGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                        <stop offset="0%" stop-color="#FF6B35"/>
                                        <stop offset="100%" stop-color="#004E89"/>
                                    </linearGradient>
                                </defs>
                                <!-- Head -->
                                <circle cx="75" cy="60" r="40" fill="url(#ceoGradient)"/>
                                <!-- Body -->
                                <rect x="45" y="100" width="60" height="40" rx="20" fill="url(#ceoGradient)"/>
                                <!-- Features -->
                                <circle cx="65" cy="55" r="3" fill="#FFFFFF"/>
                                <circle cx="85" cy="55" r="3" fill="#FFFFFF"/>
                                <path d="M 70,70 Q 75,75 80,70" stroke="#FFFFFF" stroke-width="2" fill="none"/>
                            </svg>
                        </div>
                        <div class="team-info">
                            <h3>Lakshman Sai</h3>
                            <p>CEO & Founder</p>
                            <p>Former energy sector executive with 15+ years of experience</p>
                        </div>
                    </div>
                    <div class="team-card">
                        <div class="team-vector">
                            <svg viewBox="0 0 150 150" class="vector-image">
                                <defs>
                                    <linearGradient id="cooGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                        <stop offset="0%" stop-color="#004E89"/>
                                        <stop offset="100%" stop-color="#FF6B35"/>
                                    </linearGradient>
                                </defs>
                                <!-- Head -->
                                <circle cx="75" cy="60" r="40" fill="url(#cooGradient)"/>
                                <!-- Body -->
                                <rect x="45" y="100" width="60" height="40" rx="20" fill="url(#cooGradient)"/>
                                <!-- Features -->
                                <circle cx="65" cy="55" r="3" fill="#FFFFFF"/>
                                <circle cx="85" cy="55" r="3" fill="#FFFFFF"/>
                                <path d="M 70,70 Q 75,75 80,70" stroke="#FFFFFF" stroke-width="2" fill="none"/>
                                <!-- Hair -->
                                <path d="M 45,40 Q 75,20 105,40" stroke="#2C3E50" stroke-width="8" fill="none" stroke-linecap="round"/>
                            </svg>
                        </div>
                        <div class="team-info">
                            <h3>Bhoomika Naidu</h3>
                            <p>COO</p>
                            <p>Operations expert with background in logistics and supply chain</p>
                        </div>
                    </div>
                    <div class="team-card">
                        <div class="team-vector">
                            <svg viewBox="0 0 150 150" class="vector-image">
                                <defs>
                                    <linearGradient id="ctoGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                        <stop offset="0%" stop-color="#FFC800"/>
                                        <stop offset="100%" stop-color="#004E89"/>
                                    </linearGradient>
                                </defs>
                                <!-- Head -->
                                <circle cx="75" cy="60" r="40" fill="url(#ctoGradient)"/>
                                <!-- Body -->
                                <rect x="45" y="100" width="60" height="40" rx="20" fill="url(#ctoGradient)"/>
                                <!-- Features -->
                                <circle cx="65" cy="55" r="3" fill="#FFFFFF"/>
                                <circle cx="85" cy="55" r="3" fill="#FFFFFF"/>
                                <path d="M 70,70 Q 75,75 80,70" stroke="#FFFFFF" stroke-width="2" fill="none"/>
                                <!-- Glasses -->
                                <rect x="60" y="50" width="20" height="10" rx="5" stroke="#2C3E50" stroke-width="2" fill="none"/>
                                <rect x="85" y="50" width="20" height="10" rx="5" stroke="#2C3E50" stroke-width="2" fill="none"/>
                                <line x1="80" y1="55" x2="85" y2="55" stroke="#2C3E50" stroke-width="2"/>
                            </svg>
                        </div>
                        <div class="team-info">
                            <h3>Bhavana sree</h3>
                            <p>CTO</p>
                            <p>Technology visionary with expertise in mobile platforms and IoT</p>
                        </div>
                    </div>
                    <div class="team-card">
                        <div class="team-vector">
                            <svg viewBox="0 0 150 150" class="vector-image">
                                <defs>
                                    <linearGradient id="cfoGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                        <stop offset="0%" stop-color="#FF6B35"/>
                                        <stop offset="100%" stop-color="#FFC800"/>
                                    </linearGradient>
                                </defs>
                                <!-- Head -->
                                <circle cx="75" cy="60" r="40" fill="url(#cfoGradient)"/>
                                <!-- Body -->
                                <rect x="45" y="100" width="60" height="40" rx="20" fill="url(#cfoGradient)"/>
                                <!-- Features -->
                                <circle cx="65" cy="55" r="3" fill="#FFFFFF"/>
                                <circle cx="85" cy="55" r="3" fill="#FFFFFF"/>
                                <path d="M 70,70 Q 75,75 80,70" stroke="#FFFFFF" stroke-width="2" fill="none"/>
                                <!-- Tie -->
                                <path d="M 75,100 L 70,120 L 75,125 L 80,120 Z" fill="#E74C3C"/>
                            </svg>
                        </div>
                        <div class="team-info">
                            <h3>Rishi Maharshi</h3>
                            <p>CFO</p>
                            <p>Financial strategist with experience in venture capital and scaling businesses</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Services Page -->
    <div id="services" class="page">
        <section class="hero">
            <div class="container">
                <h2>Our Services</h2>
                <p>Comprehensive fuel delivery solutions for every need across India</p>
            </div>
        </section>

        <section class="services">
            <div class="container">
                <div class="services-grid">
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="petrolGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#FF6B35"/>
                                            <stop offset="100%" stop-color="#FFC800"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Fuel Pump -->
                                    <rect x="30" y="20" width="60" height="80" rx="5" fill="url(#petrolGradient)"/>
                                    <rect x="40" y="10" width="40" height="15" rx="3" fill="#34495E"/>
                                    <rect x="50" y="25" width="20" height="50" fill="#2C3E50"/>
                                    <circle cx="60" cy="90" r="8" fill="#E74C3C"/>
                                    <!-- Drops -->
                                    <circle cx="45" cy="45" r="3" fill="#3498DB"/>
                                    <circle cx="65" cy="35" r="2" fill="#3498DB"/>
                                    <circle cx="75" cy="55" r="2.5" fill="#3498DB"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>Petrol Delivery</h3>
                            <p>Get high-quality petrol delivered directly to your vehicle at your preferred location and time.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> Available 24/7</li>
                                <li><i class="fas fa-check"></i> Certified quality fuel</li>
                                <li><i class="fas fa-check"></i> Safe delivery process</li>
                                <li><i class="fas fa-check"></i> Real-time tracking</li>
                                <li><i class="fas fa-check"></i> Multiple payment options</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">Order Now</a>
                        </div>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="dieselGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#004E89"/>
                                            <stop offset="100%" stop-color="#0066CC"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Truck -->
                                    <rect x="20" y="60" width="80" height="30" rx="5" fill="url(#dieselGradient)"/>
                                    <rect x="30" y="40" width="40" height="20" rx="3" fill="url(#dieselGradient)" opacity="0.8"/>
                                    <circle cx="40" cy="90" r="8" fill="#2C3E50"/>
                                    <circle cx="80" cy="90" r="8" fill="#2C3E50"/>
                                    <!-- Container -->
                                    <rect x="25" y="45" width="70" height="25" fill="#34495E" opacity="0.7"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>Diesel Delivery</h3>
                            <p>We deliver diesel for your commercial vehicles, generators, and equipment with safety measures.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> Bulk delivery options</li>
                                <li><i class="fas fa-check"></i> Scheduled deliveries</li>
                                <li><i class="fas fa-check"></i> Fleet management</li>
                                <li><i class="fas fa-check"></i> Volume discounts</li>
                                <li><i class="fas fa-check"></i> Emergency service</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">Order Now</a>
                        </div>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="bulkGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#FFC800"/>
                                            <stop offset="100%" stop-color="#004E89"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Industrial Tank -->
                                    <rect x="30" y="40" width="60" height="50" rx="5" fill="url(#bulkGradient)"/>
                                    <rect x="25" y="35" width="70" height="10" rx="5" fill="#34495E"/>
                                    <rect x="50" y="20" width="20" height="20" fill="#2C3E50"/>
                                    <!-- Pipes -->
                                    <rect x="40" y="70" width="10" height="30" fill="#7F8C8D"/>
                                    <rect x="70" y="70" width="10" height="30" fill="#7F8C8D"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>Bulk Fuel Delivery</h3>
                            <p>Specialized service for industries, construction sites, and fleet operators requiring bulk fuel.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> Custom delivery schedules</li>
                                <li><i class="fas fa-check"></i> Volume discounts</li>
                                <li><i class="fas fa-check"></i> Dedicated account manager</li>
                                <li><i class="fas fa-check"></i> On-site storage solutions</li>
                                <li><i class="fas fa-check"></i> Fuel quality certification</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">Order Now</a>
                        </div>
                    </div>
                    <!-- NEW SERVICES ADDED TO SERVICES PAGE -->
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="towingGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#FFC800"/>
                                            <stop offset="100%" stop-color="#FF6B35"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Tow Truck -->
                                    <rect x="25" y="60" width="70" height="25" rx="5" fill="url(#towingGradient)"/>
                                    <rect x="35" y="45" width="30" height="15" rx="3" fill="url(#towingGradient)" opacity="0.8"/>
                                    <circle cx="45" cy="85" r="7" fill="#2C3E50"/>
                                    <circle cx="75" cy="85" r="7" fill="#2C3E50"/>
                                    <!-- Hook -->
                                    <path d="M 15,65 Q 25,55 25,65" stroke="#E74C3C" stroke-width="3" fill="none"/>
                                    <circle cx="15" cy="65" r="4" fill="#E74C3C"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>Vehicle Towing Service</h3>
                            <p>Professional vehicle towing service for breakdowns, accidents, or transportation needs across India.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> 24/7 Emergency towing</li>
                                <li><i class="fas fa-check"></i> All vehicle types covered</li>
                                <li><i class="fas fa-check"></i> GPS tracked service</li>
                                <li><i class="fas fa-check"></i> Insurance assistance</li>
                                <li><i class="fas fa-check"></i> Safe & secure transport</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">Request Tow</a>
                        </div>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="mechanicGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#004E89"/>
                                            <stop offset="100%" stop-color="#FF6B35"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Car -->
                                    <rect x="25" y="60" width="70" height="25" rx="5" fill="url(#mechanicGradient)"/>
                                    <rect x="35" y="45" width="40" height="15" rx="3" fill="url(#mechanicGradient)" opacity="0.8"/>
                                    <circle cx="45" cy="85" r="7" fill="#2C3E50"/>
                                    <circle cx="75" cy="85" r="7" fill="#2C3E50"/>
                                    <!-- Tools -->
                                    <rect x="80" y="30" width="5" height="20" rx="2" fill="#34495E"/>
                                    <rect x="75" y="35" width="15" height="3" rx="1" fill="#E74C3C"/>
                                    <rect x="35" y="30" width="15" height="3" rx="1" fill="#E74C3C" transform="rotate(45 35 30)"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>On-Site Mechanic Service</h3>
                            <p>Certified mechanics available for emergency repairs, maintenance, and diagnostics at your location.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> Emergency roadside assistance</li>
                                <li><i class="fas fa-check"></i> Battery jump-start service</li>
                                <li><i class="fas fa-check"></i> Tire replacement & repair</li>
                                <li><i class="fas fa-check"></i> Basic diagnostics & repairs</li>
                                <li><i class="fas fa-check"></i> Certified professionals</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">Call Mechanic</a>
                        </div>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">
                            <div class="service-vector">
                                <svg viewBox="0 0 120 120" class="vector-image">
                                    <defs>
                                        <linearGradient id="packageGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                            <stop offset="0%" stop-color="#FF6B35"/>
                                            <stop offset="100%" stop-color="#004E89"/>
                                        </linearGradient>
                                    </defs>
                                    <!-- Shield -->
                                    <path d="M 60,20 L 90,30 L 90,70 Q 90,90 75,100 Q 60,110 45,100 Q 30,90 30,70 L 30,30 Z" fill="url(#packageGradient)"/>
                                    <!-- Checkmarks -->
                                    <path d="M 45,55 L 55,65 L 75,45" stroke="#FFFFFF" stroke-width="4" fill="none" stroke-linecap="round"/>
                                    <path d="M 45,70 L 55,80 L 75,60" stroke="#FFFFFF" stroke-width="4" fill="none" stroke-linecap="round"/>
                                </svg>
                            </div>
                        </div>
                        <div class="service-content">
                            <h3>Vehicle Assistance Package</h3>
                            <p>Complete vehicle care package including fuel, towing, and mechanic services at special bundled rates.</p>
                            <ul class="service-features">
                                <li><i class="fas fa-check"></i> Priority service access</li>
                                <li><i class="fas fa-check"></i> Discounted bundle pricing</li>
                                <li><i class="fas fa-check"></i> Monthly subscription plans</li>
                                <li><i class="fas fa-check"></i> Corporate fleet packages</li>
                                <li><i class="fas fa-check"></i> 24/7 customer support</li>
                            </ul>
                            <a href="#" class="btn order-fuel-btn">View Plans</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="how-it-works">
            <div class="container">
                <div class="section-title">
                    <h2>Service Coverage</h2>
                </div>
                <div class="cities">
                    <div class="city">Mumbai</div>
                    <div class="city">Delhi</div>
                    <div class="city">Bangalore</div>
                    <div class="city">Hyderabad</div>
                    <div class="city">Chennai</div>
                    <div class="city">Kolkata</div>
                    <div class="city">Pune</div>
                    <div class="city">Ahmedabad</div>
                    <div class="city">Jaipur</div>
                    <div class="city">Lucknow</div>
                    <div class="city">Chandigarh</div>
                    <div class="city">Kochi</div>
                    <div class="city">Bhopal</div>
                    <div class="city">Indore</div>
                    <div class="city">Patna</div>
                    <div class="city">Guwahati</div>
                </div>
            </div>
        </section>
    </div>

    <!-- Pricing Page -->
    <div id="pricing" class="page">
        <section class="pricing-hero">
            <div class="container">
                <h2>Transparent Pricing</h2>
                <p>Competitive fuel prices with no hidden charges</p>
            </div>
        </section>

        <section class="services">
            <div class="container">
                <div class="section-title">
                    <h2>Fuel Prices</h2>
                    <p>Current market rates with minimal delivery charges</p>
                </div>
                <div class="pricing-grid">
                    <div class="pricing-card">
                        <div class="pricing-header">
                            <h3>Petrol</h3>
                            <div class="pricing-price">₹106.31/L</div>
                            <p>Premium Quality</p>
                        </div>
                        <ul class="pricing-features">
                            <li>BS6 Compliant Fuel</li>
                            <li>Additive Enhanced</li>
                            <li>Minimum Order: 5 Liters</li>
                            <li>Delivery Charge: ₹49</li>
                            <li>Free delivery above 20L</li>
                        </ul>
                        <div style="padding: 20px;">
                            <a href="#" class="btn order-fuel-btn">Order Now</a>
                        </div>
                    </div>
                    <div class="pricing-card">
                        <div class="pricing-header">
                            <h3>Diesel</h3>
                            <div class="pricing-price">₹94.27/L</div>
                            <p>Commercial Grade</p>
                        </div>
                        <ul class="pricing-features">
                            <li>High Cetane Rating</li>
                            <li>Low Sulfur Content</li>
                            <li>Minimum Order: 10 Liters</li>
                            <li>Delivery Charge: ₹69</li>
                            <li>Free delivery above 50L</li>
                        </ul>
                        <div style="padding: 20px;">
                            <a href="#" class="btn order-fuel-btn">Order Now</a>
                        </div>
                    </div>
                    <div class="pricing-card">
                        <div class="pricing-header">
                            <h3>Bulk Orders</h3>
                            <div class="pricing-price">Custom</div>
                            <p>Enterprise Solutions</p>
                        </div>
                        <ul class="pricing-features">
                            <li>Volume Discounts</li>
                            <li>Scheduled Deliveries</li>
                            <li>Dedicated Account Manager</li>
                            <li>Fuel Quality Reports</li>
                            <li>24/7 Support</li>
                        </ul>
                        <div style="padding: 20px;">
                            <a href="#" class="btn">Contact Sales</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="how-it-works">
            <div class="container">
                <div class="section-title">
                    <h2>Why Choose Fuel Corner?</h2>
                </div>
                <div class="steps">
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-rupee-sign"></i>
                        </div>
                        <h3>No Price Markup</h3>
                        <p>We charge the same as fuel stations with minimal delivery fees</p>
                    </div>
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-clock"></i>
                        </div>
                        <h3>Save Time</h3>
                        <p>No more waiting in queues at fuel stations</p>
                    </div>
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <h3>Safety Assured</h3>
                        <p>Trained professionals following all safety protocols</p>
                    </div>
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-tachometer-alt"></i>
                        </div>
                        <h3>Real-time Tracking</h3>
                        <p>Track your delivery in real-time through our app</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Blog Page -->
    <div id="blog" class="page">
        <section class="blog-hero">
            <div class="container">
                <h2>Fuel Corner Blog</h2>
                <p>Insights, updates, and industry trends</p>
            </div>
        </section>

        <section class="services">
            <div class="container">
                <div class="section-title">
                    <h2>Latest Articles</h2>
                </div>
                <div class="blog-grid">
                    <div class="blog-card">
                        <div class="blog-content">
                            <div class="blog-meta">March 15, 2024 • Industry</div>
                            <h3>The Future of Fuel Delivery in India</h3>
                            <p>Exploring how on-demand fuel services are transforming the energy distribution landscape across Indian cities and rural areas.</p>
                            <a href="#" class="btn" style="margin-top: 15px;">Read More</a>
                        </div>
                    </div>
                    <div class="blog-card">
                        <div class="blog-content">
                            <div class="blog-meta">March 10, 2024 • Sustainability</div>
                            <h3>Sustainable Practices in Fuel Distribution</h3>
                            <p>How modern fuel delivery services are implementing eco-friendly practices to reduce carbon footprint and environmental impact.</p>
                            <a href="#" class="btn" style="margin-top: 15px;">Read More</a>
                        </div>
                    </div>
                    <div class="blog-card">
                        <div class="blog-content">
                            <div class="blog-meta">March 5, 2024 • Technology</div>
                            <h3>Mobile Technology Revolutionizing Fuel Access</h3>
                            <p>The role of smartphone apps and IoT in making fuel delivery more efficient, safe, and accessible to millions of Indians.</p>
                            <a href="#" class="btn" style="margin-top: 15px;">Read More</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Careers Page -->
    <div id="careers" class="page">
        <section class="careers-hero">
            <div class="container">
                <h2>Join Our Team</h2>
                <p>Build the future of fuel delivery with us</p>
            </div>
        </section>

        <section class="services">
            <div class="container">
                <div class="section-title">
                    <h2>Current Openings</h2>
                </div>
                <div class="jobs-grid">
                    <div class="job-card">
                        <h3>Delivery Operations Manager</h3>
                        <div class="job-tags">
                            <span class="job-tag">Full-time</span>
                            <span class="job-tag">Mumbai</span>
                            <span class="job-tag">Operations</span>
                        </div>
                        <p>Manage and optimize our fuel delivery operations across multiple cities, ensuring efficiency and safety standards.</p>
                        <a href="#" class="btn" style="margin-top: 15px;">Apply Now</a>
                    </div>
                    <div class="job-card">
                        <h3>Mobile App Developer</h3>
                        <div class="job-tags">
                            <span class="job-tag">Full-time</span>
                            <span class="job-tag">Bangalore</span>
                            <span class="job-tag">Technology</span>
                        </div>
                        <p>Develop and maintain our customer and delivery partner mobile applications using modern frameworks.</p>
                        <a href="#" class="btn" style="margin-top: 15px;">Apply Now</a>
                    </div>
                    <div class="job-card">
                        <h3>Safety Compliance Officer</h3>
                        <div class="job-tags">
                            <span class="job-tag">Full-time</span>
                            <span class="job-tag">Delhi</span>
                            <span class="job-tag">Compliance</span>
                        </div>
                        <p>Ensure all operations comply with safety regulations and implement best practices for fuel handling.</p>
                        <a href="#" class="btn" style="margin-top: 15px;">Apply Now</a>
                    </div>
                </div>
            </div>
        </section>

        <section class="how-it-works">
            <div class="container">
                <div class="section-title">
                    <h2>Why Work With Us?</h2>
                </div>
                <div class="steps">
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-rocket"></i>
                        </div>
                        <h3>Rapid Growth</h3>
                        <p>Be part of India's fastest growing fuel delivery startup</p>
                    </div>
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-users"></i>
                        </div>
                        <h3>Great Culture</h3>
                        <p>Collaborative environment with focus on innovation</p>
                    </div>
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-graduation-cap"></i>
                        </div>
                        <h3>Learning & Development</h3>
                        <p>Continuous learning opportunities and skill development</p>
                    </div>
                    <div class="step">
                        <div class="step-number">
                            <i class="fas fa-heart"></i>
                        </div>
                        <h3>Impact</h3>
                        <p>Make a real difference in how India accesses energy</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Contact Page -->
    <div id="contact" class="page">
        <section class="contact-hero">
            <div class="container">
                <h2>Get In Touch</h2>
                <p>We're here to help with all your fuel delivery needs</p>
            </div>
        </section>

        <section class="services">
            <div class="container">
                <div class="contact-grid">
                    <div class="contact-info">
                        <h3>Contact Information</h3>
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <div>
                                <h4>Head Office</h4>
                                <p>Guntur,Lakshmi Complex<br> Guntur 522306</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <div>
                                <h4>Phone</h4>
                                <p>+91 6301029913<br>+91 1880080808</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <div>
                                <h4>Email</h4>
                                <p>support@fuelcorner.in<br>business@fuelcorner.in</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-clock"></i>
                            <div>
                                <h4>Business Hours</h4>
                                <p>24/7 Customer Support<br>Operations: 24/7</p>
                            </div>
                        </div>
                    </div>
                    <div class="contact-form">
                        <h3>Send us a Message</h3>
                        <form>
                            <div class="form-group">
                                <label for="name">Full Name</label>
                                <input type="text" id="name" class="form-control" placeholder="Your Name">
                            </div>
                            <div class="form-group">
                                <label for="email">Email Address</label>
                                <input type="email" id="email" class="form-control" placeholder="your@email.com">
                            </div>
                            <div class="form-group">
                                <label for="phone">Phone Number</label>
                                <input type="tel" id="phone" class="form-control" placeholder="+91 XXXXX XXXXX">
                            </div>
                            <div class="form-group">
                                <label for="subject">Subject</label>
                                <input type="text" id="subject" class="form-control" placeholder="Subject">
                            </div>
                            <div class="form-group">
                                <label for="message">Message</label>
                                <textarea id="message" class="form-control" rows="5" placeholder="Your message..."></textarea>
                            </div>
                            <button type="submit" class="btn">Send Message</button>
                        </form>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Download App Modal -->
    <div id="downloadModal" class="modal">
        <div class="modal-content">
            <h3>Download Fuel Corner App</h3>
            <p>To place orders and access all features, please download our mobile app:</p>
            <div class="app-buttons" style="margin: 20px 0;">
                <a href="https://play.google.com/store/apps/details?id=com.fuelcorner.app" class="app-btn" target="_blank">
                    <i class="fab fa-google-play"></i>
                    <div>
                        <small>GET IT ON</small>
                        <div>Google Play</div>
                    </div>
                </a>
                <a href="https://apps.apple.com/app/fuel-corner/id123456789" class="app-btn" target="_blank">
                    <i class="fab fa-apple"></i>
                    <div>
                        <small>Download on the</small>
                        <div>App Store</div>
                    </div>
                </a>
            </div>
            <p style="font-size: 0.9rem; color: var(--gray);">
                Or call us at: <strong>+91 6301029913</strong>
            </p>
            <button onclick="closeModal()" class="btn" style="background: var(--gray); margin-top: 20px;">
                Close
            </button>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Fuel Corner</h3>
                    <p>India's leading on-demand fuel delivery service, making refueling convenient, safe, and efficient across every corner of the country.</p>
                    <div class="social-links">
                        <a href="https://www.facebook.com/lucky.chandu.3720/"><i class="fab fa-facebook-f"></i></a>
                        <a href="https://x.com/home"><i class="fab fa-twitter"></i></a>
                        <a href="https://www.instagram.com/"><i class="fab fa-instagram"></i></a>
                        <a href="https://www.linkedin.com/jobs/"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#" class="nav-link" data-page="home">Home</a></li>
                        <li><a href="#" class="nav-link" data-page="about">About</a></li>
                        <li><a href="#" class="nav-link" data-page="services">Services</a></li>
                        <li><a href="#" class="nav-link" data-page="pricing">Pricing</a></li>
                        <li><a href="#" class="nav-link" data-page="blog">Blog</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Services</h3>
                    <ul class="footer-links">
                        <li><a href="#">Petrol Delivery</a></li>
                        <li><a href="#">Diesel Delivery</a></li>
                        <li><a href="#">Bulk Fuel Delivery</a></li>
                        <li><a href="#">Vehicle Towing</a></li>
                        <li><a href="#">Mechanic Service</a></li>
                        <li><a href="#">Emergency Assistance</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Newsletter</h3>
                    <p>Subscribe to our newsletter for updates and offers.</p>
                    <form>
                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Your Email">
                        </div>
                        <button type="submit" class="btn btn-accent">Subscribe</button>
                    </form>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2024 Fuel Corner. All rights reserved. | /fuel to every corner/</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });

        // Page Navigation
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const targetPage = this.getAttribute('data-page');
                
                document.querySelectorAll('.page').forEach(page => {
                    page.classList.remove('active');
                });
                
                document.getElementById(targetPage).classList.add('active');
                document.querySelector('.nav-links').classList.remove('active');
                window.scrollTo(0, 0);
            });
        });

        // Order Fuel Buttons - Show Download Modal
        document.querySelectorAll('.order-fuel-btn').forEach(btn => {
            btn.addEventListener('click', function(e) {
                e.preventDefault();
                document.getElementById('downloadModal').style.display = 'flex';
            });
        });

        // Download App Buttons - Show Download Modal
        document.querySelectorAll('.download-app-btn').forEach(btn => {
            btn.addEventListener('click', function(e) {
                e.preventDefault();
                document.getElementById('downloadModal').style.display = 'flex';
            });
        });

        // Close Modal
        function closeModal() {
            document.getElementById('downloadModal').style.display = 'none';
        }

        // Enhanced Fuel Calculator with Real Distances
        document.getElementById('calculate-btn').addEventListener('click', function() {
            const fromCity = document.getElementById('from-city').value;
            const toCity = document.getElementById('to-city').value;
            const vehicleType = document.getElementById('vehicle-type').value;
            const fuelType = document.getElementById('fuel-type').value;
            
            if (!fromCity || !toCity || !vehicleType) {
                alert('Please select all required fields.');
                return;
            }
            
            if (fromCity === toCity) {
                alert('Please select different cities for travel.');
                return;
            }
            
            // Real distance matrix between major Indian cities (in km)
            const distances = {
                'mumbai-delhi': 1400,
                'mumbai-bangalore': 980,
                'mumbai-hyderabad': 710,
                'mumbai-chennai': 1300,
                'mumbai-kolkata': 2000,
                'delhi-bangalore': 2150,
                'delhi-hyderabad': 1580,
                'delhi-chennai': 2200,
                'delhi-kolkata': 1500,
                'bangalore-hyderabad': 570,
                'bangalore-chennai': 350,
                'bangalore-kolkata': 1860,
                'hyderabad-chennai': 630,
                'hyderabad-kolkata': 1490,
                'chennai-kolkata': 1670
            };
            
            const distanceKey = [fromCity, toCity].sort().join('-');
            const distance = distances[distanceKey] || 500; // Default distance
            
            // Vehicle mileage ranges
            const mileageRanges = {
                'hatchback': 18,
                'sedan': 15,
                'suv': 12,
                'bike': 45
            };
            
            const mileage = mileageRanges[vehicleType];
            
            // Fuel prices
            const petrolPrice = 106.31;
            const dieselPrice = 94.27;
            
            const fuelRequired = (distance / mileage).toFixed(2);
            const fuelCost = (fuelType === 'petrol' ? fuelRequired * petrolPrice : fuelRequired * dieselPrice).toFixed(2);
            
            // Update results
            document.getElementById('distance-result').textContent = `${distance} km`;
            document.getElementById('fuel-result').textContent = `${fuelRequired} liters`;
            document.getElementById('total-cost').textContent = `₹${fuelCost}`;
            document.getElementById('calculator-results').style.display = 'block';
        });

        // Original Simple Calculator
        document.getElementById('simple-calculate-btn').addEventListener('click', function() {
            const distance = parseFloat(document.getElementById('distance').value);
            const mileage = parseFloat(document.getElementById('mileage').value);
            const fuelType = document.getElementById('simple-fuel-type').value;
            
            if (isNaN(distance) || isNaN(mileage) || distance <= 0 || mileage <= 0) {
                alert('Please enter valid values for distance and mileage.');
                return;
            }
            
            // Approximate fuel prices in India
            const petrolPrice = 106.31;
            const dieselPrice = 94.27;
            
            const fuelRequired = distance / mileage;
            const fuelCost = fuelType === 'petrol' ? fuelRequired * petrolPrice : fuelRequired * dieselPrice;
            
            const resultElement = document.getElementById('simple-result');
            resultElement.innerHTML = `
                <h3>Estimated Fuel Cost</h3>
                <p>For ${distance} km with ${mileage} km/l mileage:</p>
                <p>Fuel required: ${fuelRequired.toFixed(2)} liters</p>
                <p>Total cost: ₹${fuelCost.toFixed(2)}</p>
                <p>Fuel type: ${fuelType.charAt(0).toUpperCase() + fuelType.slice(1)}</p>
            `;
            resultElement.style.display = 'block';
        });

        // Testimonial Carousel
        let currentSlide = 0;
        const slides = document.querySelectorAll('.testimonial-slide');
        const dots = document.querySelectorAll('.carousel-dot');

        function showSlide(n) {
            slides.forEach(slide => slide.classList.remove('active'));
            dots.forEach(dot => dot.classList.remove('active'));
            
            currentSlide = (n + slides.length) % slides.length;
            slides[currentSlide].classList.add('active');
            dots[currentSlide].classList.add('active');
        }

        // Auto-advance carousel
        setInterval(() => {
            showSlide(currentSlide + 1);
        }, 5000);

        // Dot controls
        dots.forEach((dot, index) => {
            dot.addEventListener('click', () => {
                showSlide(index);
            });
        });

        // Close modal when clicking outside
        window.addEventListener('click', function(e) {
            if (e.target === document.getElementById('downloadModal')) {
                closeModal();
            }
        });

        // Back to Top Button
        const backToTopButton = document.getElementById('backToTop');
        
        window.addEventListener('scroll', function() {
            if (window.pageYOffset > 300) {
                backToTopButton.classList.add('visible');
            } else {
                backToTopButton.classList.remove('visible');
            }
            
            // Header scroll effect
            if (window.pageYOffset > 100) {
                document.querySelector('header').classList.add('scrolled');
            } else {
                document.querySelector('header').classList.remove('scrolled');
            }
            
            // Glow effect activation
            document.querySelectorAll('.glow-section, .glow-media-container').forEach(element => {
                const rect = element.getBoundingClientRect();
                if (rect.top < window.innerHeight * 0.8 && rect.bottom > 0) {
                    element.classList.add('visible');
                }
            });
        });
        
        backToTopButton.addEventListener('click', function() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });

        // Add smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 100,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Enhanced intersection observer for Apple-like animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    
                    // Stagger children animations
                    const children = entry.target.querySelectorAll('.text-reveal, .service-card');
                    children.forEach((child, index) => {
                        setTimeout(() => {
                            child.classList.add('revealed');
                        }, index * 100);
                    });
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('section').forEach(section => {
            observer.observe(section);
        });

        // Enhanced hover effects for buttons
        document.querySelectorAll('.btn').forEach(button => {
            button.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-2px) scale(1.02)';
            });
            
            button.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0) scale(1)';
            });
        });

        // Apple-like page load animation
        window.addEventListener('load', () => {
            document.body.style.opacity = '0';
            document.body.style.transition = 'opacity 0.6s var(--ease-out-expo)';
            
            setTimeout(() => {
                document.body.style.opacity = '1';
            }, 100);
        });

        // Add floating animation to multiple elements
        document.addEventListener('DOMContentLoaded', function() {
            const floatingElements = document.querySelectorAll('.floating');
            floatingElements.forEach((el, index) => {
                el.style.animationDelay = `${index * 0.5}s`;
            });
            
            // Add hover effects to vectors
            const vectors = document.querySelectorAll('.vector-image');
            vectors.forEach(vector => {
                vector.addEventListener('mouseenter', function() {
                    this.style.transform = 'scale(1.05)';
                    this.style.transition = 'transform 0.3s ease';
                });
                
                vector.addEventListener('mouseleave', function() {
                    this.style.transform = 'scale(1)';
                });
            });
        });
    </script>
</body>
</html>
