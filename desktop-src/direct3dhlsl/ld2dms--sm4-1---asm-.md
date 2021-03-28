---
title: ld2dms (SM 4.1-ASM)
description: Liest einzelne Beispiele aus zweidimensionalen Multisample-Texturen.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101090"
---
# <a name="ld2dms-sm41---asm"></a>ld2dms (SM 4.1-ASM)

Liest einzelne Beispiele aus zweidimensionalen Multisample-Texturen.



| ld2dms \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , sampleindex (skalare Operand) |
|------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse des Ergebnis des Vorgangs. <br/>                                                                 |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>     | \[in \] den Texturkoordinaten, die zum Ausführen des Beispiels erforderlich sind.<br/>                                                    |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einem Textur Register (t \# ), das deklariert werden muss, um zu ermitteln, welche Textur oder welcher Puffer abgerufen werden soll.<br/> |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*Sample Index*<br/> | \[in werden \] die Beispiele zum Lesen aus *srkresource* unterschieden.<br/>                                                       |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung ist eine vereinfachte Alternative zur [Beispiel](sample--sm4---asm-.md) Anweisung. Er ruft Daten aus der angegebenen Textur ohne Filter (z. b. Punkt Stichproben) mithilfe der angegebenen Ganzzahl *srcaddress* und *sampleindex* ab.

*srcaddress* bietet den Satz von Texturkoordinaten, die zum Ausführen des Beispiels in Form von Ganzzahlen ohne Vorzeichen benötigt werden. Wenn *srcaddress* außerhalb des Bereichs \[ 0... liegt ( \# texeln in Dimension-1) \] , **ld2dms** gibt immer 0 (null) in allen Komponenten zurück, die im Format der Ressource vorhanden sind, und die Standardwerte (0, 0, 0, 1.0 f/0x00000001) für fehlende Komponenten.

*sampleingedex* muss kein Literalwert sein. Der Zähler für mehrere Stichproben muss nicht für die Textur Ressource angegeben werden, und er kann mit tiefen-oder Schablonen Ansichten verwendet werden.

Eine Anwendung, die eine flexiblere Kontrolle über das Adress Verhalten außerhalb des gültigen Bereichs hat, sollte stattdessen die **Beispiel** Anweisung verwenden, da Sie das als samplerzustand definierte Adress Umbruch-/Spiegelungs-/einspannen/Rahmen Verhalten berücksichtigt.

*srcaddress. b* (Post-Swizzle) wird für Texture2Ds ignoriert. , Wenn der Wert außerhalb des Bereichs der verfügbaren Array Indizes \[ 0 (null) liegt. Array Größe-1) \] , dann gibt **ld2dms** immer 0 (null) in allen Komponenten zurück, die im Format der Ressource vorhanden sind, und die Standardwerte (0, 0, 0, 1.0 f/0x00000001) für fehlende Komponenten.

Für Texture2D Arrays stellt *srcaddress. b* (Post-Swizzle) den Array Index bereit. Es hat das gleiche Verhalten wie Texture2D.

*srcaddress. a* (Post-Swizzle) wird immer ignoriert. Der HLSL-Compiler gibt nichts an dieser Ausgabe aus.

*srkresource* ist ein Textur Register (t \# ), das deklariert werden muss (22.3.11), und identifiziert, welche Textur abgerufen werden soll.

Wenn Sie von t abrufen \# , an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.

### <a name="address-offset"></a>Adress Offset

Das optionale \[ \_ aoffimmi (u, v, w)- \] Suffix (Address Offset by immediate Integer) gibt an, dass die Texturkoordinaten für die **ld2dms** durch eine Menge von bereitgestellten ganzzahligen ganzzahligen Werten für den unmittelbaren texspace versetzt werden. Bei den Literalwerten handelt es sich um einen Satz von 4 Bit 2-Komplement Nummern mit einem ganzzahligen Bereich von \[ 8, 7 \] .

Die Offsets werden den Texturkoordinaten in texspace hinzugefügt.

Adress Offsets werden nicht an der Array Achse von Texture1D/2D-Arrays angewendet.

Die Komponenten " *\_ aoffimmi v" und "w* " werden bei Texture1Ds ignoriert.

Die Komponente " *\_ aoffimmi w* " wird für Texture2Ds ignoriert.

Da die Texturkoordinaten für **ld2dms** eine ganze Zahl ohne Vorzeichen sind, wird der Offset, wenn der Offset bewirkt, dass die Adresse unter 0 (null) wechselt, in eine große Adresse umschlossen und einen Out-of-Limit-Zugriff zur Folge hat, wie z. b. **LD** gibt 0 (null) in allen Komponenten zurück, die im Format der Ressource vorhanden sind

### <a name="sample-number"></a>Stichproben Nummer

**ld2dms** ist für die Verwendung in einer beliebigen Ressource verfügbar. **ld2dms** arbeitet mit Ausnahme von 2D-Multisample-Ressourcen identisch mit **LD** , indem der zusätzliche (0-basierte) *sampleindex* -Operand verwendet wird, um zu ermitteln, welches Beispiel aus der Ressource gelesen werden soll.

Das Ergebnis der Angabe eines *samplindex* , der die Anzahl der Stichproben in der Ressource überschreitet, ist nicht definiert, aber es können keine Daten außerhalb des Adressraums des Geräte Kontexts zurückgegeben werden.

### <a name="return-type-control"></a>Rückgabe-typsteuer Element

Das Datenformat, das von **ld2dms** an das Ziel Register zurückgegeben wird, wird auf die gleiche Weise wie für die **Beispiel** Anweisung festgelegt. Sie basiert auf dem Format, das an den *srkresource* -Parameter (t) gebunden ist \# .

Wie bei der **Beispiel** Anweisung sind die zurückgegebenen Werte für **ld2dms** 4 Vektoren mit Format spezifischen Standardwerten für Komponenten, die nicht im-Format vorhanden sind. Der Wert für " *srkresource* " hängt davon ab, wie das aus der Textur Auslastung zurückgegebene Ergebnis der 4-Komponente durch die Verwendung von ". Mask" unter " *dest* " bestimmt wird, welche Komponenten in *dest* aktualisiert werden.

Wenn ein 32-Bit-Float-Wert von **ld2dms** in ein 32-Bit-Register gelesen wird, sind die Bits unverändert. Das heißt, die DENORMAL-Werte bleiben DENORMAL. Dies ist anders als bei der **Beispiel** Anweisung.

### <a name="miscellaneous-details"></a>Sonstige Details

Da dieser Anweisung keine Filterung zugeordnet ist, gelten keine Konzepte wie Lod-Bias. Dementsprechend gibt es keinen *Sampler \#* -Parameter.

### <a name="restrictions"></a>Beschränkungen

-   *srkresource* muss ein t \# -Register und kein texturecube, Texture1D oder Texture1DArray sein. *srkresource* kann kein constantbuffer-Wert sein, der nicht an t-Register gebunden werden kann \# .
-   Die relative Adressierung in *srkresource* ist nicht zulässig.
-   *srcaddress* und *sampleindex* müssen ein Temp-(r \# /x \# ), konstantes (CB \# ) oder Eingabe (v \# )-Register sein.
-   *dest* muss ein Temp-(r \# /x \# ) oder Output (o \* \# )-Register sein.

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

 

 





