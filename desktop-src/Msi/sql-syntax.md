---
description: Die SQL-Abfrage Zeichenfolgen für Windows Installer sind auf die folgenden Formate beschränkt.
ms.assetid: badee528-fa69-43ab-965e-d9e6f2529b99
title: SQL-Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1b7d1179a8b6035186a9a5e78f46fdc857ac18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864216"
---
# <a name="sql-syntax"></a>SQL-Syntax

Die SQL-Abfrage Zeichenfolgen für Windows Installer sind auf die folgenden Formate beschränkt.



| Aktion                             | Abfrage                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gruppe von Datensätzen auswählen          | Wählen Sie eine \[ eindeutige \] {Column-List} aus {Table-List} aus, \[ wobei {Operation-List} \] \[ Order by {Column-List}\]                                                                                                                                                                                                                                                                                                                                                                                                       |
| Löschen von Datensätzen aus einer Tabelle        | Aus {Table} löschen, \[ wobei {Operation-list}\]                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ändern vorhandener Datensätze in einer Tabelle | Aktualisieren von {Table-List} Set {Column} = {Constant} \[ , {Column} = {Constant} \] \[ ,.. \] \[ . Where {Operation-List} \] Update-Abfragen funktionieren nur für nicht-Primärschlüssel Spalten.<br/>                                                                                                                                                                                                                                                                                                                                      |
| Hinzufügen von Datensätzen zu einer Tabelle             | INSERT INTO {TABLE} ({Column-List})-Werte ({Constant-List} \[ ) \] können temporäre Binärdaten nicht direkt mithilfe der INSERT INTO-oder Update SQL-Abfragen in eine Tabelle eingefügt werden. Weitere Informationen finden Sie unter [Hinzufügen von Binärdaten zu einer Tabelle mithilfe von SQL](adding-binary-data-to-a-table-using-sql.md).<br/>                                                                                                                                                                                                       |
| Hinzufügen einer Tabelle                        | Beim Hinzufügen einer Tabelle müssen die Spaltentypen CREATE TABLE {table} ({Column} {Column Type}) \[ \] für jede Spalte angegeben werden. Mindestens eine Primärschlüssel Spalte muss für die Erstellung einer neuen Tabelle angegeben werden. Die möglichen Ersetzungen für {Column Type} in den oben aufgeführten lauten: Char \[ ({Size}) \] \| Zeichen \[ ({Size}) \] \| LONGCHAR \| Short \| int \| Integer \| Long \| Object \[ not NULL \] \[ temporär \] \[ lokalisierbar \] \[ , Spalte... \] \[ ,. \] .. Primärschlüssel Spalte \[ , Spalte \] \[ ,.. \] .<br/> |
| Entfernen einer Tabelle                     | DROP TABLE {table}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Hinzufügen eines Spaltennamens                       | ALTER TABLE {table} Add {Column} {Column Type} der Spaltentyp muss beim Hinzufügen einer Spalte angegeben werden. Die möglichen Ersetzungen für {Column Type} sind im obigen Beispiel: Char \[ ({Size}) \] \| Character \[ ({Size}) \] \| LONGCHAR \| Short \| int \| Integer \| Long \| Object \[ not NULL \] \[ temporär \] \[ Lokalisier barer \] \[ Halt \] .<br/>                                                                                                                                                                  |
| Speichern und Freigeben von temporären Tabellen     | ALTER TABLE {table Name} holdalter table {table Name} Free<br/> Der Benutzer kann die Hold-Befehle verwenden und freigeben, um die Lebensdauer einer temporären Tabelle oder einer temporären Spalte zu steuern. Die haltenzahl für eine Tabelle wird für jeden SQL-Hold-Vorgang in dieser Tabelle erhöht und für jeden SQL-Free-Vorgang in der Tabelle dekrementiert. Wenn die letzte haltenzahl für eine Tabelle freigegeben wird, kann nicht auf alle temporären Spalten zugegriffen werden. Wenn alle Spalten temporär sind, kann auf die Tabelle nicht zugegriffen werden.<br/>     |



 

