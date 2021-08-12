---
title: utof (sm4 - asm)
description: Ganzzahl ohne Vorzeichen in Gleitkommakonvertierung.
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd5e69476c77ee71e25c3e2286ddd53cc01027197b7ad9d83ed723438a93882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283008"
---
# <a name="utof-sm4---asm"></a>utof (sm4 - asm)

Ganzzahl ohne Vorzeichen in Gleitkommakonvertierung.



| utof dest \[ .mask \] , src0 \[ .swizzle\] |
|--------------------------------------|



 



| Element                                                            | Beschreibung                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die zu konvertierenden Komponenten.<br/>                  |



 

## <a name="remarks"></a>Hinweise

*src0* muss eine 4-Tupel-32-Bit-Ganzzahl ohne Vorzeichen enthalten. Nachdem die Anweisung ausgeführt wurde, *enthält dest* ein Gleitkomma-4-Tupel. Die Konvertierung erfolgt pro Komponente.

Wenn ein ganzzahliger Eingabewert zu groß ist, um genau im Gleitkommaformat dargestellt zu werden, runden Sie auf den nächsten geraden Modus.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





