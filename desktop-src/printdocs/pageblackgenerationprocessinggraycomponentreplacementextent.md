---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: "\"Pgeblackgenerationprocessinggraycomponentreplacementextent\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c71700b23459c087361e9e28ac0c43120aff90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869656"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="8ec6c-104">"Pgeblackgenerationprocessinggraycomponentreplacementextent"</span><span class="sxs-lookup"><span data-stu-id="8ec6c-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="8ec6c-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-105">This topic is not current.</span></span> <span data-ttu-id="8ec6c-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8ec6c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8ec6c-107">Beschreibt die übergeordneten Objekte (in den Farben), für die GCR gilt.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="8ec6c-108">0% = Uniform Component Replace, 100% = graue Komponenten Ersetzung.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="8ec6c-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8ec6c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8ec6c-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="8ec6c-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8ec6c-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8ec6c-111">Element Information</span></span>



| <span data-ttu-id="8ec6c-112">Name</span><span class="sxs-lookup"><span data-stu-id="8ec6c-112">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="8ec6c-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="8ec6c-113">Element Type</span></span> <br/>   | <span data-ttu-id="8ec6c-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8ec6c-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="8ec6c-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="8ec6c-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8ec6c-116">Seite</span><span class="sxs-lookup"><span data-stu-id="8ec6c-116">Page</span></span><br/>                                            |
| <span data-ttu-id="8ec6c-117">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ec6c-117">Notes</span></span> <br/>          | <span data-ttu-id="8ec6c-118">Verknüpft mit dem Element "pgeblackgenerationprocessing"</span><span class="sxs-lookup"><span data-stu-id="8ec6c-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8ec6c-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="8ec6c-119">Structure Content</span></span>

<span data-ttu-id="8ec6c-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="8ec6c-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8ec6c-121">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8ec6c-121">Structure Properties</span></span>

<span data-ttu-id="8ec6c-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8ec6c-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8ec6c-123">Property</span></span>                | <span data-ttu-id="8ec6c-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8ec6c-124">xsi:type</span></span>           | <span data-ttu-id="8ec6c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8ec6c-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8ec6c-126">DataType</span><span class="sxs-lookup"><span data-stu-id="8ec6c-126">DataType</span></span><br/>     | <span data-ttu-id="8ec6c-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8ec6c-127">string</span></span><br/>  | <span data-ttu-id="8ec6c-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8ec6c-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="8ec6c-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8ec6c-129">DefaultValue</span></span><br/> | <span data-ttu-id="8ec6c-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8ec6c-130">string</span></span><br/>  | <span data-ttu-id="8ec6c-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="8ec6c-131">undefined</span></span><br/>       |
| <span data-ttu-id="8ec6c-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8ec6c-132">MaxValue</span></span><br/>     | <span data-ttu-id="8ec6c-133">integer</span><span class="sxs-lookup"><span data-stu-id="8ec6c-133">integer</span></span><br/> | <span data-ttu-id="8ec6c-134">100</span><span class="sxs-lookup"><span data-stu-id="8ec6c-134">100</span></span><br/>             |
| <span data-ttu-id="8ec6c-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="8ec6c-135">MinValue</span></span><br/>     | <span data-ttu-id="8ec6c-136">integer</span><span class="sxs-lookup"><span data-stu-id="8ec6c-136">integer</span></span><br/> | <span data-ttu-id="8ec6c-137">0</span><span class="sxs-lookup"><span data-stu-id="8ec6c-137">0</span></span><br/>               |
| <span data-ttu-id="8ec6c-138">Mehrere</span><span class="sxs-lookup"><span data-stu-id="8ec6c-138">Multiple</span></span><br/>     | <span data-ttu-id="8ec6c-139">integer</span><span class="sxs-lookup"><span data-stu-id="8ec6c-139">integer</span></span><br/> | <span data-ttu-id="8ec6c-140">1</span><span class="sxs-lookup"><span data-stu-id="8ec6c-140">1</span></span><br/>               |
| <span data-ttu-id="8ec6c-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-141">Mandatory</span></span><br/>    | <span data-ttu-id="8ec6c-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8ec6c-142">string</span></span><br/>  | <span data-ttu-id="8ec6c-143">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="8ec6c-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8ec6c-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="8ec6c-144">UnitType</span></span><br/>     | <span data-ttu-id="8ec6c-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8ec6c-145">string</span></span><br/>  | <span data-ttu-id="8ec6c-146">Prozent</span><span class="sxs-lookup"><span data-stu-id="8ec6c-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="8ec6c-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8ec6c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ec6c-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="8ec6c-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




