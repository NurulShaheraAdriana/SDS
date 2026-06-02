<!DOCTYPE html>
<html lang="ms">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ujian Minat Kerjaya SDS</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f7f6;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 800px;
            margin: auto;
        }
        .container {
            background: #fff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        h1, h2, h3 { color: #2c3e50; }
        .instructions {
            background-color: #e9ecef;
            padding: 15px;
            border-left: 4px solid #3498db;
            margin-bottom: 20px;
        }
        .section { margin-top: 30px; margin-bottom: 15px; border-bottom: 2px solid #ecf0f1; padding-bottom: 10px; }
        .question-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 12px;
            padding: 8px;
            border-radius: 4px;
            transition: background 0.2s;
        }
        .question-item:hover { background-color: #f8f9fa; }
        input[type="checkbox"] { margin-top: 5px; margin-right: 15px; transform: scale(1.2); cursor: pointer; }
        label { cursor: pointer; width: 100%; }
        button {
            display: block;
            width: 100%;
            padding: 15px;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            margin-top: 30px;
        }
        button:hover { background-color: #2980b9; }
        #results {
            display: none;
            margin-top: 30px;
            padding: 20px;
            background-color: #e8f8f5;
            border: 1px solid #1abc9c;
            border-radius: 5px;
        }
        .score-row { display: flex; justify-content: space-between; max-width: 300px; margin-bottom: 5px; }
    </style>
</head>
<body>

<div class="container">
    <h1>Soal Selidik Minat Kerjaya (SDS)</h1>
    <div class="instructions">
        <p>Sila jawab semua soalan di bawah. Tandakan pada perkara yang anda <strong>SUKA/TAHU/BERMINAT</strong> dan biarkan kosong pada perkara yang anda <strong>TIDAK SUKA/TIDAK TAHU</strong>.</p>
    </div>

    <div id="questionnaire"></div>

    <button onclick="calculateResults()">Kira Keputusan</button>

    <div id="results">
        <h2>Keputusan Anda</h2>
        <h3 id="summary-code" style="color: #c0392b; font-size: 24px;"></h3>
        <p><strong>Pecahan Markah:</strong></p>
        <div id="score-breakdown"></div>
    </div>
</div>

<script>
    // --- Database of Questions ---
    // Add the rest of the 192 questions here
    const questions = [
        // Bahagian A
        { id: 1, text: "Membaiki alat-alat elektrik", type: "R", section: "Bahagian A: Kesukaan" },
        { id: 2, text: "Membaiki alat-alat mekanik", type: "R", section: "Bahagian A: Kesukaan" },
        { id: 11, text: "Membaca buku atau majalah sains", type: "I", section: "Bahagian A: Kesukaan" },
        { id: 21, text: "Melakar, melukis atau mewarna", type: "A", section: "Bahagian A: Kesukaan" },
        { id: 31, text: "Menulis surat kepada kawan", type: "S", section: "Bahagian A: Kesukaan" },
        { id: 41, text: "Mempengaruhi orang lain", type: "E", section: "Bahagian A: Kesukaan" },
        { id: 51, text: "Menaip bahan-bahan bertulis atau surat-surat", type: "C", section: "Bahagian A: Kesukaan" },
        
        // Bahagian B
        { id: 61, text: "Menggunakan jangka volta", type: "R", section: "Bahagian B: Kecekapan" },
        { id: 71, text: "Memahami fungsi tiub hampagas", type: "I", section: "Bahagian B: Kecekapan" },
        { id: 91, text: "Menerangkan sesuatu dengan jelas", type: "S", section: "Bahagian B: Kecekapan" },
        
        // Bahagian C
        { id: 121, text: "Mekanik Kapalterbang", type: "R", section: "Bahagian C: Nama Pekerjaan" },
        { id: 133, text: "Ahli Kajicuaca", type: "I", section: "Bahagian C: Nama Pekerjaan" }
    ];

    // --- Generate the Form ---
    const container = document.getElementById('questionnaire');
    let currentSection = "";

    questions.forEach(q => {
        if (q.section !== currentSection) {
            currentSection = q.section;
            container.innerHTML += `<h2 class="section">${currentSection}</h2>`;
        }

        container.innerHTML += `
            <div class="question-item">
                <input type="checkbox" id="q${q.id}" value="${q.type}">
                <label for="q${q.id}">${q.id}. ${q.text}</label>
            </div>
        `;
    });

    // --- Process Results ---
    function calculateResults() {
        // Initialize scores
        let scores = { "R": 0, "I": 0, "A": 0, "S": 0, "E": 0, "C": 0 };
        
        // Count checked boxes
        const checkboxes = document.querySelectorAll('input[type="checkbox"]:checked');
        checkboxes.forEach(box => {
            scores[box.value]++;
        });

        // Convert to array and sort descending
        let sortedScores = Object.keys(scores).map(key => {
            return { type: key, score: scores[key] };
        }).sort((a, b) => b.score - a.score);

        // Get top 3
        let summaryCode = sortedScores.slice(0, 3).map(item => item.type).join("");

        // Display Data
        document.getElementById('summary-code').innerText = "Kod Rumusan: " + summaryCode;
        
        let breakdownHTML = "";
        sortedScores.forEach(item => {
            breakdownHTML += `<div class="score-row"><span><strong>${item.type}:</strong></span> <span>${item.score}</span></div>`;
        });
        document.getElementById('score-breakdown').innerHTML = breakdownHTML;

        // Show results section
        document.getElementById('results').style.display = 'block';
        
        // Scroll to results
        document.getElementById('results').scrollIntoView({ behavior: 'smooth' });
    }
</script>

</body>
</html>