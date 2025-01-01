<html lang="ko">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<style>
    .wrapper {
        display: flex;
        align-items: center;
        height: calc(100vh - 100px);
        background-color: #EDF2EC;
        color: #438261;
    }

    .container {
        width: 100%;
        text-align: center;
        font-size: 200%;
    }
</style>
<body>
    <div class="wrapper">
        <div class="container">
            <h1>청이와 총이</h1>
            <div id="count">D+??</div>
        </div>        
    </div>
</body>
</html>
<script>
    const goalDate = new Date("2024-12-09").getTime();

    function calcDate() {
        const now = new Date().getTime();
        const distance = now - goalDate;
        

        var days = Math.floor(distance / (1000*60*60*24))+2;
        //var hours = Math.floor((distance % (1000*60*60*24)) / (1000*60*60));
        //var minutes = Math.floor((distance % (1000*60*60)) / (1000*60));
        //var seconds = Math.floor((distance % (1000*60)) / 1000);

        if (distance < 0) {
            return 'D+${days}';
        } else {
            return `${days}일`;
        }
    }
    
    setInterval(() => {
        document.getElementById('count').innerText = calcDate();
    }, 1000);

</script>
