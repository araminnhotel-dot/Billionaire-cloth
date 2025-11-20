([Immersive content redacted for brevity.]<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Billionaire Cloth | Exclusive Apparel & Luxury Goods</title>
    <!-- Tailwind CSS লোড করুন -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* কাস্টম স্টাইলস: বিলাসবহুল চেহারার জন্য */
        :root {
            --color-dark-bg: #0d0d0d;
            --color-gold: #cfa862;
            --color-light: #f3f4f6;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--color-dark-bg);
            color: var(--color-light);
            scroll-behavior: smooth;
        }

        /* গোল্ড টেক্সট ইউটিলিটি */
        .text-gold {
            color: var(--color-gold);
        }

        /* গোল্ড বাটন স্টাইল */
        .btn-gold {
            background-color: var(--color-gold);
            color: var(--color-dark-bg);
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(207, 168, 98, 0.4);
        }

        .btn-gold:hover {
            background-color: #e0bb79;
            box-shadow: 0 6px 20px rgba(207, 168, 98, 0.6);
            transform: translateY(-2px);
        }

        /* প্রোডাক্ট কার্ড এফেক্টস */
        .product-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            background-color: #1a1a1a;
            border: 1px solid #2d2d2d;
        }
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5), 0 0 10px rgba(207, 168, 98, 0.3);
        }

        /* AI বাটন (সেকেন্ডারি) */
        .ai-button-secondary {
            background-color: #2d2d2d;
            color: var(--color-gold);
            transition: all 0.3s ease;
        }
        .ai-button-secondary:hover {
            background-color: #3a3a3a;
        }
        
        /* Modal backdrop and positioning */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 100;
        }
        .modal-content {
            max-width: 90%;
            width: 600px;
            background-color: var(--color-dark-bg);
            border: 2px solid var(--color-gold);
            max-height: 80vh;
            overflow-y: auto;
        }
    </style>
