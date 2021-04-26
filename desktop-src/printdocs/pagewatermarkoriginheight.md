---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90736f8cac9c919f9d640ffc01311024ef79bc3a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994488"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="92aa7-104">PageWatermarkOriginHeight</span><span class="sxs-lookup"><span data-stu-id="92aa7-104">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="92aa7-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="92aa7-105">This topic is not current.</span></span> <span data-ttu-id="92aa7-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="92aa7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="92aa7-107">Gibt den Ursprung eines Wasserzeichens relativ zum Ursprung von PageImageableSize an.</span><span class="sxs-lookup"><span data-stu-id="92aa7-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="92aa7-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="92aa7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92aa7-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="92aa7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="92aa7-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="92aa7-110">Element Information</span></span>



| <span data-ttu-id="92aa7-111">Name</span><span class="sxs-lookup"><span data-stu-id="92aa7-111">Name</span></span> | <span data-ttu-id="92aa7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="92aa7-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="92aa7-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="92aa7-113">Element Type</span></span> <br/>   | <span data-ttu-id="92aa7-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="92aa7-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="92aa7-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="92aa7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="92aa7-116">Seite</span><span class="sxs-lookup"><span data-stu-id="92aa7-116">Page</span></span><br/>                            |
| <span data-ttu-id="92aa7-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="92aa7-117">Notes</span></span> <br/>          | <span data-ttu-id="92aa7-118">Mit PageWatermark-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="92aa7-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="92aa7-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="92aa7-119">Structure Content</span></span>

<span data-ttu-id="92aa7-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="92aa7-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="92aa7-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="92aa7-121">Structure Properties</span></span>

<span data-ttu-id="92aa7-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="92aa7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="92aa7-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="92aa7-123">Property</span></span>                | <span data-ttu-id="92aa7-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="92aa7-124">xsi:type</span></span>           | <span data-ttu-id="92aa7-125">Wert</span><span class="sxs-lookup"><span data-stu-id="92aa7-125">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="92aa7-126">DataType</span><span class="sxs-lookup"><span data-stu-id="92aa7-126">DataType</span></span><br/>     | <span data-ttu-id="92aa7-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92aa7-127">string</span></span><br/>  | <span data-ttu-id="92aa7-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="92aa7-128">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="92aa7-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="92aa7-129">DefaultValue</span></span><br/> | <span data-ttu-id="92aa7-130">integer</span><span class="sxs-lookup"><span data-stu-id="92aa7-130">integer</span></span><br/> | <span data-ttu-id="92aa7-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="92aa7-131">undefined</span></span><br/>                                                    |
| <span data-ttu-id="92aa7-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="92aa7-132">MaxValue</span></span><br/>     | <span data-ttu-id="92aa7-133">integer</span><span class="sxs-lookup"><span data-stu-id="92aa7-133">integer</span></span><br/> | <span data-ttu-id="92aa7-134">Kleiner als oder gleich PageImageableSize– ExtentHeight-Wert</span><span class="sxs-lookup"><span data-stu-id="92aa7-134">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="92aa7-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="92aa7-135">MinValue</span></span><br/>     | <span data-ttu-id="92aa7-136">integer</span><span class="sxs-lookup"><span data-stu-id="92aa7-136">integer</span></span><br/> | <span data-ttu-id="92aa7-137">0</span><span class="sxs-lookup"><span data-stu-id="92aa7-137">0</span></span><br/>                                                            |
| <span data-ttu-id="92aa7-138">Mehrere</span><span class="sxs-lookup"><span data-stu-id="92aa7-138">Multiple</span></span><br/>     | <span data-ttu-id="92aa7-139">integer</span><span class="sxs-lookup"><span data-stu-id="92aa7-139">integer</span></span><br/> | <span data-ttu-id="92aa7-140">1</span><span class="sxs-lookup"><span data-stu-id="92aa7-140">1</span></span><br/>                                                            |
| <span data-ttu-id="92aa7-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="92aa7-141">Mandatory</span></span><br/>    | <span data-ttu-id="92aa7-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92aa7-142">string</span></span><br/>  | <span data-ttu-id="92aa7-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="92aa7-143">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="92aa7-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="92aa7-144">UnitType</span></span><br/>     | <span data-ttu-id="92aa7-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92aa7-145">string</span></span><br/>  | <span data-ttu-id="92aa7-146">Mikron</span><span class="sxs-lookup"><span data-stu-id="92aa7-146">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="92aa7-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92aa7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92aa7-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="92aa7-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




