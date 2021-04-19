---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Verweis Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815ec7cd412e158a73e2b760f9f6080d7b0326a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106370362"
---
# <a name="referencing-parameters"></a><span data-ttu-id="5c4f2-104">Verweis Parameter</span><span class="sxs-lookup"><span data-stu-id="5c4f2-104">Referencing Parameters</span></span>

<span data-ttu-id="5c4f2-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5c4f2-105">This topic is not current.</span></span> <span data-ttu-id="5c4f2-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5c4f2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5c4f2-107">Ein konkretes Beispiel für eine Option, die ein ParameterRef-Element enthält, ist die Option für die benutzerdefinierte Mediengröße.</span><span class="sxs-lookup"><span data-stu-id="5c4f2-107">A concrete example of an Option that includes a ParameterRef element is the custom media size Option.</span></span> <span data-ttu-id="5c4f2-108">Beachten Sie, dass Sie auf zwei Parameter verweist: pagemediasizemediasizewidth und pagemediasizemediasizeheight.</span><span class="sxs-lookup"><span data-stu-id="5c4f2-108">Note that it references two parameters: PageMediaSizeMediaSizeWidth and PageMediaSizeMediaSizeHeight.</span></span> <span data-ttu-id="5c4f2-109">Jede ParameterRef-Instanz verweist auf eine ParameterDef-Instanz, die an anderer Stelle im printfunktionalitäten-Dokument definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5c4f2-109">Each ParameterRef instance refers to a ParameterDef instance that is defined elsewhere in the PrintCapabilities document.</span></span> <span data-ttu-id="5c4f2-110">Weitere Informationen zum ParameterDef-Element finden Sie unter [ParameterDef](parameterdef.md).</span><span class="sxs-lookup"><span data-stu-id="5c4f2-110">For information about the ParameterDef element, see [ParameterDef](parameterdef.md).</span></span> <span data-ttu-id="5c4f2-111">Konzeptionelle Informationen zum Definieren von Parametern finden Sie unter [ParameterDef-und parameterinit-Elemente](parameterdef-and-parameterinit-elements.md).</span><span class="sxs-lookup"><span data-stu-id="5c4f2-111">For conceptual information about defining parameters, see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

<span data-ttu-id="5c4f2-112">Das Erstellen einer parametrisierten Option ist nicht ausreichend, um sicherzustellen, dass die Option ordnungsgemäß behandelt und verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5c4f2-112">Merely creating a parameterized Option is not sufficient to ensure that the Option will be handled and processed correctly.</span></span> <span data-ttu-id="5c4f2-113">Der printfunktionalitäten/PrintTicket-Anbieter und die Clients müssen zusätzliche Unterstützung für die ordnungsgemäße Implementierung parametrisierter Options Instanzen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5c4f2-113">The PrintCapabilities/PrintTicket provider and clients must provide additional support to properly implement parameterized Option instances.</span></span> <span data-ttu-id="5c4f2-114">Die erforderlichen Verhalten werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5c4f2-114">The required behaviors are described in the following sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c4f2-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c4f2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c4f2-116">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="5c4f2-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



