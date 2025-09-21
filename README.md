            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }

        .neural-node {
            position: absolute;
            width: 4px;
            height: 4px;
            background: rgba(0, 255, 255, 0.6);
            border-radius: 50%;
            animation: pulse 2s ease-in-out infinite;
        }

        .neural-connection {
            position: absolute;
            height: 1px;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 255, 0.3), transparent);
            animation: flow 3s linear infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.5); }
        }

        @keyframes flow {
            0% { opacity: 0; transform: translateX(-100%); }
            50% { opacity: 1; }
            100% { opacity: 0; transform: translateX(100%); }
        }

        /* Holographic Effects */
        .holographic {
            background: linear-gradient(45deg, 
                rgba(255, 0, 150, 0.1) 0%,
                rgba(0, 255, 255, 0.1) 25%,
                rgba(255, 255, 0, 0.1) 50%,
                rgba(150, 0, 255, 0.1) 75%,
                rgba(255, 0, 150, 0.1) 100%);
            background-size: 400% 400%;
            animation: hologram 4s ease-in-out infinite;
            backdrop-filter: blur(20px);
            border: 1px solid rgba(0, 255, 255, 0.3);
            box-shadow: 0 0 30px rgba(0, 255, 255, 0.2);
        }

        @keyframes hologram {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        /* Futuristic Cards */
        .ai-card {
            background: rgba(0, 20, 40, 0.8);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(0, 255, 255, 0.2);
            border-radius: 20px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .ai-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 255, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .ai-card:hover::before {
            left: 100%;
        }

        .ai-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 255, 255, 0.3);
            border-color: rgba(0, 255, 255, 0.5);
        }

        /* Neon Text */
        .neon-text {
            color: #00ffff;
            text-shadow: 
                0 0 5px #00ffff,
                0 0 10px #00ffff,
                0 0 15px #00ffff,
                0 0 20px #00ffff;
            animation: neon-flicker 2s ease-in-out infinite alternate;
        }

        @keyframes neon-flicker {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.8; }
        }

        /* AI Status Indicators */
        .ai-status {
            display: inline-block;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            margin-right: 8px;
            animation: status-pulse 1.5s ease-in-out infinite;
        }

        .ai-status.online { background: #00ff00; }
        .ai-status.busy { background: #ffff00; }
        .ai-status.offline { background: #ff0000; }

        @keyframes status-pulse {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.7; transform: scale(1.2); }
        }

        /* Futuristic Buttons */
        .cyber-btn {
            background: linear-gradient(45deg, rgba(0, 255, 255, 0.1), rgba(255, 0, 255, 0.1));
            border: 2px solid rgba(0, 255, 255, 0.5);
            color: #00ffff;
            padding: 12px 24px;
            border-radius: 25px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .cyber-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 255, 0.2), transparent);
            transition: left 0.5s ease;
        }

        .cyber-btn:hover::before {
            left: 100%;
        }

        .cyber-btn:hover {
            box-shadow: 0 0 20px rgba(0, 255, 255, 0.5);
            transform: translateY(-2px);
        }

        /* Data Visualization */
        .data-stream {
            font-family: 'Courier New', monospace;
            color: #00ff00;
            font-size: 12px;
            line-height: 1.2;
            overflow: hidden;
            height: 200px;
            background: rgba(0, 0, 0, 0.8);
            border: 1px solid rgba(0, 255, 0, 0.3);
            border-radius: 10px;
            padding: 10px;
        }

        .data-line {
            opacity: 0;
            animation: data-appear 0.1s ease-in-out forwards;
        }

        @keyframes data-appear {
            from { opacity: 0; transform: translateX(-20px); }
            to { opacity: 1; transform: translateX(0); }
        }

        /* AI Model Cards */
        .model-card {
            background: linear-gradient(135deg, rgba(0, 50, 100, 0.3), rgba(50, 0, 100, 0.3));
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 20px;
            transition: all 0.3s ease;
            position: relative;
        }

        .model-card:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }

        /* Progress Bars */
        .ai-progress {
            width: 100%;
            height: 8px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            overflow: hidden;
            position: relative;
        }

        .ai-progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #00ffff, #ff00ff);
            border-radius: 4px;
            transition: width 1s ease;
            position: relative;
        }

        .ai-progress-fill::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            animation: progress-shine 2s ease-in-out infinite;
        }

        @keyframes progress-shine {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        /* Chat Interface */
        .chat-container {
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(0, 255, 255, 0.3);
            border-radius: 20px;
            height: 400px;
            display: flex;
            flex-direction: column;
        }

        .chat-messages {
            flex: 1;
            overflow-y: auto;
            padding: 20px;
        }

        .chat-message {
            margin-bottom: 15px;
            padding: 10px 15px;
            border-radius: 15px;
            max-width: 80%;
            animation: message-appear 0.3s ease-out;
        }

        .chat-message.user {
            background: linear-gradient(135deg, rgba(0, 255, 255, 0.2), rgba(0, 150, 255, 0.2));
            margin-left: auto;
            text-align: right;
        }

        .chat-message.ai {
            background: linear-gradient(135deg, rgba(255, 0, 255, 0.2), rgba(150, 0, 255, 0.2));
            margin-right: auto;
        }

        @keyframes message-appear {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Responsive Grid */
        .ai-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            padding: 20px;
        }

        /* Scrollbar Styling */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(135deg, #00ffff, #ff00ff);
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(135deg, #00cccc, #cc00cc);
        }

        /* Loading Animation */
        .ai-loading {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid rgba(0, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: #00ffff;
            animation: spin 1s ease-in-out infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* Floating Action Button */
        .fab {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #00ffff, #ff00ff);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 24px;
            cursor: pointer;
            box-shadow: 0 10px 25px rgba(0, 255, 255, 0.3);
            transition: all 0.3s ease;
            z-index: 1000;
        }

        .fab:hover {
            transform: scale(1.1);
            box-shadow: 0 15px 35px rgba(0, 255, 255, 0.5);
        }

        /* Modal Styles */
        .modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(10px);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 2000;
        }

        .modal.show {
            display: flex;
        }

        .modal-content {
            background: linear-gradient(135deg, rgba(0, 20, 40, 0.9), rgba(20, 0, 40, 0.9));
            backdrop-filter: blur(20px);
            border: 1px solid rgba(0, 255, 255, 0.3);
            border-radius: 20px;
            padding: 30px;
            max-width: 90%;
            max-height: 90%;
            overflow-y: auto;
            position: relative;
        }

        /* Tabs */
        .tab-container {
            border-bottom: 1px solid rgba(0, 255, 255, 0.3);
            margin-bottom: 20px;
        }

        .tab-btn {
            background: none;
            border: none;
            color: rgba(255, 255, 255, 0.7);
            padding: 15px 25px;
            cursor: pointer;
            transition: all 0.3s ease;
            border-bottom: 2px solid transparent;
        }

        .tab-btn.active {
            color: #00ffff;
            border-bottom-color: #00ffff;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
            animation: tab-appear 0.3s ease-out;
        }

        @keyframes tab-appear {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Stats Cards */
        .stat-card {
            background: linear-gradient(135deg, rgba(0, 255, 255, 0.1), rgba(255, 0, 255, 0.1));
            border: 1px solid rgba(0, 255, 255, 0.3);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 255, 255, 0.2);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 900;
            color: #00ffff;
            text-shadow: 0 0 10px rgba(0, 255, 255, 0.5);
        }

        /* AI Model Status */
        .model-status {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 10px;
        }

        .model-indicator {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            animation: pulse 2s ease-in-out infinite;
        }

        .model-indicator.active { background: #00ff00; }
        .model-indicator.training { background: #ffff00; }
        .model-indicator.error { background: #ff0000; }

        /* Voice Visualizer */
        .voice-visualizer {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 2px;
            height: 40px;
        }

        .voice-bar {
            width: 4px;
            background: linear-gradient(to top, #00ffff, #ff00ff);
            border-radius: 2px;
            animation: voice-wave 1s ease-in-out infinite;
        }

        .voice-bar:nth-child(1) { animation-delay: 0s; }
        .voice-bar:nth-child(2) { animation-delay: 0.1s; }
        .voice-bar:nth-child(3) { animation-delay: 0.2s; }
        .voice-bar:nth-child(4) { animation-delay: 0.3s; }
        .voice-bar:nth-child(5) { animation-delay: 0.4s; }

        @keyframes voice-wave {
            0%, 100% { height: 10px; }
            50% { height: 30px; }
        }
    </style>
</head>
<body>
    <!-- Neural Network Background -->
    <div class="neural-bg" id="neuralBg"></div>

    <!-- Header -->
    <header class="holographic p-6 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto flex items-center justify-between">
            <div class="flex items-center gap-4">
                <div class="text-5xl">🦊</div>
                <div>
                    <h1 class="text-3xl font-black neon-text">MOZILLA AI UNIVERSE</h1>
                    <p class="text-cyan-300 text-sm">ศูนย์รวม AI เทคโนโลยีขั้นสูงสุด พัฒนาโดยทีม Mozilla</p>
                </div>
            </div>
            <div class="flex items-center gap-4">
                <div class="ai-status online"></div>
                <span class="text-green-400 font-semibold">ระบบออนไลน์</span>
                <button class="cyber-btn" onclick="showAIAssistant()">
                    🦊 Mozilla AI Assistant
                </button>
            </div>
        </div>
    </header>

    <!-- Main Dashboard -->
    <main class="max-w-7xl mx-auto p-6">
        <!-- Stats Overview -->
        <section class="grid grid-cols-1 md:grid-cols-4 gap-6 mb-8">
            <div class="stat-card">
                <div class="stat-number" id="activeModels">247</div>
                <div class="text-cyan-300 font-semibold">โมเดล AI ที่ใช้งานได้</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="totalRequests">1.2M</div>
                <div class="text-cyan-300 font-semibold">คำขอทั้งหมด</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="successRate">99.7%</div>
                <div class="text-cyan-300 font-semibold">อัตราความสำเร็จ</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="responseTime">0.3s</div>
                <div class="text-cyan-300 font-semibold">เวลาตอบสนองเฉลี่ย</div>
            </div>
        </section>

        <!-- AI Categories -->
        <section class="mb-8">
            <h2 class="text-2xl font-bold text-white mb-6 flex items-center gap-3">
                🦊 Mozilla AI Categories ขั้นสูง
            </h2>
            <div class="ai-grid">
                <!-- Language Models -->
                <div class="ai-card p-6">
                    <div class="model-status">
                        <div class="model-indicator active"></div>
                        <h3 class="text-xl font-bold text-cyan-300">🦊 Mozilla Language Models</h3>
                    </div>
                    <p class="text-gray-300 mb-4">โมเดลภาษาขั้นสูง Firefox AI, Llamafile, Open Source LLMs</p>
                    <div class="space-y-3">
                        <div class="flex justify-between items-center">
                            <span class="text-white">🦊 Firefox AI</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 95%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">🔥 Llamafile</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 92%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">🌐 Mozilla Common Voice</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 88%"></div>
                            </div>
                        </div>
                    </div>
                    <button class="cyber-btn w-full mt-4" onclick="openLanguageModels()">
                        เข้าใช้งาน
                    </button>
                </div>

                <!-- Image Generation -->
                <div class="ai-card p-6">
                    <div class="model-status">
                        <div class="model-indicator active"></div>
                        <h3 class="text-xl font-bold text-cyan-300">🎨 Mozilla Image AI</h3>
                    </div>
                    <p class="text-gray-300 mb-4">สร้างภาพด้วย AI แบบ Open Source: Stable Diffusion, Firefox AI Art</p>
                    <div class="space-y-3">
                        <div class="flex justify-between items-center">
                            <span class="text-white">🦊 Firefox AI Art</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 97%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">🔥 Stable Diffusion XL</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 94%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">🌐 Mozilla DeepSpeech</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 91%"></div>
                            </div>
                        </div>
                    </div>
                    <button class="cyber-btn w-full mt-4" onclick="openImageGeneration()">
                        สร้างภาพ
                    </button>
                </div>

                <!-- Voice AI -->
                <div class="ai-card p-6">
                    <div class="model-status">
                        <div class="model-indicator active"></div>
                        <h3 class="text-xl font-bold text-cyan-300">🦊 Mozilla Voice AI</h3>
                    </div>
                    <p class="text-gray-300 mb-4">เสียงพูด, แปลงเสียง, สังเคราะห์เสียง ด้วย Mozilla TTS</p>
                    <div class="voice-visualizer mb-4">
                        <div class="voice-bar"></div>
                        <div class="voice-bar"></div>
                        <div class="voice-bar"></div>
                        <div class="voice-bar"></div>
                        <div class="voice-bar"></div>
                    </div>
                    <div class="space-y-3">
                        <div class="flex justify-between items-center">
                            <span class="text-white">🦊 Mozilla TTS</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 96%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">🔥 Firefox Voice</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 93%"></div>
                            </div>
                        </div>
                    </div>
                    <button class="cyber-btn w-full mt-4" onclick="openVoiceAI()">
                        ใช้งานเสียง
                    </button>
                </div>

                <!-- Video AI -->
                <div class="ai-card p-6">
                    <div class="model-status">
                        <div class="model-indicator training"></div>
                        <h3 class="text-xl font-bold text-cyan-300">🎬 Video AI</h3>
                    </div>
                    <p class="text-gray-300 mb-4">สร้างและแก้ไขวิดีโอด้วย AI</p>
                    <div class="space-y-3">
                        <div class="flex justify-between items-center">
                            <span class="text-white">Runway ML</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 89%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">Pika Labs</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 85%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">Sora (Preview)</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 78%"></div>
                            </div>
                        </div>
                    </div>
                    <button class="cyber-btn w-full mt-4" onclick="openVideoAI()">
                        สร้างวิดีโอ
                    </button>
                </div>

                <!-- Code AI -->
                <div class="ai-card p-6">
                    <div class="model-status">
                        <div class="model-indicator active"></div>
                        <h3 class="text-xl font-bold text-cyan-300">🦊 Mozilla Code AI</h3>
                    </div>
                    <p class="text-gray-300 mb-4">เขียนโค้ด, Debug, Code Review ด้วย Firefox Developer Tools AI</p>
                    <div class="space-y-3">
                        <div class="flex justify-between items-center">
                            <span class="text-white">🦊 Firefox DevTools AI</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 98%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">🔥 Mozilla CodeGen</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 92%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">🌐 Rust AI Assistant</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 87%"></div>
                            </div>
                        </div>
                    </div>
                    <button class="cyber-btn w-full mt-4" onclick="openCodeAI()">
                        เขียนโค้ด
                    </button>
                </div>

                <!-- Data Analysis AI -->
                <div class="ai-card p-6">
                    <div class="model-status">
                        <div class="model-indicator active"></div>
                        <h3 class="text-xl font-bold text-cyan-300">📊 Data Analysis AI</h3>
                    </div>
                    <p class="text-gray-300 mb-4">วิเคราะห์ข้อมูล, Machine Learning</p>
                    <div class="data-stream" id="dataStream">
                        <div class="data-line">Analyzing dataset: customers_2024.csv</div>
                        <div class="data-line">Processing 1,247,832 records...</div>
                        <div class="data-line">Feature extraction: 94% complete</div>
                        <div class="data-line">Model training: Random Forest</div>
                        <div class="data-line">Accuracy: 97.3%</div>
                    </div>
                    <button class="cyber-btn w-full mt-4" onclick="openDataAnalysis()">
                        วิเคราะห์ข้อมูล
                    </button>
                </div>

                <!-- 3D AI -->
                <div class="ai-card p-6">
                    <div class="model-status">
                        <div class="model-indicator training"></div>
                        <h3 class="text-xl font-bold text-cyan-300">🎯 3D AI</h3>
                    </div>
                    <p class="text-gray-300 mb-4">สร้างโมเดล 3D, AR/VR</p>
                    <div class="space-y-3">
                        <div class="flex justify-between items-center">
                            <span class="text-white">NeRF</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 84%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">DreamFusion</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 79%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">Point-E</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 76%"></div>
                            </div>
                        </div>
                    </div>
                    <button class="cyber-btn w-full mt-4" onclick="open3DAI()">
                        สร้าง 3D
                    </button>
                </div>

                <!-- Medical AI -->
                <div class="ai-card p-6">
                    <div class="model-status">
                        <div class="model-indicator active"></div>
                        <h3 class="text-xl font-bold text-cyan-300">🏥 Medical AI</h3>
                    </div>
                    <p class="text-gray-300 mb-4">วินิจฉัยโรค, วิเคราะห์ภาพทางการแพทย์</p>
                    <div class="space-y-3">
                        <div class="flex justify-between items-center">
                            <span class="text-white">Med-PaLM</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 91%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">DeepMind AlphaFold</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 95%"></div>
                            </div>
                        </div>
                        <div class="flex justify-between items-center">
                            <span class="text-white">IBM Watson Health</span>
                            <div class="ai-progress w-24">
                                <div class="ai-progress-fill" style="width: 88%"></div>
                            </div>
                        </div>
                    </div>
                    <button class="cyber-btn w-full mt-4" onclick="openMedicalAI()">
                        วิเคราะห์ทางการแพทย์
                    </button>
                </div>
            </div>
        </section>

        <!-- Real-time AI Monitor -->
        <section class="mb-8">
            <h2 class="text-2xl font-bold text-white mb-6 flex items-center gap-3">
                📡 การตรวจสอบ AI แบบเรียลไทม์
            </h2>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
                <div class="ai-card p-6">
                    <h3 class="text-xl font-bold text-cyan-300 mb-4">🔥 AI Models ที่ใช้งานมากที่สุด</h3>
                    <div class="space-y-4">
                        <div class="flex items-center justify-between">
                            <div class="flex items-center gap-3">
                                <div class="w-4 h-4 bg-gradient-to-r from-cyan-400 to-blue-500 rounded"></div>
                                <span class="text-white">GPT-4 Turbo</span>
                            </div>
                            <span class="text-cyan-300 font-bold">34.2%</span>
                        </div>
                        <div class="flex items-center justify-between">
                            <div class="flex items-center gap-3">
                                <div class="w-4 h-4 bg-gradient-to-r from-purple-400 to-pink-500 rounded"></div>
                                <span class="text-white">DALL-E 3</span>
                            </div>
                            <span class="text-cyan-300 font-bold">28.7%</span>
                        </div>
                        <div class="flex items-center justify-between">
                            <div class="flex items-center gap-3">
                                <div class="w-4 h-4 bg-gradient-to-r from-green-400 to-blue-500 rounded"></div>
                                <span class="text-white">Claude 3</span>
                            </div>
                            <span class="text-cyan-300 font-bold">19.3%</span>
                        </div>
                        <div class="flex items-center justify-between">
                            <div class="flex items-center gap-3">
                                <div class="w-4 h-4 bg-gradient-to-r from-yellow-400 to-orange-500 rounded"></div>
                                <span class="text-white">Whisper</span>
                            </div>
                            <span class="text-cyan-300 font-bold">17.8%</span>
                        </div>
                    </div>
                </div>

                <div class="ai-card p-6">
                    <h3 class="text-xl font-bold text-cyan-300 mb-4">⚡ ประสิทธิภาพระบบ</h3>
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="text-white">CPU Usage</span>
                                <span class="text-cyan-300">67%</span>
                            </div>
                            <div class="ai-progress">
                                <div class="ai-progress-fill" style="width: 67%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="text-white">GPU Usage</span>
                                <span class="text-cyan-300">89%</span>
                            </div>
                            <div class="ai-progress">
                                <div class="ai-progress-fill" style="width: 89%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="text-white">Memory Usage</span>
                                <span class="text-cyan-300">72%</span>
                            </div>
                            <div class="ai-progress">
                                <div class="ai-progress-fill" style="width: 72%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="text-white">Network I/O</span>
                                <span class="text-cyan-300">45%</span>
                            </div>
                            <div class="ai-progress">
                                <div class="ai-progress-fill" style="width: 45%"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Latest AI News -->
        <section class="mb-8">
            <h2 class="text-2xl font-bold text-white mb-6 flex items-center gap-3">
                📰 ข่าวสาร AI ล่าสุด
            </h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="ai-card p-6">
                    <div class="text-sm text-cyan-300 mb-2">2 ชั่วโมงที่แล้ว</div>
                    <h3 class="text-lg font-bold text-white mb-3">OpenAI เปิดตัว GPT-5 Beta</h3>
                    <p class="text-gray-300 text-sm mb-4">โมเดลภาษาใหม่ที่มีความสามารถในการเรียนรู้และตอบสนองที่ดีขึ้น 40%</p>
                    <button class="cyber-btn text-sm">อ่านเพิ่มเติม</button>
                </div>
                <div class="ai-card p-6">
                    <div class="text-sm text-cyan-300 mb-2">5 ชั่วโมงที่แล้ว</div>
                    <h3 class="text-lg font-bold text-white mb-3">Google เปิดตัว Gemini Ultra 2.0</h3>
                    <p class="text-gray-300 text-sm mb-4">ความสามารถในการประมวลผลภาพและข้อความพร้อมกันได้อย่างแม่นยำ</p>
                    <button class="cyber-btn text-sm">อ่านเพิ่มเติม</button>
                </div>
                <div class="ai-card p-6">
                    <div class="text-sm text-cyan-300 mb-2">1 วันที่แล้ว</div>
                    <h3 class="text-lg font-bold text-white mb-3">Meta เปิดตัว Llama 3</h3>
                    <p class="text-gray-300 text-sm mb-4">โมเดล Open Source ที่มีประสิทธิภาพเทียบเท่า GPT-4</p>
                    <button class="cyber-btn text-sm">อ่านเพิ่มเติม</button>
                </div>
            </div>
        </section>
    </main>

    <!-- Floating Action Button -->
    <div class="fab" onclick="showQuickActions()">
        🦊
    </div>

    <!-- AI Assistant Modal -->
    <div id="aiAssistantModal" class="modal">
        <div class="modal-content w-full max-w-4xl">
            <div class="flex justify-between items-center mb-6">
                <h2 class="text-2xl font-bold neon-text">🦊 Mozilla AI Assistant Pro</h2>
                <button onclick="closeModal('aiAssistantModal')" class="text-white text-2xl hover:text-cyan-300">×</button>
            </div>
            
            <div class="tab-container">
                <button class="tab-btn active" onclick="switchTab('chat')">💬 Chat</button>
                <button class="tab-btn" onclick="switchTab('image')">🎨 Image</button>
                <button class="tab-btn" onclick="switchTab('voice')">🎤 Voice</button>
                <button class="tab-btn" onclick="switchTab('code')">💻 Code</button>
                <button class="tab-btn" onclick="switchTab('analysis')">📊 Analysis</button>
            </div>

            <!-- Chat Tab -->
            <div id="chatTab" class="tab-content active">
                <div class="chat-container">
                    <div class="chat-messages" id="chatMessages">
                        <div class="chat-message ai">
                            <strong>Mozilla AI:</strong> สวัสดีครับ! ผมคือ Mozilla AI Assistant พร้อมช่วยเหลือคุณด้วยเทคโนโลยี Open Source 🦊✨
                        </div>
                    </div>
                    <div class="flex gap-3 p-4 border-t border-cyan-300/30">
                        <input type="text" id="chatInput" placeholder="พิมพ์ข้อความของคุณ..." 
                               class="flex-1 bg-transparent border border-cyan-300/50 rounded-lg px-4 py-2 text-white focus:outline-none focus:border-cyan-300">
                        <button onclick="sendMessage()" class="cyber-btn">ส่ง</button>
                    </div>
                </div>
            </div>

            <!-- Image Tab -->
            <div id="imageTab" class="tab-content">
                <div class="space-y-6">
                    <!-- Image Database Search -->
                    <div class="ai-card p-6">
                        <h3 class="text-xl font-bold text-cyan-300 mb-4">🌍 ฐานข้อมูลรูปภาพทั่วโลก</h3>
                        <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                            <div class="lg:col-span-2">
                                <div class="flex gap-3 mb-4">
                                    <input type="text" id="imageSearchQuery" placeholder="ค้นหารูปภาพ เช่น 'sunset mountain lake'" 
                                           class="flex-1 bg-transparent border border-cyan-300/50 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-cyan-300">
                                    <button onclick="searchGlobalImages()" class="cyber-btn">🔍 ค้นหา</button>
                                </div>
                                
                                <div class="grid grid-cols-2 gap-2 mb-4">
                                    <button onclick="searchCategory('nature')" class="cyber-btn text-sm">🌿 ธรรมชาติ</button>
                                    <button onclick="searchCategory('city')" class="cyber-btn text-sm">🏙️ เมือง</button>
                                    <button onclick="searchCategory('people')" class="cyber-btn text-sm">👥 คน</button>
                                    <button onclick="searchCategory('animals')" class="cyber-btn text-sm">🐾 สัตว์</button>
                                    <button onclick="searchCategory('food')" class="cyber-btn text-sm">🍕 อาหาร</button>
                                    <button onclick="searchCategory('technology')" class="cyber-btn text-sm">💻 เทคโนโลยี</button>
                                    <button onclick="searchCategory('art')" class="cyber-btn text-sm">🎨 ศิลปะ</button>
                                    <button onclick="searchCategory('space')" class="cyber-btn text-sm">🚀 อวกาศ</button>
                                </div>
                            </div>
                            
                            <div>
                                <label class="block text-white text-sm mb-2">📊 สถิติฐานข้อมูล</label>
                                <div class="space-y-3 bg-gray-800/50 rounded-lg p-4">
                                    <div class="flex justify-between">
                                        <span class="text-gray-300">รูปภาพทั้งหมด:</span>
                                        <span class="text-cyan-300 font-bold" id="totalImages">2.4B</span>
                                    </div>
                                    <div class="flex justify-between">
                                        <span class="text-gray-300">หมวดหมู่:</span>
                                        <span class="text-cyan-300 font-bold">50,000+</span>
                                    </div>
                                    <div class="flex justify-between">
                                        <span class="text-gray-300">ความละเอียด:</span>
                                        <span class="text-cyan-300 font-bold">4K-8K</span>
                                    </div>
                                    <div class="flex justify-between">
                                        <span class="text-gray-300">อัปเดตล่าสุด:</span>
                                        <span class="text-green-400 font-bold">เรียลไทม์</span>
                                    </div>
                                </div>
                                
                                <div class="mt-4">
                                    <label class="block text-white text-sm mb-2">🎯 ตัวกรอง</label>
                                    <select id="imageFilter" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white mb-2">
                                        <option value="all">ทั้งหมด</option>
                                        <option value="free">ฟรี</option>
                                        <option value="premium">พรีเมียม</option>
                                        <option value="creative-commons">Creative Commons</option>
                                        <option value="public-domain">Public Domain</option>
                                    </select>
                                    
                                    <select id="imageResolution" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                        <option value="all">ทุกความละเอียด</option>
                                        <option value="hd">HD (1280x720)</option>
                                        <option value="fullhd">Full HD (1920x1080)</option>
                                        <option value="4k">4K (3840x2160)</option>
                                        <option value="8k">8K (7680x4320)</option>
                                    </select>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Search Results -->
                    <div id="searchResults" class="hidden">
                        <div class="flex justify-between items-center mb-4">
                            <h3 class="text-xl font-bold text-white">🔍 ผลการค้นหา</h3>
                            <div class="flex gap-2">
                                <button onclick="sortResults('relevance')" class="cyber-btn text-sm">📊 เรียงตามความเกี่ยวข้อง</button>
                                <button onclick="sortResults('date')" class="cyber-btn text-sm">📅 เรียงตามวันที่</button>
                                <button onclick="sortResults('popular')" class="cyber-btn text-sm">🔥 เรียงตามความนิยม</button>
                            </div>
                        </div>
                        <div id="searchGrid" class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-4">
                            <!-- Search results will appear here -->
                        </div>
                        <div class="text-center mt-6">
                            <button onclick="loadMoreResults()" class="cyber-btn">📥 โหลดเพิ่มเติม</button>
                        </div>
                    </div>

                    <!-- Image Collections -->
                    <div class="ai-card p-6">
                        <h3 class="text-xl font-bold text-cyan-300 mb-4">📚 คอลเลกชันยอดนิยม</h3>
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                            <div class="collection-card cursor-pointer" onclick="loadCollection('trending')">
                                <div class="relative overflow-hidden rounded-lg group">
                                    <div class="w-full h-32 bg-gradient-to-br from-purple-500 to-pink-500 flex items-center justify-center">
                                        <div class="text-4xl">🔥</div>
                                    </div>
                                    <div class="absolute inset-0 bg-black/50 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                                        <span class="text-white font-bold">ดูคอลเลกชัน</span>
                                    </div>
                                </div>
                                <div class="mt-2">
                                    <h4 class="text-white font-semibold">🔥 Trending Now</h4>
                                    <p class="text-gray-400 text-sm">รูปภาพยอดนิยมในสัปดาห์นี้</p>
                                    <p class="text-cyan-300 text-xs">2.3M รูป</p>
                                </div>
                            </div>
                            
                            <div class="collection-card cursor-pointer" onclick="loadCollection('nature')">
                                <div class="relative overflow-hidden rounded-lg group">
                                    <div class="w-full h-32 bg-gradient-to-br from-green-500 to-blue-500 flex items-center justify-center">
                                        <div class="text-4xl">🌿</div>
                                    </div>
                                    <div class="absolute inset-0 bg-black/50 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                                        <span class="text-white font-bold">ดูคอลเลกชัน</span>
                                    </div>
                                </div>
                                <div class="mt-2">
                                    <h4 class="text-white font-semibold">🌿 Nature & Wildlife</h4>
                                    <p class="text-gray-400 text-sm">ธรรมชาติและสัตว์โลก</p>
                                    <p class="text-cyan-300 text-xs">890K รูป</p>
                                </div>
                            </div>
                            
                            <div class="collection-card cursor-pointer" onclick="loadCollection('business')">
                                <div class="relative overflow-hidden rounded-lg group">
                                    <div class="w-full h-32 bg-gradient-to-br from-blue-500 to-indigo-500 flex items-center justify-center">
                                        <div class="text-4xl">💼</div>
                                    </div>
                                    <div class="absolute inset-0 bg-black/50 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                                        <span class="text-white font-bold">ดูคอลเลกชัน</span>
                                    </div>
                                </div>
                                <div class="mt-2">
                                    <h4 class="text-white font-semibold">💼 Business & Tech</h4>
                                    <p class="text-gray-400 text-sm">ธุรกิจและเทคโนโลยี</p>
                                    <p class="text-cyan-300 text-xs">1.2M รูป</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- My Image Library -->
                    <div class="ai-card p-6">
                        <div class="flex justify-between items-center mb-4">
                            <h3 class="text-xl font-bold text-cyan-300">📁 ไลบรารี่ของฉัน</h3>
                            <div class="flex gap-2">
                                <button onclick="uploadImages()" class="cyber-btn text-sm">📤 อัปโหลด</button>
                                <button onclick="createFolder()" class="cyber-btn text-sm">📁 สร้างโฟลเดอร์</button>
                                <button onclick="importFromCloud()" class="cyber-btn text-sm">☁️ นำเข้าจากคลาวด์</button>
                            </div>
                        </div>
                        
                        <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-4">
                            <div class="folder-card p-4 border border-cyan-300/30 rounded-lg cursor-pointer hover:bg-cyan-300/10 transition-colors" onclick="openFolder('favorites')">
                                <div class="text-center">
                                    <div class="text-3xl mb-2">⭐</div>
                                    <div class="text-white font-semibold">รูปโปรด</div>
                                    <div class="text-gray-400 text-sm">247 รูป</div>
                                </div>
                            </div>
                            
                            <div class="folder-card p-4 border border-cyan-300/30 rounded-lg cursor-pointer hover:bg-cyan-300/10 transition-colors" onclick="openFolder('recent')">
                                <div class="text-center">
                                    <div class="text-3xl mb-2">🕒</div>
                                    <div class="text-white font-semibold">ล่าสุด</div>
                                    <div class="text-gray-400 text-sm">89 รูป</div>
                                </div>
                            </div>
                            
                            <div class="folder-card p-4 border border-cyan-300/30 rounded-lg cursor-pointer hover:bg-cyan-300/10 transition-colors" onclick="openFolder('ai-generated')">
                                <div class="text-center">
                                    <div class="text-3xl mb-2">🤖</div>
                                    <div class="text-white font-semibold">AI Generated</div>
                                    <div class="text-gray-400 text-sm">156 รูป</div>
                                </div>
                            </div>
                            
                            <div class="folder-card p-4 border border-cyan-300/30 rounded-lg cursor-pointer hover:bg-cyan-300/10 transition-colors" onclick="openFolder('projects')">
                                <div class="text-center">
                                    <div class="text-3xl mb-2">📋</div>
                                    <div class="text-white font-semibold">โปรเจกต์</div>
                                    <div class="text-gray-400 text-sm">34 รูป</div>
                                </div>
                            </div>
                        </div>
                        
                        <div id="libraryGrid" class="grid grid-cols-3 md:grid-cols-6 gap-3">
                            <!-- User's images will appear here -->
                        </div>
                    </div>

                    <!-- Image Editor -->
                    <div class="ai-card p-6">
                        <h3 class="text-xl font-bold text-cyan-300 mb-4">✏️ เครื่องมือแก้ไขรูปภาพ AI</h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <div class="border-2 border-dashed border-cyan-300/50 rounded-lg p-8 text-center mb-4" id="imageDropZone">
                                    <div class="text-6xl mb-4">🖼️</div>
                                    <p class="text-gray-300 mb-4">ลากรูปภาพมาวาง หรือคลิกเพื่อเลือก</p>
                                    <button onclick="selectImageToEdit()" class="cyber-btn">เลือกรูปภาพ</button>
                                    <input type="file" id="imageFileInput" accept="image/*" style="display: none;" onchange="loadImageForEdit(this)">
                                </div>
                                
                                <div id="imagePreview" class="hidden">
                                    <img id="previewImage" class="w-full rounded-lg shadow-lg" alt="Preview">
                                </div>
                            </div>
                            
                            <div>
                                <h4 class="text-white font-semibold mb-3">🎨 เครื่องมือแก้ไข</h4>
                                <div class="space-y-3">
                                    <button onclick="applyFilter('enhance')" class="cyber-btn w-full text-left">✨ ปรับปรุงคุณภาพ AI</button>
                                    <button onclick="applyFilter('upscale')" class="cyber-btn w-full text-left">🔍 ขยายความละเอียด</button>
                                    <button onclick="applyFilter('remove-bg')" class="cyber-btn w-full text-left">🎭 ลบพื้นหลัง</button>
                                    <button onclick="applyFilter('colorize')" class="cyber-btn w-full text-left">🌈 เพิ่มสีให้ภาพขาวดำ</button>
                                    <button onclick="applyFilter('style-transfer')" class="cyber-btn w-full text-left">🎨 เปลี่ยนสไตล์ศิลปะ</button>
                                    <button onclick="applyFilter('face-enhance')" class="cyber-btn w-full text-left">👤 ปรับปรุงใบหน้า</button>
                                    <button onclick="applyFilter('denoise')" class="cyber-btn w-full text-left">🔧 ลดสัญญาณรบกวน</button>
                                    <button onclick="applyFilter('cartoon')" class="cyber-btn w-full text-left">🎭 แปลงเป็นการ์ตูน</button>
                                </div>
                                
                                <div class="mt-6">
                                    <h4 class="text-white font-semibold mb-3">⚙️ การตั้งค่า</h4>
                                    <div class="space-y-3">
                                        <div>
                                            <label class="block text-white text-sm mb-1">ความเข้ม: <span id="intensityValue">50</span>%</label>
                                            <input type="range" id="filterIntensity" min="0" max="100" value="50" 
                                                   class="w-full" oninput="updateIntensity(this.value)">
                                        </div>
                                        
                                        <div>
                                            <label class="block text-white text-sm mb-1">รูปแบบส่งออก:</label>
                                            <select id="outputFormat" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                                <option value="png">PNG (คุณภาพสูง)</option>
                                                <option value="jpg">JPG (ขนาดเล็ก)</option>
                                                <option value="webp">WebP (สมดุล)</option>
                                            </select>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- Advanced Prompt Builder -->
                    <div class="ai-card p-6">
                        <h3 class="text-xl font-bold text-cyan-300 mb-4">🎯 AI Prompt Builder ขั้นสูง</h3>
                        <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
                            <div>
                                <label class="block text-white font-semibold mb-2">📝 คำอธิบายหลัก</label>
                                <textarea id="imagePrompt" placeholder="อธิบายภาพที่คุณต้องการ เช่น 'สาวสวยยืนริมทะเล'" 
                                          class="w-full bg-transparent border border-cyan-300/50 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-cyan-300 h-24"></textarea>
                                
                                <label class="block text-white font-semibold mb-2 mt-4">🚫 สิ่งที่ไม่ต้องการ (Negative Prompt)</label>
                                <textarea id="negativePrompt" placeholder="เช่น 'blurry, low quality, distorted'" 
                                          class="w-full bg-transparent border border-red-300/50 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-red-300 h-20"></textarea>
                            </div>
                            
                            <div class="space-y-4">
                                <div>
                                    <label class="block text-white text-sm mb-2">🎨 สไตล์ศิลปะ</label>
                                    <select id="imageStyle" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                        <option value="photorealistic">📸 Photorealistic</option>
                                        <option value="anime">🎌 Anime/Manga</option>
                                        <option value="digital-art">💻 Digital Art</option>
                                        <option value="oil-painting">🖼️ Oil Painting</option>
                                        <option value="watercolor">🎨 Watercolor</option>
                                        <option value="cyberpunk">🌃 Cyberpunk</option>
                                        <option value="fantasy">🧙‍♂️ Fantasy</option>
                                        <option value="sci-fi">🚀 Sci-Fi</option>
                                        <option value="vintage">📻 Vintage</option>
                                        <option value="minimalist">⚪ Minimalist</option>
                                    </select>
                                </div>
                                
                                <div class="grid grid-cols-2 gap-3">
                                    <div>
                                        <label class="block text-white text-sm mb-2">📐 ขนาดภาพ</label>
                                        <select id="imageSize" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                            <option value="1024x1024">🟦 Square (1024x1024)</option>
                                            <option value="1024x768">📱 Landscape (1024x768)</option>
                                            <option value="768x1024">📱 Portrait (768x1024)</option>
                                            <option value="1536x1024">🖥️ Wide (1536x1024)</option>
                                            <option value="512x512">⚡ Fast (512x512)</option>
                                        </select>
                                    </div>
                                    
                                    <div>
                                        <label class="block text-white text-sm mb-2">⚡ คุณภาพ</label>
                                        <select id="imageQuality" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                            <option value="ultra">💎 Ultra High (50 steps)</option>
                                            <option value="high">🔥 High (30 steps)</option>
                                            <option value="medium">⚡ Medium (20 steps)</option>
                                            <option value="fast">🚀 Fast (10 steps)</option>
                                        </select>
                                    </div>
                                </div>
                                
                                <div>
                                    <label class="block text-white text-sm mb-2">🎛️ Guidance Scale: <span id="guidanceValue">7.5</span></label>
                                    <input type="range" id="guidanceScale" min="1" max="20" value="7.5" step="0.5" 
                                           class="w-full" oninput="updateGuidanceValue(this.value)">
                                    <div class="flex justify-between text-xs text-gray-400 mt-1">
                                        <span>Creative</span>
                                        <span>Balanced</span>
                                        <span>Precise</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Quick Style Buttons -->
                        <div class="mt-6">
                            <label class="block text-white font-semibold mb-3">🎯 Quick Styles</label>
                            <div class="grid grid-cols-2 md:grid-cols-4 gap-2">
                                <button onclick="applyQuickStyle('portrait')" class="cyber-btn text-sm">👤 Portrait</button>
                                <button onclick="applyQuickStyle('landscape')" class="cyber-btn text-sm">🏔️ Landscape</button>
                                <button onclick="applyQuickStyle('abstract')" class="cyber-btn text-sm">🎨 Abstract</button>
                                <button onclick="applyQuickStyle('character')" class="cyber-btn text-sm">🦸 Character</button>
                                <button onclick="applyQuickStyle('architecture')" class="cyber-btn text-sm">🏛️ Architecture</button>
                                <button onclick="applyQuickStyle('nature')" class="cyber-btn text-sm">🌿 Nature</button>
                                <button onclick="applyQuickStyle('vehicle')" class="cyber-btn text-sm">🚗 Vehicle</button>
                                <button onclick="applyQuickStyle('food')" class="cyber-btn text-sm">🍕 Food</button>
                            </div>
                        </div>
                    </div>

                    <!-- AI Model Selection -->
                    <div class="ai-card p-6">
                        <h3 class="text-xl font-bold text-cyan-300 mb-4">🤖 เลือก AI Model</h3>
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                            <div class="model-card cursor-pointer" onclick="selectModel('sdxl')" id="model-sdxl">
                                <div class="model-status">
                                    <div class="model-indicator active"></div>
                                    <h4 class="font-bold text-white">Stable Diffusion XL</h4>
                                </div>
                                <p class="text-gray-300 text-sm">ภาพคุณภาพสูง, รายละเอียดมาก</p>
                                <div class="mt-2">
                                    <div class="text-xs text-cyan-300">⚡ Speed: Fast | 🎯 Quality: Excellent</div>
                                </div>
                            </div>
                            
                            <div class="model-card cursor-pointer" onclick="selectModel('dreamlike')" id="model-dreamlike">
                                <div class="model-status">
                                    <div class="model-indicator active"></div>
                                    <h4 class="font-bold text-white">Dreamlike Photoreal</h4>
                                </div>
                                <p class="text-gray-300 text-sm">เฉพาะภาพสมจริง</p>
                                <div class="mt-2">
                                    <div class="text-xs text-cyan-300">⚡ Speed: Medium | 🎯 Quality: Photorealistic</div>
                                </div>
                            </div>
                            
                            <div class="model-card cursor-pointer" onclick="selectModel('pollinations')" id="model-pollinations">
                                <div class="model-status">
                                    <div class="model-indicator active"></div>
                                    <h4 class="font-bold text-white">Pollinations AI</h4>
                                </div>
                                <p class="text-gray-300 text-sm">รวดเร็ว, หลากหลายสไตล์</p>
                                <div class="mt-2">
                                    <div class="text-xs text-cyan-300">⚡ Speed: Very Fast | 🎯 Quality: Good</div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Generation Controls -->
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <button onclick="generateImage()" class="cyber-btn text-lg py-4">
                            🎨 สร้างภาพด้วย AI
                        </button>
                        <button onclick="generateBatch()" class="cyber-btn text-lg py-4">
                            🔄 สร้างหลายภาพ (4 ภาพ)
                        </button>
                    </div>

                    <!-- Image Result Area -->
                    <div id="imageResult" class="hidden">
                        <div class="border border-cyan-300/30 rounded-lg p-4 text-center">
                            <div class="ai-loading mb-4"></div>
                            <p class="text-cyan-300">กำลังสร้างภาพจาก AI จริง...</p>
                            <p class="text-gray-400 text-sm mt-2">ใช้เวลาประมาณ 10-30 วินาที</p>
                        </div>
                    </div>

                    <!-- Image Gallery -->
                    <div id="imageGallery" class="hidden">
                        <h3 class="text-xl font-bold text-white mb-4">🖼️ ภาพที่สร้างล่าสุด</h3>
                        <div id="galleryGrid" class="grid grid-cols-2 md:grid-cols-3 gap-4">
                            <!-- Generated images will appear here -->
                        </div>
                    </div>
                </div>
            </div>

            <!-- Voice Tab -->
            <div id="voiceTab" class="tab-content">
                <div class="space-y-6">
                    <div class="text-center">
                        <div class="voice-visualizer mb-6"></div>
                        <button id="voiceBtn" onclick="toggleVoiceRecording()" class="cyber-btn text-lg px-8 py-4">
                            🎤 เริ่มบันทึกเสียง
                        </button>
                    </div>
                    <div class="grid grid-cols-2 gap-6">
                        <div>
                            <h3 class="text-white font-semibold mb-3">🗣️ Text to Speech</h3>
                            <textarea id="ttsText" placeholder="พิมพ์ข้อความที่ต้องการให้อ่าน..." 
                                      class="w-full bg-transparent border border-cyan-300/50 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-cyan-300 h-24"></textarea>
                            <div class="mt-3">
                                <select id="voiceType" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                    <option>เสียงหญิงไทย</option>
                                    <option>เสียงชายไทย</option>
                                    <option>เสียงหญิงอังกฤษ</option>
                                    <option>เสียงชายอังกฤษ</option>
                                </select>
                            </div>
                            <button onclick="speakText()" class="cyber-btn w-full mt-3">🔊 อ่านออกเสียง</button>
                        </div>
                        <div>
                            <h3 class="text-white font-semibold mb-3">🎵 Voice Cloning</h3>
                            <div class="border-2 border-dashed border-cyan-300/50 rounded-lg p-6 text-center">
                                <div class="text-4xl mb-2">🎤</div>
                                <p class="text-gray-300 mb-2">อัปโหลดไฟล์เสียงตัวอย่าง</p>
                                <button class="cyber-btn">เลือกไฟล์</button>
                            </div>
                            <button onclick="cloneVoice()" class="cyber-btn w-full mt-3">🎭 โคลนเสียง</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Code Tab -->
            <div id="codeTab" class="tab-content">
                <div class="space-y-6">
                    <div>
                        <label class="block text-white font-semibold mb-2">💻 อธิบายโค้ดที่ต้องการ</label>
                        <textarea id="codePrompt" placeholder="อธิบายโค้ดที่คุณต้องการให้ AI เขียน..." 
                                  class="w-full bg-transparent border border-cyan-300/50 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-cyan-300 h-24"></textarea>
                    </div>
                    <div class="grid grid-cols-3 gap-4">
                        <div>
                            <label class="block text-white text-sm mb-2">ภาษา</label>
                            <select id="codeLanguage" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                <option>Python</option>
                                <option>JavaScript</option>
                                <option>Java</option>
                                <option>C++</option>
                                <option>Go</option>
                                <option>Rust</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-white text-sm mb-2">Framework</label>
                            <select id="codeFramework" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                <option>None</option>
                                <option>React</option>
                                <option>Vue.js</option>
                                <option>Django</option>
                                <option>Flask</option>
                                <option>Express.js</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-white text-sm mb-2">ความซับซ้อน</label>
                            <select id="codeComplexity" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                <option>Beginner</option>
                                <option>Intermediate</option>
                                <option>Advanced</option>
                                <option>Expert</option>
                            </select>
                        </div>
                    </div>
                    <button onclick="generateCode()" class="cyber-btn w-full">⚡ สร้างโค้ด</button>
                    <div id="codeResult" class="hidden">
                        <div class="bg-gray-900 border border-cyan-300/30 rounded-lg p-4">
                            <div class="flex justify-between items-center mb-3">
                                <span class="text-cyan-300 font-semibold">Generated Code:</span>
                                <button onclick="copyCode()" class="cyber-btn text-sm">📋 Copy</button>
                            </div>
                            <pre id="generatedCode" class="text-green-400 text-sm overflow-x-auto"></pre>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Analysis Tab -->
            <div id="analysisTab" class="tab-content">
                <div class="space-y-6">
                    <div>
                        <label class="block text-white font-semibold mb-2">📊 อัปโหลดข้อมูลสำหรับวิเคราะห์</label>
                        <div class="border-2 border-dashed border-cyan-300/50 rounded-lg p-8 text-center">
                            <div class="text-6xl mb-4">📈</div>
                            <p class="text-gray-300 mb-4">ลากไฟล์ CSV, Excel, หรือ JSON มาวาง</p>
                            <button class="cyber-btn">เลือกไฟล์</button>
                        </div>
                    </div>
                    <div class="grid grid-cols-2 gap-6">
                        <div>
                            <label class="block text-white text-sm mb-2">ประเภทการวิเคราะห์</label>
                            <select id="analysisType" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                <option>Descriptive Statistics</option>
                                <option>Correlation Analysis</option>
                                <option>Regression Analysis</option>
                                <option>Classification</option>
                                <option>Clustering</option>
                                <option>Time Series</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-white text-sm mb-2">รูปแบบผลลัพธ์</label>
                            <select id="outputFormat" class="w-full bg-gray-800 border border-cyan-300/50 rounded-lg px-3 py-2 text-white">
                                <option>Interactive Charts</option>
                                <option>Statistical Report</option>
                                <option>Machine Learning Model</option>
                                <option>Predictions</option>
                            </select>
                        </div>
                    </div>
                    <button onclick="analyzeData()" class="cyber-btn w-full">🔍 เริ่มวิเคราะห์</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Quick Actions Modal -->
    <div id="quickActionsModal" class="modal">
        <div class="modal-content">
            <div class="flex justify-between items-center mb-6">
                <h2 class="text-2xl font-bold neon-text">🦊 Mozilla Quick Actions</h2>
                <button onclick="closeModal('quickActionsModal')" class="text-white text-2xl hover:text-cyan-300">×</button>
            </div>
            <div class="grid grid-cols-2 gap-4">
                <button class="cyber-btn p-4 text-left" onclick="quickAction('summarize')">
                    <div class="text-2xl mb-2">📝</div>
                    <div class="font-bold">สรุปข้อความ</div>
                    <div class="text-sm opacity-70">สรุปเอกสารยาวๆ</div>
                </button>
                <button class="cyber-btn p-4 text-left" onclick="quickAction('translate')">
                    <div class="text-2xl mb-2">🌐</div>
                    <div class="font-bold">แปลภาษา</div>
                    <div class="text-sm opacity-70">แปลข้อความทุกภาษา</div>
                </button>
                <button class="cyber-btn p-4 text-left" onclick="quickAction('optimize')">
                    <div class="text-2xl mb-2">⚡</div>
                    <div class="font-bold">ปรับปรุงโค้ด</div>
                    <div class="text-sm opacity-70">ทำให้โค้ดเร็วขึ้น</div>
                </button>
                <button class="cyber-btn p-4 text-left" onclick="quickAction('explain')">
                    <div class="text-2xl mb-2">🧠</div>
                    <div class="font-bold">อธิบายแนวคิด</div>
                    <div class="text-sm opacity-70">อธิบายเรื่องซับซ้อน</div>
                </button>
            </div>
        </div>
    </div>

    <script>
        // Global variables
        let isRecording = false;
        let currentTab = 'chat';

        // Initialize neural network background
        function initNeuralBackground() {
            const neuralBg = document.getElementById('neuralBg');
            
            // Create neural nodes
            for (let i = 0; i < 50; i++) {
                const node = document.createElement('div');
                node.className = 'neural-node';
                node.style.left = Math.random() * 100 + '%';
                node.style.top = Math.random() * 100 + '%';
                node.style.animationDelay = Math.random() * 2 + 's';
                neuralBg.appendChild(node);
            }

            // Create neural connections
            for (let i = 0; i < 30; i++) {
                const connection = document.createElement('div');
                connection.className = 'neural-connection';
                connection.style.left = Math.random() * 100 + '%';
                connection.style.top = Math.random() * 100 + '%';
                connection.style.width = Math.random() * 200 + 100 + 'px';
                connection.style.transform = `rotate(${Math.random() * 360}deg)`;
                connection.style.animationDelay = Math.random() * 3 + 's';
                neuralBg.appendChild(connection);
            }
        }

        // Update stats with animation
        function updateStats() {
            const stats = [
                { id: 'activeModels', target: 247, current: 0 },
                { id: 'totalRequests', target: 1200000, current: 0, suffix: 'M' },
                { id: 'successRate', target: 99.7, current: 0, suffix: '%' },
                { id: 'responseTime', target: 0.3, current: 0, suffix: 's' }
            ];

            stats.forEach(stat => {
                const element = document.getElementById(stat.id);
                const increment = stat.target / 100;
                
                const updateValue = () => {
                    if (stat.current < stat.target) {
                        stat.current += increment;
                        let displayValue = stat.current;
                        
                        if (stat.suffix === 'M') {
                            displayValue = (stat.current / 1000000).toFixed(1) + stat.suffix;
                        } else if (stat.suffix) {
                            displayValue = stat.current.toFixed(1) + stat.suffix;
                        } else {
                            displayValue = Math.floor(stat.current);
                        }
                        
                        element.textContent = displayValue;
                        requestAnimationFrame(updateValue);
                    }
                };
                
                updateValue();
            });
        }

        // Simulate data stream
        function simulateDataStream() {
            const dataStream = document.getElementById('dataStream');
            const messages = [
                'Loading neural network weights...',
                'Initializing GPU clusters...',
                'Processing batch: 1,247 items',
                'Model accuracy: 97.3%',
                'Inference time: 0.23ms',
                'Memory usage: 2.1GB',
                'Training epoch: 45/100',
                'Validation loss: 0.0023',
                'Learning rate: 0.001',
                'Gradient norm: 1.23'
            ];

            let messageIndex = 0;
            setInterval(() => {
                const lines = dataStream.querySelectorAll('.data-line');
                if (lines.length > 10) {
                    lines[0].remove();
                }

                const newLine = document.createElement('div');
                newLine.className = 'data-line';
                newLine.textContent = `> ${messages[messageIndex % messages.length]}`;
                newLine.style.animationDelay = '0s';
                dataStream.appendChild(newLine);

                messageIndex++;
                dataStream.scrollTop = dataStream.scrollHeight;
            }, 2000);
        }

        // Modal functions
        function showAIAssistant() {
            document.getElementById('aiAssistantModal').classList.add('show');
        }

        function showQuickActions() {
            document.getElementById('quickActionsModal').classList.add('show');
        }

        function closeModal(modalId) {
            document.getElementById(modalId).classList.remove('show');
        }

        // Tab switching
        function switchTab(tabName) {
            // Remove active class from all tabs
            document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
            document.querySelectorAll('.tab-content').forEach(content => content.classList.remove('active'));

            // Add active class to selected tab
            event.target.classList.add('active');
            document.getElementById(tabName + 'Tab').classList.add('active');
            currentTab = tabName;
        }

        // Chat functionality
        function sendMessage() {
            const input = document.getElementById('chatInput');
            const messages = document.getElementById('chatMessages');
            const message = input.value.trim();

            if (!message) return;

            // Add user message
            const userMessage = document.createElement('div');
            userMessage.className = 'chat-message user';
            userMessage.innerHTML = `<strong>คุณ:</strong> ${message}`;
            messages.appendChild(userMessage);

            // Clear input
            input.value = '';

            // Simulate AI response
            setTimeout(() => {
                const aiMessage = document.createElement('div');
                aiMessage.className = 'chat-message ai';
                aiMessage.innerHTML = `<strong>AI Assistant:</strong> ${generateAIResponse(message)}`;
                messages.appendChild(aiMessage);
                messages.scrollTop = messages.scrollHeight;
            }, 1000);

            messages.scrollTop = messages.scrollHeight;
        }

        function generateAIResponse(message) {
            const responses = [
                `เข้าใจแล้วครับ! เรื่อง "${message}" นี้น่าสนใจมาก ผมจะช่วยวิเคราะห์และให้คำแนะนำที่ดีที่สุด 🤖`,
                `ขอบคุณสำหรับคำถาม "${message}" ผมกำลังประมวลผลข้อมูลและจะตอบคุณในไม่ช้า ⚡`,
                `เรื่อง "${message}" นี้ผมมีข้อมูลมากมาย ต้องการให้ผมอธิบายในแง่มุมไหนเป็นพิเศษครับ? 🧠`,
                `น่าสนใจมาก! "${message}" เป็นหัวข้อที่ผมชอบ ให้ผมค้นหาข้อมูลล่าสุดให้คุณนะครับ 🔍`
            ];
            return responses[Math.floor(Math.random() * responses.length)];
        }

        // Global variables for image generation
        let selectedModel = 'sdxl';
        let generatedImages = [];

        // Update guidance value display
        function updateGuidanceValue(value) {
            document.getElementById('guidanceValue').textContent = value;
        }

        // Apply quick style presets
        function applyQuickStyle(style) {
            const promptField = document.getElementById('imagePrompt');
            const styleSelect = document.getElementById('imageStyle');
            
            const stylePresets = {
                'portrait': {
                    prompt: 'beautiful portrait of a person, professional photography, studio lighting, high detail',
                    style: 'photorealistic'
                },
                'landscape': {
                    prompt: 'breathtaking landscape, golden hour, dramatic sky, ultra wide shot, cinematic',
                    style: 'photorealistic'
                },
                'abstract': {
                    prompt: 'abstract art, flowing colors, geometric patterns, modern art style',
                    style: 'digital-art'
                },
                'character': {
                    prompt: 'fantasy character design, detailed armor, heroic pose, concept art',
                    style: 'fantasy'
                },
                'architecture': {
                    prompt: 'modern architecture, glass and steel, urban design, architectural photography',
                    style: 'photorealistic'
                },
                'nature': {
                    prompt: 'pristine nature, lush forest, wildlife, natural lighting, peaceful',
                    style: 'photorealistic'
                },
                'vehicle': {
                    prompt: 'futuristic vehicle design, sleek lines, advanced technology, concept car',
                    style: 'sci-fi'
                },
                'food': {
                    prompt: 'gourmet food photography, delicious meal, professional presentation, appetizing',
                    style: 'photorealistic'
                }
            };

            if (stylePresets[style]) {
                promptField.value = stylePresets[style].prompt;
                styleSelect.value = stylePresets[style].style;
                showNotification(`🎯 ใช้ ${style} preset แล้ว!`, 'success');
            }
        }

        // Select AI model
        function selectModel(model) {
            selectedModel = model;
            
            // Remove selection from all models
            document.querySelectorAll('[id^="model-"]').forEach(card => {
                card.classList.remove('border-cyan-300');
                card.classList.add('border-transparent');
            });
            
            // Highlight selected model
            const selectedCard = document.getElementById(`model-${model}`);
            selectedCard.classList.remove('border-transparent');
            selectedCard.classList.add('border-cyan-300');
            
            const modelNames = {
                'sdxl': 'Stable Diffusion XL',
                'dreamlike': 'Dreamlike Photoreal',
                'pollinations': 'Pollinations AI'
            };
            
            showNotification(`🤖 เลือก ${modelNames[model]} แล้ว!`, 'success');
        }

        // Enhanced AI Image Generation with Multiple APIs
        async function generateImage() {
            const prompt = document.getElementById('imagePrompt').value;
            const negativePrompt = document.getElementById('negativePrompt').value;
            const style = document.getElementById('imageStyle').value;
            const size = document.getElementById('imageSize').value;
            const quality = document.getElementById('imageQuality').value;
            const guidance = document.getElementById('guidanceScale').value;
            const result = document.getElementById('imageResult');
            
            if (!prompt.trim()) {
                showNotification('❌ กรุณาใส่คำอธิบายภาพ', 'error');
                return;
            }

            result.classList.remove('hidden');
            result.innerHTML = `
                <div class="border border-cyan-300/30 rounded-lg p-6 text-center">
                    <div class="ai-loading mb-4"></div>
                    <p class="text-cyan-300 font-semibold">🎨 กำลังสร้างภาพด้วย AI จริง...</p>
                    <p class="text-gray-400 text-sm mt-2">Model: ${getModelName(selectedModel)}</p>
                    <p class="text-gray-400 text-sm">ใช้เวลาประมาณ 10-30 วินาที</p>
                    <div class="mt-4 bg-gray-800/50 rounded-lg p-3">
                        <div class="text-xs text-left">
                            <div class="text-cyan-300">📝 Prompt: ${prompt}</div>
                            ${negativePrompt ? `<div class="text-red-300 mt-1">🚫 Negative: ${negativePrompt}</div>` : ''}
                            <div class="text-gray-400 mt-1">🎨 Style: ${style} | 📐 Size: ${size} | ⚡ Quality: ${quality}</div>
                        </div>
                    </div>
                </div>
            `;

            try {
                // Enhanced prompt based on style
                let enhancedPrompt = buildEnhancedPrompt(prompt, style, quality);
                let finalNegativePrompt = buildNegativePrompt(negativePrompt, style);

                // Get quality settings
                const qualitySettings = getQualitySettings(quality);
                
                // Try selected model first, then fallbacks
                const apis = getAPIList(selectedModel);
                let imageGenerated = false;
                
                for (const api of apis) {
                    try {
                        showNotification(`🔄 กำลังลอง ${api.name}...`, 'info');
                        
                        if (api.type === 'huggingface') {
                            const response = await fetch(api.url, {
                                method: 'POST',
                                headers: api.headers,
                                body: JSON.stringify({
                                    inputs: enhancedPrompt,
                                    parameters: {
                                        negative_prompt: finalNegativePrompt,
                                        num_inference_steps: qualitySettings.steps,
                                        guidance_scale: parseFloat(guidance),
                                        width: parseInt(size.split('x')[0]),
                                        height: parseInt(size.split('x')[1]),
                                        seed: Math.floor(Math.random() * 1000000)
                                    }
                                })
                            });

                            if (response.ok) {
                                const blob = await response.blob();
                                const imageUrl = URL.createObjectURL(blob);
                                displayGeneratedImage(imageUrl, prompt, api.name, style, size);
                                addToGallery(imageUrl, prompt, api.name);
                                showNotification(`🎨 สร้างภาพสำเร็จด้วย ${api.name}!`, 'success');
                                imageGenerated = true;
                                break;
                            }
                        } else if (api.type === 'pollinations') {
                            const pollinationsUrl = `${api.url}/${encodeURIComponent(enhancedPrompt)}?width=${size.split('x')[0]}&height=${size.split('x')[1]}&seed=${Math.floor(Math.random() * 1000000)}&model=${api.model || 'flux'}`;
                            
                            // Test if image loads
                            const testImg = new Image();
                            testImg.onload = function() {
                                displayGeneratedImage(pollinationsUrl, prompt, api.name, style, size);
                                addToGallery(pollinationsUrl, prompt, api.name);
                                showNotification(`🎨 สร้างภาพสำเร็จด้วย ${api.name}!`, 'success');
                            };
                            
                            testImg.onerror = function() {
                                throw new Error('Pollinations failed');
                            };
                            
                            testImg.src = pollinationsUrl;
                            imageGenerated = true;
                            break;
                        }
                    } catch (error) {
                        console.log(`${api.name} failed:`, error);
                        continue;
                    }
                }

                if (!imageGenerated) {
                    showErrorResult();
                }

            } catch (error) {
                console.error('Image generation error:', error);
                showErrorResult(error.message);
            }
        }

        // Generate multiple images (batch)
        async function generateBatch() {
            showNotification('🔄 กำลังสร้าง 4 ภาพ...', 'info');
            
            for (let i = 0; i < 4; i++) {
                setTimeout(() => {
                    generateImage();
                }, i * 2000); // Stagger requests by 2 seconds
            }
        }

        // Helper functions
        function getModelName(model) {
            const names = {
                'sdxl': 'Stable Diffusion XL',
                'dreamlike': 'Dreamlike Photoreal',
                'pollinations': 'Pollinations AI'
            };
            return names[model] || 'Unknown';
        }

        function buildEnhancedPrompt(prompt, style, quality) {
            let enhanced = prompt;
            
            // Add style-specific enhancements
            const styleEnhancements = {
                'photorealistic': 'photorealistic, high quality, detailed, professional photography, 8k resolution',
                'anime': 'anime style, manga, detailed, vibrant colors, studio quality',
                'digital-art': 'digital art, concept art, detailed, artstation quality, trending',
                'oil-painting': 'oil painting, classical art style, masterpiece, fine art',
                'watercolor': 'watercolor painting, soft colors, artistic, traditional media',
                'cyberpunk': 'cyberpunk style, neon lights, futuristic, dark atmosphere, sci-fi',
                'fantasy': 'fantasy art, magical, epic, detailed, concept art style',
                'sci-fi': 'science fiction, futuristic, advanced technology, concept art',
                'vintage': 'vintage style, retro, classic, nostalgic atmosphere',
                'minimalist': 'minimalist style, clean, simple, modern design'
            };

            if (styleEnhancements[style]) {
                enhanced = `${enhanced}, ${styleEnhancements[style]}`;
            }

            // Add quality enhancements
            if (quality === 'ultra') {
                enhanced += ', masterpiece, best quality, ultra detailed, 8k, professional';
            } else if (quality === 'high') {
                enhanced += ', high quality, detailed, professional';
            }

            return enhanced;
        }

        function buildNegativePrompt(userNegative, style) {
            let negative = userNegative || '';
            
            // Add common negative prompts
            const commonNegatives = 'blurry, low quality, distorted, deformed, ugly, bad anatomy, bad proportions, extra limbs, cloned face, malformed, gross proportions, missing arms, missing legs, extra arms, extra legs, mutated hands, poorly drawn hands, poorly drawn face, mutation, deformed, bad hands, three hands, fused fingers, too many fingers, disconnected limbs, malformed hands, long neck, long body, imperfect, bad composition, inaccurate eyes, extra digit, fewer digits, cropped';
            
            if (negative) {
                negative += ', ' + commonNegatives;
            } else {
                negative = commonNegatives;
            }

            return negative;
        }

        function getQualitySettings(quality) {
            const settings = {
                'ultra': { steps: 50 },
                'high': { steps: 30 },
                'medium': { steps: 20 },
                'fast': { steps: 10 }
            };
            return settings[quality] || settings['medium'];
        }

        function getAPIList(preferredModel) {
            const apis = {
                'sdxl': [
                    {
                        name: 'Stable Diffusion XL',
                        type: 'huggingface',
                        url: 'https://api-inference.huggingface.co/models/stabilityai/stable-diffusion-xl-base-1.0',
                        headers: {
                            'Authorization': 'Bearer hf_demo',
                            'Content-Type': 'application/json'
                        }
                    }
                ],
                'dreamlike': [
                    {
                        name: 'Dreamlike Photoreal',
                        type: 'huggingface',
                        url: 'https://api-inference.huggingface.co/models/dreamlike-art/dreamlike-photoreal-2.0',
                        headers: {
                            'Authorization': 'Bearer hf_demo',
                            'Content-Type': 'application/json'
                        }
                    }
                ],
                'pollinations': [
                    {
                        name: 'Pollinations AI',
                        type: 'pollinations',
                        url: 'https://image.pollinations.ai/prompt',
                        model: 'flux'
                    }
                ]
            };

            // Return preferred model first, then others as fallback
            let result = apis[preferredModel] || [];
            
            // Add other models as fallbacks
            Object.keys(apis).forEach(key => {
                if (key !== preferredModel) {
                    result = result.concat(apis[key]);
                }
            });

            return result;
        }

        function displayGeneratedImage(imageUrl, prompt, modelName, style, size) {
            const result = document.getElementById('imageResult');
            const timestamp = new Date().toLocaleString('th-TH');
            
            result.innerHTML = `
                <div class="border border-cyan-300/30 rounded-lg p-4 bg-gradient-to-br from-gray-900/50 to-gray-800/50">
                    <div class="relative group">
                        <img src="${imageUrl}" alt="Generated AI Image" class="w-full rounded-lg shadow-2xl transition-transform duration-300 group-hover:scale-105">
                        <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-colors duration-300 rounded-lg"></div>
                    </div>
                    
                    <div class="mt-4 p-4 bg-gray-800/70 rounded-lg backdrop-blur-sm">
                        <div class="flex items-center gap-2 mb-2">
                            <div class="w-2 h-2 bg-green-400 rounded-full animate-pulse"></div>
                            <p class="text-cyan-300 font-semibold">✨ สร้างสำเร็จด้วย ${modelName}</p>
                        </div>
                        <p class="text-gray-300 text-sm mb-1"><strong>Prompt:</strong> "${prompt}"</p>
                        <p class="text-gray-400 text-xs mb-2">🎨 Style: ${style} | 📐 Size: ${size} | ⏰ ${timestamp}</p>
                        
                        <div class="flex gap-2 mt-4">
                            <button onclick="downloadImage('${imageUrl}', '${prompt}')" class="cyber-btn flex-1 text-sm">
                                💾 ดาวน์โหลด
                            </button>
                            <button onclick="generateVariation('${prompt}')" class="cyber-btn flex-1 text-sm">
                                🎲 สร้างแบบใหม่
                            </button>
                            <button onclick="shareImage('${imageUrl}')" class="cyber-btn flex-1 text-sm">
                                📤 แชร์
                            </button>
                            <button onclick="enhanceImage('${imageUrl}')" class="cyber-btn flex-1 text-sm">
                                ✨ ปรับปรุง
                            </button>
                        </div>
                    </div>
                </div>
            `;
        }

        function addToGallery(imageUrl, prompt, modelName) {
            const gallery = document.getElementById('imageGallery');
            const grid = document.getElementById('galleryGrid');
            
            gallery.classList.remove('hidden');
            
            const imageCard = document.createElement('div');
            imageCard.className = 'ai-card p-3 cursor-pointer hover:scale-105 transition-transform duration-300';
            imageCard.innerHTML = `
                <img src="${imageUrl}" alt="Generated Image" class="w-full h-32 object-cover rounded-lg mb-2">
                <p class="text-white text-xs font-semibold truncate">${prompt}</p>
                <p class="text-cyan-300 text-xs">${modelName}</p>
            `;
            
            imageCard.onclick = () => {
                // Show full image in modal
                showImageModal(imageUrl, prompt, modelName);
            };
            
            grid.insertBefore(imageCard, grid.firstChild);
            
            // Keep only last 12 images
            while (grid.children.length > 12) {
                grid.removeChild(grid.lastChild);
            }
        }

        function showErrorResult(errorMessage = '') {
            const result = document.getElementById('imageResult');
            result.innerHTML = `
                <div class="border border-red-500/30 rounded-lg p-6 text-center bg-red-900/20">
                    <div class="text-6xl mb-4">⚠️</div>
                    <p class="text-red-400 font-semibold mb-2">ไม่สามารถเชื่อมต่อ AI ได้ในขณะนี้</p>
                    <p class="text-gray-400 text-sm mb-4">
                        ${errorMessage || 'กรุณาลองใหม่อีกครั้ง หรือเปลี่ยน prompt'}
                    </p>
                    <div class="space-y-2">
                        <button onclick="generateImage()" class="cyber-btn w-full">🔄 ลองใหม่</button>
                        <button onclick="tryDifferentPrompt()" class="cyber-btn w-full">✏️ เปลี่ยน Prompt</button>
                        <button onclick="selectModel('pollinations')" class="cyber-btn w-full">🤖 ลองโมเดลอื่น</button>
                    </div>
                </div>
            `;
            showNotification('❌ ไม่สามารถสร้างภาพได้ กรุณาลองใหม่', 'error');
        }

        // Global Image Database Functions
        let currentSearchResults = [];
        let searchOffset = 0;
        let currentQuery = '';

        // Search global image database
        async function searchGlobalImages() {
            const query = document.getElementById('imageSearchQuery').value.trim();
            const filter = document.getElementById('imageFilter').value;
            const resolution = document.getElementById('imageResolution').value;
            
            if (!query) {
                showNotification('❌ กรุณาใส่คำค้นหา', 'error');
                return;
            }

            currentQuery = query;
            searchOffset = 0;
            
            showNotification('🔍 กำลังค้นหาในฐานข้อมูลโลก...', 'info');
            
            try {
                // Simulate search with multiple image sources
                const results = await performGlobalSearch(query, filter, resolution);
                displaySearchResults(results);
                showNotification(`✅ พบ ${results.length.toLocaleString()} รูปภาพ!`, 'success');
            } catch (error) {
                showNotification('❌ เกิดข้อผิดพลาดในการค้นหา', 'error');
            }
        }

        // Search by category
        function searchCategory(category) {
            document.getElementById('imageSearchQuery').value = getCategoryQuery(category);
            searchGlobalImages();
        }

        function getCategoryQuery(category) {
            const queries = {
                'nature': 'beautiful nature landscape forest mountain lake',
                'city': 'modern city skyline urban architecture',
                'people': 'people portrait lifestyle photography',
                'animals': 'wildlife animals cute pets',
                'food': 'delicious food gourmet cooking',
                'technology': 'modern technology gadgets innovation',
                'art': 'beautiful art painting creative design',
                'space': 'space astronomy galaxy stars planets'
            };
            return queries[category] || category;
        }

        // Perform global search across multiple APIs
        async function performGlobalSearch(query, filter, resolution) {
            const results = [];
            
            // Simulate multiple image sources
            const sources = [
                { name: 'Unsplash', baseUrl: 'https://source.unsplash.com', count: 30 },
                { name: 'Pixabay', baseUrl: 'https://pixabay.com/api/', count: 25 },
                { name: 'Pexels', baseUrl: 'https://api.pexels.com/v1/', count: 20 },
                { name: 'Lorem Picsum', baseUrl: 'https://picsum.photos', count: 15 }
            ];

            // Generate sample results
            for (let i = 0; i < 60; i++) {
                const source = sources[i % sources.length];
                const width = resolution === '4k' ? 3840 : resolution === 'fullhd' ? 1920 : 1280;
                const height = resolution === '4k' ? 2160 : resolution === 'fullhd' ? 1080 : 720;
                
                let imageUrl;
                if (source.name === 'Unsplash') {
                    imageUrl = `${source.baseUrl}/${width}x${height}/?${encodeURIComponent(query)}&${i}`;
                } else if (source.name === 'Lorem Picsum') {
                    imageUrl = `${source.baseUrl}/${width}/${height}?random=${i}`;
                } else {
                    // Fallback to placeholder
                    imageUrl = `https://via.placeholder.com/${width}x${height}/4A90E2/FFFFFF?text=${encodeURIComponent(query)}`;
                }

                results.push({
                    id: `img_${i}`,
                    url: imageUrl,
                    thumbnail: imageUrl,
                    title: `${query} ${i + 1}`,
                    source: source.name,
                    width: width,
                    height: height,
                    license: filter === 'free' ? 'Free' : filter === 'premium' ? 'Premium' : 'CC0',
                    tags: query.split(' '),
                    downloads: Math.floor(Math.random() * 10000),
                    likes: Math.floor(Math.random() * 1000)
                });
            }

            currentSearchResults = results;
            return results;
        }

        // Display search results
        function displaySearchResults(results) {
            const searchResults = document.getElementById('searchResults');
            const searchGrid = document.getElementById('searchGrid');
            
            searchResults.classList.remove('hidden');
            searchGrid.innerHTML = '';

            results.forEach((image, index) => {
                const imageCard = document.createElement('div');
                imageCard.className = 'relative group cursor-pointer overflow-hidden rounded-lg bg-gray-800 hover:scale-105 transition-transform duration-300';
                
                imageCard.innerHTML = `
                    <div class="aspect-square">
                        <img src="${image.thumbnail}" alt="${image.title}" 
                             class="w-full h-full object-cover" 
                             onerror="this.src='https://via.placeholder.com/300x300/4A90E2/FFFFFF?text=Image'">
                    </div>
                    
                    <div class="absolute inset-0 bg-black/0 group-hover:bg-black/60 transition-colors duration-300 flex items-center justify-center opacity-0 group-hover:opacity-100">
                        <div class="text-center space-y-2">
                            <button onclick="previewImage('${image.url}', '${image.title}', '${image.source}')" 
                                    class="cyber-btn text-xs px-3 py-1">👁️ ดู</button>
                            <button onclick="downloadGlobalImage('${image.url}', '${image.title}')" 
                                    class="cyber-btn text-xs px-3 py-1">💾 ดาวน์โหลด</button>
                            <button onclick="addToFavorites('${image.id}')" 
                                    class="cyber-btn text-xs px-3 py-1">⭐ โปรด</button>
                        </div>
                    </div>
                    
                    <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/80 to-transparent p-2">
                        <div class="text-white text-xs font-semibold truncate">${image.title}</div>
                        <div class="flex justify-between items-center mt-1">
                            <span class="text-cyan-300 text-xs">${image.source}</span>
                            <div class="flex items-center gap-1 text-xs text-gray-300">
                                <span>❤️ ${image.likes}</span>
                                <span>📥 ${image.downloads}</span>
                            </div>
                        </div>
                    </div>
                `;
                
                searchGrid.appendChild(imageCard);
            });
        }

        // Sort search results
        function sortResults(sortBy) {
            if (currentSearchResults.length === 0) return;
            
            let sorted = [...currentSearchResults];
            
            switch (sortBy) {
                case 'relevance':
                    // Already sorted by relevance
                    break;
                case 'date':
                    sorted.sort((a, b) => b.id.localeCompare(a.id));
                    break;
                case 'popular':
                    sorted.sort((a, b) => b.likes - a.likes);
                    break;
            }
            
            displaySearchResults(sorted);
            showNotification(`📊 เรียงตาม${sortBy === 'relevance' ? 'ความเกี่ยวข้อง' : sortBy === 'date' ? 'วันที่' : 'ความนิยม'}`, 'info');
        }

        // Load more results
        function loadMoreResults() {
            showNotification('📥 กำลังโหลดรูปภาพเพิ่มเติม...', 'info');
            
            setTimeout(() => {
                searchOffset += 60;
                performGlobalSearch(currentQuery, 'all', 'all').then(newResults => {
                    const searchGrid = document.getElementById('searchGrid');
                    
                    newResults.forEach((image, index) => {
                        const imageCard = document.createElement('div');
                        imageCard.className = 'relative group cursor-pointer overflow-hidden rounded-lg bg-gray-800 hover:scale-105 transition-transform duration-300';
                        imageCard.innerHTML = `
                            <div class="aspect-square">
                                <img src="${image.thumbnail}" alt="${image.title}" 
                                     class="w-full h-full object-cover" 
                                     onerror="this.src='https://via.placeholder.com/300x300/4A90E2/FFFFFF?text=Image'">
                            </div>
                            <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/80 to-transparent p-2">
                                <div class="text-white text-xs font-semibold truncate">${image.title}</div>
                                <span class="text-cyan-300 text-xs">${image.source}</span>
                            </div>
                        `;
                        searchGrid.appendChild(imageCard);
                    });
                    
                    showNotification('✅ โหลดรูปภาพเพิ่มเติมแล้ว!', 'success');
                });
            }, 1000);
        }

        // Load collection
        function loadCollection(collectionType) {
            const collections = {
                'trending': 'trending popular viral',
                'nature': 'nature landscape wildlife forest',
                'business': 'business office technology professional'
            };
            
            document.getElementById('imageSearchQuery').value = collections[collectionType];
            searchGlobalImages();
        }

        // Preview image in modal
        function previewImage(imageUrl, title, source) {
            const modal = document.createElement('div');
            modal.className = 'modal show';
            modal.innerHTML = `
                <div class="modal-content max-w-6xl">
                    <div class="flex justify-between items-center mb-4">
                        <div>
                            <h3 class="text-xl font-bold text-cyan-300">${title}</h3>
                            <p class="text-gray-400">แหล่งที่มา: ${source}</p>
                        </div>
                        <button onclick="this.closest('.modal').remove()" class="text-white text-2xl hover:text-cyan-300">×</button>
                    </div>
                    
                    <div class="text-center mb-4">
                        <img src="${imageUrl}" alt="${title}" class="max-w-full max-h-96 rounded-lg shadow-2xl mx-auto">
                    </div>
                    
                    <div class="flex gap-3 justify-center">
                        <button onclick="downloadGlobalImage('${imageUrl}', '${title}')" class="cyber-btn">💾 ดาวน์โหลด</button>
                        <button onclick="useAsPromptReference('${title}')" class="cyber-btn">🎨 ใช้เป็น Reference</button>
                        <button onclick="addToLibrary('${imageUrl}', '${title}')" class="cyber-btn">📁 เพิ่มในไลบรารี่</button>
                        <button onclick="shareGlobalImage('${imageUrl}', '${title}')" class="cyber-btn">📤 แชร์</button>
                    </div>
                </div>
            `;
            
            document.body.appendChild(modal);
        }

        // Download global image
        async function downloadGlobalImage(imageUrl, title) {
            try {
                showNotification('💾 กำลังดาวน์โหลด...', 'info');
                
                const response = await fetch(imageUrl);
                const blob = await response.blob();
                const url = window.URL.createObjectURL(blob);
                const a = document.createElement('a');
                a.href = url;
                a.download = `${title.replace(/[^a-zA-Z0-9]/g, '-')}.jpg`;
                document.body.appendChild(a);
                a.click();
                document.body.removeChild(a);
                window.URL.revokeObjectURL(url);
                
                showNotification('✅ ดาวน์โหลดสำเร็จ!', 'success');
            } catch (error) {
                showNotification('❌ ไม่สามารถดาวน์โหลดได้', 'error');
            }
        }

        // Add to favorites
        function addToFavorites(imageId) {
            showNotification('⭐ เพิ่มในรายการโปรดแล้ว!', 'success');
        }

        // Use as prompt reference
        function useAsPromptReference(title) {
            document.getElementById('imagePrompt').value = `inspired by: ${title}`;
            showNotification('🎨 ใช้เป็น Reference สำหรับ AI แล้ว!', 'success');
            
            // Close modal and switch to AI generation
            document.querySelectorAll('.modal').forEach(modal => modal.remove());
        }

        // Add to library
        function addToLibrary(imageUrl, title) {
            showNotification('📁 เพิ่มในไลบรารี่แล้ว!', 'success');
        }

        // Share global image
        function shareGlobalImage(imageUrl, title) {
            if (navigator.share) {
                navigator.share({
                    title: title,
                    text: `ดูรูปภาพนี้: ${title}`,
                    url: imageUrl
                });
            } else {
                navigator.clipboard.writeText(imageUrl);
                showNotification('📋 คัดลอก URL แล้ว!', 'success');
            }
        }

        // Library Management Functions
        function uploadImages() {
            const input = document.createElement('input');
            input.type = 'file';
            input.multiple = true;
            input.accept = 'image/*';
            input.onchange = function(e) {
                const files = Array.from(e.target.files);
                showNotification(`📤 กำลังอัปโหลด ${files.length} ไฟล์...`, 'info');
                
                setTimeout(() => {
                    showNotification('✅ อัปโหลดสำเร็จ!', 'success');
                    loadLibraryImages();
                }, 2000);
            };
            input.click();
        }

        function createFolder() {
            const folderName = prompt('ชื่อโฟลเดอร์ใหม่:');
            if (folderName) {
                showNotification(`📁 สร้างโฟลเดอร์ "${folderName}" แล้ว!`, 'success');
            }
        }

        function importFromCloud() {
            showNotification('☁️ กำลังเชื่อมต่อกับคลาวด์...', 'info');
            
            setTimeout(() => {
                showNotification('✅ นำเข้าจากคลาวด์สำเร็จ!', 'success');
            }, 3000);
        }

        function openFolder(folderType) {
            showNotification(`📁 เปิดโฟลเดอร์ ${folderType}...`, 'info');
            loadLibraryImages(folderType);
        }

        function loadLibraryImages(folderType = 'all') {
            const libraryGrid = document.getElementById('libraryGrid');
            libraryGrid.innerHTML = '';
            
            // Generate sample library images
            for (let i = 0; i < 12; i++) {
                const imageCard = document.createElement('div');
                imageCard.className = 'relative group cursor-pointer overflow-hidden rounded-lg bg-gray-800 hover:scale-105 transition-transform duration-300';
                
                const imageUrl = `https://picsum.photos/200/200?random=${i + 100}`;
                
                imageCard.innerHTML = `
                    <div class="aspect-square">
                        <img src="${imageUrl}" alt="Library Image ${i + 1}" 
                             class="w-full h-full object-cover">
                    </div>
                    
                    <div class="absolute inset-0 bg-black/0 group-hover:bg-black/60 transition-colors duration-300 flex items-center justify-center opacity-0 group-hover:opacity-100">
                        <div class="text-center space-y-1">
                            <button onclick="editLibraryImage('${imageUrl}')" class="cyber-btn text-xs px-2 py-1">✏️ แก้ไข</button>
                            <button onclick="deleteLibraryImage(${i})" class="cyber-btn text-xs px-2 py-1">🗑️ ลบ</button>
                        </div>
                    </div>
                `;
                
                libraryGrid.appendChild(imageCard);
            }
        }

        function editLibraryImage(imageUrl) {
            document.getElementById('previewImage').src = imageUrl;
            document.getElementById('imagePreview').classList.remove('hidden');
            showNotification('✏️ เปิดเครื่องมือแก้ไขแล้ว!', 'success');
        }

        function deleteLibraryImage(index) {
            if (confirm('ต้องการลบรูปภาพนี้หรือไม่?')) {
                showNotification('🗑️ ลบรูปภาพแล้ว!', 'success');
                loadLibraryImages();
            }
        }

        // Image Editor Functions
        function selectImageToEdit() {
            document.getElementById('imageFileInput').click();
        }

        function loadImageForEdit(input) {
            if (input.files && input.files[0]) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    document.getElementById('previewImage').src = e.target.result;
                    document.getElementById('imagePreview').classList.remove('hidden');
                    showNotification('✅ โหลดรูปภาพสำเร็จ!', 'success');
                };
                reader.readAsDataURL(input.files[0]);
            }
        }

        function applyFilter(filterType) {
            const filterNames = {
                'enhance': 'ปรับปรุงคุณภาพ AI',
                'upscale': 'ขยายความละเอียด',
                'remove-bg': 'ลบพื้นหลัง',
                'colorize': 'เพิ่มสีให้ภาพขาวดำ',
                'style-transfer': 'เปลี่ยนสไตล์ศิลปะ',
                'face-enhance': 'ปรับปรุงใบหน้า',
                'denoise': 'ลดสัญญาณรบกวน',
                'cartoon': 'แปลงเป็นการ์ตูน'
            };
            
            showNotification(`🎨 กำลัง${filterNames[filterType]}...`, 'info');
            
            setTimeout(() => {
                showNotification(`✅ ${filterNames[filterType]}สำเร็จ!`, 'success');
            }, 3000);
        }

        function updateIntensity(value) {
            document.getElementById('intensityValue').textContent = value;
        }

        // Drag and drop for image editor
        function setupImageDropZone() {
            const dropZone = document.getElementById('imageDropZone');
            
            dropZone.addEventListener('dragover', function(e) {
                e.preventDefault();
                dropZone.classList.add('border-cyan-300');
            });
            
            dropZone.addEventListener('dragleave', function(e) {
                e.preventDefault();
                dropZone.classList.remove('border-cyan-300');
            });
            
            dropZone.addEventListener('drop', function(e) {
                e.preventDefault();
                dropZone.classList.remove('border-cyan-300');
                
                const files = e.dataTransfer.files;
                if (files.length > 0 && files[0].type.startsWith('image/')) {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        document.getElementById('previewImage').src = e.target.result;
                        document.getElementById('imagePreview').classList.remove('hidden');
                        showNotification('✅ โหลดรูปภาพสำเร็จ!', 'success');
                    };
                    reader.readAsDataURL(files[0]);
                }
            });
        }

        // Additional image functions
        function generateVariation(originalPrompt) {
            const variations = [
                'different angle',
                'different lighting',
                'different color scheme',
                'different composition',
                'different style'
            ];
            
            const variation = variations[Math.floor(Math.random() * variations.length)];
            document.getElementById('imagePrompt').value = `${originalPrompt}, ${variation}`;
            generateImage();
        }

        function enhanceImage(imageUrl) {
            showNotification('✨ กำลังปรับปรุงภาพ... (ฟีเจอร์กำลังพัฒนา)', 'info');
        }

        function showImageModal(imageUrl, prompt, modelName) {
            // Create and show image modal
            const modal = document.createElement('div');
            modal.className = 'modal show';
            modal.innerHTML = `
                <div class="modal-content max-w-4xl">
                    <div class="flex justify-between items-center mb-4">
                        <h3 class="text-xl font-bold text-cyan-300">🖼️ ภาพที่สร้างด้วย AI</h3>
                        <button onclick="this.closest('.modal').remove()" class="text-white text-2xl hover:text-cyan-300">×</button>
                    </div>
                    <img src="${imageUrl}" alt="Generated Image" class="w-full rounded-lg shadow-2xl mb-4">
                    <div class="bg-gray-800/50 rounded-lg p-4">
                        <p class="text-white"><strong>Prompt:</strong> ${prompt}</p>
                        <p class="text-cyan-300 text-sm mt-1">Model: ${modelName}</p>
                    </div>
                </div>
            `;
            
            document.body.appendChild(modal);
        }

        // Download image function
        async function downloadImage(imageUrl, prompt) {
            try {
                const response = await fetch(imageUrl);
                const blob = await response.blob();
                const url = window.URL.createObjectURL(blob);
                const a = document.createElement('a');
                a.href = url;
                a.download = `ai-image-${prompt.substring(0, 20).replace(/[^a-zA-Z0-9]/g, '-')}.png`;
                document.body.appendChild(a);
                a.click();
                document.body.removeChild(a);
                window.URL.revokeObjectURL(url);
                showNotification('💾 ดาวน์โหลดสำเร็จ!', 'success');
            } catch (error) {
                showNotification('❌ ไม่สามารถดาวน์โหลดได้', 'error');
            }
        }

        // Share image function
        async function shareImage(imageUrl) {
            if (navigator.share) {
                try {
                    const response = await fetch(imageUrl);
                    const blob = await response.blob();
                    const file = new File([blob], 'ai-generated-image.png', { type: 'image/png' });
                    
                    await navigator.share({
                        title: 'AI Generated Image',
                        text: 'ภาพที่สร้างด้วย AI Universe Pro',
                        files: [file]
                    });
                    showNotification('📤 แชร์สำเร็จ!', 'success');
                } catch (error) {
                    copyImageUrl(imageUrl);
                }
            } else {
                copyImageUrl(imageUrl);
            }
        }

        function copyImageUrl(imageUrl) {
            navigator.clipboard.writeText(imageUrl).then(() => {
                showNotification('📋 คัดลอก URL แล้ว!', 'success');
            });
        }

        function tryDifferentPrompt() {
            document.getElementById('imagePrompt').focus();
            showNotification('💡 ลองใช้คำอธิบายที่ชัดเจนมากขึ้น', 'info');
        }

        // Voice functionality
        function toggleVoiceRecording() {
            const btn = document.getElementById('voiceBtn');
            
            if (!isRecording) {
                isRecording = true;
                btn.textContent = '⏹️ หยุดบันทึก';
                btn.classList.add('bg-red-500');
                
                // Simulate recording
                setTimeout(() => {
                    isRecording = false;
                    btn.textContent = '🎤 เริ่มบันทึกเสียง';
                    btn.classList.remove('bg-red-500');
                    
                    // Add transcribed text to chat
                    const messages = document.getElementById('chatMessages');
                    const message = document.createElement('div');
                    message.className = 'chat-message user';
                    message.innerHTML = '<strong>เสียงของคุณ:</strong> สวัสดีครับ ช่วยอธิบายเรื่อง AI ให้ฟังหน่อย';
                    messages.appendChild(message);
                    
                    // AI response
                    setTimeout(() => {
                        const aiMessage = document.createElement('div');
                        aiMessage.className = 'chat-message ai';
                        aiMessage.innerHTML = '<strong>AI:</strong> AI หรือ Artificial Intelligence คือเทคโนโลยีที่ทำให้เครื่องจักรสามารถเรียนรู้และตัดสินใจได้เหมือนมนุษย์ครับ 🤖';
                        messages.appendChild(aiMessage);
                        messages.scrollTop = messages.scrollHeight;
                    }, 1000);
                }, 3000);
            }
        }

        function speakText() {
            const text = document.getElementById('ttsText').value;
            if (!text.trim()) {
                alert('กรุณาใส่ข้อความ');
                return;
            }
            
            // Simulate text-to-speech
            showNotification('กำลังอ่านออกเสียง... 🔊');
        }

        function cloneVoice() {
            showNotification('กำลังโคลนเสียง... 🎭 (ใช้เวลา 2-3 นาที)');
        }

        // Code generation
        function generateCode() {
            const prompt = document.getElementById('codePrompt').value;
            const language = document.getElementById('codeLanguage').value;
            const result = document.getElementById('codeResult');
            
            if (!prompt.trim()) {
                alert('กรุณาอธิบายโค้ดที่ต้องการ');
                return;
            }

            result.classList.remove('hidden');
            
            setTimeout(() => {
                const sampleCode = {
                    'Python': `def hello_world():
    """
    ฟังก์ชันสำหรับแสดงข้อความ Hello World
    """
    print("Hello, World!")
    return "Success"

# เรียกใช้ฟังก์ชัน
if __name__ == "__main__":
    result = hello_world()
    print(f"Result: {result}")`,
                    'JavaScript': `// ฟังก์ชันสำหรับแสดงข้อความ Hello World
function helloWorld() {
    console.log("Hello, World!");
    return "Success";
}

// เรียกใช้ฟังก์ชัน
const result = helloWorld();
console.log(\`Result: \${result}\`);`,
                    'Java': `public class HelloWorld {
    /**
     * ฟังก์ชันหลักของโปรแกรม
     */
    public static void main(String[] args) {
        String result = helloWorld();
        System.out.println("Result: " + result);
    }
    
    /**
     * ฟังก์ชันสำหรับแสดงข้อความ Hello World
     */
    public static String helloWorld() {
        System.out.println("Hello, World!");
        return "Success";
    }
}`
                };

                document.getElementById('generatedCode').textContent = sampleCode[language] || sampleCode['Python'];
            }, 2000);
        }

        function copyCode() {
            const code = document.getElementById('generatedCode').textContent;
            navigator.clipboard.writeText(code).then(() => {
                showNotification('โค้ดถูกคัดลอกแล้ว! 📋');
            });
        }

        // Data analysis
        function analyzeData() {
            showNotification('กำลังวิเคราะห์ข้อมูล... 📊 (ใช้เวลา 30 วินาที)');
        }

        // Quick actions
        function quickAction(action) {
            const actions = {
                'summarize': 'เริ่มสรุปข้อความ... 📝',
                'translate': 'เริ่มแปลภาษา... 🌐',
                'optimize': 'เริ่มปรับปรุงโค้ด... ⚡',
                'explain': 'เริ่มอธิบายแนวคิด... 🧠'
            };
            
            showNotification(actions[action]);
            closeModal('quickActionsModal');
        }

        // AI Model functions
        function openLanguageModels() {
            showNotification('เปิด Language Models... 🗣️');
        }

        function openImageGeneration() {
            showAIAssistant();
            switchTab('image');
        }

        function openVoiceAI() {
            showAIAssistant();
            switchTab('voice');
        }

        function openVideoAI() {
            showNotification('เปิด Video AI... 🎬 (กำลังพัฒนา)');
        }

        function openCodeAI() {
            showAIAssistant();
            switchTab('code');
        }

        function openDataAnalysis() {
            showAIAssistant();
            switchTab('analysis');
        }

        function open3DAI() {
            showNotification('เปิด 3D AI... 🎯 (กำลังพัฒนา)');
        }

        function openMedicalAI() {
            showNotification('เปิด Medical AI... 🏥 (ต้องการใบอนุญาต)');
        }

        // Notification system
        function showNotification(message, type = 'info') {
            const notification = document.createElement('div');
            notification.className = `fixed top-4 right-4 z-50 p-4 rounded-lg text-white font-semibold transform translate-x-full transition-transform duration-300 ${
                type === 'error' ? 'bg-red-500' : type === 'success' ? 'bg-green-500' : 'bg-cyan-500'
            }`;
            notification.textContent = message;
            
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.style.transform = 'translateX(0)';
            }, 100);
            
            setTimeout(() => {
                notification.style.transform = 'translateX(100%)';
                setTimeout(() => {
                    if (document.body.contains(notification)) {
                        document.body.removeChild(notification);
                    }
                }, 300);
            }, 3000);
        }

        // Keyboard shortcuts
        document.addEventListener('keydown', function(event) {
            if (event.key === 'Escape') {
                document.querySelectorAll('.modal.show').forEach(modal => {
                    modal.classList.remove('show');
                });
            }
            
            if (event.ctrlKey || event.metaKey) {
                switch (event.key) {
                    case 'k':
                        event.preventDefault();
                        showAIAssistant();
                        break;
                    case 'q':
                        event.preventDefault();
                        showQuickActions();
                        break;
                }
            }
        });

        // Chat input enter key
        document.getElementById('chatInput').addEventListener('keypress', function(event) {
            if (event.key === 'Enter') {
                sendMessage();
            }
        });

        // Close modals when clicking outside
        document.addEventListener('click', function(event) {
            if (event.target.classList.contains('modal')) {
                event.target.classList.remove('show');
            }
        });

        // Initialize everything
        document.addEventListener('DOMContentLoaded', function() {
            initNeuralBackground();
            updateStats();
            simulateDataStream();
            setupImageDropZone();
            loadLibraryImages();
            
            // Show welcome message
            setTimeout(() => {
                showNotification('ยินดีต้อนรับสู่ Mozilla AI Universe! 🦊✨', 'success');
            }, 1000);
            
            // Initialize search on enter key
            document.getElementById('imageSearchQuery').addEventListener('keypress', function(event) {
                if (event.key === 'Enter') {
                    searchGlobalImages();
                }
            });
        });

        // Auto-update stats every 5 seconds
        setInterval(() => {
            const elements = ['activeModels', 'totalRequests', 'successRate', 'responseTime'];
            elements.forEach(id => {
                const element = document.getElementById(id);
                const current = parseFloat(element.textContent);
                const variation = (Math.random() - 0.5) * 0.1;
                let newValue = current + variation;
                
                if (id === 'successRate') {
                    newValue = Math.max(99.0, Math.min(99.9, newValue));
                    element.textContent = newValue.toFixed(1) + '%';
                } else if (id === 'responseTime') {
                    newValue = Math.max(0.1, Math.min(0.5, newValue));
                    element.textContent = newValue.toFixed(1) + 's';
                }
            });
        }, 5000);
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'97c1e94445eb45c9',t:'MTc1NzM3MDg0NS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>

