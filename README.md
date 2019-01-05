# csvtables
converts csv into html tables

## Function
```
function csvtables($data){
$f = fopen($data, "r");
fgetcsv($f);
while (($line = fgetcsv($f)) !== false) {
        echo "<tr>";
        foreach ($line as $cell) {
                echo "<td style='padding-top:10px;'>" . htmlspecialchars($cell) . "</td>";
        }
        echo "</tr>\n";
}
fclose($f);  
}
```

## Call
```
csvtables('URL');
```
