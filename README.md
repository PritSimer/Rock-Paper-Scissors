# Rock-Paper-Scissors
Conditionals // codecademy js beginners practice project
const getUserChoice = (userInput) => {

userInput=userInput.toLowerCase();

if (userInput === 'bomb'){
  return userInput;
} else if (userInput === 'rock') {
  return userInput;
} else if (userInput === 'paper') {
  return userInput;
} else if(userInput === 'scissors') {
  return userInput;
}
else {
  console.log('That is not valid.')
}
};



function getComputerChoice() {
getRandomNumber = Math.floor(Math.random()*3);

if (getRandomNumber === 0) {
 let computerChoice = 'rock';
  return computerChoice;
} else if (getRandomNumber === 1) {
let computerChoice = 'paper';
return computerChoice;
} else if (getRandomNumber === 2) {
  let computerChoice = 'scissors'
  return computerChoice;

} else {
  console.log('not a valid entry');
}

};


function determineWinner(userChoice, computerChoice) {

 if (userChoice === 'bomb') {
    let winner = 'You are a winner ! No matter what !';
    return winner;
 }


  if (userChoice === computerChoice) {
    let tie = 'The game was a tie';
    return tie;
  }
  
  if (userChoice === 'rock') {

  if (computerChoice === 'paper'){
  let computerWon = 'The computer won!';
  return computerWon;
   } 
  } 
  if (userChoice === 'rock' && computerChoice === 'scissors'){
    let userWon = 'The user won!';
    return userWon;
    }

   if (userChoice === 'paper') {

   if (computerChoice === 'scissors'){
   let computerWon = 'The computer won!';
   return computerWon;
   }
   }
    if (userChoice === 'paper' && computerChoice === 'rock'){
    let userWon = 'The user won!';
    return userWon;
    }
   
   
    if (userChoice === 'scissors'){
    if (computerChoice === 'rock') {
    let computerWon = 'The computer won!';
    return computerWon;
    }
    }
    if (userChoice === 'scissors' && computerChoice ==='paper'){
      let userWon = 'The user won!';
      return userWon;
    } 

};
 


//console.log(determineWinner('paper', 'rock'));


function playGame (){
const userChoice = getUserChoice('paper');
const computerChoice = getComputerChoice();
console.log('You threw: '+userChoice);
console.log('The computer threw: '+computerChoice);
console.log(determineWinner(userChoice, computerChoice));
};

playGame();


