<!DOCTYPE html>
<html>
<head>
    <title>Online Voting System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .container {
            width: 50%;
            margin: 40px auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Online Voting System</h2>
        <form id="voting-form">
            <label for="candidate">Select a candidate:</label>
            <select id="candidate" name="candidate">
                <option value="ys jagan mohan">Jagan mohan ys</option>
                <option value="nara chandrababu ">chandra babu naidu</option>
                <option value="n pavan kalyan">pavan kalyan</option>
            </select>
            <button id="vote-btn">Cast Vote</button>
        </form>
        <div id="result"></div>
    </div>

    <script>
        const votingForm = document.getElementById('voting-form');
        const voteBtn = document.getElementById('vote-btn');
        const resultDiv = document.getElementById('result');

        let votes = {
            "ys jagan mohan": 0,
            "n chandra babu": 0,
            "k pavankalyan": 0
        };

        voteBtn.addEventListener('click', (e) => {
            e.preventDefault();
            const selectedCandidate = document.getElementById('candidate').value;
            votes[selectedCandidate]++;
            resultDiv.innerHTML = `You voted for ${selectedCandidate}. Current votes: ${JSON.stringify(votes)}`;
        });
    </script>
</body>
</html>
