---
title: callnz pred – vs
description: Rufen Sie auf, wenn nicht 0 (null) mit einem Prädikat. Führt einen bedingten Aufruf der Vom Bezeichnungsindex markierten Anweisung aus. Prädication verwendet einen booleschen Wert, um zu bestimmen, ob von die Anweisung nicht ausführen soll.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1449ed9fb061ea2d5a83d37cb7c0d744a4c7e8b6517d49c0d2e32a10f7f5ed9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287024"
---
# <a name="callnz-pred---vs"></a>callnz pred – vs

Rufen Sie auf, wenn nicht 0 (null) mit einem Prädikat. Führt einen bedingten Aufruf der Vom Bezeichnungsindex markierten Anweisung aus. Prädication verwendet einen booleschen Wert, um zu bestimmen, ob von die Anweisung nicht ausführen soll.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] p0. {x\|y\|z\|w} |
|----------------------------------|



 

Dabei gilt:

-   l \# ist eine Bezeichnung , im Gegensatz [zum](label---vs.md) Markieren des Anfangs der aufgerufenen Unterroutine.
-   \[!\] ist ein optionaler Negatmodifizierer.
-   p0 ist das [Prädikatregister.](dx9-graphics-reference-asm-vs-registers-predicate.md)
-   {x \| y \| z \| w} ist die erforderliche Replikation von Swizzle auf p0.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| callnz pred            |      |      | x    | x     | x    | x     |



 

Diese Anweisung führt Folgendes aus:


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



Diese Anweisung verwendet einen Vertex-Shaderanweisungsslot.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




