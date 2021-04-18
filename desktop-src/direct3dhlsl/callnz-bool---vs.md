---
title: callnz bool-vs
description: Wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist. | callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995763"
---
# <a name="callnz-bool---vs"></a>callnz bool-vs

Wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] b\# |
|----------------------|



 

Dabei gilt:

-   Where l \# ist eine [Bezeichnung-vs](label---vs.md) , die den Anfang der aufzurufenden Unterroutine kennzeichnet.
-   \[!\] der optionale boolesche not-Modifizierer.
-   b \# identifiziert ein [konstantes boolesches Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| callnz bool            |      | x    | x    | x     | x    | x     |



 

Diese Anweisung führt Folgendes aus:


```
if (specified boolean register is not zero)
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

 

 




