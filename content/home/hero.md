+++
# Hero widget. #can add a big photo to the top with this file
widget = "hero"
active = true
date = 2017-10-15T00:00:00

title = ""

<meta name="google-site-verification" content="RBTAQIQMZWUutZsA0Ppuv8RJd4wMSnbK7XTprU0Uk2Q" />

# Order that this section will appear in.
weight = 3

# Overlay a color or image (optional).
#   Deactivate an option by commenting out the line, prefixing it with `#`.
[header]
  overlay_color = "#666"  # An HTML color value.
  overlay_img = "headers/marsh_hollands.jpg"  # Image path relative to your `static/img/` folder.
  overlay_filter = 0.01  # Darken the image. Value in range 0-1.

# Call to action button (optional).
#   Activate the button by specifying a URL and button label below.
#   Deactivate by commenting out parameters, prefixing lines with `#`.
#[cta]
#  url = "./post/getting-started/"
#  label = '<i class="fa fa-download"></i> Install Now'
+++

<br>

<br><br>
<iframe style="display: inline-block;" src="" scrolling="0" width="160px" height="30px" frameborder="0"></iframe>
<iframe style="display: inline-block;" src="" scrolling="0" width="158px" height="30px" frameborder="0"></iframe>

<script type="text/javascript">
  (function defer() {
    if (window.jQuery) {
      jQuery(document).ready(function(){
        GetLatestReleaseInfo();
      });
    } else {
      setTimeout(function() { defer() }, 50);
    }
  })();  
  function GetLatestReleaseInfo() {
    $.getJSON('https://api.github.com/repos/gcushen/hugo-academic/tags').done(function (json) {
      let release = json[0];
      // let downloadURL = release.zipball_url;
      $('#academic-release').text('Latest release ' + release.name);  
    });    
}  
</script>
