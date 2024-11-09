<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Diskon Eksklusif Cafe ImajiMu</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            margin: 0;
            padding: 20px;
            background-color: #1d1e33;
            color: #fff;
        }
        .container {
            width: 100%;
            max-width: 400px;
            background: #2c2d4a;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            color: #ccc;
        }
        input[type="text"], input[type="number"] {
            width: 100%;
            padding: 10px;
            border-radius: 4px;
            border: 1px solid #666;
            background: #333;
            color: #fff;
        }
        button {
            width: 100%;
            padding: 10px;
            background: #ff6b6b;
            border: none;
            border-radius: 4px;
            color: #fff;
            font-size: 16px;
            cursor: pointer;
        }
        button:hover {
            background: #ff4e4e;
        }
        .discount-message {
            display: none;
            margin-top: 20px;
            text-align: center;
        }
        .discount-code {
            font-size: 20px;
            font-weight: bold;
            color: #ffcc00;
        }
    </style>
</head>
<body>

    <div class="container">
        <h2>Diskon Eksklusif di Cafe ImajiMu</h2>
        <p>Isi form berikut untuk mendapatkan diskon spesial saat berkunjung ke cafe kami!</p>

        <!-- Form Pengisian Data -->
        <div id="form-section">
            <div class="form-group">
                <label for="name">Nama:</label>
                <input type="text" id="name" required>
            </div>
            <div class="form-group">
                <label for="city">Tempat Tinggal/Kota Asal:</label>
                <input type="text" id="city" required>
            </div>
            <div class="form-group">
                <label for="phone">Nomor WA:</label>
                <input type="number" id="phone" required>
            </div>
            <button onclick="submitForm()">Dapatkan Diskon</button>
        </div>

        <!-- Tampilan Diskon -->
        <div id="discount-section" class="discount-message">
            <p>Terima kasih, <span id="user-name"></span>!</p>
            <p>Diskon Anda telah berhasil diterima. Tunjukkan kode berikut di kasir untuk mengklaim:</p>
            <p class="discount-code">DISKON10</p>
            <p>Diskon 10% untuk menu signature ImajiMu</p>
        </div>
    </div>

    <script>
        function submitForm() {
            // Ambil nilai dari input form
            var name = document.getElementById("name").value;
            var city = document.getElementById("city").value;
            var phone = document.getElementById("phone").value;

            // Simpan data di database (nanti bisa diimplementasikan dengan server)
            console.log("Data Pengguna:", { name, city, phone });

            // Tampilkan pesan diskon
            document.getElementById("user-name").innerText = name;
            document.getElementById("form-section").style.display = "none";
            document.getElementById("discount-section").style.display = "block";
        }
    </script>

</body>
</html>
