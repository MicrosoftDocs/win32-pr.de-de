---
title: add (sm4 - asm)
description: Komponentenweises Hinzufügen von 2 Vektoren.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a6a0fbec409f7184c0af3b305603fcf468ef867234e8b6791bff0d1d527ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795399"
---
# <a name="add-sm4---asm"></a>add (sm4 - asm)

Komponentenweises Hinzufügen von 2 Vektoren.



| add \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Der Vektor, der *src1* hinzugefügt werden soll.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der Vektor, der *src0* hinzugefügt werden soll.<br/>                |



 

## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen erzielt werden, vorausgesetzt, dass weder Überlauf noch Unterlauf auftreten. F bedeutet endliche reelle Zahl.



| **src0 src1->** | **-inf** | **-F**     | **-denorm** | **-0** | **+0** | **denorm** | **+F**     | **+inf** | **NaN** |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| **-inf**           | -inf     | -inf       | -inf        | -inf   | -inf   | -inf       | -inf       | NaN      | NaN     |
| **-F**             | -inf     | -F         | src0        | src0   | src0   | src0       | +-F oder +-0 | +inf     | NaN     |
| **-denorm**        | -inf     | src1       | -0          | -0     | +0     | +0         | src1       | +inf     | NaN     |
| **-0**             | -inf     | src1       | -0          | -0     | +0     | +0         | src1       | +inf     | NaN     |
| **+0**             | i-inf    | src1       | +0          | +0     | +0     | +0         | src1       | +inf     | NaN     |
| **+denorm**        | -inf     | src1       | +0          | +0     | +0     | +0         | src1       | +inf     | NaN     |
| **+F**             | -inf     | +-F oder +-0 | src0        | src0   | src0   | src0       | +F         | +inf     | NaN     |
| **+inf**           | NaN      | +inf       | +inf        | +inf   | +inf   | +inf       | +inf       | +inf     | NaN     |
| **NaN**            | NaN      | NaN        | NaN         | NaN    | NaN    | NaN        | NaN        | NaN      | NaN     |



 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

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

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





