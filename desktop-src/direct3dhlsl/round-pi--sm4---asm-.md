---
title: round_pi (sm4 - asm)
description: Gleitkomma rundet auf integraler Gleitkommazahl. | round_pi (sm4 - asm)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61282078b3639681eed756e2899d06744f0369e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997107"
---
# <a name="round_pi-sm4---asm"></a>round \_ pi (sm4 - asm)

Gleitkomma rundet auf integraler Gleitkommazahl.



| round \_ pi \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten im Vorgang.<br/>             |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt eine komponentenweise Gleitkommarunde der Werte in *src0* aus und schreibt integrale Gleitkommawerte, *um zu dest zu schreiben.*

**Round \_ pi** rundet in Richtung +unendlich, häufig als ceil() bekannt.

Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden.

F bedeutet endliche reale Zahl.



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | -inf     | -F     | -0          | -0     | +0     | +0          | +F     | +inf     | NaN     |



 

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

 

 





