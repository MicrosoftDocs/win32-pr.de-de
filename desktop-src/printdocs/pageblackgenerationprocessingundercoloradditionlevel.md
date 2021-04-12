---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: "\"Pgeblackgenerationprocessingundercoloradditionlevel\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fb6866dae4eb4a39de5c2b3b5d678a7388d703
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219079"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="b1d34-104">"Pgeblackgenerationprocessingundercoloradditionlevel"</span><span class="sxs-lookup"><span data-stu-id="b1d34-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="b1d34-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b1d34-105">This topic is not current.</span></span> <span data-ttu-id="b1d34-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b1d34-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b1d34-107">Beschreibt die Menge an chromatischen Freihand (in grauen Komponenten Verhältnissen), um Bereiche hinzuzufügen, in denen GCR/UCR "blackinklimit" (oder ggf. ucastart) in den dunklen und in nahezu neutralen Bereichen generiert hat.</span><span class="sxs-lookup"><span data-stu-id="b1d34-107">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="b1d34-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b1d34-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b1d34-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b1d34-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b1d34-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b1d34-110">Element Information</span></span>



| <span data-ttu-id="b1d34-111">Name</span><span class="sxs-lookup"><span data-stu-id="b1d34-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="b1d34-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="b1d34-112">Element Type</span></span> <br/>   | <span data-ttu-id="b1d34-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b1d34-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="b1d34-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="b1d34-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b1d34-115">Seite</span><span class="sxs-lookup"><span data-stu-id="b1d34-115">Page</span></span><br/>                                            |
| <span data-ttu-id="b1d34-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1d34-116">Notes</span></span> <br/>          | <span data-ttu-id="b1d34-117">Verknüpft mit dem Element "pgeblackgenerationprocessing"</span><span class="sxs-lookup"><span data-stu-id="b1d34-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b1d34-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b1d34-118">Structure Content</span></span>

<span data-ttu-id="b1d34-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="b1d34-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="b1d34-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1d34-120">Structure Properties</span></span>

<span data-ttu-id="b1d34-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b1d34-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b1d34-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b1d34-122">Property</span></span>                | <span data-ttu-id="b1d34-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b1d34-123">xsi:type</span></span>           | <span data-ttu-id="b1d34-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b1d34-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b1d34-125">DataType</span><span class="sxs-lookup"><span data-stu-id="b1d34-125">DataType</span></span><br/>     | <span data-ttu-id="b1d34-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b1d34-126">string</span></span><br/>  | <span data-ttu-id="b1d34-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b1d34-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="b1d34-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b1d34-128">DefaultValue</span></span><br/> | <span data-ttu-id="b1d34-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b1d34-129">string</span></span><br/>  | <span data-ttu-id="b1d34-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b1d34-130">undefined</span></span><br/>       |
| <span data-ttu-id="b1d34-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b1d34-131">MaxValue</span></span><br/>     | <span data-ttu-id="b1d34-132">integer</span><span class="sxs-lookup"><span data-stu-id="b1d34-132">integer</span></span><br/> | <span data-ttu-id="b1d34-133">100</span><span class="sxs-lookup"><span data-stu-id="b1d34-133">100</span></span><br/>             |
| <span data-ttu-id="b1d34-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="b1d34-134">MinValue</span></span><br/>     | <span data-ttu-id="b1d34-135">integer</span><span class="sxs-lookup"><span data-stu-id="b1d34-135">integer</span></span><br/> | <span data-ttu-id="b1d34-136">0</span><span class="sxs-lookup"><span data-stu-id="b1d34-136">0</span></span><br/>               |
| <span data-ttu-id="b1d34-137">Mehrere</span><span class="sxs-lookup"><span data-stu-id="b1d34-137">Multiple</span></span><br/>     | <span data-ttu-id="b1d34-138">integer</span><span class="sxs-lookup"><span data-stu-id="b1d34-138">integer</span></span><br/> | <span data-ttu-id="b1d34-139">1</span><span class="sxs-lookup"><span data-stu-id="b1d34-139">1</span></span><br/>               |
| <span data-ttu-id="b1d34-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="b1d34-140">Mandatory</span></span><br/>    | <span data-ttu-id="b1d34-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b1d34-141">string</span></span><br/>  | <span data-ttu-id="b1d34-142">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="b1d34-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b1d34-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="b1d34-143">UnitType</span></span><br/>     | <span data-ttu-id="b1d34-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b1d34-144">string</span></span><br/>  | <span data-ttu-id="b1d34-145">Prozent</span><span class="sxs-lookup"><span data-stu-id="b1d34-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b1d34-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b1d34-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1d34-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="b1d34-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




