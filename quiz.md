---
layout: page
title: 'Book Search Quiz: Using Pounce and UofM Databases'
---

<style>
	@import url('https://fonts.googleapis.com/css?family=Montserrat');

	input {
		margin-right: 5px;
	}

	.allContainer {
		margin: 0 auto;
		font-size: 16px;
		padding: 20px;
	}
	
	.text {
		font-family: 'Montserrat', sans-serif;
	}

	.questions {

	}

	.buttonContainer {
		text-align: center;
	}

	#quiz {

	}

	#submit {
		color: white;
		padding: 10px;
		background: #7a0019;
		border-radius: 30px;
	}

	#results {

	}

</style>

<div class="allContainer">
	<div class="questions text" id="quiz"></div>
	<div class=buttonContainer>
		<button class="text" id="submit">Get Results</button>
	</div>
	<div class="text" id="results"></div>
</div>

<script>
  var myQuestions = [
	  {
		question: "PLACEHOLDER_TEXT",
		answers: {
			a: "Yes, we have that!",
		  	b: "Sorry, we don't have that!",
		  	c: "It looks like they have that at another campus"
	  	},
	  	correctAnswer: 'b'
  	},
  	{
	  	question: "PLACEHOLDER_TEXT",
	  	answers: {
	  		a: "Yes, we have that!",
		  	b: "Sorry, we don't have that!",
		  	c: "It looks like they have that at another campus"
	  	},
  		correctAnswer: 'c'
	  }
  ];
  
  var quizContainer = document.getElementById('quiz');
  var resultsContainer = document.getElementById('results');
  var submitButton = document.getElementById('submit');
  
  function generateQuiz(questions, quizContainer, resultsContainer, submitButton){

	  function showQuestions(questions, quizContainer){
		  // we'll need a place to store the output and the answer choices
	    var output = [];
	    var answers;

	    // for each question...
	    for(var i=0; i<questions.length; i++){
		
		    // first reset the list of answers
		    answers = [];

		    // for each available answer to this question...
		    for(letter in questions[i].answers){

			    // ...add an html radio button
			    answers.push(
				    '<label>'
				    	+ '<input type="radio" name="question'+i+'" value="'+letter+'">'
				    	+ letter + ': '
				    	+ questions[i].answers[letter]
			    + '</label>'
			    );
		    }

		    // add this question and its answers to the output
		    output.push(
			    '<div class="question">' + questions[i].question + '</div>'
			    + '<div class="answers">' + answers.join('') + '</div>'
		    );
	    }

	    // finally combine our output list into one string of html and put it on the page
	    quizContainer.innerHTML = output.join('');
	      }

	  function showResults(questions, quizContainer, resultsContainer){
	
	    // gather answer containers from our quiz
	    var answerContainers = quizContainer.querySelectorAll('.answers');
	
	    // keep track of user's answers
	    var userAnswer = '';
	    var numCorrect = 0;
	
	    // for each question...
	    for(var i=0; i<questions.length; i++){

		    // find selected answer
		    userAnswer = (answerContainers[i].querySelector('input[name=question'+i+']:checked')||{}).value;
		
		    // if answer is correct
		    if(userAnswer===questions[i].correctAnswer){
		    	// add to the number of correct answers
		    	numCorrect++;
			
		    	// color the answers green
		    	answerContainers[i].style.color = 'lightgreen';
	    	}
	    	// if answer is wrong or blank
	    	else{
		    	// color the answers red
		    	answerContainers[i].style.color = 'red';
		    }
	    }

	    // show number of correct answers out of total
	    resultsContainer.innerHTML = numCorrect + ' out of ' + questions.length;
    }

	    // show the questions
	    showQuestions(questions, quizContainer);

	    // when user clicks submit, show results
	    submitButton.onclick = function(){
       showResults(questions, quizContainer, resultsContainer);
	      }
      }
  generateQuiz(myQuestions, quizContainer, resultsContainer, submitButton);
        </script>
