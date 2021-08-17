---
title: texm3x3 – ps
description: Führt eine Multiplikation der 3x3-Matrix aus, wenn sie in Verbindung mit zwei Anweisungen vom Typ texm3x3pad – ps verwendet wird.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 17030bb99eb472b5cffe53474eb04c30159e5e30ffb2d219f1ac47dfce9da205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787733"
---
# <a name="texm3x3---ps"></a>texm3x3 – ps

Führt eine Multiplikation der 3x3-Matrix aus, wenn sie in Verbindung mit zwei Anweisungen vom Typ [texm3x3pad – ps](texm3x3pad---ps.md) verwendet wird.

## <a name="syntax"></a>Syntax



| texm3x3 dst, src |
|------------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3               |      | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung entspricht der Anweisung [texm3x3tex - ps](texm3x3tex---ps.md) ohne Textursuche.

Diese Anweisung wird als letzte von drei Anweisungen verwendet, die einen 3x3-Matrix-Multiplikationsvorgang darstellen. Die 3x3-Matrix besteht aus den Texturkoordinaten der dritten Texturphase und aus den beiden vorhergehenden Texturstufen. Jede Textur, die einer der drei Texturstufen zugewiesen ist, wird ignoriert.

Diese Anweisung muss mit zwei Texm3x3pad-Anweisungen verwendet werden. Texturregister müssen der folgenden Sequenz folgen.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



Hier finden Sie weitere Details dazu, wie die 3x3-Multiplikation erreicht wird.

Die erste texm3x3pad-Anweisung führt die erste Zeile der Multiplikation aus, um u<sup>'</sup>zu finden.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Die zweite texm3x3pad-Anweisung führt die zweite Zeile der Multiplikation aus, um v<sup>'</sup>zu finden.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Die texm3x3tex-Anweisung führt die dritte Zeile der Multiplikation aus, um w<sup>'</sup>zu finden.

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Platzieren Sie das Ergebnis der Multiplikation der Matrix im Zielregister.

t(m+2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




