# filtro bd

sofia marcle medina diaz

sara lucia lozano rueda

1. Obtener los nombres de todos los actores y las películas en las
   que han actuado.

   ```sql
   SELECT act.nombre, pel.titulo FROM actor AS act
   INNER JOIN pelicula_actor AS pa ON pa.id_actor = act.id_actor
   INNER JOIN pelicula AS pel ON pel.id_pelicula = pa.id_pelicula
   LIMIT 100;
   /*
   +----------+-----------------------+
   | nombre   | titulo                |
   +----------+-----------------------+
   | PENELOPE | ACADEMY DINOSAUR      |
   | PENELOPE | ANACONDA CONFESSIONS  |
   | PENELOPE | ANGELS LIFE           |
   | PENELOPE | BULWORTH COMMANDMENTS |
   | PENELOPE | CHEAPER CLYDE         |
   | PENELOPE | COLOR PHILADELPHIA    |
   | PENELOPE | ELEPHANT TROJAN       |
   | PENELOPE | GLEAMING JAWBREAKER   |
   | PENELOPE | HUMAN GRAFFITI        |
   | PENELOPE | KING EVOLUTION        |
   | PENELOPE | LADY STAGE            |
   | PENELOPE | LANGUAGE COWBOY       |
   | PENELOPE | MULHOLLAND BEAST      |
   | PENELOPE | OKLAHOMA JUMANJI      |
   | PENELOPE | RULES HUMAN           |
   | PENELOPE | SPLASH GUMP           |
   | PENELOPE | VERTIGO NORTHWEST     |
   | PENELOPE | WESTWARD SEABISCUIT   |
   | PENELOPE | WIZARD COLDBLOODED    |
   | NICK     | ADAPTATION HOLES      |
   | NICK     | APACHE DIVINE         |
   | NICK     | BABY HALL             |
   | NICK     | BULL SHAWSHANK        |
   | NICK     | CHAINSAW UPTOWN       |
   | NICK     | CHISUM BEHAVIOR       |
   | NICK     | DESTINY SATURDAY      |
   | NICK     | DRACULA CRYSTAL       |
   | NICK     | FIGHT JAWBREAKER      |
   | NICK     | FLASH WARS            |
   | NICK     | GILBERT PELICAN       |
   | NICK     | GOODFELLAS SALUTE     |
   | NICK     | HAPPINESS UNITED      |
   | NICK     | INDIAN LOVE           |
   | NICK     | JEKYLL FROGMEN        |
   | NICK     | JERSEY SASSY          |
   | NICK     | LIAISONS SWEET        |
   | NICK     | LUCKY FLYING          |
   | NICK     | MAGUIRE APACHE        |
   | NICK     | MALLRATS UNITED       |
   | NICK     | MASK PEACH            |
   | NICK     | ROOF CHAMPION         |
   | NICK     | RUSHMORE MERMAID      |
   | NICK     | SMILE EARRING         |
   | NICK     | WARDROBE PHANTOM      |
   | ED       | ALONE TRIP            |
   | ED       | ARMY FLINTSTONES      |
   | ED       | ARTIST COLDBLOODED    |
   | ED       | BOONDOCK BALLROOM     |
   | ED       | CADDYSHACK JEDI       |
   | ED       | COWBOY DOOM           |
   | ED       | EVE RESURRECTION      |
   | ED       | FORREST SONS          |
   | ED       | FRENCH HOLIDAY        |
   | ED       | FROST HEAD            |
   | ED       | HALLOWEEN NUTS        |
   | ED       | HUNTER ALTER          |
   | ED       | IMAGE PRINCESS        |
   | ED       | JEEPERS WEDDING       |
   | ED       | LUCK OPUS             |
   | ED       | NECKLACE OUTBREAK     |
   | ED       | PLATOON INSTINCT      |
   | ED       | SPICE SORORITY        |
   | ED       | WEDDING APOLLO        |
   | ED       | WEEKEND PERSONAL      |
   | ED       | WHALE BIKINI          |
   | ED       | YOUNG LANGUAGE        |
   | JENNIFER | ANACONDA CONFESSIONS  |
   | JENNIFER | ANGELS LIFE           |
   | JENNIFER | BAREFOOT MANCHURIAN   |
   | JENNIFER | BED HIGHBALL          |
   | JENNIFER | BLADE POLISH          |
   | JENNIFER | BOONDOCK BALLROOM     |
   | JENNIFER | GHOSTBUSTERS ELF      |
   | JENNIFER | GREEDY ROOTS          |
   | JENNIFER | HANOVER GALAXY        |
   | JENNIFER | INSTINCT AIRPORT      |
   | JENNIFER | JUMANJI BLADE         |
   | JENNIFER | NATIONAL STORY        |
   | JENNIFER | OKLAHOMA JUMANJI      |
   | JENNIFER | POSEIDON FOREVER      |
   | JENNIFER | RAIDERS ANTITRUST     |
   | JENNIFER | RANDOM GO             |
   | JENNIFER | REDS POCUS            |
   | JENNIFER | SILVERADO GOLDFINGER  |
   | JENNIFER | SPLASH GUMP           |
   | JENNIFER | SUBMARINE BED         |
   | JENNIFER | TREASURE COMMAND      |
   | JENNIFER | UNFORGIVEN ZOOLANDER  |
   | JOHNNY   | AMADEUS HOLY          |
   | JOHNNY   | BANGER PINOCCHIO      |
   | JOHNNY   | BONNIE HOLOCAUST      |
   | JOHNNY   | CHITTY LOCK           |
   | JOHNNY   | COMMANDMENTS EXPRESS  |
   | JOHNNY   | CONEHEADS SMOOCHY     |
   | JOHNNY   | DADDY PITTSBURGH      |
   | JOHNNY   | DAISY MENAGERIE       |
   | JOHNNY   | ENOUGH RAGING         |
   | JOHNNY   | ESCAPE METROPOLIS     |
   | JOHNNY   | FIRE WOLVES           |
   | JOHNNY   | FRONTIER CABIN        |
   +----------+-----------------------+
   */
   ```

   

