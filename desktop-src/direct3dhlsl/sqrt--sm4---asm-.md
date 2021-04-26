---
title: sqrt (sm4 - asm)
description: Komponentenweise Quadratwurzel.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 628601e0a3a78784a5fd1a089ef7608a0cf9ca05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996607"
---
# <a name="sqrt-sm4---asm"></a>sqrt (sm4 - asm)

Komponentenweise Quadratwurzel.



| sqrt \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|-------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Das Ergebnis des Vorgangs.<br/> *dest* = sqrt(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten, für die die Quadratwurzel verwendet werden soll.<br/>             |



 

## <a name="remarks"></a>Hinweise

Die Genauigkeit beträgt 1 ulp.

Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt.

F bedeutet endliche reale Zahl.



|          | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | NaN      | NaN    | -0          | -0     | +0     | +0          | +F     | +inf     | NaN     |



 

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

 

 





