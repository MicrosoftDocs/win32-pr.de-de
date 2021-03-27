---
title: if_comp-PS
description: Startet, wenn bool-PS... Else-PS... der enumerationsblock "enumdif-PS" mit einer Bedingung, die auf Werten basiert, die in einem Shader berechnet werden können. Diese Anweisung wird verwendet, um einen Codeblock auf der Grundlage einer Bedingung zu überspringen.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719350"
---
# <a name="if_comp---ps"></a>Wenn \_ Comp-PS

Startet, [Wenn bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... der [enumerationsblock "enumdif-PS](endif---ps.md) " mit einer Bedingung, die auf Werten basiert, die in einem Shader berechnet werden können. Diese Anweisung wird verwendet, um einen Codeblock auf der Grundlage einer Bedingung zu überspringen.

## <a name="syntax"></a>Syntax



| If \_ Comp src0, Quelle1 |
|---------------------|



 

Hierbei gilt:

-   \_comp ist ein Vergleich zwischen den beiden Quell Registern. Folgende Werte sind möglich: 

    | Syntax | Vergleich            |
    |--------|-----------------------|
    | \_siegt   | Größer als          |
    | \_General   | Kleiner als             |
    | \_Färbung   | Größer als oder gleich |
    | \_Kirchturm   | Kleiner als oder gleich    |
    | \_stecken   | Gleich              |
    | \_NES   | Ungleich          |

    

     

-   src0 ist ein Quell Register. Das Replizieren der Replizierung ist erforderlich, um eine Komponente auszuwählen.
-   Quelle1 ist ein Quell Register. Das Replizieren der Replizierung ist erforderlich, um eine Komponente auszuwählen.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| If \_ comp              |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung wird verwendet, um einen Codeblock auf der Grundlage einer Bedingung zu überspringen.


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



Achten Sie darauf, die Vergleichs Modi "gleich" und "nicht gleich" für Gleit Komma Zahlen zu verwenden. Da während der Ausführung von Gleit Komma Berechnungen eine Rundung stattfindet, kann der Vergleich mit einem Epsilon-Wert (kleine Zahl ungleich null) durchgeführt werden, um Fehler zu vermeiden.

Es gelten folgende Beschränkungen:

-   Wenn \_ comp... [else-PS](else---ps.md)... [EndIf-PS-](endif---ps.md) Blöcke (zusammen mit den Prädikat- [if](if-bool---ps.md) -Blöcken) können bis zu 24 Ebenen tief verschachtelt werden.
-   src0-und Quelle1-Register erfordern ein replizieren.
-   , wenn \_ Comp-Blöcke mit einer [else-vs-](else---vs.md) oder [EndIf-vs-](endif---vs.md) Anweisung enden müssen.
-   Wenn \_ comp... [else-PS](else---ps.md)... " [umdif-PS"-](endif---ps.md) Blöcke können einen Schleifen Block nicht durchlaufen. Der if \_ Comp-Block muss sich vollständig innerhalb oder außerhalb des Schleifen Blocks befinden.

## <a name="example"></a>Beispiel

Diese Anweisung stellt die bedingte dynamische Fluss Steuerung bereit.


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




