---
title: sincos (sm4 - asm)
description: Komponentenweise sin(theta) und cos(theta) für theta im Bogenmaß.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c03118ff9a1fc2d958eaa6eb1a550a6dbf672a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997017"
---
# <a name="sincos-sm4---asm"></a>sincos (sm4 - asm)

Komponentenweise sin(theta) und cos(theta) für theta im Bogenmaß.



| sincos \[ \_ sat \] destSIN \[ \] .mask, destCOS \[ \] .mask, \[ - \] src0 abs \[ \_ \] \[ .swizzle\] |
|------------------------------------------------------------------------------------|



 



| Element                                                                                               | BESCHREIBUNG                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*<br/> | \[in \] Die Adresse von sin(*src0*), berechnet pro Komponente.<br/> |
| <span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*<br/> | \[in \] Die Adresse von cos(*src0*), berechnet pro Komponente.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                    | \[in \] Die Komponenten, für die sin und cos berechnet werden.<br/>    |



 

## <a name="remarks"></a>Hinweise

Wenn das Ergebnis nicht benötigt wird, können Sie *destSIN* und *destCOS* als NULL angeben, anstatt ein Register anzugeben.

Thetawerte können beliebige IEEE 32-Bit-Gleitkommawerte sein.

Der maximale absolute Fehler beträgt 0,0008 im Intervall von -100 \* Pi bis +100 \* Pi.

Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden.

F bedeutet endliche reale Zahl.



| **src**     | **-inf** | **-F**       | **-denorm** | **-0** | **+0** | **+denorm** | **+F**       | **+inf** | **NaN** |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| **destSIN** | NaN      | \[-1 bis +1\] | -0          | -0     | +0     | +0          | \[-1 bis +1\] | NaN      | NaN     |
| **destCOS** | NaN      | \[-1 bis +1\] | +1          | +1     | +1     | +1          | \[-1 bis +1\] | NaN      | NaN     |



 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





