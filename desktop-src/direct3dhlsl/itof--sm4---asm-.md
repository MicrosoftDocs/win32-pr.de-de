---
title: itof (sm4 – asm)
description: Konvertierung von ganzzahligen Zahlen mit Vorzeichen in Gleitkommazahlen.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f473b5cc9664ee1c9acab88381bc9de6a5b4897fac3899923c6bb20c22bba7fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986480"
---
# <a name="itof-sm4---asm"></a>itof (sm4 – asm)

Konvertierung von ganzzahligen Zahlen mit Vorzeichen in Gleitkommazahlen.



| itof dest \[ .mask \] , \[ - \] src0 \[ .swizzle\] |
|-------------------------------------------|



 



| Element                                                            | Beschreibung                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Enthält das Ergebnis des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Enthält den zu konvertierende Wert.<br/>        |



 

## <a name="remarks"></a>Hinweise

Bei dieser Konvertierungsanweisung mit Ganzzahl mit Vorzeichen in Float wird davon ausgegangen, dass *src0* eine 32-Bit-Ganzzahl mit Vorzeichen mit 4 Tupeln enthält. Nachdem die Anweisung ausgeführt wurde, enthält *dest* ein 4-Tupel mit Gleitkomma.

Die Konvertierung wird pro Komponente ausgeführt.

Wenn ein ganzzahliger Eingabewert zu groß ist, um genau im Gleitkommaformat dargestellt zu werden, wird eine Rundung auf den nächstgelegenen geraden Modus dringend empfohlen, aber nicht erforderlich.

Der optionale Negierungsmodifizierer für den Quellopernden übernimmt das Komplement von 2, bevor eine arithmetische Operation ausgeführt wird.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





