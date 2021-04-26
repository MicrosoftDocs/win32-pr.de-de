---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c13d759232670c6957a91de12f9c35cf48aeb4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995547"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="7b7d0-104">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="7b7d0-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="7b7d0-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="7b7d0-105">This topic is not current.</span></span> <span data-ttu-id="7b7d0-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="7b7d0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b7d0-107">Gibt den Winkel des Wasserzeichentexts relativ zur PageImageableSizeWidth-Richtung an.</span><span class="sxs-lookup"><span data-stu-id="7b7d0-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="7b7d0-108">Der Winkel wird gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="7b7d0-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="7b7d0-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7b7d0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7b7d0-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="7b7d0-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7b7d0-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7b7d0-111">Element Information</span></span>



| <span data-ttu-id="7b7d0-112">Name</span><span class="sxs-lookup"><span data-stu-id="7b7d0-112">Name</span></span> | <span data-ttu-id="7b7d0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7b7d0-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="7b7d0-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="7b7d0-114">Element Type</span></span> <br/>   | <span data-ttu-id="7b7d0-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7b7d0-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="7b7d0-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="7b7d0-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7b7d0-117">Seite</span><span class="sxs-lookup"><span data-stu-id="7b7d0-117">Page</span></span><br/>                            |
| <span data-ttu-id="7b7d0-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7b7d0-118">Notes</span></span> <br/>          | <span data-ttu-id="7b7d0-119">Mit PageWatermark-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="7b7d0-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7b7d0-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="7b7d0-120">Structure Content</span></span>

<span data-ttu-id="7b7d0-121">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7b7d0-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7b7d0-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b7d0-122">Structure Properties</span></span>

<span data-ttu-id="7b7d0-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7b7d0-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7b7d0-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b7d0-124">Property</span></span>                | <span data-ttu-id="7b7d0-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7b7d0-125">xsi:type</span></span>           | <span data-ttu-id="7b7d0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7b7d0-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7b7d0-127">DataType</span><span class="sxs-lookup"><span data-stu-id="7b7d0-127">DataType</span></span><br/>     | <span data-ttu-id="7b7d0-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7b7d0-128">string</span></span><br/>  | <span data-ttu-id="7b7d0-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7b7d0-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="7b7d0-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7b7d0-130">DefaultValue</span></span><br/> | <span data-ttu-id="7b7d0-131">integer</span><span class="sxs-lookup"><span data-stu-id="7b7d0-131">integer</span></span><br/> | <span data-ttu-id="7b7d0-132">0</span><span class="sxs-lookup"><span data-stu-id="7b7d0-132">0</span></span><br/>               |
| <span data-ttu-id="7b7d0-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7b7d0-133">MaxValue</span></span><br/>     | <span data-ttu-id="7b7d0-134">integer</span><span class="sxs-lookup"><span data-stu-id="7b7d0-134">integer</span></span><br/> | <span data-ttu-id="7b7d0-135">359</span><span class="sxs-lookup"><span data-stu-id="7b7d0-135">359</span></span><br/>             |
| <span data-ttu-id="7b7d0-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="7b7d0-136">MinValue</span></span><br/>     | <span data-ttu-id="7b7d0-137">integer</span><span class="sxs-lookup"><span data-stu-id="7b7d0-137">integer</span></span><br/> | <span data-ttu-id="7b7d0-138">0</span><span class="sxs-lookup"><span data-stu-id="7b7d0-138">0</span></span><br/>               |
| <span data-ttu-id="7b7d0-139">Mehrere</span><span class="sxs-lookup"><span data-stu-id="7b7d0-139">Multiple</span></span><br/>     | <span data-ttu-id="7b7d0-140">integer</span><span class="sxs-lookup"><span data-stu-id="7b7d0-140">integer</span></span><br/> | <span data-ttu-id="7b7d0-141">1</span><span class="sxs-lookup"><span data-stu-id="7b7d0-141">1</span></span><br/>               |
| <span data-ttu-id="7b7d0-142">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="7b7d0-142">Mandatory</span></span><br/>    | <span data-ttu-id="7b7d0-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7b7d0-143">string</span></span><br/>  | <span data-ttu-id="7b7d0-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="7b7d0-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7b7d0-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="7b7d0-145">UnitType</span></span><br/>     | <span data-ttu-id="7b7d0-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7b7d0-146">string</span></span><br/>  | <span data-ttu-id="7b7d0-147">Grad</span><span class="sxs-lookup"><span data-stu-id="7b7d0-147">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7b7d0-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b7d0-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b7d0-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="7b7d0-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




