---
description: Die SQL Abfragezeichenfolgen für Windows Installer sind auf die folgenden Formate beschränkt.
ms.assetid: badee528-fa69-43ab-965e-d9e6f2529b99
title: SQL-Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6512f52ae687ee3f95a00f104c7cdfa251c878b649809faeb86c73bdcf82bf84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624674"
---
# <a name="sql-syntax"></a>SQL-Syntax

Die SQL Abfragezeichenfolgen für Windows Installer sind auf die folgenden Formate beschränkt.



| Aktion                             | Abfrage                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auswählen einer Gruppe von Datensätzen          | SELECT \[ DISTINCT \] {column-list} FROM {table-list} \[ WHERE {operation-list} \] \[ ORDER BY {column-list}\]                                                                                                                                                                                                                                                                                                                                                                                                       |
| Löschen von Datensätzen aus einer Tabelle        | DELETE FROM {table} \[ WHERE {operation-list}\]                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ändern vorhandener Datensätze in einer Tabelle | UPDATE {table-list} SET {column}= {constant} \[ , {column}= {constant} \] \[ , ... \] \[ WHERE {operation-list} \] UPDATE-Abfragen funktionieren nur für Nichtprimärschlüsselspalten.<br/>                                                                                                                                                                                                                                                                                                                                      |
| Hinzufügen von Datensätzen zu einer Tabelle             | INSERT INTO {table} ({column-list}) VALUES ({constant-list}) TEMPORARY Binary data cannot be inserted into a table directly using the \[ INSERT INTO or UPDATE SQL \] queries. Weitere Informationen finden Sie unter [Adding Binary Data to a Table Using SQL](adding-binary-data-to-a-table-using-sql.md).<br/>                                                                                                                                                                                                       |
| Hinzufügen einer Tabelle                        | CREATE TABLE {table} ( {column} {spaltentyp}) HOLD-Spaltentypen müssen beim Hinzufügen einer Tabelle für jede \[ \] Spalte angegeben werden. Für die Erstellung einer neuen Tabelle muss mindestens eine Primärschlüsselspalte angegeben werden. Die möglichen Ersetzungen für {Spaltentyp} im obigen Beispiel sind: CHAR \[ ( {size} ) \] \| CHARACTER ( \[ {size} ) \] \| LONGCHAR \| SHORT \| INT INTEGER LONG OBJECT \| NOT NULL TEMPORARY \| \| \[ \] \[ \] \[ LOCALIZABLE , \] \[ column... , \] \[ ... \] PRIMARY \[ KEY-Spalte, Spalte \] \[ , ... \] .<br/> |
| Entfernen einer Tabelle                     | DROP TABLE {table}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Hinzufügen eines Spaltennamens                       | ALTER TABLE {table} ADD {column} {column type}Der Spaltentyp muss beim Hinzufügen einer Spalte angegeben werden. Die möglichen Ersetzungen für {Spaltentyp} im obigen Beispiel sind: CHAR \[ ( {size} ) \] \| CHARACTER ( \[ {size} ) \] \| LONGCHAR \| SHORT \| INT INTEGER LONG OBJECT \| NOT NULL TEMPORARY \| \| \[ \] \[ \] \[ LOCALIZABLE HOLD \] \[ \] .<br/>                                                                                                                                                                  |
| Temporäre Tabellen halten und frei     | ALTER TABLE {Tabellenname} HOLDALTER TABLE {Tabellenname} FREE<br/> Der Benutzer kann die Befehle HOLD und FREE verwenden, um die Lebensdauer einer temporären Tabelle oder einer temporären Spalte zu steuern. Die Anzahl der zurückhaltenden Daten für eine Tabelle wird für jeden SQL HOLD-Vorgang für diese Tabelle erhöht und für jeden SQL FREE-Vorgang für die Tabelle dekrementiert. Wenn die letzte Anzahl von Zurückhalten für eine Tabelle freigegeben wird, kann nicht mehr auf alle temporären Spalten zugegriffen werden. Wenn alle Spalten temporär sind, kann nicht mehr auf die Tabelle zugegriffen werden.<br/>     |



 

Weitere Informationen finden Sie unter [Beispiele für Datenbankabfragen mit SQL und Skript](examples-of-database-queries-using-sql-and-script.md).

### <a name="sql-grammar"></a>SQL-Grammatik

Die optionalen Parameter werden in Klammern \[ \] eingeschlossen. Wenn mehrere Optionen aufgeführt sind, werden die optionalen Parameter durch einen vertikalen Balken getrennt.

Eine {constant} ist entweder eine Zeichenfolge oder eine ganze Zahl. Eine Zeichenfolge muss in einfache Anführungszeichen "example" eingeschlossen werden. Eine {constant-list} ist eine durch Trennzeichen getrennte Liste von einer oder mehrere Konstanten.

Die Option LOCALIZABLE legt ein Spaltenattribut fest, das angibt, dass die Spalte lokalisiert werden muss.

Ein {column} ist ein spaltenarer Verweis auf einen Wert in einem Feld einer Tabelle.

Ein {marker} ist ein Parameterverweis auf einen Wert, der von einem mit der Abfrage übermittelten Datensatz bereitgestellt wird. Sie wird in der SQL durch ein Fragezeichen ? dargestellt. Informationen zur Verwendung von Parametern finden Sie entweder in der [**MsiViewExecute-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) oder in der [**Execute-Methode.**](view-execute.md)

