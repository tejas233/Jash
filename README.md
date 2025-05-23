<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Free online AI image generator and compression tool. Optimize your images with different compression levels for web and mobile.">
    <meta name="keywords" content="AI image generator, image compression, optimize images, reduce image size, web image tool">
    <meta name="author" content="AI Image Tools">
    <meta name="robots" content="index, follow">
    <title>AI Image Generator & Compression Tool | Optimize Your Images</title>
    <link rel="canonical" href="https://yourdomain.com" />
    
    <!-- Open Graph / Social Media Meta Tags -->
    <meta property="og:title" content="AI Image Generator & Compression Tool">
    <meta property="og:description" content="Free online AI image generator and compression tool. Optimize your images with different compression levels.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://yourdomain.com">
    <meta property="og:image" content="https://yourdomain.com/images/preview.jpg">
    
    <!-- Favicon -->
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary-color: #4a6bff;
            --secondary-color: #f8f9fa;
            --accent-color: #ff6b6b;
            --text-color: #333;
            --light-text: #777;
            --border-color: #e0e0e0;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: #f5f7ff;
            padding: 0;
            margin: 0;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background-color: white;
            box-shadow: var(--shadow);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }
        
        .logo span {
            color: var(--accent-color);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--primary-color);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
        }
        
        .hero {
            text-align: center;
            padding: 60px 0 40px;
            background: linear-gradient(135deg, #f5f7ff 0%, #e8ecff 100%);
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: var(--primary-color);
        }
        
        .hero p {
            font-size: 1.1rem;
            color: var(--light-text);
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .ad-banner {
            background-color: white;
            padding: 15px;
            margin: 20px auto;
            border-radius: 8px;
            box-shadow: var(--shadow);
            text-align: center;
            max-width: 1000px;
        }
        
        .tool-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin: 40px 0;
        }
        
        .tool-section {
            flex: 1;
            min-width: 300px;
            background-color: white;
            border-radius: 10px;
            padding: 25px;
            box-shadow: var(--shadow);
        }
        
        .section-title {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--primary-color);
            display: flex;
            align-items: center;
        }
        
        .section-title i {
            margin-right: 10px;
        }
        
        .upload-area {
            border: 2px dashed var(--border-color);
            border-radius: 8px;
            padding: 30px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
            margin-bottom: 20px;
        }
        
        .upload-area:hover {
            border-color: var(--primary-color);
            background-color: rgba(74, 107, 255, 0.05);
        }
        
        .upload-area i {
            font-size: 48px;
            color: var(--primary-color);
            margin-bottom: 15px;
        }
        
        .upload-area p {
            color: var(--light-text);
        }
        
        .upload-area.active {
            border-color: var(--primary-color);
            background-color: rgba(74, 107, 255, 0.05);
        }
        
        #fileInput {
            display: none;
        }
        
        .settings {
            margin-bottom: 20px;
        }
        
        .setting-group {
            margin-bottom: 15px;
        }
        
        .setting-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .slider {
            flex: 1;
            -webkit-appearance: none;
            height: 8px;
            border-radius: 4px;
            background: #ddd;
            outline: none;
        }
        
        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: var(--primary-color);
            cursor: pointer;
        }
        
        .slider-value {
            min-width: 40px;
            text-align: center;
            font-weight: 600;
        }
        
        .checkbox-group {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
        }
        
        .checkbox-group input {
            margin-right: 10px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 6px;
            font-size: 16px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s;
            text-align: center;
        }
        
        .btn:hover {
            background-color: #3a5bef;
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
        }
        
        .btn-block {
            display: block;
            width: 100%;
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
        }
        
        .btn-outline:hover {
            background-color: var(--primary-color);
            color: white;
        }
        
        .preview-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }
        
        .image-preview {
            flex: 1;
            min-width: 250px;
        }
        
        .image-preview h3 {
            margin-bottom: 10px;
            font-size: 1.1rem;
        }
        
        .image-box {
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 10px;
            margin-bottom: 10px;
            background-color: var(--secondary-color);
            text-align: center;
        }
        
        .image-box img {
            max-width: 100%;
            height: auto;
            display: block;
            margin: 0 auto;
            max-height: 300px;
        }
        
        .image-info {
            display: flex;
            justify-content: space-between;
            font-size: 0.9rem;
            color: var(--light-text);
            margin-top: 10px;
        }
        
        .result-actions {
            display: flex;
            gap: 10px;
            margin-top: 15px;
        }
        
        .result-actions .btn {
            flex: 1;
            padding: 10px;
            font-size: 14px;
        }
        
        .ad-sidebar {
            width: 300px;
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: var(--shadow);
            text-align: center;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 60px 0;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: var(--shadow);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
        }
        
        .feature-card i {
            font-size: 40px;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            font-size: 1.3rem;
            margin-bottom: 15px;
        }
        
        .feature-card p {
            color: var(--light-text);
        }
        
        footer {
            background-color: #2a3a7a;
            color: white;
            padding: 50px 0 20px;
            margin-top: 60px;
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
            margin-bottom: 30px;
        }
        
        .footer-column {
            flex: 1;
            min-width: 200px;
        }
        
        .footer-column h3 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 2px;
            background-color: var(--accent-color);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: white;
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        .loading {
            display: none;
            text-align: center;
            margin: 20px 0;
        }
        
        .loading-spinner {
            border: 4px solid rgba(0, 0, 0, 0.1);
            border-radius: 50%;
            border-top: 4px solid var(--primary-color);
            width: 40px;
            height: 40px;
            animation: spin 1s linear infinite;
            margin: 0 auto 15px;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        /* Responsive styles */
        @media (max-width: 992px) {
            .tool-container {
                flex-direction: column;
            }
            
            .ad-sidebar {
                width: 100%;
                order: -1;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 768px) {
            nav ul {
                display: none;
                position: absolute;
                top: 70px;
                left: 0;
                right: 0;
                background-color: white;
                flex-direction: column;
                padding: 20px;
                box-shadow: var(--shadow);
            }
            
            nav ul.show {
                display: flex;
            }
            
            nav ul li {
                margin: 10px 0;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero {
                padding: 40px 0 20px;
            }
            
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .preview-container {
                flex-direction: column;
            }
        }
        
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 1.5rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .tool-section, .feature-card {
                padding: 20px;
            }
            
            .btn {
                padding: 10px 15px;
                font-size: 14px;
            }
        }
    </style>
    
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <div class="container header-content">
            <a href="#" class="logo">AI<span>Image</span>Tools</a>
            <button class="mobile-menu-btn" id="menuBtn">
                <i class="fas fa-bars"></i>
            </button>
            <nav>
                <ul id="navMenu">
                    <li><a href="#">Home</a></li>
                    <li><a href="#tool">Tool</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <section class="hero">
        <div class="container">
            <h1>AI-Powered Image Generator & Compression Tool</h1>
            <p>Generate stunning AI images or optimize your existing ones with our advanced compression technology. Perfect for web developers, designers, and content creators.</p>
            
            <div class="ad-banner">
                <!-- Replace with your Google AdSense ad unit -->
                <!-- AdSense Header Banner -->
                <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_PUBLISHER_ID"></script>
                <!-- AI Image Tool Banner -->
                <ins class="adsbygoogle"
                     style="display:block"
                     data-ad-client="ca-pub-YOUR_PUBLISHER_ID"
                     data-ad-slot="YOUR_AD_SLOT_ID"
                     data-ad-format="auto"
                     data-full-width-responsive="true"></ins>
                <script>
                     (adsbygoogle = window.adsbygoogle || []).push({});
                </script>
            </div>
        </div>
    </section>
    
    <main class="container" id="tool">
        <div class="tool-container">
            <div class="tool-section">
                <h2 class="section-title"><i class="fas fa-image"></i> Image Generator</h2>
                
                <div class="settings">
                    <div class="setting-group">
                        <label for="prompt">Image Description</label>
                        <textarea id="prompt" rows="3" placeholder="Describe the image you want to generate..." class="upload-area" style="cursor: text;"></textarea>
                    </div>
                    
                    <div class="setting-group">
                        <label for="style">Art Style</label>
                        <select id="style" class="upload-area" style="padding: 15px; width: 100%;">
                            <option value="realistic">Realistic</option>
                            <option value="cartoon">Cartoon</option>
                            <option value="anime">Anime</option>
                            <option value="painting">Painting</option>
                            <option value="3d-render">3D Render</option>
                            <option value="pixel-art">Pixel Art</option>
                        </select>
                    </div>
                    
                    <div class="setting-group">
                        <label for="size">Image Size</label>
                        <select id="size" class="upload-area" style="padding: 15px; width: 100%;">
                            <option value="512x512">512x512 (Square)</option>
                            <option value="768x512">768x512 (Landscape)</option>
                            <option value="512x768">512x768 (Portrait)</option>
                            <option value="1024x1024">1024x1024 (HD)</option>
                        </select>
                    </div>
                </div>
                
                <button id="generateBtn" class="btn btn-block">
                    <i class="fas fa-magic"></i> Generate Image
                </button>
                
                <div class="loading" id="generatingLoader">
                    <div class="loading-spinner"></div>
                    <p>Generating your image... This may take a few seconds.</p>
                </div>
                
                <div class="preview-container" id="generatedPreview" style="display: none;">
                    <div class="image-preview">
                        <h3>Generated Image</h3>
                        <div class="image-box">
                            <img id="generatedImage" src="" alt="Generated image">
                        </div>
                        <div class="result-actions">
                            <button class="btn btn-outline" id="downloadGenerated">
                                <i class="fas fa-download"></i> Download
                            </button>
                            <button class="btn" id="compressGenerated">
                                <i class="fas fa-compress-alt"></i> Compress
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="tool-section">
                <h2 class="section-title"><i class="fas fa-compress-alt"></i> Image Compression</h2>
                
                <div class="upload-area" id="dropArea">
                    <i class="fas fa-cloud-upload-alt"></i>
                    <p>Drag & drop your image here or click to browse</p>
                    <input type="file" id="fileInput" accept="image/*">
                </div>
                
                <div class="settings">
                    <div class="setting-group">
                        <label for="compressionLevel">Compression Level: <span id="compressionValue">70</spa# Jash
