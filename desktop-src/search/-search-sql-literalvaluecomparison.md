---
description: Der Literalwertvergleich verwendet Standardvergleichsoperatoren, um eine einwertige Spalte mit einem Literalwert zu vergleichen.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Literalwertvergleich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1e311c6f98c1114b63a1bf650d6e7be004e1e8e4cf5848b962a7cbf8049bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227175"
---
# <a name="literal-value-comparison"></a>Literalwertvergleich

Der Literalwertvergleich verwendet Standardvergleichsoperatoren, um eine einwertige Spalte mit einem [Literalwert zu](-search-sql-literals.md) vergleichen. Informationen zum Vergleichen mehrwertigen Spalten finden Sie unter [Multi-Valued (ARRAY) Comparisons](-search-sql-multivaluedcomparisons.md).

Das Vergleichs prädikat für Literalwerte hat die folgende Syntax:


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> Die rechte Seite des Vergleichs muss ein Literal sein. Sie können eine Spalte nicht mit einem berechneten Wert vergleichen, und Sie können eine Spalte nicht mit einer anderen Spalte vergleichen.

 

Der Spaltenteil ist eine beliebige gültige Eigenschaftsspalte und kann bei Bedarf in einen anderen Typumsetzungen verwendet werden. Optional können Sie den Spaltennamen zur Lesbarkeit in doppelte Anführungszeichen umschließen, ohne die Funktionalität zu beeinträchtigen. Weitere Informationen finden Sie unter [Umwandlung des Datentyps einer Spalte.](-search-sql-castingdatacolumntype.md)

Das Literal kann ein beliebiges Zeichenfolgen-, numerisches, hexadezimales, boolesches oder Datumsliteral sein, das in einfache Anführungszeichen eingeschlossen ist. Es werden nur genaue Übereinstimmungen erkannt, und Platzhalterzeichen werden ignoriert. Das Literal kann auch in einen anderen Typ cast werden.

## <a name="comparison-operators"></a>Vergleichsoperatoren

In der folgenden Tabelle werden die unterstützten Vergleichsoperatoren beschrieben.



| Vergleichsoperator | BESCHREIBUNG              |
|---------------------|--------------------------|
| =                   | Gleich                 |
| != oder <>      | Ungleich             |
| >                | Größer als             |
| >=               | Größer als oder gleich |
| <                | Kleiner als                |
| <=               | Kleiner als oder gleich    |



 

 

In Verbindung mit dem Operator "=" unterstützt Windows Search strukturierte Abfragesprache (SQL) die Verwendung der Schlüsselwörter BEFORE und AFTER, die angeben, ob die Abfrage Spaltenwerte vor oder nach einem angegebenen Wert in der Wörterbuchsortierreihenfolge vergleichen soll.


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a>Beispiele

Im Folgenden finden Sie Beispiele für das Literalwertvergleichs-Prädikat.


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[LIKE-Prädikat](-search-sql-like.md)
</dt> <dt>

[DATEADD-Funktion](-search-sql-dateadd.md)
</dt> <dt>

[Mehrwertige Vergleiche (ARRAY)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[NULL-Prädikat](-search-sql-null.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Volltext-Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-Volltext-Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



