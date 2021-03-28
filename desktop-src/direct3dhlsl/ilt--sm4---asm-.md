---
title: ILT (SM4-ASM)
description: Der Komponenten Weise Vektor Integerwert ist kleiner als der Vergleich.
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c2e5e47272412bb483e4782e9a6c35e971293c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313632"
---
# <a name="ilt-sm4---asm"></a>ILT (SM4-ASM)

Der Komponenten Weise Vektor Integerwert ist kleiner als der Vergleich.



| ILT dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\] |
|-------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | Das Ergebnis des Vorgangs.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[im \] Wert, der mit *Quelle1* verglichen werden soll.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[im \] Wert, der mit *src0* verglichen werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Führt den ganzzahligen Vergleich *(src0*  <  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.

Wenn der Vergleich true ist, wird 0xFFFFFFFF für diese Komponente zurückgegeben. Andernfalls wird 0x0000000 zurückgegeben.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell



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

 

 





