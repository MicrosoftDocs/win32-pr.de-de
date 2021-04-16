---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: "\"Pgeblackgenerationprocessinggraycomponentreplacementlevel\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c0d55c2150f5a2299672ebf95d6656b238acc1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351888"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="ce483-104">"Pgeblackgenerationprocessinggraycomponentreplacementlevel"</span><span class="sxs-lookup"><span data-stu-id="ce483-104">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="ce483-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ce483-105">This topic is not current.</span></span> <span data-ttu-id="ce483-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ce483-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ce483-107">Gibt den Prozentsatz der auszuführenden grauen Komponenten Ersetzung an.</span><span class="sxs-lookup"><span data-stu-id="ce483-107">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="ce483-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ce483-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ce483-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ce483-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ce483-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ce483-110">Element Information</span></span>



| <span data-ttu-id="ce483-111">Name</span><span class="sxs-lookup"><span data-stu-id="ce483-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="ce483-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ce483-112">Element Type</span></span> <br/>   | <span data-ttu-id="ce483-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ce483-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="ce483-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="ce483-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ce483-115">Seite</span><span class="sxs-lookup"><span data-stu-id="ce483-115">Page</span></span><br/>                                            |
| <span data-ttu-id="ce483-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce483-116">Notes</span></span> <br/>          | <span data-ttu-id="ce483-117">Verknüpft mit dem Element "pgeblackgenerationprocessing"</span><span class="sxs-lookup"><span data-stu-id="ce483-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ce483-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ce483-118">Structure Content</span></span>

<span data-ttu-id="ce483-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="ce483-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="ce483-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce483-120">Structure Properties</span></span>

<span data-ttu-id="ce483-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ce483-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ce483-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ce483-122">Property</span></span>                | <span data-ttu-id="ce483-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ce483-123">xsi:type</span></span>           | <span data-ttu-id="ce483-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ce483-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ce483-125">DataType</span><span class="sxs-lookup"><span data-stu-id="ce483-125">DataType</span></span><br/>     | <span data-ttu-id="ce483-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ce483-126">string</span></span><br/>  | <span data-ttu-id="ce483-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ce483-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="ce483-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ce483-128">DefaultValue</span></span><br/> | <span data-ttu-id="ce483-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ce483-129">string</span></span><br/>  | <span data-ttu-id="ce483-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ce483-130">undefined</span></span><br/>       |
| <span data-ttu-id="ce483-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ce483-131">MaxValue</span></span><br/>     | <span data-ttu-id="ce483-132">integer</span><span class="sxs-lookup"><span data-stu-id="ce483-132">integer</span></span><br/> | <span data-ttu-id="ce483-133">100</span><span class="sxs-lookup"><span data-stu-id="ce483-133">100</span></span><br/>             |
| <span data-ttu-id="ce483-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="ce483-134">MinValue</span></span><br/>     | <span data-ttu-id="ce483-135">integer</span><span class="sxs-lookup"><span data-stu-id="ce483-135">integer</span></span><br/> | <span data-ttu-id="ce483-136">0</span><span class="sxs-lookup"><span data-stu-id="ce483-136">0</span></span><br/>               |
| <span data-ttu-id="ce483-137">Mehrere</span><span class="sxs-lookup"><span data-stu-id="ce483-137">Multiple</span></span><br/>     | <span data-ttu-id="ce483-138">integer</span><span class="sxs-lookup"><span data-stu-id="ce483-138">integer</span></span><br/> | <span data-ttu-id="ce483-139">1</span><span class="sxs-lookup"><span data-stu-id="ce483-139">1</span></span><br/>               |
| <span data-ttu-id="ce483-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ce483-140">Mandatory</span></span><br/>    | <span data-ttu-id="ce483-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ce483-141">string</span></span><br/>  | <span data-ttu-id="ce483-142">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="ce483-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ce483-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="ce483-143">UnitType</span></span><br/>     | <span data-ttu-id="ce483-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ce483-144">string</span></span><br/>  | <span data-ttu-id="ce483-145">Prozent</span><span class="sxs-lookup"><span data-stu-id="ce483-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ce483-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce483-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce483-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="ce483-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




