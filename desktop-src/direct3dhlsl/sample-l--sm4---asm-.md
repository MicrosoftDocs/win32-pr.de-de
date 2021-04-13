---
title: sample_l (SM4-ASM)
description: Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus. | sample_l (SM4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353359"
---
# <a name="sample_l-sm4---asm"></a>Sample \_ l (SM4-ASM)

Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus.



| Sample \_ l \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler, srclod. Select \_ Component |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>     | \[in \] einem Satz von Texturkoordinaten. Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einem Textur Register. Weitere Informationen finden Sie in der **Beispiel** Anweisung.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>     | \[in \] einem Samplerregister. Weitere Informationen finden Sie in der **Beispiel** Anweisung.<br/>                                 |
| <span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srclod*<br/>                     | \[in \] der Lod.<br/>                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung ist mit [Sample](sample--sm4---asm-.md)identisch, mit dem Unterschied, dass Lod direkt von der Anwendung als Skalarwert bereitgestellt wird, der keine Anisotropie darstellt. Diese Anweisung ist in allen progambaren Shader-Stufen verfügbar.

**Sample \_ l** Stichproben der Textur mithilfe von *srclod* als Lod. Wenn der Lod-Wert <= 0 ist, wird die NULL-Werte (größte Karte) ausgewählt, wobei der Vergrößerungsfilter angewendet wird (sofern zutreffend basierend auf dem Filter Modus). Da *srclod* ein Gleit Komma Wert ist, wird der Bruchteil-Wert verwendet, um zwischen zwei MIP-Ebenen zu interpolieren, wenn der minimieren-Filter linear ist, oder bei der anisotrope Filterung.

**Beispiel \_ l** ignoriert Adress Ableitungen, sodass das Filter Verhalten rein isotrotrog ist. Da Ableitungen ignoriert werden, verhält sich die anisotrope Filterung als isotrope Filter.

Die samplerzustände miplodbias und Max/minmiplevel werden berücksichtigt.

Bei Verwendung im Pixel-Shader impliziert **Sample \_ l** , dass die Wahl der Lod pro Pixel und keine Auswirkung aus benachbarten Pixeln ist, z. b. im gleichen 2 x 2-Stempel.

Wenn Sie aus einem Eingabe Slot abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| X             | X               | w            |



 

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

 

 





