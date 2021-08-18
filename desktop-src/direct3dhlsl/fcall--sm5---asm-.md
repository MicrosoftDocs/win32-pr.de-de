---
title: fcall (sm5 - asm)
description: Schnittstellenfunktionsaufruf.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7781fc0a2fc7bbd715084d3c0e9682a433ddf16e4492724df8fdb2e31c84689
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854510"
---
# <a name="fcall-sm5---asm"></a>fcall (sm5 - asm)

Schnittstellenfunktionsaufruf.



| fcall fp \# \[ arrayIndex \] \[ callSite\] |
|--------------------------------------|



 



| Element                                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*Fp\#*<br/>                                                  | \[in \] Der Funktionszeiger.<br/>                                                                                                                                                                                                                                                                    |
| <span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*Arrayindex*<br/> | \[in \] Optional. Gibt einen Offset in das Funktionszeigerarray an. Dieser Parameter muss eine literale ganze Zahl ohne Vorzeichen sein, wenn fp \# nicht als indizierbar deklariert wurde. Andernfalls kann arrayIndex die Form Literalbasis + Offset aus einem Shaderregister haben. Beispiel: fcall fp1 \[ r1.w + 0 \] \[ 0 \] .<br/> |
| <span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*callSite*<br/>     | \[in \] Optional. Ein literaler ganzzahliger Offset ohne Vorzeichen in der ausgewählten Funktionstabelle, der einen auszuführenden Funktionskörper fb \# auswählt. <br/>                                                                                                                                                                |



 

## <a name="remarks"></a>Hinweise

*fp \#* \[  \] \[ arrayIndex \] löst in eine bestimmte Funktionstabelle auf, die von der API außerhalb des Shaders aus den Funktionstabellenoptionen ausgewählt wurde, die in der Deklaration von *fp aufgeführt sind. \#*

Die Summe von \# in *fp \# und* *arrayIndex* wählt die Funktionstabelle aus. Wenn eine Schnittstelle beispielsweise als fp4 4 3 (Arraygröße von 4) deklariert ist, sind die folgenden \[ \] \[ \] **fcall-Elemente** äquivalent: fcall fp4 \[ 2 3 und \] \[ \] fp5 \[ 1 3 , da \] \[ \] 4+2 = 5+1.

### <a name="restrictions"></a>Beschränkungen

-   Wenn *arrayIndex die* dynamische Indizierung verwendet, ist das Verhalten nicht definiert, wenn *arrayIndex* bei angrenzenden Shaderaufrufen abweichend ist, was in lockstep ausgeführt werden kann. Der HLSL-Compiler versucht, diesen Fall nicht zu verwenden.

    Benachbarte Aufrufe können aufgrund der Flusssteuerung inaktiv sein, da sie die Ausführung von Sperrschritten nicht unterbricht.

-   Wenn *\# fp*  +  *arrayIndex* einen Index ohne Grenzen angibt, ist das Verhalten nicht definiert.
-   Für die hier beschriebenen nicht definierten Fälle bedeutet dies, dass das Verhalten des aktuellen D3D-Geräts nicht definiert wird, einschließlich der Möglichkeit, dass das Gerät verloren geht. Es wird jedoch nicht auf Arbeitsspeicher außerhalb des aktuellen D3D-Geräts zugegriffen oder als Code ausgeführt.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





