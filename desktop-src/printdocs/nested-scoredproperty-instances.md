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
# <a name="nested-scoredproperty-instances"></a><span data-ttu-id="54418-104">Geschsted ScoredProperty-Instanzen</span><span class="sxs-lookup"><span data-stu-id="54418-104">Nested ScoredProperty Instances</span></span>

<span data-ttu-id="54418-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="54418-105">This topic is not current.</span></span> <span data-ttu-id="54418-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="54418-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="54418-107">Beachten Sie, dass Sie nicht auf das Hinzufügen von ScoredProperty-Instanzen als untergeordnete Elemente einer Options Instanz beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="54418-107">Notice that you are not restricted to adding ScoredProperty instances as child elements of an Option instance.</span></span> <span data-ttu-id="54418-108">ScoredProperty-Instanzen können auch in anderen ScoredProperty-Instanzen geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="54418-108">ScoredProperty instances may also be nested within other ScoredProperty instances.</span></span> <span data-ttu-id="54418-109">Dies ist nützlich, wenn eine Geräte Eigenschaft Komplex ist und am besten durch mehrere unter Eigenschaften repräsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="54418-109">This is useful when a device property is complex and is best represented by multiple subproperties.</span></span> <span data-ttu-id="54418-110">Das Hinzufügen von untergeordneten Eigenschaften zu einer vorhandenen (oder öffentlichen) Eigenschaft oder ScoredProperty ist eine gute Möglichkeit, um eine Option zu verbessern und gleichzeitig die Portabilität mit Instanzen vorhandener Optionen beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="54418-110">Adding subproperties to an existing (or public) Property or ScoredProperty is a good way to enhance an Option, while retaining portability with existing Option instances.</span></span> <span data-ttu-id="54418-111">Beispielsweise enthalten die Standard-Options Instanzen für das MediaType-Feature eine ScoredProperty, die die Gewichtung der Medien als hell, Mittel, stark oder extra stark beschreibt.</span><span class="sxs-lookup"><span data-stu-id="54418-111">For example, the standard Option instances for the MediaType Feature contain a ScoredProperty describing the weight of the media as Light, Medium, Heavy, or ExtraHeavy.</span></span> <span data-ttu-id="54418-112">Wenn Sie genauere Beschreibungen der Gewichtung möchten, können Sie eine untergeordnete Eigenschaft (GramsPer100Sheets im folgenden Beispiel) hinzufügen, die die tatsächliche Gewichtung (in grams) von 100-Zeichen in Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="54418-112">If you want more precise descriptions of the weight, you can add a subproperty (GramsPer100Sheets in the following example) that contains the actual weight (in grams) of 100 sheets of media.</span></span> <span data-ttu-id="54418-113">Die Option erweitert könnte wie im folgenden Beispiel aussehen.</span><span class="sxs-lookup"><span data-stu-id="54418-113">The enhanced Option might look like the following example.</span></span>

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

<span data-ttu-id="54418-114">Ein Vergleich der ursprünglichen und erweiterten Options Instanzen erzeugt eine nahezu perfekte Entsprechung, da die erweiterte Option eine supermenge der ursprünglichen ist, und die Speicherorte und Werte der einzelnen ursprünglichen ScoredProperty-Instanzen bleiben erhalten.</span><span class="sxs-lookup"><span data-stu-id="54418-114">A comparison of the original and enhanced Option instances produces a near-perfect match, because the enhanced Option is a superset of the original, and the locations and values of each of the original ScoredProperty instances is preserved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54418-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54418-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54418-116">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="54418-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



