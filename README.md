# 2.O-severity-and-case-Assessment-2.   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Case Classification Sheet</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #f4f6f9;
            color: #222;
            padding: 30px;
        }

        .container {
            max-width: 1100px;
            margin: auto;
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 5px 25px rgba(0,0,0,0.08);
        }

        .header {
            text-align: center;
            border-bottom: 2px solid #222;
            padding-bottom: 20px;
            margin-bottom: 25px;
        }

        .header h1 {
            font-size: 28px;
            margin-bottom: 8px;
        }

        .header p {
            color: #666;
            font-size: 14px;
        }

        .section {
            margin-bottom: 25px;
        }

        .section-title {
            background: #1f2937;
            color: white;
            padding: 10px 14px;
            font-size: 16px;
            font-weight: bold;
            margin-bottom: 15px;
            border-radius: 6px;
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 16px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .full {
            grid-column: 1 / -1;
        }

        label {
            font-weight: bold;
            margin-bottom: 6px;
            font-size: 14px;
        }

        input,
        select,
        textarea {
            width: 100%;
            padding: 11px;
            border: 1px solid #cbd5e1;
            border-radius: 6px;
            font-size: 14px;
            outline: none;
        }

        input:focus,
        select:focus,
        textarea:focus {
            border-color: #2563eb;
        }

        textarea {
            min-height: 100px;
            resize: vertical;
        }

        .classification {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
        }

        .classification-card {
            border: 1px solid #ddd;
            padding: 15px;
            border-radius: 8px;
        }

        .classification-card h3 {
            font-size: 14px;
            margin-bottom: 8px;
        }

        .buttons {
            display: flex;
            gap: 12px;
            margin-top: 25px;
        }

        button {
            border: none;
            padding: 12px 22px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: bold;
            font-size: 14px;
        }

        .submit-btn {
            background: #2563eb;
            color: white;
        }

        .reset-btn {
            background: #e5e7eb;
            color: #111827;
        }

        .print-btn {
            background: #111827;
            color: white;
        }

        button:hover {
            opacity: 0.88;
        }

        .result {
            display: none;
            margin-top: 25px;
            padding: 18px;
            border-radius: 8px;
            background: #f0fdf4;
            border: 1px solid #86efac;
        }

        .result h3 {
            margin-bottom: 10px;
        }

        .result p {
            margin: 5px 0;
            font-size: 14px;
        }

        @media (max-width: 700px) {

            body {
                padding: 12px;
            }

            .container {
                padding: 18px;
            }

            .form-grid,
            .classification {
                grid-template-columns: 1fr;
            }

            .full {
                grid-column: auto;
            }

            .buttons {
                flex-direction: column;
            }

            button {
                width: 100%;
            }
        }

        @media print {

            body {
                background: white;
                padding: 0;
            }

            .container {
                box-shadow: none;
                max-width: 100%;
            }

            .buttons {
                display: none;
            }

            input,
            select,
            textarea {
                border: 1px solid #999;
            }
        }
    </style>
</head>

<body>

<div class="container">

    <div class="header">
        <h1>CASE CLASSIFICATION SHEET</h1>
        <p>Case Information & Classification Record</p>
    </div>

    <!-- CASE DETAILS -->

    <div class="section">

        <div class="section-title">
            1. CASE DETAILS
        </div>

        <div class="form-grid">

            <div class="form-group">
                <label>Case ID / Reference No.</label>
                <input type="text" id="caseId" placeholder="Enter case ID">
            </div>

            <div class="form-group">
                <label>Date</label>
                <input type="date" id="caseDate">
            </div>

            <div class="form-group">
                <label>Client / Party Name</label>
                <input type="text" id="clientName" placeholder="Enter name">
            </div>

            <div class="form-group">
                <label>Assigned Officer</label>
                <input type="text" id="officer" placeholder="Enter officer name">
            </div>

            <div class="form-group">
                <label>Department</label>
                <select id="department">
                    <option value="">Select Department</option>
                    <option>Legal</option>
                    <option>Compliance</option>
                    <option>Finance</option>
                    <option>Human Resources</option>
                    <option>Operations</option>
                    <option>Other</option>
                </select>
            </div>

            <div class="form-group">
                <label>Case Status</label>
                <select id="status">
                    <option value="">Select Status</option>
                    <option>Open</option>
                    <option>Under Review</option>
                    <option>Pending</option>
                    <option>Resolved</option>
                    <option>Closed</option>
                </select>
            </div>

        </div>

    </div>


    <!-- CLASSIFICATION -->

    <div class="section">

        <div class="section-title">
            2. CASE CLASSIFICATION
        </div>

        <div class="classification">

            <div class="classification-card">

                <h3>Case Type</h3>

                <select id="caseType">

                    <option value="">Select Type</option>
                    <option>Administrative</option>
                    <option>Financial</option>
                    <option>Legal</option>
                    <option>Technical</option>
                    <option>Customer Complaint</option>
                    <option>Other</option>

                </select>

            </div>


            <div class="classification-card">

                <h3>Priority</h3>

                <select id="priority">

                    <option value="">Select Priority</option>
                    <option>Low</option>
                    <option>Medium</option>
                    <option>High</option>
                    <option>Critical</option>

                </select>

            </div>


            <div class="classification-card">

                <h3>Risk Level</h3>

                <select id="risk">

                    <option value="">Select Risk</option>
                    <option>Low Risk</option>
                    <option>Medium Risk</option>
                    <option>High Risk</option>

                </select>

            </div>

        </div>

    </div>


    <!-- DESCRIPTION -->

    <div class="section">

        <div class="section-title">
            3. CASE DESCRIPTION
        </div>

        <div class="form-grid">

            <div class="form-group full">

                <label>Case Description</label>

                <textarea
                    id="description"
                    placeholder="Enter detailed description of the case..."
                ></textarea>

            </div>

            <div class="form-group full">

                <label>Action / Resolution Required</label>

                <textarea
                    id="action"
                    placeholder="Enter required action or resolution..."
                ></textarea>

            </div>

            <div class="form-group full">

                <label>Additional Notes</label>

                <textarea
                    id="notes"
                    placeholder="Enter additional notes..."
                ></textarea>

            </div>

        </div>

    </div>


    <!-- BUTTONS -->

    <div class="buttons">

        <button class="submit-btn" onclick="submitCase()">
            Submit Case
        </button>

        <button class="reset-btn" onclick="resetForm()">
            Reset
        </button>

        <button class="print-btn" onclick="window.print()">
            Print Sheet
        </button>

    </div>


    <!-- RESULT -->

    <div class="result" id="result">

        <h3>Case Submitted Successfully</h3>

        <p><strong>Case ID:</strong> <span id="resultCaseId"></span></p>

        <p><strong>Client:</strong> <span id="resultClient"></span></p>

        <p><strong>Case Type:</strong> <span id="resultType"></span></p>

        <p><strong>Priority:</strong> <span id="resultPriority"></span></p>

        <p><strong>Risk:</strong> <span id="resultRisk"></span></p>

        <p><strong>Status:</strong> <span id="resultStatus"></span></p>

    </div>

</div>


<script>

function submitCase() {

    const caseId = document.getElementById("caseId").value;
    const client = document.getElementById("clientName").value;
    const type = document.getElementById("caseType").value;
    const priority = document.getElementById("priority").value;
    const risk = document.getElementById("risk").value;
    const status = document.getElementById("status").value;

    if (
        caseId === "" ||
        client === "" ||
        type === "" ||
        priority === "" ||
        risk === "" ||
        status === ""
    ) {

        alert("Please complete all required case classification fields.");

        return;
    }


    document.getElementById("resultCaseId").textContent = caseId;
    document.getElementById("resultClient").textContent = client;
    document.getElementById("resultType").textContent = type;
    document.getElementById("resultPriority").textContent = priority;
    document.getElementById("resultRisk").textContent = risk;
    document.getElementById("resultStatus").textContent = status;


    document.getElementById("result").style.display = "block";
}


function resetForm() {

    document.querySelectorAll("input, select, textarea").forEach(function(element) {

        element.value = "";

    });

    document.getElementById("result").style.display = "none";
}

</script>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Case Classification Sheet</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #f4f6f9;
            color: #222;
            padding: 30px;
        }

        .container {
            max-width: 1100px;
            margin: auto;
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 5px 25px rgba(0,0,0,0.08);
        }

        .header {
            text-align: center;
            border-bottom: 2px solid #222;
            padding-bottom: 20px;
            margin-bottom: 25px;
        }

        .header h1 {
            font-size: 28px;
            margin-bottom: 8px;
        }

        .header p {
            color: #666;
            font-size: 14px;
        }

        .section {
            margin-bottom: 25px;
        }

        .section-title {
            background: #1f2937;
            color: white;
            padding: 10px 14px;
            font-size: 16px;
            font-weight: bold;
            margin-bottom: 15px;
            border-radius: 6px;
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 16px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .full {
            grid-column: 1 / -1;
        }

        label {
            font-weight: bold;
            margin-bottom: 6px;
            font-size: 14px;
        }

        input,
        select,
        textarea {
            width: 100%;
            padding: 11px;
            border: 1px solid #cbd5e1;
            border-radius: 6px;
            font-size: 14px;
            outline: none;
        }

        input:focus,
        select:focus,
        textarea:focus {
            border-color: #2563eb;
        }

        textarea {
            min-height: 100px;
            resize: vertical;
        }

        .classification {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
        }

        .classification-card {
            border: 1px solid #ddd;
            padding: 15px;
            border-radius: 8px;
        }

        .classification-card h3 {
            font-size: 14px;
            margin-bottom: 8px;
        }

        .buttons {
            display: flex;
            gap: 12px;
            margin-top: 25px;
        }

        button {
            border: none;
            padding: 12px 22px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: bold;
            font-size: 14px;
        }

        .submit-btn {
            background: #2563eb;
            color: white;
        }

        .reset-btn {
            background: #e5e7eb;
            color: #111827;
        }

        .print-btn {
            background: #111827;
            color: white;
        }

        button:hover {
            opacity: 0.88;
        }

        .result {
            display: none;
            margin-top: 25px;
            padding: 18px;
            border-radius: 8px;
            background: #f0fdf4;
            border: 1px solid #86efac;
        }

        .result h3 {
            margin-bottom: 10px;
        }

        .result p {
            margin: 5px 0;
            font-size: 14px;
        }

        @media (max-width: 700px) {

            body {
                padding: 12px;
            }

            .container {
                padding: 18px;
            }

            .form-grid,
            .classification {
                grid-template-columns: 1fr;
            }

            .full {
                grid-column: auto;
            }

            .buttons {
                flex-direction: column;
            }

            button {
                width: 100%;
            }
        }

        @media print {

            body {
                background: white;
                padding: 0;
            }

            .container {
                box-shadow: none;
                max-width: 100%;
            }

            .buttons {
                display: none;
            }

            input,
            select,
            textarea {
                border: 1px solid #999;
            }
        }
    </style>
</head>

<body>

<div class="container">

    <div class="header">
        <h1>CASE CLASSIFICATION SHEET</h1>
        <p>Case Information & Classification Record</p>
    </div>

    <!-- CASE DETAILS -->

    <div class="section">

        <div class="section-title">
            1. CASE DETAILS
        </div>

        <div class="form-grid">

            <div class="form-group">
                <label>Case ID / Reference No.</label>
                <input type="text" id="caseId" placeholder="Enter case ID">
            </div>

            <div class="form-group">
                <label>Date</label>
                <input type="date" id="caseDate">
            </div>

            <div class="form-group">
                <label>Client / Party Name</label>
                <input type="text" id="clientName" placeholder="Enter name">
            </div>

            <div class="form-group">
                <label>Assigned Officer</label>
                <input type="text" id="officer" placeholder="Enter officer name">
            </div>

            <div class="form-group">
                <label>Department</label>
                <select id="department">
                    <option value="">Select Department</option>
                    <option>Legal</option>
                    <option>Compliance</option>
                    <option>Finance</option>
                    <option>Human Resources</option>
                    <option>Operations</option>
                    <option>Other</option>
                </select>
            </div>

            <div class="form-group">
                <label>Case Status</label>
                <select id="status">
                    <option value="">Select Status</option>
                    <option>Open</option>
                    <option>Under Review</option>
                    <option>Pending</option>
                    <option>Resolved</option>
                    <option>Closed</option>
                </select>
            </div>

        </div>

    </div>


    <!-- CLASSIFICATION -->

    <div class="section">

        <div class="section-title">
            2. CASE CLASSIFICATION
        </div>

        <div class="classification">

            <div class="classification-card">

                <h3>Case Type</h3>

                <select id="caseType">

                    <option value="">Select Type</option>
                    <option>Administrative</option>
                    <option>Financial</option>
                    <option>Legal</option>
                    <option>Technical</option>
                    <option>Customer Complaint</option>
                    <option>Other</option>

                </select>

            </div>


            <div class="classification-card">

                <h3>Priority</h3>

                <select id="priority">

                    <option value="">Select Priority</option>
                    <option>Low</option>
                    <option>Medium</option>
                    <option>High</option>
                    <option>Critical</option>

                </select>

            </div>


            <div class="classification-card">

                <h3>Risk Level</h3>

                <select id="risk">

                    <option value="">Select Risk</option>
                    <option>Low Risk</option>
                    <option>Medium Risk</option>
                    <option>High Risk</option>

                </select>

            </div>

        </div>

    </div>


    <!-- DESCRIPTION -->

    <div class="section">

        <div class="section-title">
            3. CASE DESCRIPTION
        </div>

        <div class="form-grid">

            <div class="form-group full">

                <label>Case Description</label>

                <textarea
                    id="description"
                    placeholder="Enter detailed description of the case..."
                ></textarea>

            </div>

            <div class="form-group full">

                <label>Action / Resolution Required</label>

                <textarea
                    id="action"
                    placeholder="Enter required action or resolution..."
                ></textarea>

            </div>

            <div class="form-group full">

                <label>Additional Notes</label>

                <textarea
                    id="notes"
                    placeholder="Enter additional notes..."
                ></textarea>

            </div>

        </div>

    </div>


    <!-- BUTTONS -->

    <div class="buttons">

        <button class="submit-btn" onclick="submitCase()">
            Submit Case
        </button>

        <button class="reset-btn" onclick="resetForm()">
            Reset
        </button>

        <button class="print-btn" onclick="window.print()">
            Print Sheet
        </button>

    </div>


    <!-- RESULT -->

    <div class="result" id="result">

        <h3>Case Submitted Successfully</h3>

        <p><strong>Case ID:</strong> <span id="resultCaseId"></span></p>

        <p><strong>Client:</strong> <span id="resultClient"></span></p>

        <p><strong>Case Type:</strong> <span id="resultType"></span></p>

        <p><strong>Priority:</strong> <span id="resultPriority"></span></p>

        <p><strong>Risk:</strong> <span id="resultRisk"></span></p>

        <p><strong>Status:</strong> <span id="resultStatus"></span></p>

    </div>

</div>


<script>

function submitCase() {

    const caseId = document.getElementById("caseId").value;
    const client = document.getElementById("clientName").value;
    const type = document.getElementById("caseType").value;
    const priority = document.getElementById("priority").value;
    const risk = document.getElementById("risk").value;
    const status = document.getElementById("status").value;

    if (
        caseId === "" ||
        client === "" ||
        type === "" ||
        priority === "" ||
        risk === "" ||
        status === ""
    ) {

        alert("Please complete all required case classification fields.");

        return;
    }


    document.getElementById("resultCaseId").textContent = caseId;
    document.getElementById("resultClient").textContent = client;
    document.getElementById("resultType").textContent = type;
    document.getElementById("resultPriority").textContent = priority;
    document.getElementById("resultRisk").textContent = risk;
    document.getElementById("resultStatus").textContent = status;


    document.getElementById("result").style.display = "block";
}


function resetForm() {

    document.querySelectorAll("input, select, textarea").forEach(function(element) {

        element.value = "";

    });

    document.getElementById("result").style.display = "none";
}

</script>

</body>
</html>
