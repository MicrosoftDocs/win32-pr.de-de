---
title: LD (SM4-ASM)
description: Ruft Daten aus dem angegebenen Puffer oder der Textur ohne Filter (z. b. Punkt Stichproben) ab, wobei die angegebene ganzzahlige Adresse verwendet wird. Die Quelldaten können von jedem Ressourcentyp (außer texturecube) stammen.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313685"
---
# <a name="ld-sm4---asm"></a>LD (SM4-ASM)

Ruft Daten aus dem angegebenen Puffer oder der Textur ohne Filter (z. b. Punkt Stichproben) ab, wobei die angegebene ganzzahlige Adresse verwendet wird. Die Quelldaten können von jedem Ressourcentyp (außer texturecube) stammen.



| LD \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle\] |
|----------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse des Vorgangs Ergebnisses.<br/>                                                               |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>     | \[in \] den Texturkoordinaten, die zum Ausführen des Beispiels erforderlich sind.<br/>                                                     |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einem Textur Register (t \# ), das als festgelegt werden muss, welches Textur oder Puffer abgerufen werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung ist eine vereinfachte Alternative zur [Beispiel](sample--sm4---asm-.md) Anweisung. Anders als bei **Sample** kann **LD** auch Daten aus Puffern abrufen. **LD** kann auch aus Multisample-Ressourcen abrufen (nur auf dem Pixel-Shader).

*srcaddress* bietet den Satz von Texturkoordinaten, die zum Ausführen des Beispiels in Form von Ganzzahlen ohne Vorzeichen benötigt werden. Wenn *srcaddress* außerhalb des Bereichs \[ 0... liegt ( \# texeln in Dimension-1) \] , dann wird das Verhalten außerhalb des gültigen Bereichs aufgerufen, wobei **LD** in allen nicht fehlenden Komponenten im Format von *srkresource* 0 (null) und die Standardeinstellung für fehlende Komponenten zurückgibt. Eine Anwendung, die eine flexiblere Kontrolle über das Adress Verhalten außerhalb des gültigen Bereichs hat, sollte stattdessen die **Beispiel** Anweisung verwenden, da Sie das als samplerzustand definierte Adress Umbruch-/Spiegelungs-/einspannen/Rahmen Verhalten berücksichtigt.

*srcaddress. a* (POS-Swizzle) stellt immer eine MipMap-Ebene ohne Vorzeichen bereit. Wenn der Wert außerhalb des Bereichs \[ 0... liegt ( NUM miplevels in Resource-1) \] ), dann wird das Verhalten außerhalb des gültigen Bereichs aufgerufen. Wenn die Ressource ein Puffer ist, der keine Mipmaps aufweisen kann, wird *srcaddress. a ignoriert.*

*srcaddress. GB* (POS-Swizzle) wird für Puffer und texture1D (Non-Array) ignoriert. *srcaddress. b* (POS-Swizzle) wird für texture1D Arrays und texture2Ds ignoriert.

Bei texture1D Arrays stellt *srcaddress. g* (POS-Swizzle) den Array Index als Ganzzahl ohne Vorzeichen bereit. , Wenn der Wert außerhalb des Bereichs der verfügbaren Array Indizes \[ 0 (null) liegt. Array Größe-1) \] , dann wird das Verhalten außerhalb des gültigen Bereichs aufgerufen.

Für texture2D Arrays stellt *srcaddress. b* (POS-Swizzle) den Array Index bereit, andernfalls mit der gleichen Semantik wie für texture1D.

Wenn Sie von *t \#* abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.

### <a name="address-offset"></a>Adress Offset

Das optionale \[ \_ aoffimmi (u, v, w)- \] Suffix (Address Offset by immediate Integer) gibt an, dass die Texturkoordinaten für die **LD** durch eine Menge von bereitgestellten ganzzahligen ganzzahligen Werten des unmittelbaren texraums versetzt werden. Bei den Literalwerten handelt es sich um einen Satz von 4 Bit 2-Komplement Nummern mit einem ganzzahligen Bereich von \[ 8, 7 \] . Dieser Modifizierer ist nur für texture1D/2D/3D definiert, einschließlich Arrays, nicht für Puffer.

Die Offsets werden den Texturkoordinaten in texesbereich relativ zu dem vom **LD** zugegriffen auf das miplevel hinzugefügt.

Adress Offsets werden nicht an der Array Achse von texture1D/2D-Arrays angewendet.

Die Komponenten " *\_ aoffimmi v" und "w* " werden bei texture1Ds ignoriert.

Die Komponente " *\_ aoffimmi w* " wird für texture2Ds ignoriert.

Da die Texturkoordinaten für **LD** ganze Zahlen ohne Vorzeichen sind, wird der Offset, wenn der Offset bewirkt, dass die Adresse unter 0 (null) wechselt, in eine große Adresse umbrochen und führt zu einem Zugriff außerhalb des gültigen Bereichs.

### <a name="return-type-control"></a>Rückgabe-typsteuer Element

Das Datenformat, das von **LD** an das Ziel Register zurückgegeben wird, wird auf die gleiche Weise wie für die **Beispiel** Anweisung bestimmt. Sie basiert auf dem Format, das an den *srkresource* -Parameter *( \# t*) gebunden ist.

Wie bei der **Beispiel** Anweisung sind die zurückgegebenen Werte für **LD** vier Vektoren mit Format spezifischen Standardwerten für Komponenten, die nicht im-Format vorhanden sind. Der Wert für " *srkresource* " hängt davon ab, wie das aus der Textur Auslastung zurückgegebene Ergebnis der 4-Komponente durch die Verwendung von ". Mask" unter " *dest* " bestimmt wird, welche Komponenten in *dest* aktualisiert werden.

Wenn ein 32-Bit-Float-Wert von *LD* in ein 32-Bit-Register gelesen wird, sind die Bits unverändert. Das heißt, die DENORMAL-Werte bleiben DENORMAL. Dies ist anders als bei der **Beispiel** Anweisung.

### <a name="miscellaneous-details"></a>Sonstige Details

Da der **LD** -Anweisung keine Filterung zugeordnet ist, gelten Konzepte wie Lod-Bias nicht für **LD**. Dementsprechend gibt es *keinen Sampler \# -* Parameter.

### <a name="restrictions"></a>Beschränkungen

-   *srkresource* muss ein t \# -Register und kein texturecube-Element sein. *srkresource* kann kein constantbuffer-Wert sein, der nicht an t-Register gebunden werden kann \# .
-   Die relative Adressierung in *srkresource* ist nicht zulässig.
-   *srcaddress* muss ein Temp-(r \# /x \# ), konstantes (CB \# ) oder Eingabe (v \# )-Register sein.
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
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





