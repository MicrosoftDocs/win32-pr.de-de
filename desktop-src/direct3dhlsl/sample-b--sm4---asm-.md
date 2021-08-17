---
title: sample_b (sm4 – asm)
description: Stichproben von Daten aus dem angegebenen Element/der angegebenen Textur unter Verwendung der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filtermodus. | sample_b (sm4 – asm)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9193930aadf8874c759fde3beac7d7da4c9d01b709f6e0b1840b36fe0675ef8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790788"
---
# <a name="sample_b-sm4---asm"></a>Sample \_ b (sm4 - asm)

Stichproben von Daten aus dem angegebenen Element/der angegebenen Textur unter Verwendung der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filtermodus.



| sample \_ b \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] , srcSampler, srcLODBias.select \_ component |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | Beschreibung                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/>                                                              |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Eine Gruppe von Texturkoordinaten. Weitere Informationen finden [](sample--sm4---asm-.md) Sie in der Beispielanweisung.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] einem Texturregister. Weitere Informationen finden  Sie in der Beispielanweisung.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] einem Samplerregister. Weitere Informationen finden  Sie in der Beispielanweisung.<br/>                                 |
| <span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*<br/>     | \[Informationen \] zu diesem Parameter finden Sie im Abschnitt **"Hinweise".**<br/>                                        |



 

## <a name="remarks"></a>Hinweise

Die Quelldaten können von einem beliebigen Ressourcentyp stammen, mit Ausnahme von Puffern. Ein zusätzlicher Bias wird auf die Detailebene angewendet, die im Rahmen der Anweisungsausführung berechnet wird.

Diese Anweisung verhält [](sample--sm4---asm-.md) sich wie die Beispielanweisung mit dem Hinzufügen des angegebenen *srcLODBias-Werts* auf die Ebene des Detailwerts, der als Teil der Anweisungsausführung berechnet wird, bevor die MIP-Zuordnungen ausgewählt werden. Der *srcLODBias-Wert* wird der berechneten LOD pro Pixel zusammen mit dem Wert des Samplers MipLODBias vor der Klammer an MinLOD und MaxLOD hinzugefügt.

### <a name="restrictions"></a>Beschränkungen

-   **Sample \_ b** erbt die gleichen Einschränkungen wie die Beispielanweisung sowie zusätzliche Einschränkungen für den zusätzlichen Parameter. [](sample--sm4---asm-.md)
-   Der Bereich von *srcLODBias* ist (-16.0f bis 15.99f); -Werte außerhalb dieses Bereichs führen zu nicht definierten Ergebnissen.
-   *srcLODBias* muss eine einzelne Komponentenauswahl verwenden, wenn es sich nicht um einen skalaren unmittelbaren Selektor handelt.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

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

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





