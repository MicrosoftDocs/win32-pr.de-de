---
description: Erfahren Sie mehr über den PageDestinationColorProfileURI-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3cf719a97f8f8086e88425c1667199815efbbb
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396675"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="eec17-105">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="eec17-105">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="eec17-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="eec17-106">This topic is not current.</span></span> <span data-ttu-id="eec17-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="eec17-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eec17-108">Gibt einen relativen URI-Verweis auf ein in einem XPS-Dokument enthaltenes XPS-Profil an.</span><span class="sxs-lookup"><span data-stu-id="eec17-108">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="eec17-109">Die Verarbeitung dieser Option hängt von der Einstellung des PageDeviceColorSpaceUsage-Features ab.</span><span class="sxs-lookup"><span data-stu-id="eec17-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="eec17-110">Bei allen Elementen, die dieses Profil verwenden, wird davon ausgegangen, dass sie sich bereits im entsprechenden Gerätefarbraum befinden und im Treiber oder Gerät nicht farblich verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="eec17-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="eec17-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="eec17-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eec17-112">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="eec17-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="eec17-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="eec17-113">Element Information</span></span>



| <span data-ttu-id="eec17-114">Name</span><span class="sxs-lookup"><span data-stu-id="eec17-114">Name</span></span> | <span data-ttu-id="eec17-115">Wert</span><span class="sxs-lookup"><span data-stu-id="eec17-115">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="eec17-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="eec17-116">Element Type</span></span> <br/>   | <span data-ttu-id="eec17-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="eec17-117">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="eec17-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="eec17-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eec17-119">Seite</span><span class="sxs-lookup"><span data-stu-id="eec17-119">Page</span></span><br/>                                          |
| <span data-ttu-id="eec17-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eec17-120">Notes</span></span> <br/>          | <span data-ttu-id="eec17-121">Verknüpft mit dem PageDestinationColorProfile-Element</span><span class="sxs-lookup"><span data-stu-id="eec17-121">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="eec17-122">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="eec17-122">Structure Content</span></span>

<span data-ttu-id="eec17-123">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="eec17-123">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="eec17-124">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="eec17-124">Structure Properties</span></span>

<span data-ttu-id="eec17-125">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eec17-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eec17-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eec17-126">Property</span></span>                | <span data-ttu-id="eec17-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="eec17-127">xsi:type</span></span>           | <span data-ttu-id="eec17-128">Wert</span><span class="sxs-lookup"><span data-stu-id="eec17-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="eec17-129">DataType</span><span class="sxs-lookup"><span data-stu-id="eec17-129">DataType</span></span><br/>     | <span data-ttu-id="eec17-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eec17-130">string</span></span><br/>  | <span data-ttu-id="eec17-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="eec17-131">xs:string</span></span><br/>       |
| <span data-ttu-id="eec17-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="eec17-132">DefaultValue</span></span><br/> | <span data-ttu-id="eec17-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eec17-133">string</span></span><br/>  | <span data-ttu-id="eec17-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="eec17-134">undefined</span></span><br/>       |
| <span data-ttu-id="eec17-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="eec17-135">MaxLength</span></span><br/>    | <span data-ttu-id="eec17-136">integer</span><span class="sxs-lookup"><span data-stu-id="eec17-136">integer</span></span><br/> | <span data-ttu-id="eec17-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="eec17-137">undefined</span></span><br/>       |
| <span data-ttu-id="eec17-138">Minlength</span><span class="sxs-lookup"><span data-stu-id="eec17-138">MinLength</span></span><br/>    | <span data-ttu-id="eec17-139">integer</span><span class="sxs-lookup"><span data-stu-id="eec17-139">integer</span></span><br/> | <span data-ttu-id="eec17-140">1</span><span class="sxs-lookup"><span data-stu-id="eec17-140">1</span></span><br/>               |
| <span data-ttu-id="eec17-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="eec17-141">Mandatory</span></span><br/>    | <span data-ttu-id="eec17-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eec17-142">string</span></span><br/>  | <span data-ttu-id="eec17-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="eec17-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="eec17-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="eec17-144">UnitType</span></span><br/>     | <span data-ttu-id="eec17-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eec17-145">string</span></span><br/>  | <span data-ttu-id="eec17-146">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="eec17-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="eec17-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eec17-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eec17-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="eec17-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




