---
title: texreg2gb - ps
description: Interpretiert die grünen und blauen Farbkomponenten des Quellregisters als Texturadressdaten, um die Textur in der Stufe zu erfassen, die der Zielregisternummer entspricht.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb18a2a79132a08e2659c6df426299ce996beba79566af277500ab9eb0a885f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505748"
---
# <a name="texreg2gb---ps"></a>texreg2gb - ps

Interpretiert die grünen und blauen Farbkomponenten des Quellregisters als Texturadressdaten, um die Textur in der Stufe zu erfassen, die der Zielregisternummer entspricht.

## <a name="syntax"></a>Syntax



| texreg2gb dst, src |
|--------------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2gb             |      | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung ist nützlich für Neuzuordnungsvorgänge im Farbraum.

Hier sehen Sie ein Beispiel für die Sequenz, auf die die Anweisung folgt.

<dl> tex t(n)  
texreg2gb t(m), t(n) where m > n  
Die erste Anweisung lädt die Texturfarbe (RGBA).  
in register tn  
tex tn  
Die zweite Anweisung weist die Farbe neu zu  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> mit t(n)<sub>GB</sub> als Koordinaten
</dl>

\_bx2 kann nicht im src-Register für die Anweisungen [texreg2ar - ps](texreg2ar---ps.md) oder texreg2gb verwendet werden.

Für diese Anweisung muss das Quellregister nicht signierte Daten verwenden. Die Verwendung von signierten oder gemischten Daten im Quellregister führt zu nicht definierten Ergebnissen. Weitere Informationen finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 