---
title: callnz bool-PS
description: Wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist. | callnz bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995764"
---
# <a name="callnz-bool---ps"></a>callnz bool-PS

Wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] b\# |
|----------------------|



 

Hierbei gilt:

-   l \# ist eine [Bezeichnung-PS](label---ps.md) , die den Anfang der aufzurufenden Unterroutine markiert.
-   \[!\] ist ein optionaler Negation-Modifizierer.
-   b \# identifiziert ein [konstantes boolesches Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
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

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




