---
title: ige (SM4-ASM)
description: Der Komponenten Weise Vektor Integer größer-oder-gleich-Vergleich.
ms.assetid: 3A3225D1-9A3D-4928-9041-38CB6DE16E2A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8709ebedb054dffe227340f2ccd3de572d92ffce
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101071"
---
# <a name="ige-sm4---asm"></a>ige (SM4-ASM)

Der Komponenten Weise Vektor Integer größer-oder-gleich-Vergleich.



| ige dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\] |
|-------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                           |
|-----------------------------------------------------------------|-------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[im \] Ergebnis des Vorgangs.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der-Komponente, die mit *Quelle1* verglichen werden soll.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] der-Komponente, die mit *src0* verglichen werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Führt den ganzzahligen Vergleich (*src0*  >=  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.

Wenn der Vergleich true ist, wird 0xFFFFFFFF für diese Komponente zurückgegeben. Andernfalls wird 0x0000000 zurückgegeben.

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

 

 





