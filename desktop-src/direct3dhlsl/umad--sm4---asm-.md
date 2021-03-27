---
title: Umad (SM4-ASM)
description: Ganzzahl ohne Vorzeichen multiplizieren und hinzufügen.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719392"
---
# <a name="umad-sm4---asm"></a>Umad (SM4-ASM)

Ganzzahl ohne Vorzeichen multiplizieren und hinzufügen.



| Umad dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle \] , Quelle2 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[im \] Wert, der mit *Quelle1* multipliziert werden soll.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[im \] Wert, der mit *Quelle1* multipliziert werden soll.<br/>                     |
| <span id="src2"></span><span id="SRC2"></span>*Quelle2*<br/> | \[in \] dem Wert, der dem Produkt von *src0* und *Quelle1* hinzugefügt werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Komponenten Weise [Umul](umul--sm4---asm-.md) der 32-Bit-Operanden *src0* und *Quelle1* ohne Vorzeichen, wobei die unteren 32 Bits pro Komponente des Ergebnisses beibehalten werden. Diese Anweisung führt dann ein [IAdd](iadd--sm4---asm-.md) -Element von *Quelle2* aus und erzeugt das korrekte niedrige 32-Bit-Ergebnis (pro Komponente). Die 32-Bit-Ergebnisse werden in *dest* platziert.

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

 

 





