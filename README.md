****ELECTRICITY USAGE TRACJER (SDG 7)****

INTRODUCTION :

The Electricity Usage Tracker is a Python-based program used to monitor daily electricity consumption.

FEATURES :

🔹Input daily electricity usage.

🔹Set usage limit.

🔹Display daily usage report.

🔹Calculate total and average usage.

🔹Alert when usage exceeds limit ⚠️.

🔹Promote energy saving.

HOW TO RUN :

🔹Step 1:

Open Python IDLE.

🔹Step 2:

Copy the code and paste it.

🔹Step 3:

Save as 👉 electricity.py.

🔹Step 4:

Click Run (F5).

🔹Step 5:

Enter inputs when asked:

PROGRAM :

```
<!DOCTYPE html>
<html>
<head>
    <title>Electricity Tracker</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
    <h2>Electricity Usage Tracker</h2>

    <input type="number" id="usage" placeholder="Enter usage">
    <button onclick="addUsage()">Add</button>
    <button onclick="showReport()">Show Report</button>

    <pre id="output"></pre>

    <canvas id="myChart" width="400" height="200"></canvas>

    <script>
        let data = [];
        let limit = 10;
        let chart;

        function addUsage() {
            let val = Number(document.getElementById("usage").value);
            data.push(val);
            alert("Added!");
        }

        function showReport() {
            let total = 0;
            let result = "";

            data.forEach((val, i) => {
                result += "Day " + (i+1) + ": " + val + " units\n";
                total += val;
                if (val > limit) result += "High usage!\n";
            });

            let avg = total / data.length;
            result += "\nTotal: " + total;
            result += "\nAverage: " + avg.toFixed(2);

            document.getElementById("output").innerText = result;

            drawGraph();
        }

        function drawGraph() {
            let ctx = document.getElementById('myChart').getContext('2d');

            if (chart) chart.destroy();

            chart = new Chart(ctx, {
                type: 'line',
                data: {
                    labels: data.map((_, i) => "Day " + (i+1)),
                    datasets: [{
                        label: 'Units Consumed',
                        data: data,
                        borderWidth: 2
                    }]
                }
            });
        }
    </script>
</body>
</html>
```

OUTPUT :

<img width="1863" height="972" alt="image" src="https://github.com/user-attachments/assets/19bdb4c9-855a-453b-9ca9-536bffd6686c" />

RESULT :

The Electricity Usage Tracker is a Python-based program used to monitor daily electricity consumption was successfully completed. 
