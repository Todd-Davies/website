---
{"dg-publish":true,"dg-home":false,"dg-hide":true,"dg-path":"redirect.md","permalink":"/redirect/","hide":true,"dgPassFrontmatter":true}
---


<script>
(function () {
  var params = new URLSearchParams(window.location.search);
  var target = params.get('t'); // t for target
  console.log(target)
  switch (target) {
    case 'sb':
        target = 'https://www.hathiari.com';
        break;
    default:
      target = null; // Disallow all other URLs
  }
  console.log(target)
  if (target && /^https?:\/\//i.test(target)) {
	  console.log("Redirecting!")
      window.location.replace(target);
      return;
  } 
  document.addEventListener('DOMContentLoaded', function () {
    document.body.textContent = 'No valid "t" (target) parameter provided.';
  });
})();
</script>

Redirecting...