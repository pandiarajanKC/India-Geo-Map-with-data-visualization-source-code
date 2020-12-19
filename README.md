# India-Geo-Map-with-data-visualization-source-code

Demo : http://freesourcecoder.com/india-geo-map-with-data-visualization-source-code

Description :  
Displaying any parameter like Sales data or any number notation in the map is the easy way to represent the data accordance of Geographically . Displaying the data with table and normal text number is very traditional and boring presentation. In this project we are displaying number notation in statewise data.

Highcharts is an unadulterated JavaScript based outlining library intended to improve web applications by including intuitive diagramming capacity. Highcharts gives a wide assortment of outlines. For instance, line outlines, spline graphs, region diagrams, bar graphs, pie graphs, etc. This instructional exercise will show you the fundamentals of Highcharts. There are sections examining all the essential parts of Highcharts with appropriate models.

Html part follows like below:

<link href="https://cdn.metroui.org.ua/v4/css/metro.min.css">
<link href="https://cdn.metroui.org.ua/v4/css/metro-colors.min.css">
<linkhref="https://cdn.metroui.org.ua/v4/css/metro-rtl.min.css">
<link href="https://cdn.metroui.org.ua/v4/css/metro-icons.min.css">

// Prepare demo data
// Data is joined to map using value of 'hc-key' property by default.
// See API docs for 'joinBy' for more info on linking data and map.
var data = [
    ['madhya pradesh', 0],
    ['uttar pradesh', 1],
    ['karnataka', 2],
    ['nagaland', 3],
    ['bihar', 4],
    ['lakshadweep', 5],
    ['andaman and nicobar', 6],
    ['assam', 7],
    ['west bengal', 8],
    ['puducherry', 9],
    ['daman and diu', 10],
    ['gujarat', 11],
    ['rajasthan', 12],
    ['dadara and nagar havelli', 13],
    ['chhattisgarh', 14],
    ['tamil nadu', 15],
    ['chandigarh', 16],
    ['punjab', 17],
    ['haryana', 18],
    ['andhra pradesh', 19],
    ['maharashtra', 20],
    ['himachal pradesh', 21],
    ['meghalaya', 22],
    ['kerala', 23],
    ['telangana', 24],
    ['mizoram', 25],
    ['tripura', 26],
    ['manipur', 27],
    ['arunanchal pradesh', 28],
    ['jharkhand', 29],
    ['goa', 30],
    ['nct of delhi', 31],
    ['odisha', 32],
    ['jammu and kashmir', 33],
    ['sikkim', 34],
    ['uttarakhand', 35]
];

// Create the chart
Highcharts.mapChart('container', {
    chart: {
        map: 'countries/in/custom/in-all-disputed'
    },

    title: {
        text: 'Highmaps basic demo'
    },

    subtitle: {
        text: 'Source map: India with disputed territories'
    },

    mapNavigation: {
        enabled: true,
        buttonOptions: {
            verticalAlign: 'bottom'
        }
    },

    colorAxis: {
        min: 0
    },

    series: [{
        data: data,
        name: 'Random data',
        states: {
            hover: {
                color: '#BADA55'
            }
        },
        dataLabels: {
            enabled: true,
            format: '{point.name}'
        }
    }]
});
