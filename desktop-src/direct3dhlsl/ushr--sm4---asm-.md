---
title: ushr (sm4 - asm)
description: Nach rechts verschieben. | ushr (sm4 - asm)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55343f9c9b4db4fff4b0df7ab4e2a567f25f0eb43e93486fe9c41b89cf68454
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787820"
---
# <a name="ushr-sm4---asm"></a>ushr (sm4 - asm)

Nach rechts verschieben.



| ushr dest \[ .mask \] , src0 \[ .swizzle \] , src1.select \_ component |
|--------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die zu verschiebenden Komponenten.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der Betrag, um den *src0 verschoben werden soll.*<br/>                 |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt eine komponentenweise Verschiebung jedes 32-Bit-Werts in *src0* durch eine ganzzahlige Bitanzahl ohne Vorzeichen durch, die vom LSB 5 Bits (0-31-Bereich) in *der src1.select-Komponente \_* bereitgestellt wird, und fügt 0 ein. Das 32-Bit-Ergebnis pro Komponente wird in *dest platziert.* Die Anzahl ist ein Skalarwert, der auf alle Komponenten angewendet wird.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

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

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





