---
title: imul (sm4 - asm)
description: Multiplizieren von ganzzahligen Zahlen mit Vorzeichen.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87eabcc07dc5c6a662494c71a26c5f60e5fa1053265e3740ad3605ed685771a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986490"
---
# <a name="imul-sm4---asm"></a>imul (sm4 - asm)

Multiplizieren von ganzzahligen Zahlen mit Vorzeichen.



| imul destHI \[ .mask \] , destLO \[ .mask \] , \[ - \] src0 \[ .swizzle \] , \[ - \] src1 \[ .swizzle\] |
|-------------------------------------------------------------------------------------|



 



| Element                                                                                           | Beschreibung                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[in \] Die Adresse der hohen 32 Bits des Ergebnisses.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[in \] Die Adresse der niedrigen 32 Bits des Ergebnisses.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[in \] Der Wert, der mit *src1* multipliziert werden soll.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[in \] Der Wert, der mit *src0* multipliziert werden soll.<br/>             |



 

## <a name="remarks"></a>Hinweise

Komponentenweise Multiplikation der 32-Bit-Operanden *src0* und *src1* (beide sind signiert), wodurch das richtige vollständige 64-Bit-Ergebnis (pro Komponente) erzeugt wird. Die niedrigen 32 Bits (pro Komponente) werden in *destLO* platziert. Die hohen 32 Bits (pro Komponente) werden in *destHI* platziert.

Entweder *destHI* oder *destLO* kann als NULL angegeben werden, anstatt ein Register anzugeben, wenn die hohen oder niedrigen 32 Bits des 64-Bit-Ergebnisses nicht benötigt werden.

Der optionale Negierungsmodifizierer für Quellopernden nimmt das Komplement von 2 an, bevor eine arithmetische Operation ausgeführt wird.

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

 

 





