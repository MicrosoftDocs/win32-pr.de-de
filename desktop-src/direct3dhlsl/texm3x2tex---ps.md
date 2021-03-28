---
title: texm3x2tex-PS
description: Führt die letzte Zeile einer 3 x 2-Matrix multiplizieren aus und verwendet das Ergebnis, um eine Textur Suche durchzuführen. texm3x2tex muss in Verbindung mit der texm3x2pad-PS-Anweisung verwendet werden.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993094"
---
# <a name="texm3x2tex---ps"></a>texm3x2tex-PS

Führt die letzte Zeile einer 3 x 2-Matrix multiplizieren aus und verwendet das Ergebnis, um eine Textur Suche durchzuführen. texm3x2tex muss in Verbindung mit der [texm3x2pad-PS-](texm3x2pad---ps.md) Anweisung verwendet werden.

## <a name="syntax"></a>Syntax



| texm3x2tex DST, src |
|---------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2tex            | x    | x    | x    |      |      |      |       |      |       |



 

Die-Anweisung wird als eine von zwei Anweisungen verwendet, die einen 3 x 2-Matrix Multiplikations Vorgang darstellen. Diese Anweisung muss mit der [texm3x2pad-PS-](texm3x2pad---ps.md) Anweisung verwendet werden.

Bei Verwendung dieser beiden Anweisungen müssen Textur Register die folgende Sequenz verwenden.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



Hier finden Sie weitere Details dazu, wie die 3 x 2-Multiplikation durchgeführt wird.

Die texm3x2pad-Anweisung führt die erste Zeile der Multiplikation durch, um u<sup>'</sup>zu suchen.

u<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (Stufe m)<sub>UVW</sub>

Die texm3x2tex-Anweisung führt die zweite Zeile der Multiplikation durch,<sup>um v zu</sup>suchen.

v<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (Stufe m + 1)<sub>UVW</sub>

Die texm3x2tex-Anweisung Stichproben die Textur auf der Stufe (m + 1) mit (u<sup>'</sup>, v<sup>'</sup>) und speichert das Ergebnis in t (m + 1).

t (m + 1)<sub>RGB</sub> = texturesample (Phase m + 1)<sub>RGB</sub> mithilfe von (u<sup>'</sup>, v<sup>'</sup> ) als Koordinaten

## <a name="examples"></a>Beispiele

Hier ist ein Beispiel-Shader mit den Textur Maps und den identifizierten Textur Stufen.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



Für dieses Beispiel sind die folgenden Texturen in den folgenden Textur Phasen erforderlich.

-   Phase 0 nimmt eine Zuordnung mit (x, y, z) perturingdaten vor.
-   Phase 1 enthält Texturkoordinaten. In der Textur Phase ist keine Textur erforderlich.
-   Phase 2 enthält sowohl Texturkoordinaten als auch eine 2D-Textur, die in dieser Textur Phase festgelegt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




