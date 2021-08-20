---
title: sample (sm4 - asm)
description: Stichproben von Daten aus dem angegebenen Element/der angegebenen Textur unter Verwendung der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filtermodus. | sample (sm4 - asm)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b6fabb75c819bb2a95fcf500799fd1e8153d6dabfe66d33ba04c518c949fa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671880"
---
# <a name="sample-sm4---asm"></a>sample (sm4 - asm)

Stichproben von Daten aus dem angegebenen Element/der angegebenen Textur unter Verwendung der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filtermodus.



| sample \[ \_ aoffimmi(u,v,w) \] dest \[ .mask \] , srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] , srcSampler |
|--------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | Beschreibung                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/>                                      |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Eine Gruppe von Texturkoordinaten. Weitere Informationen finden Sie im Abschnitt **Hinweise**.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] einem Texturregister. Weitere Informationen finden Sie im Abschnitt **Hinweise**.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] einem Samplerregister. Weitere Informationen finden Sie im Abschnitt **Hinweise**.<br/>           |



 

## <a name="remarks"></a>Hinweise

Die Quelldaten können von einem beliebigen Ressourcentyp stammen, mit Ausnahme von Puffern.

*srcAddress* stellt den Satz von Texturkoordinaten bereit, die zum Ausführen der Stichprobe erforderlich sind, als Gleitkommawerte, die auf den normalisierten Raum in der Textur verweisen. Adressumbruchmodi (Wrap/Mirror/Klammer/Rahmen usw.) werden für Texturkoordinaten außerhalb \[ des Bereichs 0...1 \] angewendet, die aus dem Samplerzustand (s) stammen \# und angewendet werden, nachdem ein Adressoffset auf Texturkoordinaten angewendet wurde.

