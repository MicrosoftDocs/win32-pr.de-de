---
title: round_z (sm4 – asm)
description: Gleitkommagerundet auf ganzzahligen Gleitkommawert. | round_z (sm4 – asm)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc874c6d0a1f26902086af300784c55950b71569
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997127"
---
# <a name="round_z-sm4---asm"></a>round \_ z (sm4 - asm)

Gleitkommagerundet auf ganzzahligen Gleitkommawert.



| round \_ z \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|-----------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten im Vorgang.<br/>             |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt eine komponentenweise Gleitkommarunde der Werte in *src0* aus und schreibt ganzzahlige Gleitkommawerte in *dest*.

**round \_ z** rundet auf 0 (null).

Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden.



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | -inf     | -F     | -0          | -0     | +0     | +0          | +F     | +inf     | NaN     |



 

F bedeutet endliche reale Zahl.

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

 

 





