<script lang="ts">
  import Teaching from './Teaching.svelte';
  import {BLOG_POSTS, PRESENTATIONS, PUBLICATIONS} from '../constants';
  import Publication from './Publication.svelte';
</script>

<h1>Andrew McNutt</h1>
<div>PhD Student at Univeristy of Chicago in Computer Science</div>
<div>For a pdf version of my CV <a href="./assets/cv.pdf">click here</a></div>

<section class="section">
  <h2>Education</h2>
  <h3>University of Chicago</h3>
  <div>PhD, Computer Science, 2017 - Present</div>
  <div>Advised by <a href="http://people.cs.uchicago.edu/~rchugh/">Ravi Chugh</a></div>
  <br />
  <h3>University of Chicago</h3>
  <div>MS, Computer Science, 2017 - 2019</div>
  <div>Advised by <a href="http://people.cs.uchicago.edu/~glk/">Gordon Kindlmann</a></div>
  <br />
  <h3>Reed College</h3>
  <div>BA, Physics, 2010 - 2014</div>
  <div>
    Advised by <a href="https://www.union.edu/physics-and-astronomy/faculty-staff/nelia-mann">Nelia Mann</a>
  </div>
</section>

<section class="section">
  <h2>Professional Experience</h2>
  <div>Research Intern at <a href="https://research.tableau.com/">Tableau Research</a>, 2019</div>
  <div>
    Graduate Researcher at <a href="https://computerscience.uchicago.edu/">University of Chicago</a>, 2017 -
  </div>
  <div>Data Visualization Engineer at <a href="https://vis.gl/">Uber</a>, 2015 - 2017</div>
  <div>
    Scientific Visualization Developer at <a href="https://www.collaborativedrug.com/"
      >Collaborative Drug Discovery</a
    >, 2014 - 2015
  </div>
  <div>Undergraduate Researcher at <a href="https://www.reed.edu/physics/">Reed College, 2013</a></div>
</section>

<section class="section cv-pubs">
  <h2>Publications</h2>
  <div class="research-section">
    {#each PUBLICATIONS as publication}
      <Publication {publication} noImg={true} />
    {/each}
  </div>
</section>

<!-- <section class="section">
  <h2>BLOG POSTS</h2>
  <div class="research-section">
    {#each BLOG_POSTS as publication}
      <Publication {publication} noImg={true} />
    {/each}
  </div>
</section> -->

<section class="section">
  <h2>Talks</h2>
  <div class="research-section">
    {#each PRESENTATIONS as publication}
      <Publication {publication} noImg={true} />
    {/each}
  </div>
</section>

<!-- <section class="section">
  <h2>Awards</h2>
</section> -->

<section class="section">
  <h2>Teaching</h2>
  <Teaching />
</section>

<style>
  .section {
    margin-top: 50px;
  }
</style>
