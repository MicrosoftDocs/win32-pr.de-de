---
title: callnz pred - ps
description: Rufen Sie mit einem Prädikat auf, wenn dies nicht 0 (null) ist. Führt einen bedingten Aufruf der Vom Bezeichnungsindex markierten Anweisung aus. Prädication verwendet einen booleschen Wert, um zu bestimmen, ob von die Anweisung nicht ausführen soll.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f56699a4853b7012401529ecfad6fbfb0006e21990a99a2fe5631faebd57674d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983290"
---
# <a name="callnz-pred---ps"></a>callnz pred - ps

Rufen Sie mit einem Prädikat auf, wenn dies nicht 0 (null) ist. Führt einen bedingten Aufruf der Vom Bezeichnungsindex markierten Anweisung aus. Prädication verwendet einen booleschen Wert, um zu bestimmen, ob von die Anweisung nicht ausführen soll.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] p0. {x\|y\|z\|w} |
|----------------------------------|



 

Hierbei gilt:

-   Wobei l \# eine Bezeichnung ist – [ps](label---ps.md) markiert den Anfang der auf zu aufgerufenen Unterroutine.
-   \[!\] ist ein optionaler Negatmodifizierer.
-   p0 ist das Prädikatregister. Weitere Informationen [finden Sie unter Prädikatregister.](dx9-graphics-reference-asm-ps-registers-predicate.md)
-   {x \| y \| z \| w} ist die erforderliche Replikation von Swizzle auf p0.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz pred           |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung führt Folgendes aus:


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




