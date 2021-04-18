---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: "\"Pgewatermarktextcolor\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77e76dd1b304a46b2760565a09fe0134d3f0b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104530578"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="e92af-104">"Pgewatermarktextcolor"</span><span class="sxs-lookup"><span data-stu-id="e92af-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="e92af-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e92af-105">This topic is not current.</span></span> <span data-ttu-id="e92af-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e92af-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e92af-107">Definiert die sRGB-Farbe für den Wasserzeichen Text.</span><span class="sxs-lookup"><span data-stu-id="e92af-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="e92af-108">Das Format ist "ARGB: \# aarrggbb".</span><span class="sxs-lookup"><span data-stu-id="e92af-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="e92af-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e92af-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e92af-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e92af-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e92af-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e92af-111">Element Information</span></span>



| <span data-ttu-id="e92af-112">Name</span><span class="sxs-lookup"><span data-stu-id="e92af-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="e92af-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e92af-113">Element Type</span></span> <br/>   | <span data-ttu-id="e92af-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e92af-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="e92af-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="e92af-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e92af-116">Seite</span><span class="sxs-lookup"><span data-stu-id="e92af-116">Page</span></span><br/>                            |
| <span data-ttu-id="e92af-117">Notizen</span><span class="sxs-lookup"><span data-stu-id="e92af-117">Notes</span></span> <br/>          | <span data-ttu-id="e92af-118">Mit dem Element "pgewatermark" verknüpft</span><span class="sxs-lookup"><span data-stu-id="e92af-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e92af-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e92af-119">Structure Content</span></span>

<span data-ttu-id="e92af-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e92af-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e92af-121">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e92af-121">Structure Properties</span></span>

<span data-ttu-id="e92af-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e92af-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e92af-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e92af-123">Property</span></span>                | <span data-ttu-id="e92af-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e92af-124">xsi:type</span></span>           | <span data-ttu-id="e92af-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e92af-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e92af-126">DataType</span><span class="sxs-lookup"><span data-stu-id="e92af-126">DataType</span></span><br/>     | <span data-ttu-id="e92af-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e92af-127">string</span></span><br/>  | <span data-ttu-id="e92af-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e92af-128">xs:string</span></span><br/>       |
| <span data-ttu-id="e92af-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e92af-129">DefaultValue</span></span><br/> | <span data-ttu-id="e92af-130">integer</span><span class="sxs-lookup"><span data-stu-id="e92af-130">integer</span></span><br/> | <span data-ttu-id="e92af-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e92af-131">undefined</span></span><br/>       |
| <span data-ttu-id="e92af-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e92af-132">MaxValue</span></span><br/>     | <span data-ttu-id="e92af-133">integer</span><span class="sxs-lookup"><span data-stu-id="e92af-133">integer</span></span><br/> | <span data-ttu-id="e92af-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e92af-134">undefined</span></span><br/>       |
| <span data-ttu-id="e92af-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="e92af-135">MinValue</span></span><br/>     | <span data-ttu-id="e92af-136">integer</span><span class="sxs-lookup"><span data-stu-id="e92af-136">integer</span></span><br/> | <span data-ttu-id="e92af-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e92af-137">undefined</span></span><br/>       |
| <span data-ttu-id="e92af-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="e92af-138">Mandatory</span></span><br/>    | <span data-ttu-id="e92af-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e92af-139">string</span></span><br/>  | <span data-ttu-id="e92af-140">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="e92af-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e92af-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="e92af-141">UnitType</span></span><br/>     | <span data-ttu-id="e92af-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e92af-142">string</span></span><br/>  | <span data-ttu-id="e92af-143">sRGB</span><span class="sxs-lookup"><span data-stu-id="e92af-143">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="e92af-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e92af-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e92af-145">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="e92af-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




