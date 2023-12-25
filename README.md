<!DOCTYPE html>
<html>
<head>
    <title>Prop Bet Calculator</title>
    <script>
        function hH() {
            var v = parseFloat(document.getElementById("hh").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("hr").innerHTML = "Horn Bet High Side: " + ((7 * v) - (v / 4));
            updateSum();
        }

        function hL() {
            var v = parseFloat(document.getElementById("hl").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("lr").innerHTML = "Horn Bet Low Side: " + 3 * v;
            updateSum();
        }

        function cY() {
            var v = parseFloat(document.getElementById("cy").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("yr").innerHTML = "C/E Yo: " + 7 * v;
            updateSum();
        }

        function cC() {
            var v = parseFloat(document.getElementById("cc").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("cr").innerHTML = "C/E Craps: " + 3 * v;
            updateSum();
        }

        function tL() {
            var v = parseFloat(document.getElementById("3l").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("3lr").innerHTML = "3 Way Low Side: " + (4 * v + v / 3);
            updateSum();
        }

        function tH() {
            var v = parseFloat(document.getElementById("3h").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("3hr").innerHTML = "3 Way High Side: " + (9 * v + v / 3);
            updateSum();
        }

        function twoHigh() {
            var v = parseFloat(document.getElementById("2h").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("2hr").innerHTML = "2-Way High: " + (10 * v * 1.5 - v / 2);
            updateSum();
        }

        function twoLow() {
            var v = parseFloat(document.getElementById("2l").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("2lr").innerHTML = "2-Way Low: " + 7 * v;
            updateSum();
        }

        function hornHighLow() {
            var v = parseFloat(document.getElementById("hhl").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("hhlr").innerHTML = "Horn High Low: " + (2 * v + v / 5);
            updateSum();
        }

        function worldLow() {
            var v = parseFloat(document.getElementById("wl").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("wlr").innerHTML = "World Low: " + (2 * v + v / 5);
            updateSum();
        }

        function hornHigh() {
            var v = parseFloat(document.getElementById("hhg").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("hhgr").innerHTML = "Horn High: " + (5 * v + v / 5);
            updateSum();
        }

        function worldHigh() {
            var v = parseFloat(document.getElementById("wh").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("whr").innerHTML = "World High: " + (5 * v + v / 5);
            updateSum();
        }

        function hornHighLowHits() {
            var v = parseFloat(document.getElementById("hhlh").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("hhlhr").innerHTML = "Horn High Low Hits: " + (5 * v + (2 * v / 5));
            updateSum();
        }

        function hornHighHighHits() {
            var v = parseFloat(document.getElementById("hhhh").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("hhhhr").innerHTML = "Horn High High Hits: " + (11 * v + (2 * v / 5));
            updateSum();
        }

        // New functions for Any Seven, Any Craps, and Yo Eleven
        function anySeven() {
            var v = parseFloat(document.getElementById("anySeven").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("anySevenResult").innerHTML = "Any Seven: " + (4 * v);
            updateSum();
        }

        function anyCraps() {
            var v = parseFloat(document.getElementById("anyCraps").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("anyCrapsResult").innerHTML = "Any Craps: " + (7 * v);
            updateSum();
        }

        function yoEleven() {
            var v = parseFloat(document.getElementById("yoEleven").value);
            isNaN(v) ? alert("Invalid") : document.getElementById("yoElevenResult").innerHTML = "Yo Eleven: " + (15 * v);
            updateSum();
        }

        function updateSum() {
            var sum = 0;
            var resultIds = ["hr", "lr", "yr", "cr", "3lr", "3hr", "2hr", "2lr", "hhlr", "wlr", "hhgr", "whr", "hhlhr", "hhhhr", "anySevenResult", "anyCrapsResult", "yoElevenResult"];
            for (var i = 0; i < resultIds.length; i++) {
                var resultValue = parseFloat(document.getElementById(resultIds[i]).textContent.split(": ")[1]);
                if (!isNaN(resultValue)) {
                    sum += resultValue;
                }
            }
            document.getElementById("sum").innerHTML = "Total Payout: " + sum;
        }
    </script>
</head>
<body>
    <h1>Prop Bet Calculator</h1>
    <input type="text" id="hh" placeholder="Horn Bet High Side"><button onclick="hH()">HIT</button><p id="hr"></p>
    <input type="text" id="hl" placeholder="Horn Bet Low Side"><button onclick="hL()">HIT</button><p id="lr"></p>
    <input type="text" id="cy" placeholder="C/E Yo 11 Hits"><button onclick="cY()">HIT</button><p id="yr"></p>
    <input type="text" id="cc" placeholder="C/E Craps Hit"><button onclick="cC()">HIT</button><p id="cr"></p>
    <input type="text" id="3l" placeholder="3 Way Low Side"><button onclick="tL()">HIT</button><p id="3lr"></p>
    <input type="text" id="3h" placeholder="3 Way High Side"><button onclick="tH()">HIT</button><p id="3hr"></p>
    <!-- New calculations -->
    <input type="text" id="2h" placeholder="2 Way High Side"><button onclick="twoHigh()">HIT</button><p id="2hr"></p>
    <input type="text" id="2l" placeholder="2 Way Low Side"><button onclick="twoLow()">HIT</button><p id="2lr"></p>
    <input type="text" id="hhl" placeholder="Horn High LowSide"><button onclick="hornHighLow()">HIT</button><p id="hhlr"></p>
    <input type="text" id="wl" placeholder="World Bet Low Side"><button onclick="worldLow()">HIT</button><p id="wlr"></p>
    <input type="text" id="hhg" placeholder="Horn High Side"><button onclick="hornHigh()">HIT</button><p id="hhgr"></p>
    <input type="text" id="wh" placeholder="World Bet High Side"><button onclick="worldHigh()">HIT</button><p id="whr"></p>
    <input type="text" id="hhlh" placeholder="Horn High Low Hits"><button onclick="hornHighLowHits()">HIT</button><p id="hhlhr"></p>
    <input type="text" id="hhhh" placeholder="Horn High High Hits"><button onclick="hornHighHighHits()">HIT</button><p id="hhhhr"></p>
    
    <!-- New inputs for Any Seven, Any Craps, and Yo Eleven -->
    <input type="text" id="anySeven" placeholder="Any Seven"><button onclick="anySeven()">HIT</button><p id="anySevenResult"></p>
    <input type="text" id="anyCraps" placeholder="Any Craps"><button onclick="anyCraps()">HIT</button><p id="anyCrapsResult"></p>
    <input type="text" id="yoEleven" placeholder="Yo Eleven"><button onclick="yoEleven()">HIT</button><p id="yoElevenResult"></p>

    <div id="sum"></div>
</body>
</html>
