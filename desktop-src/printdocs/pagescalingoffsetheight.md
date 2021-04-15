---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: Pagescalingoffertheight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a475f7fa68cd961d9d7a7f42e40fc9ea80a72a4e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393870"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="4ee9f-104">Pagescalingoffertheight</span><span class="sxs-lookup"><span data-stu-id="4ee9f-104">PageScalingOffsetHeight</span></span>

<span data-ttu-id="4ee9f-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4ee9f-105">This topic is not current.</span></span> <span data-ttu-id="4ee9f-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4ee9f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4ee9f-107">Gibt den Skalierungs Offset in der imageablesizeheight-Richtung für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="4ee9f-107">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="4ee9f-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4ee9f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4ee9f-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4ee9f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4ee9f-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4ee9f-110">Element Information</span></span>



| <span data-ttu-id="4ee9f-111">Name</span><span class="sxs-lookup"><span data-stu-id="4ee9f-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="4ee9f-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4ee9f-112">Element Type</span></span> <br/>   | <span data-ttu-id="4ee9f-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4ee9f-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="4ee9f-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="4ee9f-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4ee9f-115">Seite</span><span class="sxs-lookup"><span data-stu-id="4ee9f-115">Page</span></span><br/>                                         |
| <span data-ttu-id="4ee9f-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ee9f-116">Notes</span></span> <br/>          | <span data-ttu-id="4ee9f-117">Verknüpft mit PageScaling-Element, benutzerdefinierte Option</span><span class="sxs-lookup"><span data-stu-id="4ee9f-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4ee9f-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4ee9f-118">Structure Content</span></span>

<span data-ttu-id="4ee9f-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="4ee9f-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetHeight">
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
    <psf:Value xsi:type="xs:decimal">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="4ee9f-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ee9f-120">Structure Properties</span></span>

<span data-ttu-id="4ee9f-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4ee9f-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4ee9f-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4ee9f-122">Property</span></span>                | <span data-ttu-id="4ee9f-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4ee9f-123">xsi:type</span></span>           | <span data-ttu-id="4ee9f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4ee9f-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4ee9f-125">DataType</span><span class="sxs-lookup"><span data-stu-id="4ee9f-125">DataType</span></span><br/>     | <span data-ttu-id="4ee9f-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ee9f-126">string</span></span><br/>  | <span data-ttu-id="4ee9f-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4ee9f-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="4ee9f-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4ee9f-128">DefaultValue</span></span><br/> | <span data-ttu-id="4ee9f-129">integer</span><span class="sxs-lookup"><span data-stu-id="4ee9f-129">integer</span></span><br/> | <span data-ttu-id="4ee9f-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4ee9f-130">undefined</span></span><br/>       |
| <span data-ttu-id="4ee9f-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4ee9f-131">MaxValue</span></span><br/>     | <span data-ttu-id="4ee9f-132">integer</span><span class="sxs-lookup"><span data-stu-id="4ee9f-132">integer</span></span><br/> | <span data-ttu-id="4ee9f-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4ee9f-133">undefined</span></span><br/>       |
| <span data-ttu-id="4ee9f-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="4ee9f-134">MinValue</span></span><br/>     | <span data-ttu-id="4ee9f-135">integer</span><span class="sxs-lookup"><span data-stu-id="4ee9f-135">integer</span></span><br/> | <span data-ttu-id="4ee9f-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4ee9f-136">undefined</span></span><br/>       |
| <span data-ttu-id="4ee9f-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="4ee9f-137">Mandatory</span></span><br/>    | <span data-ttu-id="4ee9f-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ee9f-138">string</span></span><br/>  | <span data-ttu-id="4ee9f-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="4ee9f-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4ee9f-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="4ee9f-140">Multiple</span></span><br/>     | <span data-ttu-id="4ee9f-141">integer</span><span class="sxs-lookup"><span data-stu-id="4ee9f-141">integer</span></span><br/> | <span data-ttu-id="4ee9f-142">1</span><span class="sxs-lookup"><span data-stu-id="4ee9f-142">1</span></span><br/>               |
| <span data-ttu-id="4ee9f-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="4ee9f-143">UnitType</span></span><br/>     | <span data-ttu-id="4ee9f-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ee9f-144">string</span></span><br/>  | <span data-ttu-id="4ee9f-145">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="4ee9f-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4ee9f-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ee9f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ee9f-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="4ee9f-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




