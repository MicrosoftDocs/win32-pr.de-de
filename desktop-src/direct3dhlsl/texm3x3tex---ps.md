---
title: texm3x3tex – ps
description: Führt eine Multiplikation der 3x3-Matrix aus und verwendet das Ergebnis, um eine Textursuche zu erstellen. texm3x3tex muss mit zwei Texm3x3pad - ps-Anweisungen verwendet werden.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a40c78fddadde5d58186f9a1ebb01f4d021620862f9d3534e535842a848a2e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787559"
---
# <a name="texm3x3tex---ps"></a>texm3x3tex – ps

Führt eine Multiplikation der 3x3-Matrix aus und verwendet das Ergebnis, um eine Textursuche zu erstellen. texm3x3tex muss mit zwei [Texm3x3pad - ps-Anweisungen](texm3x3pad---ps.md) verwendet werden.

## <a name="syntax"></a>Syntax



| texm3x3tex dst, src |
|---------------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3tex            | x    | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung wird als letzte von drei Anweisungen verwendet, die einen 3x3-Matrix-Multiplikationsvorgang darstellen, gefolgt von einer Textursuche. Die 3x3-Matrix besteht aus den Texturkoordinaten der dritten Texturphase und den beiden vorhergehenden Texturstufen. Der resultierende Dreikomponentenvektor (u,v,w) wird verwendet, um die Textur in Phase 3 zu beproben. Jede Textur, die den beiden vorherigen Texturstufen zugewiesen ist, wird ignoriert. Die Multiplikation der 3x3-Matrix ist in der Regel nützlich, um einen normalen Vektor auf den richtigen Tangensraum für die gerenderte Oberfläche auszurichten.

Diese Anweisung muss mit der Texm3x3pad-Anweisung verwendet werden. Texturregister müssen die folgende Sequenz verwenden.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



Hier finden Sie weitere Details dazu, wie die 3x3-Multiplikation erreicht wird.

Die erste texm3x3pad-Anweisung führt die erste Zeile der Multiplikation aus, um u<sup>'</sup>zu finden.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Die zweite texm3x3pad-Anweisung führt die zweite Zeile der Multiplikation aus, um v<sup>'</sup>zu finden.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Die texm3x3spec-Anweisung führt die dritte Zeile der Multiplikation aus, um w<sup>'</sup>zu finden.

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Schließlich werden in der texm3x3tex-Anweisung t(m+2) mit (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) entnommen und das Ergebnis in t(m+2) gespeichert.

t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) als Koordinaten.

## <a name="examples"></a>Beispiele

Hier sehen Sie einen Beispiel-Shader mit den identifizierten Texturzuordnungen und den identifizierten Texturstufen.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



Für dieses Beispiel ist die folgende Texturphaseneinrichtung erforderlich.

-   Phase 0 wird eine Texturkarte mit normalen Daten zugewiesen. Dies wird häufig als "Bump Map" bezeichnet. Die Daten sind (XYZ)-Normalitäten für jedes Texel. Texturkoordinatensatz 0 definiert die Stichprobenentnahme für diese normale Karte.
-   Texturkoordinatensatz 1 wird Zeile 1 der 3x3-Matrix zugewiesen. Jede Textur, die Phase 1 zugewiesen ist, wird ignoriert.
-   Texturkoordinatensatz 2 wird Zeile 2 der 3x3-Matrix zugewiesen. Jede Textur, die Phase 2 zugewiesen ist, wird ignoriert.
-   Texturkoordinatensatz 3 wird Zeile 3 der 3x3-Matrix zugewiesen. Ein Volume oder eine Cubetextur sollte für die Suche durch den transformierten 3D-Vektor auf Stufe 3 festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




