# Files


## base.html
<pre>
<code>&lt;!DOCTYPE html&gt;
&lt;html>
  &lt;head>
    &lt;script src="http://d3js.org/d3.v3.min.js" charset="utf-8">&lt;/script>
  &lt;/head>
  &lt;body>
  &lt;/body>
&lt;/html></code></pre>


## d3_divs.html
<pre>
<code>&lt;!DOCTYPE html>
&lt;html>
  &lt;head>
    &lt;script src="http://d3js.org/d3.v3.min.js" charset="utf-8">&lt;/script>
  &lt;/head>
  &lt;body>
    &lt;div id="d_one" class="d_small">Div 1&lt;/div>
    &lt;div id="d_two" class="d_large">Div 2&lt;/div>
    &lt;div id="d_tre" class="d_large">Div 3
      &lt;div id="d_for" class="d_medium">Div 4&lt;/div>
      &lt;div id="d_fiv" class="d_small">Div 5&lt;/div>
    &lt;/div>
  &lt;/body>
&lt;/html></code></pre>



# Exercises


## Slide 48: Exercise - Chrome
<pre>
<code>2+2;
</code></pre>


## Slide 52: Exercise - Javascript Function Super Powers
<pre>
<code>var globe = [];

function returnNum(x) { return x; }

function fillGlobe (func, n) {
    func.woo = "hoo";
    globe[0] = func;

    function insideFun(m, k) { 
      return function (j) { return m(k+j); }
    }

    return insideFun(globe[0], n);
}

// ***** ***** ***** ***** ***** //

returnNum(5);

var myResult = fillGlobe(returnNum, 2);

globe;

globe[0];

globe[0].woo;

myResult;

myResult(100);
</code></pre>

## Slide 54: Exercise - Javascript Array Method: Map
<pre>
<code>var startArray = [1,2,3,4,5];

var evenArray = startArray.map( function(x) { return x % 2 === 0; } );

var oddArray = startArray.map( function(x) { return x % 2 != 0; } );

var biggerThanTwoArray = startArray.map( function(x) { return x > 2; } );

startArray;
evenArray;
oddArray;
biggerThanTwoArray;
</code></pre>

## Slide 56: Exercise - Javascript Array Method: Filter
<pre>
<code>var startArray = [1,2,3,4,5];

var evenArray = startArray.filter( function(x) { return x % 2 === 0; } );

var oddArray = startArray.filter( function(x) { return x % 2 != 0; } );

var biggerThanTwoArray = startArray.filter( function(x) { return x > 2; } );

startArray;
evenArray;
oddArray;
biggerThanTwoArray;
</code></pre>

## Slide 59: Exercise - D3.js Setup
<pre>
<code>d3.version;
</code></pre>

## Slide 64: Exercise - D3.js Selections
<pre>
<code>d3.select("body");

d3.select("div");

d3.selectAll("div");

d3.select("#d_tre");

d3.select(".d_small");

d3.selectAll(".d_medium ");

d3.select("#d_tre").select("#d_for");

d3.select("#d_tre").select("#d_one");

d3.select("#d_tre").select("#d_fiv");

d3.select("#d_tre").selectAll("div");
</code></pre>

## Slide 66: Exercise - D3 Append Operator
<pre>
<code>d3.select("body").append("span");

d3.select("#d_for").append("div");

d3.selectAll("div").append("p");

d3.selectAll(".d_small").append("unicorn");

d3.selectAll("p").append("saturday");
</code></pre>

## Slide 71: Exercise - D3 Data Operator
<pre>
<code>d3.select("body").data(["Saturday"]);

d3.select("body").data([function() { return 2; }]);

d3.selectAll("div").data([{"x": 11}, {"x": 12}, {"x": 13}, {"x": 14}, {"x": 15}]);

d3.selectAll("div").data([[[1]], [[2]], [[3]], [[4]], [[5]]]);
</code></pre>

## Slide 75: Exercise - Data Join Scenario 1 (Special Case)
<pre>
<code>var virtualSelection = d3.select("body").selectAll("p").data([1]);

d3.selectAll("p");

virtualSelection;

virtualSelection.enter();

virtualSelection.exit();
</code></pre>

## Slide 77: Exercise - D3 Append On Enter Selection
<pre>
<code>d3.select("body").selectAll("span").data([4,5,6,7,8]).enter().append("span");

d3.selectAll("span");

// Reset page

d3.select("body").selectAll("unicorn").data([1,2,3]).enter().append("unicorn");

d3.selectAll("unicorn").data();
</code></pre>

## Slide 80: Exercise - Data Join Scenario 1
<pre>
<code>d3.select("body").append("p");

var virtualSelection = d3.select("body").selectAll("p").data([1, 2, 3]);

d3.selectAll("p");

virtualSelection;

virtualSelection.enter();

virtualSelection.exit();
</code></pre>

## Slide 82: Exercise - Data Join Scenario 2
<pre>
<code>d3.select("body").selectAll("p").data([0,0,0]).enter().append("p");

var virtualSelection = d3.select("body").selectAll("p").data([1, 2, 3]);

d3.selectAll("p");

virtualSelection;

