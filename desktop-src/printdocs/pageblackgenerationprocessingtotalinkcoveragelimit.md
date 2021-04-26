---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29918bfe48d1547a3c61b8d79425b36368f6d249
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993877"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="5fb2b-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="5fb2b-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="5fb2b-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5fb2b-105">This topic is not current.</span></span> <span data-ttu-id="5fb2b-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="5fb2b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5fb2b-107">Gibt die maximal zulässige Summe der vier Ink-Abdeckungen an einer beliebigen Stelle in einem Bild an.</span><span class="sxs-lookup"><span data-stu-id="5fb2b-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="5fb2b-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5fb2b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5fb2b-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="5fb2b-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5fb2b-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5fb2b-110">Element Information</span></span>



| <span data-ttu-id="5fb2b-111">Name</span><span class="sxs-lookup"><span data-stu-id="5fb2b-111">Name</span></span> | <span data-ttu-id="5fb2b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb2b-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="5fb2b-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="5fb2b-113">Element Type</span></span> <br/>   | <span data-ttu-id="5fb2b-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5fb2b-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="5fb2b-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="5fb2b-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5fb2b-116">Seite</span><span class="sxs-lookup"><span data-stu-id="5fb2b-116">Page</span></span><br/>                                            |
| <span data-ttu-id="5fb2b-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5fb2b-117">Notes</span></span> <br/>          | <span data-ttu-id="5fb2b-118">Verknüpft mit dem PageBlackGenerationProcessing-Element</span><span class="sxs-lookup"><span data-stu-id="5fb2b-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5fb2b-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="5fb2b-119">Structure Content</span></span>

<span data-ttu-id="5fb2b-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="5fb2b-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="5fb2b-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="5fb2b-121">Structure Properties</span></span>

<span data-ttu-id="5fb2b-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5fb2b-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5fb2b-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5fb2b-123">Property</span></span>                | <span data-ttu-id="5fb2b-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5fb2b-124">xsi:type</span></span>           | <span data-ttu-id="5fb2b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb2b-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5fb2b-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5fb2b-126">DataType</span></span><br/>     | <span data-ttu-id="5fb2b-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5fb2b-127">string</span></span><br/>  | <span data-ttu-id="5fb2b-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5fb2b-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="5fb2b-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5fb2b-129">DefaultValue</span></span><br/> | <span data-ttu-id="5fb2b-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5fb2b-130">string</span></span><br/>  | <span data-ttu-id="5fb2b-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="5fb2b-131">undefined</span></span><br/>       |
| <span data-ttu-id="5fb2b-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5fb2b-132">MaxValue</span></span><br/>     | <span data-ttu-id="5fb2b-133">integer</span><span class="sxs-lookup"><span data-stu-id="5fb2b-133">integer</span></span><br/> | <span data-ttu-id="5fb2b-134">400</span><span class="sxs-lookup"><span data-stu-id="5fb2b-134">400</span></span><br/>             |
| <span data-ttu-id="5fb2b-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="5fb2b-135">MinValue</span></span><br/>     | <span data-ttu-id="5fb2b-136">integer</span><span class="sxs-lookup"><span data-stu-id="5fb2b-136">integer</span></span><br/> | <span data-ttu-id="5fb2b-137">200</span><span class="sxs-lookup"><span data-stu-id="5fb2b-137">200</span></span><br/>             |
| <span data-ttu-id="5fb2b-138">Mehrere</span><span class="sxs-lookup"><span data-stu-id="5fb2b-138">Multiple</span></span><br/>     | <span data-ttu-id="5fb2b-139">integer</span><span class="sxs-lookup"><span data-stu-id="5fb2b-139">integer</span></span><br/> | <span data-ttu-id="5fb2b-140">1</span><span class="sxs-lookup"><span data-stu-id="5fb2b-140">1</span></span><br/>               |
| <span data-ttu-id="5fb2b-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="5fb2b-141">Mandatory</span></span><br/>    | <span data-ttu-id="5fb2b-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5fb2b-142">string</span></span><br/>  | <span data-ttu-id="5fb2b-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="5fb2b-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5fb2b-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="5fb2b-144">UnitType</span></span><br/>     | <span data-ttu-id="5fb2b-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5fb2b-145">string</span></span><br/>  | <span data-ttu-id="5fb2b-146">Prozent</span><span class="sxs-lookup"><span data-stu-id="5fb2b-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5fb2b-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5fb2b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fb2b-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="5fb2b-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




