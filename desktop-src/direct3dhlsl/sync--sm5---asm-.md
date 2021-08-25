---
title: sync (sm5 - asm)
description: Threadgruppensynchronisierung oder Speicherbarriere.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c64532669fc94d7d2109c39e501af0825e56434f66b79e20e1641c787a1a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852860"
---
# <a name="sync-sm5---asm"></a>sync (sm5 - asm)

Threadgruppensynchronisierung oder Speicherbarriere.



| sync \[ \_ uglobal\|\_ugroup \] \[ \_ g \] \[ \_ t\] |
|-------------------------------------------|



 

## <a name="remarks"></a>Hinweise

**Die Synchronisierung** verfügt \_ über die Optionen \_ uglobal, ugroup, \_ g und \_ t.

Im Pixel-Shader ist nur **sync \_ uglobal** zulässig.

Im Compute-Shader müssen ( \_ uglobal oder \_ ugroup \* ) und/oder \_ g angegeben werden. \_t ist zusätzlich optional.

### <a name="_uglobal"></a>\_uglobal

Global u \# (UAV) Memory Fence.

Alle vorherigen Lese-/Schreibvorgänge im U-Arbeitsspeicher dieses Threads in programmgeordneter Reihenfolge werden für alle Threads auf der gesamten GPU sichtbar gemacht, bevor alle nachfolgenden U-Arbeitsspeicherzugriffe \# durch diesen Thread ausgeführt \# werden. Der gesamte GPU-Teil der Definition wird in einem Fall durch einen weniger globalen Bereich ersetzt, wie unten beschrieben.

Dies gilt für den sämtlichen UAV-Speicher, der in der aktuellen Shaderphase gebunden ist.

\_"uglobal" ist im Compute-Shader oder Pixel-Shader verfügbar.

Für alle gebundenen UAV, die vom Shader nicht als global einheitlichen Wert deklariert wurden, verfügt der Uglobal u memory fence nur innerhalb der aktuellen Compute-Shaderthreadgruppe für diese UAV über Sichtbarkeit, als ob es sich um \_ \# \_ "ugroup" statt \_ "uglobal" handelt. Dieses Problem gilt nur für den Compute-Shader, da der Pixel-Shader alle UAVs als global zusammenhängend deklarieren muss.

### <a name="_ugroup"></a>\_ugroup

Threadgruppenbereich u \# (UAV) – Arbeitsspeicher-Fence.

Alle vorherigen u-Arbeitsspeicherlesevorgänge oder -schreibvorgänge dieses Threads in programmgeordneter Reihenfolge werden für alle Threads in der Threadgruppe sichtbar gemacht, bevor alle nachfolgenden \# U-Arbeitsspeicherzugriffe \# durch diesen Thread ausgeführt werden.

Dies gilt für den sämtlichen UAV-Speicher, der in der aktuellen Shaderphase gebunden ist.

\_ugroup ist nur im Compute-Shader verfügbar.

Wenn \_ ugroup verfügbar gemacht wird, für einige Implementierungen. Der Vorteil der Angabe von ugroup anstelle von uglobal ist, dass \_ der Synchronisierungsvorgang \_ schneller abgeschlossen werden kann. 

Andere Implementierungen unterscheiden ugroup nicht von uglobal, sodass beide Vorgänge gleichwertig sind \_ \_ und sich wie \_ uglobal verhalten. Anwendungen können ihre Absicht angeben, indem sie den engsten Synchronisierungsbereich **anfordern, der erforderlich** ist.

Selbst wenn eine bestimmte UAV als global zusammenhängende Synchronisierung deklariert ist, funktioniert ein ugroup-Synchronisierungsvorgang effizienter auf dieser UAV, wenn keine globale Barriere \_ erforderlich ist. 

### <a name="_g"></a>\_G

g \# (Threadgruppe shared memory) fence.

Alle vorherigen g-Arbeitsspeicherlesevorgänge oder -schreibvorgänge dieses Threads in programmgeordneter Reihenfolge werden für alle Threads in der Threadgruppe sichtbar gemacht, bevor alle nachfolgenden \# g-Speicherzugriffe \# durch diesen Thread ausgeführt werden.