virtualSelection.enter();

virtualSelection.exit();
</code></pre>

## Slide 84: Exercise - Data Join Scenario 3
<pre>
<code>d3.select("body").selectAll("p").data([0,0,0]).enter().append("p");

var virtualSelection = d3.select("body").selectAll("p").data([1]);

d3.selectAll("p");

virtualSelection;

virtualSelection.enter();

virtualSelection.exit();
</code></pre>

## Slide 88: Exercise - D3.js Attr
<pre>
<code>d3.select("div").attr("abc", "123");

// Reset page

d3.selectAll("div").attr("mos", "def");

d3.select("div").attr("mos");

// Reset page

d3.selectAll("div").attr("holiday", function() { return "inn"; });
</code></pre>

## Slide 90: Exercise - Using Data Bound To DOM Elements
<pre>
<code>d3.select("body").selectAll("span").data([4,5,6,7,8]).enter().append("span");

d3.selectAll("span").attr("d_element", function(d) { return d; });

// Reset page

d3.select("body").selectAll("unicorn").data([1,2,3]).enter().append("unicorn");

d3.selectAll("unicorn").attr("unicorn_i", function(d, i) { return i; });
</code></pre>

## Slide 92: Exercise - Text Operator
<pre>
<code>d3.select("body").selectAll("p").data([100, 200, 300]).enter().append("p");

d3.selectAll("p").text("popcorn");

d3.selectAll("p").text(function(d) { return d; });

d3.selectAll("p").text(function(d, i) { return i; });
</code></pre>

## Slide 94: Exercise - Style Attr Shortcut
<pre>
<code>d3.select("div").style("font-size", "24px");

// Reset page

d3.selectAll("div").style("font-size", function(d, i) { return (i+1)*25 + "px"; });
</code></pre>

## Slide 96: Exercise - D3.js Remove
<pre>
<code>d3.select("body").selectAll("span").data([4,5,6,7,8]).enter().append("span");

d3.select("body").selectAll("span").attr("span_d", function(d) { return d; });

d3.select("body").selectAll("span").remove();

// Reset page

d3.select("body").selectAll("unicorn").data([1,2,3]).enter().append("unicorn");

d3.select("body").selectAll("unicorn").attr("unicorn_d", function(d) { return d; });

d3.select("body").selectAll("unicorn").remove();
</code></pre>

## Slide 102: Exercise - SVG Basic Shapes
<pre>
<code>d3.select("body").append("svg").attr("height",200).attr("width",200);

d3.select("svg").append("circle").attr("cx", 35).attr("cy", 35).attr("r", 25);

// Reset page

d3.select("body").append("svg").attr("height",200).attr("width",200);

d3.select("svg").append("rect")
   .attr("x", 10).attr("y", 10).attr("height", 50).attr("width", 50);
</code></pre>

## Slide 106: Exercise - D3.js Linear Scales
<pre>
<code>scaleOne(0);

scaleOne(1000);

scaleOne(500);

scaleOne(2000);

scaleTwo(0);

scaleTwo(1000);

scaleTwo(500);

scaleTwo(2000);
</code></pre>

## Slide 107: Exercise - D3 Linear Scales To Place Things
<pre>
<code>var scaleOne = d3.scale.linear().domain([0, 1000]).range([0, 200]);

d3.select("body").append("svg").attr("width",200).attr("height",200);

d3.select("svg").append("circle")
    .attr("cx", scaleOne(500))
    .attr("cy", scaleOne(300))
    .attr("r" , scaleOne(50));
</code></pre>

## Slide 110: Exercise - D3 Ordinal Color Scales
<pre>
<code>var color = d3.scale.category10();

color("spring");
color("summer");
color("fall");
color("winter");

color.range();
color.domain();
</code></pre>

## Slide 113: Exercise - D3.js Axes
<pre>
<code>d3.select("body").append("svg").attr("height", 200).attr("width", 200);
 var axisScale = d3.scale.linear().domain([0, 10]).range([0, 200]);

var xAxis = d3.svg.axis().scale(axisScale);

var xAxisGroup = d3.select("svg").call(xAxis);
</code></pre>

## Slide 118: Exercise - D3.js Axes Text & Tick Labels
<pre>
<code>var inner = d3.select("body").append("svg")
    .attr("height", 200)
    .attr("width", 200)
  .append("g")
    .attr("transform", "translate(10, 20)");

var axisScale = d3.scale.linear().domain([0, 10]).range([0, 180]);

var xAxis = d3.svg.axis().scale(axisScale).orient("xxxxx");

var xAxisGroup = inner.call(xAxis);
</code></pre>

## Slide 120: Exercise - D3.js Axis Placement
<pre>
<code>var inner = d3.select("body").append("svg")
      .attr("height", 200).attr("width", 200)
      .append("g").attr("transform", "translate(10, 20)");

var axisScale = d3.scale.linear().domain([0, 100]).range([0, 170]);

var xAxis = d3.svg.axis().scale(axisScale).orient("bottom");

var xAxisGroup = inner.append("g")
       .attr("transform", "translate(0,140)")
       .call(xAxis);
</code></pre>

