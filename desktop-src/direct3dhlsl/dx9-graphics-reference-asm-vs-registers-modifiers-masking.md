---
title: Ziel Register Maskierung
description: Die Maskierung gibt an, welche Komponenten des Ziel Registers mit dem Ergebnis einer Anweisung aktualisiert werden. Textur Register verfügen über einen Regelsatz, und nicht Textur Register verfügen über einen anderen Satz von Regeln.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388520"
---
# <a name="destination-register-masking"></a>Ziel Register Maskierung

Die Maskierung gibt an, welche Komponenten des Ziel Registers mit dem Ergebnis einer Anweisung aktualisiert werden. Textur Register verfügen über einen Regelsatz, und nicht Textur Register verfügen über einen anderen Satz von Regeln.

-   DX9 \_ Graphics \_ Reference \_ ASM \_ vs \_ registriert \_ \_ modifizierermaskierung: Dieser Abschnitt enthält Regeln zum Anwenden von Masken auf Ziel Register.
-   Textur \_ Register \_ Masken: Textur Register verfügen über einige eindeutige Regeln.

## <a name="destination-register-masking"></a>Ziel Register Maskierung

Wie in der folgenden Tabelle gezeigt, kann die Maskierung (wobei eine der gültigen Vertex-Shader- [Register für Vertex-Shader](dx9-graphics-reference-asm-vs-registers.md)ist) auf die einzelnen Komponenten der Vektordaten angewendet werden.



| Komponentenmodifizierer | BESCHREIBUNG      |
|--------------------|------------------|
| r. {x} {y} {z} {w}     | Ziel Maske |



 

-   Im Allgemeinen ist die Angabe von Schreib Masken für die Ziel Registrierung ein guter Codierungsstil. Dadurch wird der Code einfacher zu lesen und zu warten.
-   Eine beliebige Kombination von Komponenten kann angegeben werden (einschließlich "None"), solange "x" vor "y", "y" vor "z" und "z" vorangeht.
-   Die OPTS-und ofog-Ausgabe Register dürfen nur eine Maske verwenden.
-   Bestimmte Anweisungen erfordern, dass das Ziel Register eine einzelne Schreib Maske verwendet: Exp, EXPP, Log, LogP, Pow, rcp und RSQ.
-   In Version 1,0 erforderte die FRC-Anweisung eine der folgenden Masken Kombinationen:. x oder. y oder. XY. Version 2,0 hat keine Masken Einschränkung.
-   SinCos erfordert eine der folgenden Masken Kombinationen:. x,. y oder. xyz.
-   m3x2 erfordert die. XY-Schreib Maske.
-   M3x3 und m4x3 erfordern die Schreib Maske ". xyz".
-   M3x4 und M4x4 erfordern entweder die. XYZ-Schreib Maske oder die Standard Schreib Maske (xyzw).

## <a name="texture-register-masks"></a>Textur Register Masken

Die Validierungsregeln für die Verwendung von modifiziererregistern für Texturkoordinaten Register sind enger als die Validierungsregeln für andere Register.

-   Wenn OTN geschrieben ist, müssen auch alle vorherigen Register (OTN-1 ~ oT0) geschrieben werden.
-   Die "kombinierte" Schreib Maske für alle oT- \# Register muss genau eines der folgenden sein:
    -   .x
    -   . XY
    -   . XYZ
    -   . xyzw (entspricht nicht der Verwendung von komponentenmodifizierersätzen)

Beispielsweise kann ein Vertex-Shader in separaten Anweisungen an Textur Register ausgeben.


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



Oder die Anweisungen können kombiniert werden.


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



Diese Einschränkungen gelten nur für die Texturkoordinaten Register.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-registermodifiziererer](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




