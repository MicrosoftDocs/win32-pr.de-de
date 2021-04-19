---
description: Der literale Wert Vergleich verwendet Standard Vergleichs Operatoren, um eine einwertige Spalte mit einem Literalwert zu vergleichen.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Vergleich von literalen Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346909"
---
# <a name="literal-value-comparison"></a>Vergleich von literalen Werten

Der literale Wert Vergleich verwendet Standard Vergleichs Operatoren, um eine einwertige Spalte mit einem [Literalwert](-search-sql-literals.md) zu vergleichen. Weitere Informationen zum Vergleichen von mehrwertigen Spalten finden Sie unter [Vergleiche mit mehreren Werten (Array)](-search-sql-multivaluedcomparisons.md).

Das Vergleichs Prädikat literale Wert weist die folgende Syntax auf:


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> Die Rechte Seite des Vergleichs muss ein Literalwert sein. Es ist nicht möglich, eine Spalte mit einem berechneten Wert zu vergleichen, und Sie können eine Spalte nicht mit einer anderen Spalte vergleichen.

 

Der Spalten Teil ist eine beliebige gültige Eigenschafts Spalte und kann ggf. in einen anderen Typ umgewandelt werden. Optional können Sie den Spaltennamen für die Lesbarkeit in doppelte Anführungszeichen einschließen, ohne dass sich dies auf die Funktionalität auswirkt. Weitere Informationen finden Sie unter umwandeln [des Datentyps einer Spalte](-search-sql-castingdatacolumntype.md).

Das Literale kann eine beliebige Zeichenfolge, ein numerisches, ein hexadezimal, ein boolescher Wert oder ein Datumsliteral in einfachen Anführungszeichen sein Nur genaue Übereinstimmungen werden erkannt, und Platzhalter Zeichen werden ignoriert. Das Literale kann auch in einen anderen Typ umgewandelt werden.

## <a name="comparison-operators"></a>Vergleichsoperatoren

In der folgenden Tabelle werden die unterstützten Vergleichs Operatoren beschrieben.



| Vergleichsoperator | BESCHREIBUNG              |
|---------------------|--------------------------|
| =                   | Gleich                 |
| ! = oder <>      | Ungleich             |
| >                | Größer als             |
| >=               | Größer als oder gleich |
| <                | Kleiner als                |
| <=               | Kleiner als oder gleich    |



 

 

In Verbindung mit dem Operator "=" unterstützt Windows Search Structured Query Language (SQL) die Verwendung der Schlüsselwörter "Before" und "After", die angeben, ob die Abfrage Spaltenwerte vor oder nach einem angegebenen Wert in der Wörterbuch Sortierung vergleichen soll.


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a>Beispiele

Im folgenden finden Sie Beispiele für das Vergleichs Prädikat Literalwert.


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

[DateAdd-Funktion](-search-sql-dateadd.md)
</dt> <dt>

[Mehrwertige Vergleiche (Array)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[NULL-Prädikat](-search-sql-null.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-voll Text Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



