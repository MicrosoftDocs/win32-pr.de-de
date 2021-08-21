---
description: Verwenden Sie die WHERE-Klausel, um den Bereich einer Daten-, Ereignis- oder Schemaabfrage einzugrenzen.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: WHERE-Klausel (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a6a51657dac26a002890bde8346cd7570f6057f2ace5cdfb5350d6c90d0fee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312181"
---
# <a name="where-clause-wmi"></a>WHERE-Klausel (WMI)

Verwenden Sie die WHERE-Klausel, um den Bereich einer Daten-, Ereignis- oder Schemaabfrage einzugrenzen. Weitere Informationen finden Sie unter [Abfragen mit WQL.](querying-with-wql.md) Die WHERE-Klausel besteht aus einer Eigenschaft oder einem Schlüsselwort, einem Operator und einer Konstante. Alle WHERE-Klauseln müssen einen der vordefinierten Operatoren angeben, die in der Windows Management Instrumentation (WMI) Query Language (WQL) enthalten sind. Sie können die WHERE-Klausel in einer der folgenden Formen an die SELECT-Anweisung anfügen:


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



wobei \* das abgefragte Element ist, ist class die Klasse, in der abgefragt werden soll, und constant, operator und property sind die zu verwendende Konstante, der Operator und die Eigenschaft oder das Schlüsselwort. Weitere Informationen zur SELECT-Anweisung finden Sie unter [SELECT-Anweisung für Datenabfragen,](select-statement-for-data-queries.md) [SELECT-Anweisung für Ereignisabfragen](select-statement-for-event-queries.md)oder [SELECT-Anweisung für Schemaabfragen.](select-statement-for-schema-queries.md)

Der Wert der Konstante muss den richtigen Typ für die Eigenschaft aufweisen. Darüber hinaus muss sich der Operator in der Liste der gültigen [WQL-Operatoren befinden.](wql-operators.md) Entweder muss ein Eigenschaftenname oder eine Konstante auf beiden Seiten des Operators in der WHERE-Klausel angezeigt werden.

Sie können Zeichenfolgenliterale wie "NTFS" in einer WHERE-Klausel verwenden. Wenn Sie die folgenden Sonderzeichen in die Zeichenfolge einschließen möchten, müssen Sie das Zeichen zunächst mit einem Escapezeichen versehen, indem Sie dem Zeichen einen umgekehrten Schrägstrich voran setzen ( \\ ):

-   umgekehrter Schrägstrich ( \\ \\ )
-   doppelte Anführungszeichen ( \\ ")
-   einfache Anführungszeichen ( \\ ')

Beliebige arithmetische Ausdrücke können nicht verwendet werden. Die folgende Abfrage gibt beispielsweise nur die Instanzen der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) zurück, die NTFS-Laufwerke darstellen:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



Eigenschaftsnamen können nicht auf beiden Seiten des Operators angezeigt werden. Die folgende Abfrage ist ein Beispiel für eine ungültige Abfrage:


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



Für die meisten Verwendungsmöglichkeiten von Klassendeskriptoren in einer WHERE-Klausel kennzeichnet WMI die Abfrage als ungültig und gibt einen Fehler zurück. Verwenden Sie jedoch den Punktoperator (.) für Eigenschaften des Typs **Object** in WMI. Die folgende Abfrage ist beispielsweise gültig, wenn Prop eine gültige Eigenschaft von MyClass und ein **Typobjekt** ist:

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

Bei Vergleichstests wird die Groß-/Kleinschreibung immer nicht beachtet. Das heißt, die folgenden drei Anweisungen werden alle zu **TRUE** ausgewertet:


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



Sie können eine Abfrage erstellen, die boolesche Datentypen enthält, aber die einzigen gültigen booleschen Operandentypen sind die Typen =, != und <> . Der Wert **TRUE** entspricht der Zahl 1, und der Wert **FALSE** entspricht der Zahl 0. Die folgenden Beispiele sind Abfragen, die einen booleschen Wert mit den Werten **TRUE** oder **FALSE** vergleichen.


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



Die folgenden Beispiele sind ungültige Abfragen, die versuchen, ungültige Operanden zu verwenden.


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



Mehrere Gruppen von Eigenschaften, Operatoren und Konstanten können in einer WHERE-Klausel mit logischen Operatoren und klammernförmigen Teilausdrucken kombiniert werden. Jede Gruppe muss mit den [Operatoren](wql-operators.md) AND, OR oder NOT verknüpft werden, wie in den folgenden Abfragen gezeigt. Die erste Abfrage ruft alle Instanzen der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) ab, wobei die **Name-Eigenschaft** entweder auf C oder D festgelegt ist:


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



Die zweite Abfrage ruft Datenträger mit dem Namen "C:" oder "D:" nur dann ab, wenn sie über eine bestimmte Menge an freiem Speicherplatz und NTFS-Dateisysteme verfügen:


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



Dieses Beispiel zeigt eine Schemaabfrage mithilfe der WHERE-Klausel.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



Die \_ Klassenmetaklasse identifiziert dies als Schemaabfrage, die Eigenschaft namens \_ \_ this identifiziert die Zielklasse der Abfrage, und der [ISA-Operator](isa-operator-for-schema-queries.md) fordert Definitionen für die Unterklassen der Zielklasse an. Daher gibt die vorherige Abfrage die Definition für die myClassName-Klasse und Definitionen für alle ihre Unterklassen zurück.

Das folgende Beispiel ist eine Datenabfrage, die die [ASSOCIATORS OF-Anweisung](associators-of-statement.md) mit WHERE verwendet:


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



Das nächste Beispiel zeigt eine Schemaabfrage mit ASSOCIATORS OF und WHERE:


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



Das folgende Beispiel ist eine Datenabfrage, die die [REFERENCES OF-Anweisung](references-of-statement.md) und WHERE verwendet:


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



Dieses letzte Beispiel ist eine Schemaabfrage mit REFERENCES OF und WHERE:


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Zusätzlich zum WMI [DATETIME-Format](date-and-time-format.md) unterstützt die WQL WHERE-Klausel verschiedene andere Datums- und Uhrzeitformate:

-   [Von WQL unterstützte Datumsformate](wql-supported-date-formats.md)
-   [Von WQL unterstützte Zeitformate](wql-supported-time-formats.md)

 

 
