<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <!-- 移动端自适应 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的通用网站</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Microsoft YaHei", sans-serif;
        }
        /* 导航栏 */
        nav {
            background: #2c3e50;
            color: #fff;
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 99;
        }
        .logo {
            font-size: 24px;
            font-weight: bold;
        }
        .nav-links a {
            color: white;
            text-decoration: none;
            margin-left: 25px;
            font-size: 16px;
            transition: color 0.3s;
        }
        .nav-links a:hover {
            color: #3498db;
        }
        /* 首屏横幅 */
        .banner {
            height: 85vh;
            background: linear-gradient(rgba(0,0,0,0.5),rgba(0,0,0,0.5)), #3498db;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            text-align: center;
            padding: 0 20px;
        }
        .banner h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        .banner p {
            font-size: 18px;
            max-width: 600px;
            margin-bottom: 30px;
            line-height: 1.8;
        }
        .btn {
            padding: 14px 36px;
            background: #e74c3c;
            color: white;
            text-decoration: none;
            border-radius: 6px;
            font-size: 17px;
            transition: background 0.3s;
        }
        .btn:hover {
            background: #c0392b;
        }
        /* 通用区块样式 */
        section {
            padding: 80px 5%;
        }
        .section-title {
            text-align: center;
            font-size: 34px;
            color: #2c3e50;
            margin-bottom: 60px;
        }
        /* 服务卡片区域 */
        .service-wrap {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        .service-card {
            background: #f8f9fa;
            padding: 40px 25px;
            text-align: center;
            border-radius: 10px;
            transition: transform 0.3s;
        }
        .service-card:hover {
            transform: translateY(-8px);
        }
        .service-card h3 {
            font-size: 22px;
            color: #2c3e50;
            margin: 15px 0;
        }
        .service-card p {
            color: #666;
            line-height: 1.7;
        }
        /* 关于我们 */
        .about {
            background: #ecf0f1;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 40px;
        }
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        .about-text h2 {
            font-size: 32px;
            color: #2c3e50;
            margin-bottom: 20px;
        }
        .about-text p {
            color: #555;
            line-height: 1.9;
            font-size: 16px;
        }
        /* 联系表单 */
        .contact-form {
            max-width: 700px;
            margin: 0 auto;
        }
        .form-item {
            margin-bottom: 22px;
        }
        .form-item input, .form-item textarea {
            width: 100%;
            padding: 14px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
            outline: none;
        }
        .form-item input:focus, .form-item textarea:focus {
            border-color: #3498db;
        }
        textarea {
            min-height: 150px;
            resize: vertical;
        }
        .submit-btn {
            width: 100%;
            padding: 15px;
            border: none;
            background: #3498db;
            color: white;
            font-size: 18px;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s;
        }
        .submit-btn:hover {
            background: #2980b9;
        }
        /* 页脚 */
        footer {
            background: #2c3e50;
            color: #bdc3c7;
            text-align: center;
            padding: 30px;
        }
        /* 移动端适配 */
        @media (max-width:768px) {
            .nav-links {
                display: none;
            }
            .banner h1 {
                font-size: 32px;
            }
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <nav>
        <div class="logo">我的网站</div>
        <div class="nav-links">
            <a href="#home">首页</a>
            <a href="#service">服务</a>
            <a href="#about">关于</a>
            <a href="#contact">联系我们</a>
        </div>
    </nav>

    <!-- 首屏 -->
    <div class="banner" id="home">
        <h1>欢迎来到我的演示网站</h1>
        <p>这是一套完整自适应企业官网模板，包含导航、服务展示、介绍、留言表单，无需引入外部资源，纯原生前端代码，修改文字即可直接使用。</p>
        <a href="#contact" class="btn">立即咨询</a>
    </div>

    <!-- 服务板块 -->
    <section id="service">
        <h2 class="section-title">我们的服务</h2>
        <div class="service-wrap">
            <div class="service-card">
                <h3>网站开发</h3>
                <p>定制企业官网、商城、后台管理系统，响应式适配手机电脑，代码规范易维护。</p>
            </div>
            <div class="service-card">
                <h3>UI界面设计</h3>
                <p>专业页面视觉设计、小程序界面、APP原型设计，简约高级风格。</p>
            </div>
            <div class="service-card">
                <h3>技术维护</h3>
                <p>网站安全防护、bug修复、服务器部署、定期内容更新维护。</p>
            </div>
        </div>
    </section>

    <!-- 关于我们 -->
    <section class="about" id="about">
        <div class="about-text">
            <h2>关于本站</h2>
            <p>本网页使用原生 HTML + CSS + JavaScript 编写，无第三方框架依赖，加载速度快，兼容所有主流浏览器。页面做了完整移动端适配，手机打开自动调整布局。
            <br><br>
            你可以自由修改文字、颜色、按钮、板块内容，适合用作个人展示站、小型企业官网、作品集页面。底部留言表单可搭配后端实现消息提交功能。
            </p>
        </div>
    </section>

    <!-- 联系表单 -->
    <section id="contact">
        <h2 class="section-title">在线留言</h2>
        <form class="contact-form" id="msgForm">
            <div class="form-item">
                <input type="text" placeholder="请输入您的姓名" required>
            </div>
            <div class="form-item">
                <input type="tel" placeholder="请输入联系电话" required>
            </div>
            <div class="form-item">
                <input type="email" placeholder="请输入邮箱">
            </div>
            <div class="form-item">
                <textarea placeholder="请输入留言内容"></textarea>
            </div>
            <button class="submit-btn" type="submit">提交留言</button>
        </form>
    </section>

    <!-- 页脚 -->
    <footer>
        <p>© 2026 我的演示网站 版权所有 | 前端原生网页模板</p>
    </footer>

    <!-- 简单JS交互 -->
    <script>
        // 表单提交弹窗提示
        const form = document.getElementById('msgForm');
        form.addEventListener('submit', function(e){
            e.preventDefault(); // 阻止默认刷新
            alert('留言提交成功！我们会尽快联系您');
            form.reset(); // 清空表单
        })

        // 平滑滚动（点击导航跳转）
        document.querySelectorAll('.nav-links a').forEach(item => {
            item.addEventListener('click', function(e){
                e.preventDefault();
                const targetId = this.getAttribute('href');
                document.querySelector(targetId).scrollIntoView({
                    behavior: 'smooth'
                })
            })
        })
    </script>
</body>
</html>
