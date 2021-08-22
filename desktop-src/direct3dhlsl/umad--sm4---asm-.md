---
title: umad (sm4 - asm)
description: Ganze Zahl ohne Vorzeichen multiplizieren und hinzufügen.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b6a6c649a61c78eebee249b9fec5c032a07a8a0761a3d23d6e45da573be122c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405990"
---
# <a name="umad-sm4---asm"></a>umad (sm4 - asm)

Ganze Zahl ohne Vorzeichen multiplizieren und hinzufügen.



| umad dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle \] , src2 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Der Wert, der mit *src1* multipliziert werden soll.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der Wert, der mit *src1* multipliziert werden soll.<br/>                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Der Wert, der dem Produkt von *src0* und *src1* hinzugefügt werden soll.<br/> |



 

## <a name="remarks"></a>Hinweise

[Komponentenweises Umul](umul--sm4---asm-.md) der 32-Bit-Operanden *src0* und *src1* ohne Vorzeichen, wobei die niedrigen 32 Bits pro Komponente des Ergebnisses gehalten werden. Diese Anweisung führt dann eine [Iadd](iadd--sm4---asm-.md) von *src2* aus, wodurch das richtige niedrige 32-Bit-Ergebnis (pro Komponente) erzeugt wird. Die 32-Bit-Ergebnisse werden in *dest* platziert.

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

 

 





