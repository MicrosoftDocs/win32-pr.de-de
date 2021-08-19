---
title: uge (sm4 - asm)
description: Komponentenweiser Vektor mit ganzzahligem Ganzzahlwert ohne Vorzeichen , größer als oder gleich.
ms.assetid: CA8E19EC-619F-4C19-B6FD-91650B5DAF9F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7145e011b9d08bc64ab6b2252afbfb7506a115f5a0f30c3d02db450371c569c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505078"
---
# <a name="uge-sm4---asm"></a>uge (sm4 - asm)

Komponentenweiser Vektor mit ganzzahligem Ganzzahlwert ohne Vorzeichen , größer als oder gleich.



| uge dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|-------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten, die mit *src1 verglichen werden.*<br/>        |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Komponenten, die mit *src0 verglichen werden.*<br/>        |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt den Ganzzahlvergleich ohne Vorzeichen (*src0*  >=  *src1*) für jede Komponente aus und schreibt das Ergebnis in *dest.*

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

 

 





