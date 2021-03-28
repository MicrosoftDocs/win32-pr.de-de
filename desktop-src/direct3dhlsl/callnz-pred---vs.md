---
title: callnz pred-vs
description: Mit einem Prädikat wird aufgerufen, wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist. Das-Prädikat verwendet einen booleschen Wert, um zu bestimmen, ob die Anweisung nicht durchgeführt werden soll.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038332"
---
# <a name="callnz-pred---vs"></a>callnz pred-vs

Mit einem Prädikat wird aufgerufen, wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist. Das-Prädikat verwendet einen booleschen Wert, um zu bestimmen, ob die Anweisung nicht durchgeführt werden soll.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] P0. Stuben|Teenie|z|Löw |
|----------------------------------|



 

Dabei gilt:

-   l \# ist eine [Bezeichnung-vs](label---vs.md) , die den Anfang der aufzurufenden Unterroutine markiert.
-   \[!\] ist ein optionaler Negation-Modifizierer.
-   P0 ist das [Prädikat Register](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} ist das erforderliche Replizieren von Replizieren auf p0.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| callnz-präd            |      |      | x    | x     | x    | x     |



 

Diese Anweisung führt Folgendes aus:


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



Diese Anweisung verwendet einen Vertex-Shader-Anweisungs Slot.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




