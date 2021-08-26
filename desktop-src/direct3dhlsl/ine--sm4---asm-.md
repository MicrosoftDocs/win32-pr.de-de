---
title: ine (sm4 - asm)
description: Komponentenweiser Ganzzahlvergleich für Vektoren.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0170dd8b5cfd6284356699bc065e5581a601f8868bfd6c0db99a6a53f9bcfd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023850"
---
# <a name="ine-sm4---asm"></a>ine (sm4 - asm)

Komponentenweiser Ganzzahlvergleich für Vektoren.



| ine dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|-------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Enthält den Wert, der mit *src1 verglichen werden soll.*<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Enthält den Wert, der mit *src0 verglichen werden soll.*<br/>    |



 

## <a name="remarks"></a>Hinweise

Führt den ganzzahligen Vergleich (*src0* != *src1*) für jede Komponente aus und schreibt das Ergebnis in *dest.*

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

 

 





