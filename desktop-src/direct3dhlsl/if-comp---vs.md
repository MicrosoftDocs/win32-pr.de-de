---
title: if_comp im Vergleich zu
description: Starten Sie eine if bool - vs... else – vs... endif – vs block, mit einer Bedingung, die auf Werten basiert, die in einem Shader berechnet werden können. Diese Anweisung wird verwendet, um einen Codeblock basierend auf einer Bedingung zu überspringen.
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11c7abceb9b484c4cd104e136c47edeb55b93b5273f953cb6d98052e247513d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743580"
---
# <a name="if_comp---vs"></a>if \_ comp - vs

Starten Sie eine [if bool - vs](if-bool---vs.md)... [else – vs](else---vs.md)... [endif – vs](endif---vs.md) block, mit einer Bedingung, die auf Werten basiert, die in einem Shader berechnet werden können. Diese Anweisung wird verwendet, um einen Codeblock basierend auf einer Bedingung zu überspringen.

## <a name="syntax"></a>Syntax



| if \_ comp src0, src1 |
|---------------------|



 

Hierbei gilt:

-   \_comp ist ein Vergleich zwischen den beiden Quellregistern. Folgende Werte sind möglich: 

    | Syntax | Vergleich            |
    |--------|-----------------------|
    | \_Gt   | Größer als          |
    | \_Lt   | Kleiner als             |
    | \_Ge   | Größer als oder gleich |
    | \_Le   | Kleiner oder gleich    |
    | \_Eq   | Gleich              |
    | \_Ne   | Ungleich          |

    

     

-   src0 ist ein Quellregister. Replizieren von Swizzle ist erforderlich, um eine Komponente auszuwählen.
-   src1 ist ein Quellregister. Replizieren von Swizzle ist erforderlich, um eine Komponente auszuwählen.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| if \_ comp               |      |      | x    | x     | x    | x     |



 

Diese Anweisung wird verwendet, um einen Codeblock basierend auf einer Bedingung zu überspringen.


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



Seien Sie vorsichtig, wenn Sie die Vergleichsmodi equals und not equals für Gleitkommazahlen verwenden. Da das Runden während gleitkommaberechnungen erfolgt, kann der Vergleich mit einem Epsilonwert (kleine Zahl ungleich 0) durchgeführt werden, um Fehler zu vermeiden.

Es gelten folgende Beschränkungen:

-   if \_ comp... [else – vs](else---vs.md)... [endif – im Vergleich](endif---vs.md) zu Blöcken (zusammen mit den prädikatierten if-Blöcken) können bis zu 24 Ebenen tief geschachtelt werden.
-   src0- und src1-Register erfordern eine Replizieren von Swizzle.
-   , wenn \_ comp-Blöcke mit einer [else-Anweisung](else---vs.md) enden müssen ( vs oder [endif - vs](endif---vs.md) instruction).
-   if \_ comp... [else – vs](else---vs.md)... [endif: im Vergleich](endif---vs.md) zu -Blöcken kann kein Schleifenblock durchlaufen werden. Der if \_ comp-Block muss sich vollständig innerhalb oder außerhalb der [Schleife](loop---vs.md) befinden – im Vergleich zum -Block.

## <a name="example"></a>Beispiel

Diese Anweisung stellt eine bedingte dynamische Flusssteuerung bereit.


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




