<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>猫咪职业性格测试：你的小猫适合做什么工作？</title>

    <!-- 新增的GitHub Pages优化标签 -->
    <meta name="description" content="超准的猫咪职业性格测试,快来看看你家主子的隐藏天赋!30道题揭示猫咪的真实职业倾向。">
    <meta property="og:title" content="猫咪职业性格测试">
    <meta property="og:description" content="测测你的小猫适合做什么工作？超准的猫咪职业测试！">
    <meta property="og:type" content="website">
    <meta name="twitter:card" content="summary">
    <meta name="referrer" content="no-referrer">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Helvetica Neue', Arial, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f9f3e9 0%, #e8d5c4 100%);
            color: #5a4a3a;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .container {
            max-width: 800px;
            width: 100%;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            padding: 30px;
            position: relative;
        }
        
        .cat-decoration {
            position: absolute;
            width: 120px;
            height: 120px;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path d="M50,20 C65,20 75,30 75,45 C75,60 65,70 50,70 C35,70 25,60 25,45 C25,30 35,20 50,20 Z" fill="%23ffb6c1"/><circle cx="40" cy="40" r="5" fill="%235a4a3a"/><circle cx="60" cy="40" r="5" fill="%235a4a3a"/><path d="M45,50 Q50,55 55,50" stroke="%235a4a3a" stroke-width="2" fill="none"/><path d="M35,15 Q40,5 50,5 Q60,5 65,15" stroke="%235a4a3a" stroke-width="2" fill="none"/><path d="M30,30 Q20,25 15,30" stroke="%235a4a3a" stroke-width="2" fill="none"/><path d="M70,30 Q80,25 85,30" stroke="%235a4a3a" stroke-width="2" fill="none"/></svg>');
            background-size: contain;
            background-repeat: no-repeat;
            opacity: 0.1;
            z-index: 0;
        }
        
        .decoration-1 {
            top: 20px;
            left: 20px;
        }
        
        .decoration-2 {
            bottom: 20px;
            right: 20px;
            transform: rotate(180deg);
        }
        
        .content {
            position: relative;
            z-index: 1;
        }
        
        h1 {
            text-align: center;
            color: #8b6b4c;
            margin-bottom: 15px;
            font-size: 2.2rem;
        }
        
        .subtitle {
            text-align: center;
            color: #a38a70;
            margin-bottom: 30px;
            font-size: 1.1rem;
        }
        
        .screen {
            display: none;
        }
        
        #start-screen {
            display: block;
            text-align: center;
        }
        
        .intro-text {
            margin-bottom: 30px;
            line-height: 1.6;
            font-size: 1.1rem;
            text-align: center;
        }
        
        .disclaimer {
            background-color: #fff8e1;
            border-left: 4px solid #ffd54f;
            padding: 15px;
            margin: 20px 0;
            border-radius: 8px;
            font-size: 0.9rem;
            color: #8b6b4c;
            text-align: left;
        }
        
        .cat-illustration {
            width: 200px;
            height: 200px;
            margin: 0 auto 30px;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path d="M50,25 C60,25 70,30 75,40 C80,50 80,60 75,70 C70,80 60,85 50,85 C40,85 30,80 25,70 C20,60 20,50 25,40 C30,30 40,25 50,25 Z" fill="%23ffb6c1"/><circle cx="40" cy="45" r="5" fill="%235a4a3a"/><circle cx="60" cy="45" r="5" fill="%235a4a3a"/><path d="M45,60 Q50,65 55,60" stroke="%235a4a3a" stroke-width="2" fill="none"/><path d="M35,25 Q40,15 50,15 Q60,15 65,25" stroke="%235a4a3a" stroke-width="2" fill="none"/><path d="M25,35 Q15,30 10,35" stroke="%235a4a3a" stroke-width="2" fill="none"/><path d="M75,35 Q85,30 90,35" stroke="%235a4a3a" stroke-width="2" fill="none"/></svg>');
            background-size: contain;
            background-repeat: no-repeat;
        }
        
        .btn {
            background: linear-gradient(135deg, #ffb6c1 0%, #ff8fa3 100%);
            color: white;
            border: none;
            border-radius: 50px;
            padding: 12px 30px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 143, 163, 0.3);
            display: inline-block;
            margin: 10px;
        }
        
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(255, 143, 163, 0.4);
        }
        
        .btn:disabled {
            background: #cccccc;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }
        
        .btn-secondary {
            background: linear-gradient(135deg, #a38a70 0%, #8b6b4c 100%);
            box-shadow: 0 4px 15px rgba(139, 107, 76, 0.3);
        }
        
        .btn-secondary:hover {
            box-shadow: 0 6px 20px rgba(139, 107, 76, 0.4);
        }
        
        .progress-container {
            margin-bottom: 20px;
        }
        
        .progress-bar {
            height: 8px;
            background-color: #e9dcd0;
            border-radius: 4px;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            background: linear-gradient(135deg, #ffb6c1 0%, #ff8fa3 100%);
            width: 0%;
            transition: width 0.5s ease;
        }
        
        .question-counter {
            text-align: center;
            margin-bottom: 15px;
            font-size: 1rem;
            color: #a38a70;
        }
        
        .question-text {
            font-size: 1.4rem;
            margin-bottom: 25px;
            text-align: center;
            font-weight: 500;
        }
        
        .options-container {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 30px;
        }
        
        .option {
            background-color: #f8f4f0;
            border: 2px solid #e9dcd0;
            border-radius: 12px;
            padding: 15px 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: left;
        }
        
        .option:hover {
            background-color: #f0e6dc;
            border-color: #d4c4b4;
        }
        
        .option.selected {
            background-color: #ffeef2;
            border-color: #ffb6c1;
            color: #8b6b4c;
        }
        
        .button-group {
            display: flex;
            justify-content: space-between;
            gap: 15px;
        }
        
        .button-group .btn {
            flex: 1;
        }
        
        .result-container {
            text-align: center;
            padding: 20px;
        }
        
        .result-title {
            font-size: 1.8rem;
            color: #8b6b4c;
            margin-bottom: 20px;
        }
        
        .result-image {
            width: 150px;
            height: 150px;
            margin: 0 auto 20px;
            background-size: contain;
            background-repeat: no-repeat;
            background-position: center;
        }
        
        .result-description {
            font-size: 1.1rem;
            line-height: 1.7;
            text-align: left;
            margin-bottom: 30px;
            background-color: #f8f4f0;
            padding: 20px;
            border-radius: 12px;
        }
        
        .result-advice {
            margin-bottom: 30px;
            text-align: left;
        }
        
        .advice-title {
            font-weight: bold;
            margin-bottom: 10px;
            color: #8b6b4c;
            font-size: 1.2rem;
        }
        
        #result-advice {
            background-color: #f8f4f0;
            padding: 20px;
            border-radius: 12px;
            line-height: 1.7;
        }
        
        .share-section {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #e9dcd0;
        }
        
        .share-text {
            margin-bottom: 15px;
            font-size: 1rem;
        }
        
        .share-buttons {
            display: flex;
            justify-content: center;
            gap: 15px;
        }
        
        .share-btn {
            background: #f0e6dc;
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .share-btn:hover {
            background: #e9dcd0;
            transform: scale(1.1);
        }
        
        /* 稀有度标记样式 */
        .rarity-badge {
            display: inline-block;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: bold;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 1px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .rarity-common {
            background: linear-gradient(135deg, #e8f5e9, #c8e6c9);
            color: #2e7d32;
            border: 2px solid #81c784;
        }
        
        .rarity-rare {
            background: linear-gradient(135deg, #e3f2fd, #bbdefb);
            color: #1565c0;
            border: 2px solid #64b5f6;
        }
        
        .rarity-epic {
            background: linear-gradient(135deg, #f3e5f5, #e1bee7);
            color: #7b1fa2;
            border: 2px solid #ba68c8;
            animation: pulse 2s infinite alternate;
        }
        
        .rarity-legendary {
            background: linear-gradient(135deg, #fff8e1, #ffecb3);
            color: #ff8f00;
            border: 2px solid #ffd54f;
            animation: glow 2s infinite alternate;
        }
        
        @keyframes glow {
            from {
                box-shadow: 0 0 5px #ffd54f;
            }
            to {
                box-shadow: 0 0 15px #ffd54f, 0 0 20px #ffd54f;
            }
        }
        
        @keyframes pulse {
            from {
                box-shadow: 0 0 5px #ba68c8;
            }
            to {
                box-shadow: 0 0 10px #ba68c8, 0 0 15px #ba68c8;
            }
        }
        
        .rarity-explanation {
            margin-top: 10px;
            font-size: 0.9rem;
            color: #8b6b4c;
        }
        
        /* 移动端优化 */
        @media (max-width: 600px) {
            .container {
                padding: 15px;
                margin: 10px;
                border-radius: 15px;
            }
            
            h1 {
                font-size: 1.6rem;
                line-height: 1.3;
            }
            
            .question-text {
                font-size: 1.1rem;
                line-height: 1.4;
                margin-bottom: 20px;
            }
            
            .option {
                padding: 12px;
                font-size: 0.95rem;
                line-height: 1.4;
            }
            
            /* 防止文本溢出 */
            .rarity-badge {
                font-size: 0.8rem;
                white-space: nowrap;
                padding: 6px 12px;
            }
            
            .result-description {
                font-size: 1rem;
                line-height: 1.6;
                padding: 15px;
            }
            
            .btn {
                padding: 10px 20px;
                font-size: 1rem;
            }
            
            .button-group {
                flex-direction: column;
            }
        }

        /* 触摸设备优化 */
        @media (hover: none) {
            .option:hover {
                background-color: #f8f4f0; /* 移除移动端的hover效果 */
                transform: none;
            }
    
            .btn:hover {
                transform: none;
                box-shadow: 0 4px 15px rgba(255, 143, 163, 0.3);
            }
    
            .share-btn:hover {
                transform: none;
                background: #f0e6dc;
            }
        }

        /* 防止移动端点击延迟 */
        .option, .btn, .share-btn {
            touch-action: manipulation;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="cat-decoration decoration-1"></div>
        <div class="cat-decoration decoration-2"></div>
        
        <div class="content">
            <!-- 开始屏幕 -->
            <div id="start-screen" class="screen">
                <h1>猫咪职业性格测试</h1>
                <p class="subtitle">测测你的小猫适合做什么工作？</p>
                
                <div class="cat-illustration"></div>
                
                <p class="intro-text">
                    想知道你家猫咪如果变成人类，会从事什么职业吗？<br>
                    通过观察猫咪的日常行为和性格特点，我们将为你揭示它的职业天赋！<br>
                    本测试包含30个问题，大约需要5-8分钟完成。
                </p>
                
                <div class="disclaimer">
                    <strong>注意：</strong>个人能力有限，测试结果仅供参考，请勿作为专业判断依据。
                </div>
                
                <button id="start-btn" class="btn">开始测试</button>
            </div>
            
            <!-- 问题屏幕 -->
            <div id="question-screen" class="screen">
                <div class="progress-container">
                    <div class="progress-bar">
                        <div class="progress" id="progress"></div>
                    </div>
                </div>
                
                <div class="question-counter" id="question-counter"></div>
                
                <div class="question-text" id="question-text"></div>
                
                <div class="options-container" id="options-container"></div>
                
                <div class="button-group">
                    <button id="prev-btn" class="btn btn-secondary">上一题</button>
                    <button id="next-btn" class="btn" disabled>下一题</button>
                </div>
            </div>
            
            <!-- 结果屏幕 -->
            <div id="result-screen" class="screen">
                <h2 class="result-title">测试结果</h2>
                
                <div class="result-image" id="result-image"></div>
                
                <div id="result-rarity" class="rarity-badge"></div>
                
                <div id="rarity-explanation" class="rarity-explanation"></div>
                
                <h3 id="result-job-title"></h3>
                
                <div class="result-description" id="result-description"></div>

                <div class="result-advice">
                    <div class="advice-title">相处建议：</div>
                    <div id="result-advice"></div>
                </div>
                
                <button id="restart-btn" class="btn">再测一次</button>
                
                <div class="share-section">
                    <p class="share-text">分享测试结果给朋友看看吧！</p>
                    <div class="share-buttons">
                        <div class="share-btn" id="wechat-share">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="#8b6b4c">
                                <path d="M8.691 3.042C4.328 4.241 1 8.213 1 12.983c0 1.788.579 3.441 1.563 4.785l-.656 2.945 3.109-.855c1.356.731 2.922 1.142 4.584 1.142 4.363 0 7.9-3.438 7.9-7.678 0-4.24-3.537-7.678-7.9-7.678-.483 0-.956.044-1.417.128zm-.208 1.39c.381-.057.773-.086 1.171-.086 3.708 0 6.715 2.924 6.715 6.529s-3.007 6.529-6.715 6.529a6.76 6.76 0 0 1-3.354-.885l-.211-.124-2.015.554.537-1.924-.157-.188a6.433 6.433 0 0 1-1.005-3.437c0-3.605 3.007-6.529 6.715-6.529z"/>
                            </svg>
                        </div>
                        <div class="share-btn" id="weibo-share">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="#8b6b4c">
                                <path d="M10.525 2.463c-.416-.378-1.057-.345-1.435.07-.379.416-.345 1.057.07 1.435C11.242 5.483 12 7.408 12 9.5s-.758 4.017-2.84 5.532c-.416.378-.449 1.02-.07 1.435.217.239.521.357.825.357.245 0 .49-.088.68-.262C12.909 14.716 14 12.245 14 9.5s-1.091-5.216-3.475-7.037z"/>
                                <path d="M16.5 9.5c0 1.407-.432 2.675-1.121 3.752-.396.623-.881 1.179-1.438 1.654-.416.378-.449 1.02-.07 1.435.217.239.521.357.825.357.245 0 .49-.088.68-.262a8.438 8.438 0 0 0 2.224-3.405C18.975 11.766 19.5 10.682 19.5 9.5c0-1.182-.525-2.266-1.374-3.031-.416-.378-1.057-.345-1.435.07-.379.416-.345 1.057.07 1.435.515.468.839 1.127.839 1.526z"/>
                            </svg>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // ============ 全局变量 ============
        let currentQuestionIndex = 0;
        let userScores = {};
        let selectedOptionIndex = null;
        let userChoices = [];

        // 特质分类和权重
        const traitCategories = {
            energetic: { weight: 2.0, name: "精力充沛" },
            lazy: { weight: 1.8, name: "慵懒" },
            social: { weight: 1.6, name: "社交型" },
            independent: { weight: 1.5, name: "独立型" },
            observer: { weight: 1.4, name: "观察者" },
            playful: { weight: 1.3, name: "爱玩" },
            affectionate: { weight: 1.2, name: "亲热型" },
            cautious: { weight: 1.2, name: "谨慎" },
            explorer: { weight: 1.2, name: "探索者" },
            hunter: { weight: 1.1, name: "猎手" },
            homebody: { weight: 1.1, name: "居家型" },
            foodie: { weight: 1.0, name: "吃货" },
            territorial: { weight: 1.0, name: "领地意识" },
            refined: { weight: 0.9, name: "优雅" },
            provider: { weight: 1.0, name: "提供者" },
            loyal: { weight: 1.0, name: "忠诚" }
        };

        // 初始化分数对象
        function initializeScores() {
            for (const trait in traitCategories) {
                userScores[trait] = 0;
            }
            userChoices = new Array(questions.length).fill(null);
        }

        // 优化的匹配算法
        function findBestMatch() {
            let bestMatch = null;
            let bestScore = -1;
            
            results.forEach(result => {
                const matchScore = calculateMatchScore(result.conditions);
                
                if (matchScore > bestScore) {
                    bestScore = matchScore;
                    bestMatch = result;
                }
            });
            
            console.log("最佳匹配结果:", bestMatch?.title, "得分:", bestScore.toFixed(2));
            return bestMatch;
        }

        // 匹配分数计算
        function calculateMatchScore(conditions) {
            let totalScore = 0;
            let maxPossibleScore = 0;
            
            for (const trait in conditions) {
                const requiredScore = conditions[trait];
                const userScore = userScores[trait] || 0;
                
                if (requiredScore > 0) {
                    // 计算该特质的匹配度（0-1）
                    let traitMatch = 0;
                    
                    // 使用软阈值：用户分数达到要求80%即可获得较高匹配度
                    if (userScore >= requiredScore * 0.8) {
                        traitMatch = Math.min(1.0, userScore / requiredScore);
                    } else {
                        traitMatch = (userScore / requiredScore) * 0.8;
                    }
                    
                    // 应用特质权重
                    const weight = traitCategories[trait]?.weight || 1.0;
                    totalScore += traitMatch * weight;
                    maxPossibleScore += weight;
                }
            }
            
            // 额外加分：如果用户的核心特质非常突出
            let bonusScore = 0;
            for (const trait in conditions) {
                const requiredScore = conditions[trait];
                const userScore = userScores[trait] || 0;
                
                if (requiredScore > 0 && userScore > requiredScore * 1.2) {
                    bonusScore += 0.05; // 每项突出特质额外加5%
                }
            }
            
            const baseScore = maxPossibleScore > 0 ? totalScore / maxPossibleScore : 0;
            return Math.min(1.0, baseScore + bonusScore);
        }

        // 30个测试问题
        const questions = [
            {
                question: "早上醒来时，你的猫咪通常做什么？",
                options: [
                    { text: "伸个懒腰，继续在温暖的地方打盹", scores: { lazy: 4, homebody: 3 } },
                    { text: "立刻跑到你身边，用头蹭你要求早餐", scores: { social: 4, energetic: 3 } },
                    { text: "精力充沛地在房间里跑酷，仿佛有无限能量", scores: { energetic: 5, playful: 3 } },
                    { text: "静静地坐在窗边，观察外面的世界", scores: { observer: 4, cautious: 3 } },
                    { text: "检查家里的每个角落，看看有没有变化", scores: { explorer: 4, cautious: 3 } }
                ]
            },
            {
                question: "当有新客人来访时，你的猫咪会？",
                options: [
                    { text: "躲起来，直到确定安全才出来", scores: { cautious: 5, independent: 3 } },
                    { text: "立刻上前迎接，蹭客人的腿求关注", scores: { social: 5, affectionate: 3 } },
                    { text: "先观察一会儿，然后小心翼翼地接近", scores: { observer: 4, cautious: 4 } },
                    { text: "完全无视客人，继续做自己的事", scores: { independent: 5, lazy: 3 } },
                    { text: "检查客人的包包和鞋子，像安检一样", scores: { explorer: 4, observer: 4 } }
                ]
            },
            {
                question: "你的猫咪最喜欢的玩具类型是？",
                options: [
                    { text: "互动型玩具，需要你陪着一起玩", scores: { social: 4, playful: 4 } },
                    { text: "能自己玩的玩具，比如自动激光笔或电动老鼠", scores: { independent: 4, playful: 3 } },
                    { text: "智力玩具，需要解决问题才能获得零食", scores: { observer: 4, independent: 3 } },
                    { text: "软软的、可以抱着的东西", scores: { lazy: 4, affectionate: 3 } },
                    { text: "任何可以拆解或破坏的东西", scores: { explorer: 4, playful: 3 } }
                ]
            },
            {
                question: "当窗外有小鸟或其他动物时，你的猫咪会？",
                options: [
                    { text: "发出奇怪的咔咔声，尾巴快速摆动", scores: { hunter: 5, energetic: 3 } },
                    { text: "静静地观察，几乎一动不动", scores: { observer: 5, cautious: 3 } },
                    { text: "尝试各种方法想要出去", scores: { explorer: 5, energetic: 3 } },
                    { text: "看一会儿就失去兴趣，回去睡觉", scores: { lazy: 5, homebody: 3 } },
                    { text: "兴奋地在窗台和地面之间跳来跳去", scores: { energetic: 4, playful: 4 } }
                ]
            },
            {
                question: "你的猫咪如何表达对你的爱意？",
                options: [
                    { text: "用头蹭你，在你身上踩奶", scores: { affectionate: 5, social: 3 } },
                    { text: "给你带来'礼物'(比如玩具或小虫子)", scores: { hunter: 4, provider: 3 } },
                    { text: "当你回家时在门口迎接你", scores: { social: 4, loyal: 4 } },
                    { text: "静静地待在你身边，不打扰你", scores: { lazy: 4, homebody: 3 } },
                    { text: "用爪子轻轻拍你的脸，叫你起床", scores: { energetic: 4, affectionate: 3 } }
                ]
            },
            {
                question: "你的猫咪对新环境的反应是？",
                options: [
                    { text: "立刻开始探索每个角落", scores: { explorer: 5, energetic: 3 } },
                    { text: "先躲起来观察，慢慢适应", scores: { cautious: 5, observer: 3 } },
                    { text: "紧紧跟着你，寻求安全感", scores: { social: 4, affectionate: 4 } },
                    { text: "表现得无所谓，在哪里都一样", scores: { independent: 4, lazy: 3 } },
                    { text: "仔细检查每个物品，确保安全", scores: { cautious: 4, observer: 4 } }
                ]
            },
            {
                question: "你的猫咪的睡眠习惯是？",
                options: [
                    { text: "在任何地方都能睡着，睡眠质量很好", scores: { lazy: 5, homebody: 3 } },
                    { text: "喜欢睡在高处，能俯瞰整个房间", scores: { observer: 4, independent: 3 } },
                    { text: "一定要睡在你身边或腿上", scores: { affectionate: 5, social: 3 } },
                    { text: "睡眠很浅，一点声音就会醒来", scores: { cautious: 5, observer: 3 } },
                    { text: "睡姿奇特，像在表演杂技", scores: { playful: 4, energetic: 3 } }
                ]
            },
            {
                question: "当有奇怪的声音时，你的猫咪会？",
                options: [
                    { text: "立刻警觉，寻找声音来源", scores: { observer: 4, cautious: 4 } },
                    { text: "躲到安全的地方", scores: { cautious: 5, homebody: 3 } },
                    { text: "完全不在意，继续做自己的事", scores: { independent: 4, lazy: 3 } },
                    { text: "好奇地靠近，想弄清楚是什么", scores: { explorer: 4, energetic: 3 } },
                    { text: "竖起耳朵，但保持原地不动观察", scores: { observer: 5, cautious: 3 } }
                ]
            },
            {
                question: "你的猫咪与其他动物的相处方式是？",
                options: [
                    { text: "主动示好，想交朋友", scores: { social: 5, playful: 3 } },
                    { text: "保持距离，观察对方", scores: { observer: 4, cautious: 4 } },
                    { text: "表现出敌意，捍卫自己的领地", scores: { territorial: 4, cautious: 3 } },
                    { text: "完全无视，仿佛对方不存在", scores: { independent: 5, lazy: 3 } },
                    { text: "试图追逐或玩耍，但不知轻重", scores: { playful: 4, energetic: 3 } }
                ]
            },
            {
                question: "你的猫咪对食物的态度是？",
                options: [
                    { text: "非常挑食，只吃特定的食物", scores: { cautious: 4, refined: 3 } },
                    { text: "什么都吃，胃口特别好", scores: { foodie: 5, energetic: 3 } },
                    { text: "吃得很快，好像有人要抢", scores: { energetic: 4, playful: 3 } },
                    { text: "细嚼慢咽，享受每一口", scores: { observer: 4, refined: 3 } },
                    { text: "喜欢藏食物，或者把食物弄得到处都是", scores: { playful: 4, explorer: 3 } }
                ]
            },
            {
                question: "你的猫咪对水的态度是？",
                options: [
                    { text: "讨厌水，洗澡像打仗一样", scores: { cautious: 4, homebody: 3 } },
                    { text: "对水好奇，但不敢真的接触", scores: { observer: 4, cautious: 3 } },
                    { text: "完全不怕水，甚至喜欢玩水", scores: { explorer: 4, energetic: 3 } },
                    { text: "只喝流动的水，对静止水没兴趣", scores: { refined: 4, cautious: 3 } },
                    { text: "对水漠不关心，渴了才喝", scores: { independent: 4, lazy: 3 } }
                ]
            },
            {
                question: "你的猫咪最喜欢的休息地点是？",
                options: [
                    { text: "你的床上或沙发上", scores: { affectionate: 4, social: 3 } },
                    { text: "高处，比如书架或柜子顶", scores: { observer: 5, independent: 3 } },
                    { text: "隐蔽的角落，比如床底下", scores: { cautious: 5, homebody: 3 } },
                    { text: "阳光充足的地方", scores: { lazy: 4, homebody: 4 } },
                    { text: "经常换地方，没有固定位置", scores: { explorer: 4, energetic: 3 } }
                ]
            },
            {
                question: "当你在家工作时，你的猫咪通常会？",
                options: [
                    { text: "躺在你的键盘上或电脑前", scores: { social: 4, affectionate: 4 } },
                    { text: "在旁边安静地睡觉", scores: { lazy: 5, homebody: 3 } },
                    { text: "不断打扰你，要求玩耍", scores: { playful: 5, energetic: 3 } },
                    { text: "在远处观察你", scores: { observer: 5, independent: 3 } },
                    { text: "完全无视你，做自己的事", scores: { independent: 5, lazy: 3 } }
                ]
            },
            {
                question: "你的猫咪对纸箱的态度是？",
                options: [
                    { text: "非常喜欢，一有纸箱就钻进去", scores: { explorer: 4, playful: 4 } },
                    { text: "把纸箱当床，在里面睡觉", scores: { lazy: 5, homebody: 3 } },
                    { text: "把纸箱当玩具，又抓又咬", scores: { playful: 5, energetic: 3 } },
                    { text: "对纸箱没兴趣", scores: { independent: 4, refined: 3 } },
                    { text: "把纸箱当堡垒，在里面观察外界", scores: { observer: 4, cautious: 4 } }
                ]
            },
            {
                question: "你的猫咪的叫声特点是？",
                options: [
                    { text: "很少叫，几乎是个小哑巴", scores: { independent: 4, observer: 3 } },
                    { text: "经常叫，用不同叫声表达需求", scores: { social: 5, affectionate: 3 } },
                    { text: "只在特定情况下叫，比如饿了", scores: { independent: 4, cautious: 3 } },
                    { text: "叫声很大，很有穿透力", scores: { energetic: 4, social: 3 } },
                    { text: "发出各种奇怪的声音，不只是喵喵叫", scores: { playful: 4, energetic: 3 } }
                ]
            },
            {
                question: "当你抚摸你的猫咪时，它通常会？",
                options: [
                    { text: "非常享受，发出呼噜声", scores: { affectionate: 5, social: 3 } },
                    { text: "只允许摸特定部位", scores: { independent: 4, cautious: 3 } },
                    { text: "一会儿就厌烦，然后走开", scores: { independent: 5, lazy: 3 } },
                    { text: "用爪子或牙齿轻轻回应", scores: { playful: 4, energetic: 3 } },
                    { text: "完全不让你摸", scores: { cautious: 5, independent: 3 } }
                ]
            },
            {
                question: "你的猫咪对高度的态度是？",
                options: [
                    { text: "喜欢待在高处", scores: { observer: 4, independent: 3 } },
                    { text: "害怕高度，不敢跳高", scores: { cautious: 5, homebody: 3 } },
                    { text: "是攀爬高手，哪里都能上去", scores: { energetic: 4, explorer: 4 } },
                    { text: "对高度无所谓，上下自如", scores: { independent: 4, energetic: 3 } },
                    { text: "经常从高处摔下来，但不长记性", scores: { playful: 4, energetic: 3 } }
                ]
            },
            {
                question: "你的猫咪对陌生物品的反应是？",
                options: [
                    { text: "立刻上前检查", scores: { explorer: 5, energetic: 3 } },
                    { text: "保持距离观察", scores: { observer: 5, cautious: 3 } },
                    { text: "完全无视", scores: { independent: 5, lazy: 3 } },
                    { text: "表现出恐惧，躲起来", scores: { cautious: 5, homebody: 3 } },
                    { text: "试图攻击或破坏", scores: { territorial: 4, energetic: 3 } }
                ]
            },
            {
                question: "你的猫咪的日常活动主要是？",
                options: [
                    { text: "睡觉，大部分时间在休息", scores: { lazy: 5, homebody: 4 } },
                    { text: "玩耍，精力充沛", scores: { playful: 5, energetic: 4 } },
                    { text: "观察周围环境", scores: { observer: 5, cautious: 3 } },
                    { text: "跟随你，寻求关注", scores: { social: 4, affectionate: 4 } },
                    { text: "探索家里的每个角落", scores: { explorer: 5, energetic: 3 } }
                ]
            },
            {
                question: "你的猫咪对电视或手机屏幕的态度是？",
                options: [
                    { text: "非常感兴趣，会盯着看", scores: { observer: 4, cautious: 3 } },
                    { text: "试图捕捉屏幕上的东西", scores: { hunter: 5, playful: 3 } },
                    { text: "完全无视", scores: { independent: 5, lazy: 3 } },
                    { text: "偶尔看一眼，但没太大兴趣", scores: { lazy: 4, homebody: 3 } },
                    { text: "害怕屏幕上的某些画面", scores: { cautious: 5, homebody: 3 } }
                ]
            },
            {
                question: "你的猫咪的饮食习惯是？",
                options: [
                    { text: "定时定量，很有规律", scores: { cautious: 4, refined: 3 } },
                    { text: "随时想吃，没有固定时间", scores: { foodie: 5, energetic: 3 } },
                    { text: "吃得很少，对食物不感兴趣", scores: { lazy: 4, independent: 3 } },
                    { text: "只吃特定品牌或口味的食物", scores: { refined: 4, cautious: 3 } },
                    { text: "吃相难看，会把食物弄得到处都是", scores: { playful: 4, energetic: 3 } }
                ]
            },
            {
                question: "你的猫咪对梳毛的态度是？",
                options: [
                    { text: "非常享受，主动要求梳毛", scores: { affectionate: 5, social: 3 } },
                    { text: "勉强接受，但不太喜欢", scores: { independent: 4, lazy: 3 } },
                    { text: "讨厌梳毛，会逃跑或反抗", scores: { cautious: 5, independent: 3 } },
                    { text: "只允许梳特定部位", scores: { refined: 4, cautious: 3 } },
                    { text: "会把梳子当玩具", scores: { playful: 4, energetic: 3 } }
                ]
            },
            {
                question: "你的猫咪对门的态度是？",
                options: [
                    { text: "想出去，经常在门口叫", scores: { explorer: 5, energetic: 3 } },
                    { text: "对门外世界好奇，但不敢真的出去", scores: { observer: 4, cautious: 3 } },
                    { text: "害怕出门", scores: { cautious: 5, homebody: 3 } },
                    { text: "对门没兴趣，安心待在家里", scores: { homebody: 5, lazy: 3 } },
                    { text: "会开门或试图开门", scores: { explorer: 4, energetic: 4 } }
                ]
            },
            {
                question: "你的猫咪对塑料袋的态度是？",
                options: [
                    { text: "非常喜欢，会在里面玩耍", scores: { playful: 4, energetic: 3 } },
                    { text: "害怕塑料袋的声音", scores: { cautious: 5, homebody: 3 } },
                    { text: "把塑料袋当床", scores: { lazy: 5, homebody: 3 } },
                    { text: "对塑料袋没兴趣", scores: { independent: 4, lazy: 3 } },
                    { text: "会吃塑料袋，需要特别小心", scores: { explorer: 4, energetic: 3 } }
                ]
            },
            {
                question: "你的猫咪对音乐的反应是？",
                options: [
                    { text: "喜欢音乐，会在音乐声中放松", scores: { refined: 4, observer: 3 } },
                    { text: "对音乐没反应", scores: { independent: 4, lazy: 3 } },
                    { text: "讨厌某些类型的音乐", scores: { cautious: 4, refined: 3 } },
                    { text: "会跟着音乐节奏摆动", scores: { playful: 4, energetic: 3 } },
                    { text: "害怕音乐的声音", scores: { cautious: 5, homebody: 3 } }
                ]
            },
            {
                question: "你的猫咪的社交方式是？",
                options: [
                    { text: "非常友好，喜欢所有人和动物", scores: { social: 5, affectionate: 3 } },
                    { text: "只喜欢特定的人或动物", scores: { independent: 4, cautious: 3 } },
                    { text: "害怕陌生人或动物", scores: { cautious: 5, homebody: 3 } },
                    { text: "对其他人或动物没兴趣", scores: { independent: 5, lazy: 3 } },
                    { text: "会主动攻击陌生人或动物", scores: { territorial: 5, cautious: 3 } }
                ]
            },
            {
                question: "你的猫咪对清洁的态度是？",
                options: [
                    { text: "非常爱干净，经常自我清洁", scores: { refined: 4, cautious: 3 } },
                    { text: "只在特定时间清洁自己", scores: { observer: 4, independent: 3 } },
                    { text: "不太爱干净，需要你帮忙清洁", scores: { lazy: 4, homebody: 3 } },
                    { text: "会帮你清洁（舔你的手或脸）", scores: { affectionate: 5, social: 3 } },
                    { text: "讨厌清洁，洗澡像打仗", scores: { cautious: 5, independent: 3 } }
                ]
            },
            {
                question: "你的猫咪对季节变化的反应是？",
                options: [
                    { text: "夏天找凉爽地方，冬天找温暖地方", scores: { observer: 4, cautious: 3 } },
                    { text: "对季节变化没反应", scores: { independent: 4, lazy: 3 } },
                    { text: "冬天变得更黏人", scores: { affectionate: 5, social: 3 } },
                    { text: "夏天更活跃，冬天更懒惰", scores: { energetic: 4, lazy: 3 } },
                    { text: "对季节变化感到焦虑", scores: { cautious: 5, homebody: 3 } }
                ]
            },
            {
                question: "你的猫咪对医疗护理（如喂药、剪指甲）的态度是？",
                options: [
                    { text: "非常配合，像个懂事的孩子", scores: { independent: 4, observer: 3 } },
                    { text: "勉强接受，但会表现出不满", scores: { cautious: 4, independent: 3 } },
                    { text: "强烈反抗，需要多人协助", scores: { territorial: 4, cautious: 3 } },
                    { text: "会躲起来，让你找不到", scores: { cautious: 5, homebody: 3 } },
                    { text: "完全无视，继续做自己的事", scores: { independent: 5, lazy: 3 } }
                ]
            },
            {
                question: "你的猫咪对家庭地位的认知是？",
                options: [
                    { text: "认为自己是家庭的核心", scores: { social: 4, affectionate: 4 } },
                    { text: "认为自己是家庭的保护者", scores: { territorial: 4, cautious: 4 } },
                    { text: "认为自己是家庭的客人", scores: { cautious: 4, observer: 3 } },
                    { text: "认为自己是家庭的服务者", scores: { provider: 4, loyal: 3 } },
                    { text: "完全没有概念，随心所欲", scores: { independent: 5, lazy: 3 } }
                ]
            },
            {
                question: "你的猫咪对时间的感知是？",
                options: [
                    { text: "非常准时，比如固定时间要求吃饭", scores: { refined: 4, cautious: 3 } },
                    { text: "对时间没概念，随心所欲", scores: { independent: 4, lazy: 3 } },
                    { text: "能感知你的作息时间", scores: { observer: 4, social: 3 } },
                    { text: "白天睡觉，晚上活动", scores: { energetic: 4, explorer: 3 } },
                    { text: "作息完全随你", scores: { affectionate: 4, social: 3 } }
                ]
            }
        ];

        // 职业结果数据 - 调整稀有度分布
        const results = [
            // ============ 常见职业 (12个) ============
            {
                id: "breakfastSeller",
                title: "苦命勤劳猫·早餐摊主",
                description: "你的猫咪是天生的劳模！为了维持你们一家的幸福生活，它愿意凌晨4点起床去卖包子。虽然生活艰辛，但它从不抱怨，总是默默付出。它的座右铭是：'只要主人过得好，我累点没关系！'",
                advice: "相处建议：每天给它准备一杯猫式咖啡，让它有精力继续为家庭奋斗。偶尔让它'罢工'一天，躺在沙发上当个懒猫。记得给它的小围裙绣上'家庭顶梁柱'四个大字！",
                conditions: { energetic: 45, social: 35, provider: 30 },
                rarity: "common"
            },
            {
                id: "friedChicken",
                title: "居家炸鸡腿",
                description: "你的猫咪是家里的装饰品兼炸鸡腿模型！它最大的特长就是躺着，偶尔翻个面。虽然看起来没什么用，但它为家庭氛围做出了巨大贡献——毕竟，谁能拒绝一只圆滚滚的'炸鸡腿'呢？",
                advice: "相处建议：给它准备一个舒适的'炸鸡腿专用垫'，定期给它'翻面'防止粘锅。记得每天夸它'今天炸得真均匀'，让它保持酥脆自信！",
                conditions: { lazy: 50, homebody: 40, foodie: 35 },
                rarity: "common"
            },
            {
                id: "sportsStudent",
                title: "黑皮体育生",
                description: "你的猫咪浑身散发着青春活力！它热爱运动，精力充沛，每天不是在跑酷就是在准备跑酷。虽然学习成绩可能不太理想，但体育方面绝对是佼佼者！",
                advice: "相处建议：给它准备一个小型健身房，包括跑步轮和攀爬架。每天陪它做'体能训练'，但记得在它运动后提供足够的营养补给——猫粮蛋白粉了解一下？",
                conditions: { energetic: 55, playful: 45, explorer: 35 },
                rarity: "common"
            },
            {
                id: "customsOfficer",
                title: "海关检查员",
                description: "你的猫咪对家里的所有物品都了如指掌！任何新东西都逃不过它的法眼，必须经过严格检查才能入境。它的口头禅是：'这个包裹安全吗？让我闻闻！'",
                advice: "相处建议：每次购物回家都要主动开箱接受检查，给它准备一个'海关专用印章'（无害的）。新物品入境前先让它'检疫'三天，确保没有危险气味！",
                conditions: { cautious: 55, observer: 45, independent: 35 },
                rarity: "common"
            },
            {
                id: "repairman",
                title: "万能维修师傅",
                description: "你的猫咪天生就是修东西的料！虽然它修过的东西通常会更坏，但这份热情值得鼓励。从窗帘到沙发，没有它不敢'维修'的家居用品。",
                advice: "相处建议：给它准备一个玩具工具箱，里面装满它可以随意'修理'的玩具。记得经常夸奖它的'维修技术'，即使它只是把东西抓得更烂了。",
                conditions: { explorer: 50, playful: 40, independent: 35 },
                rarity: "common"
            },
            {
                id: "programmer",
                title: "996程序员猫",
                description: "你的猫咪对电子设备有着特殊的兴趣！它喜欢在键盘上散步，偶尔还会帮你'写代码'。虽然它写的代码通常是一串乱码，但这份热情值得肯定。",
                advice: "相处建议：给它准备一个专属键盘（已断线），让它尽情'编程'。每天给它一杯'猫式咖啡'，陪它熬夜debug（抓bug）。记得定期带它做'颈椎保健操'！",
                conditions: { independent: 55, observer: 40, cautious: 35 },
                rarity: "common"
            },
            {
                id: "securityGuard",
                title: "小区保安队长",
                description: "你的猫咪是家里的安全负责人！它每天定时巡逻，检查门窗，确保没有可疑人员入侵。虽然工资不高（只有猫粮），但它工作非常认真。",
                advice: "相处建议：给它配备一个巡逻小车（玩具），定期'升职加薪'（换更好的猫粮）。每天晚上给它做工作汇报，告诉它'今日辖区平安无事'！",
                conditions: { cautious: 55, observer: 45, territorial: 35 },
                rarity: "common"
            },
            {
                id: "collegeStudent",
                title: "清澈愚蠢大学生",
                description: "你的猫咪有着大学生特有的单纯和呆萌！它看起来总是很困惑，做事毛手毛脚，但对世界充满好奇。虽然不太聪明，但非常可爱！",
                advice: "相处建议：给它准备一本《猫咪大学入学指南》，每天教它一个生活小常识（比如'猫粮不会自己跑进碗里'）。考试周记得给它准备'复习资料'（抓板）！",
                conditions: { playful: 50, social: 40, energetic: 35 },
                rarity: "common"
            },
            {
                id: "fisherman",
                title: "资深渔民",
                description: "你的猫咪有着捕鱼世家的血统！虽然生活在城市，但它对鱼类的热爱从未减退。浴缸里的玩具鱼是它的主要捕捞对象。",
                advice: "相处建议：给它准备一个'渔船'（纸箱），一根'钓竿'（逗猫棒）。每周举行'捕鱼大赛'，奖励最肥美的'鱼'（猫条）。记得教它'可持续发展'，不要过度捕捞！",
                conditions: { hunter: 60, observer: 40, cautious: 35 },
                rarity: "common"
            },
            {
                id: "model",
                title: "超模猫",
                description: "你的猫咪天生就是镜头前的明星！它姿态优雅，眼神迷人，随便一个姿势都能上杂志封面。缺点是有点自恋，经常对着镜子欣赏自己的美貌。",
                advice: "相处建议：在家开辟一个'摄影角'，用手机为它拍下每日OOTD。发朋友圈时务必配上它的'名言'，比如'喵生格言：优雅，永不过时'。它照镜子时，请自觉充当打光师。",
                conditions: { refined: 55, observer: 40, independent: 35 },
                rarity: "common"
            },
            {
                id: "spiderman",
                title: "邻居好帮手蜘蛛侠",
                description: "你的猫咪有着超凡的攀爬能力！窗帘、书架、门框都是它的游乐场。虽然偶尔会打碎东西，但它总是在努力帮助邻居（自认为）。",
                advice: "相处建议：在家里安装更多稳固的猫爬架，将它的攀爬天赋引导至正确方向。当它又不小心碰掉东西时，可以无奈地说：'没事，蜘蛛侠在拯救世界时也难免撞坏几栋楼。'",
                conditions: { energetic: 60, explorer: 50, playful: 40 },
                rarity: "common"
            },
            {
                id: "idol",
                title: "顶流爱豆猫",
                description: "你的猫咪天生就是舞台上的焦点！它喜欢被关注，享受掌声，偶尔还会开个'演唱会'（半夜嚎叫）。虽然粉丝不多（只有你一个人），但梦想很大。",
                advice: "相处建议：当它在你面前'喵喵'开演唱会时，请放下手机，充当它的全场观众，并适时献上掌声与'安可！'。但需协商好'演唱会'不能在工作日和深夜举行。",
                conditions: { social: 60, affectionate: 50, energetic: 35 },
                rarity: "common"
            },
            
            // ============ 稀有职业 (5个) ============
            {
                id: "spy",
                title: "隐藏的特务猫",
                description: "你的猫咪行踪诡秘，神出鬼没！你永远不知道它在想什么，也不知道它下一刻会出现在哪里。它可能正在执行某项秘密任务，而你只是它的掩护身份。",
                advice: "相处建议：不要试图找到它，它会自己选择现身时机。在家里多准备几个隐蔽的观察点，满足它的特务需求。偶尔放些'机密文件'（废纸团）让它调查。",
                conditions: { observer: 65, independent: 55, cautious: 45 },
                rarity: "rare"
            },
            {
                id: "assassin",
                title: "冷酷杀手猫",
                description: "你的猫咪眼神中透着一股杀气！它行动敏捷，出手精准，家里的蟑螂和小飞虫都难逃它的魔爪。虽然收费很高（要用高级猫粮支付），但业务能力一流。",
                advice: "相处建议：将它捕获的小飞虫、蟑螂视为'业绩'，并用高级猫粮或冻干作为'绩效奖金'。定期用逗猫棒进行'岗中培训'，维持它顶尖的业务水平。",
                conditions: { hunter: 70, energetic: 50, independent: 40 },
                rarity: "rare"
            },
            {
                id: "chef",
                title: "米其林大厨猫",
                description: "你的猫咪对食物有着极高的要求！它不仅要吃得好，还要吃得精致。偶尔会亲自'下厨'（把猫粮从碗里扒拉出来摆盘）。",
                advice: "相处建议：在给它摆盘猫粮时，稍微花点心思，比如将肉块堆成小塔，并恭敬地递上：'主厨，您看今天的摆盘可还满意？'如果它扒拉猫粮，就理解为'主厨正在调整菜品构图'。",
                conditions: { foodie: 70, refined: 50, independent: 40 },
                rarity: "rare"
            },
            {
                id: "detective",
                title: "名侦探猫",
                description: "你的猫咪有着敏锐的观察力和推理能力！家里任何微小的变化都逃不过它的眼睛。虽然破案率不高，但破案过程非常可爱。",
                advice: "相处建议：故意把一些小东西，比如发圈、瓶盖，放在显眼又古怪的地方，看它去调查。当它盯着某处看时，你可以配合地推理：'侦探大人，是否发现了什么新线索？'",
                conditions: { observer: 70, cautious: 55, independent: 45 },
                rarity: "rare"
            },
            {
                id: "archaeologist",
                title: "考古学家猫",
                description: "你的猫咪对家里的各个角落都充满好奇！它喜欢挖掘沙发底下、床底下等'考古遗址'，偶尔能发现失踪已久的玩具或零食。",
                advice: "相处建议：定期在沙发底、床下等它的'考古现场'，藏一些它喜欢但很久没玩的小玩具。当它叼出来时，就隆重宣布：'恭喜您，又发掘出一件失传的喵文明珍宝！'",
                conditions: { explorer: 70, observer: 50, playful: 45 },
                rarity: "rare"
            },
            
            // ============ 史诗职业 (3个) ============
            {
                id: "emperor",
                title: "猫皇帝",
                description: "你的猫咪天生就是统治者！它高傲、自信，认为整个世界都是它的领地。你只是它的仆人，负责提供食物和按摩服务。",
                advice: "相处建议：每天醒来第一件事和睡前最后一件事，就是向'陛下'请安。进贡猫粮和罐罐时，要双手奉上，并高呼：'请陛下用膳！'它若打翻水杯，要立刻上前：'是奴才放的位置不对，碍着陛下的龙爪了。'",
                conditions: { independent: 75, territorial: 55, refined: 45 },
                rarity: "epic"
            },
            {
                id: "footWarmer",
                title: "专业暖脚师傅",
                description: "你的猫咪是冬天的救星！它总是能找到最冷的脚，然后用自己的体温温暖它们。虽然服务范围有限（只服务自家人），但服务质量一流。",
                advice: "相处建议：在寒冷的夜晚，主动邀请它'上岗'。当它蜷缩在你脚边时，要真诚地道谢：'师傅技术真好，暖得快还恒温！'服务结束后，请用梳毛或按摩支付'报酬'。",
                conditions: { affectionate: 70, homebody: 60, lazy: 50 },
                rarity: "epic"
            },
            {
                id: "astronaut",
                title: "宇航员猫",
                description: "你的猫咪似乎来自外太空！它行为古怪，眼神深邃，偶尔会盯着天空发呆。也许它正在思念自己的母星。",
                advice: "相处建议：把猫包或航空箱称为'返回舱'，在带它出门前，严肃地通知：'宇航员同志，我们即将执行一次秘密太空任务。'它望着窗外发呆时，就陪它一起'观测外星风景'。",
                conditions: { observer: 75, independent: 60, cautious: 50 },
                rarity: "epic"
            },
            
            // ============ 传说职业 (1个) ============
            {
                id: "timeTraveler",
                title: "时间旅行者猫",
                description: "你的猫咪似乎能穿越时空！它时而表现得像只小奶猫，时而又像个老谋深算的长者。也许它真的来自不同的时间线。",
                advice: "相处建议：当它突然像小猫一样玩耍打滚，你可以配合演出：'欢迎回到童年时代！'当它沉稳地凝视远方，你便感慨：'看来是位来自未来的智者。'接受它时而幼稚，时而成熟的'时空错乱'行为。",
                conditions: { observer: 80, independent: 65, cautious: 55 },
                rarity: "legendary"
            }
        ];

        // DOM 元素
        const startContainer = document.getElementById('start-screen');
        const questionContainer = document.getElementById('question-screen');
        const resultContainer = document.getElementById('result-screen');
        const questionText = document.getElementById('question-text');
        const questionCounter = document.getElementById('question-counter');
        const optionsContainer = document.getElementById('options-container');
        const nextBtn = document.getElementById('next-btn');
        const prevBtn = document.getElementById('prev-btn');
        const progressBar = document.getElementById('progress');
        const resultTitle = document.getElementById('result-job-title');
        const resultDescription = document.getElementById('result-description');
        const resultImage = document.getElementById('result-image');
        const resultRarity = document.getElementById('result-rarity');
        const resultAdvice = document.getElementById('result-advice');
        const rarityExplanation = document.getElementById('rarity-explanation');
        const startBtn = document.getElementById('start-btn');
        const restartBtn = document.getElementById('restart-btn');

        // 事件监听
        startBtn.addEventListener('click', startTest);
        nextBtn.addEventListener('click', nextQuestion);
        prevBtn.addEventListener('click', prevQuestion);
        restartBtn.addEventListener('click', restartTest);

        // 开始测试
        function startTest() {
            initializeScores();
            startContainer.style.display = 'none';
            questionContainer.style.display = 'block';
            showQuestion();
        }

        // 显示当前问题
        function showQuestion() {
            try {
                const currentQuestion = questions[currentQuestionIndex];
                if (!currentQuestion) {
                    throw new Error('题目数据不存在');
                }
                
                questionText.textContent = currentQuestion.question;
                optionsContainer.innerHTML = '';
            
                // 更新题目序号
                questionCounter.textContent = `第 ${currentQuestionIndex + 1} 题 / 共 ${questions.length} 题`;
                
                // 检查是否有之前的选择
                selectedOptionIndex = userChoices[currentQuestionIndex];
                nextBtn.disabled = (selectedOptionIndex === null);

                // 更新进度条
                const progress = ((currentQuestionIndex) / questions.length) * 100;
                progressBar.style.width = `${progress}%`;

                // 更新上一题按钮状态
                prevBtn.disabled = (currentQuestionIndex === 0);

                // 创建选项
                currentQuestion.options.forEach((option, index) => {
                    const optionElement = document.createElement('div');
                    optionElement.className = 'option';
                    if (index === selectedOptionIndex) {
                        optionElement.classList.add('selected');
                    }
                    optionElement.textContent = option.text;
                    optionElement.addEventListener('click', () => selectOption(index));
                    optionsContainer.appendChild(optionElement);
                });
            } catch (error) {
                console.error('显示题目时出错:', error);
                questionContainer.innerHTML = '<div style="text-align: center; padding: 40px;"><p>抱歉，页面加载出现问题</p><button class="btn" onclick="restartTest()">重新开始测试</button></div>';
            }
        }

        // 选择选项
        function selectOption(index) {
            // 移除之前的选择
            const options = document.querySelectorAll('.option');
            options.forEach(option => option.classList.remove('selected'));
            
            // 标记当前选择
            options[index].classList.add('selected');
            selectedOptionIndex = index;
            nextBtn.disabled = false;
            
            // 保存用户选择
            userChoices[currentQuestionIndex] = index;
        }

        // 下一题
        function nextQuestion() {
            if (selectedOptionIndex === null) return;

            // 记录分数
            const currentQuestion = questions[currentQuestionIndex];
            const selectedOption = currentQuestion.options[selectedOptionIndex];
            
            for (const trait in selectedOption.scores) {
                userScores[trait] += selectedOption.scores[trait];
            }

            // 前进到下一题或显示结果
            currentQuestionIndex++;
            if (currentQuestionIndex < questions.length) {
                showQuestion();
            } else {
                showResult();
            }
        }

        // 上一题
        function prevQuestion() {
            if (currentQuestionIndex === 0) return;
            
            // 撤销当前题目的分数
            const currentQuestion = questions[currentQuestionIndex];
            const selectedOptionIndex = userChoices[currentQuestionIndex];
            
            if (selectedOptionIndex !== null) {
                const selectedOption = currentQuestion.options[selectedOptionIndex];
                for (const trait in selectedOption.scores) {
                    userScores[trait] -= selectedOption.scores[trait];
                }
            }
            
            // 回到上一题
            currentQuestionIndex--;
            showQuestion();
        }

        // 显示结果
        function showResult() {
            try {
                questionContainer.style.display = 'none';
                resultContainer.style.display = 'block';

                // 计算最适合的职业
                const bestMatch = findBestMatch();
                
                if (!bestMatch) {
                    throw new Error('无法计算结果');
                }
            
                // 显示结果
                resultTitle.textContent = bestMatch.title;
                resultDescription.textContent = bestMatch.description;
                resultAdvice.textContent = bestMatch.advice;
            
                // 设置稀有度显示
                let rarityText = "";
                let explanationText = "";
            
                switch(bestMatch.rarity) {
                    case "common":
                        rarityText = "常见职业";
                        resultRarity.className = "rarity-badge rarity-common";
                        explanationText = "大约57%的猫咪会获得此类职业";
                        break;
                    case "rare":
                        rarityText = "稀有职业";
                        resultRarity.className = "rarity-badge rarity-rare";
                        explanationText = "大约24%的猫咪会获得此类职业";
                        break;
                    case "epic":
                        rarityText = "史诗职业";
                        resultRarity.className = "rarity-badge rarity-epic";
                        explanationText = "只有14%的猫咪会获得此类职业";
                        break;
                    case "legendary":
                        rarityText = "传说职业";
                        resultRarity.className = "rarity-badge rarity-legendary";
                        explanationText = "仅有5%的猫咪会获得此类职业！恭喜！";
                        break;
                }
                resultRarity.textContent = rarityText;
                rarityExplanation.textContent = explanationText;
            
                // 设置结果图片
                resultImage.style.backgroundImage = `url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path d="M50,20 C65,20 75,30 75,45 C75,60 65,70 50,70 C35,70 25,60 25,45 C25,30 35,20 50,20 Z" fill="%23ffb6c1"/><circle cx="40" cy="40" r="5" fill="%235a4a3a"/><circle cx="60" cy="40" r="5" fill="%235a4a3a"/><path d="M45,50 Q50,55 55,50" stroke="%235a4a3a" stroke-width="2" fill="none"/><path d="M35,15 Q40,5 50,5 Q60,5 65,15" stroke="%235a4a3a" stroke-width="2" fill="none"/><path d="M30,30 Q20,25 15,30" stroke="%235a4a3a" stroke-width="2" fill="none"/><path d="M70,30 Q80,25 85,30" stroke="%235a4a3a" stroke-width="2" fill="none"/></svg>')`;

                // 设置分享功能
                setupShareButtons(bestMatch);
                
            } catch (error) {
                console.error('显示结果时出错:', error);
                resultContainer.innerHTML = '<div style="text-align: center; padding: 40px;"><p>抱歉，计算结果显示失败</p><button class="btn" onclick="restartTest()">重新开始测试</button></div>';
            }
        }

        // 分享功能函数
        function setupShareButtons(result) {
            const shareUrl = window.location.href;
            const shareText = `我的猫咪竟然是${result.title}！${result.description.substring(0, 30)}... 快来看看你家主子的隐藏职业吧！`;
    
            document.getElementById('wechat-share').addEventListener('click', function() {
                // 微信分享提示
                alert('请点击浏览器右上角分享到微信朋友圈或好友\n\n分享文案：' + shareText);
            });
    
            document.getElementById('weibo-share').addEventListener('click', function() {
                // 微博分享
                const weiboUrl = `https://service.weibo.com/share/share.php?url=${encodeURIComponent(shareUrl)}&title=${encodeURIComponent(shareText)}`;
                window.open(weiboUrl, '_blank');
            });
        }

        // 重新开始测试
        function restartTest() {
            currentQuestionIndex = 0;
            userScores = {};
            selectedOptionIndex = null;
            userChoices = [];
            
            resultContainer.style.display = 'none';
            startContainer.style.display = 'block';
        }
    </script>
</body>
</html>
