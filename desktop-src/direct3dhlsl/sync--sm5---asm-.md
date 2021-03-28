---
title: Sync (SM5-ASM)
description: Thread Gruppen Synchronisierung oder Speicherbarriere.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993263"
---
# <a name="sync-sm5---asm"></a>Sync (SM5-ASM)

Thread Gruppen Synchronisierung oder Speicherbarriere.



| \[ \_ uglobal synchronisieren \|\_ugroup \] \[ \_ g \] \[ \_ t\] |
|-------------------------------------------|



 

## <a name="remarks"></a>Bemerkungen

**Sync** verfügt über die Optionen \_ uglobal, \_ ugroup, \_ g und \_ t.

Im Pixelshader ist nur die **Synchronisierung von \_ uglobal** zulässig.

Im COMPUTE-Shader müssen ( \_ uglobal oder \_ ugroup \* ) und/oder \_ g angegeben werden. \_t ist zusätzlich optional.

### <a name="_uglobal"></a>\_uglobal

Arbeitsspeicher-Fence des globalen u \# (UAV).

Alle früheren u \# -Speicher-Lese-/Schreibvorgänge durch diesen Thread in der Programm Reihenfolge werden für alle Threads auf der gesamten GPU sichtbar gemacht, bevor nachfolgende u- \# Speicherzugriffe durch diesen Thread durchgeführt Der gesamte GPU-Teil der Definition wird in einem Fall durch einen weniger globalen Bereich ersetzt, wie unten beschrieben.

Dies gilt für den gesamten UAV-Speicher, der in der aktuellen Shader-Phase gebunden ist.

\_uglobal ist im COMPUTE-Shader oder Pixel-Shader verfügbar.

Für jede gebundene UAV, die nicht vom Shader als Global kohärent deklariert wurde, hat der \_ uglobal u- \# Speicher-Fence nur innerhalb der aktuellen Compute-Shader-Thread Gruppe für diese UAV eine Sichtbarkeit, so als ob Sie \_ ugroup anstelle von \_ uglobal ist. Dieses Problem gilt nur für den Compute-Shader, da der Pixelshader alle UAVs als Global kohärent deklarieren muss.

### <a name="_ugroup"></a>\_ugroup

Arbeitsspeicherfence für Thread Gruppenbereich u \# (UAV).

Alle \# von diesem Thread in der Programm Reihenfolge in der Programm Reihenfolge vorgenommenen Lese-oder Schreibvorgänge für den u-Speicher werden für alle Threads in der Thread Gruppe sichtbar gemacht \# .

Dies gilt für den gesamten UAV-Speicher, der in der aktuellen Shader-Phase gebunden ist.

\_ugroup ist nur im COMPUTE-Shader verfügbar.

Wenn \_ ugroup für einige Implementierungen verfügbar gemacht wird. Der Vorteil der Angabe von \_ ugroup anstelle von \_ uglobal ist, dass der **Synchronisierungs** Vorgang schneller ausgeführt werden kann.

Andere Implementierungen unterscheiden \_ ugroup nicht von \_ uglobal, sodass beide Vorgänge äquivalent sind und sich wie \_ uglobal Verhalten. Anwendungen können Ihre Absicht angeben, indem Sie den engsten Bereich der erforderlichen **Synchronisierung** anfordern.

Selbst wenn eine bestimmte UAV als Global kohärent deklariert ist, \_ wird ein ugroup- **Synchronisierungs** Vorgang auf dieser UAV effizienter funktionieren, wenn keine globale Barriere erforderlich ist.

### <a name="_g"></a>\_selbst

der \# fence "g (Thread Gruppe Shared Memory)".

Alle vorherigen g- \# Speicher Lese-oder Schreibvorgänge durch diesen Thread in der Programm Reihenfolge werden für alle Threads in der Thread Gruppe vor allen nachfolgenden g- \# Speicherzugriffen durch diesen Thread sichtbar gemacht.

