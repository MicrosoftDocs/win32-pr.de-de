---
title: ieq (sm4 - asm)
description: Komponentenweiser ganzzahliger Vektorgleichheitsvergleich.
ms.assetid: AD010554-80DC-4D2D-B04C-2638276DDC34
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942e45bedd6dd7e920d4c625a4c001d48f6650a47d74e1643eb162c87980de2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743660"
---
# <a name="ieq-sm4---asm"></a>ieq (sm4 - asm)

Komponentenweiser ganzzahliger Vektorgleichheitsvergleich.



| dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|---------------------------------------------------|



 



| Element                                                            | Beschreibung                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Der Wert, der mit *src1 verglichen werden soll.*<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der Wert, der mit *src0 verglichen werden soll.*<br/>           |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt den ganzzahligen Vergleich (*src0*  ==  *src1*) für jede Komponente aus und schreibt das Ergebnis in *dest.*

Wenn der Vergleich true ist, wird 0xFFFFFFFF Komponente zurückgegeben. Andernfalls 0x0000000 zurückgegeben.

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

 

 





