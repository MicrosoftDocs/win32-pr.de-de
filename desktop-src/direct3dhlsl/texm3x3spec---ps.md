---
title: texm3x3spec – ps
description: Führt eine 3x3-Matrixmultiplikation aus und verwendet das Ergebnis, um eine Textursuche durchzuführen. Dies kann für spiegelförmige Reflektion und Umgebungszuordnung verwendet werden. texm3x3spec muss in Verbindung mit zwei texm3x3pad -ps-Anweisungen verwendet werden.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b5fcef771d6d06a1691d5c5e953b76b1c445c7c8df7b2da37b8b4220bef2b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485430"
---
# <a name="texm3x3spec---ps"></a>texm3x3spec – ps

Führt eine 3x3-Matrixmultiplikation aus und verwendet das Ergebnis, um eine Textursuche durchzuführen. Dies kann für spiegelförmige Reflektion und Umgebungszuordnung verwendet werden. texm3x3spec muss in Verbindung mit zwei [texm3x3pad -ps-Anweisungen verwendet](texm3x3pad---ps.md) werden.

## <a name="syntax"></a>Syntax



| texm3x3spec dst, src0, src1 |
|-----------------------------|



 

where

-   dst ist das Zielregister.
-   src0 und src1 sind Quellregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3spec           | x    | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung führt die letzte Zeile einer 3x3-Matrixmultiplikation aus, verwendet den resultierenden Vektor als normalen Vektor, um einen Augenstrahlvektor widerzuspiegeln, und verwendet dann den reflektierten Vektor, um eine Textursuche durchzuführen. Der Shader liest den Augenstrahlvektor aus einem konstanten Register. Die Multiplikation der 3x3-Matrix ist in der Regel nützlich, um einen normalen Vektor am richtigen Tangensraum für die gerenderte Oberfläche zu orientieren.

Die 3x3-Matrix besteht aus den Texturkoordinaten der dritten Texturstufe und den beiden vorangehenden Texturstufen. Der resultierende Post-Reflektionsvektor (u,v,w) wird verwendet, um die Textur in der letzten Texturphase zu beproben. Jede Textur, die den vorherigen beiden Texturphasen zugewiesen ist, wird ignoriert.

Diese Anweisung muss mit zwei texm3x3pad-Anweisungen verwendet werden. Texturregister müssen die folgende Sequenz verwenden.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



Die erste texm3x3pad-Anweisung führt die erste Zeile der Multiplikation aus, um u<sup>' zu finden.</sup>

u<sup>'</sup> = TextureCoordinates(Stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Die zweite texm3x3pad-Anweisung führt die zweite Zeile der Multiplikation aus, um v<sup>' zu finden.</sup>

v<sup>'</sup> = TextureCoordinates(Stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Die texm3x3spec-Anweisung führt die dritte Zeile der Multiplikation aus, um nach w<sup>' zu suchen.</sup>

w<sup>'</sup> = TextureCoordinates(Stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Die texm3x3spec-Anweisung führt dann eine Reflektionsberechnung durch.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (N \* E)/(N \* N) \] \* N - E

wobei das normale N durch angegeben wird

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

und der Augenstrahlvektor E wird durch das Konstantenregister angegeben.

E = c \# (Beliebige Konstante register--c0, c1, c2 usw.- kann verwendet werden)

Schließlich werden die texm3x3spec-Anweisungsbeispiele t(m+2) mit (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) und das Ergebnis in t(m+2) gespeichert.

t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates

## <a name="examples"></a>Beispiele

Hier ist ein Beispiel-Shader mit den Texturzuordnungen und den identifizierten Texturstufen.


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



Für dieses Beispiel ist die folgende Texturphaseneinrichtung erforderlich.

-   Phase 0 wird eine Texturkarte mit normalen Daten zugewiesen. Dies wird häufig als "BumpMap" bezeichnet. Die Daten sind normal (XYZ) für jedes Texel. Texturkoordinaten in Phase n definieren, wo diese normale Karte entnommen werden soll.
-   Texturkoordinatensatz m wird Zeile 1 der 3x3-Matrix zugewiesen. Jede Textur, die Stage m zugewiesen ist, wird ignoriert.
-   Der Texturkoordinatensatz m+1 wird Zeile 2 der 3x3-Matrix zugewiesen. Jede Textur, die der Stufe m+1 zugewiesen ist, wird ignoriert.
-   Der Texturkoordinatensatz m+2 wird Zeile 3 der 3x3-Matrix zugewiesen. Der Stufe m+2 wird eine Volume- oder Cubetexturzuordnung zugewiesen. Die Textur bietet Farbdaten (RGBA).
-   Der Augenstrahlvektor E wird durch ein konstantes Register E = c \# angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




