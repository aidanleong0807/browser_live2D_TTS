<template>
  <div></div>
</template>



<script setup lang="ts">
import { LAppDelegate } from "../live2d/src/lappdelegate";
import { LAppGlManager } from "../live2d/src/lappglmanager";
import * as LAppDefine from "../live2d/src/lappdefine";


window.addEventListener(
    'load',
    (): void => {
        // Initialize WebGL and create the application instance
        if (!LAppDelegate.getInstance().initialize()) {
        return;
        }

        LAppDelegate.getInstance().run();
    },
    { passive: true }
);
   
   
window.addEventListener(
'beforeunload',
(): void => LAppDelegate.releaseInstance(),
{ passive: true }
);
   
   
// Resize Screen
window.addEventListener(
"resize",
() => {
    if (LAppDefine.CanvasSize === "auto") {
    LAppDelegate.getInstance().onResize();
    }
},
{ passive: true }
);
</script>


<style>
canvas {
 width: 100vw;
 height: 100vh;
 display: block;
}
</style>