Dies gilt für den g shared memory der aktuellen \# Threadgruppe.

\_g ist nur im Compute-Shader verfügbar.

### <a name="_t"></a>\_t

Threadgruppensynchronisierung. Alle Threads innerhalb einer einzelnen Threadgruppe (die den Zugriff auf einen gemeinsamen Satz freigegebener Registerspeicherplatz gemeinsam verwenden können) werden bis zu dem Punkt ausgeführt, an dem sie diese Anweisung erreichen, bevor ein Thread fortgesetzt werden kann.

\_t kann nicht in der dynamischen Flusssteuerung platziert werden (Verzweigungen, die innerhalb einer Threadgruppe variieren können), kann aber in einer einheitlichen Flusssteuerung vorhanden sein, bei der alle Threads in der Gruppe denselben Pfad auswählen.

\_t ist nur im Compute-Shader verfügbar.

Im Folgenden finden Sie eine Liste der Compute-Shader-Synchronisierungsvarianten.

-   sync \_ g
-   sync \_ ugroup\*
-   sync \_ uglobal
-   sync \_ g \_ t
-   sync \_ ugroup \_ t\*
-   sync \_ uglobal \_ t
-   sync \_ ugroup \_ g\*
-   sync \_ uglobal \_ g
-   sync \_ ugroup \_ g \_ t\*
-   sync \_ uglobal \_ g \_ t

\*Varianten mit ugroup werden möglicherweise nicht vom HLSL-Compiler als Ziel verwendet, wie weiter oben im \_ \_ Abschnitt ugroup erläutert.

Die Liste der Pixel-Shader-Synchronisierungsvarianten umfasst nur \_ sync uglobal.

Arbeitsspeichergrenzen verhindern, dass betroffene Anweisungen von Compilern oder Hardware über den Fence hinweg neu angeordnet werden.

Mehrere Lesevorgänge von derselben Adresse durch einen Shaderaufruf, die nicht durch Speicherbarrieren getrennt sind, oder Schreibvorgänge in die Adresse können zusammen reduziert werden. Gleiches gilt für Schreibvorgänge. Durch eine Barriere getrennte Zugriffe können nicht zusammengeführt oder über die Barriere verschoben werden.

Arbeitsspeicher-Fences sind nicht erforderlich, damit atomarer Betrieb an einer bestimmten Adresse durch verschiedene Threads ordnungsgemäß funktioniert. Fences sind erforderlich, wenn Atomar- und/oder Lade-/Speichervorgänge in Bezug aufeinander synchronisiert werden müssen, wie sie aus Sicht anderer Threads in einzelnen Threads angezeigt werden.

Im Pixel-Shader [](discard--sm4---asm-.md) implizieren Verwerfensanweisungen einen uglobalen Synchronisierungs-Fence, da Anweisungen nicht über die \_ verwerfende neu angeordnet **werden können.** Sync uglobal in Hilfspixeln (die nur zur Unterstützung von Ableitungen ausgeführt werden) oder verworfene Pixel haben möglicherweise \_ keine Auswirkungen. Es ist nicht zulässig, dass Hilfs- oder verworfene Pixel in UAVs schreiben, wenn im Fall eines Verwerfens die Schreibvorgänge nach dem Verwerfen ausgegeben werden. Zurückgegebene Werte von UAVs dürfen nicht zu abgeleiteten Berechnungen beitragen. Daher wird angegeben, ob die Synchronisierung von u bei Hilfspixeln oder bei der Synchronisierung nach einem \_ Verwerfen nicht mehr wichtig ist.

cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützen diese Anweisung.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shaderstufen für Direct3D 11.1 verfügbar sind, gilt die Synchronisierungs-Uglobal-Variante dieser Anweisung für alle Shaderstufen für die Direct3D 11.1-Runtime, die ab Windows 8. **\_**



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

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

 

 