2. Listar todos los clientes y los almacenes donde están
   registrados.

   ```SQL
   SELECT a.id_almacen, cl.nombre FROM cliente AS cl 
   INNER JOIN almacen AS a ON a.id_almacen = cl.id_almacen
   LIMIT 100;
   
   /*
   +------------+------------+
   | id_almacen | nombre     |
   +------------+------------+
   |          2 | BARBARA    |
   |          2 | JENNIFER   |
   |          2 | SUSAN      |
   |          2 | MARGARET   |
   |          2 | LISA       |
   |          2 | KAREN      |
   |          2 | BETTY      |
   |          2 | SANDRA     |
   |          2 | CAROL      |
   |          2 | SHARON     |
   |          2 | SARAH      |
   |          2 | KIMBERLY   |
   |          2 | JESSICA    |
   |          2 | SHIRLEY    |
   |          2 | ANGELA     |
   |          2 | BRENDA     |
   |          2 | ANNA       |
   |          2 | REBECCA    |
   |          2 | VIRGINIA   |
   |          2 | KATHLEEN   |
   |          2 | AMANDA     |
   |          2 | CAROLYN    |
   |          2 | CHRISTINE  |
   |          2 | CATHERINE  |
   |          2 | JOYCE      |
   |          2 | DORIS      |
   |          2 | EVELYN     |
   |          2 | KATHERINE  |
   |          2 | JUDITH     |
   |          2 | ROSE       |
   |          2 | JANICE     |
   |          2 | JUDY       |
   |          2 | CHRISTINA  |
   |          2 | THERESA    |
   |          2 | BEVERLY    |
   |          2 | TAMMY      |
   |          2 | IRENE      |
   |          2 | JANE       |
   |          2 | SARA       |
   |          2 | ANNE       |
   |          2 | JACQUELINE |
   |          2 | BONNIE     |
   |          2 | RUBY       |
   |          2 | LOIS       |
   |          2 | TINA       |
   |          2 | PAULA      |
   |          2 | ANNIE      |
   |          2 | EMILY      |
   |          2 | EDNA       |
   |          2 | TIFFANY    |
   |          2 | ROSA       |
   |          2 | CINDY      |
   |          2 | GRACE      |
   |          2 | SYLVIA     |
   |          2 | SHANNON    |
   |          2 | ELAINE     |
   |          2 | MONICA     |
   |          2 | ESTHER     |
   |          2 | JUANITA    |
   |          2 | ANITA      |
   |          2 | RHONDA     |
   |          2 | JOANNE     |
   |          2 | DANIELLE   |
   |          2 | MEGAN      |
   |          2 | SUZANNE    |
   |          2 | MICHELE    |
   |          2 | DARLENE    |
   |          2 | ERIN       |
   |          2 | LAUREN     |
   |          2 | JOANN      |
   |          2 | LORRAINE   |
   |          2 | SALLY      |
   |          2 | ERICA      |
   |          2 | DOLORES    |
   |          2 | YVONNE     |
   |          2 | SAMANTHA   |
   |          2 | MARION     |
   |          2 | STACY      |
   |          2 | ANA        |
   |          2 | IDA        |
   |          2 | HOLLY      |
   |          2 | BRITTANY   |
   |          2 | YOLANDA    |
   |          2 | KATIE      |
   |          2 | KRISTEN    |
   |          2 | SUE        |
   |          2 | ELSIE      |
   |          2 | BETH       |
   |          2 | JEANNE     |
   |          2 | CARLA      |
   |          2 | EILEEN     |
   |          2 | TONYA      |
   |          2 | ELLA       |
   |          2 | WILMA      |
   |          2 | JESSIE     |
   |          2 | AGNES      |
   |          2 | WILLIE     |
   |          2 | CHARLENE   |
   |          2 | DELORES    |
   |          2 | PEARL      |
   +------------+------------+
   
   */
   ```

   

