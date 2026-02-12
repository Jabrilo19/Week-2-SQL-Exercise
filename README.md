# Week-2-SQL-Exercise
# 1 and 2
MariaDB [(none)]> create database foy;
Query OK, 1 row affected (0.002 sec)
MariaDB [(none)]> use foy;
Database changed

# 3
MariaDB [foy]> create table vets (lname varchar(100), fname varchar(100), town varchar(100), state varchar(20));
Query OK, 0 rows affected (0.008 sec)

# 4
MariaDB [foy]> LOAD DATA LOCAL INFILE 'C:\\Users\\foyje\\Downloads\\VV.csv' INTO TABLE vets FIELDS TERMINATED BY ',' ENCLOSED BY '"' LINES TERMINATED BY '\n';
Query OK, 58253 rows affected (0.159 sec)
Records: 58253  Deleted: 0  Skipped: 0  Warnings: 0

# 5(A)
MariaDB [foy]>  select count(*) from vets;
+----------+
| count(*) |
+----------+
|    58253 |
+----------+
1 row in set (0.011 sec)

# 5(B)
MariaDB [foy]> select count(*) from vets where state = 'DAYTON';
+----------+
| count(*) |
+----------+
|        0 |
+----------+
1 row in set (0.012 sec)

# 5(C)
MariaDB [foy]> select fname from vets where lname = 'HARRIS';
+----------------------+
| fname                |
+----------------------+
|  ABRAHAM             |
|  ALLAN LYNN          |
|  BENJAMIN            |
|  BENJAMIN HARRY      |
|  BILLY DEAN          |
|  BOBBY GLENN         |
|  BRUCE RANDALL       |
|  BURNIE              |
|  CALVIN              |
|  CARL ALLEN          |
|  CARL COLEMAN        |
|  CARL E              |
|  CHARLES EDWARD      |
|  CHARLES LOUIS       |
|  CHARLES RICKEY      |
|  CLEVELAND SCOTT     |
|  CLINTON EUGENE JR   |
|  CURTIS RAY          |
|  DAVID STANLEY       |
|  DEAN ALLEN          |
|  DENNIS DAY          |
|  DOYLE LEE           |
|  EARL WAYNE          |
|  EDDIE CLAYTON       |
|  EDGAR               |
|  EDWARD JAMES JR     |
|  EDWARD LAWRENCE     |
|  EDWARD LEON         |
|  EDWARD LEWIS        |
|  EDWARD LOUIS        |
|  ELTON ODIS          |
|  ERVIN ELLIS         |
|  EUGENE              |
|  FRANK CAY           |
|  GARY BLUITT         |
|  GEORGE WILLIAM      |
|  GLENN ALVIN         |
|  GRADY HERSHALL      |
|  GREGORY JOHN        |
|  HAL                 |
|  HARLIN JR           |
|  HAROLD LEE          |
|  HAROLD RAY          |
|  HARRY JAMES         |
|  HARRY KENDALL JR    |
|  HARVEY C            |
|  HARVEY JR           |
|  ISAAC               |
|  JACK HAROLD         |
|  JACK JR             |
|  JACK M              |
|  JACK MARSTON        |
|  JACKIE LOUIS        |
|  JAMES BRADDOCK      |
|  JAMES CRAIG         |
|  JAMES FRANKLIN      |
|  JAMES LARRY         |
|  JAMES LOUIS         |
|  JAMES RONALD        |
|  JAMES THOMAS        |
|  JAMES WALDEN JR     |
|  JEFFREY LYNDOL      |
|  JERRY BRUCE         |
|  JERRY LEE           |
|  JESSE LEE           |
|  JESSE LEE           |
|  JESSIE EARL         |
|  JIMMY               |
|  JIMMY LEO           |
|  JOHN CARLOS         |
|  JOHN HENRY JR       |
|  JOHN JAMES          |
|  JOHN LEE JR         |
|  JOHN OLIVER         |
|  JOHNNIE DARRIEL     |
|  JOSEPH RANDAL       |
|  JOSEPH RICHARD      |
|  KENNETH RAY         |
|  KENNETH WARD        |
|  LANTIE LAWRENCE JR  |
|  LARRY CORNELIOUS    |
|  LARRY RAY           |
|  LAWRENCE HUBERT     |
|  LEE RUSSELL         |
|  LESLIE EARL JR      |
|  LEWIS CRAIG         |
|  LYNN ARDEN          |
|  MARVIN              |
|  MATTHEW N JR        |
|  MAX GILBERT         |
|  MICHAEL LEO         |
|  MICHAEL LEROY       |
|  MICHAEL PAUL        |
|  MICHAEL R JR        |
|  MICHAEL STEVENS     |
|  NATHANIEL           |
|  NED HENRY           |
|  NOEL AUSTIN JR      |
|  PATRICK JAMES       |
|  PAUL WINIFORD       |
|  PERRY LEE           |
|  PHILIP ANTHONY      |
|  PRENTISS JR         |
|  RANDALL LYNN        |
|  REUBEN BEAUMONT     |
|  RICHARD FLAMOND     |
|  RICKEY ELTON        |
|  ROBERT DUANE        |
|  ROBERT EARL         |
|  ROBERT ERNEST       |
|  ROBERT EUGENE       |
|  ROBERT GEORGE       |
|  ROBERT JOHN         |
|  ROBERT LEE          |
|  ROBERT TAYLOR       |
|  ROBERT WILLIAM      |
|  RODNEY CARSWELL     |
|  ROLAND LORENZO      |
|  RONALD LEE          |
|  ROY EDWARD          |
|  ROY GREEN JR        |
|  RUSSELL LEE         |
|  SAMUEL GARY         |
|  STEPHEN WARREN      |
|  STEVE WESTLEL       |
|  TERRENCE L          |
|  THOMAS WYATT        |
|  VERN ALLEN          |
|  WALTER              |
|  WESLEY HOMER JR     |
|  WILLIAM DEXTER      |
|  WILLIAM LAWRENCE    |
|  WILLIAM LEE         |
|  WILLIAM LEE         |
|  WILLIAM THOMAS      |
|  WILLIAM THOMAS      |
+----------------------+
136 rows in set (0.011 sec)

MariaDB [foy]>
