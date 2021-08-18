---
title: HlSL-Kachelressourcen– Belichtung
description: Die neue HLSL-Syntax (High Level Shader Language) von Microsoft ist erforderlich, um gekachelte Ressourcen in Shader Model 5 zu unterstützen.
ms.assetid: B6CE51E6-1BA9-4D15-9654-86FE9BAAF585
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66ded502bebefc1061028115a12026f67c26cad89ddc57f98a5ae6fee923591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633330"
---
# <a name="hlsl-tiled-resources-exposure"></a>HlSL-Kachelressourcen– Belichtung

Die neue HLSL-Syntax (High Level Shader Language) von Microsoft ist erforderlich, um gekachelte Ressourcen in [Shader Model 5 zu unterstützen.](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)

Die neue HLSL-Syntax ist nur auf Geräten mit Unterstützung für gekachelte Ressourcen zulässig. Jede relevante HLSL-Methode für gekachelte Ressourcen in der folgenden Tabelle akzeptiert entweder einen (Feedback) oder zwei zusätzliche optionale Parameter (Klammer und Feedback in dieser Reihenfolge). Eine **Sample-Methode** ist beispielsweise:

**Sample(sampler, location \[ , offset , clamp , feedback \[ \[ \] \] \] )**

Ein Beispiel für eine **Sample-Methode** ist [**Texture2D.Sample(S,float,int,float,uint).**](/windows/desktop/direct3dhlsl/t2darray-sample-s-float-int-float-uint-)

Die Parameter offset, clamp und feedback sind optional. Sie müssen alle optionalen Parameter bis zu dem von Ihnen benötigten Parameter angeben, was mit den C++-Regeln für Standardfunktionsargumente konsistent ist. Wenn beispielsweise der Feedbackstatus benötigt wird, müssen sowohl offset- als auch clamp-Parameter explizit an **Sample** übergeben werden, auch wenn sie möglicherweise nicht logisch benötigt werden.

Der Klammerparameter ist ein float-Skalarwert. Der Literalwert von "clamp=0,0f" gibt an, dass der Klammervorgang nicht ausgeführt wird.

Der Feedbackparameter ist eine **uint-Variable,** die Sie für die systeminterne [**CheckAccessFullyMapped-Funktion**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) für Speicherzugriffsabfragen bereitstellen können. Sie dürfen den Wert des Feedbackparameters nicht ändern oder interpretieren. der Compiler stellt jedoch keine erweiterte Analyse und Diagnose zur Verfügung, um zu ermitteln, ob Sie den Wert geändert haben.

Dies ist die Syntax von [**CheckAccessFullyMapped:**](/windows/desktop/direct3dhlsl/checkaccessfullymapped)

**bool CheckAccessFullyMapped(in uint FeedbackVar);**

[**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpretiert den Wert von *FeedbackVar* und gibt TRUE zurück, wenn alle Daten, auf die zugegriffen wird, in der Ressource zugeordnet wurden. Andernfalls **gibt CheckAccessFullyMapped** false zurück.

Wenn entweder der Klammer- oder feedback-Parameter vorhanden ist, gibt der Compiler eine Variante der grundlegenden Anweisung aus. Beispiel für eine gekachelte Ressource generiert die `sample_cl_s` -Anweisung. Wenn weder Klammer noch Feedback angegeben wird, gibt der Compiler die grundlegende Anweisung aus, sodass keine Änderung des aktuellen Verhaltens vor sich geht. Der Klammerwert 0,0f gibt an, dass keine Klammer ausgeführt wird. Daher kann der Treibercompiler die Anweisung weiter an die Zielhardware anpassen. Wenn Feedback ein NULL-Register in einer Anweisung ist, wird das Feedback nicht verwendet. Daher kann der Treibercompiler die Anweisung weiter an die Zielarchitektur anpassen.

Wenn der HLSL-Compiler diese Klammer von 0,0f abzieht und Feedback nicht verwendet wird, gibt der Compiler die entsprechende grundlegende Anweisung aus (z. B. `sample` anstelle von `sample_cl_s` ).

Wenn der Zugriff auf eine kachelierte Ressource aus mehreren konstituierenden Bytecodeanweisungen besteht, z. B. für strukturierte Ressourcen, aggregiert der Compiler einzelne Feedbackwerte über den OR-Vorgang, um den endgültigen Feedbackwert zu erzeugen. Daher sehen Sie einen einzelnen Feedbackwert für einen so komplexen Zugriff.

Dies ist die Zusammenfassungstabelle der HLSL-Methoden, die geändert werden, um Feedback und/oder Klammer zu unterstützen. Diese arbeiten alle mit gekachelten und nicht gekachelten Ressourcen aller Dimensionen. Nicht gekachelte Ressourcen scheinen immer vollständig zugeordnet zu sein.



| [HLSL-Objekte](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5-objects)                                                                                                                                                                                                                                | Systeminterne Methoden mit Feedbackoption ( \* ) – verfügt auch über eine Klammeroption                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[RW \] Texture2D<br/> \[RW \] Texture2DArray<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                                                                                                                    | versammeln<br/> GatherRed<br/> GatherGreen<br/> GatherBlue<br/> GatherAlpha<br/> GatherCmp<br/> GatherCmpRed<br/> GatherCmpGreen<br/> GatherCmpBlue<br/> GatherCmpAlpha<br/> |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[RW \] Texture2D<br/> \[RW \] Texture2DArray<br/> \[RW \] Texture3D<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                              | Beispiel\*<br/> SampleBias\*<br/> SampleCmp\*<br/> SampleCmpLevelZero<br/> SampleGrad\*<br/> SampleLevel<br/>                                                                                      |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[RW \] Texture2D<br/> Texture2DMS<br/> \[RW \] Texture2DArray<br/> Texture2DArrayMS<br/> \[RW \] Texture3D<br/> \[\]RW-Puffer<br/> \[RW \] ByteAddressBuffer<br/> \[RW \] StructuredBuffer<br/> | Laden                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipelinezugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

