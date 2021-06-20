---
description: Erfahren Sie mehr über das Verweisen auf Parameter und das ParameterDef-Element. Ein Beispiel für eine Option, die ein ParameterRef-Element enthält, ist die Option für die benutzerdefinierte Mediengröße.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Verweisen auf Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650790af5ca6849bd082b4819dd4c411adea320f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405323"
---
# <a name="referencing-parameters"></a><span data-ttu-id="78ef8-104">Verweisen auf Parameter</span><span class="sxs-lookup"><span data-stu-id="78ef8-104">Referencing Parameters</span></span>

<span data-ttu-id="78ef8-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="78ef8-105">This topic is not current.</span></span> <span data-ttu-id="78ef8-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="78ef8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="78ef8-107">Ein konkretes Beispiel für eine Option, die ein ParameterRef-Element enthält, ist die Option für die benutzerdefinierte Mediengröße.</span><span class="sxs-lookup"><span data-stu-id="78ef8-107">A concrete example of an Option that includes a ParameterRef element is the custom media size Option.</span></span> <span data-ttu-id="78ef8-108">Beachten Sie, dass auf zwei Parameter verwiesen wird: PageMediaSizeMediaSizeWidth und PageMediaSizeMediaSizeHeight.</span><span class="sxs-lookup"><span data-stu-id="78ef8-108">Note that it references two parameters: PageMediaSizeMediaSizeWidth and PageMediaSizeMediaSizeHeight.</span></span> <span data-ttu-id="78ef8-109">Jede ParameterRef-Instanz verweist auf eine ParameterDef-Instanz, die an anderer Stelle im PrintCapabilities-Dokument definiert ist.</span><span class="sxs-lookup"><span data-stu-id="78ef8-109">Each ParameterRef instance refers to a ParameterDef instance that is defined elsewhere in the PrintCapabilities document.</span></span> <span data-ttu-id="78ef8-110">Informationen zum ParameterDef-Element finden Sie unter [ParameterDef.](parameterdef.md)</span><span class="sxs-lookup"><span data-stu-id="78ef8-110">For information about the ParameterDef element, see [ParameterDef](parameterdef.md).</span></span> <span data-ttu-id="78ef8-111">Konzeptionelle Informationen zum Definieren von Parametern finden Sie unter [ParameterDef und ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span><span class="sxs-lookup"><span data-stu-id="78ef8-111">For conceptual information about defining parameters, see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

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

<span data-ttu-id="78ef8-112">Lediglich das Erstellen einer parametrisierten Option reicht nicht aus, um sicherzustellen, dass die Option ordnungsgemäß behandelt und verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="78ef8-112">Merely creating a parameterized Option is not sufficient to ensure that the Option will be handled and processed correctly.</span></span> <span data-ttu-id="78ef8-113">Der PrintCapabilities/PrintTicket-Anbieter und -Clients müssen zusätzliche Unterstützung bereitstellen, um parametrisierte Optionsinstanzen ordnungsgemäß zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="78ef8-113">The PrintCapabilities/PrintTicket provider and clients must provide additional support to properly implement parameterized Option instances.</span></span> <span data-ttu-id="78ef8-114">Die erforderlichen Verhaltensweisen werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="78ef8-114">The required behaviors are described in the following sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78ef8-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78ef8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ef8-116">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="78ef8-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



