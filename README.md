<html lang="ko">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title></title>
</head>
<style>
    .wrapper {
        display: flex;
        align-items: center;
        height: calc(100vh - 100px);
        background-color: #5800FD;
        color: #03F3B3;
    }

    .container {
        width: 100%;
        text-align: center;
        font-size: 200%;
    }

    .container iframe {
        margin-top: 40px;
    }
</style>
<body>
    <div class="wrapper">
        <div class="container">
            <h1></h1>
            <h3>2023년 새해까지</h3>
            <div id="count">0일 0시간 0분 0초 남음</div>
        </div>        
    </div>
</body>
</html>
<script>
    const goalDate = new Date("2024-12-09").getTime();

    function calcDate() {
        const now = new Date().getTime();
        distance = now - goalDate +2;
        

        var days = Math.floor(distance / (1000*60*60*24));
        #var hours = Math.floor((distance % (1000*60*60*24)) / (1000*60*60));
        #var minutes = Math.floor((distance % (1000*60*60)) / (1000*60));
        #var seconds = Math.floor((distance % (1000*60)) / 1000);

        if (distance < 0) {
            return '${days}일';
        } else {
            return `${days}일`;
        }
    }
    
    setInterval(() => {
        document.getElementById('count').innerText = calcDate();
    }, 1000);

</script>
