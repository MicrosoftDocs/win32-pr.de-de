---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: "\"Pgeblackgenerationprocessingtotalinkcoveragelimit\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07566926c2115855ea7321af90e7d1caebcd0a82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355118"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="380f2-104">"Pgeblackgenerationprocessingtotalinkcoveragelimit"</span><span class="sxs-lookup"><span data-stu-id="380f2-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="380f2-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="380f2-105">This topic is not current.</span></span> <span data-ttu-id="380f2-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="380f2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="380f2-107">Gibt die maximal zulässige Summe der vier frei Handabdeckung an beliebiger Stelle in einem Bild an.</span><span class="sxs-lookup"><span data-stu-id="380f2-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="380f2-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="380f2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="380f2-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="380f2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="380f2-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="380f2-110">Element Information</span></span>



| <span data-ttu-id="380f2-111">Name</span><span class="sxs-lookup"><span data-stu-id="380f2-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="380f2-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="380f2-112">Element Type</span></span> <br/>   | <span data-ttu-id="380f2-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="380f2-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="380f2-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="380f2-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="380f2-115">Seite</span><span class="sxs-lookup"><span data-stu-id="380f2-115">Page</span></span><br/>                                            |
| <span data-ttu-id="380f2-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="380f2-116">Notes</span></span> <br/>          | <span data-ttu-id="380f2-117">Verknüpft mit dem Element "pgeblackgenerationprocessing"</span><span class="sxs-lookup"><span data-stu-id="380f2-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="380f2-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="380f2-118">Structure Content</span></span>

<span data-ttu-id="380f2-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="380f2-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="380f2-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="380f2-120">Structure Properties</span></span>

<span data-ttu-id="380f2-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="380f2-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="380f2-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="380f2-122">Property</span></span>                | <span data-ttu-id="380f2-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="380f2-123">xsi:type</span></span>           | <span data-ttu-id="380f2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="380f2-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="380f2-125">DataType</span><span class="sxs-lookup"><span data-stu-id="380f2-125">DataType</span></span><br/>     | <span data-ttu-id="380f2-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="380f2-126">string</span></span><br/>  | <span data-ttu-id="380f2-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="380f2-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="380f2-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="380f2-128">DefaultValue</span></span><br/> | <span data-ttu-id="380f2-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="380f2-129">string</span></span><br/>  | <span data-ttu-id="380f2-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="380f2-130">undefined</span></span><br/>       |
| <span data-ttu-id="380f2-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="380f2-131">MaxValue</span></span><br/>     | <span data-ttu-id="380f2-132">integer</span><span class="sxs-lookup"><span data-stu-id="380f2-132">integer</span></span><br/> | <span data-ttu-id="380f2-133">400</span><span class="sxs-lookup"><span data-stu-id="380f2-133">400</span></span><br/>             |
| <span data-ttu-id="380f2-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="380f2-134">MinValue</span></span><br/>     | <span data-ttu-id="380f2-135">integer</span><span class="sxs-lookup"><span data-stu-id="380f2-135">integer</span></span><br/> | <span data-ttu-id="380f2-136">200</span><span class="sxs-lookup"><span data-stu-id="380f2-136">200</span></span><br/>             |
| <span data-ttu-id="380f2-137">Mehrere</span><span class="sxs-lookup"><span data-stu-id="380f2-137">Multiple</span></span><br/>     | <span data-ttu-id="380f2-138">integer</span><span class="sxs-lookup"><span data-stu-id="380f2-138">integer</span></span><br/> | <span data-ttu-id="380f2-139">1</span><span class="sxs-lookup"><span data-stu-id="380f2-139">1</span></span><br/>               |
| <span data-ttu-id="380f2-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="380f2-140">Mandatory</span></span><br/>    | <span data-ttu-id="380f2-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="380f2-141">string</span></span><br/>  | <span data-ttu-id="380f2-142">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="380f2-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="380f2-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="380f2-143">UnitType</span></span><br/>     | <span data-ttu-id="380f2-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="380f2-144">string</span></span><br/>  | <span data-ttu-id="380f2-145">Prozent</span><span class="sxs-lookup"><span data-stu-id="380f2-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="380f2-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="380f2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="380f2-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="380f2-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




