---
title: texm3x2tex – ps
description: Führt die letzte Zeile einer 3x2-Matrixmultiplikation aus und verwendet das Ergebnis für eine Textursuche. texm3x2tex muss in Verbindung mit der texm3x2pad - ps-Anweisung verwendet werden.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9653325098b05959fcbd9e7a838801652a532d936bdaebc829055b717a49096f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723018"
---
# <a name="texm3x2tex---ps"></a>texm3x2tex – ps

Führt die letzte Zeile einer 3x2-Matrixmultiplikation aus und verwendet das Ergebnis für eine Textursuche. texm3x2tex muss in Verbindung mit der [texm3x2pad - ps-Anweisung verwendet](texm3x2pad---ps.md) werden.

## <a name="syntax"></a>Syntax



| texm3x2tex dst, src |
|---------------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2tex            | x    | x    | x    |      |      |      |       |      |       |



 

Die -Anweisung wird als eine von zwei Anweisungen verwendet, die einen 3x2-Matrixmultiplikationsvorgang darstellen. Diese Anweisung muss mit der [texm3x2pad - ps-Anweisung verwendet](texm3x2pad---ps.md) werden.

Wenn Sie diese beiden Anweisungen verwenden, müssen Texturregister die folgende Sequenz verwenden.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



Hier finden Sie weitere Details dazu, wie die 3x2-Multiplikation erreicht wird.

Die Texm3x2pad-Anweisung führt die erste Zeile der Multiplikation aus, um u<sup>' zu finden.</sup>

u<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m)<sub>UVW</sub>

Die texm3x2tex-Anweisung führt die zweite Zeile der Multiplikation aus, um v<sup>' zu finden.</sup>

v<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m+1)<sub>UVW</sub>

Die texm3x2tex-Anweisung untersucht die Textur auf der Stufe (m+1) mit (u<sup>'</sup>,v<sup>'</sup>) und speichert das Ergebnis in t(m+1).

t(m+1)<sub>RGB</sub> = TextureSample(Stage m+1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) as coordinates

## <a name="examples"></a>Beispiele

Hier ist ein Beispiel-Shader mit den Texturzuordnungen und den identifizierten Texturstufen.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



Für dieses Beispiel sind die folgenden Texturen in den folgenden Texturphasen erforderlich.

-   Phase 0 nimmt eine Karte mit (x,y,z)-Stördaten an.
-   Phase 1 enthält Texturkoordinaten. In der Texturphase ist keine Textur erforderlich.
-   Phase 2 enthält sowohl Texturkoordinaten als auch eine 2D-Textur, die in dieser Texturphase festgelegt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




