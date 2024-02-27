<br>`from js import robot`<br>

`while robot.is_ok():`<br>
    `  delta = robot.front_right_sensor() - robot.front_left_sensor()`<br>
    `  onemli_nokta = 0`<br>
    `  hata = onemli_nokta - delta`<br>
    `  artma = 0.1`<br>
    `  komut = hata*artma`<br>
    `  robot.rotate(komut)`<br>
    `  robot.move(2.0)`<br>
    `  yavaslama = abs(komut)`<br>
    `  robot.move(10 - min(8.0,yavaslama))`<br>
