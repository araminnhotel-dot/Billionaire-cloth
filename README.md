<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Billionaire Cloth | Exclusive Apparel & Luxury Goods</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom Styles for a Rich, Luxury Feel */
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

        /* Rich Gold Text Utility */
        .text-gold {
            color: var(--color-gold);
        }

        /* Gold Button Styling */
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

        /* Subtle Hover Effect for Nav Links */
        .nav-link:hover {
            color: var(--color-gold);
            text-shadow: 0 0 5px rgba(255, 255, 255, 0.3);
        }

        /* Product Card Effects */
        .product-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            background-color: #1a1a1a;
            border: 1px solid #2d2d2d;
        }
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5), 0 0 10px rgba(207, 168, 98, 0.3);
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
        .ai-button-secondary {
            background-color: #2d2d2d;
            color: var(--color-gold);
            transition: all 0.3s ease;
        }
        .ai-button-secondary:hover {
            background-color: #3a3a3a;
        }
    </style>
</head>
<body>

    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-black/80 backdrop-blur-sm shadow-lg border-b border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- Logo -->
            <a href="#" class="text-3xl font-extrabold tracking-widest uppercase text-gold">
                BC.
            </a>

            <!-- Desktop Nav Links -->
            <nav class="hidden lg:flex space-x-8">
                <a href="#new-arrivals" class="nav-link text-sm font-medium uppercase tracking-wider">New Arrivals</a>
                <a href="#featured" class="nav-link text-sm font-medium uppercase tracking-wider">The Collection</a>
                <a href="#" class="nav-link text-sm font-medium uppercase tracking-wider">Lookbook</a>
                <a href="#" class="nav-link text-sm font-medium uppercase tracking-wider">Our Story</a>
            </nav>

            <!-- Icons/Actions (Cart & Menu Button) -->
            <div class="flex items-center space-x-6">
                <!-- Search Icon (Using SVG for simplicity) -->
                <button class="text-gray-400 hover:text-gold transition duration-200 hidden sm:block">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                    </svg>
                </button>
                <!-- Cart Icon -->
                <button class="relative text-gray-400 hover:text-gold transition duration-200">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
                    </svg>
                    <span class="absolute top-0 right-0 inline-flex items-center justify-center px-2 py-1 text-xs font-bold leading-none text-black transform translate-x-1/2 -translate-y-1/2 bg-gold rounded-full">3</span>
                </button>
                <!-- Mobile Menu Button -->
                <button id="mobile-menu-button" class="lg:hidden text-gray-400 hover:text-gold transition duration-200">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
                    </svg>
                </button>
            </div>
        </div>

        <!-- Mobile Menu (Hidden by default) -->
        <nav id="mobile-menu" class="hidden lg:hidden px-4 pt-2 pb-4 space-y-1 border-t border-gray-800">
            <a href="#new-arrivals" class="block py-2 text-sm font-medium text-gray-300 hover:text-gold rounded-md">New Arrivals</a>
            <a href="#featured" class="block py-2 text-sm font-medium text-gray-300 hover:text-gold rounded-md">The Collection</a>
            <a href="#" class="block py-2 text-sm font-medium text-gray-300 hover:text-gold rounded-md">Lookbook</a>
            <a href="#" class="block py-2 text-sm font-medium text-gray-300 hover:text-gold rounded-md">Our Story</a>
            <a href="#" class="block py-2 text-sm font-medium text-gold border-t border-gray-800 mt-2 pt-2">Account / Sign In</a>
        </nav>
    </header>

    <main>
        <!-- Hero Section: High Impact Visual -->
        <section class="relative h-screen flex items-center justify-center overflow-hidden">
            <!-- Background Image Placeholder (Dramatic, cinematic feel) -->
            <div class="absolute inset-0">
                <img src="https://placehold.co/1920x1080/1a1a1a/cfa862?text=THE+NEW+STANDARD" 
                     class="w-full h-full object-cover opacity-70" 
                     alt="Cinematic fashion shot with luxurious texture.">
                <!-- Dark Overlay -->
                <div class="absolute inset-0 bg-black opacity-40"></div>
            </div>

            <!-- Content -->
            <div class="relative z-10 text-center max-w-4xl px-4">
                <h1 class="text-4xl sm:text-6xl lg:text-8xl font-black uppercase mb-6 leading-tight text-white">
                    <span class="text-gold">The Standard</span> Is Set.
                </h1>
                <p class="text-lg sm:text-xl text-gray-300 mb-10 tracking-wider">
                    Exclusive materials, bespoke tailoring. Wear the wealth you've earned.
                </p>
                <a href="#new-arrivals" class="btn-gold px-10 py-4 text-sm font-bold uppercase rounded-lg tracking-widest">
                    Explore New Arrivals
                </a>
            </div>
        </section>

        <!-- Featured Products Grid -->
        <section id="featured" class="py-16 md:py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-4xl font-bold uppercase mb-12 text-center text-white">
                The Core Collection
            </h2>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Product Card 1: Executive Blazer (AI Features Here) -->
                <div class="product-card rounded-xl overflow-hidden shadow-2xl">
                    <img src="https://placehold.co/600x800/222222/cfa862?text=EXECUTIVE+BLAZER" 
                         class="w-full h-72 object-cover object-center" 
                         alt="Executive collection blazer">
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-semibold mb-2 text-white">The Executive Blazer</h3>
                        <p class="text-gray-400 text-sm mb-4">Cashmere Blend</p>
                        <p class="text-2xl font-bold text-gold">$1,999</p>
                        <!-- AI Feature 1: Style Match -->
                        <button onclick="generateStyleAdvice('Executive Blazer in Cashmere Blend', 'style')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-2">
                            ✨ AI Style Match
                        </button>
                        <!-- AI Feature 2: Product Story -->
                        <button onclick="generateStyleAdvice('Executive Blazer in Cashmere Blend', 'story')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-3">
                            ✨ Generate Product Story
                        </button>
                        <button class="btn-gold w-full py-2 text-xs uppercase font-semibold rounded-lg">Add to Cart</button>
                    </div>
                </div>

                <!-- Product Card 2: Signature Watch -->
                <div class="product-card rounded-xl overflow-hidden shadow-2xl">
                    <img src="https://placehold.co/600x800/333333/cfa862?text=SIGNATURE+TIMEPIECE" 
                         class="w-full h-72 object-cover object-center" 
                         alt="Signature collection timepiece">
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-semibold mb-2 text-white">Signature Timepiece</h3>
                        <p class="text-gray-400 text-sm mb-4">Swiss Movement</p>
                        <p class="text-2xl font-bold text-gold">$9,500</p>
                        <!-- AI Feature 1: Style Match -->
                        <button onclick="generateStyleAdvice('Signature Timepiece with Swiss Movement', 'style')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-2">
                            ✨ AI Style Match
                        </button>
                        <!-- AI Feature 2: Product Story -->
                        <button onclick="generateStyleAdvice('Signature Timepiece with Swiss Movement', 'story')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-3">
                            ✨ Generate Product Story
                        </button>
                        <button class="btn-gold w-full py-2 text-xs uppercase font-semibold rounded-lg">Add to Cart</button>
                    </div>
                </div>

                <!-- Product Card 3: Silk Dress Shirt -->
                <div class="product-card rounded-xl overflow-hidden shadow-2xl">
                    <img src="https://placehold.co/600x800/444444/cfa862?text=SILK+DRESS+SHIRT" 
                         class="w-full h-72 object-cover object-center" 
                         alt="Luxury silk dress shirt">
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-semibold mb-2 text-white">Heirloom Silk Shirt</h3>
                        <p class="text-gray-400 text-sm mb-4">100% Italian Silk</p>
                        <p class="text-2xl font-bold text-gold">$499</p>
                         <!-- AI Feature 1: Style Match -->
                        <button onclick="generateStyleAdvice('Heirloom Silk Shirt in 100% Italian Silk', 'style')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-2">
                            ✨ AI Style Match
                        </button>
                        <!-- AI Feature 2: Product Story -->
                        <button onclick="generateStyleAdvice('Heirloom Silk Shirt in 100% Italian Silk', 'story')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-3">
                            ✨ Generate Product Story
                        </button>
                        <button class="btn-gold w-full py-2 text-xs uppercase font-semibold rounded-lg">Add to Cart</button>
                    </div>
                </div>

                <!-- Product Card 4: Diamond Cufflinks -->
                <div class="product-card rounded-xl overflow-hidden shadow-2xl">
                    <img src="https://placehold.co/600x800/555555/cfa862?text=DIAMOND+CUFFLINKS" 
                         class="w-full h-72 object-cover object-center" 
                         alt="Diamond accent cufflinks">
                    <div class="p-6 text-center">
                        <h3 class="text-xl font-semibold mb-2 text-white">Diamond Accents</h3>
                        <p class="text-gray-400 text-sm mb-4">Rose Gold Plated</p>
                        <p class="text-2xl font-bold text-gold">$2,500</p>
                         <!-- AI Feature 1: Style Match -->
                        <button onclick="generateStyleAdvice('Diamond Accents Cufflinks in Rose Gold Plating', 'style')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-2">
                            ✨ AI Style Match
                        </button>
                        <!-- AI Feature 2: Product Story -->
                        <button onclick="generateStyleAdvice('Diamond Accents Cufflinks in Rose Gold Plating', 'story')" 
                                class="w-full py-2 text-xs uppercase font-semibold rounded-lg ai-button-secondary hover:bg-gray-700 transition duration-200 mb-3">
                            ✨ Generate Product Story
                        </button>
                        <button class="btn-gold w-full py-2 text-xs uppercase font-semibold rounded-lg">Add to Cart</button>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <a href="#" class="text-sm font-semibold uppercase text-gold hover:text-white transition duration-200 border-b border-gold hover:border-white pb-1">
                    View All Collections &rarr;
                </a>
            </div>
        </section>

        <!-- Brand Manifesto / Motto Section -->
        <section id="new-arrivals" class="bg-[#1a1a1a] py-16 md:py-32">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <p class="text-lg font-light italic text-gray-500 mb-4 tracking-widest">
                    THE BILIONAIRE PHILOSOPHY
                </p>
                <blockquote class="text-3xl sm:text-5xl font-extrabold leading-snug text-white">
                    "Luxury is not a price point, but an <span class="text-gold">uncompromising dedication</span> to the pursuit of perfection."
                </blockquote>
                <p class="text-base text-gray-400 mt-8 max-w-2xl mx-auto">
                    Every thread, every stitch, every detail is engineered for those who understand that true value lies in enduring quality and masterful craftsmanship. We do not follow trends—we define legacy.
                </p>
            </div>
        </section>
        
        <!-- Lookbook Call-to-Action -->
        <section class="py-16 bg-cover bg-center" style="background-image: url('https://placehold.co/1920x600/101010/888888?text=THE+EXCLUSIVE+LOOKBOOK');">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center py-12 bg-black/50 rounded-lg">
                <h3 class="text-3xl font-bold uppercase mb-4 text-white">Discover the <span class="text-gold">Lookbook</span></h3>
                <p class="text-gray-300 mb-8 max-w-xl mx-auto">
                    See the latest runway pieces and style them before anyone else. Access granted for members only.
                </p>
                <button class="btn-gold px-8 py-3 text-sm font-bold uppercase rounded-lg">
                    Request Early Access
                </button>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="bg-black border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="grid grid-cols-2 md:grid-cols-5 gap-8">
                <!-- Brand Info -->
                <div class="col-span-2 md:col-span-1">
                    <h3 class="text-2xl font-extrabold tracking-widest uppercase text-gold mb-4">BC.</h3>
                    <p class="text-sm text-gray-500">
                        The pinnacle of luxury apparel and enduring style.
                    </p>
                </div>
                
                <!-- Shop Links -->
                <div>
                    <h4 class="text-lg font-semibold mb-4 text-white uppercase">Shop</h4>
                    <ul class="space-y-2 text-sm text-gray-400">
                        <li><a href="#" class="hover:text-gold transition">Men's Collection</a></li>
                        <li><a href="#" class="hover:text-gold transition">Women's Collection</a></li>
                        <li><a href="#" class="hover:text-gold transition">Accessories</a></li>
                        <li><a href="#" class="hover:text-gold transition">Pre-Order</a></li>
                    </ul>
                </div>

                <!-- Customer Service -->
                <div>
                    <h4 class="text-lg font-semibold mb-4 text-white uppercase">Support</h4>
                    <ul class="space-y-2 text-sm text-gray-400">
                        <li><a href="#" class="hover:text-gold transition">Contact Us</a></li>
                        <li><a href="#" class="hover:text-gold transition">Shipping & Returns</a></li>
                        <li><a href="#" class="hover:text-gold transition">Size Guide</a></li>
                        <li><a href="#" class="hover:text-gold transition">FAQ</a></li>
                    </ul>
                </div>
                
                <!-- Company -->
                <div>
                    <h4 class="text-lg font-semibold mb-4 text-white uppercase">Company</h4>
                    <ul class="space-y-2 text-sm text-gray-400">
                        <li><a href="#" class="hover:text-gold transition">Our Story</a></li>
                        <li><a href="#" class="hover:text-gold transition">Careers</a></li>
                        <li><a href="#" class="hover:text-gold transition">Press</a></li>
                        <li><a href="#" class="hover:text-gold transition">Affiliates</a></li>
                    </ul>
                </div>
                
                <!-- Newsletter Signup (Now includes AI trend analysis) -->
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
                        ✨ Get Global Luxury Trends Snapshot
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
        // --- Gemini API Configuration ---
        const API_KEY = ""; // Canvas will automatically provide the API key
        const API_URL = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${API_KEY}`;
        const MAX_RETRIES = 5;

        // --- Utility Functions ---

        // Function to handle fetch with exponential backoff
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

        // Function to open the modal and set title
        function openModal(title) {
            document.getElementById('modal-title').textContent = title;
            document.getElementById('ai-modal').classList.remove('hidden');
        }

        // Function to close the modal
        function closeModal() {
            document.getElementById('ai-modal').classList.add('hidden');
            document.getElementById('modal-content-text').innerHTML = ''; // Clear previous content
            document.getElementById('modal-loading-indicator').classList.add('hidden');
        }
        
        // Function to show loading state
        function showLoading(message = 'Crafting a bespoke recommendation...') {
            const modalTextElement = document.getElementById('modal-content-text');
            const loadingIndicator = document.getElementById('modal-loading-indicator');
            modalTextElement.textContent = '';
            loadingIndicator.classList.remove('hidden');
            loadingIndicator.querySelector('p').textContent = message;
        }
        
        // Function to display error
        function showError(message) {
            document.getElementById('modal-content-text').innerHTML = `<p class="text-red-400">${message}</p>`;
        }

        // --- Gemini LLM Feature: AI Style Match & Product Story ---

        async function generateStyleAdvice(productName, featureType) {
            let systemPrompt = "";
            let userQuery = "";
            let modalTitle = "";
            
            if (featureType === 'style') {
                modalTitle = `✨ AI Style Match for: ${productName}`;
                systemPrompt = "You are 'The Billionaire Cloth AI Stylist.' Your persona is sophisticated, concise, and focused on high-end luxury fashion. Always recommend three complementary items (shoes, accessories, or other apparel) and describe the overall aesthetic, using rich, evocative language. The response must be a single, cohesive paragraph formatted in clean Markdown (no headings or bullets).";
                userQuery = `Generate a complete styling recommendation for a ${productName}.`;
            } else if (featureType === 'story') {
                modalTitle = `✨ Product Story: The ${productName}`;
                systemPrompt = "You are a master luxury copywriter for Billionaire Cloth. Your task is to write a highly evocative, short narrative (3-5 sentences) that describes the product's exclusive heritage, materials, and the feeling of owning it. Use hyperbole and rich, sensual language. The response must be a single, cohesive paragraph formatted in clean Markdown (no headings or bullets).";
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
                
                document.getElementById('modal-content-text').innerHTML = text; // LLM response should contain necessary formatting
            } catch (error) {
                console.error("Gemini API call error:", error);
                showError("An error occurred while fetching the AI content. Please try again.");
            } finally {
                document.getElementById('modal-loading-indicator').classList.add('hidden');
            }
        }

        // --- Gemini LLM Feature: Global Luxury Trends (Grounded Search) ---
        
        async function getLuxuryTrends() {
            openModal("✨ Global Luxury Trend Snapshot");
            showLoading('Analyzing real-time global market data...');

            const systemPrompt = "You are a top-tier luxury market analyst for Billionaire Cloth. Summarize the 3 most important, current global trends affecting high-end fashion, materials, and consumption patterns. Be concise, providing each trend in a short, separate paragraph. Your analysis must be grounded in real-time information. Use formal, professional language.";
            const userQuery = "What are the latest global trends in luxury fashion and materials?";

            const payload = {
                contents: [{ parts: [{ text: userQuery }] }],
                tools: [{ "google_search": {} }], // Enable Google Search grounding
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
                        sourcesHtml += '<p class="text-sm font-bold text-gold mb-2">Sources:</p>';
                        sourcesHtml += '<ul class="text-xs text-gray-500 space-y-1">';
                        sources.slice(0, 3).forEach(source => { // Limit to 3 sources for clean display
                            sourcesHtml += `<li><a href="${source.uri}" target="_blank" class="hover:text-gold">${source.title}</a></li>`;
                        });
                        sourcesHtml += '</ul></div>';
                    }
                }
                
                // Display text and sources
                document.getElementById('modal-content-text').innerHTML = text.replace(/\n/g, '<br><br>') + sourcesHtml;

            } catch (error) {
                console.error("Gemini Search API call error:", error);
                showError("An error occurred while fetching the global trends. Please try again.");
            } finally {
                document.getElementById('modal-loading-indicator').classList.add('hidden');
            }
        }
        // --- General JavaScript ---

        // JavaScript for Mobile Menu Toggle
        document.getElementById('mobile-menu-button').addEventListener('click', function() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        });

        // Simple form submission handler
        function handleSubscription(event) {
            event.preventDefault();
            const message = document.getElementById('subscribe-message');
            message.classList.remove('hidden');
            message.textContent = 'Thank you for subscribing to Billionaire Cloth\'s exclusive updates!';
            
            // Optionally clear the input field after a short delay
            setTimeout(() => {
                event.target.querySelector('input[type="email"]').value = '';
            }, 500);
        }
    </script>

</body>
</html># Billionaire-cloth
