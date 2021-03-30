---
title: SinCos (SM4-ASM)
description: Komponentenweise Sin (urta) und cos (-TA) für die TA im Bogenmaße.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992991"
---
# <a name="sincos-sm4---asm"></a>SinCos (SM4-ASM)

Komponentenweise Sin (urta) und cos (-TA) für die TA im Bogenmaße.



| SinCos \[ \_ Sat \] destsin \[ . mask \] , destcos \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|------------------------------------------------------------------------------------|



 



| Element                                                                                               | BESCHREIBUNG                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destsin*<br/> | \[in \] der Adresse von Sin (*src0*), berechnet pro Komponente.<br/> |
| <span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destcos*<br/> | \[in \] der Adresse von cos (*src0*), berechnet pro Komponente.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                    | \[in \] den Komponenten, für die Sin und COS berechnet werden sollen.<br/>    |



 

## <a name="remarks"></a>Bemerkungen

Wenn das Ergebnis nicht benötigt wird, können Sie *destsin* und *destcos* als NULL angeben, anstatt ein Register anzugeben.

Bei den Metrikwerten kann es sich um beliebige IEEE 32-Bit-Gleit Komma Werte handeln.

Der absolute absolute Fehler ist 0,0008 im Intervall von-100 \* Pi bis + 100 \* Pi.

In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen abgerufen wurden.

F bedeutet eine endliche reelle Zahl.



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| **src**     | **-INF** | **-F**       | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F**       | **+ INF** | **NaN** |
| **destsin** | NaN      | \[-1 bis + 1\] | -0          | -0     | +0     | +0          | \[-1 bis + 1\] | NaN      | NaN     |
| **destcos** | NaN      | \[-1 bis + 1\] | +1          | +1     | +1     | +1          | \[-1 bis + 1\] | NaN      | NaN     |



 

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

 

 