## Slide 134: Exercise - D3.js Simple Example
<pre>
<code>var dataset = [2, 1, 5, 4, 6];

var svg = d3.select("body").append("svg")
    .attr("width", 200)
    .attr("height", 200);

svg.selectAll("rect")
    .data(dataset)
  .enter().append("rect")
    .attr("x", function(d, i) { return i * 33; })
    .attr("y", 0)
    .attr("width", 30)
    .attr("height", function(d) { return d * 30; });
</code></pre>

## Slide 144: Exercise - D3.js & AJAX -> In The Wild
<pre>
<code>// Scatterplot link: http://bl.ocks.org/mbostock/raw/3887118/

var tempData;

d3.tsv("data.tsv", function(error, data) {
        tempData = data;
});

tempData;
</code></pre>

## Slide 157: Exercise - Add “click” Event To Paragraphs
<pre>
<code>var paras = d3.select("body").selectAll("p")
    .data([10, 11, 12, 13, 14])
  .enter().append("p")
    .text(function(d, i) { return d; });

paras.on("click", function() { alert("clicked"); });

paras.on("click", function(d, i) { alert(i); });

paras.on("click", function(d, i) { alert(i); d3.select(this).remove() });
</code></pre>

## Slide 158: Exercise - Two Event Listeners
<pre>
<code>var paras = d3.select("body").selectAll("p")
    .data([10, 11, 12, 13, 14])
  .enter().append("p")
    .text(function(d, i) { return d; });

function colorBlack() { d3.select(this).style("color", "black"); }

function colorRed() { d3.select(this).style("color", "red"); }

paras
    .on("mouseover", colorRed)
    .on("mouseout", colorBlack); 
</code></pre>

## Slide 159: Exercise - Remove Scatterplot Dots
<pre>
<code>// Scatterplot link: http://bl.ocks.org/mbostock/raw/3887118/

function mouseOver () { d3.select(this).remove(); }

d3.selectAll(".dot").on("mouseover", mouseOver);
</code></pre>

## Slide 164: Exercise - Give Scatterplot Tool Tips
<pre>
<code>var div = d3.select("body").append("div")
    .style("position", "absolute")
    .style("text-align", "center")
    .style("width", "240px")
    .style("height", "2.5em")
    .style("font", "1.5em sans-serif")
    .style("color", "yellow")
    .style("pointer-events", "none")
    .style("background", "black")
    .style("border-radius", "8px")
    .style("border", "solid 1px green")
    .style("opacity", 0);

function mouseover(d) {
    div.html("Sepal Width: " + d.sepalWidth + "&lt;br /&gt; Sepal Length: " + d.sepalLength)
        .style("left", (d3.event.pageX + 9) + "px")
        .style("top", (d3.event.pageY - 43) + "px")
        .style("opacity", 1);
}

function mouseout() {
    div.style("opacity", 1e-6);
}

d3.selectAll(".dot")
    .on("mouseover", mouseover)
    .on("mouseout",  mouseout);
</code></pre>

## Slide 169: Exercise - Event Listener - Attr Transition
<pre>
<code>var paras = d3.select("body").selectAll("p")
    .data([100, 101, 102, 103, 104])
  .enter().append("p")
    .text(function(d, i) { return d; })
    .style("font-size", "48px");

function colorBlack() {
     d3.select(this).transition().duration(5000).style("color", "black");
}

function colorRed() { d3.select(this).style("color", "red"); }

paras
    .on("mouseover", colorRed)
    .on("mouseout", colorBlack); 
</code></pre>

## Slide 178: Exercise - Circle - Radius Attr Transition
<pre>
<code>var circle = d3.select("body").append("svg").selectAll("circle")
    .data([1]).enter().append("circle")
    .attr("cx", "50").attr("cy", "50").attr("r", "25");

function rChange() { 
    d3.select(this)
        .transition()
            .ease("elastic")
            .delay(1000)
            .duration(2000)
            .attr("r", function () { return Math.floor(Math.random()*99+20); }) }

circle
    .on("click", rChange);
</code></pre>

## Slide 183: Exercise - Circle - Multi-Attr Transition Chain
<pre>
<code>var circle = d3.select("body").append("svg").attr("height", 300).selectAll("circle")
    .data([1]).enter().append("circle")
    .attr("cx", "50").attr("cy", "50").attr("r", "25");

function clickFun() { 
    d3.select(this)
        .transition().duration(2000).attr("cx", "200").style("fill", "red")
        .transition().duration(1000).attr("cy", "200").style("fill", "green")
        .transition().duration(2000).attr("cx", "50").style("fill", "blue")
        .transition().duration(3000).attr("cy", "50").style("fill", "black");
}

circle
    .on("click", clickFun);
</code></pre>

## Slide 188: Exercise - Circle - Data-Driven Transition
<pre>
<code>var circle = d3.select("body").append("svg").selectAll("circle")
    .data([1, 2]).enter().append("circle")
    .attr("cx", function(d, i) { return d * 50 + 25 * i; })
    .attr("cy", "50").attr("r", "25");

