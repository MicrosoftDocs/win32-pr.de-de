---
title: sample_c (SM4-ASM)
description: Führt einen Vergleichs Filter aus.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993023"
---
# <a name="sample_c-sm4---asm"></a>Beispiel \_ c (SM4-ASM)

Führt einen Vergleichs Filter aus.



| Beispiel \_ c \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource. r,//muss lauten. r Swizzle srcsampler, srkreferencevalue//Single Component Selected |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                       | BESCHREIBUNG                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>                             | \[in \] einem Satz von Texturkoordinaten. Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/>                         | \[in \] einem Textur Register. Weitere Informationen finden Sie in der **Beispiel** Anweisung.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>                             | \[in \] einem Samplerregister. Weitere Informationen finden Sie in der **Beispiel** Anweisung.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srkreferencevalue*<br/> | \[in \] einem Register, bei dem eine einzelne Komponente ausgewählt ist, die im Vergleich verwendet wird.<br/>                            |



 

## <a name="remarks"></a>Bemerkungen

Der Hauptzweck dieser Anweisung besteht darin, einen Baustein für die Percentage-Closer Tiefe Filterung bereitzustellen. Das "c" in **Beispiel \_ c** steht für den Vergleich.

Die Operanden für **" \_ c** " sind identisch mit der [Beispiel](sample--sm4---asm-.md) Anweisung, mit dem Unterschied, dass es einen zusätzlichen float32-Quell Operanden (" *srkreferencevalue*") gibt, bei dem es sich um eine Registerkarte mit einer einzelnen Komponente oder einen skalaren Literalwert handeln muss.

Der *srkresource* -Parameter muss eine. r (rot)-Swizzle aufweisen. **Beispiel \_ c** arbeitet ausschließlich auf der roten Komponente und gibt einen einzelnen Wert zurück. Das. r-wischen in *srkresource* gibt an, dass das skalare Ergebnis an alle Komponenten repliziert wird.

Wenn ein tiefen Puffer als Eingabe Textur festgelegt wird, wird der tiefen Wert in der roten Komponente angezeigt.

Wenn diese Anweisung mit einer Ressource verwendet wird, die kein Texture1D/2D/2darray/Cube/cubearray ist, werden nicht definierte Ergebnisse erzeugt.

Wenn diese Anweisung ausgeführt wird, verwendet die samplinghardware die comparisonfunction des aktuellen Samplers zum Vergleichen von *srkreferencevalue* mit dem Wert der roten Komponente für die Quell Ressource an jedem Filter-Tap-Speicherort (Texel), den der aktuell konfigurierte Textur Filter abdeckt, basierend auf den bereitgestellten Koordinaten in *srcaddress*.

Der Vergleich findet statt, nachdem *srkreferencevalue* mit der Genauigkeit des Textur Formats quantifisiert wurde, und zwar genau auf die gleiche Weise, wie z in der Tiefe der Puffer Genauigkeit quantifisiert wird, bevor der tiefen Vergleich beim Ergebnis der Ausgabe Zusammenführung erfolgt. Dies schließt eine Klammer für den Formatbereich ein (z. b. \[ 0.. 1 \] für ein unorm-Format).

Die rote Komponente des Quell texgs wird mit dem quantifizierten *srroferencevalue* verglichen. Bei texeln, die auf die Ressource zurückgreifen, wird der Wert der roten Komponente durch Anwenden der Adress Modi (und bordercolorr, wenn im Rahmen Modus) vom Sampler festgelegt. Beim Vergleich werden alle D3D11-Gleit Komma Vergleichs Regeln berücksichtigt, wenn das Textur Format Gleit Komma Wert ist.

Jeder übergebenen Vergleich gibt 1.0 f als den roten Komponenten Wert für den Texttyp zurück, und jeder fehlgeschlagene Vergleich gibt 0,0 f als den roten Wert für die Textur zurück. Das Filtern erfolgt dann genau wie in den samplerzuständen angegeben, nur in der roten Komponente betrieben, und es wird ein einzelnes skalarfiltergebnis zurück an den Shader zurückgegeben, das auf *alle maskierten* Endkomponenten repliziert wird.

Die Verwendung von **Beispiel \_ c** ist orthogonal zu allen anderen allgemeinen Filterungs Steuerelementen. **Beispiel \_ c** funktioniert nahtlos mit den anderen allgemeinen Filtermodi. in **Beispiel \_ c** wird das Verhalten der allgemeinen Filter so geändert, dass die Filter, die alle gefiltert werden, aufgrund von Vergleichs Ergebnissen 1.0 f oder 0,0 f werden.

Wenn Sie aus einem Eingabe Slot abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.

Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





