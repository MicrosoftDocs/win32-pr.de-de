---
title: ld2dms (sm4.1 – asm)
description: Liest einzelne Stichproben aus zweidimensionalen Mehrstichprobentexturen.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17d00b3d6cdc3640f0b8d5266bd6dc8fd6dafefaf10cf47b500011cfe952d4ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043788"
---
# <a name="ld2dms-sm41---asm"></a>ld2dms (sm4.1 – asm)

Liest einzelne Stichproben aus zweidimensionalen Mehrstichprobentexturen.



| ld2dms \[ \_ aoffimmi(u,v) \] dest \[ .mask \] , srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] , sampleIndex (Skalaroperand) |
|------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | Beschreibung                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Die Adresse des Ergebnisses des Vorgangs. <br/>                                                                 |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Die Texturkoordinaten, die zum Ausführen des Beispiels erforderlich sind.<br/>                                                    |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] einem Texturregister (t \# ), das deklariert worden sein muss, um die Textur oder den Puffer zu identifizieren, aus der abgerufen werden soll.<br/> |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[in \] Idendifies the samples to read from *srcResource*.<br/>                                                       |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung ist eine vereinfachte [](sample--sm4---asm-.md) Alternative zur Beispielanweisung. Sie ruft Daten aus der angegebenen Textur ohne Filterung (z. B. Punktsampling) mithilfe der bereitgestellten ganzzahligen *Werte srcAddress* und *sampleIndex* ab.

*srcAddress* stellt den Satz von Texturkoordinaten bereit, die zum Ausführen der Stichprobe in Form von ganzzahligen Zahlen ohne Vorzeichen erforderlich sind. Wenn *srcAddress* den Bereich \[ 0... ( \# Texel in Dimension -1) \] , **ld2dms** gibt immer 0 in allen Komponenten zurück, die im Format der Ressource vorhanden sind, und Standardwerte (0,0,0,1,0f/0x00000001) für fehlende Komponenten.

*sampleIndex* muss kein Literal sein. Die Anzahl mehrerer Stichproben muss nicht für die Texturressource angegeben werden und funktioniert mit Tiefen- oder Schablonenansichten.

Eine Anwendung, die eine flexiblere Kontrolle über das Adressverhalten außerhalb des Bereichs wünschen, sollte stattdessen die Beispielanweisung verwenden, da sie das als Samplerzustand definierte Verhalten von Adressumbruch/Spiegelung/Klammer/Rahmen berücksichtigt. 

*srcAddress.b* (post-swizzle) wird für Texture2Ds ignoriert. Wenn der Wert außerhalb des Bereichs der verfügbaren Arrayindizes \[ liegt, 0...( array size-1) \] , dann gibt **ld2dms** immer 0 in allen Komponenten zurück, die im Format der Ressource vorhanden sind, und standardwertt (0,0,0,1,0f/0x00000001) für fehlende Komponenten.

Für Texture2D-Arrays stellt *srcAddress.b* (post-swizzle) den Arrayindex bereit. Oherwise hat das gleiche Verhalten wie Texture2D.

*srcAddress.a* (post-swizzle) wird immer ignoriert. Der HLSL-Compiler gibt dort nie etwas aus.

*srcResource* ist ein Texturregister (t \# ), das deklariert worden sein muss (22.3.11), das angibt, von welcher Textur abgerufen werden soll.

Beim Abrufen von aus \# t, an das nichts gebunden ist, wird für alle Komponenten 0 zurückgegeben.

### <a name="address-offset"></a>Adressoffset

Das optionale \[ \_ Suffix aoffimmi(u,v,w) \] (Adressoffset durch sofortige ganzzahlige Zahl) gibt an, dass die Texturkoordinaten für die **ld2dms** durch einen Satz von angegebenen unmittelbaren integer-Werten für den Texelraum versetzt werden sollen. Die Literalwerte sind eine Gruppe von Komplementzahlen von 4 Bit 2 mit einem ganzzahligen Bereich \[ von -8,7 \] .

Die Offsets werden den Texturkoordinaten im Texelbereich hinzugefügt.

Adressoffsets werden nicht entlang der Arrayachse von Texture1D/2D-Arrays angewendet.

Die Komponenten *\_ aoffimmi v,w* werden für Texture1Ds ignoriert.

Die *\_ Komponente aoffimmi w* wird für Texture2Ds ignoriert.

Da die Texturkoordinaten für **ld2dms** ganze Zahlen ohne Vorzeichen sind und der Offset bewirkt, dass die Adresse unter 0 (null) fällt, wird sie mit einer großen Adresse umbrochen und führt zu einem Zugriff außerhalb der Grenzen, der wie **ld** in allen Komponenten im Format der Ressource 0 zurückgibt, und die Standardwerte (0,0,0,1,0f/0x00000001) für fehlende Komponenten.

### <a name="sample-number"></a>Beispielnummer

**ld2dms** steht für jede Ressource zur Verfügung. **ld2dms** funktioniert mit ausnahme von 2D-Multisampleressourcen identisch mit **ld,** indem der zusätzliche (0-basierte) *sampleIndex-Operand* verwendet wird, um zu identifizieren, welches Beispiel aus der Ressource gelesen werden soll.

Das Ergebnis der Angabe eines *sampleIndex,* der die Anzahl der Stichproben in der Ressource überschreitet, ist nicht definiert, kann jedoch keine Daten außerhalb des Adressraums des Gerätekontexts zurückgeben.

### <a name="return-type-control"></a>Rückgabetyp-Steuerelement

Das datenformat, das von **ld2dms** an das Zielregister zurückgegeben wird, wird auf die gleiche Weise bestimmt wie für die Beispielanweisung beschrieben.  Sie basiert auf dem Format, das an den *srcResource-Parameter* (t) gebunden \# ist.

Wie bei  der Beispielanweisung sind die zurückgegebenen Werte für **ld2dms** vier Vektoren mit formatspezifischen Standardwerten für Komponenten, die nicht im -Format vorhanden sind. Die Swizzle auf *srcResource* bestimmt, wie das Ergebnis mit vier Komponenten aus der Texturlast swizzle wird. Danach bestimmt .mask on *dest,* welche Komponenten in *dest* aktualisiert werden.

Wenn ein 32-Bit-Gleitkommawert von **ld2dms** in ein 32-Bit-Register gelesen wird, bleiben die Bits unverändert. Das heißt, denormale Werte bleiben denormal. Dies unterscheidet  sich von der Beispielanweisung.

### <a name="miscellaneous-details"></a>Sonstige Details

Da dieser Anweisung keine Filterung zugeordnet ist, gelten Konzepte wie LOD-Voreingenommenheit nicht. Entsprechend gibt es keinen *\# Sampler-s-Parameter.*

### <a name="restrictions"></a>Beschränkungen

-   *srcResource* muss ein t \# register und kein TextureCube, Texture1D oder Texture1DArray sein. *srcResource* kann kein ConstantBuffer sein, der nicht an t-Register gebunden werden \# kann.
-   Die relative Adressierung für *srcResource* ist nicht zulässig.
-   *srcAddress* und *sampleIndex* müssen ein temp-Register (r \# /x), eine Konstante \# (cb) oder ein \# Eingaberegister \# (v) sein.
-   *dest* muss ein temp-Register (r \# \# /x) oder eine Ausgabe (o ) \* \# sein.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