function clickFun() {
    d3.select(this)
        .transition()
            .duration(function(d,i) { return d * 2000; })
            .style("fill", "red")
        .transition().duration(1000).style("fill", "black")
}

circle.on("click", clickFun);
</code></pre>

## Slide 198: Exercise - Enter + Update Selection
<pre>
<code>var updateSelection = d3.select("body").selectAll("p").data([0,0,0]);

updateSelection;

var enterSelection = updateSelection.enter();

updateSelection;

enterSelection;

var enterUpdateSelection = enterSelection.append("p");

enterSelection;

updateSelection;

enterUpdateSelection;
</code></pre>

## Slide 200: Exercise - General Update Pattern (1 of 5)
<pre>
<code>var text = d3.select("body").selectAll("p")
    .data("winter".split(""))
  .enter().append("p")
    .attr("class", "enter_selection_winter")
    .text(function(d) { return d; });
</code></pre>

## Slide 201: Exercise - General Update Pattern (2 of 5)
<pre>
<code>var springText = d3.select("body").selectAll("p")
    .data("spring".split(""));

springText.attr("class", "update_selection_spring");

springText.enter().append("p")
    .attr("class", "enter_selection_spring");

springText.text(function(d) { return d; });

springText.exit()
    .attr("class", "exit_selection_spring");

springText.exit().remove();
</code></pre>

## Slide 202: Exercise - General Update Pattern (3 of 5)
<pre>
<code>var summerText = d3.select("body").selectAll("p")
    .data("summertime".split(""));

summerText.attr("class", "update_selection_summer");

summerText.enter().append("p")
    .attr("class", "enter_selection_summer");

summerText.text(function(d) { return d; });

summerText.exit()
    .attr("class", "exit_selection_summer");

summerText.exit().remove();
</code></pre>

## Slide 203: Exercise - General Update Pattern (4 of 5)
<pre>
<code>var fallText = d3.select("body").selectAll("p")
    .data("fall".split(""));

fallText.attr("class", "update_selection_fall");

fallText.enter().append("p")
    .attr("class", "enter_selection_fall");

fallText.text(function(d) { return d; });

fallText.exit()
    .attr("class", "exit_selection_fall");

fallText.exit().remove();
</code></pre>

## Slide 204: Exercise - General Update Pattern (5 of 5)
<pre>
<code>var winterText = d3.select("body").selectAll("p")
    .data("winter".split(""));

winterText.attr("class", "update_selection_winter");

winterText.enter().append("p")
    .attr("class", "enter_selection_winter");

winterText.text(function(d) { return d; });

winterText.exit()
    .attr("class", "exit_selection_winter");

winterText.exit().remove();
</code></pre>

## Slide 210: Exercise - Key Function Update Pattern (1 of 3)
<pre>
<code>var dataSet = [{"color": "red", "r": 5},
                            {"color": "blue", "r": 15},
                            {"color": "green", "r": 25}];

var svg = d3.select("body").append("svg");

var circles = svg.selectAll("circle")
    .data(dataSet)
  .enter().append("circle")
    .attr("cx", function(d, i) { return i * 50 + 25; })
    .attr("cy", 25)
    .attr("r", function(d, i) { return d.r; })
    .style("fill", function(d, i) { return d.color; });
</code></pre>

## Slide 211: Exercise - Key Function Update Pattern (2 of 3)
<pre>
<code>var dataSet = [{"color": "blue", "r": 35},
                            {"color": "green", "r": 25},
                            {"color": "red", "r": 5}];

// Update Circle Data Properties
svg.selectAll("circle")
    .data(dataSet);

// No enter or Exit, so just focus on Update selection

d3.selectAll("circle")
    .attr("cx", function(d, i) { return i * 50 + 25; })
    .attr("cy", 25)
    .attr("r", function(d, i) { return d.r; })
    .style("fill", function(d, i) { return d.color; });
</code></pre>

## Slide 212: Exercise - Key Function Update Pattern (3 of 3)
<pre>
<code>// Reload Slide 210, then run below
var dataSet = [{"color": "blue", "r": 35},
                            {"color": "green", "r": 25},
                            {"color": "red", "r": 5}];

// Update Circle Data Properties
svg.selectAll("circle")
    .data(dataSet, function(d, i) { return d.color; });

// No enter or Exit, so just focus on Update selection
d3.selectAll("circle")
    .attr("cx", function(d, i) { return i * 50 + 25; })
    .attr("cy", 25)
    .attr("r", function(d, i) { return d.r; })
    .style("fill", function(d, i) { return d.color; });
</code></pre>

## Slide 219: Exercise - Dynamic General Update (1 of 3)
<pre>
<code>function update(data) {

  // Data Join
  var text = d3.select("body").selectAll("p")
      .data(data);

  // Update
  text.attr("class", "update");
  
  // Enter
  text.enter().append("p")
      .attr("class", "enter");

  // Enter + Update
  text.text(function(d) { return d; });

  // Exit
  text.exit().attr("class", "exit").remove()
}
</code></pre>

## Slide 220: Exercise - Dynamic General Update (2 of 3)
<pre>
<code>var data =  "winter".split("");
update(data);

var data =  "spring".split("");
update(data);

