---
title: ilt (sm4 - asm)
description: Komponentenweiser Vektor ganzzahliger Kleiner-als-Vergleich.
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8d70e2c71ad0e503e7119abc2b28e76819053d843b0091d15bfd2045d5351d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119454"
---
# <a name="ilt-sm4---asm"></a>ilt (sm4 - asm)

Komponentenweiser Vektor ganzzahliger Kleiner-als-Vergleich.



| ilt dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|-------------------------------------------------------|



 



| Element                                                            | Beschreibung                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | Das Ergebnis des Vorgangs.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Der wert, der mit *src1 verglichen werden soll.*<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der wert, der mit *src0 verglichen werden soll.*<br/> |



 

## <a name="remarks"></a>Hinweise

Führt den *ganzzahligen Vergleich (src0*  <  *src1)* für jede Komponente aus und schreibt das Ergebnis in *dest.*

Wenn der Vergleich true ist, wird 0xFFFFFFFF Komponente zurückgegeben. Andernfalls 0x0000000 zurückgegeben.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell



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

 

 





