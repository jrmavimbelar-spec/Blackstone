# Blackstone
my demo website 
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blackstone Legal | Justice. Strategy. Results.</title>
    <meta name="description" content="Elite legal representation for Fortune 500 companies and ultra-high-net-worth individuals. 25+ years of excellence in corporate, criminal, and family law.">
    
    <!-- Open Graph -->
    <meta property="og:title" content="Blackstone Legal | Justice. Strategy. Results.">
    <meta property="og:description" content="Elite legal representation trusted by industry leaders worldwide.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://blackstonelegal.com">
    <meta property="og:image" content="https://blackstonelegal.com/assets/og-image.jpg">
    
    <!-- Schema Markup -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "LegalService",
        "name": "Blackstone Legal",
        "description": "Elite legal representation for Fortune 500 companies and ultra-high-net-worth individuals.",
        "url": "https://blackstonelegal.com",
        "telephone": "+1-800-555-0199",
        "email": "contact@blackstonelegal.com",
        "address": {
            "@type": "PostalAddress",
            "streetAddress": "350 Fifth Avenue, Suite 7600",
            "addressLocality": "New York",
            "addressRegion": "NY",
            "postalCode": "10118",
            "addressCountry": "US"
        },
        "openingHours": "Mo-Fr 08:00-20:00",
        "priceRange": "$$$$",
        "aggregateRating": {
            "@type": "AggregateRating",
            "ratingValue": "4.9",
            "reviewCount": "500"
        }
    }
    </script>

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;0,700;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        navy: {
                            900: '#0B1F3A',
                            800: '#0F2847',
                            700: '#15325A',
                            600: '#1A3D6B',
                        },
                        gold: {
                            DEFAULT: '#C9A227',
                            light: '#D4B43A',
                            dark: '#A88820',
                        },
                    },
                    fontFamily: {
                        serif: ['Cormorant Garamond', 'serif'],
                        sans: ['Inter', 'sans-serif'],
                    },
                    animation: {
                        'fade-in-up': 'fadeInUp 0.8s ease-out forwards',
                        'counter': 'counter 2s ease-out forwards',
                    },
                    keyframes: {
                        fadeInUp: {
                            '0%': { opacity: '0', transform: 'translateY(30px)' },
                            '100%': { opacity: '1', transform: 'translateY(0)' },
                        }
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Styles for Premium Feel */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0B1F3A;
            color: #ffffff;
            overflow-x: hidden;
        }

        .font-serif {
            font-family: 'Cormorant Garamond', serif;
        }

        /* Glassmorphism */
        .glass {
            background: rgba(11, 31, 58, 0.7);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(201, 162, 39, 0.1);
        }

        .glass-light {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }

        /* Loading Screen */
        #loading-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #0B1F3A;
            z-index: 9999;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            transition: opacity 0.8s ease-out, visibility 0.8s;
        }

        #loading-screen.hidden {
            opacity: 0;
            visibility: hidden;
        }

        .loader-line {
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, transparent, #C9A227, transparent);
            animation: loadLine 1.5s ease-in-out forwards;
        }

        @keyframes loadLine {
            0% { width: 0; opacity: 0; }
            50% { opacity: 1; }
            100% { width: 200px; opacity: 0; }
        }

        /* Hero Parallax */
        .hero-bg {
            background-image: linear-gradient(rgba(11, 31, 58, 0.85), rgba(11, 31, 58, 0.9)), url('https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
        }

        /* Scroll Reveal */
        .reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* Button Ripple */
        .btn-ripple {
            position: relative;
            overflow: hidden;
        }

        .btn-ripple::after {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }

        .btn-ripple:active::after {
            width: 300px;
            height: 300px;
        }

        /* Practice Area Cards */
        .practice-card {
            transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .practice-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(201, 162, 39, 0.15);
            border-color: rgba(201, 162, 39, 0.3);
        }

        .practice-card .icon-wrapper {
            transition: all 0.4s ease;
        }

        .practice-card:hover .icon-wrapper {
            background: rgba(201, 162, 39, 0.15);
            transform: scale(1.1);
        }

        /* Attorney Cards */
        .attorney-card {
            transition: all 0.5s ease;
        }

        .attorney-card:hover {
            transform: translateY(-8px);
        }

        .attorney-card:hover .attorney-overlay {
            opacity: 1;
        }

        .attorney-overlay {
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        /* Testimonial Carousel */
        .testimonial-slide {
            display: none;
            animation: fadeIn 0.6s ease;
        }

        .testimonial-slide.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateX(20px); }
            to { opacity: 1; transform: translateX(0); }
        }

        /* Timeline */
        .timeline-item {
            position: relative;
            padding-left: 40px;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(to bottom, #C9A227, rgba(201, 162, 39, 0.1));
        }

        .timeline-dot {
            position: absolute;
            left: -6px;
            top: 0;
            width: 14px;
            height: 14px;
            background: #C9A227;
            border: 3px solid #0B1F3A;
            border-radius: 50%;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: #0B1F3A;
        }

        ::-webkit-scrollbar-thumb {
            background: #1A3D6B;
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: #C9A227;
        }

        /* Mobile Menu */
        .mobile-menu {
            transform: translateX(100%);
            transition: transform 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .mobile-menu.open {
            transform: translateX(0);
        }

        /* Form Focus States */
        .form-input:focus {
            outline: none;
            border-color: #C9A227;
            box-shadow: 0 0 0 3px rgba(201, 162, 39, 0.1);
        }

        /* Gold Gradient Text */
        .text-gold-gradient {
            background: linear-gradient(135deg, #C9A227 0%, #D4B43A 50%, #A88820 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Subtle grain texture */
        .grain {
            position: relative;
        }

        .grain::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.03;
            background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
            pointer-events: none;
            z-index: 1;
        }

        .grain > * {
            position: relative;
            z-index: 2;
        }
    </style>
</head>
<body class="antialiased">

    <!-- Loading Screen -->
    <div id="loading-screen">
        <div class="text-center">
            <h1 class="font-serif text-4xl md:text-5xl text-white mb-2 tracking-wider">BLACKSTONE</h1>
            <p class="text-gold text-sm tracking-[0.3em] uppercase mb-8">Legal</p>
            <div class="loader-line mx-auto"></div>
        </div>
    </div>

    <!-- Navigation -->
    <nav id="navbar" class="fixed w-full z-50 transition-all duration-500">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-24">
                <!-- Logo -->
                <div class="flex-shrink-0 flex items-center">
                    <a href="#home" class="flex flex-col items-start">
                        <span class="font-serif text-2xl md:text-3xl text-white tracking-wider">BLACKSTONE</span>
                        <span class="text-gold text-[10px] tracking-[0.4em] uppercase -mt-1">Legal</span>
                    </a>
                </div>

                <!-- Desktop Menu -->
                <div class="hidden lg:flex items-center space-x-8">
                    <a href="#home" class="text-sm text-gray-300 hover:text-gold transition-colors duration-300 tracking-wide">Home</a>
                    <a href="#about" class="text-sm text-gray-300 hover:text-gold transition-colors duration-300 tracking-wide">About</a>
                    <a href="#practice" class="text-sm text-gray-300 hover:text-gold transition-colors duration-300 tracking-wide">Practice Areas</a>
                    <a href="#attorneys" class="text-sm text-gray-300 hover:text-gold transition-colors duration-300 tracking-wide">Attorneys</a>
                    <a href="#results" class="text-sm text-gray-300 hover:text-gold transition-colors duration-300 tracking-wide">Results</a>
                    <a href="#testimonials" class="text-sm text-gray-300 hover:text-gold transition-colors duration-300 tracking-wide">Testimonials</a>
                    <a href="#insights" class="text-sm text-gray-300 hover:text-gold transition-colors duration-300 tracking-wide">Insights</a>
                    <a href="#contact" class="ml-4 px-6 py-2.5 border border-gold text-gold text-sm tracking-wider hover:bg-gold hover:text-navy-900 transition-all duration-300 btn-ripple">Contact</a>
                </div>

                <!-- Mobile Menu Button -->
                <div class="lg:hidden">
                    <button id="mobile-menu-btn" class="text-white hover:text-gold transition-colors p-2">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="mobile-menu fixed top-0 right-0 w-full sm:w-80 h-full bg-navy-900 z-50 shadow-2xl">
            <div class="p-8">
                <div class="flex justify-between items-center mb-12">
                    <span class="font-serif text-xl text-white">Menu</span>
                    <button id="close-menu-btn" class="text-white hover:text-gold transition-colors">
                        <i class="fas fa-times text-2xl"></i>
                    </button>
                </div>
                <div class="flex flex-col space-y-6">
                    <a href="#home" class="text-lg text-gray-300 hover:text-gold transition-colors py-2 border-b border-navy-700">Home</a>
                    <a href="#about" class="text-lg text-gray-300 hover:text-gold transition-colors py-2 border-b border-navy-700">About</a>
                    <a href="#practice" class="text-lg text-gray-300 hover:text-gold transition-colors py-2 border-b border-navy-700">Practice Areas</a>
                    <a href="#attorneys" class="text-lg text-gray-300 hover:text-gold transition-colors py-2 border-b border-navy-700">Attorneys</a>
                    <a href="#results" class="text-lg text-gray-300 hover:text-gold transition-colors py-2 border-b border-navy-700">Results</a>
                    <a href="#testimonials" class="text-lg text-gray-300 hover:text-gold transition-colors py-2 border-b border-navy-700">Testimonials</a>
                    <a href="#insights" class="text-lg text-gray-300 hover:text-gold transition-colors py-2 border-b border-navy-700">Insights</a>
                    <a href="#contact" class="mt-4 px-6 py-3 border border-gold text-gold text-center tracking-wider hover:bg-gold hover:text-navy-900 transition-all">Contact Us</a>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="relative h-screen min-h-[700px] flex items-center justify-center hero-bg grain">
        <div class="absolute inset-0 bg-gradient-to-b from-transparent via-navy-900/50 to-navy-900"></div>
        
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <div class="reveal active">
                <p class="text-gold text-sm md:text-base tracking-[0.4em] uppercase mb-6">Justice. Strategy. Results.</p>
                <h1 class="font-serif text-4xl md:text-6xl lg:text-7xl text-white leading-tight mb-8 max-w-5xl mx-auto">
                    Protecting Your Future With <span class="text-gold-gradient">Elite Legal Representation</span>
                </h1>
                <p class="text-gray-300 text-lg md:text-xl max-w-3xl mx-auto mb-12 leading-relaxed">
                    Trusted by individuals and businesses for exceptional legal advice and powerful courtroom advocacy. We deliver results that matter.
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <a href="#contact" class="px-8 py-4 bg-gold text-navy-900 font-medium tracking-wider hover:bg-gold-light transition-all duration-300 btn-ripple shadow-lg shadow-gold/20">
                        Book a Consultation
                    </a>
                    <a href="#practice" class="px-8 py-4 border border-white/30 text-white tracking-wider hover:bg-white/10 transition-all duration-300 btn-ripple">
                        Our Practice Areas
                    </a>
                </div>
            </div>
        </div>

        <!-- Scroll Indicator -->
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
            <div class="w-6 h-10 border-2 border-white/30 rounded-full flex justify-center pt-2">
                <div class="w-1 h-2 bg-gold rounded-full animate-pulse"></div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-24 md:py-32 bg-navy-900 grain">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid lg:grid-cols-2 gap-16 items-center">
                <div class="reveal">
                    <p class="text-gold text-sm tracking-[0.3em] uppercase mb-4">About Blackstone</p>
                    <h2 class="font-serif text-4xl md:text-5xl text-white mb-8 leading-tight">
                        A Legacy of Excellence in <span class="text-gold-gradient">Legal Practice</span>
                    </h2>
                    <p class="text-gray-300 text-lg leading-relaxed mb-6">
                        For over two decades, Blackstone Legal has stood at the pinnacle of legal excellence. Our firm represents Fortune 500 companies, ultra-high-net-worth individuals, and businesses navigating complex legal landscapes.
                    </p>
                    <p class="text-gray-400 leading-relaxed mb-8">
                        We combine deep industry knowledge with strategic thinking to deliver outcomes that protect your interests and advance your objectives. Our attorneys are recognized leaders in their fields, committed to the highest standards of professionalism.
                    </p>
                    <div class="flex items-center gap-8">
                        <div>
                            <p class="font-serif text-3xl text-gold">25+</p>
                            <p class="text-sm text-gray-400 mt-1">Years Experience</p>
                        </div>
                        <div class="w-px h-12 bg-navy-700"></div>
                        <div>
                            <p class="font-serif text-3xl text-gold">150+</p>
                            <p class="text-sm text-gray-400 mt-1">Expert Attorneys</p>
                        </div>
                    </div>
                </div>
                <div class="reveal relative">
                    <div class="absolute -inset-4 bg-gold/10 rounded-lg transform rotate-3"></div>
                    <img src="https://images.unsplash.com/photo-1505664194779-8beaceb93744?ixlib=rb-4.0.3&auto=format&fit=crop&w=1740&q=80" alt="Modern Law Office" class="relative rounded-lg shadow-2xl w-full h-[500px] object-cover">
                    <div class="absolute bottom-8 left-8 right-8 glass p-6 rounded-lg">
                        <p class="text-white font-serif text-xl italic">"Excellence is not an act, but a habit."</p>
                        <p class="text-gold text-sm mt-2">— Aristotle</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Practice Areas -->
    <section id="practice" class="py-24 md:py-32 bg-navy-800 grain">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-20 reveal">
                <p class="text-gold text-sm tracking-[0.3em] uppercase mb-4">Our Expertise</p>
                <h2 class="font-serif text-4xl md:text-5xl text-white">Practice Areas</h2>
                <div class="w-24 h-px bg-gold mx-auto mt-8"></div>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Corporate Law -->
                <div class="practice-card glass-light p-8 rounded-lg cursor-pointer reveal">
                    <div class="icon-wrapper w-16 h-16 rounded-full bg-navy-700 flex items-center justify-center mb-6">
                        <i class="fas fa-briefcase text-2xl text-gold"></i>
                    </div>
                    <h3 class="font-serif text-xl text-white mb-3">Corporate Law</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Mergers, acquisitions, corporate governance, and strategic business transactions.</p>
                </div>

                <!-- Family Law -->
                <div class="practice-card glass-light p-8 rounded-lg cursor-pointer reveal">
                    <div class="icon-wrapper w-16 h-16 rounded-full bg-navy-700 flex items-center justify-center mb-6">
                        <i class="fas fa-users text-2xl text-gold"></i>
                    </div>
                    <h3 class="font-serif text-xl text-white mb-3">Family Law</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Divorce, custody, prenuptial agreements, and family estate matters.</p>
                </div>

                <!-- Criminal Defense -->
                <div class="practice-card glass-light p-8 rounded-lg cursor-pointer reveal">
                    <div class="icon-wrapper w-16 h-16 rounded-full bg-navy-700 flex items-center justify-center mb-6">
                        <i class="fas fa-shield-alt text-2xl text-gold"></i>
                    </div>
                    <h3 class="font-serif text-xl text-white mb-3">Criminal Defense</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">White-collar crimes, federal charges, and complex criminal litigation.</p>
                </div>

                <!-- Property Law -->
                <div class="practice-card glass-light p-8 rounded-lg cursor-pointer reveal">
                    <div class="icon-wrapper w-16 h-16 rounded-full bg-navy-700 flex items-center justify-center mb-6">
                        <i class="fas fa-building text-2xl text-gold"></i>
                    </div>
                    <h3 class="font-serif text-xl text-white mb-3">Property Law</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Real estate transactions, zoning, land use, and property disputes.</p>
                </div>

                <!-- Civil Litigation -->
                <div class="practice-card glass-light p-8 rounded-lg cursor-pointer reveal">
                    <div class="icon-wrapper w-16 h-16 rounded-full bg-navy-700 flex items-center justify-center mb-6">
                        <i class="fas fa-gavel text-2xl text-gold"></i>
                    </div>
                    <h3 class="font-serif text-xl text-white mb-3">Civil Litigation</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Complex commercial disputes, class actions, and appellate advocacy.</p>
                </div>

                <!-- Employment Law -->
                <div class="practice-card glass-light p-8 rounded-lg cursor-pointer reveal">
                    <div class="icon-wrapper w-16 h-16 rounded-full bg-navy-700 flex items-center justify-center mb-6">
                        <i class="fas fa-user-tie text-2xl text-gold"></i>
                    </div>
                    <h3 class="font-serif text-xl text-white mb-3">Employment Law</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Executive contracts, discrimination claims, and labor relations.</p>
                </div>

                <!-- Personal Injury -->
                <div class="practice-card glass-light p-8 rounded-lg cursor-pointer reveal">
                    <div class="icon-wrapper w-16 h-16 rounded-full bg-navy-700 flex items-center justify-center mb-6">
                        <i class="fas fa-heartbeat text-2xl text-gold"></i>
                    </div>
                    <h3 class="font-serif text-xl text-white mb-3">Personal Injury</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Catastrophic injuries, medical malpractice, and wrongful death claims.</p>
                </div>

                <!-- Estate Planning -->
                <div class="practice-card glass-light p-8 rounded-lg cursor-pointer reveal">
                    <div class="icon-wrapper w-16 h-16 rounded-full bg-navy-700 flex items-center justify-center mb-6">
                        <i class="fas fa-file-contract text-2xl text-gold"></i>
                    </div>
                    <h3 class="font-serif text-xl text-white mb-3">Estate Planning</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Trusts, wills, wealth preservation, and succession planning.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Attorneys Section -->
    <section id="attorneys" class="py-24 md:py-32 bg-navy-900 grain">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-20 reveal">
                <p class="text-gold text-sm tracking-[0.3em] uppercase mb-4">Our Team</p>
                <h2 class="font-serif text-4xl md:text-5xl text-white">Distinguished Attorneys</h2>
                <div class="w-24 h-px bg-gold mx-auto mt-8"></div>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Attorney 1 -->
                <div class="attorney-card reveal">
                    <div class="relative overflow-hidden rounded-lg mb-6">
                        <img src="https://images.unsplash.com/photo-1560250097-0b93528c311a?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="James Blackstone" class="w-full h-[400px] object-cover">
                        <div class="attorney-overlay absolute inset-0 bg-navy-900/80 flex items-center justify-center">
                            <div class="flex space-x-4">
                                <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-navy-900 transition-all text-white">
                                    <i class="fab fa-linkedin-in"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-navy-900 transition-all text-white">
                                    <i class="fab fa-twitter"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <h3 class="font-serif text-xl text-white">James Blackstone</h3>
                    <p class="text-gold text-sm mb-2">Managing Partner</p>
                    <p class="text-gray-400 text-sm">Corporate Law & M&A</p>
                </div>

                <!-- Attorney 2 -->
                <div class="attorney-card reveal">
                    <div class="relative overflow-hidden rounded-lg mb-6">
                        <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Sarah Chen" class="w-full h-[400px] object-cover">
                        <div class="attorney-overlay absolute inset-0 bg-navy-900/80 flex items-center justify-center">
                            <div class="flex space-x-4">
                                <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-navy-900 transition-all text-white">
                                    <i class="fab fa-linkedin-in"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-navy-900 transition-all text-white">
                                    <i class="fab fa-twitter"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <h3 class="font-serif text-xl text-white">Sarah Chen</h3>
                    <p class="text-gold text-sm mb-2">Senior Partner</p>
                    <p class="text-gray-400 text-sm">Criminal Defense</p>
                </div>

                <!-- Attorney 3 -->
                <div class="attorney-card reveal">
                    <div class="relative overflow-hidden rounded-lg mb-6">
                        <img src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Michael Torres" class="w-full h-[400px] object-cover">
                        <div class="attorney-overlay absolute inset-0 bg-navy-900/80 flex items-center justify-center">
                            <div class="flex space-x-4">
                                <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-navy-900 transition-all text-white">
                                    <i class="fab fa-linkedin-in"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-navy-900 transition-all text-white">
                                    <i class="fab fa-twitter"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <h3 class="font-serif text-xl text-white">Michael Torres</h3>
                    <p class="text-gold text-sm mb-2">Partner</p>
                    <p class="text-gray-400 text-sm">Litigation & Appeals</p>
                </div>

                <!-- Attorney 4 -->
                <div class="attorney-card reveal">
                    <div class="relative overflow-hidden rounded-lg mb-6">
                        <img src="https://images.unsplash.com/photo-1580489944761-15a19d654956?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Emily Watson" class="w-full h-[400px] object-cover">
                        <div class="attorney-overlay absolute inset-0 bg-navy-900/80 flex items-center justify-center">
                            <div class="flex space-x-4">
                                <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-navy-900 transition-all text-white">
                                    <i class="fab fa-linkedin-in"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center hover:bg-gold hover:text-navy-900 transition-all text-white">
                                    <i class="fab fa-twitter"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <h3 class="font-serif text-xl text-white">Emily Watson</h3>
                    <p class="text-gold text-sm mb-2">Partner</p>
                    <p class="text-gray-400 text-sm">Family Law</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Choose Us / Statistics -->
    <section class="py-24 md:py-32 bg-navy-800 grain relative overflow-hidden">
        <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1497366216548-37526070297c?ixlib=rb-4.0.3&auto=format&fit=crop&w=2069&q=80')] bg-cover bg-center opacity-10"></div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center mb-20 reveal">
                <p class="text-gold text-sm tracking-[0.3em] uppercase mb-4">Our Track Record</p>
                <h2 class="font-serif text-4xl md:text-5xl text-white">Why Choose Blackstone</h2>
                <div class="w-24 h-px bg-gold mx-auto mt-8"></div>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div class="text-center reveal">
                    <div class="font-serif text-5xl md:text-6xl text-gold mb-4 counter" data-target="25">0</div>
                    <p class="text-white text-lg mb-2">Years Experience</p>
                    <p class="text-gray-400 text-sm">Decades of legal excellence</p>
                </div>
                <div class="text-center reveal">
                    <div class="font-serif text-5xl md:text-6xl text-gold mb-4 counter" data-target="5000">0</div>
                    <p class="text-white text-lg mb-2">Cases Won</p>
                    <p class="text-gray-400 text-sm">Proven track record</p>
                </div>
                <div class="text-center reveal">
                    <div class="font-serif text-5xl md:text-6xl text-gold mb-4 counter" data-target="98">0</div>
                    <p class="text-white text-lg mb-2">% Client Satisfaction</p>
                    <p class="text-gray-400 text-sm">Exceptional service</p>
                </div>
                <div class="text-center reveal">
                    <div class="font-serif text-5xl md:text-6xl text-gold mb-4">24/7</div>
                    <p class="text-white text-lg mb-2">Legal Support</p>
                    <p class="text-gray-400 text-sm">Always available</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Case Results -->
    <section id="results" class="py-24 md:py-32 bg-navy-900 grain">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-20 reveal">
                <p class="text-gold text-sm tracking-[0.3em] uppercase mb-4">Victories</p>
                <h2 class="font-serif text-4xl md:text-5xl text-white">Major Case Results</h2>
                <div class="w-24 h-px bg-gold mx-auto mt-8"></div>
            </div>

            <div class="max-w-4xl mx-auto">
                <div class="timeline-item pb-12 reveal">
                    <div class="timeline-dot"></div>
                    <div class="glass-light p-8 rounded-lg">
                        <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-4">
                            <h3 class="font-serif text-2xl text-white">Fortune 500 Merger Defense</h3>
                            <span class="text-gold text-sm mt-2 md:mt-0">2023</span>
                        </div>
                        <p class="text-gray-300 mb-4">Successfully defended a $2.4 billion merger against regulatory challenges, securing approval from the FTC and DOJ.</p>
                        <div class="flex items-center gap-4">
                            <span class="text-gold font-serif text-3xl">$2.4B</span>
                            <span class="text-gray-400 text-sm">Transaction Value</span>
                        </div>
                    </div>
                </div>

                <div class="timeline-item pb-12 reveal">
                    <div class="timeline-dot"></div>
                    <div class="glass-light p-8 rounded-lg">
                        <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-4">
                            <h3 class="font-serif text-2xl text-white">Class Action Settlement</h3>
                            <span class="text-gold text-sm mt-2 md:mt-0">2022</span>
                        </div>
                        <p class="text-gray-300 mb-4">Secured a landmark settlement for 5,000+ plaintiffs in a consumer protection class action against a major tech corporation.</p>
                        <div class="flex items-center gap-4">
                            <span class="text-gold font-serif text-3xl">$185M</span>
                            <span class="text-gray-400 text-sm">Settlement</span>
                        </div>
                    </div>
                </div>

                <div class="timeline-item pb-12 reveal">
                    <div class="timeline-dot"></div>
                    <div class="glass-light p-8 rounded-lg">
                        <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-4">
                            <h3 class="font-serif text-2xl text-white">White Collar Acquittal</h3>
                            <span class="text-gold text-sm mt-2 md:mt-0">2021</span>
                        </div>
                        <p class="text-gray-300 mb-4">Achieved full acquittal for a C-suite executive facing federal fraud charges in a high-profile criminal trial.</p>
                        <div class="flex items-center gap-4">
                            <span class="text-gold font-serif text-3xl">Not Guilty</span>
                            <span class="text-gray-400 text-sm">Verdict</span>
                        </div>
                    </div>
                </div>

                <div class="timeline-item reveal">
                    <div class="timeline-dot"></div>
                    <div class="glass-light p-8 rounded-lg">
                        <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-4">
                            <h3 class="font-serif text-2xl text-white">Real Estate Portfolio Acquisition</h3>
                            <span class="text-gold text-sm mt-2 md:mt-0">2020</span>
                        </div>
                        <p class="text-gray-300 mb-4">Facilitated the acquisition of a premium commercial real estate portfolio across 12 major metropolitan areas.</p>
                        <div class="flex items-center gap-4">
                            <span class="text-gold font-serif text-3xl">$750M</span>
                            <span class="text-gray-400 text-sm">Portfolio Value</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section id="testimonials" class="py-24 md:py-32 bg-navy-800 grain">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-20 reveal">
                <p class="text-gold text-sm tracking-[0.3em] uppercase mb-4">Client Voices</p>
                <h2 class="font-serif text-4xl md:text-5xl text-white">Testimonials</h2>
                <div class="w-24 h-px bg-gold mx-auto mt-8"></div>
            </div>

            <div class="max-w-4xl mx-auto relative">
                <div id="testimonial-container">
                    <!-- Testimonial 1 -->
                    <div class="testimonial-slide active">
                        <div class="glass-light p-10 md:p-16 rounded-lg text-center">
                            <i class="fas fa-quote-left text-4xl text-gold/30 mb-8"></i>
                            <p class="font-serif text-2xl md:text-3xl text-white italic leading-relaxed mb-8">
                                "Blackstone Legal's strategic approach to our complex corporate litigation was nothing short of masterful. They delivered results that exceeded all expectations."
                            </p>
                            <div class="flex items-center justify-center gap-4">
                                <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80" alt="Client" class="w-14 h-14 rounded-full object-cover">
                                <div class="text-left">
                                    <p class="text-white font-medium">Robert Sterling</p>
                                    <p class="text-gold text-sm">CEO, Sterling Industries</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Testimonial 2 -->
                    <div class="testimonial-slide">
                        <div class="glass-light p-10 md:p-16 rounded-lg text-center">
                            <i class="fas fa-quote-left text-4xl text-gold/30 mb-8"></i>
                            <p class="font-serif text-2xl md:text-3xl text-white italic leading-relaxed mb-8">
                                "In my darkest hour, the team at Blackstone stood by me with unwavering dedication. Their expertise in criminal defense is truly unparalleled."
                            </p>
                            <div class="flex items-center justify-center gap-4">
                                <img src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80" alt="Client" class="w-14 h-14 rounded-full object-cover">
                                <div class="text-left">
                                    <p class="text-white font-medium">David Chen</p>
                                    <p class="text-gold text-sm">Private Client</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Testimonial 3 -->
                    <div class="testimonial-slide">
                        <div class="glass-light p-10 md:p-16 rounded-lg text-center">
                            <i class="fas fa-quote-left text-4xl text-gold/30 mb-8"></i>
                            <p class="font-serif text-2xl md:text-3xl text-white italic leading-relaxed mb-8">
                                "Their attention to detail and commitment to excellence made all the difference in our family estate planning. Truly a world-class firm."
                            </p>
                            <div class="flex items-center justify-center gap-4">
                                <img src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80" alt="Client" class="w-14 h-14 rounded-full object-cover">
                                <div class="text-left">
                                    <p class="text-white font-medium">Amanda Westfield</p>
                                    <p class="text-gold text-sm">Family Office Director</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Carousel Controls -->
                <div class="flex justify-center gap-4 mt-10">
                    <button id="prev-testimonial" class="w-12 h-12 rounded-full border border-white/20 flex items-center justify-center text-white hover:bg-gold hover:border-gold hover:text-navy-900 transition-all">
                        <i class="fas fa-arrow-left"></i>
                    </button>
                    <button id="next-testimonial" class="w-12 h-12 rounded-full border border-white/20 flex items-center justify-center text-white hover:bg-gold hover:border-gold hover:text-navy-900 transition-all">
                        <i class="fas fa-arrow-right"></i>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Insights Section -->
    <section id="insights" class="py-24 md:py-32 bg-navy-900 grain">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-20 reveal">
                <p class="text-gold text-sm tracking-[0.3em] uppercase mb-4">Knowledge</p>
                <h2 class="font-serif text-4xl md:text-5xl text-white">Legal Insights</h2>
                <div class="w-24 h-px bg-gold mx-auto mt-8"></div>
            </div>

            <div class="grid md:grid-cols-3 gap-8">
                <!-- Article 1 -->
                <article class="group cursor-pointer reveal">
                    <div class="overflow-hidden rounded-lg mb-6">
                        <img src="https://images.unsplash.com/photo-1450101499163-c8848c66ca85?ixlib=rb-4.0.3&auto=format&fit=crop&w=1740&q=80" alt="Corporate Law" class="w-full h-64 object-cover transform group-hover:scale-105 transition-transform duration-500">
                    </div>
                    <div class="flex items-center gap-4 mb-3">
                        <span class="text-gold text-xs tracking-wider uppercase">Corporate Law</span>
                        <span class="text-gray-500 text-xs">Jan 15, 2024</span>
                    </div>
                    <h3 class="font-serif text-xl text-white group-hover:text-gold transition-colors mb-3">Navigating M&A Regulations in 2024</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Key regulatory changes affecting mergers and acquisitions this year...</p>
                </article>

                <!-- Article 2 -->
                <article class="group cursor-pointer reveal">
                    <div class="overflow-hidden rounded-lg mb-6">
                        <img src="https://images.unsplash.com/photo-1589829545856-d10d557cf95f?ixlib=rb-4.0.3&auto=format&fit=crop&w=1740&q=80" alt="Criminal Defense" class="w-full h-64 object-cover transform group-hover:scale-105 transition-transform duration-500">
                    </div>
                    <div class="flex items-center gap-4 mb-3">
                        <span class="text-gold text-xs tracking-wider uppercase">Criminal Defense</span>
                        <span class="text-gray-500 text-xs">Jan 10, 2024</span>
                    </div>
                    <h3 class="font-serif text-xl text-white group-hover:text-gold transition-colors mb-3">White Collar Crime Trends to Watch</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Emerging patterns in federal prosecution of financial crimes...</p>
                </article>

                <!-- Article 3 -->
                <article class="group cursor-pointer reveal">
                    <div class="overflow-hidden rounded-lg mb-6">
                        <img src="https://images.unsplash.com/photo-1521791136064-7986c2920216?ixlib=rb-4.0.3&auto=format&fit=crop&w=1740&q=80" alt="Family Law" class="w-full h-64 object-cover transform group-hover:scale-105 transition-transform duration-500">
                    </div>
                    <div class="flex items-center gap-4 mb-3">
                        <span class="text-gold text-xs tracking-wider uppercase">Family Law</span>
                        <span class="text-gray-500 text-xs">Jan 5, 2024</span>
                    </div>
                    <h3 class="font-serif text-xl text-white group-hover:text-gold transition-colors mb-3">Estate Planning for Modern Families</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Comprehensive strategies for complex family structures...</p>
                </article>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-24 md:py-32 bg-navy-800 grain">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-20 reveal">
                <p class="text-gold text-sm tracking-[0.3em] uppercase mb-4">Get in Touch</p>
                <h2 class="font-serif text-4xl md:text-5xl text-white">Contact Us</h2>
                <div class="w-24 h-px bg-gold mx-auto mt-8"></div>
            </div>

            <div class="grid lg:grid-cols-2 gap-16">
                <!-- Contact Form -->
                <div class="reveal">
                    <form id="contact-form" class="space-y-6">
                        <div class="grid md:grid-cols-2 gap-6">
                            <div>
                                <label class="block text-sm text-gray-300 mb-2">First Name</label>
                                <input type="text" class="form-input w-full bg-navy-900 border border-navy-600 rounded-lg px-4 py-3 text-white placeholder-gray-500 transition-all" placeholder="John" required>
                            </div>
                            <div>
                                <label class="block text-sm text-gray-300 mb-2">Last Name</label>
                                <input type="text" class="form-input w-full bg-navy-900 border border-navy-600 rounded-lg px-4 py-3 text-white placeholder-gray-500 transition-all" placeholder="Doe" required>
                            </div>
                        </div>
                        <div>
                            <label class="block text-sm text-gray-300 mb-2">Email Address</label>
                            <input type="email" class="form-input w-full bg-navy-900 border border-navy-600 rounded-lg px-4 py-3 text-white placeholder-gray-500 transition-all" placeholder="john@example.com" required>
                        </div>
                        <div>
                            <label class="block text-sm text-gray-300 mb-2">Phone Number</label>
                            <input type="tel" class="form-input w-full bg-navy-900 border border-navy-600 rounded-lg px-4 py-3 text-white placeholder-gray-500 transition-all" placeholder="+1 (555) 000-0000">
                        </div>
                        <div>
                            <label class="block text-sm text-gray-300 mb-2">Practice Area</label>
                            <select class="form-input w-full bg-navy-900 border border-navy-600 rounded-lg px-4 py-3 text-white transition-all">
                                <option value="">Select a practice area</option>
                                <option value="corporate">Corporate Law</option>
                                <option value="family">Family Law</option>
                                <option value="criminal">Criminal Defense</option>
                                <option value="property">Property Law</option>
                                <option value="civil">Civil Litigation</option>
                                <option value="employment">Employment Law</option>
                                <option value="injury">Personal Injury</option>
                                <option value="estate">Estate Planning</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-sm text-gray-300 mb-2">Message</label>
                            <textarea class="form-input w-full bg-navy-900 border border-navy-600 rounded-lg px-4 py-3 text-white placeholder-gray-500 transition-all h-32 resize-none" placeholder="Tell us about your case..." required></textarea>
                        </div>
                        <button type="submit" class="w-full py-4 bg-gold text-navy-900 font-medium tracking-wider hover:bg-gold-light transition-all duration-300 btn-ripple shadow-lg shadow-gold/20">
                            Send Message
                        </button>
                    </form>
                </div>

                <!-- Contact Info -->
                <div class="reveal">
                    <div class="glass-light p-8 rounded-lg mb-8">
                        <h3 class="font-serif text-2xl text-white mb-6">Office Information</h3>
                        <div class="space-y-6">
                            <div class="flex items-start gap-4">
                                <div class="w-10 h-10 rounded-full bg-gold/10 flex items-center justify-center flex-shrink-0 mt-1">
                                    <i class="fas fa-map-marker-alt text-gold"></i>
                                </div>
                                <div>
                                    <p class="text-white font-medium mb-1">Address</p>
                                    <p class="text-gray-400 text-sm">350 Fifth Avenue, Suite 7600<br>New York, NY 10118</p>
                                </div>
                            </div>
                            <div class="flex items-start gap-4">
                                <div class="w-10 h-10 rounded-full bg-gold/10 flex items-center justify-center flex-shrink-0 mt-1">
                                    <i class="fas fa-clock text-gold"></i>
                                </div>
                                <div>
                                    <p class="text-white font-medium mb-1">Office Hours</p>
                                    <p class="text-gray-400 text-sm">Mon - Fri: 8:00 AM - 8:00 PM<br>Sat: 9:00 AM - 2:00 PM</p>
                                </div>
                            </div>
                            <div class="flex items-start gap-4">
                                <div class="w-10 h-10 rounded-full bg-gold/10 flex items-center justify-center flex-shrink-0 mt-1">
                                    <i class="fas fa-phone text-gold"></i>
                                </div>
                                <div>
                                    <p class="text-white font-medium mb-1">Phone</p>
                                    <p class="text-gray-400 text-sm">+1 (800) 555-0199</p>
                                </div>
                            </div>
                            <div class="flex items-start gap-4">
                                <div class="w-10 h-10 rounded-full bg-gold/10 flex items-center justify-center flex-shrink-0 mt-1">
                                    <i class="fas fa-envelope text-gold"></i>
                                </div>
                                <div>
                                    <p class="text-white font-medium mb-1">Email</p>
                                    <p class="text-gray-400 text-sm">contact@blackstonelegal.com</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- WhatsApp Button -->
                    <a href="https://wa.me/18005550199" target="_blank" class="flex items-center justify-center gap-3 w-full py-4 bg-green-600 text-white rounded-lg hover:bg-green-700 transition-all duration-300 mb-6">
                        <i class="fab fa-whatsapp text-xl"></i>
                        <span class="tracking-wider">Chat on WhatsApp</span>
                    </a>

                    <!-- Social Links -->
                    <div class="flex justify-center gap-4">
                        <a href="#" class="w-12 h-12 rounded-full bg-navy-700 flex items-center justify-center text-white hover:bg-gold hover:text-navy-900 transition-all">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="#" class="w-12 h-12 rounded-full bg-navy-700 flex items-center justify-center text-white hover:bg-gold hover:text-navy-900 transition-all">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="w-12 h-12 rounded-full bg-navy-700 flex items-center justify-center text-white hover:bg-gold hover:text-navy-900 transition-all">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="w-12 h-12 rounded-full bg-navy-700 flex items-center justify-center text-white hover:bg-gold hover:text-navy-900 transition-all">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </div>
                </div>
            </div>

            <!-- Map Placeholder -->
            <div class="mt-16 reveal">
                <div class="w-full h-96 bg-navy-700 rounded-lg overflow-hidden relative">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3022.1422937950147!2d-73.98731968482413!3d40.75889497932681!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c25855c6480299%3A0x55194ec5a1ae072e!2sTimes%20Square!5e0!3m2!1sen!2sus!4v1620000000000!5m2!1sen!2sus" 
                        width="100%" 
                        height="100%" 
                        style="border:0; filter: grayscale(100%) invert(92%) contrast(83%);" 
                        allowfullscreen="" 
                        loading="lazy"
                        title="Office Location">
                    </iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-navy-900 border-t border-navy-700 pt-16 pb-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-12 mb-12">
                <!-- Logo & Description -->
                <div>
                    <div class="flex flex-col items-start mb-6">
                        <span class="font-serif text-2xl text-white tracking-wider">BLACKSTONE</span>
                        <span class="text-gold text-[10px] tracking-[0.4em] uppercase -mt-1">Legal</span>
                    </div>
                    <p class="text-gray-400 text-sm leading-relaxed mb-6">
                        Elite legal representation for Fortune 500 companies and ultra-high-net-worth individuals. Excellence in every case.
                    </p>
                </div>

                <!-- Quick Links -->
                <div>
                    <h4 class="text-white font-medium mb-6 tracking-wider">Quick Links</h4>
                    <ul class="space-y-3">
                        <li><a href="#home" class="text-gray-400 text-sm hover:text-gold transition-colors">Home</a></li>
                        <li><a href="#about" class="text-gray-400 text-sm hover:text-gold transition-colors">About</a></li>
                        <li><a href="#practice" class="text-gray-400 text-sm hover:text-gold transition-colors">Practice Areas</a></li>
                        <li><a href="#attorneys" class="text-gray-400 text-sm hover:text-gold transition-colors">Attorneys</a></li>
                        <li><a href="#contact" class="text-gray-400 text-sm hover:text-gold transition-colors">Contact</a></li>
                    </ul>
                </div>

                <!-- Practice Areas -->
                <div>
                    <h4 class="text-white font-medium mb-6 tracking-wider">Practice Areas</h4>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 text-sm hover:text-gold transition-colors">Corporate Law</a></li>
                        <li><a href="#" class="text-gray-400 text-sm hover:text-gold transition-colors">Criminal Defense</a></li>
                        <li><a href="#" class="text-gray-400 text-sm hover:text-gold transition-colors">Family Law</a></li>
                        <li><a href="#" class="text-gray-400 text-sm hover:text-gold transition-colors">Estate Planning</a></li>
                        <li><a href="#" class="text-gray-400 text-sm hover:text-gold transition-colors">Personal Injury</a></li>
                    </ul>
                </div>

                <!-- Contact -->
                <div>
                    <h4 class="text-white font-medium mb-6 tracking-wider">Contact</h4>
                    <ul class="space-y-3">
                        <li class="flex items-center gap-3 text-gray-400 text-sm">
                            <i class="fas fa-map-marker-alt text-gold w-4"></i>
                            350 Fifth Avenue, Suite 7600
                        </li>
                        <li class="flex items-center gap-3 text-gray-400 text-sm">
                            <i class="fas fa-phone text-gold w-4"></i>
                            +1 (800) 555-0199
                        </li>
                        <li class="flex items-center gap-3 text-gray-400 text-sm">
                            <i class="fas fa-envelope text-gold w-4"></i>
                            contact@blackstonelegal.com
                        </li>
                    </ul>
                </div>
            </div>

            <div class="border-t border-navy-700 pt-8 flex flex-col md:flex-row justify-between items-center gap-4">
                <p class="text-gray-500 text-sm"> 2024 Blackstone Legal. All rights reserved.</p>
                <div class="flex gap-6">
                    <a href="#" class="text-gray-500 text-sm hover:text-gold transition-colors">Privacy Policy</a>
                    <a href="#" class="text-gray-500 text-sm hover:text-gold transition-colors">Terms of Service</a>
                    <a href="#" class="text-gray-500 text-sm hover:text-gold transition-colors">Disclaimer</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <button id="back-to-top" class="fixed bottom-8 right-8 w-12 h-12 bg-gold text-navy-900 rounded-full shadow-lg flex items-center justify-center opacity-0 invisible transition-all duration-300 hover:bg-gold-light z-40">
        <i class="fas fa-arrow-up"></i>
    </button>

    <script>
        // Loading Screen
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.getElementById('loading-screen').classList.add('hidden');
            }, 1500);
        });

        // Navbar Scroll Effect
        const navbar = document.getElementById('navbar');
        let lastScroll = 0;

        window.addEventListener('scroll', () => {
            const currentScroll = window.pageYOffset;
            
            if (currentScroll > 100) {
                navbar.classList.add('glass', 'shadow-lg');
            } else {
                navbar.classList.remove('glass', 'shadow-lg');
            }
            
            lastScroll = currentScroll;
        });

        // Mobile Menu
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const closeMenuBtn = document.getElementById('close-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.add('open');
            document.body.style.overflow = 'hidden';
        });

        closeMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.remove('open');
            document.body.style.overflow = '';
        });

        // Close mobile menu when clicking on links
        mobileMenu.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.remove('open');
                document.body.style.overflow = '';
            });
        });

        // Scroll Reveal Animation
        const revealElements = document.querySelectorAll('.reveal');

        const revealOnScroll = () => {
            const windowHeight = window.innerHeight;
            const elementVisible = 100;

            revealElements.forEach((element) => {
                const elementTop = element.getBoundingClientRect().top;
                if (elementTop < windowHeight - elementVisible) {
                    element.classList.add('active');
                }
            });
        };

        window.addEventListener('scroll', revealOnScroll);
        revealOnScroll(); // Trigger on load

        // Animated Counters
        const counters = document.querySelectorAll('.counter');
        let countersStarted = false;

        const startCounters = () => {
            const section = document.querySelector('.counter').closest('section');
            const sectionTop = section.getBoundingClientRect().top;
            const windowHeight = window.innerHeight;

            if (sectionTop < windowHeight - 100 && !countersStarted) {
                countersStarted = true;
                
                counters.forEach(counter => {
                    const target = parseInt(counter.getAttribute('data-target'));
                    const duration = 2000;
                    const increment = target / (duration / 16);
                    let current = 0;

                    const updateCounter = () => {
                        current += increment;
                        if (current < target) {
                            counter.textContent = Math.floor(current) + (target > 100 ? '+' : '');
                            requestAnimationFrame(updateCounter);
                        } else {
                            counter.textContent = target + (target > 100 ? '+' : '');
                        }
                    };

                    updateCounter();
                });
            }
        };

        window.addEventListener('scroll', startCounters);

        // Testimonial Carousel
        const testimonialSlides = document.querySelectorAll('.testimonial-slide');
        const prevBtn = document.getElementById('prev-testimonial');
        const nextBtn = document.getElementById('next-testimonial');
        let currentSlide = 0;

        const showSlide = (index) => {
            testimonialSlides.forEach((slide, i) => {
                slide.classList.remove('active');
                if (i === index) {
                    slide.classList.add('active');
                }
            });
        };

        const nextSlide = () => {
            currentSlide = (currentSlide + 1) % testimonialSlides.length;
            showSlide(currentSlide);
        };

        const prevSlide = () => {
            currentSlide = (currentSlide - 1 + testimonialSlides.length) % testimonialSlides.length;
            showSlide(currentSlide);
        };

        nextBtn.addEventListener('click', nextSlide);
        prevBtn.addEventListener('click', prevSlide);

        // Auto-advance testimonials
        setInterval(nextSlide, 6000);

        // Back to Top Button
        const backToTopBtn = document.getElementById('back-to-top');

        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 500) {
                backToTopBtn.classList.remove('opacity-0', 'invisible');
                backToTopBtn.classList.add('opacity-100', 'visible');
            } else {
                backToTopBtn.classList.add('opacity-0', 'invisible');
                backToTopBtn.classList.remove('opacity-100', 'visible');
            }
        });

        backToTopBtn.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });

        // Form Submission
        document.getElementById('contact-form').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Thank you for your message. Our team will contact you within 24 hours.');
            e.target.reset();
        });

        // Smooth Scroll for Anchor Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Parallax Effect for Hero
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const hero = document.querySelector('.hero-bg');
            if (hero && scrolled < window.innerHeight) {
                hero.style.transform = `translateY(${scrolled * 0.5}px)`;
            }
        });
    </script>
</body>
</html>
