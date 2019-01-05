# csvtables
converts csv into html tables using php

## Function
```
function csvtables($data){
$f = fopen($data, "r");
fgetcsv($f);
while (($line = fgetcsv($f)) !== false) {
        echo "<tr>";
        foreach ($line as $cell) {
                echo "<td>" . htmlspecialchars($cell) . "</td>";
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