3. Encontrar todas las películas y sus respectivas categorías.

   ```sql
   SELECT p.id_pelicula, p.titulo, c.nombre FROM categoria AS c 
   INNER JOIN pelicula_categoria AS pc ON pc.id_categoria = c.id_categoria
   INNER JOIN pelicula AS p ON p.id_pelicula = pc.id_pelicula
   LIMIT 100;
   
   /*
   +-------------+-------------------------+-----------+
   | id_pelicula | titulo                  | nombre    |
   +-------------+-------------------------+-----------+
   |          19 | AMADEUS HOLY            | Action    |
   |          21 | AMERICAN CIRCUS         | Action    |
   |          29 | ANTITRUST TOMATOES      | Action    |
   |          38 | ARK RIDGEMONT           | Action    |
   |          56 | BAREFOOT MANCHURIAN     | Action    |
   |          67 | BERETS AGENT            | Action    |
   |          97 | BRIDE INTRIGUE          | Action    |
   |         105 | BULL SHAWSHANK          | Action    |
   |         111 | CADDYSHACK JEDI         | Action    |
   |         115 | CAMPUS REMEMBER         | Action    |
   |         126 | CASUALTIES ENCINO       | Action    |
   |         130 | CELEBRITY HORN          | Action    |
   |         162 | CLUELESS BUCKET         | Action    |
   |         194 | CROW GREASE             | Action    |
   |         205 | DANCES NONE             | Action    |
   |         210 | DARKO DORADO            | Action    |
   |         212 | DARN FORRESTER          | Action    |
   |         229 | DEVIL DESIRE            | Action    |
   |         250 | DRAGON SQUAD            | Action    |
   |         252 | DREAM PICKUP            | Action    |
   |         253 | DRIFTER COMMANDMENTS    | Action    |
   |         271 | EASY GLADIATOR          | Action    |
   |         287 | ENTRAPMENT SATISFACTION | Action    |
   |         292 | EXCITEMENT EVE          | Action    |
   |         303 | FANTASY TROOPERS        | Action    |
   |         318 | FIREHOUSE VIETNAM       | Action    |
   |         327 | FOOL MOCKINGBIRD        | Action    |
   |         329 | FORREST SONS            | Action    |
   |         360 | GLASS DYING             | Action    |
   |         371 | GOSFORD DONNIE          | Action    |
   |         375 | GRAIL FRANKENSTEIN      | Action    |
   |         395 | HANDICAP BOONDOCK       | Action    |
   |         417 | HILLS NEIGHBORS         | Action    |
   |         501 | KISSING DOLLS           | Action    |
   |         511 | LAWRENCE LOVE           | Action    |
   |         530 | LORD ARIZONA            | Action    |
   |         542 | LUST LOCK               | Action    |
   |         549 | MAGNOLIA FORRESTER      | Action    |
   |         574 | MIDNIGHT WESTWARD       | Action    |
   |         579 | MINDS TRUMAN            | Action    |
   |         586 | MOCKINGBIRD HOLLYWOOD   | Action    |
   |         594 | MONTEZUMA COMMAND       | Action    |
   |         659 | PARK CITIZEN            | Action    |
   |         664 | PATRIOT ROMAN           | Action    |
   |         697 | PRIMARY GLASS           | Action    |
   |         707 | QUEST MUSSOLINI         | Action    |
   |         717 | REAR TRADING            | Action    |
   |         732 | RINGS HEARTBREAKERS     | Action    |
   |         748 | RUGRATS SHAKESPEARE     | Action    |
   |         793 | SHRUNK DIVINE           | Action    |
   |         794 | SIDE ARK                | Action    |
   |         802 | SKY MIRACLE             | Action    |
   |         823 | SOUTH WAIT              | Action    |
   |         825 | SPEAKEASY DATE          | Action    |
   |         838 | STAGECOACH ARMAGEDDON   | Action    |
   |         850 | STORY SIDE              | Action    |
   |         869 | SUSPECTS QUILLS         | Action    |
   |         911 | TRIP NEWTON             | Action    |
   |         915 | TRUMAN CRAZY            | Action    |
   |         927 | UPRISING UPTOWN         | Action    |
   |         964 | WATERFRONT DELIVERANCE  | Action    |
   |         968 | WEREWOLF LOLA           | Action    |
   |         982 | WOMEN DORADO            | Action    |
   |         991 | WORST BANGER            | Action    |
   |          18 | ALTER VICTORY           | Animation |
   |          23 | ANACONDA CONFESSIONS    | Animation |
   |          36 | ARGONAUTS TOWN          | Animation |
   |          70 | BIKINI BORROWERS        | Animation |
   |          78 | BLACKOUT PRIVATE        | Animation |
   |          89 | BORROWERS BEDAZZLED     | Animation |
   |         118 | CANYON STOCK            | Animation |
   |         121 | CAROL TEXAS             | Animation |
   |         134 | CHAMPION FLATLINERS     | Animation |
   |         154 | CLASH FREDDY            | Animation |
   |         160 | CLUB GRAFFITI           | Animation |
   |         193 | CROSSROADS CASUALTIES   | Animation |
   |         208 | DARES PLUTO             | Animation |
   |         223 | DESIRE ALIEN            | Animation |
   |         239 | DOGMA FAMILY            | Animation |
   |         241 | DONNIE ALLEY            | Animation |
   |         243 | DOORS PRESIDENT         | Animation |
   |         245 | DOUBLE WRATH            | Animation |
   |         259 | DUCK RACER              | Animation |
   |         268 | EARLY HOME              | Animation |
   |         300 | FALCON VOLUME           | Animation |
   |         314 | FIGHT JAWBREAKER        | Animation |
   |         325 | FLOATS GARDEN           | Animation |
   |         326 | FLYING HOOK             | Animation |
   |         330 | FORRESTER COMANCHEROS   | Animation |
   |         349 | GANGS PRIDE             | Animation |
   |         355 | GHOSTBUSTERS ELF        | Animation |
   |         402 | HARPER DYING            | Animation |
   |         430 | HOOK CHARIOTS           | Animation |
   |         433 | HORN WORKING            | Animation |
   |         456 | INCH JET                | Animation |
   |         461 | INSECTS STONE           | Animation |
   |         464 | INTENTIONS EMPIRE       | Animation |
   |         470 | ISHTAR ROCKETEER        | Animation |
   |         489 | JUGGLER HARDLY          | Animation |
   |         510 | LAWLESS VISION          | Animation |
   +-------------+-------------------------+-----------+
   */
   ```

   

