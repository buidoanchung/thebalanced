<html lang="vi" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard Tương Tác: Chiến Lược Thị Trường Đồng Phục HR</title>
    <!-- Chosen Palette: Calm Corporate (Neutrals: #F8F7F4, #EAE7E1; Accent: #3A7CA5; Highlight: #D6A25B; Text: #2F3D40) -->
    <!-- Application Structure Plan: The SPA is designed as an interactive dashboard, diverging from the linear report structure for better usability. It follows a narrative flow: 1. **Hero Header**: Captures the core opportunity. 2. **Sticky Navigation**: Enables non-linear exploration of key pillars: Market, Customer, Competition, and Strategy. 3. **The Opportunity**: A visual summary of macro trends (Sustainability, Hybrid Work) to establish context. 4. **The Target Customer**: Deep-dives into the HR professional, focusing on the critical "dual role" insight. 5. **The Battlefield**: An interactive competitor analysis section. 6. **The Game Plan**: A tabbed interface to present the multi-faceted strategy (Product, Pricing, Distribution) without overwhelming the user. This structure guides the user from the "why" (market opportunity) to the "who" (customer) and finally the "how" (the strategy), making complex information digestible and engaging. -->
    <!-- Visualization & Content Choices: 
        - Market Growth: Goal: Change -> Viz: Line Chart (Chart.js) -> Interaction: Hover for details -> Justification: Clearly shows trend over time.
        - Consumer Attitude: Goal: Inform -> Viz: Donut Chart with central text (Chart.js/HTML) -> Interaction: Static -> Justification: Strong visual for a key statistic.
        - Hybrid Work Needs: Goal: Inform -> Viz: Icon-based list (HTML/Tailwind/Unicode) -> Interaction: Static -> Justification: Quickly communicates key attributes.
        - HR Dual Role: Goal: Organize -> Viz: Overlapping circles diagram (HTML/Tailwind) -> Interaction: Static -> Justification: Visually represents the core strategic insight of the report.
        - Competitor Pricing: Goal: Compare -> Viz: Floating Bar Chart (Chart.js) -> Interaction: Hover tooltips -> Justification: Effectively shows price ranges for multiple competitors.
        - Strategy Tabs: Goal: Organize -> Viz: Tabbed Interface (HTML/JS) -> Interaction: Click to switch views -> Justification: Manages complex strategy information in a clean, user-controlled manner.
        - Distribution Model: Goal: Organize -> Viz: Flowchart (HTML/Tailwind) -> Interaction: Static -> Justification: Illustrates the multi-channel process clearly without SVG/Mermaid.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Be Vietnam Pro', sans-serif;
            background-color: #F8F7F4;
            color: #2F3D40;
        }
        .chart-container {
            position: relative;
            width: 100%;
            height: 300px;
            max-height: 350px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
                max-height: 400px;
            }
        }
        .nav-link.active {
            color: #D6A25B;
            font-weight: 600;
        }
        .strategy-tab.active {
            background-color: #3A7CA5;
            color: white;
        }
        .strategy-tab {
            background-color: #EAE7E1;
            color: #3A7CA5;
        }
    </style>
