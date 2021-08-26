---
title: sample_c (sm4 – asm)
description: Führt einen Vergleichsfilter aus.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2656f70a95487ce98aadc30a028fccaed00cb1c8d6324d64bb22c9672543d5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067730"
---
# <a name="sample_c-sm4---asm"></a>Sample \_ c (sm4 - asm)

Führt einen Vergleichsfilter aus.



| sample \_ c \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swizzle \] , srcResource.r, / must be .r swizzle srcSampler, srcReferenceValue / single component selected |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                       | BESCHREIBUNG                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] Eine Gruppe von Texturkoordinaten. Weitere Informationen finden [](sample--sm4---asm-.md) Sie in der Beispielanweisung.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] einem Texturregister. Weitere Informationen finden  Sie in der Beispielanweisung.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] einem Samplerregister. Weitere Informationen finden  Sie in der Beispielanweisung.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] Ein Register mit einer einzelnen ausgewählten Komponente, die im Vergleich verwendet wird.<br/>                            |



 

## <a name="remarks"></a>Hinweise

Der Hauptzweck dieser Anweisung besteht darin, einen Baustein für Percentage-Closer Tiefenfilterung bereitzustellen. "c" in **Beispiel \_ c** steht für Vergleich.

Die Operanden für **Sample \_ c** sind mit der Beispielanweisung identisch, mit der Ausnahme, dass ein zusätzlicher float32-Quellopernd, *srcReferenceValue,* vorhanden ist, der ein Register mit ausgewählter Einzelkomponente oder ein skalares Literal sein muss. [](sample--sm4---asm-.md)

Der *srcResource-Parameter* muss eine R-Swizzle (rot) aufweisen. **Sample \_ c** arbeitet ausschließlich mit der roten Komponente und gibt einen einzelnen Wert zurück. Die R-Swizzle auf *srcResource* gibt an, dass das Skalarergebnis auf alle Komponenten repliziert wird.

Wenn ein Tiefenpuffer als Eingabetextur festgelegt ist, wird der Tiefenwert in der roten Komponente angezeigt.

Wenn diese Anweisung mit einer Ressource verwendet wird, die kein Texture1D/2D/2DArray/Cube/CubeArray ist, erzeugt sie nicht definierte Ergebnisse.

Wenn diese Anweisung ausgeführt wird, verwendet die Samplinghardware die Vergleichsfunktion des aktuellen Samplers, um *srcReferenceValue* mit dem Wert der Red-Komponente für die Quellressource an jeder Filterabtippposition (Texel) zu vergleichen, die der aktuell konfigurierte Texturfilter basierend auf den bereitgestellten Koordinaten in *srcAddress* abdeckt.

Der Vergleich erfolgt, nachdem *srcReferenceValue* auf die Genauigkeit des Texturformats quantisiert wurde. Dies entspricht genau der Art und Weise, wie z vor dem Tiefenvergleich beim Sichtbarkeitstest der Ausgabezusammenführung in die Genauigkeit des Tiefenpuffers quantisiert wird. Dies schließt eine Klammer an den Formatbereich ein \[ (z.B. 0..1 \] für ein UNORM-Format).

Die Red-Komponente des Quell-Texels wird mit dem quantisierten *srcReferenceValue* verglichen. Für Texel, die aus der Ressource fallen, wird der Wert der Red-Komponente bestimmt, indem die Adressmodi (und BorderColorR im Border-Modus) aus dem Sampler angewendet werden. Der Vergleich berücksichtigt alle D3D11-Gleitkommavergleichsregeln, falls das Texturformat Gleitkomma ist.

Jeder bestandene Vergleich gibt 1,0f als Red-Komponentenwert für das Texel zurück, und jeder Fehlgeschlagene Vergleich gibt 0,0f als Red-Wert für die Textur zurück. Die Filterung erfolgt dann genau wie durch den Sampler-Status angegeben, funktioniert nur in der Red-Komponente und gibt ein einzelnes skalares Filterergebnis zurück an den Shader zurück, repliziert auf alle maskierten *Dest-Komponenten.*

Die Verwendung von **\_ Beispiel c** ist für alle anderen allgemeinen Filtersteuerelemente orthogonal. **Beispiel \_ c** funktioniert nahtlos mit den anderen allgemeinen Filtermodi. **Sample \_ c** ändert das Verhalten der allgemeinen Filter, sodass alle gefilterten Werte aufgrund von Vergleichsergebnissen 1,0f oder 0,0f werden.

Beim Abrufen aus einem Eingabeslot, an den nichts gebunden ist, wird für alle Komponenten 0 zurückgegeben.

Weitere Informationen finden [](sample--sm4---asm-.md) Sie in der Beispielanweisung.

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

 

 





