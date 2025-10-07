## compost-img-tool

This is the content-aware image editing tool developed by Mariana Marangoni for the ‘More-Than-Human Design Through Critical Climate Computing’ project that significantly reduces the image’s file sizes while giving them a unique visual signature that stands out from other widely available tools for pixelating and dithering images available online.  

This image editing tool functions by 'recomposting' the uploaded image onto a <canvas>, giving access to its pixel data as an array of RGBA values. Instead of preserving all pixel colors, each pixel in the cell is replaced with the average, massively reducing visual detail and pixel variance.  A limited number of representative colors is extracted using a simple K-means clustering algorithm.

Each pixel’s average is mapped to the closest color in this reduced palette (Large flat areas = fewer bytes needed). That way, the image’s most detailed areas are preserved and elements such as a background sky or wall are heavily compressed. Approaches such as these can be explored to reduce filesize wherever possible in images hosted on low-carbon websites. 
