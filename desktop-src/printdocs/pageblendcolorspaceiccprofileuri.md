---
description: Erfahren Sie mehr über den PageBlendColorSpaceICCProfileURI-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db89757737ff5aa6a1358af418ee33809b960e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549318"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="0bbf2-105">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="0bbf2-105">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="0bbf2-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0bbf2-106">This topic is not current.</span></span> <span data-ttu-id="0bbf2-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="0bbf2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0bbf2-108">Gibt einen relativen URI-Verweis auf ein MIXER-Profil an, das den Farbraum definiert, der für das Mischen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bbf2-108">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="0bbf2-109"><Uri>ist ein absoluter \_ Teilname relativ zum Paketstamm.</span><span class="sxs-lookup"><span data-stu-id="0bbf2-109">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="0bbf2-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0bbf2-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0bbf2-111">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="0bbf2-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0bbf2-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0bbf2-112">Element Information</span></span>



| <span data-ttu-id="0bbf2-113">Name</span><span class="sxs-lookup"><span data-stu-id="0bbf2-113">Name</span></span> | <span data-ttu-id="0bbf2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0bbf2-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbf2-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0bbf2-115">Element Type</span></span> <br/>   | <span data-ttu-id="0bbf2-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0bbf2-116">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="0bbf2-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="0bbf2-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0bbf2-118">Seite</span><span class="sxs-lookup"><span data-stu-id="0bbf2-118">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="0bbf2-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0bbf2-119">Notes</span></span> <br/>          | <span data-ttu-id="0bbf2-120">Dies gilt nur für XPS-Dokumente und sollte nicht in beliebigen PrintTickets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bbf2-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="0bbf2-121">Verknüpft mit dem PageBlendColorSpace-Element.</span><span class="sxs-lookup"><span data-stu-id="0bbf2-121">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0bbf2-122">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="0bbf2-122">Structure Content</span></span>

<span data-ttu-id="0bbf2-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="0bbf2-123">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0bbf2-124">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="0bbf2-124">Structure Properties</span></span>

<span data-ttu-id="0bbf2-125">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0bbf2-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0bbf2-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0bbf2-126">Property</span></span>                | <span data-ttu-id="0bbf2-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0bbf2-127">xsi:type</span></span>           | <span data-ttu-id="0bbf2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0bbf2-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0bbf2-129">DataType</span><span class="sxs-lookup"><span data-stu-id="0bbf2-129">DataType</span></span><br/>     | <span data-ttu-id="0bbf2-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0bbf2-130">string</span></span><br/>  | <span data-ttu-id="0bbf2-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="0bbf2-131">xs:string</span></span><br/>       |
| <span data-ttu-id="0bbf2-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0bbf2-132">DefaultValue</span></span><br/> | <span data-ttu-id="0bbf2-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0bbf2-133">string</span></span><br/>  | <span data-ttu-id="0bbf2-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="0bbf2-134">undefined</span></span><br/>       |
| <span data-ttu-id="0bbf2-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="0bbf2-135">MaxLength</span></span><br/>    | <span data-ttu-id="0bbf2-136">integer</span><span class="sxs-lookup"><span data-stu-id="0bbf2-136">integer</span></span><br/> | <span data-ttu-id="0bbf2-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="0bbf2-137">undefined</span></span><br/>       |
| <span data-ttu-id="0bbf2-138">Minlength</span><span class="sxs-lookup"><span data-stu-id="0bbf2-138">MinLength</span></span><br/>    | <span data-ttu-id="0bbf2-139">integer</span><span class="sxs-lookup"><span data-stu-id="0bbf2-139">integer</span></span><br/> | <span data-ttu-id="0bbf2-140">1</span><span class="sxs-lookup"><span data-stu-id="0bbf2-140">1</span></span><br/>               |
| <span data-ttu-id="0bbf2-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="0bbf2-141">Mandatory</span></span><br/>    | <span data-ttu-id="0bbf2-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0bbf2-142">string</span></span><br/>  | <span data-ttu-id="0bbf2-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="0bbf2-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0bbf2-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="0bbf2-144">UnitType</span></span><br/>     | <span data-ttu-id="0bbf2-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0bbf2-145">string</span></span><br/>  | <span data-ttu-id="0bbf2-146">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="0bbf2-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="0bbf2-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0bbf2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bbf2-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="0bbf2-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




