---
description: ScoredProperty-Instanzen können auch in anderen ScoredProperty-Instanzen oder als untergeordnete Elemente einer Optionsinstanz geschachtelt werden.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Geschachtelte ScoredProperty-Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0824e5645d723cdf3f0f45d985f3dd06b8c1b74de32fd2e47bb5843e37c2540f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099044"
---
# <a name="nested-scoredproperty-instances"></a>Geschachtelte ScoredProperty-Instanzen

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Beachten Sie, dass Sie nicht auf das Hinzufügen von ScoredProperty-Instanzen als untergeordnete Elemente einer Optionsinstanz beschränkt sind. ScoredProperty-Instanzen können auch in anderen ScoredProperty-Instanzen geschachtelt sein. Dies ist nützlich, wenn eine Geräteeigenschaft komplex ist und am besten durch mehrere Untereigenschaften dargestellt wird. Das Hinzufügen von Untereigenschaften zu einer vorhandenen (oder öffentlichen) Eigenschaft oder ScoredProperty ist eine gute Möglichkeit, eine Option zu verbessern und gleichzeitig die Portabilität mit vorhandenen Optionsinstanzen zu erhalten. Beispielsweise enthalten die Standardoption-Instanzen für das MediaType-Feature eine ScoredProperty, die die Gewichtung der Medien als Light, Medium, Heavy oder ExtraHeavy beschreibt. Wenn Sie genauere Beschreibungen der Gewichtung wünschen, können Sie eine Untereigenschaften (Im folgenden Beispiel "GramsPer100Sheets") hinzufügen, die das tatsächliche Gewicht (in Grammen) von 100 Medienblättern enthält. Die erweiterte Option könnte wie im folgenden Beispiel aussehen.

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

Ein Vergleich der ursprünglichen und erweiterten Option-Instanzen ergibt eine nahezu perfekte Übereinstimmung, da die erweiterte Option eine Obermenge des Originals ist und die Speicherorte und Werte der einzelnen ursprünglichen ScoredProperty-Instanzen beibehalten werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



