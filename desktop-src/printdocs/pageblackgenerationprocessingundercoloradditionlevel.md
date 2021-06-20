---
description: Hier erfahren Sie mehr über das PageBlackGenerationProcessingUnderColorAdditionLevel-Element, das die Menge der freizugebenden Freihand in Bereichen mit BlackInkLimit beschreibt.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b496fbe890f53d1da8d1054cc5a19fe6318811
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408413"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="4736c-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="4736c-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="4736c-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4736c-104">This topic is not current.</span></span> <span data-ttu-id="4736c-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="4736c-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4736c-106">Beschreibt die Menge an freihandfarbener Freihand (in grauen Komponentenverhältnissen), die Bereichen hinzugefügt werden soll, in denen GCR/UCR "BlackInkLimit" (oder , falls angegeben), in den dunklen Neutralen und nahezu neutralen Bereichen generiert hat.</span><span class="sxs-lookup"><span data-stu-id="4736c-106">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="4736c-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4736c-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4736c-108">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4736c-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4736c-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4736c-109">Element Information</span></span>



| <span data-ttu-id="4736c-110">Name</span><span class="sxs-lookup"><span data-stu-id="4736c-110">Name</span></span> | <span data-ttu-id="4736c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="4736c-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="4736c-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4736c-112">Element Type</span></span> <br/>   | <span data-ttu-id="4736c-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4736c-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="4736c-114">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="4736c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4736c-115">Seite</span><span class="sxs-lookup"><span data-stu-id="4736c-115">Page</span></span><br/>                                            |
| <span data-ttu-id="4736c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4736c-116">Notes</span></span> <br/>          | <span data-ttu-id="4736c-117">Verknüpft mit dem PageBlackGenerationProcessing-Element</span><span class="sxs-lookup"><span data-stu-id="4736c-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4736c-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4736c-118">Structure Content</span></span>

<span data-ttu-id="4736c-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="4736c-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="4736c-120">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="4736c-120">Structure Properties</span></span>

<span data-ttu-id="4736c-121">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4736c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4736c-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4736c-122">Property</span></span>                | <span data-ttu-id="4736c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4736c-123">xsi:type</span></span>           | <span data-ttu-id="4736c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4736c-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4736c-125">DataType</span><span class="sxs-lookup"><span data-stu-id="4736c-125">DataType</span></span><br/>     | <span data-ttu-id="4736c-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4736c-126">string</span></span><br/>  | <span data-ttu-id="4736c-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4736c-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="4736c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4736c-128">DefaultValue</span></span><br/> | <span data-ttu-id="4736c-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4736c-129">string</span></span><br/>  | <span data-ttu-id="4736c-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4736c-130">undefined</span></span><br/>       |
| <span data-ttu-id="4736c-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4736c-131">MaxValue</span></span><br/>     | <span data-ttu-id="4736c-132">integer</span><span class="sxs-lookup"><span data-stu-id="4736c-132">integer</span></span><br/> | <span data-ttu-id="4736c-133">100</span><span class="sxs-lookup"><span data-stu-id="4736c-133">100</span></span><br/>             |
| <span data-ttu-id="4736c-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="4736c-134">MinValue</span></span><br/>     | <span data-ttu-id="4736c-135">integer</span><span class="sxs-lookup"><span data-stu-id="4736c-135">integer</span></span><br/> | <span data-ttu-id="4736c-136">0</span><span class="sxs-lookup"><span data-stu-id="4736c-136">0</span></span><br/>               |
| <span data-ttu-id="4736c-137">Mehrere</span><span class="sxs-lookup"><span data-stu-id="4736c-137">Multiple</span></span><br/>     | <span data-ttu-id="4736c-138">integer</span><span class="sxs-lookup"><span data-stu-id="4736c-138">integer</span></span><br/> | <span data-ttu-id="4736c-139">1</span><span class="sxs-lookup"><span data-stu-id="4736c-139">1</span></span><br/>               |
| <span data-ttu-id="4736c-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="4736c-140">Mandatory</span></span><br/>    | <span data-ttu-id="4736c-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4736c-141">string</span></span><br/>  | <span data-ttu-id="4736c-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="4736c-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4736c-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="4736c-143">UnitType</span></span><br/>     | <span data-ttu-id="4736c-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4736c-144">string</span></span><br/>  | <span data-ttu-id="4736c-145">Prozent</span><span class="sxs-lookup"><span data-stu-id="4736c-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4736c-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4736c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4736c-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="4736c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




