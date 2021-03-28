---
title: Sample (SM4-ASM)
description: Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus. | Sample (SM4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961441"
---
# <a name="sample-sm4---asm"></a>Sample (SM4-ASM)

Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus.



| Sample \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler |
|--------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse des Vorgangs Ergebnisses.<br/>                                      |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>     | \[in \] einem Satz von Texturkoordinaten. Weitere Informationen finden Sie im Abschnitt **Hinweise**.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einem Textur Register. Weitere Informationen finden Sie im Abschnitt **Hinweise**.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>     | \[in \] einem Samplerregister. Weitere Informationen finden Sie im Abschnitt **Hinweise**.<br/>           |



 

## <a name="remarks"></a>Bemerkungen

Die Quelldaten können von jedem Ressourcentyp (außer Puffern) stammen.

*srcaddress* bietet den Satz von Texturkoordinaten, die zum Ausführen des Beispiels erforderlich sind, als Gleit Komma Werte, die auf normalisierten Raum in der Textur verweisen. Adress Umbruch Modi (Wrap/Mirror/Clamp/Border usw.) werden für Texturkoordinaten außerhalb \[ von 0... 1 \] Bereich angewendet, der aus den samplerzuständen entnommen \# und nach dem Anwenden eines beliebigen Adress Offsets auf Texturkoordinaten angewendet wird.

*srkresource* ist ein Textur Register (t \# ). Dies ist einfach ein Platzhalter für eine Textur, einschließlich des Rückgabe Datentyps der zu sammelnden Ressource. Alle diese Informationen werden in der Shader-Präambel deklariert. Die tatsächlich zu sammelnde Ressource ist an den Shader extern am Slot \# (für t \# ) gebunden.

*srcsampler* ist ein Samplerregister. Dabei handelt es sich um einen Platzhalter für eine Auflistung von Filter Steuerelementen, wie z. b. Point-und linear-, Mipmapping-und Adress Wrapping Steuerung.

Der Satz der Informationen, die für die Hardware zum Durchführen der Stichprobenentnahme erforderlich sind, wird in zwei orthogonale Teile aufgeteilt. Zuerst bietet das Textur Registerinformationen zum Quell Datentyp, z. b. Informationen darüber, ob die Textur sRGB-Daten enthält. Er verweist auch auf den tatsächlich ausgesuchten Speicher. Zweitens definiert das Samplerregister den anzuwendenden Filter Modus.

### <a name="array-resources"></a>Array Ressourcen

Bei Texture1D Arrays wählt die *srcaddress* g-Komponente (POS-Swizzle) aus, aus welchem Array Slice Sie abgerufen werden sollen. Dies wird immer als skalierter Gleit Komma Wert behandelt, nicht als der normalisierte Raum für standardmäßige Texturkoordinaten, und ein roundTo-Next-Wert wird auf den Wert angewendet, gefolgt von einer Klammer zum verfügbaren bufferarray-Bereich.

Bei Texture2D Arrays wählt die *srcaddress* b-Komponente (POS-Swizzle) aus, aus welchem Array Slice abgerufen werden soll, andernfalls mit der gleichen Semantik, die für Texture1D Arrays beschrieben wird.

### <a name="address-offset"></a>Adress Offset

Das optionale \[ \_ aoffimmi (u, v, w)- \] Suffix (Address Offset by immediate Integer) gibt an, dass die Texturkoordinaten für die Stichprobe um einen Satz von angegebenen ganzzahligen ganzzahligen Werten für den unmittelbaren texspace versetzt werden sollen. Bei den Literalwerten handelt es sich um einen Satz von 4 Bit 2-Komplement Nummern mit einem ganzzahligen Bereich von \[ 8, 7 \] . Dieser Modifizierer wird für alle Ressourcen definiert, einschließlich Texture1D/2D-Arrays und Texture3D, ist aber für texturecube nicht definiert.

Die Hardware kann sofort wissen, dass eine Durchführung eines Umfangs von texeln über einen gemeinsamen Standort durch eine Reihe von Beispiel Anweisungen erfolgt. Dies kann mithilfe von \_ aoffimmi (u, v, w) übermittelt werden.

Die Offsets werden den Texturkoordinaten in texesbereich relativ zu den einzelnen miplevel-Zeichen hinzugefügt, auf die zugegriffen wird. Obwohl Texturkoordinaten als normalisierte Gleit Komma Werte bereitgestellt werden, wendet der Offset einen ganzzahligen Wert für texturspace an.

Adress Offsets werden nicht an der Array Achse von Texture1D/2D-Arrays angewendet.

\_aoffimmi v, w-Komponenten werden für Texture1Ds ignoriert.

\_die Komponente "aoffimmi w" wird für Texture2Ds ignoriert.

Adress Umbruch Modi (Umbruch/Spiegelung/Klammer/Rahmen usw.) aus den samplerzuständen \# werden angewendet, nachdem alle Adress Offsets auf Texturkoordinaten angewendet wurden.

### <a name="return-type-control"></a>Rückgabe-typsteuer Element

Das Datenformat, das vom Beispiel an das Ziel Register zurückgegeben wird, wird durch das Ressourcen Format (DXGI- \_ Format \* ) bestimmt, das an den *srkresource* -Parameter (t) gebunden ist \# . Wenn z. b. das angegebene t an \# eine Ressource mit dem Format DXGI- \_ Format \_ A8B8G8R8 \_ unorm \_ sRGB gebunden wurde, konvertiert der Samplingvorgang samplingtexels von Gamma 2,0 in 1,0, wendet Filter an, und das Ergebnis wird als Gleit Komma Werte im Bereich \[ 0.. 1 in das Ziel Register geschrieben \] .

Zurückgegebene Werte sind 4 Vektoren (mit Format spezifischen Standardeinstellungen für Komponenten, die nicht im Format vorhanden sind). Der *Wert für* " *srkresource* " hängt davon ab, wie das aus dem Textur Beispiel/-Filter zurückgegebene Ergebnis der 4-Komponente ausgeblendet wird 

Wenn **Sample** einen 32-Bit-Float-Wert in ein 32-Bit-Register liest, wobei Punkt Stichproben (keine Filterung) vorliegen, können DENORMAL-Werte geleert oder nicht geändert werden. andernfalls sind Zahlen unverändert. Wenn die Ungewissheit mit den Wert Werten für die Punkt Stichproben Entnahme für eine Anwendung ein Problem ist, verwenden Sie die [LD](ld--sm4---asm-.md) -Anweisung, die sicherstellt, dass 32-Bit-Float-Werte unverändert gelesen werden.

### <a name="lod-calculation"></a>LOD-Berechnung

Ausführliche Informationen zur Berechnung von Ableitungen bei der Ermittlung der Lod für das Filtern finden Sie unter [DERIV \_ RTX](deriv-rtx--sm4---asm-.md) und [DERIV \_ Eigenschaft](deriv-rty--sm4---asm-.md). Die **Beispiel** Anweisung berechnet implizit Ableitungen der Texturkoordinaten mithilfe derselben Definition, die von den **DERIV** -shaderanweisungen verwendet wird. Dies gilt nicht für die Anweisungen für eine [Beispiel- \_ l](sample-l--sm4---asm-.md) oder eine [Beispiel \_ -d](sample-d--sm4---asm-.md) . Diese Anweisungen werden direkt von der Anwendung bereitgestellt.

Bei der **Beispiel** Anweisung können Implementierungen die gleiche Lod-Berechnung für alle 4 Pixel in einem 2 x 2-Stempel (aber keinen größeren Bereich) verwenden oder pro Pixel-Lod-Berechnungen durchführen.

### <a name="miscellaneous-details"></a>Sonstige Details

Für buffer & Texture1D werden *srcaddress* . GBA-Komponenten (POS-Swizzle) ignoriert. Für Texture1D Arrays werden die *srcaddress* . BA-Komponenten (POS-Swizzle) ignoriert. Für Texture2Ds wird die *srcaddress* . a-Komponente (POS-Swizzle) ignoriert.

Wenn Sie aus einem Eingabe Slot abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.

### <a name="restrictions"></a>Beschränkungen

-   *srkresource* muss ein t- \# Register sein. *srkresource* kann kein constantbuffer-Wert sein, der nicht an t-Register gebunden werden kann \# .
-   *srcsampler* muss ein s- \# Register sein.
-   Die relative Adressierung in *srkresource* oder *srcsampler* ist nicht zulässig.
-   *srcaddress* muss ein Temp (r \# /x \# ), ein constantbuffer (CB \# ), ein Eingabe (v \# )-Register oder unmittelbare Werte sein.
-   *dest* muss ein Temp-(r \# /x \# ) oder Output (o \* \# )-Register sein.
-   \_aoffimmi (u, v, w) ist für texturecubes nicht zulässig.

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

 

 





