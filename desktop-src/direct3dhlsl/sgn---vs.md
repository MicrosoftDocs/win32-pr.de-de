---
title: SGN-vs
description: Berechnet das Vorzeichen der Eingabe.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389543"
---
# <a name="sgn---vs"></a>SGN-vs

Berechnet das Vorzeichen der Eingabe.

## <a name="syntax"></a>Syntax



| SGN DST, src0, Quelle1, Quelle2 |
|---------------------------|



 

where

-   DST ist das Ziel Register.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein temporäres Register, das Zwischenergebnisse enthält. Nach der Ausführung sind die Inhalte nicht definiert.
-   Quelle2 ist ein temporäres Register, das Zwischenergebnisse enthält. Nach der Ausführung sind die Inhalte nicht definiert.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| SGN                    |      | x    | x    | x     | x    | x     |



 

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



Quelle1 und Quelle2 müssen unterschiedliche [temporäre Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s aufweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




