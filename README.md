<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tính FCR trong Chăn Nuôi</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 20px;
            background-color: #f4f4f4;
        }
        h1 {
            text-align: center;
        }
        .container {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        input[type="number"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #a72828;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
        .result {
            margin-top: 20px;
            font-size: 1.2em;
            text-align: center;
        }
        .message {
            margin-top: 10px;
            font-size: 1em;
            color: #007bff;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Tính FCR trong Chăn Nuôi</h1>
    <label for="food">Lượng thức ăn tiêu thụ (kg):</label>
    <input type="number" id="food" placeholder="Nhập lượng thức ăn" required>

    <label for="weight">Trọng lượng tăng thêm (kg):</label>
    <input type="number" id="weight" placeholder="Nhập trọng lượng tăng thêm" required>

    <button onclick="calculateFCR()">Tính FCR</button>

    <div class="result" id="result"></div>
    <div class="message" id="message"></div>
</div>

<script>
    function calculateFCR() {
        var food = parseFloat(document.getElementById('food').value);
        var weight = parseFloat(document.getElementById('weight').value);

        if (food > 0 && weight > 0) {
            var fcr = (food / weight).toFixed(2);
            document.getElementById('result').innerText = "FCR = " + fcr;

            // Kiểm tra FCR tốt hay không
            if (fcr <= 2) {
                document.getElementById('message').innerText = "FCR vật nuôi của bạn rất tốt! Tiếp tục duy trì chế độ ăn uống hợp lý.";
            } else {
                document.getElementById('message').innerText = "FCR vật nuôi của bạn chưa tốt. Cần chỉnh lại chế độ ăn.";
            }
        } else {
            document.getElementById('result').innerText = "Vui lòng nhập giá trị hợp lệ.";
            document.getElementById('message').innerText = "";
        }
    }
</script>
</body>
<html>
<head>
<title>Lời khuyên random</title>
</head>
<body>

<h1>Lời khuyên random</h1>

<button onclick="showRandomTip()">Hãy xem lời khuyên của tôi!</button>

<p id="tip"></p>

<script>
const tips = [
"Cung cấp cho vật nuôi của bạn với môi trường phù hợp",
"Giữ sạch silo chứa thức ăn",
"Sử dụng đúng loại máng ăn",
"Đặt máng ăn và máng uống tại vị trí chính xác",
"Không nên cho ăn qua nhiều",
"Hệ thống chiếu sáng thích hợp phải được tuân theo",
"Giữ cho đàn vật nuôi của bạn khỏe mạnh",
"Tiêm vắc-xin phòng bệnh truyền nhiễm cho đàn vật nuôi của bạn",
"Thực hiện theo các hướng dẫn trên thị trường"
];

function showRandomTip() {
  const randomIndex = Math.floor(Math.random() * tips.length);
  document.getElementById("tip").innerHTML = tips[randomIndex];
}
</script>
</body>
</html>