</head>
<body>

    <!-- হেডার এবং নেভিগেশন -->
    <header class="sticky top-0 z-50 bg-black/80 backdrop-blur-sm shadow-lg border-b border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- লোগো -->
            <a href="#" class="text-3xl font-extrabold tracking-widest uppercase text-gold">
                BC.
            </a>

            <!-- ডেস্কটপ নেভিগেশন লিঙ্কস (নতুন ক্যাটাগরি যুক্ত করা হয়েছে) -->
            <nav class="hidden lg:flex space-x-6">
                <a href="#featured" class="nav-link text-sm font-medium uppercase tracking-wider hover:text-gold transition duration-200">New Arrivals</a>
                <a href="#category-shirts" class="nav-link text-sm font-medium uppercase tracking-wider hover:text-gold transition duration-200">Shirts</a>
                <a href="#category-jackets" class="nav-link text-sm font-medium uppercase tracking-wider hover:text-gold transition duration-200">Jackets</a>
                <a href="#category-panjabi" class="nav-link text-sm font-medium uppercase tracking-wider hover:text-gold transition duration-200">Panjabi</a>
                <a href="#category-hoodies" class="nav-link text-sm font-medium uppercase tracking-wider hover:text-gold transition duration-200">Hoodies</a>
            </nav>

            <!-- আইকন / অ্যাকশন -->
            <div class="flex items-center space-x-6">
                <!-- কার্ট আইকন -->
                <button class="relative text-gray-400 hover:text-gold transition duration-200">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
                    </svg>
                    <span class="absolute top-0 right-0 inline-flex items-center justify-center px-2 py-1 text-xs font-bold leading-none text-black transform translate-x-1/2 -translate-y-1/2 bg-gold rounded-full">3</span>
                </button>
                <!-- মোবাইল মেনু বাটন -->
                <button id="mobile-menu-button" class="lg:hidden text-gray-400 hover:text-gold transition duration-200">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
                    </svg>
                </button>
            </div>
        </div>

        <!-- মোবাইল মেনু (Hidden by default) -->
        <nav id="mobile-menu" class="hidden lg:hidden px-4 pt-2 pb-4 space-y-1 border-t border-gray-800">
            <a href="#featured" class="block py-2 text-sm font-medium text-gray-300 hover:text-gold rounded-md">New Arrivals</a>
            <a href="#category-shirts" class="block py-2 text-sm font-medium text-gray-300 hover:text-gold rounded-md">Shirts</a>
            <a href="#category-jackets" class="block py-2 text-sm font-medium text-gray-300 hover:text-gold rounded-md">Jackets</a>
            <a href="#category-panjabi" class="block py-2 text-sm font-medium text-gray-300 hover:text-gold rounded-md">Panjabi</a>
            <a href="#category-hoodies" class="block py-2 text-sm font-medium text-gray-300 hover:text-gold rounded-md">Hoodies</a>
        </nav>
    </header>

    <main>
        <!-- হিরো সেকশন: হাই ইমপ্যাক্ট ভিজ্যুয়াল -->
        <section class="relative h-screen flex items-center justify-center overflow-hidden">
            <!-- Background Image Placeholder (আপনার কাস্টম ব্যানার ইমেজ URL দিন) -->
            <div class="absolute inset-0">
                <!-- IMPORTANT: এখানে আপনার ব্যানার ইমেজের URL দিন -->
                <img src="https://placehold.co/1920x1080/1a1a1a/cfa862?text=BC+LUXURY+BANNER" 
                     class="w-full h-full object-cover opacity-70" 
                     alt="Cinematic fashion shot with luxurious texture.">
                <!-- ডার্ক ওভারলে -->
                <div class="absolute inset-0 bg-black opacity-40"></div>
            </div>

            <!-- কন্টেন্ট -->
            <div class="relative z-10 text-center max-w-4xl px-4">
                <h1 class="text-4xl sm:text-6xl lg:text-8xl font-black uppercase mb-6 leading-tight text-white">
                    <span class="text-gold">The Standard</span> Is Set.
                </h1>
                <p class="text-lg sm:text-xl text-gray-300 mb-10 tracking-wider">
                    "বিলাসিতা একটি পছন্দ নয়, এটি একটি জীবনধারা। আপনি শুধু পোশাক পরছেন না, আপনি একটি উত্তরাধিকার পরিধান করছেন।"
                </p>
                <a href="#featured" class="btn-gold px-10 py-4 text-sm font-bold uppercase rounded-lg tracking-widest">
                    এক্সক্লুসিভ কালেকশন দেখুন
                </a>
            </div>
        </section>

        <!-- নতুন ব্যানার সেকশন (ভিডিওর বিকল্প হিসেবে) -->
        <section class="py-12 bg-cover bg-center" style="background-image: url('https://placehold.co/1920x400/222222/cfa862?text=BC+NEW+COLLECTION+BANNER');">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center py-12 bg-black/30 rounded-lg">
                <h3 class="text-4xl font-extrabold uppercase mb-2 text-white">The Winter Drop: <span class="text-gold">Tailored Warmth</span></h3>
                <p class="text-gray-300 mb-6 max-w-xl mx-auto">
                    শীতকালীন আরাম ও বিলাসের নিখুঁত মিশ্রণ। প্রতিটি সূতোয় আভিজাত্যের স্পর্শ।
                </p>
                <a href="#category-jackets" class="btn-gold px-8 py-3 text-sm font-bold uppercase rounded-lg">
                    জ্যাকেট ও হুডি এক্সপ্লোর করুন
                </a>
            </div>
        </section>
        
        <!-- প্রোডাক্ট সেকশন: শার্ট, জ্যাকেট, পাঞ্জাবি, হুডি -->
        <section id="featured" class="py-16 md:py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-4xl font-bold uppercase mb-12 text-center text-white">
                নির্বাচিত প্রিমিয়াম কালেকশন
            </h2>

            <!-- প্রোডাক্ট গ্রিড -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                
                <!-- 1. Executive Blazer (আগের পণ্য) -->
                <div class="product-card rounded-xl overflow-hidden shadow-2xl">
                    <!-- IMPORTANT: ছবির URL দিন -->
                    <img src="https://placehold.co/600x800/222222/cfa862?text=EXECUTIVE+BLAZER" 
                         class="w-full h-72 object-cover object-center" 
                         alt="Executive collection blazer">
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-semibold mb-2 text-white">The Executive Blazer</h3>
                        <p class="text-gray-400 text-sm mb-4">Cashmere Blend</p>
                        <p class="text-2xl font-bold text-gold">$2,999</p>
                        <button onclick="generateStyleAdvice('Executive Blazer in Cashmere Blend', 'style')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-2">
                            ✨ AI স্টাইল ম্যাচ
                        </button>
                        <button onclick="generateStyleAdvice('Executive Blazer in Cashmere Blend', 'story')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-3">
                            ✨ প্রোডাক্ট স্টোরি
                        </button>
                        <button class="btn-gold w-full py-2 text-xs uppercase font-semibold rounded-lg">কার্টে যোগ করুন</button>
                    </div>
                </div>

                <!-- 2. The Legacy Shirt (নতুন পণ্য: শার্ট) -->
                <div class="product-card rounded-xl overflow-hidden shadow-2xl" id="category-shirts">
                    <!-- IMPORTANT: ছবির URL দিন -->
                    <img src="https://placehold.co/600x800/222222/cfa862?text=LEGACY+SHIRT" 
                         class="w-full h-72 object-cover object-center" 
                         alt="The Legacy Shirt">
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-semibold mb-2 text-white">The Legacy Shirt</h3>
                        <p class="text-gray-400 text-sm mb-4">Egyptian Cotton | Tagline: "প্রতিটি সূতোয় আভিজাত্যের ইতিহাস"</p>
                        <p class="text-2xl font-bold text-gold">$350</p>
                        <button onclick="generateStyleAdvice('The Legacy Shirt in Egyptian Cotton', 'style')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-2">
                            ✨ AI স্টাইল ম্যাচ
                        </button>
                        <button onclick="generateStyleAdvice('The Legacy Shirt in Egyptian Cotton', 'story')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-3">
                            ✨ প্রোডাক্ট স্টোরি
                        </button>
                        <button class="btn-gold w-full py-2 text-xs uppercase font-semibold rounded-lg">কার্টে যোগ করুন</button>
                    </div>
                </div>

                <!-- 3. The Grand Panjabi (নতুন পণ্য: পাঞ্জাবি) -->
                <div class="product-card rounded-xl overflow-hidden shadow-2xl" id="category-panjabi">
                    <!-- IMPORTANT: ছবির URL দিন -->
                    <img src="https://placehold.co/600x800/333333/cfa862?text=GRAND+PANJABI" 
                         class="w-full h-72 object-cover object-center" 
                         alt="The Grand Panjabi">
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-semibold mb-2 text-white">The Grand Panjabi</h3>
                        <p class="text-gray-400 text-sm mb-4">Raw Silk | Tagline: "ঐতিহ্যের অহংকার, আধুনিকতার স্বাক্ষর"</p>
                        <p class="text-2xl font-bold text-gold">$500</p>
                        <button onclick="generateStyleAdvice('The Grand Panjabi in Raw Silk', 'style')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-2">
                            ✨ AI স্টাইল ম্যাচ
                        </button>
                        <button onclick="generateStyleAdvice('The Grand Panjabi in Raw Silk', 'story')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-3">
                            ✨ প্রোডাক্ট স্টোরি
                        </button>
                        <button class="btn-gold w-full py-2 text-xs uppercase font-semibold rounded-lg">কার্টে যোগ করুন</button>
                    </div>
                </div>
                
                <!-- 4. The Apex Hoodie (নতুন পণ্য: হুডি) -->
                <div class="product-card rounded-xl overflow-hidden shadow-2xl" id="category-hoodies">
                    <!-- IMPORTANT: ছবির URL দিন -->
                    <img src="https://placehold.co/600x800/444444/cfa862?text=APEX+HOODIE" 
                         class="w-full h-72 object-cover object-center" 
                         alt="The Apex Hoodie">
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-semibold mb-2 text-white">The Apex Hoodie</h3>
                        <p class="text-gray-400 text-sm mb-4">Heavyweight Pima Cotton | Tagline: "আপনার বিশ্রামের দিনগুলোতেও আভিজাত্য"</p>
                        <p class="text-2xl font-bold text-gold">$420</p>
                        <button onclick="generateStyleAdvice('The Apex Hoodie in Heavyweight Pima Cotton', 'style')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-2">
                            ✨ AI স্টাইল ম্যাচ
                        </button>
                        <button onclick="generateStyleAdvice('The Apex Hoodie in Heavyweight Pima Cotton', 'story')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-3">
                            ✨ প্রোডাক্ট স্টোরি
                        </button>
                        <button class="btn-gold w-full py-2 text-xs uppercase font-semibold rounded-lg">কার্টে যোগ করুন</button>
                    </div>
                </div>
                
                <!-- 5. The Dynasty Jacket (নতুন পণ্য: জ্যাকেট) -->
                 <div class="product-card rounded-xl overflow-hidden shadow-2xl" id="category-jackets">
                    <!-- IMPORTANT: ছবির URL দিন -->
                    <img src="https://placehold.co/600x800/555555/cfa862?text=DYNASTY+JACKET" 
                         class="w-full h-72 object-cover object-center" 
                         alt="The Dynasty Jacket">
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-semibold mb-2 text-white">The Dynasty Jacket</h3>
                        <p class="text-gray-400 text-sm mb-4">Italian Leather | Tagline: "ক্ষমতা আর ফ্যাশনের নতুন সংজ্ঞা"</p>
                        <p class="text-2xl font-bold text-gold">$3,999</p>
                        <button onclick="generateStyleAdvice('The Dynasty Jacket in Italian Leather', 'style')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-2">
                            ✨ AI স্টাইল ম্যাচ
                        </button>
                        <button onclick="generateStyleAdvice('The Dynasty Jacket in Italian Leather', 'story')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-3">
                            ✨ প্রোডাক্ট স্টোরি
                        </button>
                        <button class="btn-gold w-full py-2 text-xs uppercase font-semibold rounded-lg">কার্টে যোগ করুন</button>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <a href="#" class="text-sm font-semibold uppercase text-gold hover:text-white transition duration-200 border-b border-gold hover:border-white pb-1">
                    সমস্ত কালেকশন দেখুন &rarr;
                </a>
            </div>
        </section>
        
        <!-- নতুন ভিডিও প্রেজেন্টেশন সেকশন -->
        <section class="py-16 md:py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <h2 class="text-4xl font-bold uppercase mb-12 text-white">
                বিহাইনড দ্য সিন: <span class="text-gold">কারুকার্য</span>
            </h2>
            <div class="relative w-full aspect-video bg-gray-900 rounded-xl overflow-hidden shadow-2xl border border-gray-700">
                <!-- IMPORTANT: এখানে আপনার YouTube/ভিডিও URL দিন -->
                <!-- Embed কোড ব্যবহার করুন, যেমন: <iframe src="আপনার ভিডিও URL" ...></iframe> -->
                <iframe class="absolute top-0 left-0 w-full h-full" 
                        src="https://www.youtube.com/embed/dQw4w9WgXcQ?controls=0" 
                        frameborder="0" 
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                        allowfullscreen 
                        title="Billionaire Cloth Craftsmanship Video">
                </iframe>
                <!-- যদি ভিডিও এমবেড না করতে চান, তাহলে এই প্লেসহোল্ডারটি ব্যবহার করুন: -->
                <!-- <div class="flex items-center justify-center w-full h-full text-2xl text-gold">ভিডিও প্লেসহোল্ডার: আপনার ভিডিও URL এখানে বসান</div> -->
            </div>
            <p class="text-sm text-gray-500 mt-4">বিলাসী ইতালীয় চামড়ার ট্যানিং প্রক্রিয়া দেখানো হলো।</p>
        </section>


        <!-- ব্র্যান্ড মেনিফেস্টো / মোটো সেকশন -->
        <section id="new-arrivals" class="bg-[#1a1a1a] py-16 md:py-32">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <p class="text-lg font-light italic text-gray-500 mb-4 tracking-widest">
                    দ্য বিলিয়নিয়ার ফিলোসফি
                </p>
                <blockquote class="text-3xl sm:text-5xl font-extrabold leading-snug text-white">
                    "বিলাসিতা একটি পছন্দ নয়, এটি একটি জীবনধারা। আপনি শুধু পোশাক পরছেন না, আপনি একটি <span class="text-gold">উত্তরাধিকার</span> পরিধান করছেন।"
                </blockquote>
                <p class="text-base text-gray-400 mt-8 max-w-2xl mx-auto">
                    Every thread, every stitch, every detail is engineered for those who understand that true value lies in enduring quality and masterful craftsmanship. We do not follow trends—we define legacy.
                </p>
            </div>
        </section>
        

    </main>

    <!-- ফুটার -->
    <footer class="bg-black border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="grid grid-cols-2 md:grid-cols-5 gap-8">
                <!-- ব্র্যান্ড ইনফো -->
                <div class="col-span-2 md:col-span-1">
                    <h3 class="text-2xl font-extrabold tracking-widest uppercase text-gold mb-4">BC.</h3>
                    <p class="text-sm text-gray-500">
                        The pinnacle of luxury apparel and enduring style.
                    </p>
                </div>
                
                <!-- শপ লিঙ্কস -->
                <div>
                    <h4 class="text-lg font-semibold mb-4 text-white uppercase">Shop</h4>
                    <ul class="space-y-2 text-sm text-gray-400">
                        <li><a href="#category-shirts" class="hover:text-gold transition">Shirts</a></li>
                        <li><a href="#category-jackets" class="hover:text-gold transition">Jackets</a></li>
                        <li><a href="#category-panjabi" class="hover:text-gold transition">Panjabi</a></li>
                        <li><a href="#category-hoodies" class="hover:text-gold transition">Hoodies</a></li>
                    </ul>
                </div>

                <!-- কাস্টমার সার্ভিস -->
                <div>
                    <h4 class="text-lg font-semibold mb-4 text-white uppercase">Support</h4>
                    <ul class="space-y-2 text-sm text-gray-400">
                        <li><a href="#" class="hover:text-gold transition">Contact Us</a></li>
                        <li><a href="#" class="hover:text-gold transition">Shipping & Returns</a></li>
                        <li><a href="#" class="hover:text-gold transition">Size Guide</a></li>
                        <li><a href="#" class="hover:text-gold transition">FAQ</a></li>
                    </ul>
                </div>
                
                <!-- কোম্পানি -->
                <div>
                    <h4 class="text-lg font-semibold mb-4 text-white uppercase">Company</h4>
                    <ul class="space-y-2 text-sm text-gray-400">
                        <li><a href="#" class="hover:text-gold transition">Our Story</a></li>
                        <li><a href="#" class="hover:text-gold transition">Careers</a></li>
                        <li><a href="#" class="hover:text-gold transition">Press</a></li>
                        <li><a href="#" class="hover:text-gold transition">Affiliates</a></li>
                    </ul>
                </div>
                
                <!-- নিউজলেটার সাইনআপ (এখন AI ট্রেন্ডস যুক্ত) -->
                <div class="col-span-2 md:col-span-1">
                    <h4 class="text-lg font-semibold mb-4 text-white uppercase">Exclusive Access</h4>
                    <p class="text-sm text-gray-400 mb-4">
                        Be the first to know about drops and private sales.
                    </p>
                    <form onsubmit="handleSubscription(event)">
                        <input type="email" placeholder="Enter your email" required
                               class="w-full px-4 py-3 bg-gray-900 border border-gray-700 text-white rounded-lg focus:ring-gold focus:border-gold outline-none">
                        <button type="submit" class="btn-gold w-full mt-3 py-3 text-sm font-semibold uppercase rounded-lg">
                            Subscribe
                        </button>
                    </form>
                    <p id="subscribe-message" class="text-xs text-green-400 mt-2 hidden">Subscribed successfully!</p>
                    <button onclick="getLuxuryTrends()" class="w-full py-2 text-xs uppercase font-semibold rounded-lg mt-3 ai-button-secondary hover:bg-gray-700 transition duration-200">
                        ✨ গ্লোবাল লাক্সারি ট্রেন্ডস স্ন্যাপশট
                    </button>
                </div>

            </div>
            
            <div class="mt-12 pt-8 border-t border-gray-800 text-center">
                <p class="text-sm text-gray-500">&copy; 2025 Billionaire Cloth. All rights reserved. | Crafted for the elite.</p>
            </div>
        </div>
    </footer>

    <!-- AI Style Advice Modal -->
    <div id="ai-modal" class="modal-overlay hidden">
        <div class="modal-content rounded-xl p-6 relative">
            <button onclick="closeModal()" class="absolute top-4 right-4 text-gold hover:text-white transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                </svg>
            </button>
            <h3 id="modal-title" class="text-2xl font-extrabold mb-4 border-b border-gold/50 pb-2 text-gold">
                <!-- Title injected here -->
            </h3>
            <div id="modal-content-text" class="text-gray-300 text-base leading-relaxed whitespace-pre-wrap">
                <!-- Content will be injected here -->
            </div>
            <div id="modal-loading-indicator" class="text-center py-8 hidden">
                <svg class="animate-spin h-8 w-8 text-gold mx-auto" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                    <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                    <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                </svg>
                <p class="mt-4 text-gray-400">Crafting a bespoke recommendation...</p>
            </div>
        </div>
    </div>

    <script>
        // --- Gemini API কনফিগারেশন ---
        const API_KEY = ""; // Canvas স্বয়ংক্রিয়ভাবে API key সরবরাহ করবে
        const API_URL = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${API_KEY}`;
        const MAX_RETRIES = 5;

        // --- ইউটিলিটি ফাংশনস ---

        // এক্সপোনেনশিয়াল ব্যাকঅফ সহ Fetch ফাংশন
        async function fetchWithExponentialBackoff(url, options, retries = 0) {
            try {
                const response = await fetch(url, options);
                if (!response.ok) {
                    if (response.status === 429 && retries < MAX_RETRIES) {
                        const delay = Math.pow(2, retries) * 1000 + Math.random() * 1000;
                        console.log(`Rate limit exceeded (429). Retrying in ${delay / 1000}s...`);
                        await new Promise(resolve => setTimeout(resolve, delay));
                        return fetchWithExponentialBackoff(url, options, retries + 1);
                    }
                    throw new Error(`API call failed with status: ${response.status} ${response.statusText}`);
                }
                return response;
            } catch (error) {
                if (retries < MAX_RETRIES) {
                    const delay = Math.pow(2, retries) * 1000 + Math.random() * 1000;
                    console.error(`Fetch failed. Retrying in ${delay / 1000}s...`, error);
                    await new Promise(resolve => setTimeout(resolve, delay));
                    return fetchWithExponentialBackoff(url, options, retries + 1);
                }
                throw new Error("Failed to connect to the API after multiple retries.");
            }
        }

        // মডাল ওপেন এবং টাইটেল সেট করার ফাংশন
        function openModal(title) {
            document.getElementById('modal-title').textContent = title;
            document.getElementById('ai-modal').classList.remove('hidden');
        }

        // মডাল ক্লোজ করার ফাংশন
        function closeModal() {
            document.getElementById('ai-modal').classList.add('hidden');
            document.getElementById('modal-content-text').innerHTML = ''; // পূর্বের কন্টেন্ট মুছে দিন
            document.getElementById('modal-loading-indicator').classList.add('hidden');
        }
        
        // লোডিং স্টেট দেখানোর ফাংশন
        function showLoading(message = 'Creating a bespoke recommendation...') {
            const modalTextElement = document.getElementById('modal-content-text');
            const loadingIndicator = document.getElementById('modal-loading-indicator');
            modalTextElement.textContent = '';
            loadingIndicator.classList.remove('hidden');
            loadingIndicator.querySelector('p').textContent = message;
        }
        
        // এরর দেখানোর ফাংশন
        function showError(message) {
            document.getElementById('modal-content-text').innerHTML = `<p class="text-red-400">${message}</p>`;
        }

        // --- Gemini LLM ফিচার: AI স্টাইল ম্যাচ এবং প্রোডাক্ট স্টোরি ---

        async function generateStyleAdvice(productName, featureType) {
            let systemPrompt = "";
            let userQuery = "";
            let modalTitle = "";
            
            if (featureType === 'style') {
                modalTitle = `✨ AI স্টাইল ম্যাচ: ${productName}`;
                systemPrompt = "You are 'The Billionaire Cloth AI Stylist.' Your persona is sophisticated, concise, and focused on high-end luxury fashion. Always recommend three complementary items (shoes, accessories, or other apparel) and describe the overall aesthetic, using rich, evocative language. The response must be a single, cohesive paragraph formatted in clean Markdown (no headings or bullets). Use formal English.";
                userQuery = `Generate a complete styling recommendation for a ${productName}.`;
            } else if (featureType === 'story') {
                modalTitle = `✨ প্রোডাক্ট স্টোরি: The ${productName}`;
                systemPrompt = "You are a master luxury copywriter for Billionaire Cloth. Your task is to write a highly evocative, short narrative (3-5 sentences) that describes the product's exclusive heritage, materials, and the feeling of owning it. Use hyperbole and rich, sensual language. The response must be a single, cohesive paragraph formatted in clean Markdown (no headings or bullets). Use formal English.";
                userQuery = `Write a compelling luxury marketing story for the product: ${productName}.`;
            }

            openModal(modalTitle);
            showLoading(featureType === 'story' ? 'Writing the exclusive narrative...' : 'Crafting a bespoke recommendation...');

            const payload = {
                contents: [{ parts: [{ text: userQuery }] }],
                systemInstruction: {
                    parts: [{ text: systemPrompt }]
                },
            };

            const options = {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify(payload)
            };

            try {
                const response = await fetchWithExponentialBackoff(API_URL, options);
                const result = await response.json();

                const text = result.candidates?.[0]?.content?.parts?.[0]?.text || "Apologies, the AI feature is currently unavailable. Please try again shortly.";
                
                document.getElementById('modal-content-text').innerHTML = text; 
            } catch (error) {
                console.error("Gemini API call error:", error);
                showError("An error occurred while fetching the AI content. Please try again.");
            } finally {
                document.getElementById('modal-loading-indicator').classList.add('hidden');
            }
        }

        // --- Gemini LLM ফিচার: গ্লোবাল লাক্সারি ট্রেন্ডস (Grounded Search) ---
        
        async function getLuxuryTrends() {
            openModal("✨ গ্লোবাল লাক্সারি ট্রেন্ডস স্ন্যাপশট");
            showLoading('Analyzing real-time global market data...');

            const systemPrompt = "You are a top-tier luxury market analyst for Billionaire Cloth. Summarize the 3 most important, current global trends affecting high-end fashion, materials, and consumption patterns. Be concise, providing each trend in a short, separate paragraph. Your analysis must be grounded in real-time information. Use formal, professional English.";
            const userQuery = "What are the latest global trends in luxury fashion and materials?";

            const payload = {
                contents: [{ parts: [{ text: userQuery }] }],
                tools: [{ "google_search": {} }], // Google Search গ্রাউন্ডিং সক্ষম করুন
                systemInstruction: {
                    parts: [{ text: systemPrompt }]
                },
            };

            const options = {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify(payload)
            };

            try {
                const response = await fetchWithExponentialBackoff(API_URL, options);
                const result = await response.json();

                const candidate = result.candidates?.[0];
                const text = candidate?.content?.parts?.[0]?.text || "Apologies, the trend analysis service is currently unavailable. Please try again shortly.";
                
                let sourcesHtml = '';
                const groundingMetadata = candidate?.groundingMetadata;
                if (groundingMetadata && groundingMetadata.groundingAttributions) {
                    const sources = groundingMetadata.groundingAttributions
                        .map(attr => ({
                            uri: attr.web?.uri,
                            title: attr.web?.title,
                        }))
                        .filter(source => source.uri && source.title);

                    if (sources.length > 0) {
                        sourcesHtml = '<div class="mt-6 pt-4 border-t border-gray-700">';
                        sourcesHtml += '<p class="text-sm font-bold text-gold mb-2">Sources (উৎস):</p>';
                        sourcesHtml += '<ul class="text-xs text-gray-500 space-y-1">';
                        sources.slice(0, 3).forEach(source => { 
                            sourcesHtml += `<li><a href="${source.uri}" target="_blank" class="hover:text-gold">${source.title}</a></li>`;
                        });
                        sourcesHtml += '</ul></div>';
                    }
                }
                
                // টেক্সট এবং উৎস প্রদর্শন করুন
                document.getElementById('modal-content-text').innerHTML = text.replace(/\n/g, '<br><br>') + sourcesHtml;

            } catch (error) {
                console.error("Gemini Search API call error:", error);
                showError("An error occurred while fetching the global trends. Please try again.");
            } finally {
                document.getElementById('modal-loading-indicator').classList.add('hidden');
            }
        }
        // --- সাধারণ জাভাস্ক্রিপ্ট ---

        // মোবাইল মেনু টগল করার জাভাস্ক্রিপ্ট
        document.getElementById('mobile-menu-button').addEventListener('click', function() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        });

        // ফর্ম সাবমিশন হ্যান্ডেলার
        function handleSubscription(event) {
            event.preventDefault();
            const message = document.getElementById('subscribe-message');
            message.classList.remove('hidden');
            message.textContent = 'Thank you for subscribing to Billionaire Cloth\'s exclusive updates!';
            
            // ইনপুট ফিল্ড ক্লিয়ার করুন
            setTimeout(() => {
                event.target.querySelector('input[type="email"]').value = '';
            }, 500);
        }
    </script>

</body>
</html>
            

</body>
</html># Billionaire-cloth
