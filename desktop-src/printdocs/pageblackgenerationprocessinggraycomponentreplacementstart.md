---
description: Erfahren Sie mehr über das PageBlackGenerationProcessingGrayComponentReplacementStart-Element, das den Punkt beschreibt, an dem GCR beginnen soll.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e7e5a7e22c20b15dc373a2cce2bfe19e3417d4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408463"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="a6fb4-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="a6fb4-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="a6fb4-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-104">This topic is not current.</span></span> <span data-ttu-id="a6fb4-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a6fb4-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a6fb4-106">Beschreibt den Punkt im Bereich "Highlight to Shadow", an dem GCR beginnen soll (100 % dunkelster Schatten).</span><span class="sxs-lookup"><span data-stu-id="a6fb4-106">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="a6fb4-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a6fb4-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a6fb4-108">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="a6fb4-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a6fb4-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a6fb4-109">Element Information</span></span>



| <span data-ttu-id="a6fb4-110">Name</span><span class="sxs-lookup"><span data-stu-id="a6fb4-110">Name</span></span> | <span data-ttu-id="a6fb4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="a6fb4-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="a6fb4-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a6fb4-112">Element Type</span></span> <br/>   | <span data-ttu-id="a6fb4-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a6fb4-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="a6fb4-114">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a6fb4-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a6fb4-115">Seite</span><span class="sxs-lookup"><span data-stu-id="a6fb4-115">Page</span></span><br/>                                            |
| <span data-ttu-id="a6fb4-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a6fb4-116">Notes</span></span> <br/>          | <span data-ttu-id="a6fb4-117">Verknüpft mit dem PageBlackGenerationProcessing-Element</span><span class="sxs-lookup"><span data-stu-id="a6fb4-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a6fb4-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="a6fb4-118">Structure Content</span></span>

<span data-ttu-id="a6fb4-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="a6fb4-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart">
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

## <a name="structure-properties"></a><span data-ttu-id="a6fb4-120">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="a6fb4-120">Structure Properties</span></span>

<span data-ttu-id="a6fb4-121">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a6fb4-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a6fb4-122">Property</span></span>                | <span data-ttu-id="a6fb4-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a6fb4-123">xsi:type</span></span>           | <span data-ttu-id="a6fb4-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a6fb4-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a6fb4-125">DataType</span><span class="sxs-lookup"><span data-stu-id="a6fb4-125">DataType</span></span><br/>     | <span data-ttu-id="a6fb4-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a6fb4-126">string</span></span><br/>  | <span data-ttu-id="a6fb4-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a6fb4-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="a6fb4-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a6fb4-128">DefaultValue</span></span><br/> | <span data-ttu-id="a6fb4-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a6fb4-129">string</span></span><br/>  | <span data-ttu-id="a6fb4-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="a6fb4-130">undefined</span></span><br/>       |
| <span data-ttu-id="a6fb4-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a6fb4-131">MaxValue</span></span><br/>     | <span data-ttu-id="a6fb4-132">integer</span><span class="sxs-lookup"><span data-stu-id="a6fb4-132">integer</span></span><br/> | <span data-ttu-id="a6fb4-133">100</span><span class="sxs-lookup"><span data-stu-id="a6fb4-133">100</span></span><br/>             |
| <span data-ttu-id="a6fb4-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="a6fb4-134">MinValue</span></span><br/>     | <span data-ttu-id="a6fb4-135">integer</span><span class="sxs-lookup"><span data-stu-id="a6fb4-135">integer</span></span><br/> | <span data-ttu-id="a6fb4-136">0</span><span class="sxs-lookup"><span data-stu-id="a6fb4-136">0</span></span><br/>               |
| <span data-ttu-id="a6fb4-137">Mehrere</span><span class="sxs-lookup"><span data-stu-id="a6fb4-137">Multiple</span></span><br/>     | <span data-ttu-id="a6fb4-138">integer</span><span class="sxs-lookup"><span data-stu-id="a6fb4-138">integer</span></span><br/> | <span data-ttu-id="a6fb4-139">1</span><span class="sxs-lookup"><span data-stu-id="a6fb4-139">1</span></span><br/>               |
| <span data-ttu-id="a6fb4-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-140">Mandatory</span></span><br/>    | <span data-ttu-id="a6fb4-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a6fb4-141">string</span></span><br/>  | <span data-ttu-id="a6fb4-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="a6fb4-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a6fb4-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="a6fb4-143">UnitType</span></span><br/>     | <span data-ttu-id="a6fb4-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a6fb4-144">string</span></span><br/>  | <span data-ttu-id="a6fb4-145">Prozent</span><span class="sxs-lookup"><span data-stu-id="a6fb4-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a6fb4-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6fb4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6fb4-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a6fb4-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




