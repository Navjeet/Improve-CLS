# Improve-CLS

<style>
  body {
    opacity: 0.01;
    transition: opacity 0.1s ease-out;
  }
  body.active {
    opacity: 1;
  }
</style>

<script>
  function activateBody () {
    var bodyEl = document.querySelector('body')
    setTimeout(function(){
      bodyEl.classList.add('active')
    }, 3)
  }
  // RUNS ON DOM COMPLETE, NOT PAGE READY
  // PAGE READY IS WAY TOO SLOW
  if (document.readyState !== 'loading') {
    activateBody()
  } else {
    document.addEventListener('DOMContentLoaded', activateBody)
  }
</script>
