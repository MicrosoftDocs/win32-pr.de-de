---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: "\"Pgewatermarktextangle\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916e409040f0c7163f1168d48581270f077aaa3a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219076"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="22dde-104">"Pgewatermarktextangle"</span><span class="sxs-lookup"><span data-stu-id="22dde-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="22dde-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="22dde-105">This topic is not current.</span></span> <span data-ttu-id="22dde-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="22dde-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="22dde-107">Gibt den Winkel des Wasserzeichen Texts relativ zur pageimageablesizewidth-Richtung an.</span><span class="sxs-lookup"><span data-stu-id="22dde-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="22dde-108">Der Winkel wird in der Richtung gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="22dde-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="22dde-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="22dde-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="22dde-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="22dde-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="22dde-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="22dde-111">Element Information</span></span>



| <span data-ttu-id="22dde-112">Name</span><span class="sxs-lookup"><span data-stu-id="22dde-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="22dde-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="22dde-113">Element Type</span></span> <br/>   | <span data-ttu-id="22dde-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="22dde-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="22dde-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="22dde-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="22dde-116">Seite</span><span class="sxs-lookup"><span data-stu-id="22dde-116">Page</span></span><br/>                            |
| <span data-ttu-id="22dde-117">Notizen</span><span class="sxs-lookup"><span data-stu-id="22dde-117">Notes</span></span> <br/>          | <span data-ttu-id="22dde-118">Mit dem Element "pgewatermark" verknüpft</span><span class="sxs-lookup"><span data-stu-id="22dde-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="22dde-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="22dde-119">Structure Content</span></span>

<span data-ttu-id="22dde-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="22dde-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="22dde-121">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22dde-121">Structure Properties</span></span>

<span data-ttu-id="22dde-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="22dde-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="22dde-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22dde-123">Property</span></span>                | <span data-ttu-id="22dde-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="22dde-124">xsi:type</span></span>           | <span data-ttu-id="22dde-125">Wert</span><span class="sxs-lookup"><span data-stu-id="22dde-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="22dde-126">DataType</span><span class="sxs-lookup"><span data-stu-id="22dde-126">DataType</span></span><br/>     | <span data-ttu-id="22dde-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22dde-127">string</span></span><br/>  | <span data-ttu-id="22dde-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="22dde-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="22dde-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="22dde-129">DefaultValue</span></span><br/> | <span data-ttu-id="22dde-130">integer</span><span class="sxs-lookup"><span data-stu-id="22dde-130">integer</span></span><br/> | <span data-ttu-id="22dde-131">0</span><span class="sxs-lookup"><span data-stu-id="22dde-131">0</span></span><br/>               |
| <span data-ttu-id="22dde-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="22dde-132">MaxValue</span></span><br/>     | <span data-ttu-id="22dde-133">integer</span><span class="sxs-lookup"><span data-stu-id="22dde-133">integer</span></span><br/> | <span data-ttu-id="22dde-134">359</span><span class="sxs-lookup"><span data-stu-id="22dde-134">359</span></span><br/>             |
| <span data-ttu-id="22dde-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="22dde-135">MinValue</span></span><br/>     | <span data-ttu-id="22dde-136">integer</span><span class="sxs-lookup"><span data-stu-id="22dde-136">integer</span></span><br/> | <span data-ttu-id="22dde-137">0</span><span class="sxs-lookup"><span data-stu-id="22dde-137">0</span></span><br/>               |
| <span data-ttu-id="22dde-138">Mehrere</span><span class="sxs-lookup"><span data-stu-id="22dde-138">Multiple</span></span><br/>     | <span data-ttu-id="22dde-139">integer</span><span class="sxs-lookup"><span data-stu-id="22dde-139">integer</span></span><br/> | <span data-ttu-id="22dde-140">1</span><span class="sxs-lookup"><span data-stu-id="22dde-140">1</span></span><br/>               |
| <span data-ttu-id="22dde-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="22dde-141">Mandatory</span></span><br/>    | <span data-ttu-id="22dde-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22dde-142">string</span></span><br/>  | <span data-ttu-id="22dde-143">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="22dde-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="22dde-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="22dde-144">UnitType</span></span><br/>     | <span data-ttu-id="22dde-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22dde-145">string</span></span><br/>  | <span data-ttu-id="22dde-146">Grad</span><span class="sxs-lookup"><span data-stu-id="22dde-146">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="22dde-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22dde-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22dde-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="22dde-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