var data =  "summertime".split("");
update(data);

var data =  "fall".split("");
update(data);

var data =  "winter".split("");
update(data);
</code></pre>

## Slide 221: Exercise - Dynamic General Update (3 of 3)
<pre>
<code>// Generate Data Set
var data = ["spring", "summertime", "fall", "winter"].map(function(d) { return d.split("")});

// General Update Pattern Function
function update(data) {

  var text = d3.select("body").selectAll("p")
      .data(data);

  text.attr("class", "update");
  
  text.enter().append("p").attr("class", "enter");

  text.text(function(d) { return d; });

  text.exit().attr("class", "exit").remove()
}

// Initial Display of Spring
update(data[0]);

// Grab a random season and update display
setInterval(function() {
  update(data[Math.floor(Math.random() * 4)]);
}, 1500);
</code></pre>

## Slide 230: Exercise - JS Function Object Properties
<pre>
<code>function plusOne (d) { return d + 1; }

plusOne(10);

plusOne.ten = 10;

plusOne.ten;

plusOne.twenty = function() { return 20; };

plusOne.twenty();
</code></pre>

## Slide 246: Exercise - Bar Chart With Multiple Data Sets
barchart.html
<pre>
<code>&lt;!DOCTYPE html>
&lt;meta charset="utf-8">
&lt;html>
  &lt;head>
    &lt;script src="http://d3js.org/d3.v3.min.js" charset="utf-8">&lt;/script>
    &lt;script>
    function barChart() {

    // Internal Variables for Closure
    var svgHeight,
        svgWidth;

    // Creation of the Chart
    function chart(selection) {

      // Given a selection, go through each element and create a chart for it.
      selection.each(function(d, i) {

        // Bar X Spacing
        var barXSpacing = svgWidth / d.length;

        // Define Unit Bar Height
        var barUnitHeight = Math.floor(svgHeight / d3.max(d));

        // SVG Creation
        var barChartSVG = d3.select(this).append("svg")
            .attr( "width", svgWidth)
            .attr("height", svgHeight);

        // Bar Chart Bar Creation
        barChartSVG.selectAll("rect")
            .data(d)
          .enter().append("rect")
            .attr("x", function (d, i) { return i * barXSpacing; })
            .attr("y", 0)
            .attr("width", function(d, i) { return barXSpacing -2; })
            .attr("height", function(d) { return d * barUnitHeight; })

        }); // end of selection.each(...);
      } // end of function chart(...);

      // SVG Width Getter / Setter
      chart.svgWidth = function(value) {
        if (!arguments.length) return svgWidth;
        svgWidth = value;
        return chart;
      };

      // SVG Height Getter / Setter
      chart.svgHeight = function(value) {
        if (!arguments.length) return svgHeight;
        svgHeight = value;
        return chart;
      };

      // Return Chart function for method chaining
      return chart;
    }
    &lt;/script>
  &lt;/head>
  &lt;body>&lt;/body>
&lt;/html></code>
</pre>
Code:
<pre>
<code>var dataset = [[1, 10, 2, 3], [5, 8, 13, 8], [5, 3, 20, 1, 10], [1, 1, 2, 3, 5, 8, 13, 21]];

var myBarChart = barChart();

myBarChart.svgWidth(200).svgHeight(200);

d3.select("body").selectAll("div").data(dataset).enter().append("div");

d3.selectAll("div");

d3.selectAll("div").call(myBarChart);
</code></pre>

## Slide 273: Exercise - Many Points Path Generator
<pre>
<code>var lineFunction = d3.svg.line()
       .x(function(d) { return d.x; })
       .y(function(d) { return d.y; })
       .interpolate("linear");

var lineData = [{x:10, y: 10}, {x:50, y: 210}, { x:80, y:20}];

d3.select("body").append("svg").append("path")
    .attr("d", lineFunction(lineData))
    .attr("stroke-width", 5)
    .attr("stroke", "blue").attr("fill","none");
</code></pre>

## Slide 277: Exercise - SVG Arc Generator - Multi Arc
<pre>
<code>var data = [{start: 0, size: 3.14159}, {start: 3.92694, size: 1.57079}];

var arc = d3.svg.arc()
    .innerRadius(80)
    .outerRadius(100)
    .startAngle(function(d, i) { return d.start; })
    .endAngle(function(d, i) { return d.start + d.size; });

var chart = d3.select("body").append("svg")
    .attr("class", "chart")
  .append("g")
    .attr("transform", "translate(150,100)");

chart.selectAll("path")
    .data(data)
  .enter().append("path")
    .attr("d", arc);
</code></pre>

## Slide 279: Exercise - SVG Arc Generator - Radii
<pre>
<code>var data = [ {start: 0, size: 2,      inner: 50, outer: 100, color: "green"},
             {start: 2, size: 2,      inner: 25, outer: 150, color: "blue"},
             {start: 4, size: 2.28, inner: 75, outer: 125, color: "red"}];

var arc = d3.svg.arc()
    .innerRadius(function(d, i) { return d.inner; })
    .outerRadius(function(d, i) { return d.outer; })
    .startAngle(function(d, i) { return d.start; })
    .endAngle(function(d, i) { return d.start + d.size; });

