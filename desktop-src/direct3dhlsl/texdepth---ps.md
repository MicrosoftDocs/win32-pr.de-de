---
title: texdepth - ps
description: Berechnen Sie die Tiefenwerte, die im Tiefenpuffervergleichstest für dieses Pixel verwendet werden sollen.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f39135c34c07a9a20f03c9ebc979647733884b37680ef07b9bc666b882052690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284174"
---
# <a name="texdepth---ps"></a>texdepth - ps

Berechnen Sie die Tiefenwerte, die im Tiefenpuffervergleichstest für dieses Pixel verwendet werden sollen.

## <a name="syntax"></a>Syntax



| texdepth dst |
|--------------|



 

where

-   dst ist das Zielregister.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdepth              |      |      |      | w    |      |      |       |      |       |



 

Diese Anweisung verwendet r5.r/r5.g im Tiefenpuffervergleichstest für dieses Pixel. Die Daten im blauen und Alphakanal werden ignoriert. Wenn r5.g = 0 ist, ist das Ergebnis von r5.r / r5.g = 1,0.

Das temporäre Register r5 ist das einzige Register, das von dieser Anweisung verwendet werden kann.

Nach dem Ausführen dieser Anweisung ist das temporäre Register r5 für die zusätzliche Verwendung im Shader nicht verfügbar.

Beim Multisampling entfällt durch die Verwendung dieser Anweisung der größte Teil des Vorteils des Tiefenpuffers mit höherer Auflösung. Da der Pixelshader einmal pro Pixel ausgeführt wird, wird der einzelne Tiefenwert, der von [texm3x2depth - ps](texm3x2depth---ps.md) oder texdepth ausgegeben wird, für jeden der Subpixel-Tiefenvergleichstests verwendet.

## <a name="examples"></a>Beispiele

Hier ist ein Beispiel für die Verwendung von texdepth.


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