Dies gilt für den gesamten g Shared Memory-Speicher der aktuellen Thread Gruppe \# .

\_g ist nur im COMPUTE-Shader verfügbar.

### <a name="_t"></a>\_t

Synchronisierung der Thread Gruppe. Alle Threads innerhalb einer einzelnen Thread Gruppe (diejenigen, die den Zugriff auf einen gemeinsamen Satz von frei gegebenem Register Bereich freigeben können) werden bis zu dem Punkt ausgeführt, an dem Sie diese Anweisung erreichen, bevor ein Thread fortgesetzt werden kann.

\_t kann nicht in der dynamischen Fluss Steuerung platziert werden (Verzweigungen, die sich innerhalb einer Thread Gruppe unterscheiden können), aber in der einheitlichen Fluss Steuerung vorhanden sein, in der alle Threads in der Gruppe denselben Pfad auswählen.

\_t ist nur im COMPUTE-Shader verfügbar.

Im folgenden finden Sie eine Liste der COMPUTE-Shader-Varianten "Sync".

-   Synchronisieren \_ g
-   \_ugroup synchronisieren\*
-   Synchronisieren von \_ uglobal
-   Synchronisieren \_ g \_ t
-   \_ugroup \_ t synchronisieren\*
-   Synchronisieren von \_ uglobal \_ t
-   \_ugroup \_ g synchronisieren\*
-   Synchronisieren von \_ uglobal \_ g
-   \_ugroup-Gruppe \_ g \_ t synchronisieren\*
-   \_uglobal \_ g \_ t synchronisieren

\*Varianten mit \_ ugroup werden möglicherweise nicht durch den HLSL-Compiler als Ziel angesehen \_

Die Auflistung der Pixel-shadersynchronisierungsvarianten umfasst nur die synchrone \_ uglobal.

Durch Speicher Zäune wird verhindert, dass betroffene Anweisungen durch Compiler oder Hardware auf dem Fence neu angeordnet werden.

Mehrere Lesevorgänge von derselben Adresse durch einen shaderaufruf, die nicht durch Speicherbarrieren oder Schreibvorgänge in die Adresse getrennt sind, können zusammen reduziert werden. Gleiches gilt für Schreibvorgänge. Durch eine Barriere getrennte Zugriffe können nicht zusammengeführt oder über die Barriere verschoben werden.

Arbeitsspeicherzäune sind nicht erforderlich, damit atomarische Vorgänge an einer bestimmten Adresse von verschiedenen Threads ordnungsgemäß funktionieren. Es sind Zäune erforderlich, wenn Atomics-und/oder lade-/Speicher Vorgänge in Bezug zueinander synchronisiert werden müssen, da Sie in einzelnen Threads aus der Sicht anderer Threads angezeigt werden.

In der Pixelshader weisen die Anweisungen zum [verwerfen](discard--sm4---asm-.md) einen \_ globalen Fence der Synchronisierung auf, da diese Anweisungen nicht über den **verwerfen** hinweg neu angeordnet werden können. Synchronisieren \_ von uglobal in hilfspixeln (die nur zur Unterstützung von Ableitungen ausgeführt werden) oder verworfene Pixel haben möglicherweise keinerlei Auswirkung. Es ist nicht zulässig, dass Hilfsobjekte oder verworfene Pixel in UAVs geschrieben werden, wenn die Schreibvorgänge im Fall von verwerfen nach dem verwerfen ausgegeben werden. Zurückgegebene Werte von UAVs dürfen nicht zu abgeleiteten Berechnungen beitragen. Daher ist die Synchronisierung \_ von u für Hilfsskripts oder bei der Ausstellung nach einem Verwerfungs Bedarf nicht mehr zu tun.

CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt die synchrone uglobal-Variante dieser Anweisung für alle **\_ shaderphasen** der Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.



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

 

 




