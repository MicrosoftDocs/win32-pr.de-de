---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9a790d66d1f7806a7ef86ee4a85f62225aa836
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997707"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="1ab69-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="1ab69-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="1ab69-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="1ab69-105">This topic is not current.</span></span> <span data-ttu-id="1ab69-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="1ab69-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1ab69-107">Beschreibt die über neutrale Werte hinaus (in gitterfarbenen Farben), die gcr angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ab69-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="1ab69-108">0 % = Austausch von einheitlichen Komponenten, 100 % = Grauer Komponentenaustausch.</span><span class="sxs-lookup"><span data-stu-id="1ab69-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="1ab69-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1ab69-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1ab69-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="1ab69-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1ab69-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1ab69-111">Element Information</span></span>



| <span data-ttu-id="1ab69-112">Name</span><span class="sxs-lookup"><span data-stu-id="1ab69-112">Name</span></span> | <span data-ttu-id="1ab69-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1ab69-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="1ab69-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="1ab69-114">Element Type</span></span> <br/>   | <span data-ttu-id="1ab69-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1ab69-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="1ab69-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="1ab69-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1ab69-117">Seite</span><span class="sxs-lookup"><span data-stu-id="1ab69-117">Page</span></span><br/>                                            |
| <span data-ttu-id="1ab69-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ab69-118">Notes</span></span> <br/>          | <span data-ttu-id="1ab69-119">Mit PageBlackGenerationProcessing-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="1ab69-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1ab69-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="1ab69-120">Structure Content</span></span>

<span data-ttu-id="1ab69-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="1ab69-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent">
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

## <a name="structure-properties"></a><span data-ttu-id="1ab69-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ab69-122">Structure Properties</span></span>

<span data-ttu-id="1ab69-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1ab69-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1ab69-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1ab69-124">Property</span></span>                | <span data-ttu-id="1ab69-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1ab69-125">xsi:type</span></span>           | <span data-ttu-id="1ab69-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1ab69-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1ab69-127">DataType</span><span class="sxs-lookup"><span data-stu-id="1ab69-127">DataType</span></span><br/>     | <span data-ttu-id="1ab69-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1ab69-128">string</span></span><br/>  | <span data-ttu-id="1ab69-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1ab69-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="1ab69-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1ab69-130">DefaultValue</span></span><br/> | <span data-ttu-id="1ab69-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1ab69-131">string</span></span><br/>  | <span data-ttu-id="1ab69-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="1ab69-132">undefined</span></span><br/>       |
| <span data-ttu-id="1ab69-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1ab69-133">MaxValue</span></span><br/>     | <span data-ttu-id="1ab69-134">integer</span><span class="sxs-lookup"><span data-stu-id="1ab69-134">integer</span></span><br/> | <span data-ttu-id="1ab69-135">100</span><span class="sxs-lookup"><span data-stu-id="1ab69-135">100</span></span><br/>             |
| <span data-ttu-id="1ab69-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="1ab69-136">MinValue</span></span><br/>     | <span data-ttu-id="1ab69-137">integer</span><span class="sxs-lookup"><span data-stu-id="1ab69-137">integer</span></span><br/> | <span data-ttu-id="1ab69-138">0</span><span class="sxs-lookup"><span data-stu-id="1ab69-138">0</span></span><br/>               |
| <span data-ttu-id="1ab69-139">Mehrere</span><span class="sxs-lookup"><span data-stu-id="1ab69-139">Multiple</span></span><br/>     | <span data-ttu-id="1ab69-140">integer</span><span class="sxs-lookup"><span data-stu-id="1ab69-140">integer</span></span><br/> | <span data-ttu-id="1ab69-141">1</span><span class="sxs-lookup"><span data-stu-id="1ab69-141">1</span></span><br/>               |
| <span data-ttu-id="1ab69-142">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="1ab69-142">Mandatory</span></span><br/>    | <span data-ttu-id="1ab69-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1ab69-143">string</span></span><br/>  | <span data-ttu-id="1ab69-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="1ab69-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1ab69-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="1ab69-145">UnitType</span></span><br/>     | <span data-ttu-id="1ab69-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1ab69-146">string</span></span><br/>  | <span data-ttu-id="1ab69-147">Prozent</span><span class="sxs-lookup"><span data-stu-id="1ab69-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1ab69-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ab69-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ab69-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="1ab69-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




