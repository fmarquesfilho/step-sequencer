<script>
  let notes = Array(64).fill('');
</script>


<div class="sequencer">
  {#each notes as note, i}
  <div class="note {i == 0 ? 'active': ''}">{note}</div>
  {/each}
</div>

<style>
  .sequencer {
    display: grid;
    grid-template-columns: repeat(16, 1fr);
    grid-gap: 5px;
    width: 100%;
  }

  .note {
    background: #ccc;
    width: 50px;
    height: 50px;
    border: 1px solid #ccc;
    border-radius: 7px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2rem;
  }

  .note.active {
    background: #600889;
    border: 1px solid #600889;
    color: #fff;
  }
</style>
