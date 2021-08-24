---
title: if_comp ps
description: Starten Sie eine if bool - ps... else - ps... endif – ps block, mit einer Bedingung, die auf Werten basiert, die in einem Shader berechnet werden können. Diese Anweisung wird verwendet, um einen Codeblock basierend auf einer Bedingung zu überspringen.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5d0a2271dbd67902a039ddadf585611ed98fdb115f468c3962baa8cb46f48508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788970"
---
# <a name="if_comp---ps"></a>if \_ comp - ps

Starten Sie einen [, wenn bool – ps](if-bool---ps.md)... [else – ps](else---ps.md)... [endif – ps](endif---ps.md) block, mit einer Bedingung, die auf Werten basiert, die in einem Shader berechnet werden können. Diese Anweisung wird verwendet, um einen Codeblock basierend auf einer Bedingung zu überspringen.

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



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| if \_ comp              |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung wird verwendet, um einen Codeblock basierend auf einer Bedingung zu überspringen.


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



Seien Sie vorsichtig, wenn Sie die Vergleichsmodi equals und not equals für Gleitkommazahlen verwenden. Da das Runden während gleitkommaberechnungen erfolgt, kann der Vergleich mit einem Epsilonwert (kleine Zahl ungleich 0) durchgeführt werden, um Fehler zu vermeiden.

Es gelten folgende Beschränkungen:

-   if \_ comp... [else – ps](else---ps.md)... [endif: PS-Blöcke](endif---ps.md) (zusammen mit den prädikatierten if-Blöcken) können bis zu 24 Ebenen tief geschachtelt werden. [](if-bool---ps.md)
-   src0- und src1-Register erfordern eine Replizieren von Swizzle.
-   , wenn \_ comp-Blöcke mit einer [else-Anweisung](else---vs.md) enden müssen ( vs oder [endif - vs](endif---vs.md) instruction).
-   if \_ comp... [else – ps](else---ps.md)... [endif:](endif---ps.md) PS-Blöcke können sich nicht über einen Schleifenblock erstreckt. Der if \_ comp-Block muss sich vollständig innerhalb oder außerhalb des Schleifenblocks befinden.

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

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




