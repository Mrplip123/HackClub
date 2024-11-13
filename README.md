<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Supa Sigma Spelling</title>
</head>
<body>
    <script>
    let points = 0;
    let names = []; 
    function Sigma() { 
        if (names.length === 0)
        { names = Array.from(document.querySelectorAll('#promptlist li')).map(li => li.textContent); 
        if (names.length === 0) { alert("Your score was: " + points + "/10. Well Done!"); 
        return; 
        }} 
        const index = Math.floor(Math.random() * names.length); 
        const Result = names[index]; 
        const SplitRes = Result.split(": ")[1]; 
        const BrokeRes = (Result.split(": ")[0]).toLowerCase(); 
        var answer = prompt(SplitRes); 
        if (answer.toLowerCase() === BrokeRes) { alert("Correct"); 
        points += 1;
        } else { alert("Wrong, it was: " + BrokeRes)} names.splice(index, 1);
        document.querySelectorAll('#promptlist li')[index].remove(); 
        Sigma(); }
    </script>
    <style>
    body{
        background-color: aquamarine;
    }
    h1{
        text-align: center;
    }
    h4{
        text-align: center;
    }
    button{
        margin: auto;
        color: rgb(115, 38, 171);
        height: 7vh;
        width: 14vh;
        margin-left: 590px;
    }
    .buttons{
        display: flex;
        justify-content: center; 
        align-items: center; 
        height: 100vh;
    }
    ul{
        display: none;
    }
    </style>
    <ul id="promptlist">
        <li>Suspense: A feeling of excitement or worry about what will happen next in a story or situation.</li>
        <li>Ancient: Very old; from a long time ago, often referring to things that are thousands of years old.</li>
        <li>Decent: Good enough; acceptable and proper, showing respect for others.</li>
        <li>Intelligence: The ability to gain and apply knowledge; secret information acquired by the military or government agency.</li>
        <li>Confidence: Believing in yourself and your abilities; feeling sure about something.</li>
        <li>Evidence: Facts or information that help prove something is true or not true.</li>
        <li>Permanent: Lasting forever; not meant to be changed or removed.</li>
        <li>Current: Happening now; the present time.</li>
        <li>Obedience: Following rules or orders from someone in charge.</li>
        <li>Dispense: To give out or distribute something, like supplies or information.</li>
    </ul>
    <h1>Supa Sigma Spelling App</h1>
    <h4>       By: Adi         </h4>
    <div .buttons>
        <button onclick="Sigma()">Play</button>
        <button><a href="../pages/Aboutme.html">About me</a></button>
    </div>
</body>
</html>