var chart = d3.select("body").append("svg")
    .attr("class", "chart")
  .append("g")
    .attr("transform", "translate(150,200)");

chart.selectAll("path")
    .data(data)
  .enter().append("path")
    .style("fill", function(d, i) { return d.color; })
    .attr("d", arc);
</code></pre>

## Slide 284: Exercise - Pie Layout Arc Generator
<pre>
<code>var data = [
    {amount: 0.75},
    {amount: 2.5},
    {amount: 3.75}
];

var pie = d3.layout.pie()
      .sort(null)
      .value(function(d) { return d.amount; });

console.table(pie(data));
</code></pre>

## Slide 286: Exercise - Pie Layout Pie Chart Generation
<pre>
<code>var data = [ {amount: 10, color: "red"}, {amount: 20, color: "green"}, {amount: 5, color: "blue"}];

var arc = d3.svg.arc()
      .innerRadius(0)
      .outerRadius(100);

var pie = d3.layout.pie()
      .sort(null)
      .value(function(d) { return d.amount; });

var chart = d3.select("body").append("svg").append("g")
      .attr("transform", "translate(100,100)");

var arcGs = chart.selectAll(".arc")
      .data(pie(data))
   .enter().append("g");

arcGs.append("path")
      .attr("d", arc)
      .style("fill", function(d, i) { return d.data.color; });
</code></pre>

## Slide 292: Exercise - Basic Drag
<pre>
<code>var svg = d3.select("body").append("svg");

function dragmove(d) {
      d3.select(this)
            .attr("cx", d.x = d3.event.x)
            .attr("cy", d.y = d3.event.y);
}

var drag = d3.behavior.drag()
      .origin(Object)
      .on("drag", dragmove);

svg.selectAll("circle")
      .data([{x: 25, y: 25}])
   .enter().append("circle")
      .attr("r", 25)
      .attr("cx", function(d, i) { return d.x; })
      .attr("cy", function(d, i) { return d.y; })
      .call(drag);
</code></pre>

## Slide 293: Exercise - Drag The Circle
drag.html
<pre>
<code>&lt;!DOCTYPE html>
&lt;meta charset="utf-8">
&lt;html>
  &lt;head>
    &lt;script src="http://d3js.org/d3.v3.min.js" charset="utf-8">&lt;/script>
  &lt;/head>
  &lt;body>
  &lt;script>

  var width = 200,
      height = 200,
      radius = 25;

  var drag = d3.behavior.drag()
      .origin(Object)
      .on("drag", dragmove);

  var svg = d3.select("body").append("svg")
      .attr("width", width)
      .attr("height", height)
      .style("border", "solid 1px #aaa");

  svg.selectAll("circle")
      .data([{x: 100, y: 100}])
    .enter().append("circle")
      .attr("r", radius)
      .attr("cx", function(d, i) { return d.x; })
      .attr("cy", function(d, i) { return d.y; })
      .call(drag);

  function dragmove(d) {
    d3.select(this)
        .attr("cx", d.x = d3.event.x )
        .attr("cy", d.y = d3.event.y );
  }

  &lt;/script>
  &lt;/body>
&lt;/html></code>
</pre>
Code:
<pre>
<code>// Read & Understand it</code>
</pre>

## Slide 294: Exercise - Drag The Circle With Boundaries
drag_with_boundaries.html
<pre>
<code>&lt;!DOCTYPE html>
&lt;meta charset="utf-8">
&lt;html>
  &lt;head>
    &lt;script src="http://d3js.org/d3.v3.min.js" charset="utf-8">&lt;/script>
  &lt;/head>
  &lt;body>
  &lt;script>

  var width = 200,
      height = 200,
      radius = 25;

  var drag = d3.behavior.drag()
      .origin(Object)
      .on("drag", dragmove);

  var svg = d3.select("body").selectAll("svg")
      .data([{x: 100, y: 100}])
    .enter().append("svg")
      .attr("width", width)
      .attr("height", height)
      .style("border", "solid 1px #aaa");

  svg.append("circle")
      .attr("r", radius)
      .attr("cx", 100)
      .attr("cy", 100)
      .call(drag);

  function dragmove(d) {
    d3.select(this)
        .attr("cx", d.x = Math.max(radius, Math.min(width - radius, d3.event.x)))
        .attr("cy", d.y = Math.max(radius, Math.min(height - radius, d3.event.y)));
  }

  &lt;/script>
  &lt;/body>
&lt;/html></code>
</pre>
Code:
<pre>
<code>// Read & Understand it</code>
</pre>