Weitere Informationen finden Sie unter [Beispiele für Datenbankabfragen mit SQL und Skript](examples-of-database-queries-using-sql-and-script.md).

### <a name="sql-grammar"></a>SQL-Grammatik

Die optionalen Parameter werden in eckige Klammern angezeigt \[ \] . Wenn mehrere Optionen aufgeführt werden, werden die optionalen Parameter durch einen senkrechten Strich getrennt.

"{Constant}" ist entweder eine Zeichenfolge oder eine ganze Zahl. Eine Zeichenfolge muss in einfache Anführungszeichen ' example ' eingeschlossen werden. "{Constant-List}" ist eine durch Trennzeichen getrennte Liste mit einer oder mehreren Konstanten.

Mit der lokalisierbaren Option wird ein Spalten Attribut festgelegt, das angibt, dass die Spalte lokalisiert werden muss.

Ein {Column} ist ein Spalten basierter Verweis auf einen Wert in einem Feld einer Tabelle.

Ein {Marker} ist ein Parameter Verweis auf einen Wert, der von einem mit der Abfrage übermittelten Datensatz bereitgestellt wird. Sie wird in der SQL-Anweisung durch ein Fragezeichen dargestellt?. Weitere Informationen zur Verwendung von Parametern finden Sie unter der [**msiviewexecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) -Funktion oder der [**Execute**](view-execute.md) -Methode.

Die Windows Installer SQL-Syntax unterstützt das Escapezeichen in einfachen Anführungszeichen (ASCII-Wert 39) nicht in einem Zeichenfolgenliteral. Sie können jedoch den Datensatz abrufen oder erstellen, das Feld mit der [**StringData**](record-stringdata.md) -Eigenschaft oder der [**IntegerData**](record-integerdata.md) -Eigenschaft festlegen und dann die [**Modify**](view-modify.md) -Methode aufzurufen. Alternativ können Sie einen Datensatz erstellen und die in der [**Execute**](view-execute.md) -Methode beschriebene Parametermarker (?) verwenden. Dies können Sie auch mithilfe der Datenbankfunktionen " [**msiviewexecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)", " [**msirecordsetinteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)" und " [**msirecordsetstring**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)" erreichen.

Eine WHERE {Operation-list}-Klausel ist optional und eine Gruppierung von Vorgängen, die zum Filtern der Auswahl verwendet werden. Die Vorgänge müssen die folgenden Typen aufweisen:

