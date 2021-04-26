---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b321cba1608b1098dcc91f3800ef11f4968fb3f2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996097"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="0576a-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="0576a-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="0576a-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0576a-105">This topic is not current.</span></span> <span data-ttu-id="0576a-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="0576a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0576a-107">Gibt einen relativen URI-Verweis auf ein INTS-Profil an, das in einem XPS-Dokument enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0576a-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="0576a-108">Die Verarbeitung dieser Option hängt von der Einstellung des Features PageDeviceColorSpaceUsage ab.</span><span class="sxs-lookup"><span data-stu-id="0576a-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="0576a-109">Es wird davon ausgegangen, dass sich alle Elemente, die dieses Profil verwenden, bereits im entsprechenden Gerätefarbraum befinden und nicht im Treiber oder Gerät farblich verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="0576a-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="0576a-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0576a-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0576a-111">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="0576a-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0576a-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0576a-112">Element Information</span></span>



| <span data-ttu-id="0576a-113">Name</span><span class="sxs-lookup"><span data-stu-id="0576a-113">Name</span></span> | <span data-ttu-id="0576a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0576a-114">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="0576a-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0576a-115">Element Type</span></span> <br/>   | <span data-ttu-id="0576a-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0576a-116">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="0576a-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="0576a-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0576a-118">Seite</span><span class="sxs-lookup"><span data-stu-id="0576a-118">Page</span></span><br/>                                          |
| <span data-ttu-id="0576a-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0576a-119">Notes</span></span> <br/>          | <span data-ttu-id="0576a-120">Mit PageDestinationColorProfile-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="0576a-120">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0576a-121">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="0576a-121">Structure Content</span></span>

<span data-ttu-id="0576a-122">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="0576a-122">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="0576a-123">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="0576a-123">Structure Properties</span></span>

<span data-ttu-id="0576a-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0576a-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0576a-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0576a-125">Property</span></span>                | <span data-ttu-id="0576a-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0576a-126">xsi:type</span></span>           | <span data-ttu-id="0576a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0576a-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0576a-128">DataType</span><span class="sxs-lookup"><span data-stu-id="0576a-128">DataType</span></span><br/>     | <span data-ttu-id="0576a-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0576a-129">string</span></span><br/>  | <span data-ttu-id="0576a-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="0576a-130">xs:string</span></span><br/>       |
| <span data-ttu-id="0576a-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0576a-131">DefaultValue</span></span><br/> | <span data-ttu-id="0576a-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0576a-132">string</span></span><br/>  | <span data-ttu-id="0576a-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="0576a-133">undefined</span></span><br/>       |
| <span data-ttu-id="0576a-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="0576a-134">MaxLength</span></span><br/>    | <span data-ttu-id="0576a-135">integer</span><span class="sxs-lookup"><span data-stu-id="0576a-135">integer</span></span><br/> | <span data-ttu-id="0576a-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="0576a-136">undefined</span></span><br/>       |
| <span data-ttu-id="0576a-137">Minlength</span><span class="sxs-lookup"><span data-stu-id="0576a-137">MinLength</span></span><br/>    | <span data-ttu-id="0576a-138">integer</span><span class="sxs-lookup"><span data-stu-id="0576a-138">integer</span></span><br/> | <span data-ttu-id="0576a-139">1</span><span class="sxs-lookup"><span data-stu-id="0576a-139">1</span></span><br/>               |
| <span data-ttu-id="0576a-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="0576a-140">Mandatory</span></span><br/>    | <span data-ttu-id="0576a-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0576a-141">string</span></span><br/>  | <span data-ttu-id="0576a-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="0576a-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0576a-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="0576a-143">UnitType</span></span><br/>     | <span data-ttu-id="0576a-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0576a-144">string</span></span><br/>  | <span data-ttu-id="0576a-145">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="0576a-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="0576a-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0576a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0576a-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="0576a-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




