---
title: sample_d (SM4-ASM)
description: Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus. | sample_d (SM4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995638"
---
# <a name="sample_d-sm4---asm"></a>Sample \_ d (SM4-ASM)

Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus.



| ssample \_ d \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler, srcxderivatives \[ . Swizzle \] , srcyderivatives \[ . Swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                               | BESCHREIBUNG                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                    | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/>                                                                  |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>                     | \[in \] einem Satz von Texturkoordinaten. Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.<br/>      |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/>                 | \[in \] einem Textur Register. Weitere Informationen finden Sie in der **Beispiel** Anweisung.<br/>                                      |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>                     | \[in \] einem Samplerregister. Weitere Informationen finden Sie in der **Beispiel** Anweisung.<br/>                                      |
| <span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcxableitungen*<br/> | \[in \] den Ableitungen für die Quelladresse in der x-Richtung. Weitere Informationen finden Sie im Abschnitt **Hinweise**.<br/> |
| <span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcY-Ableitungen*<br/> | \[in \] den Ableitungen für die Quelladresse in der y-Richtung. Weitere Informationen finden Sie im Abschnitt **Hinweise**.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung verhält sich wie die [Beispiel](sample--sm4---asm-.md) Anweisung, mit der Ausnahme, dass Ableitungen für die Quelladresse in der x-und der y-Richtung von zusätzlichen Parametern, *srcxderivatives* bzw. *srcyderivatives*, bereitgestellt werden. Diese Ableitungen befinden sich im normalisierten Texturkoordinaten Bereich.

Die r-, g-und b-Komponenten von *srcxderivatives* (POS-Swizzle) stellen du/DX, DV/DX und DW/DX bereit. Die Komponente "a" (POS-Swizzle) wird ignoriert.

Die r-, g-und b-Komponenten von *srcyderivatives* (POS-Swizzle) stellen du/dy, DV/DY und DW/dy bereit. Die Komponente "a" (POS-Swizzle) wird ignoriert.

Anders als bei der **Beispiel** Anweisung, die eine einzelne Lod-Berechnung für einen 2 x 2-Stempel freigeben darf, muss **Sample \_ d** Lod bei der Verwendung im Pixelshader vollständig einzeln berechnen.

Wenn die abgeleiteten Eingaben für **Stichprobe \_ d** aus den Anweisungen für die Ableitung von Anweisungen im Pixelshader stammen und die Werte INF/Nan enthalten, entspricht das Verhalten von **Beispiel \_ d** möglicherweise nicht der **Beispiel** Anweisung, die implizit die Ableitung berechnet. Die INF/NaN-Werte können die Lod-Berechnung anders beeinflussen.

Wenn Sie aus einem Eingabe Slot abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.

### <a name="restrictions"></a>Beschränkungen

-   **Stichprobe \_ d** erbt die gleichen Einschränkungen wie die **Beispiel** Anweisung und zusätzlich eine Einschränkung unten für die zusätzlichen Parameter.
-   *srcxderivatives* und *srcyderivatives* müssen Temp (r \# /x \# ), constantbuffer (CB \# ), Eingabe (v)- \# Register oder unmittelbare Werte sein.

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

 

 