4. Listar los nombres de las ciudades junto con sus países.

   ```sql
   SELECT c.nombre, p.nombre FROM ciudad AS c
   INNER JOIN pais AS p ON p.id_pais = c.id_pais
   LIMIT 50;
   /*
   +----------------------+----------------+
   | nombre               | nombre         |
   +----------------------+----------------+
   | Kabul                | Afghanistan    |
   | Batna                | Algeria        |
   | Bchar                | Algeria        |
   | Skikda               | Algeria        |
   | Tafuna               | American Samoa |
   | Benguela             | Angola         |
   | Namibe               | Angola         |
   | South Hill           | Anguilla       |
   | Almirante Brown      | Argentina      |
   | Avellaneda           | Argentina      |
   | Baha Blanca          | Argentina      |
   | Crdoba               | Argentina      |
   | Escobar              | Argentina      |
   | Ezeiza               | Argentina      |
   | La Plata             | Argentina      |
   | Merlo                | Argentina      |
   | Quilmes              | Argentina      |
   | San Miguel de Tucumn | Argentina      |
   | Santa F              | Argentina      |
   | Tandil               | Argentina      |
   | Vicente Lpez         | Argentina      |
   | Yerevan              | Armenia        |
   | Woodridge            | Australia      |
   | Graz                 | Austria        |
   | Linz                 | Austria        |
   | Salzburg             | Austria        |
   | Baku                 | Azerbaijan     |
   | Sumqayit             | Azerbaijan     |
   | al-Manama            | Bahrain        |
   | Dhaka                | Bangladesh     |
   | Jamalpur             | Bangladesh     |
   | Tangail              | Bangladesh     |
   | Mogiljov             | Belarus        |
   | Molodetno            | Belarus        |
   | El Alto              | Bolivia        |
   | Sucre                | Bolivia        |
   | Alvorada             | Brazil         |
   | Angra dos Reis       | Brazil         |
   | Anpolis              | Brazil         |
   | Aparecida de Goinia  | Brazil         |
   | Araatuba             | Brazil         |
   | Bag                  | Brazil         |
   | Belm                 | Brazil         |
   | Blumenau             | Brazil         |
   | Boa Vista            | Brazil         |
   | Braslia              | Brazil         |
   | Goinia               | Brazil         |
   | Guaruj               | Brazil         |
   | guas Lindas de Gois  | Brazil         |
   | Ibirit               | Brazil         |
   +----------------------+----------------+
   */
   ```

   

