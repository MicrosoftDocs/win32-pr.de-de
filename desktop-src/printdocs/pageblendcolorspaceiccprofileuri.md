---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: "\"Pgeblendcolorspaceiccprofileuri\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a6143bd934ebcb75c3e5455a30c7365f1a89
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050741"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="10792-104">"Pgeblendcolorspaceiccprofileuri"</span><span class="sxs-lookup"><span data-stu-id="10792-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="10792-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="10792-105">This topic is not current.</span></span> <span data-ttu-id="10792-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="10792-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="10792-107">Gibt einen relativen URI-Verweis auf ein ICC-Profil an, das den für die Mischung zu verwendenden Farbraum definiert.</span><span class="sxs-lookup"><span data-stu-id="10792-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="10792-108">Der <Uri> ist ein absoluter Teile \_ Name relativ zum Paket Stamm.</span><span class="sxs-lookup"><span data-stu-id="10792-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="10792-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="10792-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="10792-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="10792-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="10792-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="10792-111">Element Information</span></span>



| <span data-ttu-id="10792-112">Name</span><span class="sxs-lookup"><span data-stu-id="10792-112">Name</span></span>                       |                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10792-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="10792-113">Element Type</span></span> <br/>   | <span data-ttu-id="10792-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="10792-114">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="10792-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="10792-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="10792-116">Seite</span><span class="sxs-lookup"><span data-stu-id="10792-116">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="10792-117">Notizen</span><span class="sxs-lookup"><span data-stu-id="10792-117">Notes</span></span> <br/>          | <span data-ttu-id="10792-118">Dies gilt nur für XPS-Dokumente und sollte nicht in beliebigen Print Tickets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10792-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="10792-119">Verknüpft mit dem Element "pgeblendcolorspace".</span><span class="sxs-lookup"><span data-stu-id="10792-119">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="10792-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="10792-120">Structure Content</span></span>

<span data-ttu-id="10792-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="10792-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlendColorSpaceICCProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="10792-122">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10792-122">Structure Properties</span></span>

<span data-ttu-id="10792-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="10792-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="10792-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="10792-124">Property</span></span>                | <span data-ttu-id="10792-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="10792-125">xsi:type</span></span>           | <span data-ttu-id="10792-126">Wert</span><span class="sxs-lookup"><span data-stu-id="10792-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="10792-127">DataType</span><span class="sxs-lookup"><span data-stu-id="10792-127">DataType</span></span><br/>     | <span data-ttu-id="10792-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="10792-128">string</span></span><br/>  | <span data-ttu-id="10792-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="10792-129">xs:string</span></span><br/>       |
| <span data-ttu-id="10792-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="10792-130">DefaultValue</span></span><br/> | <span data-ttu-id="10792-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="10792-131">string</span></span><br/>  | <span data-ttu-id="10792-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="10792-132">undefined</span></span><br/>       |
| <span data-ttu-id="10792-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="10792-133">MaxLength</span></span><br/>    | <span data-ttu-id="10792-134">integer</span><span class="sxs-lookup"><span data-stu-id="10792-134">integer</span></span><br/> | <span data-ttu-id="10792-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="10792-135">undefined</span></span><br/>       |
| <span data-ttu-id="10792-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="10792-136">MinLength</span></span><br/>    | <span data-ttu-id="10792-137">integer</span><span class="sxs-lookup"><span data-stu-id="10792-137">integer</span></span><br/> | <span data-ttu-id="10792-138">1</span><span class="sxs-lookup"><span data-stu-id="10792-138">1</span></span><br/>               |
| <span data-ttu-id="10792-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="10792-139">Mandatory</span></span><br/>    | <span data-ttu-id="10792-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="10792-140">string</span></span><br/>  | <span data-ttu-id="10792-141">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="10792-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="10792-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="10792-142">UnitType</span></span><br/>     | <span data-ttu-id="10792-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="10792-143">string</span></span><br/>  | <span data-ttu-id="10792-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="10792-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="10792-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10792-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10792-146">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="10792-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




