---
title: movc (sm4 - asm)
description: Komponentenweises bedingtes Verschieben. | movc (sm4 - asm)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81da36b39f60929bdfbac3b4a37c379189cf358ed4844e1a4cc899f867970065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095360"
---
# <a name="movc-sm4---asm"></a>movc (sm4 - asm)

Komponentenweises bedingtes Verschieben.



| movc \[ \_ sat \] dest \[ .mask \] , src0 \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle , \] \[ - \] src2 abs \[ \_ \] \[ .swizzle \] , |
|----------------------------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs. <br/> Wenn *src0*, dann *dest*  =  *src1* else *dest*  =  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten, für die die Bedingung getestet werden soll.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die zu verschiebende Komponenten. <br/>                                                                                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Die zu verschiebende Komponenten.<br/>                                                                                      |



 

## <a name="remarks"></a>Hinweise

Im folgenden Beispiel wird die Verwendung dieser Anweisung veranschaulicht.

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

Die Modifizierer für *src1* und *src2*, mit Ausnahme von swizzle, setzen voraus, dass es sich bei den Daten um Gleitkommadaten handelt. Das Fehlen von Modifizierern verschiebt nur Daten, ohne Bits zu ändern.

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

 

 





