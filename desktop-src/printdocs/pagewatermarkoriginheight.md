---
description: Hier finden Sie Informationen zum PageWatermarkOriginHeight-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59e9336088d44cef1941df03319519ae69af1c3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395985"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="b396d-105">PageWatermarkOriginHeight</span><span class="sxs-lookup"><span data-stu-id="b396d-105">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="b396d-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b396d-106">This topic is not current.</span></span> <span data-ttu-id="b396d-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="b396d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b396d-108">Gibt den Ursprung eines Wasserzeichens relativ zum Ursprung von PageImageableSize an.</span><span class="sxs-lookup"><span data-stu-id="b396d-108">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="b396d-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b396d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b396d-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b396d-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b396d-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b396d-111">Element Information</span></span>



| <span data-ttu-id="b396d-112">Name</span><span class="sxs-lookup"><span data-stu-id="b396d-112">Name</span></span> | <span data-ttu-id="b396d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b396d-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="b396d-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="b396d-114">Element Type</span></span> <br/>   | <span data-ttu-id="b396d-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b396d-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="b396d-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="b396d-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b396d-117">Seite</span><span class="sxs-lookup"><span data-stu-id="b396d-117">Page</span></span><br/>                            |
| <span data-ttu-id="b396d-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b396d-118">Notes</span></span> <br/>          | <span data-ttu-id="b396d-119">Mit PageWatermark-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="b396d-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b396d-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b396d-120">Structure Content</span></span>

<span data-ttu-id="b396d-121">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b396d-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b396d-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="b396d-122">Structure Properties</span></span>

<span data-ttu-id="b396d-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b396d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b396d-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b396d-124">Property</span></span>                | <span data-ttu-id="b396d-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b396d-125">xsi:type</span></span>           | <span data-ttu-id="b396d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b396d-126">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b396d-127">DataType</span><span class="sxs-lookup"><span data-stu-id="b396d-127">DataType</span></span><br/>     | <span data-ttu-id="b396d-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b396d-128">string</span></span><br/>  | <span data-ttu-id="b396d-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b396d-129">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="b396d-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b396d-130">DefaultValue</span></span><br/> | <span data-ttu-id="b396d-131">integer</span><span class="sxs-lookup"><span data-stu-id="b396d-131">integer</span></span><br/> | <span data-ttu-id="b396d-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b396d-132">undefined</span></span><br/>                                                    |
| <span data-ttu-id="b396d-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b396d-133">MaxValue</span></span><br/>     | <span data-ttu-id="b396d-134">integer</span><span class="sxs-lookup"><span data-stu-id="b396d-134">integer</span></span><br/> | <span data-ttu-id="b396d-135">Kleiner als oder gleich PageImageableSize– ExtentHeight-Wert</span><span class="sxs-lookup"><span data-stu-id="b396d-135">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="b396d-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="b396d-136">MinValue</span></span><br/>     | <span data-ttu-id="b396d-137">integer</span><span class="sxs-lookup"><span data-stu-id="b396d-137">integer</span></span><br/> | <span data-ttu-id="b396d-138">0</span><span class="sxs-lookup"><span data-stu-id="b396d-138">0</span></span><br/>                                                            |
| <span data-ttu-id="b396d-139">Mehrere</span><span class="sxs-lookup"><span data-stu-id="b396d-139">Multiple</span></span><br/>     | <span data-ttu-id="b396d-140">integer</span><span class="sxs-lookup"><span data-stu-id="b396d-140">integer</span></span><br/> | <span data-ttu-id="b396d-141">1</span><span class="sxs-lookup"><span data-stu-id="b396d-141">1</span></span><br/>                                                            |
| <span data-ttu-id="b396d-142">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="b396d-142">Mandatory</span></span><br/>    | <span data-ttu-id="b396d-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b396d-143">string</span></span><br/>  | <span data-ttu-id="b396d-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="b396d-144">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="b396d-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="b396d-145">UnitType</span></span><br/>     | <span data-ttu-id="b396d-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b396d-146">string</span></span><br/>  | <span data-ttu-id="b396d-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="b396d-147">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="b396d-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b396d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b396d-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="b396d-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




