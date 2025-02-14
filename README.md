<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>苏州中学动植物介绍地图</title>
    <style>
        /* 通用样式 */
        body {
            font-family: "Arial", sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
            color: #333;
        }

        h1 {
            text-align: center;
            margin: 20px 0;
            color: #0056b3;
        }

        /* 导航栏样式 */
        .navbar {
            background-color: #0056b3;
            padding: 10px 0;
            text-align: center;
        }

        .navbar a {
            color: #fff;
            text-decoration: none;
            margin: 0 15px;
            font-size: 16px;
        }

        .navbar a:hover {
            text-decoration: underline;
        }

        /* 地图容器样式 */
        #school-map-container {
            position: relative;
            max-width: 800px;
            margin: 20px auto;
            border: 2px solid #ddd;
            border-radius: 10px;
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .map-image {
            width: 100%;
            border-radius: 10px;
        }

        /* 高亮区域样式 */
        .highlight {
            position: absolute;
            background-color: rgba(255, 223, 0, 0.5);
            pointer-events: none;
            display: none;
            border-radius: 50%;
        }

        /* 页脚样式 */
        .footer {
            text-align: center;
            padding: 10px;
            background-color: #0056b3;
            color: #fff;
            margin-top: 20px;
            font-size: 14px;
        }
    </style>
    <script>
        function highlightArea(id) {
            document.getElementById(id).style.display = 'block';
        }

        function resetHighlight(id) {
            document.getElementById(id).style.display = 'none';
        }
    </script>
</head>

<body>

    <!-- 导航栏 -->
    <div class="navbar">
        <a href="index.html">首页</a>
        <a href="map.html">校园地图</a>
        <a href="about.html">关于我们</a>
        <a href="contact.html">联系我们</a>
    </div>

    <!-- 页面标题 -->
    <h1>苏州中学动植物介绍地图</h1>

    <!-- 地图容器 -->
    <div id="school-map-container">
        <img src="/static/school_map.jpg" alt="苏州中学地图" class="map-image" usemap="#school-map">

        <!-- 定义高亮区域 -->
        <div id="highlight-2" class="highlight" style="top: 190px; left: 180px; width: 120px; height: 120px;"></div>
    </div>

    <!-- 地图点击区域 -->
    <map name="school-map">
        <area shape="circle" coords="240,250,60" alt="2" href="2.html" target="_blank" onmouseover="highlightArea('highlight-2')" onmouseout="resetHighlight('highlight-2')">
    </map>

    <!-- 页脚 -->
    <div class="footer">
        版权所有 © 2024 苏州中学 | 技术支持：SevenLiu,AmilyFan,JasonYu
    </div>

</body>

</html>
