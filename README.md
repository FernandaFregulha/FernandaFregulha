### Hello visitor! 👋
## I'm Fernanda Fregulha!

 

:computer: I'm Full-Stack Developer!

:house_with_garden: I’m from Brazil.

:books: I’m currently learning everything.
<!DOCTYPE html>
<html>
<head>
  <title>Gráfico de Pizza</title>
  <style>
    .chart-container {
      width: 300px;
      height: 300px;
      position: relative;
    }

    .chart-text {
      font-family: Arial, sans-serif;
      font-size: 14px;
      text-anchor: middle;
      fill: #ffffff;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="chart-container">
    <svg id="chart"></svg>
    <div class="chart-text">Gráfico de Pizza</div>
  </div>

  <script src="https://d3js.org/d3.v4.min.js"></script>
  <script>
    // Dados do gráfico
    var data = [
      { label: "CSS", value: 10, color: "#ffa500" },
      { label: "HTML", value: 10, color: "#ffa500" },
      { label: "Python", value: 10, color: "#ffa500" },
      { label: "SQL", value: 5, color: "#ffd700" },
      { label: "Oracle", value: 5, color: "#ffd700" },
      { label: "PHP", value: 5, color: "#ffd700" },
      { label: "JavaScript", value: 30, color: "#ff0000" },
      { label: "Kotlin", value: 20, color: "#ff0000" },
      { label: "Java", value: 15, color: "#ff0000" }
    ];

    // Configurações do gráfico
    var width = 300;
    var height = 300;
    var radius = Math.min(width, height) / 2;
    var svg = d3.select("#chart")
      .attr("width", width)
      .attr("height", height);
    var g = svg.append("g")
      .attr("transform", "translate(" + width / 2 + "," + height / 2 + ")");

    // Função para calcular o ângulo
    var pie = d3.pie()
      .sort(null)
      .value(function(d) { return d.value; });

    // Gerar os arcos
    var path = d3.arc()
      .outerRadius(radius - 10)
      .innerRadius(0);

    // Gerar o gráfico de pizza
    var arc = g.selectAll(".arc")
      .data(pie(data))
      .enter().append("g")
        .attr("class", "arc");

    arc.append("path")
      .attr("d", path)
      .attr("fill", function(d) { return d.data.color; });

    arc.append("text")
      .attr("transform", function(d) { return "translate(" + path.centroid(d) + ")"; })
      .attr("dy", "0.35em")
      .text(function(d) { return d.data.label; })
      .attr("class", "chart-text");
  </script>
</body>
</html>



:outbox_tray: 2021 Goals: create a new project and find a new job.
CSS: ![CSS](https://img.shields.io/badge/-CSS-ffa500?style=for-the-badge&logo=css3&logoColor=black)
HTML: ![HTML](https://img.shields.io/badge/-HTML-ffa500?style=for-the-badge&logo=html5&logoColor=black)
Python: ![Python](https://img.shields.io/badge/-Python-ffa500?style=for-the-badge&logo=python&logoColor=black)
SQL: ![SQL](https://img.shields.io/badge/-SQL-ffd700?style=for-the-badge&logo=sql&logoColor=black)
Oracle: ![Oracle](https://img.shields.io/badge/-Oracle-ffd700?style=for-the-badge&logo=oracle&logoColor=black)
PHP: ![PHP](https://img.shields.io/badge/-PHP-ffd700?style=for-the-badge&logo=php&logoColor=black)
JavaScript: ![JavaScript](https://img.shields.io/badge/-JavaScript-ff0000?style=for-the-badge&logo=javascript&logoColor=black)
Kotlin: ![Kotlin](https://img.shields.io/badge/-Kotlin-ff0000?style=for-the-badge&logo=kotlin&logoColor=black)
Java: ![Java](https://img.shields.io/badge/-Java-ff0000?style=for-the-badge&logo=java&logoColor=black)
