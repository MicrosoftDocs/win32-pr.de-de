---
title: callnz bool – ps
description: Rufen Sie auf, wenn nicht 0 (null) ist. Führt einen bedingten Aufruf der Vom Bezeichnungsindex markierten Anweisung aus. | callnz bool – ps
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 793feb1934b86b46f26050a67b5f26d94b9f277e31735c4d1912805374bab903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516626"
---
# <a name="callnz-bool---ps"></a>callnz bool – ps

Rufen Sie auf, wenn nicht 0 (null) ist. Führt einen bedingten Aufruf der Vom Bezeichnungsindex markierten Anweisung aus.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] B\# |
|----------------------|



 

Hierbei gilt:

-   l \# ist eine Bezeichnung – [ps,](label---ps.md) die den Anfang der aufgerufenen Unterroutine markiert.
-   \[!\] ist ein optionaler Negatmodifizierer.
-   b \# identifiziert einen [konstanten booleschen Register.](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz bool           |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung führt Folgendes aus:


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




