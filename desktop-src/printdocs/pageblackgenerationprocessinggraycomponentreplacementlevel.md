---
description: Erfahren Sie mehr über das PageBlackGenerationProcessingGrayComponentReplacementLevel-Element, das den Prozentsatz des Ersetzens grauer Komponenten angibt.
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: PageBlackGenerationProcessingGrayComponentReplacementLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8499c8521b974d01657c171a99e86e738c82b4e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408483"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="e4876-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span><span class="sxs-lookup"><span data-stu-id="e4876-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="e4876-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e4876-104">This topic is not current.</span></span> <span data-ttu-id="e4876-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="e4876-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e4876-106">Gibt den Prozentsatz des zu ersetzenden grauen Komponenten an.</span><span class="sxs-lookup"><span data-stu-id="e4876-106">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="e4876-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e4876-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e4876-108">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e4876-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e4876-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e4876-109">Element Information</span></span>



| <span data-ttu-id="e4876-110">Name</span><span class="sxs-lookup"><span data-stu-id="e4876-110">Name</span></span> | <span data-ttu-id="e4876-111">Wert</span><span class="sxs-lookup"><span data-stu-id="e4876-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="e4876-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e4876-112">Element Type</span></span> <br/>   | <span data-ttu-id="e4876-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e4876-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="e4876-114">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="e4876-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e4876-115">Seite</span><span class="sxs-lookup"><span data-stu-id="e4876-115">Page</span></span><br/>                                            |
| <span data-ttu-id="e4876-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4876-116">Notes</span></span> <br/>          | <span data-ttu-id="e4876-117">Mit PageBlackGenerationProcessing-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="e4876-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e4876-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e4876-118">Structure Content</span></span>

<span data-ttu-id="e4876-119">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="e4876-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="e4876-120">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4876-120">Structure Properties</span></span>

<span data-ttu-id="e4876-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e4876-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e4876-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4876-122">Property</span></span>                | <span data-ttu-id="e4876-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e4876-123">xsi:type</span></span>           | <span data-ttu-id="e4876-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e4876-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e4876-125">DataType</span><span class="sxs-lookup"><span data-stu-id="e4876-125">DataType</span></span><br/>     | <span data-ttu-id="e4876-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e4876-126">string</span></span><br/>  | <span data-ttu-id="e4876-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e4876-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="e4876-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e4876-128">DefaultValue</span></span><br/> | <span data-ttu-id="e4876-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e4876-129">string</span></span><br/>  | <span data-ttu-id="e4876-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e4876-130">undefined</span></span><br/>       |
| <span data-ttu-id="e4876-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e4876-131">MaxValue</span></span><br/>     | <span data-ttu-id="e4876-132">integer</span><span class="sxs-lookup"><span data-stu-id="e4876-132">integer</span></span><br/> | <span data-ttu-id="e4876-133">100</span><span class="sxs-lookup"><span data-stu-id="e4876-133">100</span></span><br/>             |
| <span data-ttu-id="e4876-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="e4876-134">MinValue</span></span><br/>     | <span data-ttu-id="e4876-135">integer</span><span class="sxs-lookup"><span data-stu-id="e4876-135">integer</span></span><br/> | <span data-ttu-id="e4876-136">0</span><span class="sxs-lookup"><span data-stu-id="e4876-136">0</span></span><br/>               |
| <span data-ttu-id="e4876-137">Mehrere</span><span class="sxs-lookup"><span data-stu-id="e4876-137">Multiple</span></span><br/>     | <span data-ttu-id="e4876-138">integer</span><span class="sxs-lookup"><span data-stu-id="e4876-138">integer</span></span><br/> | <span data-ttu-id="e4876-139">1</span><span class="sxs-lookup"><span data-stu-id="e4876-139">1</span></span><br/>               |
| <span data-ttu-id="e4876-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="e4876-140">Mandatory</span></span><br/>    | <span data-ttu-id="e4876-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e4876-141">string</span></span><br/>  | <span data-ttu-id="e4876-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="e4876-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e4876-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="e4876-143">UnitType</span></span><br/>     | <span data-ttu-id="e4876-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e4876-144">string</span></span><br/>  | <span data-ttu-id="e4876-145">Prozent</span><span class="sxs-lookup"><span data-stu-id="e4876-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e4876-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4876-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4876-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="e4876-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




