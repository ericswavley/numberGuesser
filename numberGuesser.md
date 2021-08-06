# numberGuesser

let humanScore = 0;
let computerScore = 0;
let currentRoundNumber = 1;

const generateTarget = () =>{
  return Math.floor(Math.random() * 10);
}
const compareGuesses = (userGuess, computerGuess, targetGuess) =>{
  const userDifference = Math.abs(targetGuess - userGuess)
  const computerDifference = Math.abs(targetGuess - computerGuess)
  return userDifference <= computerDifference;
};

const updateScore = (winner) =>{
  if(winner === 'You win'){
    userScore++;
  }else if (winner === 'You lost'){
    computerScore++;
    }
};

const advanceRound = () =>{ currentRoundNumber++; }