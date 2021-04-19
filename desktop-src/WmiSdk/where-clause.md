---
description: Verwenden Sie die WHERE-Klausel, um den Bereich einer Daten-, Ereignis-oder Schema Abfrage einzuschränken.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: WHERE-Klausel (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e68d8266b72f6e41e17c0b85766b7a58bb197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362731"
---
# <a name="where-clause-wmi"></a>WHERE-Klausel (WMI)

Verwenden Sie die WHERE-Klausel, um den Bereich einer Daten-, Ereignis-oder Schema Abfrage einzuschränken. Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md). Die WHERE-Klausel besteht aus einer Eigenschaft oder einem Schlüsselwort, einem Operator und einer Konstante. Alle WHERE-Klauseln müssen einen der vordefinierten Operatoren angeben, die im Windows-Verwaltungsinstrumentation (WMI) Query Language (WQL) enthalten sind. Sie können die WHERE-Klausel an die SELECT-Anweisung anfügen, indem Sie eine der folgenden Formen verwenden:


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



Where \* ist das Element, nach dem abgefragt wird, die Klasse ist die Klasse, in der abgefragt werden soll, und Konstante, Operator und Eigenschaft sind die Konstante, der Operator und die Eigenschaft bzw. das Schlüsselwort, die verwendet werden sollen. Weitere Informationen zur SELECT-Anweisung finden Sie unter [SELECT-Anweisung für Daten Abfragen](select-statement-for-data-queries.md), [SELECT-Anweisung für Ereignis Abfragen](select-statement-for-event-queries.md)oder [SELECT-Anweisung für Schema Abfragen](select-statement-for-schema-queries.md).

Der Wert der Konstante muss den richtigen Typ für die Eigenschaft aufweisen. Außerdem muss der Operator in der Liste der gültigen [WQL-Operatoren](wql-operators.md)enthalten sein. Entweder ein Eigenschaftsname oder eine Konstante muss auf beiden Seiten des Operators in der WHERE-Klausel angezeigt werden.

Sie können Zeichen folgen Literale, wie z. b. "NTFS", in einer WHERE-Klausel verwenden. Wenn Sie die folgenden Sonderzeichen in die Zeichenfolge einschließen möchten, müssen Sie das Zeichen zunächst mit einem Escapezeichen versehen, indem Sie dem Zeichen einen umgekehrten Schrägstrich ( \) :

-   umgekehrten Schrägstrich\\\)
-   doppelte Anführungszeichen ( \\ ")
-   einfache Anführungszeichen ( \\ ')

Beliebige arithmetische Ausdrücke können nicht verwendet werden. Die folgende Abfrage gibt beispielsweise nur die Instanzen der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse zurück, die NTFS-Laufwerke darstellen:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



Eigenschaftsnamen können nicht auf beiden Seiten des Operators angezeigt werden. Die folgende Abfrage ist ein Beispiel für eine ungültige Abfrage:


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



Bei den meisten Verwendungsmöglichkeiten von Klassen Deskriptoren in einer WHERE-Klausel wird die Abfrage von WMI als ungültig gekennzeichnet, und es wird ein Fehler zurückgegeben. Verwenden Sie jedoch den Punkt Operator (.) für Eigenschaften vom Typ " **Object** " in WMI. Beispielsweise ist die folgende Abfrage gültig, wenn "prop" eine gültige Eigenschaft von "MyClass" und "Type **Object**" ist:

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

Bei Vergleichstests wird immer die Groß-/Kleinschreibung beachtet Das heißt, die folgenden drei Anweisungen werden alle als **true** ausgewertet:


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



Sie können eine Abfrage erstellen, die boolesche Datentypen enthält, aber die einzigen gültigen booleschen Operanden Typen sind die Typen =,! = und <> . Der Wert **true** entspricht der Zahl 1, und der Wert **false** entspricht der Zahl 0. Die folgenden Beispiele sind Abfragen, die einen booleschen Wert mit den Werten **true** oder **false** vergleichen.


```sql
SELECT * FROM MyClass WHERE BoolProp = 1
SELECT * FROM MyClass WHERE BoolProp = TRUE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
SELECT * FROM MyClass WHERE BoolProp = 0
SELECT * FROM MyClass WHERE BoolProp = FALSE
SELECT * FROM MyClass WHERE BoolProp != 1
SELECT * FROM MyClass WHERE BoolProp != FALSE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
```



Die folgenden Beispiele sind ungültige Abfragen, bei denen versucht wird, ungültige Operanden zu verwenden.


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



Mehrere Gruppen von Eigenschaften, Operatoren und Konstanten können in einer WHERE-Klausel mit logischen Operatoren und Klammer unter Ausdrücken kombiniert werden. Jede Gruppe muss mit den [Operatoren](wql-operators.md) and, or oder not verknüpft werden, wie in den folgenden Abfragen gezeigt. Die erste Abfrage ruft alle Instanzen der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse ab, wobei die **Name** -Eigenschaft entweder auf C oder D festgelegt ist:


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



Die zweite Abfrage ruft Datenträger mit dem Namen "C:" oder "D:" nur dann ab, wenn Sie über eine bestimmte Menge an freiem Speicherplatz verfügen und NTFS-Dateisysteme aufweisen:


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



Dieses Beispiel zeigt eine Schema Abfrage mit der WHERE-Klausel.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



Die Klasse Meta \_ Class identifiziert dies als Schema Abfrage. die Eigenschaft, die als bezeichnet wird, \_ \_ identifiziert die Zielklasse der Abfrage, und der [ISA-Operator](isa-operator-for-schema-queries.md) fordert Definitionen für die Unterklassen der Zielklasse an. Daher gibt die vorherige Abfrage die Definition für die myClassName-Klasse und Definitionen für alle zugehörigen Unterklassen zurück.

Das folgende Beispiel ist eine Datenabfrage, die die [assoziatoren der-Anweisung](associators-of-statement.md) mit WHERE verwendet:


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



Das nächste Beispiel zeigt eine Schema Abfrage mit assoziatoren von und, wobei:


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



Das folgende Beispiel zeigt eine Datenabfrage, die die [Verweise der-Anweisung](references-of-statement.md) und wobei verwendet:


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



Bei diesem letzten Beispiel handelt es sich um eine Schema Abfrage mit Verweisen auf und, wobei:


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Zusätzlich zum WMI- [DateTime](date-and-time-format.md) -Format unterstützt die WQL WHERE-Klausel verschiedene andere Datums-und Uhrzeit Formate:

-   [WQL-unterstützte Datumsformate](wql-supported-date-formats.md)
-   [Von WQL unterstützte Zeitformate](wql-supported-time-formats.md)

 

 
