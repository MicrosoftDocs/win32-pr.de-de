---
title: dcl_interface (SM5-ASM)
description: Deklarieren Sie Funktionstabellen Zeiger (Schnittstellen). | dcl_interface (SM5-ASM)
ms.assetid: 5A4D911E-7117-409B-8FDC-9CEC2C185C15
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61435e06d0d5b88bb82ca91f758646d7911d3bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995431"
---
# <a name="dcl_interface-sm5---asm"></a>DCL \_ -Schnittstelle (SM5-ASM)

Deklarieren Sie Funktionstabellen Zeiger (Schnittstellen).



| DCL- \_ Schnittstelle FP \# \[ arraySize \] \[ numcallsites \] = {ft \# , ft \# ,...} |
|----------------------------------------------------------------------|



 



| Element                                                          | BESCHREIBUNG                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*FP\#*<br/> | \[in \] den Funktionstabellen Zeigern.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Jede Schnittstelle muss von der API gebunden werden, bevor der Shader verwendet werden kann. Die Bindung gibt einen Verweis auf eine der Funktionstabellen aus, sodass die Methoden Slots ausgefüllt werden können. Der Compiler generiert keine Zeiger für Objekte, auf die nicht verwiesen wird.

Ein Funktionstabellen Zeiger verfügt über einen vollständigen Satz von Methoden Slots, um die zusätzliche Dereferenzierungsebene zu vermeiden, die eine C++-Darstellung von Zeiger auf Vtable erfordern würde. Dies erfordert auch, dass es sich bei diesen Zeigern um 5 Tupel handelt. Im virtuellen HLSL-Inlining-Modell ist immer bekannt, welche globale Variable/Eingabe für einen-Rückruf verwendet wird, sodass wir Tabellen pro Stamm Objekt einrichten können.

Funktionszeiger Deklarationen geben an, welche Funktionstabellen für Sie zulässig sind. Dadurch wird auch die Ableitung von Methoden Korrelations Informationen ermöglicht.

Der erste \[ \] einer Schnittstellen Deklaration ist die Array Größe. Wenn die dynamische Indizierung verwendet wird, gibt die Deklaration dies wie gezeigt an. Ein Array von Schnittstellen Zeigern kann auch statisch indiziert werden. es ist nicht erforderlich, dass Arrays von Schnittstellen Zeigern eine dynamische Indizierung bedeuten.

Die Nummerierung von Schnittstellen Zeigern beginnt bei 0 für die erste Deklaration und nimmt anschließend die Array Größe in Betracht, sodass der erste Zeiger nach einem vier-Eintrag-Array FP0 \[ 4 \] \[ 1 \] FP4 ist \[ \] \[ \] .

Der zweite Wert \[ \] einer Schnittstellen Deklaration ist die Anzahl von CallSites, die der Anzahl von Text in jeder Tabelle entsprechen muss, auf die in der Deklaration verwiesen wird.

Es gibt keine Grenzen, wie viele Optionen für Funktionstabellen (ft \# ) in einer Schnittstellen Deklaration aufgelistet werden können.

Eine bestimmte Funktions Tabelle (ft \# ) kann in einer oder mehreren Schnittstellen Deklarationen mehrmals vorkommen.

### <a name="restrictions"></a>Beschränkungen

-   Die Anzahl der Objekt Standorte in einem Shader, die die Summe über alle *\# FP* -Deklarationen Ihrer \[ arraySize- \] Deklarationen hinweg ist, darf nicht größer als 253 sein. Diese Zahl gibt an, wie viele **dieser** Zeiger vorhanden sein können. Die Runtime erzwingt dieses 253-Limit, um die Größe des DDI für die Kommunikation mit diesen Zeiger Daten zu beschränken.
-   Die Anzahl der Aufrufen von Websites in einem Shader, die die Summe aller fcallsanweisungen der Anzahl potenzieller Verzweigungs Ziele ist, darf nicht größer als 4096 sein.

    Ein [fcalltyp](fcall--sm5---asm-.md) , der einen statischen Index für die erste *\[ \] \[ \] FP* -Dimension verwendet, zählt z. b. wie folgt:

    `                       fcall fp0[0][0]         // +1`

    Ein **fcalltyp** , der einen dynamischen Index verwendet, zählt als Anzahl von Elementen im Array (erste \[ \] der **DCL- \_ Schnittstelle**):

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    Mit dieser Beschränkung können einige Implementierungen problemlos Tabellen der Funktions Textauswahl im Konstanten Puffer ähnlichen Speicher anpassen.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV und SRV.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