*srcResource* ist ein Texturregister (t \# ). Dies ist einfach ein Platzhalter für eine Textur, einschließlich des Rückgabedatentyps der Ressource, für die die Stichprobe durchgeführt wird. Alle diese Informationen werden in der Shader-Präambel deklariert. Die tatsächliche Ressource, für die Stichproben entnommen werden sollen, wird extern am Slot an den Shader gebunden \# (für t \# ).

*srcSampler* ist ein Samplerregister (s). Dies ist einfach ein Platzhalter für eine Auflistung von Filtersteuerelementen wie Punkt- im Vergleich zu linearen, mipmapping- und Address Wrapping-Steuerelementen.

Der Satz von Informationen, die für die Hardware zum Durchführen der Stichprobenentnahme erforderlich sind, wird in zwei orthogonale Teile aufgeteilt. Zunächst stellt das Texturregister Informationen zum Quelldatentyp bereit, z. B. Informationen darüber, ob die Textur SRGB-Daten enthält. Sie verweist auch auf den tatsächlichen Arbeitsspeicher, der als Stichprobe entnommen wird. Zweitens definiert das Samplerregister den filtering-Modus, der angewendet werden soll.

### <a name="array-resources"></a>Arrayressourcen

Für Texture1D-Arrays wählt die *Komponente srcAddress* g (POS-swizzle) aus, von welchem Arrayslice abgerufen werden soll. Dies wird immer als skalierter gleitkommawert und nicht als normalisierter Raum für Standardtexturkoordinaten behandelt, und es wird ein Round-to-Near-Wert auf den Wert angewendet, gefolgt von einer Klammer an den verfügbaren BufferArray-Bereich.

Bei Texture2D-Arrays wählt die *Komponente srcAddress* b (POS-swizzle) aus, von welchem Arrayslice abgerufen werden soll, andernfalls mit der gleichen Semantik, die für Texture1D-Arrays beschrieben wird.

### <a name="address-offset"></a>Adressoffset

Das optionale \[ \_ Suffix aoffimmi(u,v,w) \] (Adressoffset durch sofortige ganzzahlige Zahl) gibt an, dass die Texturkoordinaten für die Stichprobe durch eine Reihe von unmittelbar bereitgestellten konstanten Werten für den Texelbereich versetzt werden sollen. Die Literalwerte sind eine Gruppe von Komplementzahlen von 4 Bit 2 mit einem ganzzahligen Bereich \[ von -8,7 \] . Dieser Modifizierer ist für alle Ressourcen definiert, einschließlich Texture1D/2D Arrays und Texture3D, aber für TextureCube nicht definiert.

Hardware kann von der unmittelbaren Kenntnis profitieren, dass ein Durchlauf über einen Teil der Texel über einen gemeinsamen Standort durch eine Reihe von Beispielanweisungen erfolgt. Dies kann mithilfe von \_ aoffimmi(u,v,w) vermittelt werden.

Die Offsets werden den Texturkoordinaten im Texelbereich relativ zu jedem Miplevel hinzugefügt, auf das zugegriffen wird. Obwohl Texturkoordinaten als normalisierte Gleitkommawerte bereitgestellt werden, wendet der Offset einen ganzzahligen Offset für den Texelbereich an.

Adressoffsets werden nicht entlang der Arrayachse von Texture1D/2D-Arrays angewendet.

\_aoffimmi v,w-Komponenten werden für Texture1Ds ignoriert.

\_Die Komponente aoffimmi w wird für Texture2Ds ignoriert.

Adressumbruchmodi (Wrap/Mirror/Klammer/Rahmen usw.) aus dem Samplerzustand \# (s) werden angewendet, nachdem ein Adressoffset auf Texturkoordinaten angewendet wurde.

### <a name="return-type-control"></a>Rückgabetyp-Steuerelement

Das vom Beispiel an das Zielregister zurückgegebene Datenformat wird durch das Ressourcenformat (DXGI FORMAT) bestimmt, \_ \* das an den *srcResource-Parameter* (t) gebunden \# ist. Wenn das angegebene t beispielsweise \# mit einer Ressource im Format DXGI FORMAT \_ \_ A8B8G8R8 \_ UNORM SRGB gebunden \_ wurde, konvertiert der Samplingvorgang die stichprobenierten Texel von Gamma 2.0 in 1.0, wendet die Filterung an, und das Ergebnis wird als Gleitkommawerte im Bereich \[ 0..1 in das Zielregister \] geschrieben.

Zurückgegebene Werte sind 4 Vektoren (mit formatspezifischen Standardwerten für Komponenten, die nicht im Format vorhanden sind). Die Swizzle auf *srcResource* bestimmt, wie das Ergebnis mit vier Komponenten aus dem Texturbeispiel bzw. -filter swizzle wird. Danach bestimmt .mask on *dest,* welche Komponenten in *dest* aktualisiert werden.

Wenn **sample** einen 32-Bit-Gleitkommawert in ein 32-Bit-Register mit Punktsampling (ohne Filterung) liest, werden denormale Werte möglicherweise oder nicht geleert, andernfalls werden Zahlen unverändert. Wenn die Unsicherheit mit denormalen Punktstichprobenwerten ein [](ld--sm4---asm-.md) Problem für eine Anwendung darstellt, verwenden Sie die ld-Anweisung, die sicherstellt, dass 32-Bit-Gleitkommawerte unverändert gelesen werden.

### <a name="lod-calculation"></a>LOD-Berechnung

Ausführliche Informationen dazu, wie Ableitungen beim Bestimmen der LOD für die Filterung berechnet werden, finden Sie unter [deriv \_ rtx](deriv-rtx--sm4---asm-.md) und [deriv \_ rty](deriv-rty--sm4---asm-.md). Die  Beispielanweisung berechnet implizit Ableitungen auf den Texturkoordinaten mit der gleichen Definition, die von den Anweisungen des **deriv-Shaders** verwendet wird. Dies gilt nicht für [beispiel \_ l-](sample-l--sm4---asm-.md) oder [sample \_ d-Anweisungen.](sample-d--sm4---asm-.md) Für diese Anweisungen werden LOD oder Ableitungen direkt von der Anwendung bereitgestellt.

Für  die Beispielanweisung können Implementierungen die gleiche LOD-Berechnung für alle 4 Pixel in einem 2x2-Stempel (aber keinen größeren Bereich) verwenden oder berechnungen pro Pixel durchführen.

### <a name="miscellaneous-details"></a>Sonstige Details

Für Buffer & Texture1D werden *srcAddress* .gba-Komponenten (POS-swizzle) ignoriert. Für Texture1D-Arrays werden *srcAddress* .ba-Komponenten (POS-swizzle) ignoriert. Für Texture2Ds wird *srcAddress* .a-Komponente (POS-swizzle) ignoriert.

Beim Abrufen aus einem Eingabeslot, an den nichts gebunden ist, wird für alle Komponenten 0 zurückgegeben.

### <a name="restrictions"></a>Beschränkungen

-   *srcResource* muss ein t \# register sein. *srcResource* kann kein ConstantBuffer sein, der nicht an t-Register gebunden werden \# kann.
-   *srcSampler* muss ein s \# register sein.
-   Die relative Adressierung für *srcResource* oder *srcSampler* ist nicht zulässig.
-   *srcAddress* muss ein temp -Wert (r \# \# /x), constantBuffer (cb \# ), input (v ) register oder sofortige Werte \# sein.
-   *dest* muss ein temp-Register (r \# \# /x) oder eine Ausgabe (o ) \* \# sein.
-   \_aoffimmi(u,v,w) ist für TextureCubes nicht zulässig.

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

 

 





