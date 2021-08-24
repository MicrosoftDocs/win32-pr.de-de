---
description: Die Schlüsselwörter ALL BITWISE und SOME BITWISE werden zum Testen der Bits in einem integralen Typ verwendet.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: ALL BITWISE und SOME BITWISE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac133e04eae78fe9b943c1e354d9e4dcf451640ad60be1883eecc938ec1d418a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594720"
---
# <a name="all-bitwise-and-some-bitwise"></a>ALL BITWISE und SOME BITWISE

Die **Schlüsselwörter ALL BITWISE** und **SOME BITWISE** werden zum Testen der Bits in einem integralen Typ verwendet. Wenn alle festgelegten Bits in einer Eigenschaft mit der Maske übereinstimmen, **ist ALL BITWISE** true. Wenn mindestens eines der festgelegten Bits in einer Eigenschaft der Maske entspricht, **ist SOME BITWISE** true.

Operatoren können sowohl auf Skalareigenschaften (Einzelwerteigenschaften) als auch auf Vektoreigenschaften (mehrere Werte) angewendet werden. Das folgende Codebeispiel zeigt, wie Eigenschaftswerte mit **ALL BITWISE** und **SOME BITWISE testen.**


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a>Vergleichsoperatoren

Die unterstützten Vergleichsoperatoren für BITWISE-Tests sind in der folgenden Tabelle aufgeführt.



| Vergleichsoperator | BESCHREIBUNG  |
|---------------------|--------------|
| =                   | Gleich     |
| != oder <>      | Ungleich |



 

Die Logik von BITWISE-Tests ist in der folgenden Tabelle aufgeführt.



| BITWISE-Test- und Vergleichsoperator | Logik                   |
|--------------------------------------|-------------------------|
| = ALL BITWISE                        | Property & Mask = Mask  |
| = BITWEISE                       | Property & Mask != 0    |
| <> ALLE BITWEISE                 | Property & Mask != Mask |
| <> BITWEISE                | Property & Mask = 0     |



 

In der folgenden Wahrheitstabelle werden Binär- und Hexadezimalwerte verwendet, um die Logik von BITWISE-Tests zu demonstateieren.



| Eigenschaft in binärer Form (hexadezimal) | Maskieren in binärer Form (hexadezimal) | Property & Mask = binary (hex) | = BITWEISE | = ALL BITWISE |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| 0001 (0x1)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0001 (0x1)               | 0011 (0x3)           | 0001 (0x1)                     | True           | False         |
| 0011 (0x3)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0010 (0x2)               | 0001 (0x1)           | 0000 (0x0)                     | False          | False         |
| 11110000 (0xF0)          | 00000011 (0x03)      | 00000000 (0x00)                | False          | False         |
| 11110010 (0xF2)          | 11110010 (0xF2)      | 11110010 (0xF2)                | True           | True          |
| 11110010 (0xF2)          | 00000011 (0x03)      | 00000010 (0x02)                | True           | False         |



 

## <a name="example"></a>Beispiel

Im Folgenden finden Sie ein Beispiel für das **ALL BITWISE-Prädikat.**


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Volltext-Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-Volltext-Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



