<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>忍影巨刀重生時間計算器</title>
    <style>
        body {
            font-family: 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background-color: #f0f2f5;
            color: #333;
            padding: 20px;
            box-sizing: border-box;
        }

        .container {
            background-color: #fff;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 550px;
            text-align: center;
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        h1 {
            color: #1a73e8;
            margin: 0 0 10px;
            font-size: 2em;
        }

        .section {
            background-color: #f8f9fa;
            padding: 25px;
            border-radius: 10px;
            box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.05);
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        h2 {
            color: #555;
            margin: 0;
            font-size: 1.5em;
        }

        .input-group {
            text-align: left;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            font-size: 1.1em;
            color: #555;
        }

        input[type="text"] {
            width: 100%;
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 8px;
            box-sizing: border-box;
            font-size: 1em;
            transition: border-color 0.3s;
        }

        input[type="text"]:focus {
            outline: none;
            border-color: #1a73e8;
            box-shadow: 0 0 0 3px rgba(26, 115, 232, 0.2);
        }

        button {
            padding: 12px 25px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1em;
            font-weight: bold;
            color: #fff;
            transition: background-color 0.3s, transform 0.2s;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 200px;
            align-self: center;
        }

        #calculateRealTime {
            background-color: #4CAF50; /* 綠色 */
        }

        #calculateRealTime:hover {
            background-color: #45a049;
            transform: translateY(-2px);
        }

        #calculateGameTime {
            background-color: #f44336; /* 紅色 */
        }

        #calculateGameTime:hover {
            background-color: #e53935;
            transform: translateY(-2px);
        }

        .result {
            margin-top: 15px;
            padding: 20px;
            border-radius: 8px;
            background-color: #e9ecef;
            display: none;
            text-align: center;
            animation: fadeIn 0.5s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .result p {
            font-size: 1.1em;
            margin: 0;
            color: #555;
        }

        .result strong {
            color: #1a73e8;
            font-size: 1.5em;
            display: block;
            margin-top: 10px;
        }

        .error-message {
            color: #d9534f;
            font-size: 1em;
            display: none;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>忍影巨刀重生時間計算器</h1>

    <!-- 現實時間計算區塊 -->
    <div class="section">
        <h2>現實時間</h2>
        <div class="input-group">
            <label for="realTimeInput">輸入 Boss 死亡時間 (例如：1616)：</label>
            <input type="text" id="realTimeInput" placeholder="例如：1616 或 161600">
        </div>
        <button id="calculateRealTime">計算重生時間（+1H 24M）</button>
        <div id="realTimeError" class="error-message"></div>
        <div class="result" id="result-real-time">
            <p>下次重生時間為：</p>
            <strong id="real-time-output"></strong>
        </div>
    </div>

    <!-- 遊戲時間計算區塊 -->
    <div class="section">
        <h2>遊戲時間</h2>
        <div class="input-group">
            <label for="gameTimeInput">輸入 Boss 死亡時間 (例如：0815)：</label>
            <input type="text" id="gameTimeInput" placeholder="例如：0815 或 081500">
        </div>
        <button id="calculateGameTime">計算重生時間（+16H 48M）</button>
        <div id="gameTimeError" class="error-message"></div>
        <div class="result" id="result-game-time">
            <p>下次重生時間為：</p>
            <strong id="game-time-output"></strong>
        </div>
    </div>
</div>

<script>
    /**
     * 計算並格式化時間
     * @param {string} inputId - 輸入欄位的 ID
     * @param {number} hoursToAdd - 要增加的小時數
     * @param {number} minutesToAdd - 要增加的分鐘數
     * @param {string} outputId - 輸出欄位的 ID
     * @param {string} errorId - 錯誤訊息欄位的 ID
     */
    function calculateTime(inputId, hoursToAdd, minutesToAdd, outputId, errorId) {
        const input = document.getElementById(inputId);
        const output = document.getElementById(outputId);
        const resultDiv = output.parentElement;
        const errorDiv = document.getElementById(errorId);
        
        const timeValue = input.value.trim();
        let hours = 0;
        let minutes = 0;
        let seconds = 0;
        
        // 檢查輸入是否為純數字，並且長度為 4 或 6
        if (!/^\d{4}$|^\d{6}$/.test(timeValue)) {
            errorDiv.textContent = '請輸入正確的數字格式 (例如：1616 或 161600)！';
            errorDiv.style.display = 'block';
            resultDiv.style.display = 'none';
            return;
        }

        // 根據長度解析時間
        if (timeValue.length === 4) {
            hours = parseInt(timeValue.substring(0, 2), 10);
            minutes = parseInt(timeValue.substring(2, 4), 10);
        } else if (timeValue.length === 6) {
            hours = parseInt(timeValue.substring(0, 2), 10);
            minutes = parseInt(timeValue.substring(2, 4), 10);
            seconds = parseInt(timeValue.substring(4, 6), 10);
        }

        // 檢查時分秒的範圍是否有效
        if (hours < 0 || hours > 23 || minutes < 0 || minutes > 59 || seconds < 0 || seconds > 59) {
            errorDiv.textContent = '請輸入有效的時間 (時:0-23, 分:0-59, 秒:0-59)！';
            errorDiv.style.display = 'block';
            resultDiv.style.display = 'none';
            return;
        }
        
        // 為了方便時間計算，我們使用今天的日期作為基準
        const baseDate = new Date();
        baseDate.setHours(hours, minutes, seconds, 0);

        // 增加小時和分鐘
        const newTime = new Date(baseDate.getTime() + (hoursToAdd * 60 + minutesToAdd) * 60 * 1000);
        
        // 格式化輸出，只顯示時間
        const formattedTime = newTime.toLocaleTimeString('zh-TW', {
            hour: '2-digit',
            minute: '2-digit',
            second: '2-digit',
            hour12: false
        });

        output.textContent = formattedTime;
        resultDiv.style.display = 'block';
        errorDiv.style.display = 'none';
    }

    // 為現實時間按鈕添加事件監聽器
    document.getElementById('calculateRealTime').addEventListener('click', () => {
        calculateTime('realTimeInput', 1, 24, 'real-time-output', 'realTimeError');
    });

    // 為遊戲時間按鈕添加事件監聽器
    document.getElementById('calculateGameTime').addEventListener('click', () => {
        calculateTime('gameTimeInput', 16, 48, 'game-time-output', 'gameTimeError');
    });
</script>

</body>
</html>
