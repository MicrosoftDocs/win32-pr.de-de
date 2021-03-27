---
title: imm_atomic_alloc (SM5-ASM)
description: Inkremente Sie den ausgeblendeten 32-Bit-Leistungs Zähler atomisch, der mit einer Anzahl oder angefügt ist, und fügen Sie den ursprünglichen Wert zurück.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719427"
---
# <a name="imm_atomic_alloc-sm5---asm"></a>imm \_ Atomic- \_ Zuweisung (SM5-ASM)

Inkremente Sie den ausgeblendeten 32-Bit-Leistungs Zähler atomisch, der mit einer Anzahl oder angefügt ist, und fügen Sie den ursprünglichen Wert zurück.



| imm \_ Atomic- \_ Zuweisung dst0 \[ . \_ einzelkomponentenmaske \_ \] , dstuav |
|-------------------------------------------------------------|



 



| Element                                                                                           | BESCHREIBUNG                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[in \] enthält den zurückgegebenen Leistungs Zählers.<br/>                    |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*<br/> | \[in \] einem strukturierten Puffer-UAV mit dem count-oder Append-Flag. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Es ist ein ausgeblendeter ganzzahliger 32-Bit-Zählerwert ohne Vorzeichen zugeordnet, der mit jeder Anzahl oder angefügten Puffer Ansicht verknüpft ist, die initialisiert wird, wenn die Sicht an die Pipeline gebunden ist, einschließlich der Option, den vorherigen Wert beizubehalten.

Diese Anweisung führt eine atomarische Inkrement des Leistungs Zählers durch und gibt den ursprünglichen an *dst0* zurück.

Bei einer Append-UAV ist der zurückgegebene Wert nur für die Dauer des Shader-Aufrufe gültig. Danach kann die Implementierung das Speicher Layout neu anordnen. Alle Speicher Adressierung, die auf dem zurückgegebenen Wert basiert, muss auf den Shader-Aufruf beschränkt sein.

Bei einer Append-UAV kann der HLSL-Compiler im Shader-Aufruf den zurückgegebenen Wert als Struktur Index verwenden, der für den Zugriff auf den strukturierten Puffer verwendet werden soll. Der Zugriff auf einen anderen Struktur Index als jene, die von Aufrufen an die Definition von " [ \_](imm-atomic-consume--sm5---asm-.md) **imm \_ Atomic \_** " oder "using" zurückgegeben werden, führt dazu, dass der Zugriff auf die Speicherorte innerhalb der UAV zufällig erfolgt und nur für die Lebensdauer des shaderaufruders festgelegt wird.

Bei einer UAV-Anzahl kann der zurückgegebene Wert von der Anwendung als Verweis auf einen festgelegten Speicherort innerhalb der UAV gespeichert werden, der nach dem Aufruf des Shader aussagekräftig ist. Auf jeden Speicherort in der Anzahl der UAV kann immer unabhängig von der Anzahl des Werts zugegriffen werden.

Es gibt keine Klammer für die Anzahl, sodass Sie bei einem Überlauf umbrochen wird.

Der gleiche Shader kann nicht gleichzeitig sowohl einen " **imm \_ Atomic- \_ Zuweisungen** " als auch einen " **imm Atomic"- \_ \_ Verbrauch** auf derselben UAV Darüber hinaus kann die GPU nicht mehrere shaderaufrufe zulassen, um die Verwendung von " **imm \_ Atomic \_ zugc** " und " **imm \_ Atomic \_** " in derselben UAV zu mischen.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.



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



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