## Slide 295: Exercise - Drag The Circle With 3 Drag Events
drag_with_three_events.html
<pre>
<code>&lt;!DOCTYPE html>
&lt;meta charset="utf-8">
&lt;html>
  &lt;head>
    &lt;script src="http://d3js.org/d3.v3.min.js" charset="utf-8">&lt;/script>
  &lt;/head>
  &lt;body>
  &lt;script>

  var width = 200,
      height = 200,
      radius = 25;

  var drag = d3.behavior.drag()
      .origin(Object)
      .on("dragstart", dragstart)
      .on("dragend",   dragend  )
      .on("drag",      dragmove );

  var svg = d3.select("body").selectAll("svg")
      .data([{x: 100, y: 100}])
    .enter().append("svg")
      .attr("width", width)
      .attr("height", height)
      .style("border", "solid 1px #aaa");

  svg.append("circle")
      .attr("r", radius)
      .attr("cx", 100)
      .attr("cy", 100)
      .call(drag);

  function dragstart(d) { d3.select(this).style("fill", "red"  ); }
  function dragend(d)   { d3.select(this).style("fill", "black"); }

  function dragmove(d) {
    d3.select(this)
        .attr("cx", d.x = Math.max(radius, Math.min(width - radius, d3.event.x)))
        .attr("cy", d.y = Math.max(radius, Math.min(height - radius, d3.event.y)));
  }

  &lt;/script>
  &lt;/body>
&lt;/html></code>
</pre>
Code:
<pre>
<code>// Read & Understand it</code>
</pre>

## Slide 303: Exercise - Circle Zoom
zoom.html
<pre>
<code>&lt;!DOCTYPE html>
&lt;meta charset="utf-8">
&lt;html>
  &lt;head>
    &lt;script src="http://d3js.org/d3.v3.min.js" charset="utf-8">&lt;/script>
  &lt;/head>
  &lt;body>
    &lt;script>
      // Variables
      var svgWidth  = 400,
          svgHeight = 400,    
          originalCircle = {"cx": 100, "cy": 100, "radius": 20},
          margin = {"top": 25, "right": 25, "bottom": 50, "left": 50},
          width  = svgWidth - margin.left - margin.right,       
          height = svgHeight - margin.top  - margin.bottom;

      // SVG Viewport
      var svgViewport = d3.select("body").append("svg")
          .attr("width", width + margin.left + margin.right)
          .attr("height", height + margin.top + margin.bottom)
          .style("border", "2px solid");

      // Scales
      var xAxisScale = d3.scale.linear()
          .domain([0, width])
          .range([0, width]);

      var yAxisScale = d3.scale.linear()
          .domain([0, height])
          .range([height, 0]);

      // Axis Functions
      var xAxis = d3.svg.axis()
          .scale(xAxisScale)
          .orient("bottom")
          .ticks(5);

      var yAxis = d3.svg.axis()
          .scale(yAxisScale)
          .orient("left")
          .ticks(5);

      // Zoom Function Event Listener
      function zoomFunction() {
  
          // Select All Circles
          var circles = d3.select("svg").selectAll("circle");
    
          // Pan Vector
          var panVector = d3.event.translate;
          var panX = panVector[0];
          var panY = panVector[1];
  
          // Scaling Multiplier
          var scaleMultiplier = d3.event.scale;
    
          // Tell us in HTML what is going on
          d3.select("#pan_x_span").text(panX);
          d3.select("#pan_y_span").text(panY);
          d3.select("#v_scale_val").text(scaleMultiplier);
  
          // Redraw the Axis
          innerSpace.select(".x.axis").call(xAxis);
          innerSpace.select(".y.axis").call(yAxis);
    
          // Redraw the Circle
          circles
              .attr("cx", function(d, i) { return xAxisScale(d.cx); })
              .attr("cy", function(d, i) { return yAxisScale(d.cy); })
              .attr("r",  function(d, i) { return (d.radius * scaleMultiplier); });
    
      }

      // Zoom Behavior
      var zoom = d3.behavior.zoom()
          .x(xAxisScale)
          .y(yAxisScale)
          .scaleExtent([0.2, 10])
          .on("zoom", zoomFunction);

      // Inner Drawing Space
      var innerSpace = svgViewport.append("g")
          .attr("class", "inner_space")
          .attr("transform", "translate(" + margin.left + "," + margin.top + ")")
          .call(zoom);

      // Draw Axis
      innerSpace.append("g")
          .attr("class", "x axis")
          .attr("transform", "translate(0," + height + ")")
          .call(xAxis);

      innerSpace.append("g")
          .attr("class", "y axis")
          .call(yAxis);

      // Initial Drawing of Circle For Scale
      var circle = innerSpace.selectAll("circle")
          .data([originalCircle])
        .enter().append("circle")
          .attr("cx", function(d) { return xAxisScale(d.cx); })
          .attr("cy", function(d) { return yAxisScale(d.cy); })
          .attr("r",  function(d) { return d.radius; })
          .style("fill", "green");

      // HTML Printout To Tell Us What Is Going ON
      d3.select("body").append("div").attr("id", "pan_x_div").text("Pan X Translate: ");
      d3.select("body").append("div").attr("id", "pan_y_div").text("Pan Y Translate: ");
      d3.select("body").append("div").attr("id", "v_scale").text("D3 Zoom Scale: ");
      d3.select("#pan_x_div").append("span").attr("id", "pan_x_span");
      d3.select("#pan_y_div").append("span").attr("id", "pan_y_span");
      d3.select("#v_scale").append("span").attr("id", "v_scale_val");
    &lt;/script>
  &lt;/body>
