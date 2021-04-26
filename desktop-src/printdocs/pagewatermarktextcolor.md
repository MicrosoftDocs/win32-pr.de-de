---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2cc4d4f88724080b09ef52d7ded781039ff852
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996887"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="e44ac-104">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="e44ac-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="e44ac-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e44ac-105">This topic is not current.</span></span> <span data-ttu-id="e44ac-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="e44ac-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e44ac-107">Definiert die sRGB-Farbe für den Wasserzeichentext.</span><span class="sxs-lookup"><span data-stu-id="e44ac-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="e44ac-108">Das Format ist ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="e44ac-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="e44ac-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e44ac-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e44ac-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e44ac-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e44ac-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e44ac-111">Element Information</span></span>



| <span data-ttu-id="e44ac-112">Name</span><span class="sxs-lookup"><span data-stu-id="e44ac-112">Name</span></span> | <span data-ttu-id="e44ac-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e44ac-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="e44ac-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e44ac-114">Element Type</span></span> <br/>   | <span data-ttu-id="e44ac-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e44ac-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="e44ac-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="e44ac-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e44ac-117">Seite</span><span class="sxs-lookup"><span data-stu-id="e44ac-117">Page</span></span><br/>                            |
| <span data-ttu-id="e44ac-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e44ac-118">Notes</span></span> <br/>          | <span data-ttu-id="e44ac-119">Mit PageWatermark-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="e44ac-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e44ac-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e44ac-120">Structure Content</span></span>

<span data-ttu-id="e44ac-121">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e44ac-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="e44ac-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="e44ac-122">Structure Properties</span></span>

<span data-ttu-id="e44ac-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e44ac-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e44ac-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e44ac-124">Property</span></span>                | <span data-ttu-id="e44ac-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e44ac-125">xsi:type</span></span>           | <span data-ttu-id="e44ac-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e44ac-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e44ac-127">DataType</span><span class="sxs-lookup"><span data-stu-id="e44ac-127">DataType</span></span><br/>     | <span data-ttu-id="e44ac-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e44ac-128">string</span></span><br/>  | <span data-ttu-id="e44ac-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="e44ac-129">xs:string</span></span><br/>       |
| <span data-ttu-id="e44ac-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e44ac-130">DefaultValue</span></span><br/> | <span data-ttu-id="e44ac-131">integer</span><span class="sxs-lookup"><span data-stu-id="e44ac-131">integer</span></span><br/> | <span data-ttu-id="e44ac-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e44ac-132">undefined</span></span><br/>       |
| <span data-ttu-id="e44ac-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e44ac-133">MaxValue</span></span><br/>     | <span data-ttu-id="e44ac-134">integer</span><span class="sxs-lookup"><span data-stu-id="e44ac-134">integer</span></span><br/> | <span data-ttu-id="e44ac-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e44ac-135">undefined</span></span><br/>       |
| <span data-ttu-id="e44ac-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="e44ac-136">MinValue</span></span><br/>     | <span data-ttu-id="e44ac-137">integer</span><span class="sxs-lookup"><span data-stu-id="e44ac-137">integer</span></span><br/> | <span data-ttu-id="e44ac-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e44ac-138">undefined</span></span><br/>       |
| <span data-ttu-id="e44ac-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="e44ac-139">Mandatory</span></span><br/>    | <span data-ttu-id="e44ac-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e44ac-140">string</span></span><br/>  | <span data-ttu-id="e44ac-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="e44ac-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e44ac-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="e44ac-142">UnitType</span></span><br/>     | <span data-ttu-id="e44ac-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e44ac-143">string</span></span><br/>  | <span data-ttu-id="e44ac-144">Srgb</span><span class="sxs-lookup"><span data-stu-id="e44ac-144">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="e44ac-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e44ac-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e44ac-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="e44ac-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




