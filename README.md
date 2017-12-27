## Inspiration and code:
- [Mike Bostock's: Zoomable Sunburst](https://bl.ocks.org/mbostock/4348373)
- [Eduard Trott's: Zoomable Sunburst on d3.js v4](https://bl.ocks.org/maybelinot/5552606564ef37b5de7e47ed2b7dc099)

## D3 Stuff 
### Tooltip 
Stackoverflow solution: https://stackoverflow.com/questions/10805184/show-data-on-mouseover-of-circle

append div: 
```
var tooltip = d3.select("body")
    .append("div")
    .style("position", "absolute")
    .style("z-index", "10")
    .style("visibility", "hidden")
    .text("a simple tooltip");
```

toggle it where data is inserted:
```
.on("mouseover", function(){return tooltip.style("visibility", "visible");})
.on("mousemove", function(){return tooltip.style("top",
    (d3.event.pageY-10)+"px").style("left",(d3.event.pageX+10)+"px");})
.on("mouseout", function(){return tooltip.style("visibility", "hidden");});
```
