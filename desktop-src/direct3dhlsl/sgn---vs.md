---
title: sgn – vs
description: Berechnet das Vorzeichen der Eingabe.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1a4994c807ff1df99016aad734edf71e5e1ce6efe59fd53a4fb9bb3ee91a4b25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671680"
---
# <a name="sgn---vs"></a>sgn – vs

Berechnet das Vorzeichen der Eingabe.

## <a name="syntax"></a>Syntax



| sgn dst, src0, src1, src2 |
|---------------------------|



 

where

-   dst ist das Zielregister.
-   src0 ist ein Quellregister.
-   src1 ist ein temporäres Register, das Zwischenergebnisse enthält. Nach der Ausführung sind die Inhalte nicht definiert.
-   src2 ist ein temporäres Register, das Zwischenergebnisse enthält. Nach der Ausführung sind die Inhalte nicht definiert.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Sgn                    |      | x    | x    | x     | x    | x     |



 

Diese Anweisung funktioniert wie unten gezeigt.


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



src1 und src2 müssen unterschiedliche [temporäre Register](dx9-graphics-reference-asm-vs-registers-temporary.md)sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