5. Obtener los detalles de los alquileres, incluyendo el cliente y el
   empleado que gestionó el alquiler.

   ```sql
   SELECT a.id_alquiler,
   CONCAT_WS(' ', e.nombre, e.apellidos) AS nombre_empleado,
   CONCAT_WS(' ', c.nombre, c.apellidos) AS nombre_cliente
   FROM cliente AS c
   INNER JOIN alquiler AS a ON a.id_cliente = c.id_cliente
   INNER JOIN empleado AS e ON e.id_empleado = a.id_empleado
   LIMIT 50;
   
   /*
   +-------------+-----------------+------------------+
   | id_alquiler | nombre_empleado | nombre_cliente   |
   +-------------+-----------------+------------------+
   |          76 | Jon Stephens    | MARY SMITH       |
   |         573 | Mike Hillyer    | MARY SMITH       |
   |        1185 | Jon Stephens    | MARY SMITH       |
   |        1422 | Jon Stephens    | MARY SMITH       |
   |        1476 | Mike Hillyer    | MARY SMITH       |
   |        1725 | Mike Hillyer    | MARY SMITH       |
   |        2308 | Jon Stephens    | MARY SMITH       |
   |        2363 | Mike Hillyer    | MARY SMITH       |
   |        3284 | Mike Hillyer    | MARY SMITH       |
   |        4526 | Jon Stephens    | MARY SMITH       |
   |        4611 | Jon Stephens    | MARY SMITH       |
   |        5244 | Jon Stephens    | MARY SMITH       |
   |        5326 | Mike Hillyer    | MARY SMITH       |
   |        6163 | Jon Stephens    | MARY SMITH       |
   |        7273 | Mike Hillyer    | MARY SMITH       |
   |        7841 | Jon Stephens    | MARY SMITH       |
   |        8033 | Mike Hillyer    | MARY SMITH       |
   |        8074 | Mike Hillyer    | MARY SMITH       |
   |        8116 | Mike Hillyer    | MARY SMITH       |
   |        8326 | Jon Stephens    | MARY SMITH       |
   |        9571 | Jon Stephens    | MARY SMITH       |
   |       10437 | Mike Hillyer    | MARY SMITH       |
   |       11299 | Jon Stephens    | MARY SMITH       |
   |       11367 | Mike Hillyer    | MARY SMITH       |
   |       11824 | Jon Stephens    | MARY SMITH       |
   |       12250 | Mike Hillyer    | MARY SMITH       |
   |       13068 | Jon Stephens    | MARY SMITH       |
   |       13176 | Jon Stephens    | MARY SMITH       |
   |       14762 | Mike Hillyer    | MARY SMITH       |
   |       14825 | Jon Stephens    | MARY SMITH       |
   |       15298 | Mike Hillyer    | MARY SMITH       |
   |       15315 | Jon Stephens    | MARY SMITH       |
   |         320 | Jon Stephens    | PATRICIA JOHNSON |
   |        2128 | Jon Stephens    | PATRICIA JOHNSON |
   |        5636 | Mike Hillyer    | PATRICIA JOHNSON |
   |        5755 | Mike Hillyer    | PATRICIA JOHNSON |
   |        7346 | Mike Hillyer    | PATRICIA JOHNSON |
   |        7376 | Jon Stephens    | PATRICIA JOHNSON |
   |        7459 | Jon Stephens    | PATRICIA JOHNSON |
   |        8230 | Jon Stephens    | PATRICIA JOHNSON |
   |        8598 | Jon Stephens    | PATRICIA JOHNSON |
   |        8705 | Mike Hillyer    | PATRICIA JOHNSON |
   |        9031 | Jon Stephens    | PATRICIA JOHNSON |
   |        9236 | Mike Hillyer    | PATRICIA JOHNSON |
   |        9248 | Mike Hillyer    | PATRICIA JOHNSON |
   |        9296 | Mike Hillyer    | PATRICIA JOHNSON |
   |        9465 | Jon Stephens    | PATRICIA JOHNSON |
   |       10136 | Mike Hillyer    | PATRICIA JOHNSON |
   |       10466 | Mike Hillyer    | PATRICIA JOHNSON |
   |       10918 | Mike Hillyer    | PATRICIA JOHNSON |
   +-------------+-----------------+------------------+
   */
   ```

   

