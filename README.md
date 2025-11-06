# Ex06 BMI Calculator
## Date:

## AIM
To create a BMI calculator using React Router 

## ALGORITHM
### STEP 1 State Initialization
Manage the current page (Home or Calculator) using React Router.

### STEP 2 User Input
Accept weight and height inputs from the user.

### STEP 3 BMI Calculation
Calculate the BMI based on user input.

### STEP 4 Categorization
Classify the BMI result into categories (Underweight, Normal weight, Overweight, Obesity).

### STEP 5 Navigation
Navigate between pages using React Router.

## STEP 6: Display Result
Show calculated BMI.
Show category based on BMI range:
Underweight, Normal, Overweight, Obese, etc.
## STEP 7: Navigation Options
Provide a button to go back to the BMI form to calculate again.
## STEP 8: Enhancements
Add styling using CSS or Tailwind.

## PROGRAM
## APP.JS
```
import React, { useState } from 'react';
import './App.css';

function App() {
  const [weight, setWeight] = useState('');
  const [height, setHeight] = useState('');
  const [bmi, setBmi] = useState(null);

  const calculateBMI = () => {
    const w = parseFloat(weight);
    const h = parseFloat(height) / 100;
    if (w > 0 && h > 0) {
      const result = w / (h * h);
      setBmi(result.toFixed(2));
    } else {
      alert("Please enter valid weight and height.");
    }
  };

  return (
    <div className="container">
      <h1>BMI Calculator</h1>
      <input
        type="number"
        placeholder="Weight (kg)"
        value={weight}
        onChange={(e) => setWeight(e.target.value)}
      />
      <input
        type="number"
        placeholder="Height (cm)"
        value={height}
        onChange={(e) => setHeight(e.target.value)}
      />
      <button onClick={calculateBMI}>Calculate BMI</button>
      {bmi && <h3>Your BMI is: {bmi}</h3>}
      <footer>
        <p>Created by : NARRA RAMYA</p>
        <p>Reg No: 212223040128</p>
      </footer>
    </div>
  );
}

export default App;
```
## APP.CSS
```
body {
  margin: 0;
  padding: 0;
  font-family: sans-serif;
  background-image: url('https://images.pexels.com/photos/1103970/pexels-photo-1103970.jpeg?cs=srgb&dl=pexels-jplenio-1103970.jpg&fm=jpg'); /* or any URL */
  background-size: cover;
  background-position: center;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  background: whitesmoke; /* semi-transparent white */
  padding: 30px 40px;
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 4px 8px rgba(0,0,0,0.3);
  width: 300px;
}


.container h1 {
  margin-bottom: 20px;
}

input {
  width: 100%;
  padding: 10px;
  margin: 10px 0;
  color:black;
}

button {
  padding: 10px 15px;
  margin-top: 10px;
  cursor: pointer;
  color:black;
}

footer {
  margin-top: 20px;
  font-size: 12px;
  color: black;
}



```
## OUTPUT

<img width="803" height="447" alt="image" src="https://github.com/user-attachments/assets/4aaa4a6d-2103-4e86-ad22-28c64356e1c9" />



## RESULT
The program for creating BMI Calculator using React Router is executed successfully.
