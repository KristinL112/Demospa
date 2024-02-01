<script setup></script>
<!-- Mallen för en hero image -->
<template>
<div id="wrapper-hero">
    <img src="../assets/img/jared-rice-PibraWHb4h8-unsplash.jpg" alt="Spa-bad" class="img-fluid"/>

    <!-- En behållare med klassen "center" som innehåller centrerad text i -->
    <div class="centered">
        <h1>Tag hand om dig.</h1>
    </div>
</div>
</template>

<style>
#wrapper-hero img{
    margin: 0 auto;
    height: auto;
    overflow-x: hidden;
}
#wrapper-hero .centered{
    position: absolute;
    top:50%;
    left:50%;
    transform: translate(-50%, -50%);
    color: white;
}
</style>
