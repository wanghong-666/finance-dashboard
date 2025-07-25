# finance-dashboard
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>会计行业商业智能数据分析平台</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.8/dist/chart.umd.min.js"></script>
  
  <!-- Tailwind 配置 -->
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: '#165DFF',
            secondary: '#36CFC9',
            success: '#52C41A',
            warning: '#FAAD14',
            danger: '#FF4D4F',
            neutral: {
              100: '#F5F7FA',
              200: '#E5E6EB',
              300: '#C9CDD4',
              400: '#86909C',
              500: '#4E5969',
              600: '#272E3B',
              700: '#1D2129',
            }
          },
          fontFamily: {
            sans: ['Inter', 'system-ui', 'sans-serif'],
          },
        },
      }
    }
  </script>
  
  <style type="text/tailwindcss">
    @layer utilities {
      .content-auto {
        content-visibility: auto;
      }
      .table-shadow {
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
      }
      .card-hover {
        transition: all 0.3s ease;
      }
      .card-hover:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 25px rgba(22, 93, 255, 0.1);
      }
    }
  </style>
</head>
<body class="bg-neutral-100 font-sans text-neutral-700">
  <!-- 顶部导航栏 -->
  <header class="bg-white shadow-sm sticky top-0 z-50 transition-all duration-300">
    <div class="container mx-auto px-4 py-4 flex justify-between items-center">
      <div class="flex items-center space-x-2">
        <i class="fa fa-bar-chart text-primary text-2xl"></i>
        <h1 class="text-xl font-bold text-neutral-700">财务商业智能分析平台</h1>
      </div>
      
      <div class="hidden md:flex items-center space-x-6">
        <a href="#" class="text-primary font-medium border-b-2 border-primary pb-1">数据分析</a>
        <a href="#" class="text-neutral-500 hover:text-primary transition-colors">流程优化</a>
        <a href="#" class="text-neutral-500 hover:text-primary transition-colors">决策支持</a>
        <a href="#" class="text-neutral-500 hover:text-primary transition-colors">风险控制</a>
      </div>
      
      <div class="flex items-center space-x-4">
        <button class="hidden md:block bg-primary/10 hover:bg-primary/20 text-primary px-4 py-2 rounded-lg transition-colors">
          <i class="fa fa-download mr-1"></i> 导出报告
        </button>
        <button class="md:hidden text-neutral-500 hover:text-primary">
          <i class="fa fa-bars text-xl"></i>
        </button>
      </div>
    </div>
  </header>

  <main class="container mx-auto px-4 py-8">
    <!-- 页面标题 -->
    <div class="mb-8">
      <h2 class="text-[clamp(1.5rem,3vw,2.5rem)] font-bold text-neutral-700 mb-2">会计行业商业智能实战分析</h2>
      <p class="text-neutral-500">财务数据分析与决策支持 | 企业财务流程优化评估</p>
    </div>
    
    <!-- 核心指标概览 -->
    <section class="mb-10">
      <h3 class="text-lg font-semibold mb-4 text-neutral-700">核心绩效指标</h3>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <!-- 指标卡片 1 -->
        <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
          <div class="flex justify-between items-start mb-4">
            <div>
              <p class="text-neutral-500 text-sm">财务流程效率提升</p>
              <h4 class="text-2xl font-bold mt-1">37.5%</h4>
            </div>
            <div class="w-10 h-10 rounded-full bg-success/10 flex items-center justify-center">
              <i class="fa fa-line-chart text-success"></i>
            </div>
          </div>
          <div class="flex items-center text-success text-sm">
            <i class="fa fa-arrow-up mr-1"></i>
            <span>较上年提升12.3%</span>
          </div>
        </div>
        
        <!-- 指标卡片 2 -->
        <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
          <div class="flex justify-between items-start mb-4">
            <div>
              <p class="text-neutral-500 text-sm">决策响应时间</p>
              <h4 class="text-2xl font-bold mt-1">4.2小时</h4>
            </div>
            <div class="w-10 h-10 rounded-full bg-primary/10 flex items-center justify-center">
              <i class="fa fa-clock-o text-primary"></i>
            </div>
          </div>
          <div class="flex items-center text-success text-sm">
            <i class="fa fa-arrow-down mr-1"></i>
            <span>较上年缩短68.4%</span>
          </div>
        </div>
        
        <!-- 指标卡片 3 -->
        <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
          <div class="flex justify-between items-start mb-4">
            <div>
              <p class="text-neutral-500 text-sm">风险预警准确率</p>
              <h4 class="text-2xl font-bold mt-1">92.8%</h4>
            </div>
            <div class="w-10 h-10 rounded-full bg-secondary/10 flex items-center justify-center">
              <i class="fa fa-shield text-secondary"></i>
            </div>
          </div>
          <div class="flex items-center text-success text-sm">
            <i class="fa fa-arrow-up mr-1"></i>
            <span>较上年提升8.7%</span>
          </div>
        </div>
        
        <!-- 指标卡片 4 -->
        <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
          <div class="flex justify-between items-start mb-4">
            <div>
              <p class="text-neutral-500 text-sm">财务运营成本</p>
              <h4 class="text-2xl font-bold mt-1">-18.3%</h4>
            </div>
            <div class="w-10 h-10 rounded-full bg-danger/10 flex items-center justify-center">
              <i class="fa fa-money text-danger"></i>
            </div>
          </div>
          <div class="flex items-center text-success text-sm">
            <i class="fa fa-arrow-down mr-1"></i>
            <span>较上年降低6.2%</span>
          </div>
        </div>
      </div>
    </section>
    
    <!-- 图表分析区域 -->
    <section class="mb-10 grid grid-cols-1 lg:grid-cols-2 gap-6">
      <!-- 图表 1：财务流程优化效果 -->
      <div class="bg-white rounded-xl p-6 shadow-sm">
        <h3 class="text-lg font-semibold mb-4 text-neutral-700">财务流程优化效果对比</h3>
        <div class="h-80">
          <canvas id="processOptimizationChart"></canvas>
        </div>
      </div>
      
      <!-- 图表 2：决策效率提升 -->
      <div class="bg-white rounded-xl p-6 shadow-sm">
        <h3 class="text-lg font-semibold mb-4 text-neutral-700">决策效率提升趋势</h3>
        <div class="h-80">
          <canvas id="decisionEfficiencyChart"></canvas>
        </div>
      </div>
    </section>
    
    <!-- 主要数据表格区域 -->
    <section class="mb-10">
      <div class="flex justify-between items-center mb-4">
        <h3 class="text-lg font-semibold text-neutral-700">企业财务流程优化详细数据</h3>
        <div class="flex space-x-2">
          <button class="bg-white border border-neutral-200 px-3 py-1 rounded-md hover:bg-neutral-50 transition-colors">
            <i class="fa fa-filter mr-1"></i> 筛选
          </button>
          <button class="bg-white border border-neutral-200 px-3 py-1 rounded-md hover:bg-neutral-50 transition-colors">
            <i class="fa fa-sort mr-1"></i> 排序
          </button>
        </div>
      </div>
      
      <div class="bg-white rounded-xl overflow-hidden table-shadow">
        <div class="overflow-x-auto">
          <table class="w-full">
            <thead>
              <tr class="bg-neutral-50 text-left">
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">企业规模</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">财务流程</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">优化前耗时</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">优化后耗时</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">效率提升</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">成本节约</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">实施时间</th>
              </tr>
            </thead>
            <tbody>
              <tr class="hover:bg-neutral-50 transition-colors">
                <td class="px-6 py-4 border-b">大型企业</td>
                <td class="px-6 py-4 border-b">月度财务结算</td>
                <td class="px-6 py-4 border-b">7.5天</td>
                <td class="px-6 py-4 border-b">2.1天</td>
                <td class="px-6 py-4 border-b text-success font-medium">72.0%</td>
                <td class="px-6 py-4 border-b">¥326,000/月</td>
                <td class="px-6 py-4 border-b">3个月</td>
              </tr>
              <tr class="hover:bg-neutral-50 transition-colors">
                <td class="px-6 py-4 border-b">大型企业</td>
                <td class="px-6 py-4 border-b">供应商付款审批</td>
                <td class="px-6 py-4 border-b">5.2天</td>
                <td class="px-6 py-4 border-b">1.8天</td>
                <td class="px-6 py-4 border-b text-success font-medium">65.4%</td>
                <td class="px-6 py-4 border-b">¥189,500/月</td>
                <td class="px-6 py-4 border-b">2个月</td>
              </tr>
              <tr class="hover:bg-neutral-50 transition-colors">
                <td class="px-6 py-4 border-b">中型企业</td>
                <td class="px-6 py-4 border-b">预算编制与分析</td>
                <td class="px-6 py-4 border-b">12.0天</td>
                <td class="px-6 py-4 border-b">4.5天</td>
                <td class="px-6 py-4 border-b text-success font-medium">62.5%</td>
                <td class="px-6 py-4 border-b">¥156,200/季</td>
                <td class="px-6 py-4 border-b">4个月</td>
              </tr>
              <tr class="hover:bg-neutral-50 transition-colors">
                <td class="px-6 py-4 border-b">中型企业</td>
                <td class="px-6 py-4 border-b">财务报表生成</td>
                <td class="px-6 py-4 border-b">4.8天</td>
                <td class="px-6 py-4 border-b">1.2天</td>
                <td class="px-6 py-4 border-b text-success font-medium">75.0%</td>
                <td class="px-6 py-4 border-b">¥98,700/月</td>
                <td class="px-6 py-4 border-b">1.5个月</td>
              </tr>
              <tr class="hover:bg-neutral-50 transition-colors">
                <td class="px-6 py-4">小型企业</td>
                <td class="px-6 py-4">费用报销处理</td>
                <td class="px-6 py-4">3.5天</td>
                <td class="px-6 py-4">0.8天</td>
                <td class="px-6 py-4 text-success font-medium">77.1%</td>
                <td class="px-6 py-4">¥45,300/月</td>
                <td class="px-6 py-4">1个月</td>
              </tr>
            </tbody>
          </table>
        </div>
        
        <div class="px-6 py-4 flex justify-between items-center border-t">
          <p class="text-sm text-neutral-500">显示 1 至 5 条，共 24 条记录</p>
          <div class="flex space-x-1">
            <button class="w-8 h-8 flex items-center justify-center rounded border border-neutral-200 bg-white hover:bg-neutral-50 disabled:opacity-50" disabled>
              <i class="fa fa-chevron-left text-xs"></i>
            </button>
            <button class="w-8 h-8 flex items-center justify-center rounded border border-primary bg-primary text-white">1</button>
            <button class="w-8 h-8 flex items-center justify-center rounded border border-neutral-200 bg-white hover:bg-neutral-50">2</button>
            <button class="w-8 h-8 flex items-center justify-center rounded border border-neutral-200 bg-white hover:bg-neutral-50">3</button>
            <button class="w-8 h-8 flex items-center justify-center rounded border border-neutral-200 bg-white hover:bg-neutral-50">4</button>
            <button class="w-8 h-8 flex items-center justify-center rounded border border-neutral-200 bg-white hover:bg-neutral-50">5</button>
            <button class="w-8 h-8 flex items-center justify-center rounded border border-neutral-200 bg-white hover:bg-neutral-50">
              <i class="fa fa-chevron-right text-xs"></i>
            </button>
          </div>
        </div>
      </div>
    </section>
    
    <!-- 风险控制能力分析表格 -->
    <section class="mb-10">
      <div class="flex justify-between items-center mb-4">
        <h3 class="text-lg font-semibold text-neutral-700">企业风险控制能力评估</h3>
        <div class="flex space-x-2">
          <button class="bg-white border border-neutral-200 px-3 py-1 rounded-md hover:bg-neutral-50 transition-colors">
            <i class="fa fa-filter mr-1"></i> 筛选
          </button>
          <button class="bg-white border border-neutral-200 px-3 py-1 rounded-md hover:bg-neutral-50 transition-colors">
            <i class="fa fa-sort mr-1"></i> 排序
          </button>
        </div>
      </div>
      
      <div class="bg-white rounded-xl overflow-hidden table-shadow">
        <div class="overflow-x-auto">
          <table class="w-full">
            <thead>
              <tr class="bg-neutral-50 text-left">
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">风险类型</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">传统方法识别率</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">BI系统识别率</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">提升幅度</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">平均响应时间</th>
                <th class="px-6 py-4 font-semibold text-neutral-600 border-b">年度损失减少</th>
              </tr>
            </thead>
            <tbody>
              <tr class="hover:bg-neutral-50 transition-colors">
                <td class="px-6 py-4 border-b font-medium">欺诈风险</td>
                <td class="px-6 py-4 border-b">42.3%</td>
                <td class="px-6 py-4 border-b">91.7%</td>
                <td class="px-6 py-4 border-b text-success font-medium">+49.4%</td>
                <td class="px-6 py-4 border-b">1.2天</td>
                <td class="px-6 py-4 border-b">¥856,000</td>
              </tr>
              <tr class="hover:bg-neutral-50 transition-colors">
                <td class="px-6 py-4 border-b font-medium">合规风险</td>
                <td class="px-6 py-4 border-b">65.8%</td>
                <td class="px-6 py-4 border-b">94.2%</td>
                <td class="px-6 py-4 border-b text-success font-medium">+28.4%</td>
                <td class="px-6 py-4 border-b">2.5天</td>
                <td class="px-6 py-4 border-b">¥1,245,000</td>
              </tr>
              <tr class="hover:bg-neutral-50 transition-colors">
                <td class="px-6 py-4 border-b font-medium">流动性风险</td>
                <td class="px-6 py-4 border-b">51.5%</td>
                <td class="px-6 py-4 border-b">88.3%</td>
                <td class="px-6 py-4 border-b text-success font-medium">+36.8%</td>
                <td class="px-6 py-4 border-b">3.8天</td>
                <td class="px-6 py-4 border-b">¥2,158,000</td>
              </tr>
              <tr class="hover:bg-neutral-50 transition-colors">
                <td class="px-6 py-4 border-b font-medium">市场风险</td>
                <td class="px-6 py-4 border-b">38.7%</td>
                <td class="px-6 py-4 border-b">76.9%</td>
                <td class="px-6 py-4 border-b text-success font-medium">+38.2%</td>
                <td class="px-6 py-4 border-b">5.2天</td>
                <td class="px-6 py-4 border-b">¥3,420,000</td>
              </tr>
              <tr class="hover:bg-neutral-50 transition-colors">
                <td class="px-6 py-4 font-medium">信用风险</td>
                <td class="px-6 py-4">47.2%</td>
                <td class="px-6 py-4">89.5%</td>
                <td class="px-6 py-4 text-success font-medium">+42.3%</td>
                <td class="px-6 py-4">4.0天</td>
                <td class="px-6 py-4">¥1,876,500</td>
              </tr>
            </tbody>
          </table>
        </div>
        
        <div class="px-6 py-4 flex justify-between items-center border-t">
          <p class="text-sm text-neutral-500">显示 1 至 5 条，共 12 条记录</p>
          <div class="flex space-x-1">
            <button class="w-8 h-8 flex items-center justify-center rounded border border-neutral-200 bg-white hover:bg-neutral-50 disabled:opacity-50" disabled>
              <i class="fa fa-chevron-left text-xs"></i>
            </button>
            <button class="w-8 h-8 flex items-center justify-center rounded border border-primary bg-primary text-white">1</button>
            <button class="w-8 h-8 flex items-center justify-center rounded border border-neutral-200 bg-white hover:bg-neutral-50">2</button>
            <button class="w-8 h-8 flex items-center justify-center rounded border border-neutral-200 bg-white hover:bg-neutral-50">3</button>
            <button class="w-8 h-8 flex items-center justify-center rounded border border-neutral-200 bg-white hover:bg-neutral-50">
              <i class="fa fa-chevron-right text-xs"></i>
            </button>
          </div>
        </div>
      </div>
    </section>
    
    <!-- 数据分析洞察 -->
    <section class="mb-10">
      <h3 class="text-lg font-semibold mb-4 text-neutral-700">数据分析洞察</h3>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
          <div class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center mb-4">
            <i class="fa fa-lightbulb-o text-primary text-xl"></i>
          </div>
          <h4 class="font-semibold text-neutral-700 mb-2">流程自动化价值</h4>
          <p class="text-neutral-500 text-sm">实施商务智能系统后，大型企业财务流程平均效率提升60%以上，其中自动化程度最高的流程获得了最大收益。</p>
        </div>
        
        <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
          <div class="w-12 h-12 rounded-full bg-secondary/10 flex items-center justify-center mb-4">
            <i class="fa fa-line-chart text-secondary text-xl"></i>
          </div>
          <h4 class="font-semibold text-neutral-700 mb-2">决策效率与规模</h4>
          <p class="text-neutral-500 text-sm">企业规模与决策效率提升呈正相关，大型企业通过BI系统获得的决策效率提升(68.4%)显著高于中小型企业。</p>
        </div>
        
        <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
          <div class="w-12 h-12 rounded-full bg-success/10 flex items-center justify-center mb-4">
            <i class="fa fa-shield text-success text-xl"></i>
          </div>
          <h4 class="font-semibold text-neutral-700 mb-2">风险控制投资回报</h4>
          <p class="text-neutral-500 text-sm">在风险控制方面，欺诈风险和信用风险的识别能力提升最为显著，平均为企业减少年度损失超200万元。</p>
        </div>
      </div>
    </section>
  </main>
  
  <!-- 页脚 -->
  <footer class="bg-white border-t border-neutral-200">
    <div class="container mx-auto px-4 py-8">
      <div class="flex flex-col md:flex-row justify-between items-center">
        <div class="mb-4 md:mb-0">
          <p class="text-neutral-500 text-sm">© 2023 财务商业智能分析平台. 保留所有权利.</p>
        </div>
        <div class="flex space-x-6">
          <a href="#" class="text-neutral-500 hover:text-primary transition-colors text-sm">关于我们</a>
          <a href="#" class="text-neutral-500 hover:text-primary transition-colors text-sm">使用条款</a>
          <a href="#" class="text-neutral-500 hover:text-primary transition-colors text-sm">隐私政策</a>
          <a href="#" class="text-neutral-500 hover:text-primary transition-colors text-sm">联系我们</a>
        </div>
      </div>
    </div>
  </footer>

  <!-- JavaScript -->
  <script>
    // 页面滚动时导航栏效果
    window.addEventListener('scroll', function() {
      const header = document.querySelector('header');
      if (window.scrollY > 10) {
        header.classList.add('py-2');
        header.classList.remove('py-4');
        header.classList.add('shadow');
      } else {
        header.classList.add('py-4');
        header.classList.remove('py-2');
        header.classList.remove('shadow');
      }
    });
    
    // 财务流程优化效果图表
    const processCtx = document.getElementById('processOptimizationChart').getContext('2d');
    const processChart = new Chart(processCtx, {
      type: 'bar',
      data: {
        labels: ['月度结算', '付款审批', '预算编制', '报表生成', '费用报销'],
        datasets: [
          {
            label: '优化前(天)',
            data: [7.5, 5.2, 12.0, 4.8, 3.5],
            backgroundColor: 'rgba(201, 205, 212, 0.7)',
            borderColor: 'rgba(201, 205, 212, 1)',
            borderWidth: 1
          },
          {
            label: '优化后(天)',
            data: [2.1, 1.8, 4.5, 1.2, 0.8],
            backgroundColor: 'rgba(22, 93, 255, 0.7)',
            borderColor: 'rgba(22, 93, 255, 1)',
            borderWidth: 1
          }
        ]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        plugins: {
          legend: {
            position: 'top',
          },
          tooltip: {
            mode: 'index',
            intersect: false
          }
        },
        scales: {
          y: {
            beginAtZero: true,
            title: {
              display: true,
              text: '处理时间(天)'
            }
          }
        }
      }
    });
    
    // 决策效率提升趋势图表
    const decisionCtx = document.getElementById('decisionEfficiencyChart').getContext('2d');
    const decisionChart = new Chart(decisionCtx, {
      type: 'line',
      data: {
        labels: ['2019 Q1', '2019 Q3', '2020 Q1', '2020 Q3', '2021 Q1', '2021 Q3', '2022 Q1', '2022 Q3'],
        datasets: [
          {
            label: '大型企业',
            data: [13.2, 11.8, 9.5, 7.2, 5.8, 5.1, 4.5, 4.2],
            borderColor: 'rgba(22, 93, 255, 1)',
            backgroundColor: 'rgba(22, 93, 255, 0.1)',
            tension: 0.3,
            fill: true
          },
          {
            label: '中型企业',
            data: [15.6, 14.2, 12.8, 10.5, 9.2, 8.7, 7.5, 6.8],
            borderColor: 'rgba(54, 207, 201, 1)',
            backgroundColor: 'rgba(54, 207, 201, 0.1)',
            tension: 0.3,
            fill: true
          },
          {
            label: '小型企业',
            data: [18.3, 17.5, 16.2, 14.8, 13.5, 12.1, 10.8, 9.5],
            borderColor: 'rgba(82, 196, 26, 1)',
            backgroundColor: 'rgba(82, 196, 26, 0.1)',
            tension: 0.3,
            fill: true
          }
        ]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        plugins: {
          legend: {
            position: 'top',
          },
          tooltip: {
            mode: 'index',
            intersect: false
          }
        },
        scales: {
          y: {
            beginAtZero: false,
            title: {
              display: true,
              text: '决策响应时间(小时)'
            }
          }
        }
      }
    });
  </script>
</body>
</html>
