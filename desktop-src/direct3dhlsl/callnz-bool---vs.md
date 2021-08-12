---
title: callnz bool – vs
description: Rufen Sie auf, wenn nicht 0 (null) ist. Führt einen bedingten Aufruf der Vom Bezeichnungsindex markierten Anweisung aus. | callnz bool – vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a6d5a7646670d182b0b685ab742fb5b2094a89a717a31019165054bcbc4816b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287258"
---
# <a name="callnz-bool---vs"></a>callnz bool – vs

Rufen Sie auf, wenn nicht 0 (null) ist. Führt einen bedingten Aufruf der Vom Bezeichnungsindex markierten Anweisung aus.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] B\# |
|----------------------|



 

Dabei gilt:

-   wobei l \# eine Bezeichnung [ist, im Gegensatz zum](label---vs.md) Markieren des Anfangs der auf zu aufgerufenen Unterroutine.
-   \[!\] ist der optionale boolesche NOT-Modifizierer.
-   b \# identifiziert einen [konstanten booleschen Register.](dx9-graphics-reference-asm-vs-registers-constant-boolean.md)

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
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



Diese Anweisung verwendet einen Vertex-Shaderanweisungsslot.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