&lt;/html></code>
</pre>
Code:
<pre>
<code>// Read & Understand it</code>
</pre>

## Slide 305: Exercise - Circle Zoom With Hidden Rectangle
zoom_secret.html
<pre>
<code>&lt;!DOCTYPE html>
&lt;meta charset="utf-8">
&lt;html>
  &lt;head>
    &lt;script src="http://d3js.org/d3.v3.min.js" charset="utf-8">&lt;/script>
  &lt;/head>
  &lt;body>
    &lt;script>
    // Variables
    var svgWidth  = 400,
        svgHeight = 400,    
        originalCircle = {"cx": 100, "cy": 100, "radius": 20},
        margin = {"top": 25, "right": 25, "bottom": 50, "left": 50},
        width  = svgWidth  - margin.left - margin.right,       
        height = svgHeight - margin.top  - margin.bottom;

    // SVG Viewport
    var svgViewport = d3.select("body").append("svg")
        .attr("width",  width  + margin.left + margin.right)
        .attr("height", height + margin.top  + margin.bottom)
        .style("border", "2px solid");

    // Scales
    var xAxisScale = d3.scale.linear()
        .domain([0, width])
        .range([0, width]);

    var yAxisScale = d3.scale.linear()
        .domain([0, height])
        .range([height, 0]);

    // Axis Functions
    var xAxis = d3.svg.axis()
        .scale(xAxisScale)
        .orient("bottom")
        .ticks(5);

    var yAxis = d3.svg.axis()
        .scale(yAxisScale)
        .orient("left")
        .ticks(5);

    // Zoom Function Event Listener
    function zoomFunction() {

        // Select All Circles
        var circles = d3.select("svg").selectAll("circle");
  
        // Pan Vector
        var panVector = d3.event.translate;
        var panX = panVector[0];
        var panY = panVector[1];

        // Scaling Multiplier
        var scaleMultiplier = d3.event.scale;
  
        // Tell us in HTML what is going on
        d3.select("#pan_x_span").text(panX);
        d3.select("#pan_y_span").text(panY);
        d3.select("#v_scale_val").text(scaleMultiplier);

        // Redraw the Axis
        innerSpace.select(".x.axis").call(xAxis);
        innerSpace.select(".y.axis").call(yAxis);
  
        // Redraw the Circle
        circles
            .attr("cx", function(d, i) { return xAxisScale(d.cx); })
            .attr("cy", function(d, i) { return yAxisScale(d.cy); })
            .attr("r",  function(d, i) { return (d.radius * scaleMultiplier); });
  
    }

    // Zoom Behavior
    var zoom = d3.behavior.zoom()
        .x(xAxisScale)
        .y(yAxisScale)
        .scaleExtent([0.2, 10])
        .on("zoom", zoomFunction);

    // Inner Drawing Space
    var innerSpace = svgViewport.append("g")
        .attr("class", "inner_space")
        .attr("transform", "translate(" + margin.left + "," + margin.top + ")")
        .call(zoom);

    // Hidden Rectangle to Fully Capture Zoom Events
    innerSpace.append("g").attr("class", "hidden rectangle")
        .append("rect")
        .attr("class", "background")
        .attr("x", function(d, i) { return xAxisScale(0); })
        .attr("y", function(d, i) { return yAxisScale(height); })
        .attr("width", function(d, i) { return xAxisScale(width); })
        .attr("height", function(d, i) { return yAxisScale(0); })
        .style("fill", "white");

    // Draw Axes
    innerSpace.append("g")
        .attr("class", "x axis")
        .attr("transform", "translate(0," + height + ")")
        .call(xAxis);

    innerSpace.append("g")
        .attr("class", "y axis")
        .call(yAxis);

    // Initial Drawing of Circle For Scale
    var circle = innerSpace.selectAll("circle")
        .data([originalCircle])
      .enter().append("circle")
        .attr("cx", function(d) { return xAxisScale(d.cx); })
        .attr("cy", function(d) { return yAxisScale(d.cy); })
        .attr("r",  function(d) { return d.radius; })
        .style("fill", "green");

    // HTML Printout To Tell Us What Is Going ON
    d3.select("body").append("div").attr("id", "pan_x_div").text("Pan X Translate: ");
    d3.select("body").append("div").attr("id", "pan_y_div").text("Pan Y Translate: ");
    d3.select("body").append("div").attr("id", "v_scale").text("D3 Zoom Scale: ");
    d3.select("#pan_x_div").append("span").attr("id", "pan_x_span");
    d3.select("#pan_y_div").append("span").attr("id", "pan_y_span");
    d3.select("#v_scale").append("span").attr("id", "v_scale_val");
    &lt;/script>
  &lt;/body>
&lt;/html></code>
</pre>

## Slide 321: Exercise - GeoJSONLint.com
<pre>
<code>// http://GeoJSONLint.com
</code></pre>

## Slide 337: Exercise - North America map projections
<pre>
<code>// https://www.dashingd3js.com/na-map-projections
</code></pre>


## Slide 344: Exercise - Mapping Objects On NA Projection
<pre>
<code>// https://www.dashingd3js.com/objects-on-na-map-projections
</code></pre>