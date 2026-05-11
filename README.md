<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>K-Beauty Test Page</title>
    <style>
        /* 1. GIỮ NGUYÊN CSS CŨ CỦA BẠN (Dưới đây là phần bổ sung) */
        body { font-family: sans-serif; margin: 0; padding: 0; text-align: center; }
        
        .btn-borogagi {
            background-color: #000;
            color: #fff;
            padding: 12px 40px;
            font-size: 16px;
            font-weight: bold;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin: 20px 0;
        }

        /* 2. PHẦN MỸ PHẨM GIẢM GIÁ (ẨN LÚC ĐẦU) */
        #sale-section {
            display: none; /* Ẩn đi */
            max-width: 500px;
            margin: 20px auto;
            padding: 15px;
            background: #fff;
            text-align: left;
            border-top: 1px solid #eee;
        }

        .tabs { display: flex; gap: 8px; overflow-x: auto; margin-bottom: 20px; }
        .tabs span {
            border: 1px solid #ddd;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 13px;
            white-space: nowrap;
            color: #666;
        }
        .tabs .active { background: #000; color: #fff; border-color: #000; }

        .sale-title { font-size: 18px; font-weight: bold; margin-bottom: 15px; }

        .product-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        .product-card { margin-bottom: 20px; }
        .img-placeholder {
            width: 100%;
            aspect-ratio: 1/1;
            background: #f4f4f4;
            border-radius: 8px;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #ccc;
        }

        .old-price { text-decoration: line-through; color: #aaa; font-size: 12px; }
        .price-info { display: flex; align-items: baseline; gap: 4px; margin-top: 2px; }
        .discount { color: #ff4d4d; font-weight: bold; font-size: 16px; }
        .current-price { font-weight: bold; font-size: 16px; }
    </style>
</head>
<body>

    <div style="padding: 50px 20px;">
        <h1>Chào mừng bạn đến với trang web của Phương Linh</h1>
        <p>Khám phá bộ sưu tập mỹ phẩm mới nhất ngay tại đây.</p>
        
        <button class="btn-borogagi" id="btn-show">보러가기</button>
    </div>

    <div id="sale-section">
        <div class="tabs">
            <span class="active">전체</span>
            <span>스킨케어</span>
            <span>메이크업</span>
            <span>바디케어</span>
            <span>헤어케어</span>
        </div>

        <div class="sale-title">놓치면 끝! cuối cùng cơ hội</div>

        <div class="product-grid">
            <div class="product-card">
                <div class="img-placeholder">Product 1</div>
                <div class="old-price">30,000원</div>
                <div class="price-info">
                    <span class="discount">20%</span>
                    <span class="current-price">14,820원~</span>
                </div>
            </div>
            <div class="product-card">
                <div class="img-placeholder">Product 2</div>
                <div class="old-price">42,000원</div>
                <div class="price-info">
                    <span class="discount">20%</span>
                    <span class="current-price">20,740원~</span>
                </div>
            </div>
            </div>
    </div>

    <script>
        // Script điều khiển hiện/ẩn
        document.getElementById('btn-show').addEventListener('click', function() {
            const saleSection = document.getElementById('sale-section');
            
            // Hiện phần giảm giá
            saleSection.style.display = 'block';
            
            // Cuộn mượt xuống phần vừa hiện
            saleSection.scrollIntoView({ behavior: 'smooth' });

            // LƯU Ý CHO VWO: Nếu bạn muốn đo lường việc người dùng nhấn nút này
            // Hãy đảm bảo nút này có ID là 'btn-show' trong cấu hình Goal của VWO.
        });
    </script>

</body>
</html>
