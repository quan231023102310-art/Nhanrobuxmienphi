<!DOCTYPE html>
<html lang="vi">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Form Nhập Thông Tin</title>

<style>
    body {
        font-family: Arial;
        background: #f5f5f5;
        padding: 20px;
    }

    .container {
        background: white;
        padding: 20px;
        border-radius: 10px;
        width: 100%;
        max-width: 400px;
        margin: auto;
        box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    input, textarea {
        width: 100%;
        padding: 12px;
        margin-top: 10px;
        border: 1px solid #ccc;
        border-radius: 8px;
        font-size: 16px;
    }

    button {
        width: 100%;
        padding: 12px;
        margin-top: 15px;
        background: #007bff;
        color: white;
        font-size: 18px;
        border: none;
        border-radius: 8px;
    }
</style>
</head>
<body>

<div class="container">
    <h2>Nhập Thông Tin</h2>

    <label>Tên:</label>
    <input type="text" id="name" placeholder="Nhập tên của bạn..." />

    <label>Yêu cầu:</label>
    <textarea id="request" placeholder="Nhập yêu cầu..." rows="4"></textarea>

    <button onclick="sendData()">Gửi</button>
</div>

<script>
function sendData() {
    let name = document.getElementById("name").value;
    let req = document.getElementById("request").value;

    if (name === "" || req === "") {
        alert("Vui lòng nhập đầy đủ 2 ô!");
        return;
    }

    alert("Đã gửi:\nTên: " + name + "\nYêu cầu: " + req);
}
</script>

</body>
</html>
