# PEMBAGIAN TUGAS PROYEK

<div id="table"></div>
<script>
fetch(https://docs.google.com/spreadsheets/d/e/2PACX-1vS1THMl94BR2cyKvsVy9h8OElZlUHkD6u1qjh1E3roP6H0zYYT4dd9oTPY7lamcw39y4xDt0AiejlDk/pub?gid=89798501&single=true&output=csv)
  .then(res=>res.text())
  .then(csv=>{
    const rows = csv.split('\n').map(r=>r.split(','));
    const t = ['<table>'];
    rows.forEach(r=>{
      t.push('<tr>'+r.map(c=>'<td>'+c+'</td>').join('')+'</tr>');
    });
    t.push('</table>');
    document.getElementById('table').innerHTML = t.join('');
  });
</script>
(https://docs.google.com/spreadsheets/d/e/2PACX-1vS1THMl94BR2cyKvsVy9h8OElZlUHkD6u1qjh1E3roP6H0zYYT4dd9oTPY7lamcw39y4xDt0AiejlDk/pub?gid=89798501&single=true&output=csv)
