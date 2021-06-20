---
description: ScoredProperty-Instanzen können auch in anderen ScoredProperty-Instanzen oder als untergeordnete Elemente einer Optionsinstanz geschachtelt werden.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Geschachtelte ScoredProperty-Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a80d291fa59b2f36191f42b2f99ea9d22789a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408603"
---
# <a name="nested-scoredproperty-instances"></a><span data-ttu-id="11dfe-103">Geschachtelte ScoredProperty-Instanzen</span><span class="sxs-lookup"><span data-stu-id="11dfe-103">Nested ScoredProperty Instances</span></span>

<span data-ttu-id="11dfe-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="11dfe-104">This topic is not current.</span></span> <span data-ttu-id="11dfe-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="11dfe-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="11dfe-106">Beachten Sie, dass Sie nicht auf das Hinzufügen von ScoredProperty-Instanzen als untergeordnete Elemente einer Optionsinstanz beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="11dfe-106">Notice that you are not restricted to adding ScoredProperty instances as child elements of an Option instance.</span></span> <span data-ttu-id="11dfe-107">ScoredProperty-Instanzen können auch in anderen ScoredProperty-Instanzen geschachtelt sein.</span><span class="sxs-lookup"><span data-stu-id="11dfe-107">ScoredProperty instances may also be nested within other ScoredProperty instances.</span></span> <span data-ttu-id="11dfe-108">Dies ist nützlich, wenn eine Geräteeigenschaft komplex ist und am besten durch mehrere Untereigenschaften dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="11dfe-108">This is useful when a device property is complex and is best represented by multiple subproperties.</span></span> <span data-ttu-id="11dfe-109">Das Hinzufügen von Untereigenschaften zu einer vorhandenen (oder öffentlichen) Eigenschaft oder ScoredProperty ist eine gute Möglichkeit, eine Option zu verbessern und gleichzeitig die Portabilität mit vorhandenen Optionsinstanzen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="11dfe-109">Adding subproperties to an existing (or public) Property or ScoredProperty is a good way to enhance an Option, while retaining portability with existing Option instances.</span></span> <span data-ttu-id="11dfe-110">Beispielsweise enthalten die Standardoption-Instanzen für das MediaType-Feature eine ScoredProperty, die die Gewichtung der Medien als Light, Medium, Heavy oder ExtraHeavy beschreibt.</span><span class="sxs-lookup"><span data-stu-id="11dfe-110">For example, the standard Option instances for the MediaType Feature contain a ScoredProperty describing the weight of the media as Light, Medium, Heavy, or ExtraHeavy.</span></span> <span data-ttu-id="11dfe-111">Wenn Sie genauere Beschreibungen der Gewichtung wünschen, können Sie eine Untereigenschaften (Im folgenden Beispiel "GramsPer100Sheets") hinzufügen, die das tatsächliche Gewicht (in Grammen) von 100 Medienblättern enthält.</span><span class="sxs-lookup"><span data-stu-id="11dfe-111">If you want more precise descriptions of the weight, you can add a subproperty (GramsPer100Sheets in the following example) that contains the actual weight (in grams) of 100 sheets of media.</span></span> <span data-ttu-id="11dfe-112">Die erweiterte Option könnte wie im folgenden Beispiel aussehen.</span><span class="sxs-lookup"><span data-stu-id="11dfe-112">The enhanced Option might look like the following example.</span></span>

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

<span data-ttu-id="11dfe-113">Ein Vergleich der ursprünglichen und erweiterten Option-Instanzen erzeugt eine nahezu perfekte Übereinstimmung, da die erweiterte Option eine Obermenge des Originals ist und die Speicherorte und Werte der einzelnen ursprünglichen ScoredProperty-Instanzen beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="11dfe-113">A comparison of the original and enhanced Option instances produces a near-perfect match, because the enhanced Option is a superset of the original, and the locations and values of each of the original ScoredProperty instances is preserved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11dfe-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11dfe-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11dfe-115">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="11dfe-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



