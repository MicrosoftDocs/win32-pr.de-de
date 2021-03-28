---
title: texm3x3vspec-PS
description: Führt eine 3X3-Matrix Multiplikation aus und verwendet das Ergebnis, um eine Textur Suche auszuführen.
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948325"
---
# <a name="texm3x3vspec---ps"></a>texm3x3vspec-PS

Führt eine 3X3-Matrix Multiplikation aus und verwendet das Ergebnis, um eine Textur Suche auszuführen. Dies kann für Glanz Reflektion und Umgebungs Zuordnung verwendet werden, bei denen der Eye-Ray-Vektor nicht konstant ist. texm3x3vspec muss in Verbindung mit zwei [texm3x3pad-PS-](texm3x3pad---ps.md) Anweisungen verwendet werden. Wenn der Augen Strahl Vektor konstant ist, führt die [texm3x3spec-PS-](texm3x3spec---ps.md) Anweisung die gleiche Matrix Multiplikation und Textur Suche aus.

## <a name="syntax"></a>Syntax



| texm3x3vspec DST, src |
|-----------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3vspec          | x    | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung führt die letzte Zeile eines 3X3-Matrix Multiplikations Vorgangs aus, interpretiert den resultierenden Vektor als normalen Vektor, um einen Augen Strahl Vektor widerzuspiegeln, und verwendet dann den reflektierten Vektor als Textur Adresse für eine Textur Suche. Es funktioniert genauso wie [texm3x3spec-PS](texm3x3spec---ps.md), mit dem Unterschied, dass der Augen Strahl Vektor aus der vierten Komponente der Texturkoordinaten entnommen wird. Die 3X3-Matrix Multiplikation ist in der Regel hilfreich, um einen normalen Vektor auf den richtigen Tangenten Raum für die zu rendernde Oberfläche zu ausrichten.

Die 3X3-Matrix besteht aus den Texturkoordinaten der dritten Textur Phase und den beiden vorangehenden Textur Stufen. Der resultierende postreflection Vector (UVW) wird verwendet, um eine Stichprobe der Textur in Phase 3 durchführen. Jede Textur, die den vorherigen zwei Textur Stufen zugewiesen ist, wird ignoriert.

Diese Anweisung muss mit der texm3x3pad-Anweisung verwendet werden. Textur Register müssen die folgende Sequenz verwenden.


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



Die erste texm3x3pad-Anweisung führt die erste Zeile der Multiplikation durch, um u<sup>'</sup>zu suchen.

u<sup>'</sup> = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n) <sub>RGB</sub>

Die zweite texm3x3pad-Anweisung führt die zweite Zeile der Multiplikation durch,<sup>um v zu</sup>suchen.

v<sup>'</sup> = TextureCoordinates (Stufe m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Die texm3x3spec-Anweisung führt die dritte Zeile der Multiplikation aus, um w<sup>'</sup>zu suchen.

w<sup>'</sup> = TextureCoordinates (Stufe m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Die texm3x3vspec-Anweisung führt auch eine reflektionsanberechnung durch.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (N \* )/(n \* n) \] \* N-E

Gibt an, wo der normale N von angegeben wird.

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

und der Augen Strahl Vektor E wird von

E = (TextureCoordinates (Stufe m)<sub>Q</sub> ,

TextureCoordinates (Phase m + 1)<sub>Q</sub> ,

TextureCoordinates (Stufe m + 2)<sub>Q</sub> )

Schließlich wird die texm3x3vspec-Anweisung mit t (m + 2) with (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) und das Ergebnis in t (m + 2) gespeichert.

t (m + 2)<sub>RGBA</sub> = texturesample (Phase m + 2)<sub>RGBA</sub> mithilfe von (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) als Koordinaten

## <a name="examples"></a>Beispiele

Hier ist ein Beispiel-Shader mit den identifizierten Textur Zuordnungen und den identifizierten Textur Stufen.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



Für dieses Beispiel ist die folgende Textur Stufen Einrichtung erforderlich.

-   Phase 0 wird eine Textur Zuordnung mit normalen Daten zugewiesen. Dies wird häufig als Bump Map bezeichnet. Bei den Daten handelt es sich um (XYZ) normale für jedes texaus. Texturkoordinaten in Phase n definieren, wie diese normale Karte als Stichprobe festgelegt wird.
-   Der Texturkoordinaten Satz m wird der Zeile 1 der 3X3-Matrix zugewiesen. Alle der Phase m zugewiesenen Textur werden ignoriert.
-   Der Texturkoordinaten Satz m + 1 wird Zeile 2 der 3X3-Matrix zugewiesen. Alle der Phase m + 1 zugewiesenen Textur werden ignoriert.
-   Der Texturkoordinaten Satz m + 2 wird Zeile 3 der 3X3-Matrix zugewiesen. Phase m + 2 wird ein Volume oder eine cubetexturmap zugewiesen. Die Textur stellt Farbdaten (RGBA) bereit.
-   Der Eye-Ray-Vektor E wird an die Anweisung in der vierten Komponente (q) der Texturkoordinaten Daten in den Phasen m, m + 1 und m + 2 geleitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