Die Windows Installer SQL syntax unterstützt das Verwenden von einfachen Anführungszeichen (ASCII-Wert 39) in einem Zeichenfolgenliteral nicht. Sie können den Datensatz jedoch abrufen oder erstellen, das Feld mit der [**StringData-**](record-stringdata.md) oder [**IntegerData-Eigenschaft**](record-integerdata.md) festlegen und dann die [**Modify-Methode**](view-modify.md) aufrufen. Alternativ können Sie einen Datensatz erstellen und die Parametermarkierungen (?) verwenden, die unter [**Execute-Methode beschrieben**](view-execute.md) sind. Sie können dies auch mithilfe der Datenbankfunktionen [**MsiViewExecute,**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)und [**MsiRecordSetString tun.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)

Eine WHERE{operation-list}-Klausel ist optional und eine Gruppierung von Vorgängen, die zum Filtern der Auswahl verwendet werden sollen. Die Vorgänge müssen die folgenden Typen haben:

-   {column} = {column}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {constant}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {marker}
-   {column} ist NULL
-   {column} ist nicht NULL

Für Zeichenfolgenwerte sind nur die Vorgänge = oder <> möglich. Objektwertvergleiche sind auf IS NULL und IS NOT NULL beschränkt.

Einzelne Vorgänge können nach AND- oder OR-Operatoren gruppiert werden. Die Sortierung kann mithilfe von Klammern () erzwingt werden.

Die ORDER BY-Klausel ist optional und verursacht eine anfängliche Verzögerung während der Sortierung. Durch die Sortierung nach Zeichenfolgen werden identische Zeichenfolgen gruppiert, aber die Zeichenfolgen werden nicht alphabetisch sortiert.

Die DISTINCT-Klausel ist optional und wiederholt keine identischen Datensätze im zurückgegebenen Ergebnisset.

Ein {table-list} ist eine durch Trennzeichen getrennte Liste von Tabellennamen, die im Join als {table} bezeichnet werden.

{column-list} ist eine durch Trennzeichen getrennte Liste von tabellenspalten, die als {column} bezeichnet werden. Mehrdeutige Spalten können als {tablename.column} weiter qualifiziert werden. Ein Sternchen kann als Spaltenliste in einer SELECT-Abfrage verwendet werden, um alle Spalten in den Tabellen, auf die verwiesen wird, zu darstellen. Wenn Sie auf Felder nach Spaltenposition verweisen, wählen Sie die Spalten anhand des Namens aus, anstatt das Sternchen zu verwenden. Ein Sternchen kann nicht als Spaltenliste in einer INSERT INTO-Abfrage verwendet werden.

Um Tabellen- und Spaltennamen mit Escapezeichen zu SQL, schließen Sie den Namen zwischen zwei Akzentmarkierungen \` \` (ASCII-Wert 96) ein. Wenn ein Spaltenname mit Escape escapet werden muss und als {tablename.column} qualifiziert ist, müssen die Tabelle und die Spalte einzeln als { tablename mit Escape \` escapet \` werden. \` Spalte \` }. Es wird empfohlen, dass alle Tabellen- und Spaltennamen auf diese Weise mit Escape escapen, um Konflikte mit reservierten Wörtern zu vermeiden und eine erhebliche Leistung zu erzielen.

Tabellennamen sind auf 31 Zeichen beschränkt. Weitere Informationen finden Sie unter [Tabellennamen.](table-names.md) Bei Tabellen- und Spaltennamen wird die Kleinschreibung beachtet. SQL Schlüsselwörtern wird die Kleinschreibung nicht beachtet.

Die maximale Anzahl von Ausdrücken in einer WHERE-Klausel einer SQL ist auf 32 beschränkt.

Nur innere Joins werden unterstützt und durch einen Vergleich von Spalten aus verschiedenen Tabellen angegeben. Zirkuläre Joins werden nicht unterstützt. Ein zirkulärer Join ist eine SQL Abfrage, die drei oder mehr Tabellen mit einer Verbindung verknüpft. Im Folgenden finden Sie z. B. einen kreisförmigen Join:

``` syntax
WHERE Table1.Field1=Table2.Field1 AND Table2.Field2=Table3.Field1 AND Table3.Field2=Table1.Field2.
```

Spalten, die Teil der Primärschlüssel für eine Tabelle sind, müssen zuerst in der Prioritäts reihenfolge definiert werden, gefolgt von allen spalten, die nicht dem Primärschlüssel gehören. Persistente Spalten müssen vor temporären Spalten definiert werden. Die Sortierreihenfolge einer Textspalte ist nicht definiert. identische Textwerte werden jedoch immer miteinander identident.

Beachten Sie, dass Sie beim Hinzufügen oder Erstellen einer Spalte den Spaltentyp angeben müssen.

Tabellen dürfen nicht mehr als eine Spalte vom Typ "Objekt" enthalten.

Die maximale Größe, die explizit für eine Zeichenfolgenspalte in einer abfrage angegeben SQL ist 255. Eine Zeichenfolgenspalte mit unendlicher Länge wird als 0 dargestellt. Weitere Informationen finden Sie unter [Spaltendefinitionsformat](column-definition-format.md).

Zum Ausführen einer SQL-Anweisung muss eine Sicht erstellt werden. Eine Sicht, die kein ResultSet erstellt, z. B. CREATE TABLE oder INSERT INTO, kann jedoch nicht mit [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) oder der [**Modify-Methode**](view-modify.md) verwendet werden, um Tabellen über die Sicht zu aktualisieren.

Beachten Sie, dass Sie keinen Datensatz mit Binärdaten aus einer Datenbank abrufen und dann mit diesem Datensatz die Daten in eine völlig andere Datenbank einfügen können. Um Binärdaten aus einer Datenbank in eine andere zu verschieben, sollten Sie die Daten in eine Datei exportieren und sie dann über eine Abfrage und die [**MsiRecordSetStream-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) in die neue Datenbank importieren. Dadurch wird sichergestellt, dass jede Datenbank über eine eigene Kopie der Binärdaten verfügt.

 

 




