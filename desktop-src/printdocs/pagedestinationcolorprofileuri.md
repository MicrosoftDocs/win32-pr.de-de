---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: Pagedestinationcolorprofileuri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fff2ca269eaed9331f6c2077e6b396cca5a01c4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353648"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="1daa8-104">Pagedestinationcolorprofileuri</span><span class="sxs-lookup"><span data-stu-id="1daa8-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="1daa8-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="1daa8-105">This topic is not current.</span></span> <span data-ttu-id="1daa8-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1daa8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1daa8-107">Gibt einen relativen URI-Verweis auf ein in einem XPS-Dokument enthaltenes ICC-Profil an.</span><span class="sxs-lookup"><span data-stu-id="1daa8-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="1daa8-108">Die Verarbeitung dieser Option hängt von der Einstellung der pagedevicecolorspaceusage-Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="1daa8-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="1daa8-109">Es wird davon ausgegangen, dass alle Elemente, die dieses Profil verwenden, sich bereits im entsprechenden Geräte Farbraum befinden und im Treiber oder Gerät nicht farblich verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="1daa8-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="1daa8-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1daa8-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1daa8-111">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="1daa8-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1daa8-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1daa8-112">Element Information</span></span>



| <span data-ttu-id="1daa8-113">Name</span><span class="sxs-lookup"><span data-stu-id="1daa8-113">Name</span></span>                       |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="1daa8-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="1daa8-114">Element Type</span></span> <br/>   | <span data-ttu-id="1daa8-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1daa8-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="1daa8-116">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="1daa8-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1daa8-117">Seite</span><span class="sxs-lookup"><span data-stu-id="1daa8-117">Page</span></span><br/>                                          |
| <span data-ttu-id="1daa8-118">Notizen</span><span class="sxs-lookup"><span data-stu-id="1daa8-118">Notes</span></span> <br/>          | <span data-ttu-id="1daa8-119">Verknüpft mit pagedestinationcolorprofile-Element</span><span class="sxs-lookup"><span data-stu-id="1daa8-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1daa8-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="1daa8-120">Structure Content</span></span>

<span data-ttu-id="1daa8-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="1daa8-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1daa8-122">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1daa8-122">Structure Properties</span></span>

<span data-ttu-id="1daa8-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1daa8-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1daa8-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1daa8-124">Property</span></span>                | <span data-ttu-id="1daa8-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1daa8-125">xsi:type</span></span>           | <span data-ttu-id="1daa8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1daa8-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1daa8-127">DataType</span><span class="sxs-lookup"><span data-stu-id="1daa8-127">DataType</span></span><br/>     | <span data-ttu-id="1daa8-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1daa8-128">string</span></span><br/>  | <span data-ttu-id="1daa8-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="1daa8-129">xs:string</span></span><br/>       |
| <span data-ttu-id="1daa8-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1daa8-130">DefaultValue</span></span><br/> | <span data-ttu-id="1daa8-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1daa8-131">string</span></span><br/>  | <span data-ttu-id="1daa8-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="1daa8-132">undefined</span></span><br/>       |
| <span data-ttu-id="1daa8-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="1daa8-133">MaxLength</span></span><br/>    | <span data-ttu-id="1daa8-134">integer</span><span class="sxs-lookup"><span data-stu-id="1daa8-134">integer</span></span><br/> | <span data-ttu-id="1daa8-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="1daa8-135">undefined</span></span><br/>       |
| <span data-ttu-id="1daa8-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="1daa8-136">MinLength</span></span><br/>    | <span data-ttu-id="1daa8-137">integer</span><span class="sxs-lookup"><span data-stu-id="1daa8-137">integer</span></span><br/> | <span data-ttu-id="1daa8-138">1</span><span class="sxs-lookup"><span data-stu-id="1daa8-138">1</span></span><br/>               |
| <span data-ttu-id="1daa8-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="1daa8-139">Mandatory</span></span><br/>    | <span data-ttu-id="1daa8-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1daa8-140">string</span></span><br/>  | <span data-ttu-id="1daa8-141">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="1daa8-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1daa8-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="1daa8-142">UnitType</span></span><br/>     | <span data-ttu-id="1daa8-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1daa8-143">string</span></span><br/>  | <span data-ttu-id="1daa8-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="1daa8-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="1daa8-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1daa8-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1daa8-146">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="1daa8-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




