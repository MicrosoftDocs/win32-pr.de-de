---
title: gather4 (sm4.1 – asm)
description: Erfasst die vier Texel, die in einem bilinearen Filtervorgang verwendet werden, und packt sie in ein einziges Register. | gather4 (sm4.1 – asm)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb39918bdb421123cb3e2bfe41931740e271f85a27cf36b8994d493656d91c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457580"
---
# <a name="gather4-sm41---asm"></a>gather4 (sm4.1 – asm)

Erfasst die vier Texel, die in einem bilinearen Filtervorgang verwendet werden, und packt sie in ein einziges Register.



| gather4 \[ \_ aoffimmi(u,v) \] dest \[ .mask \] , srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] srcSampler.r |
|--------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/>                                                                                                       |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Enthält die Texturkoordinaten. <br/>                                                                                                                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] Einem Ressourcenregister. <br/> Die Swizzle ermöglicht es, die zurückgegebenen Werte willkürlich zu wischen, bevor sie in *dest* geschrieben werden. <br/>            |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] einem Samplerregister.<br/> Dieser Parameter muss eine R-Swizzle (rot) aufweisen, die angibt, dass der Wert des R-Kanals in *dest* kopiert wird. <br/> |



 

## <a name="remarks"></a>Hinweise

Dieser Vorgang funktioniert nur mit single channel 2D- oder CubeMap-Texturen. Für 2D-Texturen werden nur die Adressierungsmodi des Samplers verwendet, und die oberste Ebene einer Mip-Pyramide wird verwendet.

Diese Anweisung verhält [](sample--sm4---asm-.md) sich wie die Beispielanweisung, aber es wird kein gefiltertes Beispiel generiert. Die vier Beispiele, die zur Filterung beitragen würden, werden im Uhrzeigersinn in xyzw platziert, beginnend mit der Stichprobe links unten am abgefragten Speicherort. Dies entspricht der Punktsampling mit (u,v) Texturkoordinatendelta an den folgenden Stellen: (-,+),(+,+),(+,-),(-,-), wobei die Größe der Deltas immer ein halbes Texel ist.

Für CubeMap-Texturen, wenn ein bilinearer Fußabdruck ein Edge-Texel vom benachbarten Gesicht umfasst, werden verwendet. Ecken verwenden die gleichen  Regeln wie die Beispielanweisung. Dies ist die unpräzische Ecke, die als Durchschnitt der drei einprägenden Gesichtsecken betrachtet wird.

Die Texturformateinschränkungen, die für die **Beispielanweisungen** gelten, gelten auch für die **gather4-Anweisung.**

Bei Hardwareimplementierungen können Optimierungen bei herkömmlicher bilinearer Filterung, die Stichproben direkt auf Texel erkennen und das Lesen von Texel überspringen, die gewicht 0 haben würden, nicht mit **gather4** genutzt werden. **gather4** gibt immer alle angeforderten Texel zurück.

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
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





