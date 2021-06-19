---
description: Weitere Informationen zum PageWatermarkTextAngle-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dce37512314e1eaac0cbbe3b5b4b817cb2ee455
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395975"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="211af-105">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="211af-105">PageWatermarkTextAngle</span></span>

<span data-ttu-id="211af-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="211af-106">This topic is not current.</span></span> <span data-ttu-id="211af-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="211af-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="211af-108">Gibt den Winkel des Wasserzeichentexts relativ zur PageImageableSizeWidth-Richtung an.</span><span class="sxs-lookup"><span data-stu-id="211af-108">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="211af-109">Der Winkel wird gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="211af-109">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="211af-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="211af-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="211af-111">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="211af-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="211af-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="211af-112">Element Information</span></span>



| <span data-ttu-id="211af-113">Name</span><span class="sxs-lookup"><span data-stu-id="211af-113">Name</span></span> | <span data-ttu-id="211af-114">Wert</span><span class="sxs-lookup"><span data-stu-id="211af-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="211af-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="211af-115">Element Type</span></span> <br/>   | <span data-ttu-id="211af-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="211af-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="211af-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="211af-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="211af-118">Seite</span><span class="sxs-lookup"><span data-stu-id="211af-118">Page</span></span><br/>                            |
| <span data-ttu-id="211af-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="211af-119">Notes</span></span> <br/>          | <span data-ttu-id="211af-120">Verknüpft mit dem PageWatermark-Element</span><span class="sxs-lookup"><span data-stu-id="211af-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="211af-121">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="211af-121">Structure Content</span></span>

<span data-ttu-id="211af-122">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="211af-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextAngle">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">359</psf:Value>
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
    <psf:Value xsi:type="xs:string">degrees</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="211af-123">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="211af-123">Structure Properties</span></span>

<span data-ttu-id="211af-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="211af-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="211af-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="211af-125">Property</span></span>                | <span data-ttu-id="211af-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="211af-126">xsi:type</span></span>           | <span data-ttu-id="211af-127">Wert</span><span class="sxs-lookup"><span data-stu-id="211af-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="211af-128">DataType</span><span class="sxs-lookup"><span data-stu-id="211af-128">DataType</span></span><br/>     | <span data-ttu-id="211af-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="211af-129">string</span></span><br/>  | <span data-ttu-id="211af-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="211af-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="211af-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="211af-131">DefaultValue</span></span><br/> | <span data-ttu-id="211af-132">integer</span><span class="sxs-lookup"><span data-stu-id="211af-132">integer</span></span><br/> | <span data-ttu-id="211af-133">0</span><span class="sxs-lookup"><span data-stu-id="211af-133">0</span></span><br/>               |
| <span data-ttu-id="211af-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="211af-134">MaxValue</span></span><br/>     | <span data-ttu-id="211af-135">integer</span><span class="sxs-lookup"><span data-stu-id="211af-135">integer</span></span><br/> | <span data-ttu-id="211af-136">359</span><span class="sxs-lookup"><span data-stu-id="211af-136">359</span></span><br/>             |
| <span data-ttu-id="211af-137">Minvalue</span><span class="sxs-lookup"><span data-stu-id="211af-137">MinValue</span></span><br/>     | <span data-ttu-id="211af-138">integer</span><span class="sxs-lookup"><span data-stu-id="211af-138">integer</span></span><br/> | <span data-ttu-id="211af-139">0</span><span class="sxs-lookup"><span data-stu-id="211af-139">0</span></span><br/>               |
| <span data-ttu-id="211af-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="211af-140">Multiple</span></span><br/>     | <span data-ttu-id="211af-141">integer</span><span class="sxs-lookup"><span data-stu-id="211af-141">integer</span></span><br/> | <span data-ttu-id="211af-142">1</span><span class="sxs-lookup"><span data-stu-id="211af-142">1</span></span><br/>               |
| <span data-ttu-id="211af-143">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="211af-143">Mandatory</span></span><br/>    | <span data-ttu-id="211af-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="211af-144">string</span></span><br/>  | <span data-ttu-id="211af-145">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="211af-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="211af-146">Unittype</span><span class="sxs-lookup"><span data-stu-id="211af-146">UnitType</span></span><br/>     | <span data-ttu-id="211af-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="211af-147">string</span></span><br/>  | <span data-ttu-id="211af-148">Grad</span><span class="sxs-lookup"><span data-stu-id="211af-148">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="211af-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="211af-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="211af-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="211af-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




