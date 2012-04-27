This projec is based on:
Tom Ellis' Linear and Radial Gradient cssHook for jQuery (https://github.com/brandonaaron/jquery-cssHooks)
and uses webtoolkit's base64 encoding for the encoding it's SVG background gradients (http://www.webtoolkit.info/)

- I am still working on implementing degree for SVG


-linear-gradient (with all it's prefixes)
  Most of this logic is from Tom Ellis, I just added the webkit legacy support for the old webkit-only gradient 
  syntax as a lot of mobile devices still use older webkit versions.

-Using Filter (IE6-IE8):
  Ms' Filter only support 2 colors, theirfore it will only pick up the first and last color in your gradient. 
  Furthermore it only supports only horizontal and vertical gradients.

-SVG (IE9 and some older Opera version) 
  SVG has some advantages over filter (more colors, support for rounded corners etc.) 
  however as IE does not have a method like window.btoa() to base64 encode a string I am 
  using webtoolkit's base64 encoding. 