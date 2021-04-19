---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Geschsted ScoredProperty-Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1bfed09c48bc0ac6e93e09f96dc8116e8b0a91
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355113"
---
# <a name="nested-scoredproperty-instances"></a>Geschsted ScoredProperty-Instanzen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Beachten Sie, dass Sie nicht auf das Hinzufügen von ScoredProperty-Instanzen als untergeordnete Elemente einer Options Instanz beschränkt sind. ScoredProperty-Instanzen können auch in anderen ScoredProperty-Instanzen geschachtelt werden. Dies ist nützlich, wenn eine Geräte Eigenschaft Komplex ist und am besten durch mehrere unter Eigenschaften repräsentiert wird. Das Hinzufügen von untergeordneten Eigenschaften zu einer vorhandenen (oder öffentlichen) Eigenschaft oder ScoredProperty ist eine gute Möglichkeit, um eine Option zu verbessern und gleichzeitig die Portabilität mit Instanzen vorhandener Optionen beizubehalten. Beispielsweise enthalten die Standard-Options Instanzen für das MediaType-Feature eine ScoredProperty, die die Gewichtung der Medien als hell, Mittel, stark oder extra stark beschreibt. Wenn Sie genauere Beschreibungen der Gewichtung möchten, können Sie eine untergeordnete Eigenschaft (GramsPer100Sheets im folgenden Beispiel) hinzufügen, die die tatsächliche Gewichtung (in grams) von 100-Zeichen in Zeichen enthält. Die Option erweitert könnte wie im folgenden Beispiel aussehen.

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

Ein Vergleich der ursprünglichen und erweiterten Options Instanzen erzeugt eine nahezu perfekte Entsprechung, da die erweiterte Option eine supermenge der ursprünglichen ist, und die Speicherorte und Werte der einzelnen ursprünglichen ScoredProperty-Instanzen bleiben erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



