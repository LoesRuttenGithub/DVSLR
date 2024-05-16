<script>
    export let datapoint = {};
    $: howmany=datapoint
</script>

<g>
    <!-- <circle cx="0" cy="0" r="10" class={datapoint.species} /> -->
    <!-- <rect x={-3-0.5*1.8*howmany} y={-3-0.5*1.8*howmany} width={6+1.8*howmany} height={6+1.2*howmany} class={datapoint.species} stroke="black" stroke-width="1" />  -->
    <!-- <rect x={-3-0.5*1.8*howmany}+6 y={-3-0.5*1.8*howmany-5} width="8" height="4" stroke="black" stroke-width="2"  />    -->
    <!--<polygon points="1,0 4,0 3,3 4,3 1,7 0,4 1,4" class="polygon" troke="grey" stroke-width="2" />-->
    <!-- <polygon points="5,0 20,0 15,12 20,12 5,33 8,16 4,16" transform={`scale(${0.05*sw}, ${0.05*sl}) translate(${50-2*sw}, -13)`} class="transformed-polygon" /> -->
    <rect x={-0.5*1.8*howmany} y={12-1.2*howmany} width={1.8*howmany} height={1.2*howmany} class="batteryfullness" stroke="black" stroke-width="1" fill="black"/>  

    <!--
    <path style="transform: rotate(270deg)" d={sepal_path} />
    <path style="transform: rotate(30deg)" d={sepal_path} />
    <path style="transform: rotate(150deg)" d={sepal_path} />
   
    <path style="transform: rotate(325deg)" d={petal_path} />
    <path style="transform: rotate(90deg)" d={petal_path} />
    <path style="transform: rotate(210deg)" d={petal_path} />
     -->
</g>

<style>
    circle.setosa {
        fill: #7570b3;
        fill-opacity: 0.8;
    }
    circle.virginica {
        fill: #1b9e77;
        fill-opacity: 0.8;
    }
    circle.versicolor {
        fill: #d95f02;
        fill-opacity: 0.8;
    }

    rect.setosa {
        fill: #00ff00;
        fill-opacity: 0.3;
    }
    rect.virginica {
        fill: #fbff00;
        fill-opacity: 0.3;
    }
    rect.versicolor {
        fill: #ffa600;
        fill-opacity: 0.3;
    }

    rect.batteryfullness {
    fill: black; /* Solid black fill */
    stroke: black;
    stroke-width: 1;
  }       
</style>