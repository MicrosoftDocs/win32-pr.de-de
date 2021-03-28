---
title: texm3x3-PS
description: Führt eine 3X3-Matrix Multiplikation aus, wenn Sie in Verbindung mit zwei texm3x3pad-PS-Anweisungen verwendet wird.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976353"
---
# <a name="texm3x3---ps"></a>texm3x3-PS

Führt eine 3X3-Matrix Multiplikation aus, wenn Sie in Verbindung mit zwei [texm3x3pad-PS-](texm3x3pad---ps.md) Anweisungen verwendet wird.

## <a name="syntax"></a>Syntax



| texm3x3 DST, src |
|------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3               |      | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung ist mit der [texm3x3tex-PS-](texm3x3tex---ps.md) Anweisung ohne die Textur Suche identisch.

Diese Anweisung wird als letzte von drei Anweisungen verwendet, die einen 3X3-Matrix Multiplikations Vorgang darstellen. Die 3X3-Matrix besteht aus den Texturkoordinaten der dritten Textur Phase und den beiden vorangehenden Textur Stufen. Jede Textur, die einer der drei Textur Stufen zugewiesen ist, wird ignoriert.

Diese Anweisung muss mit zwei texm3x3pad-Anweisungen verwendet werden. Textur Register müssen der folgenden Reihenfolge folgen.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



Hier finden Sie weitere Details dazu, wie die 3X3-Multiplikation durchgeführt wird.

Die erste texm3x3pad-Anweisung führt die erste Zeile der Multiplikation durch, um u<sup>'</sup>zu suchen.

u<sup>'</sup> = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Die zweite texm3x3pad-Anweisung führt die zweite Zeile der Multiplikation durch,<sup>um v zu</sup>suchen.

v<sup>'</sup> = TextureCoordinates (Stufe m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Die texm3x3tex-Anweisung führt die dritte Zeile der Multiplikation aus, um w<sup>'</sup>zu suchen.

w<sup>'</sup> = TextureCoordinates (Stufe m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Platzieren Sie das Ergebnis der Matrix Multiplikation im Ziel Register.

t (m + 2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




