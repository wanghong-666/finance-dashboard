# finance-dashboard
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <!-- Tailwind CSS 样式（CDN加速） -->
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@3.3.2/dist/tailwind.min.css" rel="stylesheet">
  <!-- 图标库（Font Awesome） -->
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
  <title>财务分析平台</title>
  <style>
    /* 自定义图表容器样式 */
    .chart-container {
      height: 300px;
      margin: 20px 0;
    }
  </style>
</head>
<body class="bg-gray-100">
  <!-- 导航栏 -->
  <nav class="bg-white p-4 shadow">
    <div class="container mx-auto flex justify-between items-center">
      <h1 class="text-2xl font-bold text-gray-800">财务分析平台</h1>
      <div class="flex items-center">
        <button class="text-gray-600 hover:text-gray-800 mr-4">
          <i class="fas fa-chart-line"></i> 数据概览
        </button>
        <button class="text-gray-600 hover:text-gray-800">
          <i class="fas fa-table"></i> 明细报表
        </button>
      </div>
    </div>
  </nav>

  <!-- 主内容容器 -->
  <div class="container mx-auto p-4">
    <!-- 核心指标卡片 -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-8">
      <div class="bg-white p-4 rounded shadow flex flex-col justify-between">
        <div>
          <p class="text-gray-600 text-sm">优化后流程效率</p>
          <h2 class="text-2xl font-bold text-green-500">85%</h2>
        </div>
        <p class="text-right text-sm text-gray-500 mt-2">提升30%对比旧流程</p>
      </div>
      <div class="bg-white p-4 rounded shadow flex flex-col justify-between">
        <div>
          <p class="text-gray-600 text-sm">决策响应时间</p>
          <h2 class="text-2xl font-bold text-blue-500">2.5小时</h2>
        </div>
        <p class="text-right text-sm text-gray-500 mt-2">缩短60%对比传统模式</p>
      </div>
      <div class="bg-white p-4 rounded shadow flex flex-col justify-between">
        <div>
          <p class="text-gray-600 text-sm">风险识别覆盖率</p>
          <h2 class="text-2xl font-bold text-red-500">92%</h2>
        </div>
        <p class="text-right text-sm text-gray-500 mt-2">提升25%对比人工审计</p>
      </div>
    </div>

    <!-- 图表区域 -->
    <div class="bg-white p-4 rounded shadow mb-8">
      <h2 class="text-xl font-bold text-gray-800 mb-4">成本收益趋势</h2>
      <div class="chart-container" id="costChart"></div>
    </div>

    <!-- 数据表格 -->
    <div class="bg-white p-4 rounded shadow">
      <h2 class="text-xl font-bold text-gray-800 mb-4">财务明细</h2>
      <table class="w-full text-sm text-left text-gray-500">
        <thead class="text-xs text-gray-700 uppercase bg-gray-50">
          <tr>
            <th scope="col" class="px-6 py-3">项目</th>
            <th scope="col" class="px-6 py-3">预算</th>
            <th scope="col" class="px-6 py-3">实际支出</th>
            <th scope="col" class="px-6 py-3">差异率</th>
          </tr>
        </thead>
        <tbody>
          <tr class="bg-white border-b">
            <td class="px-6 py-4">薪资成本</td>
            <td class="px-6 py-4">¥500,000</td>
            <td class="px-6 py-4">¥480,000</td>
            <td class="px-6 py-4 text-green-500">-4%</td>
          </tr>
          <tr class="bg-white border-b">
            <td class="px-6 py-4">营销费用</td>
            <td class="px-6 py-4">¥200,000</td>
            <td class="px-6 py-4">¥220,000</td>
            <td class="px-6 py-4 text-red-500">+10%</td>
          </tr>
          <tr class="bg-white">
            <td class="px-6 py-4">研发投入</td>
            <td class="px-6 py-4">¥300,000</td>
            <td class="px-6 py-4">¥310,000</td>
            <td class="px-6 py-4 text-red-500">+3.3%</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>

  <!-- Chart.js 依赖（CDN） -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.1/dist/chart.umd.min.js"></script>
  <script>
    // 初始化图表（成本收益趋势）
    const ctx = document.getElementById('costChart').getContext('2d');
    new Chart(ctx, {
      type: 'line',
      data: {
        labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun'],
        datasets: [{
          label: '成本',
          data: [80000, 85000, 92000, 88000, 95000, 100000],
          borderColor: '#ff6b6b',
          backgroundColor: 'rgba(255, 107, 107, 0.1)',
          fill: true
        }, {
          label: '收益',
          data: [120000, 130000, 145000, 150000, 160000, 175000],
          borderColor: '#4ecdc4',
          backgroundColor: 'rgba(78, 205, 196, 0.1)',
          fill: true
        }]
      },
      options: {
        responsive: true,
        scales: {
          y: {
            beginAtZero: true,
            title: { display: true, text: '金额（元）' }
          },
          x: { title: { display: true, text: '月份' } }
        }
      }
    });
  </script>
</body>
</html>