6. Encontrar todas las películas que se encuentran en un almacén
   específico.

   ```SQL
   SELECT p.titulo, a.id_almacen FROM pelicula AS p
   INNER JOIN inventario AS i ON i.id_pelicula = p.id_pelicula 
   INNER JOIN almacen AS a ON a.id_almacen = i.id_almacen
   LIMIT 50;
   
   /*
   +------------------+------------+
   | titulo           | id_almacen |
   +------------------+------------+
   | ACADEMY DINOSAUR |          1 |
   | ACADEMY DINOSAUR |          1 |
   | ACADEMY DINOSAUR |          1 |
   | ACADEMY DINOSAUR |          1 |
   | ACADEMY DINOSAUR |          2 |
   | ACADEMY DINOSAUR |          2 |
   | ACADEMY DINOSAUR |          2 |
   | ACADEMY DINOSAUR |          2 |
   | ACE GOLDFINGER   |          2 |
   | ACE GOLDFINGER   |          2 |
   | ACE GOLDFINGER   |          2 |
   | ADAPTATION HOLES |          2 |
   | ADAPTATION HOLES |          2 |
   | ADAPTATION HOLES |          2 |
   | ADAPTATION HOLES |          2 |
   | AFFAIR PREJUDICE |          1 |
   | AFFAIR PREJUDICE |          1 |
   | AFFAIR PREJUDICE |          1 |
   | AFFAIR PREJUDICE |          1 |
   | AFFAIR PREJUDICE |          2 |
   | AFFAIR PREJUDICE |          2 |
   | AFFAIR PREJUDICE |          2 |
   | AFRICAN EGG      |          2 |
   | AFRICAN EGG      |          2 |
   | AFRICAN EGG      |          2 |
   | AGENT TRUMAN     |          1 |
   | AGENT TRUMAN     |          1 |
   | AGENT TRUMAN     |          1 |
   | AGENT TRUMAN     |          2 |
   | AGENT TRUMAN     |          2 |
   | AGENT TRUMAN     |          2 |
   | AIRPLANE SIERRA  |          1 |
   | AIRPLANE SIERRA  |          1 |
   | AIRPLANE SIERRA  |          2 |
   | AIRPLANE SIERRA  |          2 |
   | AIRPLANE SIERRA  |          2 |
   | AIRPORT POLLOCK  |          2 |
   | AIRPORT POLLOCK  |          2 |
   | AIRPORT POLLOCK  |          2 |
   | AIRPORT POLLOCK  |          2 |
   | ALABAMA DEVIL    |          1 |
   | ALABAMA DEVIL    |          1 |
   | ALABAMA DEVIL    |          1 |
   | ALABAMA DEVIL    |          2 |
   | ALABAMA DEVIL    |          2 |
   | ALADDIN CALENDAR |          1 |
   | ALADDIN CALENDAR |          1 |
   | ALADDIN CALENDAR |          1 |
   | ALADDIN CALENDAR |          1 |
   | ALADDIN CALENDAR |          2 |
   +------------------+------------+
   */
   ```

   

