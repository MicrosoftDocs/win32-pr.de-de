---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: PageMediaSizeMediaSizeHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 305f67179343fa4acb2fa784113d63d5d2333b0b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993707"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="5f16c-104">PageMediaSizeMediaSizeHeight</span><span class="sxs-lookup"><span data-stu-id="5f16c-104">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="5f16c-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5f16c-105">This topic is not current.</span></span> <span data-ttu-id="5f16c-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="5f16c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5f16c-107">Gibt die MediaSizeHeight-Dimensionsrichtung für die Option Custom MediaSize an.</span><span class="sxs-lookup"><span data-stu-id="5f16c-107">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="5f16c-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5f16c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5f16c-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="5f16c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5f16c-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5f16c-110">Element Information</span></span>



| <span data-ttu-id="5f16c-111">Name</span><span class="sxs-lookup"><span data-stu-id="5f16c-111">Name</span></span> | <span data-ttu-id="5f16c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5f16c-112">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="5f16c-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="5f16c-113">Element Type</span></span> <br/>   | <span data-ttu-id="5f16c-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5f16c-114">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="5f16c-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="5f16c-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5f16c-116">Seite</span><span class="sxs-lookup"><span data-stu-id="5f16c-116">Page</span></span><br/>                                           |
| <span data-ttu-id="5f16c-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f16c-117">Notes</span></span> <br/>          | <span data-ttu-id="5f16c-118">Mit PageMediaSize-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="5f16c-118">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5f16c-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="5f16c-119">Structure Content</span></span>

<span data-ttu-id="5f16c-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="5f16c-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5f16c-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f16c-121">Structure Properties</span></span>

<span data-ttu-id="5f16c-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5f16c-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5f16c-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5f16c-123">Property</span></span>                | <span data-ttu-id="5f16c-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5f16c-124">xsi:type</span></span>           | <span data-ttu-id="5f16c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5f16c-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5f16c-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5f16c-126">DataType</span></span><br/>     | <span data-ttu-id="5f16c-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5f16c-127">string</span></span><br/>  | <span data-ttu-id="5f16c-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5f16c-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="5f16c-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5f16c-129">DefaultValue</span></span><br/> | <span data-ttu-id="5f16c-130">integer</span><span class="sxs-lookup"><span data-stu-id="5f16c-130">integer</span></span><br/> | <span data-ttu-id="5f16c-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="5f16c-131">undefined</span></span><br/>       |
| <span data-ttu-id="5f16c-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5f16c-132">MaxValue</span></span><br/>     | <span data-ttu-id="5f16c-133">integer</span><span class="sxs-lookup"><span data-stu-id="5f16c-133">integer</span></span><br/> | <span data-ttu-id="5f16c-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="5f16c-134">undefined</span></span><br/>       |
| <span data-ttu-id="5f16c-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="5f16c-135">MinValue</span></span><br/>     | <span data-ttu-id="5f16c-136">integer</span><span class="sxs-lookup"><span data-stu-id="5f16c-136">integer</span></span><br/> | <span data-ttu-id="5f16c-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="5f16c-137">undefined</span></span><br/>       |
| <span data-ttu-id="5f16c-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="5f16c-138">Mandatory</span></span><br/>    | <span data-ttu-id="5f16c-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5f16c-139">string</span></span><br/>  | <span data-ttu-id="5f16c-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="5f16c-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5f16c-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="5f16c-141">Multiple</span></span><br/>     | <span data-ttu-id="5f16c-142">integer</span><span class="sxs-lookup"><span data-stu-id="5f16c-142">integer</span></span><br/> | <span data-ttu-id="5f16c-143">1</span><span class="sxs-lookup"><span data-stu-id="5f16c-143">1</span></span><br/>               |
| <span data-ttu-id="5f16c-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="5f16c-144">UnitType</span></span><br/>     | <span data-ttu-id="5f16c-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5f16c-145">string</span></span><br/>  | <span data-ttu-id="5f16c-146">Mikron</span><span class="sxs-lookup"><span data-stu-id="5f16c-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5f16c-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f16c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f16c-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="5f16c-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




