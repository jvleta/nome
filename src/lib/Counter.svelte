<script lang="ts">
  let count: number = 0
  const increment = () => {
    count += 1
    const click = <HTMLVideoElement> document.getElementById("metronome-beat"); 
    click.play(); 
  }
  const bpm = 80;
  setInterval(increment, (bpm / 60) * 1000);
</script>

<audio id="metronome-beat">
  <source src="/metronome-beat.mp3" type="audio/mpeg">
</audio>

<button on:click={increment}>
  count is {count}
</button>


