---
description: Verwenden Sie die WHERE-Klausel, um den Bereich einer Daten-, Ereignis- oder Schemaabfrage zu engen.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: WHERE-Klausel (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0587bffb1a10c4611773de8a61fdb7ac1576952
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386720"
---
# <a name="where-clause-wmi"></a>WHERE-Klausel (WMI)

Verwenden Sie die WHERE-Klausel, um den Bereich einer Daten-, Ereignis- oder Schemaabfrage zu engen. Weitere Informationen finden Sie unter [Abfragen mit WQL.](querying-with-wql.md) Die WHERE-Klausel besteht aus einer Eigenschaft oder einem Schlüsselwort, einem Operator und einer Konstante. Alle WHERE-Klauseln müssen einen der vordefinierten Operatoren angeben, die in der Windows-Verwaltungsinstrumentation (WMI) Query Language (WQL) enthalten sind. Sie können die WHERE-Klausel mit einer der folgenden Formen an die SELECT-Anweisung anfügen:


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



Wobei das abgefragte Element ist, ist class die Klasse, in der abgefragt werden soll, und constant, operator und property sind die Konstante, der Operator und die Eigenschaft oder das Schlüsselwort, die \* verwendet werden sollen. Weitere Informationen zur SELECT-Anweisung finden Sie unter [SELECT-Anweisung](select-statement-for-data-queries.md)für Datenabfragen, [SELECT-Anweisung](select-statement-for-event-queries.md)für Ereignisabfragen oder [SELECT-Anweisung für Schemaabfragen.](select-statement-for-schema-queries.md)

Der Wert der Konstante muss den richtigen Typ für die Eigenschaft haben. Darüber hinaus muss der -Operator in der Liste der gültigen [WQL-Operatoren enthalten sein.](wql-operators.md) Entweder ein Eigenschaftenname oder eine Konstante muss auf beiden Seiten des Operators in der WHERE-Klausel angezeigt werden.

Sie können Zeichenfolgenliterale wie "NTFS" in einer WHERE-Klausel verwenden. Wenn Sie die folgenden Sonderzeichen in die Zeichenfolge eingeben möchten, müssen Sie das Zeichen zunächst mit Escapezeichen verketten, indem Sie dem Zeichen einen zurückgestellten Schrägstrich ( ) voran \\ stellen:

-   schräger Schrägstrich ( \\ \\ )
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



Bei den meisten Verwendungen von Klassendeskriptoren in einer WHERE-Klausel kennzeichnet WMI die Abfrage als ungültig und gibt einen Fehler zurück. Verwenden Sie jedoch den Punktoperator (.) für Eigenschaften vom Typ **Objekt** in WMI. Die folgende Abfrage ist beispielsweise gültig, wenn Prop eine gültige Eigenschaft von MyClass und ein Typobjekt **ist:**

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

Bei Vergleichstests wird die Groß-/Kleinschreibung immer nicht beachtet. Das heißt, die folgenden drei Anweisungen werden alle als **TRUE ausgewertet:**


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



Sie können eine Abfrage erstellen, die boolesche Datentypen enthält, aber die einzigen gültigen booleschen Operandentypen sind die Typen =, != und <> . Der Wert **TRUE** entspricht der Zahl 1, und der Wert **FALSE** entspricht der Zahl 0. Die folgenden Beispiele sind Abfragen, die einen booleschen Wert mit den Werten **TRUE** oder **FALSE vergleichen.**


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



Mehrere Gruppen von Eigenschaften, Operatoren und Konstanten können in einer WHERE-Klausel mithilfe logischer Operatoren und klammerischer Teilausdrucke kombiniert werden. Jede Gruppe muss mit den Operatoren AND, OR oder [NOT](wql-operators.md) verbunden werden, wie in den folgenden Abfragen gezeigt. Die erste Abfrage ruft alle Instanzen der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) ab, bei der die **Name-Eigenschaft** entweder auf C oder D festgelegt ist:


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



Die zweite Abfrage ruft Datenträger mit den Namen "C:" oder "D:" nur dann ab, wenn sie über eine bestimmte Menge an freiem Speicherplatz und NTFS-Dateisystemen verfügen:


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



Dieses Beispiel zeigt eine Schemaabfrage mithilfe der WHERE-Klausel.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



Die Klassenmetaklasse identifiziert dies als Schemaabfrage, die Eigenschaft namens this identifiziert die Zielklasse der Abfrage, und der ISA-Operator fordert Definitionen für die Unterklassen der \_ \_ \_ Zielklasse an. [](isa-operator-for-schema-queries.md) Daher gibt die vorherige Abfrage die Definition für die myClassName-Klasse und Definitionen für alle ihre Unterklassen zurück.

Das folgende Beispiel ist eine Datenabfrage, die die [ASSOCIATORS OF-Anweisung mit](associators-of-statement.md) WHERE verwendet:


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



Das nächste Beispiel zeigt eine Schemaabfrage mit ASSOCIATORS OF und WHERE:


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



Das folgende Beispiel ist eine Datenabfrage, die die [REFERENCES OF-Anweisung und](references-of-statement.md) WHERE verwendet:


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



Das letzte Beispiel ist eine Schemaabfrage mit REFERENCES OF und WHERE:


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Zusätzlich zum WMI [DATETIME-Format](date-and-time-format.md) unterstützt die WQL WHERE-Klausel mehrere andere Datums- und Uhrzeitformate:

-   [Von WQL unterstützte Datumsformate](wql-supported-date-formats.md)
-   [Von WQL unterstützte Zeitformate](wql-supported-time-formats.md)

 

 
