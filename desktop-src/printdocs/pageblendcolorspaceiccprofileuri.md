---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbf1233e172a81053baee0abe1e21d79064045a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997697"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="d66e8-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="d66e8-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="d66e8-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="d66e8-105">This topic is not current.</span></span> <span data-ttu-id="d66e8-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="d66e8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d66e8-107">Gibt einen relativen URI-Verweis auf ein MIXER-Profil an, das den Farbraum definiert, der für das Mischen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d66e8-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="d66e8-108"><Uri>ist ein absoluter \_ Teilname relativ zum Paketstamm.</span><span class="sxs-lookup"><span data-stu-id="d66e8-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="d66e8-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d66e8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d66e8-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="d66e8-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d66e8-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d66e8-111">Element Information</span></span>



| <span data-ttu-id="d66e8-112">Name</span><span class="sxs-lookup"><span data-stu-id="d66e8-112">Name</span></span> | <span data-ttu-id="d66e8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d66e8-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d66e8-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="d66e8-114">Element Type</span></span> <br/>   | <span data-ttu-id="d66e8-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d66e8-115">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="d66e8-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="d66e8-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d66e8-117">Seite</span><span class="sxs-lookup"><span data-stu-id="d66e8-117">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="d66e8-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d66e8-118">Notes</span></span> <br/>          | <span data-ttu-id="d66e8-119">Dies gilt nur für XPS-Dokumente und sollte nicht in beliebigen PrintTickets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d66e8-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="d66e8-120">Verknüpft mit dem PageBlendColorSpace-Element.</span><span class="sxs-lookup"><span data-stu-id="d66e8-120">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d66e8-121">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="d66e8-121">Structure Content</span></span>

<span data-ttu-id="d66e8-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="d66e8-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="d66e8-123">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="d66e8-123">Structure Properties</span></span>

<span data-ttu-id="d66e8-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d66e8-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d66e8-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d66e8-125">Property</span></span>                | <span data-ttu-id="d66e8-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d66e8-126">xsi:type</span></span>           | <span data-ttu-id="d66e8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d66e8-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d66e8-128">DataType</span><span class="sxs-lookup"><span data-stu-id="d66e8-128">DataType</span></span><br/>     | <span data-ttu-id="d66e8-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d66e8-129">string</span></span><br/>  | <span data-ttu-id="d66e8-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="d66e8-130">xs:string</span></span><br/>       |
| <span data-ttu-id="d66e8-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d66e8-131">DefaultValue</span></span><br/> | <span data-ttu-id="d66e8-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d66e8-132">string</span></span><br/>  | <span data-ttu-id="d66e8-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="d66e8-133">undefined</span></span><br/>       |
| <span data-ttu-id="d66e8-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="d66e8-134">MaxLength</span></span><br/>    | <span data-ttu-id="d66e8-135">integer</span><span class="sxs-lookup"><span data-stu-id="d66e8-135">integer</span></span><br/> | <span data-ttu-id="d66e8-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="d66e8-136">undefined</span></span><br/>       |
| <span data-ttu-id="d66e8-137">Minlength</span><span class="sxs-lookup"><span data-stu-id="d66e8-137">MinLength</span></span><br/>    | <span data-ttu-id="d66e8-138">integer</span><span class="sxs-lookup"><span data-stu-id="d66e8-138">integer</span></span><br/> | <span data-ttu-id="d66e8-139">1</span><span class="sxs-lookup"><span data-stu-id="d66e8-139">1</span></span><br/>               |
| <span data-ttu-id="d66e8-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="d66e8-140">Mandatory</span></span><br/>    | <span data-ttu-id="d66e8-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d66e8-141">string</span></span><br/>  | <span data-ttu-id="d66e8-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="d66e8-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d66e8-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="d66e8-143">UnitType</span></span><br/>     | <span data-ttu-id="d66e8-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d66e8-144">string</span></span><br/>  | <span data-ttu-id="d66e8-145">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="d66e8-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="d66e8-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d66e8-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d66e8-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="d66e8-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




