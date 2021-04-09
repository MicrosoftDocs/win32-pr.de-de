---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: "\"Pgewatermarkoriginwidth\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6780dd5cc3b90a4f15cb6ada66ab82c4269acd82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869648"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="f2da6-104">"Pgewatermarkoriginwidth"</span><span class="sxs-lookup"><span data-stu-id="f2da6-104">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="f2da6-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="f2da6-105">This topic is not current.</span></span> <span data-ttu-id="f2da6-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f2da6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f2da6-107">Gibt den Ursprung eines Wasserzeichens relativ zum Ursprung von PageImageableSize an.</span><span class="sxs-lookup"><span data-stu-id="f2da6-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="f2da6-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f2da6-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f2da6-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="f2da6-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f2da6-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f2da6-110">Element Information</span></span>



| <span data-ttu-id="f2da6-111">Name</span><span class="sxs-lookup"><span data-stu-id="f2da6-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="f2da6-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="f2da6-112">Element Type</span></span> <br/>   | <span data-ttu-id="f2da6-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f2da6-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="f2da6-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="f2da6-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f2da6-115">Seite</span><span class="sxs-lookup"><span data-stu-id="f2da6-115">Page</span></span><br/>                            |
| <span data-ttu-id="f2da6-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2da6-116">Notes</span></span> <br/>          | <span data-ttu-id="f2da6-117">Mit dem Element "pgewatermark" verknüpft</span><span class="sxs-lookup"><span data-stu-id="f2da6-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f2da6-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="f2da6-118">Structure Content</span></span>

<span data-ttu-id="f2da6-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="f2da6-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="f2da6-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2da6-120">Structure Properties</span></span>

<span data-ttu-id="f2da6-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f2da6-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f2da6-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f2da6-122">Property</span></span>                | <span data-ttu-id="f2da6-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f2da6-123">xsi:type</span></span>           | <span data-ttu-id="f2da6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f2da6-124">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="f2da6-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f2da6-125">DataType</span></span><br/>     | <span data-ttu-id="f2da6-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f2da6-126">string</span></span><br/>  | <span data-ttu-id="f2da6-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f2da6-127">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="f2da6-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f2da6-128">DefaultValue</span></span><br/> | <span data-ttu-id="f2da6-129">integer</span><span class="sxs-lookup"><span data-stu-id="f2da6-129">integer</span></span><br/> | <span data-ttu-id="f2da6-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="f2da6-130">undefined</span></span><br/>                                                   |
| <span data-ttu-id="f2da6-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f2da6-131">MaxValue</span></span><br/>     | <span data-ttu-id="f2da6-132">integer</span><span class="sxs-lookup"><span data-stu-id="f2da6-132">integer</span></span><br/> | <span data-ttu-id="f2da6-133">Kleiner oder gleich dem PageImageableSize-ExtentWidth-Wert</span><span class="sxs-lookup"><span data-stu-id="f2da6-133">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="f2da6-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="f2da6-134">MinValue</span></span><br/>     | <span data-ttu-id="f2da6-135">integer</span><span class="sxs-lookup"><span data-stu-id="f2da6-135">integer</span></span><br/> | <span data-ttu-id="f2da6-136">0</span><span class="sxs-lookup"><span data-stu-id="f2da6-136">0</span></span><br/>                                                           |
| <span data-ttu-id="f2da6-137">Mehrere</span><span class="sxs-lookup"><span data-stu-id="f2da6-137">Multiple</span></span><br/>     | <span data-ttu-id="f2da6-138">integer</span><span class="sxs-lookup"><span data-stu-id="f2da6-138">integer</span></span><br/> | <span data-ttu-id="f2da6-139">1</span><span class="sxs-lookup"><span data-stu-id="f2da6-139">1</span></span><br/>                                                           |
| <span data-ttu-id="f2da6-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="f2da6-140">Mandatory</span></span><br/>    | <span data-ttu-id="f2da6-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f2da6-141">string</span></span><br/>  | <span data-ttu-id="f2da6-142">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="f2da6-142">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="f2da6-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="f2da6-143">UnitType</span></span><br/>     | <span data-ttu-id="f2da6-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f2da6-144">string</span></span><br/>  | <span data-ttu-id="f2da6-145">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="f2da6-145">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="f2da6-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2da6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2da6-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="f2da6-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