7. Listar los nombres y apellidos de los empleados junto con las
   direcciones de los almacenes en los que trabajan.

   ```SQL
   select CONCAT_WS(' ', e.nombre, e.apellidos) AS nombre_empleado,
   d.direccion, d.direccion2
   FROM empleado AS e
   INNER JOIN almacen AS a ON e.id_almacen = a.id_almacen
   INNER JOIN direccion AS d ON d.id_direccion = a.id_direccion 
   INNER JOIN ciudad AS ci ON ci.id_ciudad = d.id_ciudad
   INNER JOIN pais AS p ON p.id_pais = ci.id_pais
   LIMIT 50;
   
   /*
   +-----------------+--------------------+------------+
   | nombre_empleado | direccion          | direccion2 |
   +-----------------+--------------------+------------+
   | Mike Hillyer    | 28 MySQL Boulevard | NULL       |
   | Jon Stephens    | 28 MySQL Boulevard | NULL       |
   | Pepe Spilberg   | 28 MySQL Boulevard | NULL       |
   | Ada Byron       | 47 MySakila Drive  | NULL       |
   | Ringo Rooksby   | 47 MySakila Drive  | NULL       |
   +-----------------+--------------------+------------+
   */
   ```

   

8. Obtener una lista de pagos realizados, incluyendo el cliente, el
   empleado que registró el pago y el alquiler correspondiente.

   ```sql
   SELECT p.id_pago,
   CONCAT_WS(' ', e.nombre, e.apellidos) AS nombre_empleado,
   CONCAT_WS(' ', c.nombre, c.apellidos) AS nombre_cliente
   FROM empleado AS e 
   INNER JOIN pago AS p ON p.id_empleado = e.id_empleado
   INNER JOIN cliente AS c ON p.id_cliente = c.id_cliente
   LIMIT 50;
   /*+---------+-----------------+------------------+
   | id_pago | nombre_empleado | nombre_cliente   |
   +---------+-----------------+------------------+
   |       1 | Mike Hillyer    | MARY SMITH       |
   |       2 | Mike Hillyer    | MARY SMITH       |
   |       3 | Mike Hillyer    | MARY SMITH       |
   |       4 | Jon Stephens    | MARY SMITH       |
   |       5 | Jon Stephens    | MARY SMITH       |
   |       6 | Mike Hillyer    | MARY SMITH       |
   |       7 | Mike Hillyer    | MARY SMITH       |
   |       8 | Jon Stephens    | MARY SMITH       |
   |       9 | Mike Hillyer    | MARY SMITH       |
   |      10 | Jon Stephens    | MARY SMITH       |
   |      11 | Mike Hillyer    | MARY SMITH       |
   |      12 | Mike Hillyer    | MARY SMITH       |
   |      13 | Mike Hillyer    | MARY SMITH       |
   |      14 | Mike Hillyer    | MARY SMITH       |
   |      15 | Jon Stephens    | MARY SMITH       |
   |      16 | Mike Hillyer    | MARY SMITH       |
   |      17 | Jon Stephens    | MARY SMITH       |
   |      18 | Mike Hillyer    | MARY SMITH       |
   |      19 | Jon Stephens    | MARY SMITH       |
   |      20 | Jon Stephens    | MARY SMITH       |
   |      21 | Jon Stephens    | MARY SMITH       |
   |      22 | Jon Stephens    | MARY SMITH       |
   |      23 | Jon Stephens    | MARY SMITH       |
   |      24 | Mike Hillyer    | MARY SMITH       |
   |      25 | Jon Stephens    | MARY SMITH       |
   |      26 | Mike Hillyer    | MARY SMITH       |
   |      27 | Jon Stephens    | MARY SMITH       |
   |      28 | Jon Stephens    | MARY SMITH       |
   |      29 | Mike Hillyer    | MARY SMITH       |
   |      30 | Mike Hillyer    | MARY SMITH       |
   |      31 | Jon Stephens    | MARY SMITH       |
   |      32 | Mike Hillyer    | MARY SMITH       |
   |      33 | Mike Hillyer    | PATRICIA JOHNSON |
   |      34 | Mike Hillyer    | PATRICIA JOHNSON |
   |      35 | Mike Hillyer    | PATRICIA JOHNSON |
   |      36 | Mike Hillyer    | PATRICIA JOHNSON |
   |      37 | Jon Stephens    | PATRICIA JOHNSON |
   |      38 | Mike Hillyer    | PATRICIA JOHNSON |
   |      39 | Jon Stephens    | PATRICIA JOHNSON |
   |      40 | Jon Stephens    | PATRICIA JOHNSON |
   |      41 | Mike Hillyer    | PATRICIA JOHNSON |
   |      42 | Jon Stephens    | PATRICIA JOHNSON |
   |      43 | Mike Hillyer    | PATRICIA JOHNSON |
   |      44 | Jon Stephens    | PATRICIA JOHNSON |
   |      45 | Jon Stephens    | PATRICIA JOHNSON |
   |      46 | Jon Stephens    | PATRICIA JOHNSON |
   |      47 | Jon Stephens    | PATRICIA JOHNSON |
   |      48 | Mike Hillyer    | PATRICIA JOHNSON |
   |      49 | Mike Hillyer    | PATRICIA JOHNSON |
   |      50 | Mike Hillyer    | PATRICIA JOHNSON |
   +---------+-----------------+------------------+*/
   ```

   

9. Listar las películas y los idiomas en los que están disponibles.

10. Encontrar todos los empleados y los almacenes que gestionan.
    Obtener los títulos de las películas que nunca han sido
    alquiladas.

11. Listar los empleados que trabajan en el mismo almacén que el
    empleado con id_empleado = 1.

12. Encontrar el nombre de las ciudades que no tienen ningún
    cliente registrado.

13. Obtener los nombres y apellidos de los actores que han
    participado en más de 10 películas.(having)

14. Encontrar los nombres y apellidos de los clientes que han
    realizado un pago mayor a 100.

15. Listar los títulos de las películas lanzadas en el mismo año que
    la película con id_pelicula = 2.