</head>
<body class="antialiased">

    <!-- Header -->
    <header class="text-center py-16 px-4 bg-white shadow-sm">
        <h1 class="text-3xl md:text-5xl font-extrabold text-[#3A7CA5] mb-4">Dashboard Chiến Lược: Thị Trường Đồng Phục</h1>
        <p class="text-lg md:text-xl text-[#2F3D40] max-w-3xl mx-auto">Một phân tích tương tác về cơ hội chinh phục ngách khách hàng Nữ Chuyên gia Nhân sự tại Việt Nam.</p>
    </header>

    <!-- Sticky Navigation -->
    <nav id="navbar" class="sticky top-0 z-50 bg-white/80 backdrop-blur-lg shadow-md">
        <div class="container mx-auto px-4">
            <div class="flex justify-center items-center h-16 space-x-4 md:space-x-8">
                <a href="#opportunity" class="nav-link text-gray-600 hover:text-[#D6A25B] transition-colors duration-300 font-medium px-3 py-2 text-sm md:text-base">Cơ Hội</a>
                <a href="#customer" class="nav-link text-gray-600 hover:text-[#D6A25B] transition-colors duration-300 font-medium px-3 py-2 text-sm md:text-base">Khách Hàng</a>
                <a href="#competition" class="nav-link text-gray-600 hover:text-[#D6A25B] transition-colors duration-300 font-medium px-3 py-2 text-sm md:text-base">Cạnh Tranh</a>
                <a href="#strategy" class="nav-link text-gray-600 hover:text-[#D6A25B] transition-colors duration-300 font-medium px-3 py-2 text-sm md:text-base">Chiến Lược</a>
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="container mx-auto p-4 md:p-8">

        <!-- Section 1: The Opportunity -->
        <section id="opportunity" class="py-16">
            <h2 class="text-3xl font-bold text-center mb-4 text-[#3A7CA5]">Cơ Hội Vàng Từ Các Xu Hướng Vĩ Mô</h2>
            <p class="text-center text-gray-600 max-w-3xl mx-auto mb-12">Thị trường đang được định hình lại bởi những thay đổi lớn trong nhận thức người tiêu dùng và mô hình làm việc, tạo ra một không gian độc đáo cho các sản phẩm đồng phục thế hệ mới.</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Card: Sustainable Fashion -->
                <div class="bg-white rounded-lg shadow-lg p-6 transform hover:-translate-y-2 transition-transform duration-300">
                    <h3 class="font-bold text-xl mb-3 text-[#3A7CA5]">Tăng Trưởng Thời Trang Bền Vững</h3>
                    <p class="text-gray-600 text-sm mb-4">Thị trường toàn cầu được dự báo tăng trưởng thần tốc, cho thấy nhu cầu ngày càng cao cho các sản phẩm có trách nhiệm.</p>
                    <div class="chart-container h-56 md:h-64">
                        <canvas id="sustainableGrowthChart"></canvas>
                    </div>
                </div>

                <!-- Card: Consumer Attitude -->
                <div class="bg-white rounded-lg shadow-lg p-6 transform hover:-translate-y-2 transition-transform duration-300 flex flex-col justify-center items-center">
                    <h3 class="font-bold text-xl mb-3 text-center text-[#3A7CA5]">Thái Độ Người Tiêu Dùng Việt</h3>
                    <div class="w-48 h-48 relative">
                       <canvas id="consumerAttitudeChart"></canvas>
                       <div class="absolute inset-0 flex items-center justify-center text-5xl font-bold text-[#3A7CA5]">72%</div>
                    </div>
                    <p class="text-gray-600 text-sm text-center mt-4">Sẵn sàng chi trả nhiều hơn cho các sản phẩm "xanh", thân thiện môi trường.</p>
                </div>

                <!-- Card: Hybrid Work -->
                <div class="bg-white rounded-lg shadow-lg p-6 transform hover:-translate-y-2 transition-transform duration-300">
                    <h3 class="font-bold text-xl mb-3 text-[#3A7CA5]">Yêu Cầu Từ Mô Hình Hybrid</h3>
                    <p class="text-gray-600 text-sm mb-6">Trang phục công sở cần phải vượt qua giới hạn của văn phòng, hướng tới sự đa năng và thoải mái tuyệt đối.</p>
                    <div class="space-y-4">
                        <div class="flex items-center">
                            <span class="text-3xl mr-4 text-[#D6A25B]">✓</span>
                            <div>
                                <h4 class="font-semibold text-gray-800">Đa năng & Linh hoạt</h4>
                                <p class="text-xs text-gray-500">Mặc đi làm, đi chơi, gặp gỡ bạn bè.</p>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <span class="text-3xl mr-4 text-[#D6A25B]">✓</span>
                            <div>
                                <h4 class="font-semibold text-gray-800">Chất liệu cao cấp</h4>
                                <p class="text-xs text-gray-500">Thoáng khí, co giãn, ít nhăn.</p>
                            </div>
                        </div>
                        <div class="flex items-center">
                             <span class="text-3xl mr-4 text-[#D6A25B]">✓</span>
                            <div>
                                <h4 class="font-semibold text-gray-800">Phong cách "Smart Casual"</h4>
                                <p class="text-xs text-gray-500">Thanh lịch nhưng vẫn thoải mái.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Section 2: The Target Customer -->
        <section id="customer" class="py-16 bg-[#EAE7E1] -mx-4 md:-mx-8 px-4 md:px-8">
            <h2 class="text-3xl font-bold text-center mb-4 text-[#3A7CA5]">Trái Tim Chiến Lược: Thấu Hiểu Chuyên Gia HR</h2>
            <p class="text-center text-gray-600 max-w-3xl mx-auto mb-12">Thành công nằm ở việc giải quyết "nỗi đau" của nhóm khách hàng đặc biệt này, những người giữ vai trò kép trong quyết định mua sắm đồng phục.</p>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-center">
                <div class="bg-white rounded-lg shadow-lg p-6">
                    <h3 class="font-bold text-xl mb-4 text-[#3A7CA5]">Nhu Cầu và Kỳ Vọng</h3>
                    <p class="text-gray-600 text-sm mb-4">Đối với họ, trang phục không chỉ là quần áo. Đó là công cụ giao tiếp, thể hiện sự chuyên nghiệp, uy tín và phong cách cá nhân.</p>
                    <ul class="list-none space-y-3 text-gray-700">
                        <li class="flex items-start"><span class="text-xl text-[#D6A25B] mr-2 mt-1">●</span><div><strong class="font-semibold">Chất lượng & Thoải mái:</strong> Ưu tiên hàng đầu cho ngày dài làm việc.</div></li>
                        <li class="flex items-start"><span class="text-xl text-[#D6A25B] mr-2 mt-1">●</span><div><strong class="font-semibold">Thẩm mỹ & Tôn dáng:</strong> Thiết kế hiện đại, che khuyết điểm.</div></li>
                        <li class="flex items-start"><span class="text-xl text-[#D6A25B] mr-2 mt-1">●</span><div><strong class="font-semibold">Phong cách chuyên nghiệp:</strong> "Smart Casual" và "Power Dressing" được ưa chuộng.</div></li>
                        <li class="flex items-start"><span class="text-xl text-[#D6A25B] mr-2 mt-1">●</span><div><strong class="font-semibold">Câu chuyện thương hiệu:</strong> Bị thu hút bởi các giá trị bền vững và đạo đức.</div></li>
                    </ul>
                </div>

                <div class="bg-white rounded-lg shadow-lg p-6 h-full flex flex-col items-center justify-center">
                    <h3 class="font-bold text-xl text-center mb-4 text-[#3A7CA5]">"Vai Trò Kép" - Chìa Khóa Chiến Lược</h3>
                     <p class="text-gray-600 text-center text-sm mb-6">Họ vừa là người dùng cuối, vừa là người quyết định. Chinh phục trái tim của họ với tư cách cá nhân là cách để có được hợp đồng doanh nghiệp.</p>
                     <div class="relative w-full h-52 flex items-center justify-center">
                        <div class="absolute w-40 h-40 bg-[#3A7CA5] bg-opacity-70 rounded-full flex items-center justify-center text-white text-center p-4 transform -translate-x-12" style="z-index: 1;">
                            <span class="font-semibold text-sm">Người Dùng Cuối<br><small class="font-normal">(End-user)</small></span>
                        </div>
                        <div class="absolute w-40 h-40 bg-[#D6A25B] bg-opacity-70 rounded-full flex items-center justify-center text-white text-center p-4 transform translate-x-12" style="z-index: 2;">
                           <span class="font-semibold text-sm">Người Quyết Định<br><small class="font-normal">(Gatekeeper)</small></span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Section 3: The Competition -->
        <section id="competition" class="py-16">
            <h2 class="text-3xl font-bold text-center mb-4 text-[#3A7CA5]">Bản Đồ Cạnh Tranh</h2>
            <p class="text-center text-gray-600 max-w-3xl mx-auto mb-12">Thị trường có sự phân hóa rõ rệt, tạo ra khoảng trống đáng giá ở phân khúc "Trung cấp Thời trang" - nơi chất lượng và phong cách gặp gỡ mức giá hợp lý.</p>
            <div class="bg-white rounded-lg shadow-lg p-6">
                <h3 class="font-bold text-xl mb-4 text-[#3A7CA5]">Phân Tích Khung Giá Áo Sơ Mi Nữ (Tham khảo B2B)</h3>
                <p class="text-gray-600 text-sm mb-4">Biểu đồ dưới đây thể hiện khoảng giá (từ thấp nhất đến cao nhất) của các đối thủ cạnh tranh chính. NNS được đề xuất một khung giá chiến lược để lấp đầy khoảng trống thị trường.</p>
                <div class="chart-container h-[450px] max-h-[500px]">
                    <canvas id="competitorPriceChart"></canvas>
                </div>
            </div>
        </section>

        <!-- Section 4: The Game Plan -->
        <section id="strategy" class="py-16 bg-[#EAE7E1] -mx-4 md:-mx-8 px-4 md:px-8">
            <h2 class="text-3xl font-bold text-center mb-4 text-[#3A7CA5]">Chiến Lược Toàn Diện cho NNS</h2>
            <p class="text-center text-gray-600 max-w-3xl mx-auto mb-12">Một kế hoạch hành động chi tiết, được xây dựng trên ba trụ cột: Sản phẩm, Giá & Phân phối, và Marketing, nhằm mục tiêu chiếm lĩnh thị trường ngách.</p>
            
            <div class="bg-white rounded-lg shadow-lg p-6">
                <!-- Strategy Tabs -->
                <div class="mb-6 flex flex-wrap justify-center border-b border-gray-300">
                    <button data-tab="product" class="strategy-tab active text-sm md:text-base font-semibold px-4 py-3 rounded-t-lg transition-colors duration-300">Sản Phẩm</button>
                    <button data-tab="distribution" class="strategy-tab text-sm md:text-base font-semibold px-4 py-3 rounded-t-lg transition-colors duration-300">Phân Phối</button>
                    <button data-tab="marketing" class="strategy-tab text-sm md:text-base font-semibold px-4 py-3 rounded-t-lg transition-colors duration-300">Marketing</button>
                </div>

                <!-- Tab Content -->
                <div id="strategy-content">
                    <!-- Product Content -->
                    <div id="content-product" class="strategy-content-item">
                        <h3 class="font-bold text-xl text-center mb-2 text-[#3A7CA5]">Ma Trận Sản Phẩm 3 Phân Khúc</h3>
                        <p class="text-center text-gray-600 text-sm mb-8">Đáp ứng mọi nhu cầu từ cơ bản đến cao cấp, với triết lý "Thiết kế cho chuyên gia Nhân sự".</p>
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                            <div class="border border-[#EAE7E1] rounded-lg p-6 text-center hover:shadow-xl hover:border-[#D6A25B] transition-all duration-300">
                                <h4 class="font-bold text-lg text-[#3A7CA5]">The Essential</h4>
                                <p class="text-sm font-semibold text-gray-500 mt-1">Phân khúc Cơ bản</p>
                                <p class="text-sm mt-3 text-gray-600">Tập trung vào độ bền, tính năng và chi phí tối ưu. Chất liệu Kate Silk, Lon.</p>
                                <p class="font-bold text-lg text-[#D6A25B] mt-4">180k - 240k</p>
                            </div>
                            <div class="border-2 border-[#3A7CA5] rounded-lg p-6 text-center shadow-2xl transition-all duration-300 scale-105">
                                <span class="text-xs font-bold bg-[#3A7CA5] text-white px-3 py-1 rounded-full absolute -top-3">CHIẾN LƯỢC</span>
                                <h4 class="font-bold text-lg text-[#3A7CA5]">The Professional</h4>
                                <p class="text-sm font-semibold text-gray-500 mt-1">Phân khúc Trung cấp</p>
                                <p class="text-sm mt-3 text-gray-600">Cân bằng giữa phong cách hiện đại và sự thoải mái. Chất liệu Kate Ý/Mỹ, Modal.</p>
                                <p class="font-bold text-lg text-[#D6A25B] mt-4">280k - 550k</p>
                            </div>
                            <div class="border border-[#EAE7E1] rounded-lg p-6 text-center hover:shadow-xl hover:border-[#D6A25B] transition-all duration-300">
                                <h4 class="font-bold text-lg text-[#3A7CA5]">The Leader</h4>
                                <p class="text-sm font-semibold text-gray-500 mt-1">Phân khúc Cao cấp</p>
                                <p class="text-sm mt-3 text-gray-600">Đẳng cấp, bền vững và quyền lực. Chất liệu Bamboo, Vải tái chế.</p>
                                <p class="font-bold text-lg text-[#D6A25B] mt-4">> 600k</p>
                            </div>
                        </div>
                    </div>
                    <!-- Distribution Content -->
                    <div id="content-distribution" class="strategy-content-item hidden">
                        <h3 class="font-bold text-xl text-center mb-2 text-[#3A7CA5]">Mô Hình Phân Phối Đa Điểm Chạm</h3>
                         <p class="text-center text-gray-600 text-sm mb-8">Tiếp cận khách hàng ở mọi nơi họ hiện diện, từ online đến offline, từ cá nhân đến doanh nghiệp.</p>
                         <div class="flex flex-col md:flex-row items-stretch justify-around space-y-8 md:space-y-0 md:space-x-4">
                            <div class="text-center flex-1 flex flex-col items-center">
                                <div class="w-24 h-24 bg-[#EAE7E1] rounded-full flex items-center justify-center mx-auto mb-3 text-[#3A7CA5] text-4xl">🛒</div>
                                <h4 class="font-bold">E-commerce & B2B Sales</h4>
                                <p class="text-sm text-gray-600 mt-2 flex-grow">Website bán lẻ cho dòng Professional & Leader. Đội ngũ sales B2B tiếp cận trực tiếp doanh nghiệp.</p>
                            </div>
                            <div class="text-3xl text-[#D6A25B] font-light flex items-center justify-center transform md:rotate-0 rotate-90">→</div>
                            <div class="text-center flex-1 flex flex-col items-center">
                                <div class="w-24 h-24 bg-[#EAE7E1] rounded-full flex items-center justify-center mx-auto mb-3 text-[#3A7CA5] text-4xl">🏢</div>
                                <h4 class="font-bold">Showroom Trải Nghiệm</h4>
                                <p class="text-sm text-gray-600 mt-2 flex-grow">Không gian vật lý cao cấp tại các thành phố lớn để khách hàng cảm nhận sản phẩm và nhận tư vấn chuyên sâu.</p>
                            </div>
                         </div>
                    </div>
                    <!-- Marketing Content -->
                    <div id="content-marketing" class="strategy-content-item hidden">
                         <h3 class="font-bold text-xl text-center mb-2 text-[#3A7CA5]">Chiến Lược Tiếp Thị "B2C-to-B2B"</h3>
                         <p class="text-center text-gray-600 text-sm mb-8">Xây dựng lòng tin với chuyên gia HR với tư cách người dùng cuối, để họ trở thành đại sứ thương hiệu trong chính doanh nghiệp của mình.</p>
                         <div class="flex flex-col md:flex-row items-center justify-around space-y-8 md:space-y-0 md:space-x-4 p-4 rounded-lg">
                            <div class="text-center">
                                <div class="text-4xl mb-2">①</div>
                                <h4 class="font-semibold">Thu Hút (B2C)</h4>
                                <p class="text-sm text-gray-500">Content marketing giá trị trong cộng đồng HR, quảng cáo nhắm mục tiêu chính xác.</p>
                            </div>
                            <div class="text-3xl text-[#D6A25B] font-light md:mt-8 transform md:rotate-0 rotate-90">→</div>
                            <div class="text-center">
                                <div class="text-4xl mb-2">②</div>
                                <h4 class="font-semibold">Xây Dựng Lòng Tin</h4>
                                <p class="text-sm text-gray-500">Trải nghiệm sản phẩm qua kênh bán lẻ, đánh giá từ những người có ảnh hưởng.</p>
                            </div>
                             <div class="text-3xl text-[#D6A25B] font-light md:mt-8 transform md:rotate-0 rotate-90">→</div>
                            <div class="text-center">
                                 <div class="text-4xl mb-2">③</div>
                                <h4 class="font-semibold">Chuyển Đổi (B2B)</h4>
                                <p class="text-sm text-gray-500">Chuyên gia HR tin tưởng và đề xuất NNS cho hợp đồng đồng phục của công ty.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="text-center mt-8 py-8 border-t border-[#EAE7E1]">
        <p class="text-gray-500 text-sm">Dashboard được tạo dựa trên "Báo cáo Nghiên cứu và Chiến lược Kinh doanh".</p>
        <p class="text-gray-400 text-xs mt-2">© 2025. NNS. Mọi quyền được bảo lưu.</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const palette = {
                accent: '#3A7CA5',
                highlight: '#D6A25B',
                neutralLight: '#EAE7E1',
                neutralDark: '#2F3D40',
                white: '#FFFFFF'
            };

            const wrapLabel = (label, maxLength = 16) => {
                if (typeof label !== 'string' || label.length <= maxLength) return label;
                const words = label.split(' ');
                const lines = [];
                let currentLine = '';
                words.forEach(word => {
                    if ((currentLine + ' ' + word).trim().length > maxLength) {
                        lines.push(currentLine.trim());
                        currentLine = word;
                    } else {
                        currentLine += (currentLine ? ' ' : '') + word;
                    }
                });
                lines.push(currentLine.trim());
                return lines;
            };

            const tooltipTitleCallback = (tooltipItems) => {
                const item = tooltipItems[0];
                let label = item.chart.data.labels[item.dataIndex];
                return Array.isArray(label) ? label.join(' ') : label;
            };

            const defaultChartOptions = {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: {
                        position: 'bottom',
                        labels: {
                            font: { family: "'Be Vietnam Pro', sans-serif" },
                            color: palette.neutralDark
                        }
                    },
                    tooltip: {
                        callbacks: { title: tooltipTitleCallback },
                        titleFont: { family: "'Be Vietnam Pro', sans-serif" },
                        bodyFont: { family: "'Be Vietnam Pro', sans-serif" },
                        backgroundColor: 'rgba(0, 0, 0, 0.8)'
                    }
                },
                scales: {
                    x: { ticks: { font: { family: "'Be Vietnam Pro', sans-serif" }, color: palette.neutralDark }, grid: { display: false } },
                    y: { ticks: { font: { family: "'Be Vietnam Pro', sans-serif" }, color: palette.neutralDark }, grid: { color: '#EAE7E1' } }
                }
            };

            // Chart 1: Sustainable Growth
            new Chart(document.getElementById('sustainableGrowthChart'), {
                type: 'line',
                data: {
                    labels: ['2023', '2025', '2027', '2030'],
                    datasets: [{
                        label: 'Quy mô thị trường (tỷ USD)',
                        data: [7.8, 11.8, 17.8, 33.05],
                        borderColor: palette.accent,
                        backgroundColor: 'rgba(58, 124, 165, 0.1)',
                        fill: true,
                        tension: 0.4,
                        pointBackgroundColor: palette.accent
                    }]
                },
                options: { ...defaultChartOptions, plugins: { ...defaultChartOptions.plugins, legend: { display: false } } }
            });

            // Chart 2: Consumer Attitude
            new Chart(document.getElementById('consumerAttitudeChart'), {
                type: 'doughnut',
                data: {
                    labels: ['Sẵn sàng chi trả thêm', 'Không sẵn sàng'],
                    datasets: [{
                        data: [72, 28],
                        backgroundColor: [palette.accent, palette.neutralLight],
                        borderColor: '#F8F7F4',
                        borderWidth: 4
                    }]
                },
                options: { responsive: true, maintainAspectRatio: true, cutout: '75%', plugins: { legend: { display: false }, tooltip: { enabled: false } } }
            });

            // Chart 3: Competitor Price
            new Chart(document.getElementById('competitorPriceChart'), {
                type: 'bar',
                data: {
                    labels: ['Đồng Phục SG', 'De Charme', 'VIKOR', 'Việt Tiến', 'May 10', 'NNS (Đề xuất)'],
                    datasets: [{
                        label: 'Khoảng giá (VNĐ)',
                        data: [ [150000, 400000], [195000, 480000], [200000, 700000], [260000, 340000], [280000, 550000], [180000, 550000] ],
                        backgroundColor: (context) => context.raw[0] === 180000 ? palette.highlight : palette.accent,
                        borderColor: (context) => context.raw[0] === 180000 ? palette.highlight : palette.accent,
                        borderWidth: 1,
                        borderRadius: 4,
                        borderSkipped: false
                    }]
                },
                options: { ...defaultChartOptions, indexAxis: 'y', plugins: { ...defaultChartOptions.plugins, legend: { display: false }, tooltip: {
                    callbacks: {
                        title: tooltipTitleCallback,
                        label: function(context) {
                            const value = context.raw;
                            const low = new Intl.NumberFormat('vi-VN').format(value[0]);
                            const high = new Intl.NumberFormat('vi-VN').format(value[1]);
                            return `Từ ${low} đến ${high} VNĐ`;
                        }
                    }
                }},
                 scales: {
                    x: { ticks: { callback: (value) => (value / 1000) + 'k' }, title: { display: true, text: 'Khoảng giá (VNĐ)' } },
                    y: { ticks: { font: { size: 10 } } }
                }}
            });

            // Strategy Tabs Logic
            const tabs = document.querySelectorAll('.strategy-tab');
            const contents = document.querySelectorAll('.strategy-content-item');
            tabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    tabs.forEach(item => item.classList.remove('active'));
                    tab.classList.add('active');
                    const target = tab.getAttribute('data-tab');
                    contents.forEach(content => {
                        if (content.id === `content-${target}`) {
                            content.classList.remove('hidden');
                        } else {
                            content.classList.add('hidden');
                        }
                    });
                });
            });

            // Navbar Scroll Logic
            const navbar = document.getElementById('navbar');
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-link');
            window.addEventListener('scroll', () => {
                let current = '';
                sections.forEach(section => {
                    const sectionTop = section.offsetTop;
                    if (pageYOffset >= sectionTop - navbar.clientHeight - 20) {
                        current = section.getAttribute('id');
                    }
                });
                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('href').includes(current)) {
                        link.classList.add('active');
                    }
                });
            });
        });
    </script>
</body>
</html>
