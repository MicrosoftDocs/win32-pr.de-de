---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b43d8d9ee366fc742dc3d7b1617f6297fc96e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995667"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="18953-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="18953-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="18953-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="18953-105">This topic is not current.</span></span> <span data-ttu-id="18953-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="18953-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="18953-107">Beschreibt die Menge an roter Freifläche (in grauen Komponentenverhältnisse), die Bereichen hinzugefügt werden soll, in denen GCR/UCR "BlackInkLimit" (oder UKAStart, falls angegeben) in den dunkelneutralen und nahezu neutralen Bereichen generiert hat.</span><span class="sxs-lookup"><span data-stu-id="18953-107">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="18953-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="18953-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="18953-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="18953-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="18953-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="18953-110">Element Information</span></span>



| <span data-ttu-id="18953-111">Name</span><span class="sxs-lookup"><span data-stu-id="18953-111">Name</span></span> | <span data-ttu-id="18953-112">Wert</span><span class="sxs-lookup"><span data-stu-id="18953-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="18953-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="18953-113">Element Type</span></span> <br/>   | <span data-ttu-id="18953-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="18953-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="18953-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="18953-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="18953-116">Seite</span><span class="sxs-lookup"><span data-stu-id="18953-116">Page</span></span><br/>                                            |
| <span data-ttu-id="18953-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="18953-117">Notes</span></span> <br/>          | <span data-ttu-id="18953-118">Mit PageBlackGenerationProcessing-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="18953-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="18953-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="18953-119">Structure Content</span></span>

<span data-ttu-id="18953-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="18953-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="18953-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="18953-121">Structure Properties</span></span>

<span data-ttu-id="18953-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="18953-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="18953-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="18953-123">Property</span></span>                | <span data-ttu-id="18953-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="18953-124">xsi:type</span></span>           | <span data-ttu-id="18953-125">Wert</span><span class="sxs-lookup"><span data-stu-id="18953-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="18953-126">DataType</span><span class="sxs-lookup"><span data-stu-id="18953-126">DataType</span></span><br/>     | <span data-ttu-id="18953-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18953-127">string</span></span><br/>  | <span data-ttu-id="18953-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="18953-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="18953-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="18953-129">DefaultValue</span></span><br/> | <span data-ttu-id="18953-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18953-130">string</span></span><br/>  | <span data-ttu-id="18953-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="18953-131">undefined</span></span><br/>       |
| <span data-ttu-id="18953-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="18953-132">MaxValue</span></span><br/>     | <span data-ttu-id="18953-133">integer</span><span class="sxs-lookup"><span data-stu-id="18953-133">integer</span></span><br/> | <span data-ttu-id="18953-134">100</span><span class="sxs-lookup"><span data-stu-id="18953-134">100</span></span><br/>             |
| <span data-ttu-id="18953-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="18953-135">MinValue</span></span><br/>     | <span data-ttu-id="18953-136">integer</span><span class="sxs-lookup"><span data-stu-id="18953-136">integer</span></span><br/> | <span data-ttu-id="18953-137">0</span><span class="sxs-lookup"><span data-stu-id="18953-137">0</span></span><br/>               |
| <span data-ttu-id="18953-138">Mehrere</span><span class="sxs-lookup"><span data-stu-id="18953-138">Multiple</span></span><br/>     | <span data-ttu-id="18953-139">integer</span><span class="sxs-lookup"><span data-stu-id="18953-139">integer</span></span><br/> | <span data-ttu-id="18953-140">1</span><span class="sxs-lookup"><span data-stu-id="18953-140">1</span></span><br/>               |
| <span data-ttu-id="18953-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="18953-141">Mandatory</span></span><br/>    | <span data-ttu-id="18953-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18953-142">string</span></span><br/>  | <span data-ttu-id="18953-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="18953-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="18953-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="18953-144">UnitType</span></span><br/>     | <span data-ttu-id="18953-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="18953-145">string</span></span><br/>  | <span data-ttu-id="18953-146">Prozent</span><span class="sxs-lookup"><span data-stu-id="18953-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="18953-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18953-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18953-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="18953-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




