---
title: Mad (SM4-ASM)
description: Fügen Sie die Komponenten Weise Multiplikation hinzu.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d34823cdb3545f29426117b35903c97c08c5807
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038321"
---
# <a name="mad-sm4---asm"></a>Mad (SM4-ASM)

Die Komponenten Weise Multiplikation & hinzufügen.



| : Mad \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle2 \[ \_ ABS \] \[ . Swizzle\] |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[im \] Ergebnis des Vorgangs.<br/> *dest*  =  *src0* \* *Quelle1*  +  *Quelle2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] multiplicand.<br/>                                                          |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[im \] Multiplikator.<br/>                                                            |
| <span id="src2"></span><span id="SRC2"></span>*Quelle2*<br/> | \[im \] Addend.<br/>                                                                |



 

## <a name="remarks"></a>Bemerkungen

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

 

 





