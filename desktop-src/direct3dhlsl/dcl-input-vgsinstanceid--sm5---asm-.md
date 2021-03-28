---
title: dcl_input vgsinstanceid (SM5-ASM)
description: Aktivieren Sie die Instanziierung von Geometry-Shader.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313763"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a>DCL \_ -Eingabe vgsinstanceid (SM5-ASM)

Aktivieren Sie die Instanziierung von Geometry-Shader.



| DCL \_ -Eingabe vgsinstanceid, InstanceCount |
|-----------------------------------------|



 



| Element                                                                                                                       | BESCHREIBUNG                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vgsinstanceid*<br/> | \[in \] der Instanz-ID.<br/>    |
| <span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*<br/> | \[in \] der Instanzanzahl.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der *InstanceCount* -Parameter der Deklaration gibt an, wie viele Instanzen der Geometry-Shader für jede Eingabe primitive ausführen soll. Der maximale Wert für *InstanceCount* ist 32.

Die maximale Anzahl der für die Ausgabe deklarierten Scheitel Punkte über [**DCL \_ maxoutputvertexcount**](dcl-maxoutputvertexcount.md)gilt einzeln für jede Instanz.

Die Anzahl der Instanzen in dieser Deklaration, multipliziert mit der maximalen Vertex-Anzahl pro Instanz über [**DCL \_ maxoutputvertexcount**](dcl-maxoutputvertexcount.md), muss <= 1024 sein.

Die Datenmenge, die eine bestimmte Geometry-Shader-Instanz ausgeben kann, beträgt 1024 skalare Höchstwerte, die überprüft werden, indem alle für die Eingabe deklarierten Skars gezählt und die Anzahl der deklarierten Ausgabe Vertex multipliziert wird.

Die Verwendung der Geometrie-Shader-Instanziierung erhöht die Gesamtmenge der Daten, die pro Eingabe primitive ausgegeben werden können. 1024 skalare für eine einzelne Instanz ergeben bis zu 1024 \* 32 skalare der Ausgabedaten für alle Geometry-Shader-Instanzen für einen einzelnen Eingabe primitive. Je mehr Instanzen jedoch, desto weniger Scheitel Punkte können von jeder Instanz ausgegeben werden. Eine einzelne Instanz (keine Instanziierung) kann 1024 Vertices ausgeben. Wenn Sie 32-Instanzen deklarieren, \* bedeutet dies, dass jede Instanz nur 1024/32 = 32 Vertices ausgeben kann.

Die Geometry-Shader-instanziierungsdeklaration stellt dem Programm ein eigenständiges 32-Bit-Ganzzahl-Eingabe Register ( *vgsinstanceid*) zur Verfügung. Jede Geometry-Shader-Instanz wird durch den Wert identifiziert, der in " *vgsinstanceid* \[ 0, 1, 2..." enthalten \] ist.

*vgsinstanceid* ist nicht Teil des Geometry-Shader-Eingabe Vertex-Arrays (z. b. 3 Scheitel Punkte beim Einfügen eines Dreiecks). Das *vgsinstanceid-* Register steht eigenständig, wie z. b. vprimitiveid.

Wenn jede Geometry-Shader-Instanz beendet wird, gibt es eine implizite Ausschneide in der Ausgabe Topologie, sodass aufeinander folgende Instanzen nicht voneinander abhängen.

Obwohl jede Geometry-Shader-Instanz von der Hardware parallel ausgeführt werden kann, wird die Ausgabe aller Instanzen am Ende serialisiert, als ob alle instanzierten Geometry-shaderaufrufe nacheinander in einer Schleife ausgeführt werden, die *vgsinstanceid* von 0 bis *InstanceCount*-1 durchläuft, wobei am Ende jeder Instanz ein impliziter Wert für die Ausgabe Topologie erfolgt.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





