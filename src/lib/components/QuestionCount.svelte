<div class="input-group">
  <button id="decrement" onclick="decrement()">-</button>
  <input type="number" id="input" value="1" readonly>
  <button id="increment" onclick="increment()">+</button>
  <script>
    let counter = 1;
  
    function increment() {
      if (counter!=10) {
      counter++;
      document.getElementById("input").value = counter;
      }
    }
  
    function decrement() {
      if (counter!=1) {
      counter--;
      document.getElementById("input").value = counter;
      }
    }
  
    function get() {
      return counter;
    }
  
    const inc = document.getElementById("increment");
  </script>
  
</div>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    background: linear-gradient(
      225deg,
      rgba(242, 113, 33, 1) 0%,
      rgba(233, 64, 87, 1) 47%,
      rgba(138, 35, 135, 1) 100%
    );
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0 1rem;
  }

  .input-group {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    box-shadow: 2px 3px 4px rgba(0, 0, 0, 0.3), 4px 7px 15px rgba(0, 0, 0, 0.2),
      9px 15px 25px rgba(0, 0, 0, 0.2);
    border-radius: 15px;
  }

  button,
  input {
    outline: none;
    border: none;
    padding: 16px;
    font-size: 18px;
  }

  input {
    text-align: center;
  }

  button {
    cursor: pointer;
  }

  button:nth-child(3) {
    border-bottom-right-radius: 15px;
    border-top-right-radius: 15px;
  }

  button:nth-child(1) {
    border-bottom-left-radius: 15px;
    border-top-left-radius: 15px;
  }

  button:hover {
    background-color: #e6e6e6;
  }

  button:nth-last-child(1):active {
    box-shadow: inset -4px 5px 10px rgba(0, 0, 0, 0.5);
  }

  button:nth-child(1):active {
    box-shadow: inset 4px 5px 10px rgba(0, 0, 0, 0.5);
  }
</style>
