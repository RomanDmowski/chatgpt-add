<script lang="ts">
  import Fa from 'svelte-fa/src/fa.svelte'
  import {
    faGithub
  } from '@fortawesome/free-brands-svg-icons/index'

  let classes = ''
export { classes as class }
  export let pin: boolean = false
  export let strongMask: boolean = false
</script>

<div class="lower-mask section-footer-mask" class:pin-footer={pin}/>
<div class="lower-mask2" class:strong-mask={strongMask} />
<div class="section-footer {classes}" class:pin-footer={pin}>
  <slot />
  <div class="content has-text-right is-size-7">
    <p>
      <strong>ChatGPT-web</strong>
      <span class="author">by Niek van der Maas</span>
      <!-- <a target="_blank" class="ml-4" href="https://github.com/Niek/chatgpt-web"><span style="position:absolute" class="icon default-text"><Fa size="2x" icon="{faGithub}"/></span></a>
      <span style="display:inline-block;width:30px;height:20px;"></span> -->
    </p>
  </div>
</div>
