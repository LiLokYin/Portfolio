<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>個人作品集 | 簡約專業風格</title>
    <!-- 載入 Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 載入 Inter 字體 -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap" rel="stylesheet">
    <style>
        /* 設定全域字體為 Inter，並將背景和文字顏色設定為黑白灰主調 */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #1a1a1a; /* 深灰/近黑背景 */
            color: #e5e5e5; /* 淺灰文字 */
        }
        /* 導覽列連結的hover效果 */
        .nav-link:hover {
            color: #ffffff;
            border-bottom: 2px solid #ffffff;
        }
        /* 按鈕基礎樣式 */
        .primary-button {
            transition: all 0.3s ease;
        }
        .primary-button:hover {
            background-color: #262626; /* 稍微亮一點的灰 */
            color: #ffffff;
        }
    </style>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'primary-dark': '#1a1a1a',
                        'secondary-dark': '#262626',
                        'light-text': '#e5e5e5',
                    }
                }
            }
        }
    </script>
</head>
<body class="antialiased">

    <!-- 導覽列 (Navbar) -->
    <header class="sticky top-0 z-50 bg-primary-dark shadow-xl shadow-black/30 border-b border-gray-700">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- 名字/品牌 -->
            <a href="#" class="text-2xl font-bold tracking-widest text-white hover:text-gray-300 transition duration-300">
                您的名字 / 藝術家
            </a>

            <!-- 連結 -->
            <div class="space-x-8 hidden md:flex">
                <a href="#about" class="nav-link text-light-text font-medium pb-1 transition duration-200">關於我</a>
                <a href="#work" class="nav-link text-light-text font-medium pb-1 transition duration-200">最新作品</a>
                <a href="#contact" class="nav-link text-light-text font-medium pb-1 transition duration-200">聯絡我們</a>
            </div>

            <!-- Mobile Menu Button (Placeholder for simplicity, full menu toggle omitted) -->
            <div class="md:hidden">
                <button class="text-light-text p-2 rounded-md hover:bg-secondary-dark">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
                </button>
            </div>
        </nav>
    </header>

    <main>
        <!-- 主視覺 (Hero Section) -->
        <section id="hero" class="relative h-[80vh] flex items-center justify-center overflow-hidden">
            <!-- 背景圖 (使用佔位圖URL) -->
            <img 
                src="https://placehold.co/1920x1080/404040/ffffff?text=+攝影作品+Placeholder" 
                alt="主視覺攝影作品" 
                class="absolute inset-0 w-full h-full object-cover opacity-70"
                onerror="this.onerror=null; this.src='https://placehold.co/1920x1080/404040/ffffff?text=攝影作品'" 
            >
            <!-- 疊加層，增加標題對比度 -->
            <div class="absolute inset-0 bg-black opacity-40"></div>
            
            <div class="relative z-10 text-center p-8 bg-black bg-opacity-30 rounded-lg backdrop-blur-sm border border-gray-600">
                <h1 class="text-6xl md:text-8xl font-extrabold tracking-tight text-white shadow-lg">
                    歡迎觀看我的作品
                </h1>
                <p class="mt-4 text-xl md:text-2xl text-gray-200 font-light">
                    透過鏡頭與畫筆，記錄與創造世界
                </p>
            </div>
        </section>

        <!-- 關於我們 (About Us) -->
        <section id="about" class="py-16 md:py-24 max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 border-b border-gray-800">
            <h2 class="text-4xl font-bold text-white mb-8 border-l-4 border-white pl-4">關於我</h2>
            <div class="text-lg leading-relaxed text-gray-400 space-y-4">
                <p>
                    我是 [您的名字]，一位專注於捕捉光影與線條的藝術愛好者。我的創作根植於對細節的觀察和情感的表達，希望在我的作品中，能呈現出對環境、人物和內在世界的深刻理解。
                </p>
                <p>
                    本次作品集旨在為未來的學術申請提供一個全面的視角，展示我在攝影、平面藝術（繪圖/繪畫）和立體創作上的探索與實踐。我堅信，無論是透過鏡頭的精準捕捉，還是畫筆的自由揮灑，每一件作品都承載著獨特的敘事。
                </p>
                <p>
                    期待您的寶貴意見，並很高興與您分享我的創作旅程。
                </p>
            </div>
        </section>

        <!-- 最新作品 (Latest Work) -->
        <section id="work" class="py-16 md:py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-4xl font-bold text-white mb-12 border-l-4 border-white pl-4">最新作品</h2>

            <!-- 作品分類導覽 Tabs -->
            <div class="mb-8 border-b border-gray-700">
                <ul class="flex flex-wrap -mb-px text-sm font-medium text-center" id="work-tabs" role="tablist">
                    <li class="mr-2" role="presentation">
                        <button class="inline-block p-4 border-b-2 border-white rounded-t-lg text-white primary-button" id="photography-tab" data-tab-target="photography" type="button" role="tab" aria-controls="photography" aria-selected="true">攝影 (Photography)</button>
                    </li>
                    <li class="mr-2" role="presentation">
                        <button class="inline-block p-4 border-b-2 border-transparent rounded-t-lg hover:text-gray-300 hover:border-gray-500 primary-button text-gray-400" id="drawing-tab" data-tab-target="drawing" type="button" role="tab" aria-controls="drawing" aria-selected="false">繪圖 (Drawing/Painting)</button>
                    </li>
                    <li role="presentation">
                        <button class="inline-block p-4 border-b-2 border-transparent rounded-t-lg hover:text-gray-300 hover:border-gray-500 primary-button text-gray-400" id="3d-tab" data-tab-target="3d" type="button" role="tab" aria-controls="3d" aria-selected="false">立體作品 (3D/Sculpture)</button>
                    </li>
                </ul>
            </div>

            <!-- 作品內容 Tab Content -->
            <div id="work-tab-content">
                
                <!-- 攝影作品區塊 -->
                <div class="p-4 rounded-lg" id="photography" role="tabpanel" aria-labelledby="photography-tab">
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                        <!-- 作品卡片 1 -->
                        <div class="bg-secondary-dark rounded-xl overflow-hidden shadow-lg hover:shadow-2xl transition duration-300 border border-gray-700">
                            <img src="https://placehold.co/600x400/3d3d3d/b8b8b8?text=作品+A" alt="攝影作品 A" class="w-full h-64 object-cover">
                            <div class="p-6">
                                <h3 class="text-xl font-semibold text-white mb-2">城市輪廓</h3>
                                <p class="text-gray-400 text-sm">類別：黑白街拍 | 時間：2023年春</p>
                                <p class="mt-3 text-gray-500 text-sm">簡述：利用高反差捕捉城市結構的線條美學。</p>
                            </div>
                        </div>
                        <!-- 作品卡片 2 -->
                        <div class="bg-secondary-dark rounded-xl overflow-hidden shadow-lg hover:shadow-2xl transition duration-300 border border-gray-700">
                            <img src="https://placehold.co/600x400/3d3d3d/b8b8b8?text=作品+B" alt="攝影作品 B" class="w-full h-64 object-cover">
                            <div class="p-6">
                                <h3 class="text-xl font-semibold text-white mb-2">晨曦光影</h3>
                                <p class="text-gray-400 text-sm">類別：自然風光 | 時間：2024年夏</p>
                                <p class="mt-3 text-gray-500 text-sm">簡述：在日出時分，微光穿透樹林的瞬間。</p>
                            </div>
                        </div>
                        <!-- 作品卡片 3 -->
                        <div class="bg-secondary-dark rounded-xl overflow-hidden shadow-lg hover:shadow-2xl transition duration-300 border border-gray-700">
                            <img src="https://placehold.co/600x400/3d3d3d/b8b8b8?text=作品+C" alt="攝影作品 C" class="w-full h-64 object-cover">
                            <div class="p-6">
                                <h3 class="text-xl font-semibold text-white mb-2">人像剪影</h3>
                                <p class="text-gray-400 text-sm">類別：人像攝影 | 時間：2023年秋</p>
                                <p class="mt-3 text-gray-500 text-sm">簡述：在逆光下捕捉人物的姿態與輪廓。</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 繪圖作品區塊 (初始隱藏) -->
                <div class="hidden p-4 rounded-lg" id="drawing" role="tabpanel" aria-labelledby="drawing-tab">
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                        <!-- 作品卡片 4 -->
                        <div class="bg-secondary-dark rounded-xl overflow-hidden shadow-lg hover:shadow-2xl transition duration-300 border border-gray-700">
                            <img src="https://placehold.co/600x400/3d3d3d/b8b8b8?text=繪畫+作品+D" alt="繪圖作品 D" class="w-full h-64 object-cover">
                            <div class="p-6">
                                <h3 class="text-xl font-semibold text-white mb-2">炭筆素描：靜物</h3>
                                <p class="text-gray-400 text-sm">媒材：炭筆 | 尺寸：A3</p>
                                <p class="mt-3 text-gray-500 text-sm">簡述：強調材質紋理與陰影對比的練習作。</p>
                            </div>
                        </div>
                        <!-- 作品卡片 5 -->
                        <div class="bg-secondary-dark rounded-xl overflow-hidden shadow-lg hover:shadow-2xl transition duration-300 border border-gray-700">
                            <img src="https://placehold.co/600x400/3d3d3d/b8b8b8?text=繪畫+作品+E" alt="繪圖作品 E" class="w-full h-64 object-cover">
                            <div class="p-6">
                                <h3 class="text-xl font-semibold text-white mb-2">壓克力：抽象空間</h3>
                                <p class="text-gray-400 text-sm">媒材：壓克力 | 尺寸：F6</p>
                                <p class="mt-3 text-gray-500 text-sm">簡述：以黑、白、灰三色構成的幾何抽象畫。</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 立體作品區塊 (初始隱藏) -->
                <div class="hidden p-4 rounded-lg" id="3d" role="tabpanel" aria-labelledby="3d-tab">
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                        <!-- 作品卡片 6 -->
                        <div class="bg-secondary-dark rounded-xl overflow-hidden shadow-lg hover:shadow-2xl transition duration-300 border border-gray-700">
                            <img src="https://placehold.co/600x400/3d3d3d/b8b8b8?text=立體+作品+F" alt="立體作品 F" class="w-full h-64 object-cover">
                            <div class="p-6">
                                <h3 class="text-xl font-semibold text-white mb-2">金屬線編織</h3>
                                <p class="text-gray-400 text-sm">媒材：不鏽鋼絲 | 尺寸：20cm高</p>
                                <p class="mt-3 text-gray-500 text-sm">簡述：探討結構與輕盈感的立體作品。</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
        </section>

        <!-- 聯絡我們 (Contact Us) -->
        <section id="contact" class="py-16 md:py-24 bg-secondary-dark border-t border-gray-700">
            <div class="max-w-xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <h2 class="text-4xl font-bold text-white mb-6">聯絡我們</h2>
                <p class="text-lg text-gray-400 mb-8">
                    若您對我的作品感興趣、需要進一步了解作品細節，或是有任何合作機會，請透過以下方式聯繫我。
                </p>
                <div class="space-y-4">
                    <p class="text-xl font-medium text-white">電子郵件：<a href="mailto:your.email@example.com" class="text-gray-300 hover:text-white transition duration-200 underline">your.email@example.com</a></p>
                    <p class="text-xl font-medium text-white">電話：+886 9XX XXX XXX</p>
                    <p class="text-gray-500 text-sm pt-4">此處可加上作品集下載或預約拜訪連結 (如果適用)。</p>
                </div>
            </div>
        </section>

    </main>

    <!-- 頁腳 (Footer) -->
    <footer class="bg-primary-dark py-8 border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center text-sm text-gray-500">
            <p>&copy; 2024 [您的名字/品牌]. 版權所有。</p>
            <p>作品集展示，設計風格：簡約專業 (Minimalist & Professional)</p>
        </div>
    </footer>

    <!-- JavaScript 處理 Tab 切換邏輯 -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const tabsContainer = document.getElementById('work-tabs');
            const tabContentContainer = document.getElementById('work-tab-content');
            
            if (!tabsContainer || !tabContentContainer) return;

            // 預設選中的 Tab
            let activeTabId = 'photography';
            
            // 處理 Tab 點擊事件
            tabsContainer.addEventListener('click', (event) => {
                const targetButton = event.target.closest('button[data-tab-target]');
                if (!targetButton) return;

                const newActiveTabId = targetButton.getAttribute('data-tab-target');
                if (newActiveTabId === activeTabId) return;

                // 1. 更新按鈕樣式
                // 移除舊的 active 樣式
                document.getElementById(`${activeTabId}-tab`).classList.remove('border-white', 'text-white');
                document.getElementById(`${activeTabId}-tab`).classList.add('border-transparent', 'hover:text-gray-300', 'hover:border-gray-500', 'text-gray-400');
                
                // 添加新的 active 樣式
                targetButton.classList.add('border-white', 'text-white');
                targetButton.classList.remove('border-transparent', 'hover:text-gray-300', 'hover:border-gray-500', 'text-gray-400');


                // 2. 更新內容區塊顯示
                // 隱藏舊的內容
                document.getElementById(activeTabId).classList.add('hidden');
                document.getElementById(activeTabId).setAttribute('aria-selected', 'false');

                // 顯示新的內容
                document.getElementById(newActiveTabId).classList.remove('hidden');
                document.getElementById(newActiveTabId).setAttribute('aria-selected', 'true');
                
                // 更新 active 狀態
                activeTabId = newActiveTabId;
            });
        });
    </script>
</body>
</html>
