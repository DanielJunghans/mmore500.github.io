---
layout: widecontent
title: Welcome
permalink: /
---

<script type="text/javascript">

images_list= {{ site.data.welcome | jsonify}}

console.log(images_list)

  function getImageHTML() {
    var html_code = '<img src=\"';
    var randomIndex = Math.floor(Math.random() * images_list.length);
    html_code += images_list[randomIndex]["href"];
    html_code += '\"  style=\"max-width:90vw; max-height:60vh;\" alt=\"have you tried ~refreshing~?!\"/>';
    html_code += "<br /><p align=\"left\">"
    html_code += images_list[randomIndex]["title"];
    html_code += "<br />"
    html_code += images_list[randomIndex]["caption"];
    html_code += "</p>"

    return html_code;
  }
</script>

<div style="text-align:center">
  <div style="display: inline-block;">
  <script type="text/javascript">
    document.write(getImageHTML());
  </script>
  </div>
</div>
