---
description: Der Literalwertvergleich verwendet Standardvergleichsoperatoren, um eine einwertige Spalte mit einem Literalwert abzugleichen.
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

Der Literalwertvergleich verwendet Standardvergleichsoperatoren, um eine einwertige Spalte mit einem [Literalwert](-search-sql-literals.md) abzugleichen. Informationen zum Vergleichen mehrwertiger Spalten finden Sie unter [Arrayvergleiche mit mehreren Werten.](-search-sql-multivaluedcomparisons.md)

Das Literalwertvergleichsprädikat weist die folgende Syntax auf:


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> Die rechte Seite des Vergleichs muss ein Literal sein. Sie können eine Spalte nicht mit einem berechneten Wert vergleichen, und Sie können eine Spalte nicht mit einer anderen Spalte vergleichen.

 

Der Spaltenteil ist eine beliebige gültige Eigenschaftenspalte und kann bei Bedarf in einen anderen Typ typisiert werden. Optional können Sie den Spaltennamen aus Gründen der Lesbarkeit in doppelte Anführungszeichen einschließen, ohne die Funktionalität zu beeinträchtigen. Weitere Informationen finden Sie unter [Umwandeln des Datentyps einer Spalte.](-search-sql-castingdatacolumntype.md)

Das Literal kann ein beliebiges Zeichenfolgenliteral, numerisches, hexadezimales, boolesches oder Datumsliteral sein, das in einfache Anführungszeichen eingeschlossen ist. Es werden nur genaue Übereinstimmungen erkannt, und Platzhalterzeichen werden ignoriert. Das Literal kann auch in einen anderen Typ typisiert werden.

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



 

 

In Verbindung mit dem Operator "=" unterstützt Windows Search strukturierte Abfragesprache (SQL) die Verwendung der Schlüsselwörter BEFORE und AFTER, die angeben, ob die Abfrage Spaltenwerte vor oder nach einem angegebenen Wert in der Sortierreihenfolge des Wörterbuchs vergleichen soll.


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a>Beispiele

Im Folgenden sind Beispiele für das Vergleichsprädikat für Literalwerte aufgeführt.


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

[Volltextprädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-Volltextprädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



