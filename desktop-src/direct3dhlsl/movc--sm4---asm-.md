---
title: "\"muvc\" (SM4-ASM)"
description: Bedingter Wechsel in Komponenten. | "muvc" (SM4-ASM)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3116b7bc13102386c57c9b8c63d3534147a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995478"
---
# <a name="movc-sm4---asm"></a>"muvc" (SM4-ASM)

Bedingter Wechsel in Komponenten.



| der Pfad von "netvc" ist " \[ \_ \] dest \[ . Mask" \] , src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle2 \[ \_ ABS \] \[ . Swizzle \] , |
|----------------------------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses. <br/> Wenn *src0*, dann *dest*  =  *Quelle1* Else *dest*  =  *Quelle2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten, für die die Bedingung getestet werden soll.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] den zu Verschieb-Komponenten. <br/>                                                                                     |
| <span id="src2"></span><span id="SRC2"></span>*Quelle2*<br/> | \[in \] den zu Verschieb-Komponenten.<br/>                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Das folgende Beispiel zeigt die Verwendung dieser Anweisung.

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

Bei den Modifizierern auf *Quelle1* und *Quelle2*, mit Ausnahme von Swizzle, wird davon ausgegangen, dass die Daten Gleit Komma sind. Das Fehlen von Modifizierern verschiebt Daten nur, ohne Bits zu ändern.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





