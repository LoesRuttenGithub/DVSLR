<script>
    // A datapoint looks like this:
    // { petalLength: 1.4,
    //   petalWidth: 0.2,
    //   sepalLength: 5.1,
    //   sepalWidth: 3.5,
    //   species: "setosa" }

    export let datapoint = {};

    let scale = 3;
    $: sl = scale * datapoint.sepalLength;
    $: sw = scale * datapoint.sepalWidth;
    $: pl = scale * datapoint.petalLength;
    $: pw = scale * datapoint.petalWidth;
    $: sepal_path =
        "M 0,0 " + "C " + sl + ",-" + sw + " " + sl + "," + sw + " 0,0 Z";
    $: petal_path =
        "M 0,0 " + "C " + pl + ",-" + pw + " " + pl + "," + pw + " 0,0 Z";
</script>

<g>
    <!-- <circle cx="0" cy="0" r="10" class={datapoint.species} /> -->
    <rect x="-10" y="-15" width="20" height="30" class={datapoint.species} stroke="black" stroke-width="1" />  
    <rect x="-4" y="-20" width="8" height="4" stroke="black" stroke-width="2"  />    
    <!--<polygon points="1,0 4,0 3,3 4,3 1,7 0,4 1,4" class="polygon" troke="grey" stroke-width="2" />-->
    <polygon points="5,0 20,0 15,12 20,12 5,33 8,16 4,16" transform={`scale(${0.05*sw}, ${0.05*sl}) translate(${50-2*sw}, -13)`} class="transformed-polygon" />
    <rect x={-0.5*1.8*pw} y={12-1.2*pl} width={1.8*pw} height={1.2*pl} class="batteryfullness" stroke="black" stroke-width="1" fill="black"/>  

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