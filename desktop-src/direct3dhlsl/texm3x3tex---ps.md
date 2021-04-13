---
title: texm3x3tex-PS
description: Führt eine 3X3-Matrix Multiplikation aus und verwendet das Ergebnis, um eine Textur Suche durchzuführen. texm3x3tex muss mit zwei texm3x3pad-PS-Anweisungen verwendet werden.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389610"
---
# <a name="texm3x3tex---ps"></a>texm3x3tex-PS

Führt eine 3X3-Matrix Multiplikation aus und verwendet das Ergebnis, um eine Textur Suche durchzuführen. texm3x3tex muss mit zwei [texm3x3pad-PS-](texm3x3pad---ps.md) Anweisungen verwendet werden.

## <a name="syntax"></a>Syntax



| texm3x3tex DST, src |
|---------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3tex            | x    | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung wird als letzte von drei Anweisungen verwendet, die einen 3X3-Matrix Multiplikations Vorgang darstellen, gefolgt von einer Textur Suche. Die 3X3-Matrix besteht aus den Texturkoordinaten der dritten Textur Phase und den beiden vorangehenden Textur Stufen. Der resultierende Vektor mit drei Komponenten (u, v, w) wird verwendet, um eine Stichprobe der Textur in Phase 3 durchführen. Jede Textur, die den vorherigen zwei Textur Stufen zugewiesen ist, wird ignoriert. Die 3X3-Matrix Multiplikation ist in der Regel hilfreich, um einen normalen Vektor auf den richtigen Tangenten Raum für die zu rendernde Oberfläche zu ausrichten.

Diese Anweisung muss mit der texm3x3pad-Anweisung verwendet werden. Textur Register müssen die folgende Sequenz verwenden.


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



Hier finden Sie weitere Details dazu, wie die 3X3-Multiplikation durchgeführt wird.

Die erste texm3x3pad-Anweisung führt die erste Zeile der Multiplikation durch, um u<sup>'</sup>zu suchen.

u<sup>'</sup> = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Die zweite texm3x3pad-Anweisung führt die zweite Zeile der Multiplikation durch,<sup>um v zu</sup>suchen.

v<sup>'</sup> = TextureCoordinates (Stufe m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Die texm3x3spec-Anweisung führt die dritte Zeile der Multiplikation aus, um w<sup>'</sup>zu suchen.

w<sup>'</sup> = TextureCoordinates (Stufe m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Schließlich wird die texm3x3tex-Anweisung mit t (m + 2) with (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) und das Ergebnis in t (m + 2) gespeichert.

t (m + 2)<sub>RGBA</sub> = texturesample (Phase m + 2)<sub>RGBA</sub> mithilfe von (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) als Koordinaten.

## <a name="examples"></a>Beispiele

Hier ist ein Beispiel-Shader mit den identifizierten Textur Zuordnungen und den identifizierten Textur Stufen.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



Für dieses Beispiel ist die folgende Textur Stufen Einrichtung erforderlich.

-   Phase 0 wird eine Textur Zuordnung mit normalen Daten zugewiesen. Dies wird häufig als Bump Map bezeichnet. Bei den Daten handelt es sich um (XYZ) normale für jedes texaus. Texturkoordinaten Satz 0 definiert, wie diese normale Karte Stichprobe ist.
-   Der Texturkoordinaten Satz 1 wird Zeile 1 der 3X3-Matrix zugewiesen. Alle der Phase 1 zugewiesenen Textur werden ignoriert.
-   Der Texturkoordinaten Satz 2 wird Zeile 2 der 3X3-Matrix zugewiesen. Alle der Phase 2 zugewiesenen Textur werden ignoriert.
-   Der Texturkoordinaten Satz 3 wird Zeile 3 der 3X3-Matrix zugewiesen. Ein Volume oder eine cubetextur sollte für die Suche nach dem transformierten 3D-Vektor auf Phase 3 festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




