<script lang="ts">
  import Chapter from "./Chapter.svelte";
  import ChapterA from "./levels/chapter-A";
  import ChapterB from "./levels/chapter-B";
  import ChapterC from "./levels/chapter-C";
  import ChapterD from "./levels/chapter-D";
  import ChapterE from "./levels/chapter-E";
</script>

<main class="points">
  <div>
    <h1>244/244</h1>
    <img src="/img/skill_point.png" alt="skill_point" />
  </div>
  <div>
    <h1>45/45</h1>
    <img src="/img/exploration_point.png" alt="exploration_point" />
  </div>
</main>

<main class="levels">
  <Chapter id="A" levels={ChapterA} />
  <Chapter id="B" levels={ChapterB} />
  <Chapter id="C" levels={ChapterC} />
  <Chapter id="D" levels={ChapterD} />
  <Chapter id="E" levels={ChapterE} />
</main>

<style lang="scss">
  .points {
    position: fixed;
    left: 50%;
    top: 1rem;
    transform: translateX(-50%);
    display: flex;
    gap: 5rem;
    align-items: center;
    div {
      display: flex;
      gap: 0.75rem;
      align-items: center;
      justify-content: center;
      h1 {
        font-size: 1.25rem;
        margin-top: 0.25rem;
        filter: drop-shadow(0 0 8px #8c82d8);
      }
      img {
        filter: drop-shadow(0 0 8px #8c82d8);
      }
    }
  }

  .levels {
    height: 100%;
    width: 100%;
    margin-top: 4rem;
    display: flex;
    gap: 2rem;
    align-items: center;
    max-width: 100%;
    margin-left: auto;
  }
</style>
