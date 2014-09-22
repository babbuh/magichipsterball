<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Magic 8 Ball</title>
<style>
#eight-ball{
    width:500px;
    margin: 0 auto;
    text-align: center;
    
}
</style>
</head>

<body bgcolor="#E6E6FA">


    <div id="eight-ball">
        <button onclick="shake()">Shake</button>
        <p id="question"></p>
        <p id="answer"></p>
    <div>

</body>

<script>

    // Called when we click the shake button 
    function shake(){
        // The question we asked
        var question = prompt("Ask me a question");
        var questionText = document.getElementById('question');
        questionText.innerHTML = question;

        // Number of possible answers  
        var numberOfAnswers = 6;

        // Answers the 8 Ball can return
        var answerOne = 'Love, it will not betray you, dismay or enslave you, it will set you free. <br> Mumford & Sons';
        var answerTwo = 'This ship will carry our bodies safe to shore. <br> Of Monster and Men';      
		var answerThree = 'If Heaven and Hell decide that they both are satisfied. <br> Death Cab for Cutie';
        var answerFour = 'Realize I am to blame, but fever let me play the game. <br> The Black Keys'; 
		var answerFive = 'For now I can only guess what is coming next by examining your timid smile. <br> First Aid Kit';
        var answerSix = 'Shake it out, shake it out, shake it out. <br> Florence and The Machine'; 
        var answerSeven = 'I say dont you know. You say you dont know. I say... take me out! <br> Franz Ferdinand'; 
        var answerEight = 'See, people they dont understand. No, girlfriends, they cant understand Your grandsons, they wont understand. <br> The Strokes'; 


        // Answer returned by our 8 Ball
        var chosenAnswer = getAnswerNumber(numberOfAnswers);        
        displayAnswer(chosenAnswer);

        // Returns a number based on the number of sides
        function getAnswerNumber(answerCount){
            var number = getRandomInt(1,answerCount);
            return number;
        }

        // Returns a random integer between two numbers
        function getRandomInt(min,max){
            return Math.floor(Math.random() * (max - min + 1)) + min;
        }

        // Show our answer in the document 
        function displayAnswer(answer) {

            // Access the DOM element we want to to change
            var fortuneText = document.getElementById('answer');

            if ( answer == 1 ) {
                fortuneText.innerHTML = answerOne;
            }
            else if ( answer == 2 ) {
                fortuneText.innerHTML = answerTwo;
            }
            
            if ( answer == 3 ) {
                fortuneText.innerHTML = answerThree;
            }
           	
           	else if ( answer == 4 ) {
                fortuneText.innerHTML = answerFour;
            }
           
            if ( answer == 5 ) {
                fortuneText.innerHTML = answerFive;
            }
           
           	else if ( answer == 6 ) {
                fortuneText.innerHTML = answerSix;
            }
           
           
            if ( answer == 7 ) {
                fortuneText.innerHTML = answerSeven;
            }
           	
           	else if ( answer == 8 ) {
                fortuneText.innerHTML = answerEight;
            }
           
        
            
        }

    }
</script>

</html>
