---
title: gather4 (SM 4.1-ASM)
description: Sammelt die vier texeln, die in einem bilinearen Filter Vorgang verwendet werden, und verpackt Sie in ein einzelnes Register. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981560"
---
# <a name="gather4-sm41---asm"></a>gather4 (SM 4.1-ASM)

Sammelt die vier texeln, die in einem bilinearen Filter Vorgang verwendet werden, und verpackt Sie in ein einzelnes Register.



| gather4 \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] srcsampler. r |
|--------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse des Vorgangs Ergebnisses.<br/>                                                                                                       |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>     | \[in \] enthält die Texturkoordinaten. <br/>                                                                                                                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einem Ressourcen Register. <br/> Das Swizzle ermöglicht, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in den *dest*-Wert geschrieben werden. <br/>            |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>     | \[in \] einem Samplerregister.<br/> Dieser Parameter muss über eine. r (rot)-Swizzle verfügen, was darauf hinweist, dass der Wert des r-Kanals in das *dest*-Objekt kopiert wird. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieser Vorgang funktioniert nur mit einzelnen Kanälen 2D-oder cubemap-Texturen. Bei 2D-Texturen werden nur die Adressierungs Modi des Samplers verwendet und die oberste Ebene jeder MIP-Pyramide verwendet.

Diese Anweisung verhält sich wie die [Beispiel](sample--sm4---asm-.md) Anweisung, aber ein gefiltertes Beispiel wird nicht generiert. Die vier Beispiele, die zum Filtern beitragen würden, werden in xyzw im Uhrzeigersinn im Uhrzeigersinn eingefügt, beginnend mit dem Beispiel in der unteren linken Ecke des abgefragten Speicher Orts. Dies ist identisch mit der Punkt Stichprobe mit (u, v) Texturkoordinaten Deltas an den folgenden Positionen: (-, +), (+, +), (+,-), (-,-), wobei die Größe der Deltas immer eine halbe Texturgröße ist.

Bei cubemap-Texturen, bei denen ein bidirektionale Speicherbedarf einen edgetext aus dem benachbarten Gesicht umfasst, werden verwendet. Für Ecken werden dieselben Regeln wie für die **Beispiel** Anweisung verwendet. Dies ist die unbekannter-Ecke, die als Durchschnitt der drei sich erziehenden Gesichts Ecken betrachtet wird.

Die auf die **Beispiel** Anweisungen geltenden Textur Format Einschränkungen gelten auch für die **gather4** -Anweisung.

Bei Hardware Implementierungen können Optimierungen in herkömmlichen bilinearen filtern, die Beispiele direkt in texeln erkennen und das Lesen von texeln überspringen, die eine Gewichtung von 0 haben, nicht mit **gather4** genutzt werden. **gather4** gibt immer alle angeforderten Texels zurück.

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
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





