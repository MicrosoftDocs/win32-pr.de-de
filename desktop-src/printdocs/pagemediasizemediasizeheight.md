---
description: Abrufen von Informationen zum PageMediaSizeMediaSizeHeight-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: PageMediaSizeMediaSizeHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547077e7a63d91d6db43e8ebf6225a771bf237d8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395795"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="15617-105">PageMediaSizeMediaSizeHeight</span><span class="sxs-lookup"><span data-stu-id="15617-105">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="15617-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="15617-106">This topic is not current.</span></span> <span data-ttu-id="15617-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="15617-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="15617-108">Gibt die MediaSizeHeight-Dimensionsrichtung für die Option Custom MediaSize an.</span><span class="sxs-lookup"><span data-stu-id="15617-108">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="15617-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="15617-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="15617-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="15617-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="15617-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="15617-111">Element Information</span></span>



| <span data-ttu-id="15617-112">Name</span><span class="sxs-lookup"><span data-stu-id="15617-112">Name</span></span> | <span data-ttu-id="15617-113">Wert</span><span class="sxs-lookup"><span data-stu-id="15617-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="15617-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="15617-114">Element Type</span></span> <br/>   | <span data-ttu-id="15617-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="15617-115">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="15617-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="15617-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="15617-117">Seite</span><span class="sxs-lookup"><span data-stu-id="15617-117">Page</span></span><br/>                                           |
| <span data-ttu-id="15617-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15617-118">Notes</span></span> <br/>          | <span data-ttu-id="15617-119">Mit PageMediaSize-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="15617-119">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="15617-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="15617-120">Structure Content</span></span>

<span data-ttu-id="15617-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="15617-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="15617-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="15617-122">Structure Properties</span></span>

<span data-ttu-id="15617-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="15617-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="15617-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="15617-124">Property</span></span>                | <span data-ttu-id="15617-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="15617-125">xsi:type</span></span>           | <span data-ttu-id="15617-126">Wert</span><span class="sxs-lookup"><span data-stu-id="15617-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="15617-127">DataType</span><span class="sxs-lookup"><span data-stu-id="15617-127">DataType</span></span><br/>     | <span data-ttu-id="15617-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15617-128">string</span></span><br/>  | <span data-ttu-id="15617-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="15617-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="15617-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="15617-130">DefaultValue</span></span><br/> | <span data-ttu-id="15617-131">integer</span><span class="sxs-lookup"><span data-stu-id="15617-131">integer</span></span><br/> | <span data-ttu-id="15617-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="15617-132">undefined</span></span><br/>       |
| <span data-ttu-id="15617-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="15617-133">MaxValue</span></span><br/>     | <span data-ttu-id="15617-134">integer</span><span class="sxs-lookup"><span data-stu-id="15617-134">integer</span></span><br/> | <span data-ttu-id="15617-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="15617-135">undefined</span></span><br/>       |
| <span data-ttu-id="15617-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="15617-136">MinValue</span></span><br/>     | <span data-ttu-id="15617-137">integer</span><span class="sxs-lookup"><span data-stu-id="15617-137">integer</span></span><br/> | <span data-ttu-id="15617-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="15617-138">undefined</span></span><br/>       |
| <span data-ttu-id="15617-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="15617-139">Mandatory</span></span><br/>    | <span data-ttu-id="15617-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15617-140">string</span></span><br/>  | <span data-ttu-id="15617-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="15617-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="15617-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="15617-142">Multiple</span></span><br/>     | <span data-ttu-id="15617-143">integer</span><span class="sxs-lookup"><span data-stu-id="15617-143">integer</span></span><br/> | <span data-ttu-id="15617-144">1</span><span class="sxs-lookup"><span data-stu-id="15617-144">1</span></span><br/>               |
| <span data-ttu-id="15617-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="15617-145">UnitType</span></span><br/>     | <span data-ttu-id="15617-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="15617-146">string</span></span><br/>  | <span data-ttu-id="15617-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="15617-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="15617-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15617-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15617-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="15617-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




