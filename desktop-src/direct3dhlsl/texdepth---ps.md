---
title: textiefe-PS
description: Berechnen von tiefen Werten, die im tiefen Puffer Vergleichstest für dieses Pixel verwendet werden sollen.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857755"
---
# <a name="texdepth---ps"></a>textiefe-PS

Berechnen von tiefen Werten, die im tiefen Puffer Vergleichstest für dieses Pixel verwendet werden sollen.

## <a name="syntax"></a>Syntax



| textiefe DST |
|--------------|



 

where

-   DST ist das Ziel Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| textiefe              |      |      |      | x    |      |      |       |      |       |



 

Diese Anweisung verwendet "R5. r/R5. g" im tiefen Puffer Vergleichstest für dieses Pixel. Die Daten in den blauen und Alpha Kanälen werden ignoriert. Wenn R5. g = 0, das Ergebnis von R5. r/R5. g = 1,0.

Temporäres Register R5 ist das einzige Register, das von dieser Anweisung verwendet werden kann.

Nach dem Ausführen dieser Anweisung ist das temporäre Register "R5" für zusätzliche Verwendung im Shader nicht verfügbar.

Wenn Sie mit dieser Anweisung eine Multisampling-Anweisung verwenden, entfällt der größte Vorteil des tiefen Puffers höherer Auflösung. Da der Pixelshader einmal pro Pixel ausgeführt wird, wird der einzelne tiefen Wert, der von [texm3x2depth-PS](texm3x2depth---ps.md) oder textiefe ausgegeben wird, für jeden Vergleichstest des Subpixels-tiefen Werts verwendet.

## <a name="examples"></a>Beispiele

Hier finden Sie ein Beispiel für die Verwendung von textiefe.


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

 

 




