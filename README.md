# web-20251019
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML主要标签展示</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1e3c72, #2a5298);
            color: #333;
            line-height: 1.6;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            background-color: rgba(255, 255, 255, 0.95);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            margin-bottom: 30px;
        }
        
        h1 {
            color: #1e3c72;
            font-size: 2.8rem;
            margin-bottom: 10px;
        }
        
        .subtitle {
            color: #666;
            font-size: 1.3rem;
            margin-bottom: 20px;
        }
        
        .intro {
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto;
            color: #444;
        }
        
        .nav-tabs {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 30px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
        }
        
        .tab-btn {
            background: none;
            border: none;
            padding: 12px 20px;
            margin: 5px;
            font-size: 1rem;
            cursor: pointer;
            border-radius: 8px;
            transition: all 0.3s;
            color: #1e3c72;
            font-weight: 600;
        }
        
        .tab-btn:hover {
            background-color: #e9ecef;
        }
        
        .tab-btn.active {
            background-color: #1e3c72;
            color: white;
        }
        
        .content-section {
            display: none;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 30px;
        }
        
        .content-section.active {
            display: block;
        }
        
        .section-title {
            color: #1e3c72;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #e9ecef;
            font-size: 1.8rem;
        }
        
        .tag-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .tag-card {
            background-color: #f8f9fa;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s;
            border-left: 5px solid #1e3c72;
        }
        
        .tag-card:hover {
            transform: translateY(-5px);
        }
        
        .tag-name {
            font-size: 1.4rem;
            color: #1e3c72;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }
        
        .tag-name code {
            background-color: #e9ecef;
            padding: 3px 8px;
            border-radius: 4px;
            font-family: monospace;
            margin-right: 10px;
        }
        
        .tag-description {
            margin-bottom: 15px;
            color: #555;
        }
        
        .tag-example {
            background-color: #2c3e50;
            color: #ecf0f1;
            padding: 15px;
            border-radius: 8px;
            font-family: monospace;
            overflow-x: auto;
            margin-top: 10px;
        }
        
        .tag-example code {
            white-space: pre;
        }
        
        .tag-attributes {
            margin-top: 15px;
            font-size: 0.9rem;
        }
        
        .tag-attributes h4 {
            color: #1e3c72;
            margin-bottom: 8px;
        }
        
        .tag-attributes ul {
            padding-left: 20px;
        }
        
        .tag-attributes li {
            margin-bottom: 5px;
        }
        
        .demo-area {
            background-color: #f8f9fa;
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
            border: 1px solid #e9ecef;
        }
        
        .demo-title {
            font-size: 1.2rem;
            color: #1e3c72;
            margin-bottom: 10px;
        }
        
        footer {
            text-align: center;
            background-color: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 15px;
            color: #666;
            margin-top: 30px;
        }
        
        @media (max-width: 768px) {
            .tag-grid {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .nav-tabs {
                flex-direction: column;
            }
            
            .tab-btn {
                width: 100%;
                margin: 5px 0;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>HTML主要标签展示</h1>
            <p class="subtitle">学习HTML基本结构与常用标签</p>
            <p class="intro">HTML（超文本标记语言）是构建网页的基础。本页面展示了HTML中最常用的标签及其用法示例。</p>
        </header>
        
        <div class="nav-tabs">
            <button class="tab-btn active" data-tab="structure">结构标签</button>
            <button class="tab-btn" data-tab="text">文本标签</button>
            <button class="tab-btn" data-tab="media">媒体标签</button>
            <button class="tab-btn" data-tab="forms">表单标签</button>
            <button class="tab-btn" data-tab="semantic">语义化标签</button>
        </div>
        
        <!-- 结构标签部分 -->
        <section id="structure" class="content-section active">
            <h2 class="section-title">HTML结构标签</h2>
            <div class="tag-grid">
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;html&gt;</code>根元素</h3>
                    <p class="tag-description">定义HTML文档的根元素，包含整个HTML内容。</p>
                    <div class="tag-example">
                        <code>&lt;html&gt;
  &lt;head&gt;...&lt;/head&gt;
  &lt;body&gt;...&lt;/body&gt;
&lt;/html&gt;</code>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;head&gt;</code>头部</h3>
                    <p class="tag-description">包含文档的元数据，如标题、字符集、样式表和脚本链接。</p>
                    <div class="tag-example">
                        <code>&lt;head&gt;
  &lt;title&gt;页面标题&lt;/title&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;link rel="stylesheet" href="style.css"&gt;
&lt;/head&gt;</code>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;body&gt;</code>主体</h3>
                    <p class="tag-description">包含所有在网页上显示的内容，如文本、图像、链接等。</p>
                    <div class="tag-example">
                        <code>&lt;body&gt;
  &lt;h1&gt;我的网页&lt;/h1&gt;
  &lt;p&gt;这是我的第一个网页。&lt;/p&gt;
&lt;/body&gt;</code>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;div&gt;</code>分区</h3>
                    <p class="tag-description">用于分组内容的通用容器，常用于布局和样式化。</p>
                    <div class="tag-example">
                        <code>&lt;div class="container"&gt;
  &lt;h2&gt;标题&lt;/h2&gt;
  &lt;p&gt;段落内容&lt;/p&gt;
&lt;/div&gt;</code>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- 文本标签部分 -->
        <section id="text" class="content-section">
            <h2 class="section-title">HTML文本标签</h2>
            <div class="tag-grid">
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;h1&gt;-&lt;h6&gt;</code>标题</h3>
                    <p class="tag-description">定义标题，h1是最高级标题，h6是最低级标题。</p>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <h1>h1 标题</h1>
                        <h2>h2 标题</h2>
                        <h3>h3 标题</h3>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;p&gt;</code>段落</h3>
                    <p class="tag-description">定义文本段落，浏览器会自动在段落前后添加空白。</p>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <p>这是一个段落。HTML是构建网页的基础语言。</p>
                        <p>这是另一个段落。CSS用于样式化网页。</p>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;a&gt;</code>链接</h3>
                    <p class="tag-description">创建超链接，用于链接到其他页面或位置。</p>
                    <div class="tag-attributes">
                        <h4>常用属性：</h4>
                        <ul>
                            <li><strong>href</strong>: 指定链接目标URL</li>
                            <li><strong>target</strong>: 指定如何打开链接</li>
                        </ul>
                    </div>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <p>访问<a href="https://www.example.com" target="_blank">示例网站</a></p>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;ul&gt;/&lt;ol&gt;</code>列表</h3>
                    <p class="tag-description">创建无序列表(ul)或有序列表(ol)，列表项使用&lt;li&gt;标签。</p>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <p>无序列表：</p>
                        <ul>
                            <li>项目一</li>
                            <li>项目二</li>
                            <li>项目三</li>
                        </ul>
                        <p>有序列表：</p>
                        <ol>
                            <li>第一步</li>
                            <li>第二步</li>
                            <li>第三步</li>
                        </ol>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- 媒体标签部分 -->
        <section id="media" class="content-section">
            <h2 class="section-title">HTML媒体标签</h2>
            <div class="tag-grid">
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;img&gt;</code>图像</h3>
                    <p class="tag-description">用于在网页中嵌入图像。</p>
                    <div class="tag-attributes">
                        <h4>常用属性：</h4>
                        <ul>
                            <li><strong>src</strong>: 图像URL</li>
                            <li><strong>alt</strong>: 替代文本</li>
                            <li><strong>width/height</strong>: 图像尺寸</li>
                        </ul>
                    </div>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <img src="https://via.placeholder.com/150" alt="示例图像" width="150" height="150">
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;audio&gt;</code>音频</h3>
                    <p class="tag-description">用于在网页中嵌入音频内容。</p>
                    <div class="tag-attributes">
                        <h4>常用属性：</h4>
                        <ul>
                            <li><strong>src</strong>: 音频文件URL</li>
                            <li><strong>controls</strong>: 显示控制界面</li>
                            <li><strong>autoplay</strong>: 自动播放</li>
                        </ul>
                    </div>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <audio controls>
                            <source src="#" type="audio/mpeg">
                            您的浏览器不支持音频元素。
                        </audio>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;video&gt;</code>视频</h3>
                    <p class="tag-description">用于在网页中嵌入视频内容。</p>
                    <div class="tag-attributes">
                        <h4>常用属性：</h4>
                        <ul>
                            <li><strong>src</strong>: 视频文件URL</li>
                            <li><strong>controls</strong>: 显示控制界面</li>
                            <li><strong>width/height</strong>: 视频尺寸</li>
                        </ul>
                    </div>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <video width="320" height="240" controls>
                            <source src="#" type="video/mp4">
                            您的浏览器不支持视频元素。
                        </video>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- 表单标签部分 -->
        <section id="forms" class="content-section">
            <h2 class="section-title">HTML表单标签</h2>
            <div class="tag-grid">
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;form&gt;</code>表单</h3>
                    <p class="tag-description">创建包含输入元素的表单，用于收集用户输入。</p>
                    <div class="tag-attributes">
                        <h4>常用属性：</h4>
                        <ul>
                            <li><strong>action</strong>: 表单提交的URL</li>
                            <li><strong>method</strong>: 提交方法(GET/POST)</li>
                        </ul>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;input&gt;</code>输入</h3>
                    <p class="tag-description">创建各种类型的输入字段。</p>
                    <div class="tag-attributes">
                        <h4>常用type值：</h4>
                        <ul>
                            <li><strong>text</strong>: 文本输入</li>
                            <li><strong>password</strong>: 密码输入</li>
                            <li><strong>email</strong>: 邮箱输入</li>
                            <li><strong>checkbox</strong>: 复选框</li>
                            <li><strong>radio</strong>: 单选按钮</li>
                        </ul>
                    </div>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <form>
                            <p>文本: <input type="text" placeholder="输入文本"></p>
                            <p>密码: <input type="password" placeholder="输入密码"></p>
                            <p>邮箱: <input type="email" placeholder="输入邮箱"></p>
                            <p>复选框: 
                                <input type="checkbox" id="check1">
                                <label for="check1">选项1</label>
                                <input type="checkbox" id="check2">
                                <label for="check2">选项2</label>
                            </p>
                        </form>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;textarea&gt;</code>文本区域</h3>
                    <p class="tag-description">创建多行文本输入区域。</p>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <textarea rows="4" cols="40" placeholder="请输入多行文本..."></textarea>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;select&gt;</code>下拉列表</h3>
                    <p class="tag-description">创建下拉选择列表。</p>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <select>
                            <option value="option1">选项一</option>
                            <option value="option2">选项二</option>
                            <option value="option3">选项三</option>
                        </select>
                    </div>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;button&gt;</code>按钮</h3>
                    <p class="tag-description">创建可点击的按钮。</p>
                    <div class="demo-area">
                        <div class="demo-title">示例效果：</div>
                        <button type="button">普通按钮</button>
                        <button type="submit">提交按钮</button>
                        <button type="reset">重置按钮</button>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- 语义化标签部分 -->
        <section id="semantic" class="content-section">
            <h2 class="section-title">HTML语义化标签</h2>
            <div class="tag-grid">
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;header&gt;</code>页眉</h3>
                    <p class="tag-description">定义文档或节的页眉，通常包含介绍性内容或导航链接。</p>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;nav&gt;</code>导航</h3>
                    <p class="tag-description">定义导航链接的部分。</p>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;main&gt;</code>主体</h3>
                    <p class="tag-description">定义文档的主要内容。</p>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;section&gt;</code>章节</h3>
                    <p class="tag-description">定义文档中的节，如章节、页眉、页脚等。</p>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;article&gt;</code>文章</h3>
                    <p class="tag-description">定义独立的自包含内容，如博客文章、新闻文章等。</p>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;aside&gt;</code>侧边</h3>
                    <p class="tag-description">定义与主要内容相关但不是主要内容一部分的内容。</p>
                </div>
                
                <div class="tag-card">
                    <h3 class="tag-name"><code>&lt;footer&gt;</code>页脚</h3>
                    <p class="tag-description">定义文档或节的页脚，通常包含版权信息、联系信息等。</p>
                </div>
            </div>
        </section>
        
        <footer>
            <p>HTML标签展示页面 &copy; 2023 | 学习HTML，构建更好的网页</p>
        </footer>
    </div>

    <script>
        // 标签切换功能
        document.addEventListener('DOMContentLoaded', function() {
            const tabBtns = document.querySelectorAll('.tab-btn');
            const contentSections = document.querySelectorAll('.content-section');
            
            tabBtns.forEach(btn => {
                btn.addEventListener('click', function() {
                    // 移除所有活动类
                    tabBtns.forEach(b => b.classList.remove('active'));
                    contentSections.forEach(section => section.classList.remove('active'));
                    
                    // 添加活动类到当前按钮
                    this.classList.add('active');
                    
                    // 显示对应内容区域
                    const tabId = this.getAttribute('data-tab');
                    document.getElementById(tabId).classList.add('active');
                });
            });
        });
    </script>
</body>
</html>
