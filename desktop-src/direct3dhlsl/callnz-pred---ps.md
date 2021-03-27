---
title: callnz pred-PS
description: Ruft mit einem Prädikat auf, wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist. Das-Prädikat verwendet einen booleschen Wert, um zu bestimmen, ob die Anweisung nicht durchgeführt werden soll.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948317"
---
# <a name="callnz-pred---ps"></a>callnz pred-PS

Ruft mit einem Prädikat auf, wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist. Das-Prädikat verwendet einen booleschen Wert, um zu bestimmen, ob die Anweisung nicht durchgeführt werden soll.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] P0. Stuben|Teenie|z|Löw |
|----------------------------------|



 

Hierbei gilt:

-   dabei \# ist l eine [Bezeichnung-PS](label---ps.md) , die den Anfang der aufzurufenden Unterroutine kennzeichnet.
-   \[!\] ist ein optionaler Negation-Modifizierer.
-   P0 ist das Prädikat Register. Siehe [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} ist das erforderliche Replizieren von Replizieren auf p0.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz-präd           |      |      |      |      |      | x    | x     | x    | x     |



 

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

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




