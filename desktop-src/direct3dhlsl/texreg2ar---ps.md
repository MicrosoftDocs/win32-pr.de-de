---
title: texreg2ar – ps
description: Interpretiert die Alpha- und rot-Farbkomponenten des Quellregisters als Texturadressdaten (u,v), um die Textur in der Phase zu beproben, die der Zielregisternummer entspricht. Das Ergebnis wird im Zielregister gespeichert.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee9516c43f5e8d774ef496a0e66ae1a8ee839ff3df6f2f5436caaf887f95da54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284001"
---
# <a name="texreg2ar---ps"></a>texreg2ar – ps

Interpretiert die Alpha- und rot-Farbkomponenten des Quellregisters als Texturadressdaten (u,v), um die Textur in der Phase zu beproben, die der Zielregisternummer entspricht. Das Ergebnis wird im Zielregister gespeichert.

## <a name="syntax"></a>Syntax



| texreg2ar dst, src |
|--------------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2ar             | x    | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung ist nützlich für Farbraum-Neu-App-Vorgänge.

Hier ist ein Beispiel für die Sequenz, der die Anweisung folgt:

<dl> tex t(n)  
texreg2ar t(m), t(n) where m > n  
Die erste Anweisung lädt die Texturfarbe (RGBA).  
in register tn  
tex tn  
Mit der zweiten Anweisung wird die Farbe neu zuzuordnungen.  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>AR</sub> as coordinates
</dl>

\_bx2 kann nicht im src-Register für texreg2ar oder [texreg2gb verwendet](texreg2gb---ps.md) werden – ps-Anweisungen.

Für diese Anweisung muss das Quellregister nicht signierte Daten verwenden. Die Verwendung von signierten oder gemischten Daten im Quellregister führt zu nicht definierten Ergebnissen. Weitere Informationen finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 