-   {Column} = {Column}
-   {Column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {Konstante}
-   {Column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {Marker}
-   {column} ist NULL.
-   {column} ist nicht NULL.

Für Zeichen folgen Werte sind nur die Vorgänge = oder <> möglich. Objektwert Vergleiche sind auf is NULL und is not NULL beschränkt.

Einzelne Vorgänge können nach-und-oder-oder-Operatoren gruppiert werden. Die Reihenfolge kann durch die Verwendung von Klammern () erzwungen werden.

Die Order By-Klausel ist optional und bewirkt eine anfängliche Verzögerung während der Sortierung. Durch die Sortierung nach Zeichen folgen werden identische Zeichen folgen gruppiert, aber die Zeichen folgen werden nicht alphabetisch sortiert.

Die eindeutige-Klausel ist optional und wiederholt keine identischen Datensätze im zurückgegebenen Resultset.

Eine {Table-List} ist eine durch Trennzeichen getrennte Liste mit einem oder mehreren Tabellennamen, die im Join als {Table} bezeichnet werden.

Eine {Column-List} ist eine durch Trennzeichen getrennte Liste mit einer oder mehreren Tabellen Spalten, die als {Column} Selected bezeichnet werden. Mehrdeutige Spalten können als {TableName. Column} weiter qualifiziert werden. Ein Sternchen kann als Spaltenliste in einer SELECT-Abfrage verwendet werden, um alle Spalten in den Tabellen darzustellen, auf die verwiesen wird. Wenn Sie nach Spaltenposition auf Felder verweisen, wählen Sie die Spalten anhand des Namens aus, anstatt das Sternchen zu verwenden. Ein Sternchen kann nicht als Spaltenliste in einer INSERT INTO-Abfrage verwendet werden.

Um Tabellennamen und Spaltennamen, die mit SQL-Schlüsselwörtern kollidieren, zu beenden, müssen Sie den Namen zwischen zwei schweren Akzentzeichen \` \` (ASCII-Wert 96) einschließen. Wenn ein Spaltenname mit Escapezeichen versehen werden muss und als {TableName. Column} qualifiziert ist, müssen die Tabelle und die Spalte einzeln mit Escapezeichen versehen werden ({ \` TableName) \` . \` Spalte \` }. Es wird empfohlen, dass alle Tabellennamen und Spaltennamen auf diese Weise mit Escapezeichen versehen werden, um Konflikte mit reservierten Wörtern zu vermeiden und eine deutliche Leistung zu erzielen.

Tabellennamen sind auf 31 Zeichen beschränkt. Weitere Informationen finden Sie unter [Tabellennamen](table-names.md). Bei Tabellen-und Spaltennamen wird Groß-/Kleinschreibung beachtet. Bei SQL-Schlüsselwörtern wird die Groß-/Kleinschreibung

Die maximale Anzahl von Ausdrücken in einer WHERE-Klausel einer SQL-Abfrage ist auf 32 beschränkt.

Nur innere Joins werden unterstützt und durch einen Vergleich von Spalten aus unterschiedlichen Tabellen angegeben. Zirkuläre Joins werden nicht unterstützt. Bei einem Zirkel Join handelt es sich um eine SQL-Abfrage, die drei oder mehr Tabellen miteinander verknüpft. Beispielsweise ist der folgende zirkuläre Join:

``` syntax
WHERE Table1.Field1=Table2.Field1 AND Table2.Field2=Table3.Field1 AND Table3.Field2=Table1.Field2.
```

Spalten, die Teil der Primärschlüssel für eine Tabelle sind, müssen zuerst in der Prioritäts Reihenfolge und dann nach allen nicht-Primärschlüssel Spalten definiert werden. Persistente Spalten müssen vor temporären Spalten definiert werden. Die Sortierreihenfolge einer Text Spalte ist nicht definiert. identische Text Werte werden jedoch immer gruppiert.

Beachten Sie, dass Sie beim Hinzufügen oder Erstellen von Spalten den Spaltentyp angeben müssen.

Tabellen dürfen nicht mehr als eine Spalte vom Typ ' Object ' enthalten.

Die maximale Größe, die für eine Zeichen folgen Spalte in einer SQL-Abfrage explizit angegeben werden kann, ist 255. Eine Zeichen folgen Spalte mit unbegrenzter Länge wird als Größe 0 dargestellt. Weitere Informationen finden Sie unter [Column Definition Format](column-definition-format.md).

Zum Ausführen einer SQL-Anweisung muss eine Sicht erstellt werden. Eine Sicht, die kein Resultset erstellt (z. b. CREATE TABLE oder INSERT INTO), kann jedoch nicht mit [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) oder der [**Modify**](view-modify.md) -Methode verwendet werden, um Tabellen in der Sicht zu aktualisieren.

Beachten Sie, dass Sie keinen Datensatz abrufen können, der Binärdaten aus einer Datenbank enthält, und dann diesen Datensatz verwenden, um die Daten in eine vollständig andere Datenbank einzufügen. Wenn Sie Binärdaten aus einer Datenbank in eine andere verschieben möchten, sollten Sie die Daten in eine Datei exportieren und Sie dann über eine Abfrage und die [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) -Funktion in die neue Datenbank importieren. Dadurch wird sichergestellt, dass jede Datenbank über eine eigene Kopie der Binärdaten verfügt.

 

 




