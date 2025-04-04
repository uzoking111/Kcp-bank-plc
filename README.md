# Kcp-bank-plc
Automated cheque clearing system 
Item details
Logo for Gemini Apps
Gemini Apps
Prompted Replicate this code to automation of the cheque clearing system
Attached 1 file.
- image.png
- image.png

Details
event
Today at 4:12 AM
apps
Gemini Apps
chat
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Automated Cheque Clearing System - Dashboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="header">
        <h1>Cheque Clearing Dashboard</h1>
    </header>

    <main class="container">
        <a href="index.html" class="home-button">Home</a>
        <a href="javascript:history.back()" class="back-button">Back</a>

        <div class="dashboard">
            <h2>System Overview</h2>

            <div class="dashboard-list">
                </div>

            <div class="dashboard-actions">
                <input type="text" id="filter-cheques" placeholder="Filter Cheques">
                <button onclick="applyFilter()">Apply Filter</button>

                <p>Total Cheques Processed: <span id="total-processed">0</span></p>

                <button onclick="clearDashboard()">Clear Dashboard</button>
                <button onclick="exportData()">Export Data</button>
            </div>
        </div>
    </main>

    <footer class="footer">
        <p>&copy; 2024 KCP BANK PLC</p>
    </footer>

    <script>
        let processedCheques = []; // Replace with actual data fetching

        function updateDashboard() {
            const dashboardList = document.getElementById('dashboard-list');
            const totalProcessedElement = document.getElementById('total-processed');

            dashboardList.innerHTML = '';
            totalProcessedElement.textContent = processedCheques.length;

            if (processedCheques.length === 0) {
                dashboardList.innerHTML = '<div>No cheques processed yet.</div>';
                return;
            }

            processedCheques.forEach(cheque => {
                const chequeItem = document.createElement('div');
                chequeItem.innerHTML = `
                    <p>Cheque ID: ${cheque.id}</p>
                    <p>Amount: ${cheque.amount}</p>
                    <p>Status: ${cheque.status}</p>
                `;
                dashboardList.appendChild(chequeItem);
            });
        }

        function applyFilter() {
            const filterValue = document.getElementById('filter-cheques').value.toLowerCase();
            // Implement filtering logic based on filterValue
            // Update processedCheques and call updateDashboard()
        }

        function clearDashboard() {
            processedCheques = [];
            updateDashboard();
        }

        function exportData() {
            // Implement data export functionality (e.g., download CSV)
        }

        // Simulate data loading (replace with actual data fetching)
        function loadData() {
            // Example data (replace with actual data)
            processedCheques = [
                { id: 'CHQ123', amount: 1000, status: 'Cleared' },
                { id: 'CHQ456', amount: 500, status: 'Pending' },
                { id: 'CHQ789', amount: 2000, status: 'Cleared' }
            ];
            updateDashboard();
        }

        loadData(); // Load initial data
    </script>
</body>
</html>
