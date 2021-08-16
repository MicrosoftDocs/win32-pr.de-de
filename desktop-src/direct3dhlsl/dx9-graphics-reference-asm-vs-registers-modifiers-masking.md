---
title: Zielregistermaskierung
description: Die Maskierung gibt an, welche Komponenten des Zielregisters mit dem Ergebnis einer Anweisung aktualisiert werden. Texturregister verfügen über einen Satz von Regeln, und Nichttexturregister verfügen über einen anderen Satz von Regeln.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a8d45e847f7da785bd09b83e778d140cee68007add882066b508b38043550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119684"
---
# <a name="destination-register-masking"></a>Zielregistermaskierung

Die Maskierung gibt an, welche Komponenten des Zielregisters mit dem Ergebnis einer Anweisung aktualisiert werden. Texturregister verfügen über einen Satz von Regeln, und Nichttexturregister verfügen über einen anderen Satz von Regeln.

-   dx9 \_ graphics \_ reference \_ asm vs \_ \_ registers \_ modifizierer \_ maskierung: Dieser Abschnitt enthält Regeln zum Anwenden von Masken auf Zielregister.
-   \_ \_ Texturregistermasken: Texturregister verfügen über einige eindeutige Regeln.

## <a name="destination-register-masking"></a>Zielregistermaskierung

Wie in der folgenden Tabelle gezeigt, kann die Maskierung (wobei einer der gültigen [Vertex-Shader-Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)ist) auf die einzelnen Komponenten der Vektordaten angewendet werden.



| Komponentenmodifizierer | Beschreibung      |
|--------------------|------------------|
| r.{x}{y}{z}{w}     | Zielmaske |



 

-   Im Allgemeinen ist die Angabe von Zielregister-Schreibmasken ein guter Codierungsstil. Dies erleichtert das Lesen und Verwalten von Code.
-   Eine beliebige Kombination von Komponenten kann (einschließlich keiner) angegeben werden, solange x vor y, y vor z und z vor w.
-   Die oPts- und oFog-Ausgaberegister dürfen nur eine Maske verwenden.
-   Bestimmte Anweisungen erfordern, dass das Zielregister eine einzelne Schreibmaske verwendet: exp, expp, log, logp, pow, rcp und rsq.
-   In Version 1.0 erforderte die frc-Anweisung eine der folgenden Maskenkombinationen: .x oder .y oder .xy. Für Version 2.0 gelten keine Maskeneinschränkungen.
-   sincos erfordert eine der folgenden Maskenkombinationen: .x oder .y oder .xyz.
-   m3x2 erfordert die XY-Schreibmaske.
-   m3x3 und m4x3 erfordern die Schreibmaske .xyz.
-   m3x4 und m4x4 erfordern entweder die Schreibmaske .xyz oder die Standardschreibmaske (xyzw).

## <a name="texture-register-masks"></a>Texturregistermasken

Die Validierungsregeln für die Verwendung von Modifizierern für Texturkoordinatenregister sind enger als die Validierungsregeln für andere Register.

-   Wenn oTn geschrieben wird, müssen auch alle vorherigen Register (oTn-1 ~ oT0) geschrieben werden.
-   Die "kombinierte" Schreibmaske für ein beliebiges \# oT-Register muss genau eine der folgenden Sein:
    -   .x
    -   .xy
    -   .xyz
    -   .xyzw (entspricht nicht der Verwendung von Komponentenmodifizierern)

Beispielsweise kann ein Vertex-Shader in separaten Anweisungen an Texturregister ausgegeben werden.


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



Alternativ können die Anweisungen kombiniert werden.


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



Diese Einschränkungen gelten nur für die Texturkoordinatenregister.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Registermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




