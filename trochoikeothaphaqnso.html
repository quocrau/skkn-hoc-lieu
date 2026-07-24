<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trò Chơi Kéo Thả Phân Số</title>
    <style>
        body {
            font-family: 'Comic Sans MS', 'Chalkboard SE', sans-serif;
            background-color: #f0f8ff;
            text-align: center;
            color: #333;
            margin: 0;
            padding: 20px;
        }

        h1 {
            color: #ff6347;
            text-transform: uppercase;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }

        .subtitle {
            font-size: 1.2rem;
            color: #4682b4;
            margin-bottom: 30px;
        }

        .game-container {
            display: flex;
            justify-content: center;
            gap: 50px;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
        }

        .draggables-container {
            display: flex;
            flex-direction: column;
            gap: 20px;
            justify-content: center;
        }

        .fraction-card {
            width: 80px;
            height: 80px;
            background-color: #ffd700;
            border: 4px solid #ffa500;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            font-weight: bold;
            cursor: grab;
            box-shadow: 3px 3px 0px rgba(0,0,0,0.1);
            transition: transform 0.2s;
        }

        .fraction-card:active {
            cursor: grabbing;
            transform: scale(0.95);
        }

        .drop-zones-container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .drop-zone {
            width: 350px;
            height: 80px;
            background-color: #f9f9f9;
            border: 3px dashed #87ceeb;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 15px;
            box-sizing: border-box;
            transition: background-color 0.3s;
        }

        .drop-zone.hover {
            background-color: #e0ffff;
            border-color: #00ced1;
        }

        .visual-bar {
            display: flex;
            width: 200px;
            height: 40px;
            border: 2px solid #555;
            border-radius: 5px;
            overflow: hidden;
        }

        .visual-bar div {
            flex: 1;
            border-right: 1px solid #555;
        }

        .visual-bar div:last-child {
            border-right: none;
        }

        .colored {
            background-color: #32cd32;
        }

        .correct-zone {
            background-color: #e8f5e9 !important;
            border: 3px solid #4caf50 !important;
        }

        .message-board {
            margin-top: 30px;
            font-size: 24px;
            color: #ff4500;
            font-weight: bold;
            height: 40px;
        }
        
        .fraction-display {
            display: flex;
            flex-direction: column;
            align-items: center;
            line-height: 1;
        }
        
        .fraction-display span:first-child {
            border-bottom: 3px solid #333;
            padding-bottom: 2px;
            margin-bottom: 2px;
        }
    </style>
</head>
<body>

    <h1>Trò Chơi Kéo Thả Phân Số</h1>
    <div class="subtitle">Chào mừng các em học sinh Trường Tiểu Học Minh Hoà! Hãy kéo thẻ phân số vào đúng hình biểu diễn nhé.</div>

    <div class="game-container">
        <div class="draggables-container">
            <div class="fraction-card" draggable="true" id="frac-1" data-val="1/2">
                <div class="fraction-display"><span>1</span><span>2</span></div>
            </div>
            <div class="fraction-card" draggable="true" id="frac-2" data-val="3/4">
                <div class="fraction-display"><span>3</span><span>4</span></div>
            </div>
            <div class="fraction-card" draggable="true" id="frac-3" data-val="2/5">
                <div class="fraction-display"><span>2</span><span>5</span></div>
            </div>
            <div class="fraction-card" draggable="true" id="frac-4" data-val="5/8">
                <div class="fraction-display"><span>5</span><span>8</span></div>
            </div>
        </div>

        <div class="drop-zones-container">
            
            <div class="drop-zone" data-target="3/4">
                <div class="visual-bar">
                    <div class="colored"></div><div class="colored"></div><div class="colored"></div><div></div>
                </div>
            </div>

            <div class="drop-zone" data-target="1/2">
                <div class="visual-bar">
                    <div class="colored"></div><div></div>
                </div>
            </div>

            <div class="drop-zone" data-target="5/8">
                <div class="visual-bar">
                    <div class="colored"></div><div class="colored"></div><div class="colored"></div><div class="colored"></div><div class="colored"></div><div></div><div></div><div></div>
                </div>
            </div>

            <div class="drop-zone" data-target="2/5">
                <div class="visual-bar">
                    <div class="colored"></div><div class="colored"></div><div></div><div></div><div></div>
                </div>
            </div>

        </div>
    </div>

    <div class="message-board" id="message"></div>

    <script>
        const draggables = document.querySelectorAll('.fraction-card');
        const dropZones = document.querySelectorAll('.drop-zone');
        const message = document.getElementById('message');
        let correctCount = 0;

        // Xử lý sự kiện khi bắt đầu kéo thẻ
        draggables.forEach(draggable => {
            draggable.addEventListener('dragstart', (e) => {
                e.dataTransfer.setData('text/plain', draggable.dataset.val);
                e.dataTransfer.setData('id', draggable.id);
                setTimeout(() => {
                    draggable.style.opacity = '0.5';
                }, 0);
            });

            draggable.addEventListener('dragend', () => {
                draggable.style.opacity = '1';
            });
        });

        // Xử lý sự kiện cho các vùng thả
        dropZones.forEach(zone => {
            zone.addEventListener('dragover', e => {
                e.preventDefault();
                zone.classList.add('hover');
            });

            zone.addEventListener('dragleave', () => {
                zone.classList.remove('hover');
            });

            zone.addEventListener('drop', e => {
                e.preventDefault();
                zone.classList.remove('hover');
                
                const draggedVal = e.dataTransfer.getData('text/plain');
                const draggedId = e.dataTransfer.getData('id');
                const targetVal = zone.dataset.target;

                // Kiểm tra nếu thẻ kéo đúng với giá trị của ô
                if (draggedVal === targetVal) {
                    const draggableElement = document.getElementById(draggedId);
                    
                    // Di chuyển thẻ vào ô và làm cho nó không kéo được nữa
                    zone.appendChild(draggableElement);
                    draggableElement.style.margin = '0 auto';
                    draggableElement.setAttribute('draggable', 'false');
                    draggableElement.style.cursor = 'default';
                    draggableElement.style.boxShadow = 'none';
                    
                    zone.classList.add('correct-zone');
                    
                    correctCount++;
                    
                    if (correctCount === draggables.length) {
                        message.style.color = '#32cd32';
                        message.innerText = "Tuyệt vời! Các em đã hoàn thành xuất sắc bài tập!";
                    } else {
                        message.style.color = '#ff8c00';
                        message.innerText = "Chính xác! Giỏi lắm.";
                        setTimeout(() => message.innerText = "", 1500);
                    }
                } else {
                    message.style.color = '#ff0000';
                    message.innerText = "Chưa đúng rồi, hãy quan sát kĩ lại nhé!";
                    setTimeout(() => message.innerText = "", 1500);
                }
            });
        });
    </script>
</body>
</html>
