---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: "\"Pgewatermarkoriginheight\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d3e12591f6c648e6e636e1bb72f4df694d0d13
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961263"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="866bc-104">"Pgewatermarkoriginheight"</span><span class="sxs-lookup"><span data-stu-id="866bc-104">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="866bc-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="866bc-105">This topic is not current.</span></span> <span data-ttu-id="866bc-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="866bc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="866bc-107">Gibt den Ursprung eines Wasserzeichens relativ zum Ursprung von PageImageableSize an.</span><span class="sxs-lookup"><span data-stu-id="866bc-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="866bc-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="866bc-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="866bc-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="866bc-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="866bc-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="866bc-110">Element Information</span></span>



| <span data-ttu-id="866bc-111">Name</span><span class="sxs-lookup"><span data-stu-id="866bc-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="866bc-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="866bc-112">Element Type</span></span> <br/>   | <span data-ttu-id="866bc-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="866bc-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="866bc-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="866bc-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="866bc-115">Seite</span><span class="sxs-lookup"><span data-stu-id="866bc-115">Page</span></span><br/>                            |
| <span data-ttu-id="866bc-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="866bc-116">Notes</span></span> <br/>          | <span data-ttu-id="866bc-117">Mit dem Element "pgewatermark" verknüpft</span><span class="sxs-lookup"><span data-stu-id="866bc-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="866bc-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="866bc-118">Structure Content</span></span>

<span data-ttu-id="866bc-119">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="866bc-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="866bc-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="866bc-120">Structure Properties</span></span>

<span data-ttu-id="866bc-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="866bc-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="866bc-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="866bc-122">Property</span></span>                | <span data-ttu-id="866bc-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="866bc-123">xsi:type</span></span>           | <span data-ttu-id="866bc-124">Wert</span><span class="sxs-lookup"><span data-stu-id="866bc-124">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="866bc-125">DataType</span><span class="sxs-lookup"><span data-stu-id="866bc-125">DataType</span></span><br/>     | <span data-ttu-id="866bc-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="866bc-126">string</span></span><br/>  | <span data-ttu-id="866bc-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="866bc-127">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="866bc-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="866bc-128">DefaultValue</span></span><br/> | <span data-ttu-id="866bc-129">integer</span><span class="sxs-lookup"><span data-stu-id="866bc-129">integer</span></span><br/> | <span data-ttu-id="866bc-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="866bc-130">undefined</span></span><br/>                                                    |
| <span data-ttu-id="866bc-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="866bc-131">MaxValue</span></span><br/>     | <span data-ttu-id="866bc-132">integer</span><span class="sxs-lookup"><span data-stu-id="866bc-132">integer</span></span><br/> | <span data-ttu-id="866bc-133">Kleiner oder gleich dem PageImageableSize-ExtentHeight-Wert</span><span class="sxs-lookup"><span data-stu-id="866bc-133">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="866bc-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="866bc-134">MinValue</span></span><br/>     | <span data-ttu-id="866bc-135">integer</span><span class="sxs-lookup"><span data-stu-id="866bc-135">integer</span></span><br/> | <span data-ttu-id="866bc-136">0</span><span class="sxs-lookup"><span data-stu-id="866bc-136">0</span></span><br/>                                                            |
| <span data-ttu-id="866bc-137">Mehrere</span><span class="sxs-lookup"><span data-stu-id="866bc-137">Multiple</span></span><br/>     | <span data-ttu-id="866bc-138">integer</span><span class="sxs-lookup"><span data-stu-id="866bc-138">integer</span></span><br/> | <span data-ttu-id="866bc-139">1</span><span class="sxs-lookup"><span data-stu-id="866bc-139">1</span></span><br/>                                                            |
| <span data-ttu-id="866bc-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="866bc-140">Mandatory</span></span><br/>    | <span data-ttu-id="866bc-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="866bc-141">string</span></span><br/>  | <span data-ttu-id="866bc-142">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="866bc-142">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="866bc-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="866bc-143">UnitType</span></span><br/>     | <span data-ttu-id="866bc-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="866bc-144">string</span></span><br/>  | <span data-ttu-id="866bc-145">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="866bc-145">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="866bc-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="866bc-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="866bc-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="866bc-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




