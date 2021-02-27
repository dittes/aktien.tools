## Handelszeiten
Die Handelszeiten der verschiedenen Börsen unterscheiden sich stark voneinander. Das liegt vor allem an den verschiedenen Zeitzonen. Wir haben die Öffnungszeiten der Börsen hier für euch zusammengestellt.

<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>

<script type="text/javascript">
google.charts.load("current", {packages:["timeline"]});
google.charts.setOnLoadCallback(drawChart);
function drawChart() {

  var container = document.getElementById('handelszeiten');
  var chart = new google.visualization.Timeline(container);
  var dataTable = new google.visualization.DataTable();

  var today = new Date();
  today.setHours(0,0,0,0);

  dataTable.addColumn({ type: 'string', id: 'Börse' });
  dataTable.addColumn({ type: 'string', id: 'Name' });
  dataTable.addColumn({ type: 'date', id: 'Start' });
  dataTable.addColumn({ type: 'date', id: 'End' });

  dataTable.addRows([
    [ 'Australian Securities Exchange', 'ASX', new Date(0,0,0,1,0,0), new Date(0,0,0,7,0,0) ],
    [ 'Shanghai Stock Exchange', 'SSE', new Date(0,0,0,2,30,0), new Date(0,0,0,8,0,0) ],
    [ 'Hong Kong Stock Exchange', 'HKEX', new Date(0,0,0,2,30,0), new Date(0,0,0,5,0,0) ],
    [ 'Hong Kong Stock Exchange', 'HKEX', new Date(0,0,0,6,0,0), new Date(0,0,0,9,0,0) ],
    [ 'Lang & Schwarz', 'LUS', new Date(0,0,0,7,30,0),  new Date(0,0,0,23,0,0) ],
    [ 'Tradegate', 'TRADEGATE', new Date(0,0,0,8,0,0),  new Date(0,0,0,22,0,0) ],
    [ 'Xetra', 'IBIS', new Date(0,0,0,9,0,0),  new Date(0,0,0,17,30,0) ],
    [ 'London Stock Exchange', 'LSE', new Date(0,0,0,9,0,0), new Date(0,0,0,17,30,0) ],
    [ 'New York Stock Exchange', 'NYSE', new Date(0,0,0,15,30,0), new Date(0,0,0,22,0,0) ],
    [ 'Nasdaq', 'NASDAQ', new Date(0,0,0,15,30,0), new Date(0,0,0,22,0,0) ]]);

  var options = {
    timeline: { singleColor: '#288c6c' },
    hAxis: { format: 'HH:mm' },
    backgroundColor: '#fff' 
  };

  chart.draw(dataTable, options);
}

</script>

<div id="handelszeiten" style="height:420px;"></div>

<script type="text/javascript">
google.charts.load("current", {packages:["timeline"]});
google.charts.setOnLoadCallback(drawChart);
function drawChart() {

  var container = document.getElementById('wochenendhandel');
  var chart = new google.visualization.Timeline(container);
  var dataTable = new google.visualization.DataTable();
  dataTable.addColumn({ type: 'string', id: 'Börse' });
  dataTable.addColumn({ type: 'string', id: 'Name' });
  dataTable.addColumn({ type: 'date', id: 'Start' });
  dataTable.addColumn({ type: 'date', id: 'End' });
  dataTable.addRows([
    [ 'Lang & Schwarz Samstag', 'LUS', new Date(0,0,0,10,0,0),  new Date(0,0,0,13,0,0) ],
    [ 'Lang & Schwarz Sonntag', 'LUS', new Date(0,0,0,17,0,0),  new Date(0,0,0,19,0,0) ]]);

  var options = {
    timeline: { singleColor: '#288c6c' },
    hAxis: { format: 'HH:mm' },
    backgroundColor: '#fff'
  };

  chart.draw(dataTable, options);

}

</script>

<div id="wochenendhandel" style="height:120px;"></div>
