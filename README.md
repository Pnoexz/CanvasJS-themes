CanvasJS-themes
===============

Adds the ability to use customized themes with CanvasJS. For documentation, refer to http://canvasjs.com



Adding your own theme
=====================

Include this before you call CanvasJS.Chart(). You can edit as you want.

	var isCanvasSupported = !!document.createElement("canvas").getContext; // You might want to remove this line if you are not planning on using it.
	
	var theme = {
		Chart: {
			colorSet: "colorSet1"
		},
		Title: {
			fontFamily: isCanvasSupported ? "Calibri, Optima, Candara, Verdana, Geneva, sans-serif" : "calibri",
			fontSize: 33,
			fontColor: "#3A3A3A",
			fontWeight: "bold",
			verticalAlign: "top",
			margin: 10
		},
		Axis: {
			titleFontSize: 26,
			titleFontColor: "#666666",
			titleFontFamily: isCanvasSupported ? "Calibri, Optima, Candara, Verdana, Geneva, sans-serif" : "calibri",

			labelFontFamily: isCanvasSupported ? "Calibri, Optima, Candara, Verdana, Geneva, sans-serif" : "calibri",
			labelFontSize: 18,
			labelFontColor: "grey",
			tickColor: "#BBBBBB",
			tickThickness: 2,
			gridThickness: 2,
			gridColor: "#BBBBBB",
			lineThickness: 2,
			lineColor: "#BBBBBB"
		},
		Legend: {
			verticalAlign: "bottom",
			horizontalAlign: "center",
			fontFamily: isCanvasSupported ? "monospace, sans-serif,arial black" : "calibri"
		},
		DataSeries: {
			//bevelEnabled: true,
			indexLabelFontColor: "grey",
			//indexLabelFontFamily: "Trebuchet MS, monospace, Courier New, Courier",
			indexLabelFontFamily: isCanvasSupported ? "Calibri, Optima, Candara, Verdana, Geneva, sans-serif" : "calibri",
			//indexLabelFontWeight: "bold",
			indexLabelFontSize: 18,
			//indexLabelLineColor: "lightgrey",
			indexLabelLineThickness: 1
		}
	}
	CanvasJS.addTheme('Pnoexz',theme); // You can use any name

You then use them as any other theme

	var chart = new CanvasJS.Chart("someElement", {
		title: { text: "Company Stars" },
		theme: 'Pnoexz',
		...
		
TODO
====

 - Add minimized version.
 - Maybe throw in a few themes.
