---
description: Das LIKE-Prädikat führt einen Muster vergleichsvergleich für die angegebene Spalte aus.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: LIKE-Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340162"
---
# <a name="like-predicate"></a>LIKE-Prädikat

Das LIKE-Prädikat führt einen Muster vergleichsvergleich für die angegebene Spalte aus. Es verwendet die folgende Syntax:


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<column>Kann ein regulärer oder Begrenzungs [Bezeichner](-search-sql-identifiers.md)sein. Die-Spalte ist auf die Eigenschaften im Eigenschaften Speicher beschränkt.

Der <Platzhalter \_ Literal> ist ein Zeichenfolgenliteral Er ist in Anführungszeichen eingeschlossen und kann optional Platzhalter Zeichen enthalten. Die Match-Zeichenfolge kann bei Bedarf mehrere Platzhalter Zeichen enthalten. In der folgenden Tabelle werden die Platzhalter Zeichen beschrieben, die vom LIKE-Prädikat erkannt werden.



| Platzhalter                | BESCHREIBUNG                                                                                                                                                                                     | Beispiel                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| % (Prozent)             | Entspricht 0 (null) oder mehr Zeichen.                                                                                                                                                         | "Comp% r" entspricht "Comp", gefolgt von NULL oder mehr Zeichen, die auf eine r enden.                                                                                                                                  |
| \_ (Unterstrich)         | Entspricht einem beliebigen einzelnen Zeichen.                                                                                                                                                                   | "Comp \_ ter" entspricht "Comp", gefolgt von genau einem beliebigen Zeichen, gefolgt von "ter".                                                                                                                              |
| \[\](eckige Klammern) | Entspricht einem beliebigen einzelnen Zeichen innerhalb des angegebenen Bereichs oder der angegebenen Menge. Beispielsweise \[ gibt a-z \] einen Bereich an. \[ AEIOU \] gibt den Satz von Vokalen an.                                                  | "Comp \[ a-z \] re" entspricht "Comp", gefolgt von einem einzelnen Zeichen im Bereich von a bis z, gefolgt von "be". "Comp \[ Ao \] " entspricht "Comp", gefolgt von einem einzelnen Zeichen, das entweder ein oder ein o sein muss.<br/> |
| \[^ \] Einfügemarke          | Entspricht einem beliebigen einzelnen Zeichen, das nicht innerhalb des angegebenen Bereichs oder Satzes liegt. Beispielsweise \[ gibt ^ a-z \] einen Bereich an, der a bis z ausschließt. \[ ^ AEIOU \] gibt eine Menge an, die Vokale ausschließt. | "Comp \[ ^ u \] " entspricht "Comp", gefolgt von einem einzelnen Zeichen, das kein u ist.                                                                                                                                        |



 

Wenn Sie Prädikate mit mehreren Bereichen erstellen, müssen die Bereiche in der richtigen Reihenfolge vorliegen.

> [!Note]  
> Um die Platzhalter Zeichen als Literalzeichen für den Abgleich und nicht als Platzhalter Zeichen abzugleichen, platzieren Sie das Zeichen in eckigen Klammern. Verwenden Sie z. b. "", um das Prozentzeichen abzugleichen. \[ % \]

 

## <a name="examples"></a>Beispiele


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Vergleich von literalen Werten](-search-sql-literalvaluecomparison.md)
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

 

 




