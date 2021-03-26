---
title: texreg2gb-PS
description: Interpretiert die grünen und blauen Farbkomponenten des Quell Registers als Textur Adressdaten, um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976689"
---
# <a name="texreg2gb---ps"></a>texreg2gb-PS

Interpretiert die grünen und blauen Farbkomponenten des Quell Registers als Textur Adressdaten, um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht.

## <a name="syntax"></a>Syntax



| texreg2gb DST, src |
|--------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2gb             |      | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung ist für die Neuzuordnung von Farbräumen nützlich.

Im folgenden finden Sie ein Beispiel für die Sequenz, auf die die Anweisung folgt.

<dl> tex t (n)  
texreg2gb t (m), t (n), wobei m > n  
Die erste Anweisung lädt die Textur Farbe (RGBA).  
in Register TN  
tex TN  
Mit der zweiten Anweisung wird die Farbe neu zugeordnet.  
t (m)<sub>RGBA</sub> = texturesample (Stufe m)<sub>RGBA</sub> mit t (n)<sub>GB</sub> als Koordinaten
</dl>

\_bx2 kann nicht für das src-Register für [texreg2ar-PS-](texreg2ar---ps.md) oder texreg2gb-Anweisungen verwendet werden.

Für diese Anweisung muss das Quell Register nicht signierte Daten verwenden. Die Verwendung von signierten oder gemischten Daten im Quell Register führt zu undefinierten Ergebnissen. Weitere Informationen finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 