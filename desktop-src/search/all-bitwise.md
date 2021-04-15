---
description: Alle bitweisen und einige bitweise Schlüsselwörter werden zum Testen der Bits in einem ganzzahligen Typ verwendet.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: Alle bitweisen und einige bitweise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709db4829f5b620bcb14e0b4261fac7e7d9a6f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525472"
---
# <a name="all-bitwise-and-some-bitwise"></a>Alle bitweisen und einige bitweise

**Alle bitweisen** und **einige bitweise** Schlüsselwörter werden zum Testen der Bits in einem ganzzahligen Typ verwendet. Wenn alle Satz Bits in einer Eigenschaft mit der Maske identisch sind, ist **all bitweise** true. Wenn mindestens eines der Satz Bits in einer Eigenschaft mit der Maske übereinstimmt, ist **bitweise** true.

Operatoren können sowohl auf skalare Eigenschaften (Einzelwert Eigenschaften) als auch auf Vektor Eigenschaften (mehrfach Wert) angewendet werden. Im folgenden Codebeispiel wird gezeigt, wie Eigenschaftswerte mit **allen bitweisen** und **einigen bitweisen** getestet werden.


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a>Vergleichsoperatoren

Die unterstützten Vergleichs Operatoren für bitweise Tests sind in der folgenden Tabelle aufgeführt.



| Vergleichsoperator | BESCHREIBUNG  |
|---------------------|--------------|
| =                   | Gleich     |
| ! = oder <>      | Ungleich |



 

Die Logik von bitweisen Tests ist in der folgenden Tabelle aufgeführt.



| Bitweiser Test-und Vergleichs Operator | Logik                   |
|--------------------------------------|-------------------------|
| = alle bitweisen                        | Property & mask = mask  |
| = Einige bitweise                       | Eigenschaft & Maske! = 0    |
| <> alle bitweisen                 | Property & mask! = mask |
| <> einige bitweise                | Property & mask = 0     |



 

In der folgenden Wahrheitstabelle werden binäre und hexadezimale Werte verwendet, um die Logik von bitweisen Tests zu verteueren.



| Eigenschaft in binary (Hex) | Mask in binary (Hex) | Property & Mask = Binary (Hex) | = Einige bitweise | = alle bitweisen |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| 0001 (0x1)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0001 (0x1)               | 0011 (0x3)           | 0001 (0x1)                     | Richtig           | False         |
| 0011 (0x3)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0010 (0x2)               | 0001 (0x1)           | 0000 (0x0)                     | False          | False         |
| 11110000 (0xF)          | 00000011 (0x03)      | 00000000 (0x00)                | False          | False         |
| 11110010 (0xF 2)          | 11110010 (0xF 2)      | 11110010 (0xF 2)                | True           | True          |
| 11110010 (0xF 2)          | 00000011 (0x03)      | 00000010 (0x02)                | Richtig           | False         |



 

## <a name="example"></a>Beispiel

Im folgenden finden Sie ein Beispiel für das **bitweise all** -Prädikat.


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-voll Text Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



