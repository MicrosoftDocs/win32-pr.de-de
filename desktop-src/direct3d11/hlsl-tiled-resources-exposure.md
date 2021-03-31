---
title: Verfügbar machen von HLSL-Kacheln
description: Die neue Syntax von Microsoft High Level Shader Language (HLSL) ist erforderlich, um gekachelte Ressourcen in Shader-Modell 5 zu unterstützen.
ms.assetid: B6CE51E6-1BA9-4D15-9654-86FE9BAAF585
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b266b98045b38645e1e8d24ed0014a5f448a38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473604"
---
# <a name="hlsl-tiled-resources-exposure"></a>Verfügbar machen von HLSL-Kacheln

Die neue Syntax von Microsoft High Level Shader Language (HLSL) ist erforderlich, um gekachelte Ressourcen in [Shader-Modell 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)zu unterstützen.

Die neue HLSL-Syntax ist nur auf Geräten mit Unterstützung für gekachelte Ressourcen zulässig. Jede relevante HLSL-Methode für die gekachelten Ressourcen in der folgenden Tabelle akzeptiert entweder eine (Feedback) oder zwei (in dieser Reihenfolge eine Klammer und Feedback) zusätzliche optionale Parameter. Beispielsweise ist eine **Beispiel** Methode wie folgt:

**Sample (Sampler, Location \[ , Offset \[ , Clamp \[ , Feedback \] \] \] )**

Ein Beispiel für eine **Beispiel Methode** ist [**Texture2D. Sample (S, float, int, float, uint)**](/windows/desktop/direct3dhlsl/t2darray-sample-s-float-int-float-uint-).

Die Offset-, Clamp-und Feedback-Parameter sind optional. Sie müssen alle optionalen Parameter angeben, die Sie benötigen. Dies entspricht den C++-Regeln für Standard Funktionsargumente. Wenn der Feedback Status z. b. erforderlich ist, müssen sowohl Offset-als auch Klammer Parameter explizit für **Stichproben** bereitgestellt werden, auch wenn Sie möglicherweise nicht logisch benötigt werden.

Der Klammer Parameter ist ein skalarer float-Wert. Der Literalwert von Clamp = 0,0 f gibt an, dass der Klammer Vorgang nicht ausgeführt wird.

Der Feedback Parameter ist eine **uint** -Variable, die Sie der systeminternen [**checkaccessfullymapping**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) -Funktion für den Speicherzugriff zur Abfrage bereitstellen können. Der Wert des Parameters "Feedback" darf nicht geändert oder interpretiert werden. der Compiler bietet jedoch keine erweiterte Analyse und Diagnose, um zu ermitteln, ob Sie den Wert geändert haben.

Dies ist die Syntax von [**checkaccessfullymapping**](/windows/desktop/direct3dhlsl/checkaccessfullymapped):

**bool checkaccessfullymapping (in uint feedbackvar);**

[**Checkaccessfullymapping**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpretiert den Wert von *feedbackvar* und gibt true zurück, wenn alle Daten, auf die zugegriffen wird, in der Ressource zugeordnet wurden. Andernfalls gibt **checkaccessfullymapping** den Wert false zurück.

Wenn entweder der Parameter "Clamp" oder "Feedback" vorhanden ist, gibt der Compiler eine Variante der Grund Anweisung aus. Beispielsweise generiert Sample einer gekachelten Ressource die- `sample_cl_s` Anweisung. Wenn weder "Clamp" noch "Feedback" angegeben ist, gibt der Compiler die grundlegende Anweisung aus, sodass es keine Änderung des aktuellen Verhaltens gibt. Der Klammer Wert von 0,0 f gibt an, dass keine Klammer ausgeführt wird. Daher kann der Treiber Compiler die Anweisung weiter an die Zielhardware anpassen. Wenn Feedback ein NULL-Register in einer Anweisung ist, wird das Feedback nicht verwendet. Daher kann der Treiber Compiler die Anweisung weiter an die Zielarchitektur anpassen.

Wenn der HLSL-Compiler diese Klammer als 0,0 f ausgibt und Feedback nicht verwendet wird, gibt der Compiler die entsprechende Grund Anweisung aus (z `sample` . b `sample_cl_s` . anstelle von).

Wenn ein gekachelter Ressourcen Zugriff aus mehreren einzelnen Anweisungen für den Byte Code besteht (z. b. bei strukturierten Ressourcen), aggregiert der Compiler einzelne Feedback Werte über den Vorgang oder, um den endgültigen Feedback Wert zu erhalten. Aus diesem Grund wird ein einzelner Feedback Wert für einen solchen komplexen Zugriff angezeigt.

Dies ist die Zusammenfassungs Tabelle der HLSL-Methoden, die zur Unterstützung von Feedback und/oder der Klammer geändert werden. Diese Vorgänge funktionieren bei Kacheln und nicht gekachelten Ressourcen aller Dimensionen. Nicht gekachelte Ressourcen scheinen immer vollständig zugeordnet zu sein.



| [HLSL-Objekte](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5-objects)                                                                                                                                                                                                                                | Intrinsische Methoden mit der Option "Feedback" ( \* ): auch die Option "Klemme"                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[RW \] Texture2D<br/> \[RW \] Texture2DArray<br/> Texturecube<br/> Texturecubearray<br/>                                                                                                                                                                                    | Informieren<br/> Gatherred<br/> Gathergrün<br/> Gatherblue<br/> Gatheralpha<br/> Gathercmp<br/> Gathercmpred<br/> Gathercmpgreen<br/> Gathercmpblue<br/> Gathercmpalpha<br/> |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[RW \] Texture2D<br/> \[RW \] Texture2DArray<br/> \[RW \] Texture3D<br/> Texturecube<br/> Texturecubearray<br/>                                                                                              | Beispiel\*<br/> Samplebias\*<br/> Samplecmp\*<br/> Samplecmplevelzero<br/> Samplegrad\*<br/> Samplelevel<br/>                                                                                      |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[RW \] Texture2D<br/> Texture2DMS<br/> \[RW \] Texture2DArray<br/> Texture2DArrayMS<br/> \[RW \] Texture3D<br/> \[RW- \] Puffer<br/> \[RW- \] byteaddressbuffer<br/> \[RW \] structuredbuffer<br/> | Laden                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipeline Zugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

