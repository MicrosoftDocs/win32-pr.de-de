---
title: lt (SM4-ASM)
description: Der Komponenten Weise Vektor Gleit Komma-kleiner-als-Vergleich.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a727987e4eaee017137d62dbe12f8581540876
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313674"
---
# <a name="lt-sm4---asm"></a>lt (SM4-ASM)

Der Komponenten Weise Vektor Gleit Komma-kleiner-als-Vergleich.



| lt dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[im \] Wert, der mit *Quelle1* verglichen werden soll.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[im \] Wert, der mit *src0* verglichen werden soll.<br/>             |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt den float-Vergleich (*src0*  <  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.

Wenn der Vergleich true ist, wird 0xFFFFFFFF für diese Komponente zurückgegeben. Andernfalls wird 0x0000000 zurückgegeben.

Denorms werden vor dem Vergleich geleert. die ursprünglichen Quell Register sind unverändert.

+ 0 ist 0 (null).

Der Vergleich mit Nan gibt false zurück.

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

 

 





