---
title: fcall(SM5-ASM)
description: Schnittstellen Funktionsaufrufe.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389586"
---
# <a name="fcall-sm5---asm"></a>fcall(SM5-ASM)

Schnittstellen Funktionsaufrufe.



| fcallcenter FP \# \[ arrayIndex \] \[ CallSite\] |
|--------------------------------------|



 



| Element                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*FP\#*<br/>                                                  | \[im \] Funktionszeiger.<br/>                                                                                                                                                                                                                                                                    |
| <span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*Array Index*<br/> | \[in \] optional. Gibt einen Offset im Funktionszeiger Array an. Dieser Parameter muss eine Literale Ganzzahl ohne Vorzeichen sein, wenn FP \# nicht als Indexable deklariert wurde. Andernfalls weist Arrayindex möglicherweise die Form "literalbasis + Offset" aus einem Shader-Register auf. Beispiel: fcallfp1 \[ R1. w + 0 \] \[ 0 \] .<br/> |
| <span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*CallSite*<br/>     | \[in \] optional. Eine Literale Abweichung ohne Vorzeichen in der ausgewählten Funktions Tabelle, wobei eine Funktions Text-FB ausgewählt wird, die \# ausgeführt werden soll. <br/>                                                                                                                                                                |



 

## <a name="remarks"></a>Bemerkungen

*FP \#* \[ *arrayIndex* \] \[ \] löst eine bestimmte Funktions Tabelle aus, die aus der API außerhalb des Shaders aus den in der Deklaration von *FP \#* aufgelisteten Funktionstabellen Optionen ausgewählt wurde.

Die Summe von \# in *FP \#* und *arrayIndex* wählen Sie die Funktions Tabelle aus. Wenn eine Schnittstelle beispielsweise als FP4 \[ 4 \] \[ 3 \] (Array Größe 4) deklariert ist, sind die folgenden **fcalls** äquivalent: fcallfp4 \[ 2 \] \[ 3 \] und FP5 \[ 1 \] \[ 3 \] , da 4 + 2 = 5 + 1 ist.

### <a name="restrictions"></a>Beschränkungen

-   Wenn *arrayIndex* dynamische Indizierung verwendet, ist das Verhalten nicht definiert, wenn *arrayIndex* bei angrenzenden shaderaufrufen abweicht, die in Lockstep ausgeführt werden könnten. Der HLSL-Compiler versucht, diesen Fall zu unterbinden.

    Angrenzende Aufrufe können aufgrund der Fluss Steuerung inaktiv sein, da Sie die Ausführung von Gleichschritt nicht unterbrechen.

-   Wenn *FP \#*  +  *arrayIndex* einen Out-of-Bounds-Index angibt, ist das Verhalten nicht definiert.
-   In den hier beschriebenen undefinierten Fällen bedeutet dies, dass das Verhalten des aktuellen D3D-Geräts nicht definiert ist, einschließlich der Möglichkeit, dass das Gerät verloren geht. Es wird jedoch kein Speicher außerhalb des aktuellen D3D-Geräts aufgerufen oder als Code ausgeführt.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





