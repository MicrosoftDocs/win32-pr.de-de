---
title: texreg2ar-PS
description: Interpretiert die Alpha-und roten Farbkomponenten des Quell Registers als Textur Adressdaten (u, v), um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht. Das Ergebnis wird im Ziel Register gespeichert.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473453"
---
# <a name="texreg2ar---ps"></a>texreg2ar-PS

Interpretiert die Alpha-und roten Farbkomponenten des Quell Registers als Textur Adressdaten (u, v), um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht. Das Ergebnis wird im Ziel Register gespeichert.

## <a name="syntax"></a>Syntax



| texreg2ar DST, src |
|--------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2ar             | x    | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung ist für die Neuzuordnung von Farbräumen nützlich.

Im folgenden finden Sie ein Beispiel für die Reihenfolge der Anweisung:

<dl> tex t (n)  
texreg2ar t (m), t (n), wobei m > n  
Die erste Anweisung lädt die Textur Farbe (RGBA).  
in Register TN  
tex TN  
Mit der zweiten Anweisung wird die Farbe neu zugeordnet.  
t (m)<sub>RGBA</sub> = texturesample (Phase m)<sub>RGBA</sub> mit t (n)<sub>AR</sub> als Koordinaten
</dl>

\_bx2 kann nicht für das src-Register für texreg2ar [-oder texreg2gb-PS-](texreg2gb---ps.md) Anweisungen verwendet werden.

Für diese Anweisung muss das Quell Register nicht signierte Daten verwenden. Die Verwendung von signierten oder gemischten Daten im Quell Register führt zu undefinierten Ergebnissen. Weitere Informationen finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 