# Laitao.github.io
NICE
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CATL奋斗主题页面</title>
    <style>
        /* 页面基础样式 */
        body {
            font-family: "Microsoft Yahei", sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
            background-color: #f5f5f5;
            padding: 20px;
        }

        /* 点击链接样式 */
        .trigger-link {
            font-size: 20px;
            color: #0066cc;
            text-decoration: none;
            cursor: pointer;
            transition: color 0.3s;
            margin-bottom: 20px;
        }

        .trigger-link:hover {
            color: #004999;
            text-decoration: underline;
        }

        /* 奋斗内容容器（默认隐藏） */
        .fight-content {
            display: none;
            text-align: center;
            max-width: 500px;
            width: 100%;
        }

        /* 彩色渐变文字通用样式 */
        .color-text {
            font-weight: bold;
            /* 彩色渐变核心样式 */
            background: linear-gradient(90deg, #e63946, #f77f00, #fcbf49, #43aa8b, #577590, #0066cc, #9381ff);
            background-size: 400% 100%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-fill-color: transparent;
            /* 动画效果：渐变色彩流动 */
            animation: gradientMove 8s linear infinite;
            line-height: 1.5;
        }

        /* 主标语样式 */
        .main-text {
            font-size: 32px;
            margin-bottom: 15px;
        }

        /* 副标语样式 */
        .sub-text {
            font-size: 28px;
            margin-bottom: 20px;
            /* 默认隐藏，第二次点击显示 */
            display: none;
            letter-spacing: 8px; /* 增加字间距，更美观 */
        }

        /* 渐变流动动画 */
        @keyframes gradientMove {
            0% {
                background-position: 0% 50%;
            }
            100% {
                background-position: 100% 50%;
            }
        }

        /* 动图样式 */
        .fight-gif {
            width: 100%;
            max-width: 400px;
            height: auto;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>
    <!-- 点击触发的链接 -->
    <a class="trigger-link" id="triggerLink">点击查看CATL奋斗宣言</a>

    <!-- 奋斗内容容器（点击后显示） -->
    <div class="fight-content" id="fightContent">
        <div class="color-text main-text">为CATL奋斗终生！</div>
        <div class="color-text sub-text" id="subText">修己、达人、奋斗、创新</div>
        <!-- 替换为你想要的奋斗动图链接 -->
        <img src="https://tse4.mm.bing.net/th/id/OIP._3pRbcPYM78Ib0oeQGzkiAHaEK?rs=1&pid=ImgDetMain&o=7&rm=3" alt="奋斗动图" class="fight-gif">
    </div>

    <script>
        // 获取页面元素
        const triggerLink = document.getElementById('triggerLink');
        const fightContent = document.getElementById('fightContent');
        const subText = document.getElementById('subText');
        
        // 记录点击次数
        let clickCount = 0;

        // 点击链接分步显示内容
        triggerLink.addEventListener('click', function(e) {
            e.preventDefault(); // 阻止链接默认跳转
            clickCount++; // 点击次数+1

            // 第一次点击：显示主内容（主标语+动图）
            if (clickCount === 1) {
                fightContent.style.display = 'block';
                // 平滑滚动到内容位置
                fightContent.scrollIntoView({ behavior: 'smooth' });
            }
            // 第二次点击：显示副标语
            else if (clickCount === 2) {
                subText.style.display = 'block';
            }
            // 可选：多次点击后重置（如需循环显示可保留，不需要可删除）
            // else {
            //     clickCount = 0;
            //     fightContent.style.display = 'none';
            //     subText.style.display = 'none';
            // }
        });
    </script>
</body>
</html>
