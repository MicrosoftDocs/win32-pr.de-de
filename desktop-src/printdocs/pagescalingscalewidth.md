---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7918f1a466621377e57190e0b967980fec1a07e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363054"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="72bfb-104">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="72bfb-104">PageScalingScaleWidth</span></span>

<span data-ttu-id="72bfb-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="72bfb-105">This topic is not current.</span></span> <span data-ttu-id="72bfb-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="72bfb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="72bfb-107">Gibt den Skalierungsfaktor in der imageablesizewidth-Richtung für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="72bfb-107">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="72bfb-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="72bfb-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="72bfb-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="72bfb-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="72bfb-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="72bfb-110">Element Information</span></span>



| <span data-ttu-id="72bfb-111">Name</span><span class="sxs-lookup"><span data-stu-id="72bfb-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="72bfb-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="72bfb-112">Element Type</span></span> <br/>   | <span data-ttu-id="72bfb-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="72bfb-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="72bfb-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="72bfb-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="72bfb-115">Seite</span><span class="sxs-lookup"><span data-stu-id="72bfb-115">Page</span></span><br/>                                         |
| <span data-ttu-id="72bfb-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="72bfb-116">Notes</span></span> <br/>          | <span data-ttu-id="72bfb-117">Verknüpft mit PageScaling-Element, benutzerdefinierte Option</span><span class="sxs-lookup"><span data-stu-id="72bfb-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="72bfb-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="72bfb-118">Structure Content</span></span>

<span data-ttu-id="72bfb-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="72bfb-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleWidth">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="72bfb-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="72bfb-120">Structure Properties</span></span>

<span data-ttu-id="72bfb-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="72bfb-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="72bfb-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="72bfb-122">Property</span></span>                | <span data-ttu-id="72bfb-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="72bfb-123">xsi:type</span></span>           | <span data-ttu-id="72bfb-124">Wert</span><span class="sxs-lookup"><span data-stu-id="72bfb-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="72bfb-125">DataType</span><span class="sxs-lookup"><span data-stu-id="72bfb-125">DataType</span></span><br/>     | <span data-ttu-id="72bfb-126">String</span><span class="sxs-lookup"><span data-stu-id="72bfb-126">String</span></span><br/>  | <span data-ttu-id="72bfb-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="72bfb-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="72bfb-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="72bfb-128">DefaultValue</span></span><br/> | <span data-ttu-id="72bfb-129">Integer</span><span class="sxs-lookup"><span data-stu-id="72bfb-129">Integer</span></span><br/> | <span data-ttu-id="72bfb-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="72bfb-130">undefined</span></span><br/>       |
| <span data-ttu-id="72bfb-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="72bfb-131">MaxValue</span></span><br/>     | <span data-ttu-id="72bfb-132">Integer</span><span class="sxs-lookup"><span data-stu-id="72bfb-132">Integer</span></span><br/> | <span data-ttu-id="72bfb-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="72bfb-133">undefined</span></span><br/>       |
| <span data-ttu-id="72bfb-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="72bfb-134">MinValue</span></span><br/>     | <span data-ttu-id="72bfb-135">Integer</span><span class="sxs-lookup"><span data-stu-id="72bfb-135">Integer</span></span><br/> | <span data-ttu-id="72bfb-136">1</span><span class="sxs-lookup"><span data-stu-id="72bfb-136">1</span></span><br/>               |
| <span data-ttu-id="72bfb-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="72bfb-137">Mandatory</span></span><br/>    | <span data-ttu-id="72bfb-138">String</span><span class="sxs-lookup"><span data-stu-id="72bfb-138">String</span></span><br/>  | <span data-ttu-id="72bfb-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="72bfb-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="72bfb-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="72bfb-140">Multiple</span></span><br/>     | <span data-ttu-id="72bfb-141">Integer</span><span class="sxs-lookup"><span data-stu-id="72bfb-141">Integer</span></span><br/> | <span data-ttu-id="72bfb-142">1</span><span class="sxs-lookup"><span data-stu-id="72bfb-142">1</span></span><br/>               |
| <span data-ttu-id="72bfb-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="72bfb-143">UnitType</span></span><br/>     | <span data-ttu-id="72bfb-144">String</span><span class="sxs-lookup"><span data-stu-id="72bfb-144">String</span></span><br/>  | <span data-ttu-id="72bfb-145">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="72bfb-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="72bfb-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72bfb-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72bfb-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="72bfb-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




