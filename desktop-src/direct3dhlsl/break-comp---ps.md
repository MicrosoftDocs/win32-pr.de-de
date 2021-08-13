---
title: break_comp – ps
description: Break out of the current loop at the nearest endloop - ps or endrep - ps, based on a per-component comparison.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fa79b7aa50bc734ddc1f9fb1fd54e4130c48518dd47ed429b4177b8fb867d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794458"
---
# <a name="break_comp---ps"></a>break \_ comp - ps

Break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md), based on a per-component comparison.

## <a name="syntax"></a>Syntax



| break \_ comp src0, src1 |
|------------------------|



 

Hierbei gilt:

-   \_comp ist ein skalarer (oder einzelner) Vergleich zwischen den beiden Quellregistern. Folgende Werte sind möglich: 

    | Syntax | Vergleich            |
    |--------|-----------------------|
    | \_Gt   | Größer als          |
    | \_Lt   | Kleiner als             |
    | \_Ge   | Größer als oder gleich |
    | \_Le   | Kleiner als oder gleich    |
    | \_Eq   | Gleich              |
    | \_Ne   | Ungleich          |

    

     

-   src0 ist ein Quellregister. Replizieren von Swizzle ist erforderlich, wenn Sie eine einzelne Komponente auswählen.
-   src1 ist ein Quellregister. Replizieren von Swizzle ist erforderlich, wenn Sie eine einzelne Komponente auswählen.

## <a name="remarks"></a>Hinweise

Diese Anweisung wird in den folgenden Versionen unterstützt.



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| break \_ comp           |      |      |      |      |      | x    | x     | x    | x     |



 

Wenn der Vergleich true ist, bricht er wie gezeigt aus der aktuellen Schleife auf.


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen zum Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




