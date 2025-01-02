<script>
  // x + a = b
  // => x = a - b
  let a = 6;
  let b = 9;
  let solution = b - a;
  let isHidden = true;

  function generateRandomInt(min,max) {
    return Math.floor(min + Math.random()*(max-min + 1));
  }

  let newEquation = () => {
    a = generateRandomInt(1,32);
    b = generateRandomInt(1,32);
    solution = b - a;
    isHidden = true;
  }

  let showSolution = () => {
    isHidden = false;
  }
</script>
<style>
  .hidden {
    visibility: hidden;
  }
</style>


<h1>exercises</h1>
<button
  on:click={newEquation}
  >new equation</button>
<button
  on:click={showSolution}
  >show solution</button>

<p>x + {a} = {b}</p>
<p class:hidden={isHidden}>x = {b} - {a}</p>
<p class:hidden={isHidden}>x = {solution}</p>
