---
description: Abrufen von Informationen zum PageScalingOffsetHeight-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f02370d28716dd3a8840001959bb7d963307d2f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548958"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="602b9-105">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="602b9-105">PageScalingOffsetHeight</span></span>

<span data-ttu-id="602b9-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="602b9-106">This topic is not current.</span></span> <span data-ttu-id="602b9-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="602b9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="602b9-108">Gibt den Skalierungsoffset in der Richtung ImageableSizeHeight für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="602b9-108">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="602b9-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="602b9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="602b9-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="602b9-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="602b9-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="602b9-111">Element Information</span></span>



| <span data-ttu-id="602b9-112">Name</span><span class="sxs-lookup"><span data-stu-id="602b9-112">Name</span></span> | <span data-ttu-id="602b9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="602b9-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="602b9-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="602b9-114">Element Type</span></span> <br/>   | <span data-ttu-id="602b9-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="602b9-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="602b9-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="602b9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="602b9-117">Seite</span><span class="sxs-lookup"><span data-stu-id="602b9-117">Page</span></span><br/>                                         |
| <span data-ttu-id="602b9-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="602b9-118">Notes</span></span> <br/>          | <span data-ttu-id="602b9-119">Mit PageScaling-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="602b9-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="602b9-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="602b9-120">Structure Content</span></span>

<span data-ttu-id="602b9-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="602b9-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetHeight">
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
    <psf:Value xsi:type="xs:decimal">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="602b9-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="602b9-122">Structure Properties</span></span>

<span data-ttu-id="602b9-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="602b9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="602b9-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="602b9-124">Property</span></span>                | <span data-ttu-id="602b9-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="602b9-125">xsi:type</span></span>           | <span data-ttu-id="602b9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="602b9-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="602b9-127">DataType</span><span class="sxs-lookup"><span data-stu-id="602b9-127">DataType</span></span><br/>     | <span data-ttu-id="602b9-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="602b9-128">string</span></span><br/>  | <span data-ttu-id="602b9-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="602b9-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="602b9-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="602b9-130">DefaultValue</span></span><br/> | <span data-ttu-id="602b9-131">integer</span><span class="sxs-lookup"><span data-stu-id="602b9-131">integer</span></span><br/> | <span data-ttu-id="602b9-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="602b9-132">undefined</span></span><br/>       |
| <span data-ttu-id="602b9-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="602b9-133">MaxValue</span></span><br/>     | <span data-ttu-id="602b9-134">integer</span><span class="sxs-lookup"><span data-stu-id="602b9-134">integer</span></span><br/> | <span data-ttu-id="602b9-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="602b9-135">undefined</span></span><br/>       |
| <span data-ttu-id="602b9-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="602b9-136">MinValue</span></span><br/>     | <span data-ttu-id="602b9-137">integer</span><span class="sxs-lookup"><span data-stu-id="602b9-137">integer</span></span><br/> | <span data-ttu-id="602b9-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="602b9-138">undefined</span></span><br/>       |
| <span data-ttu-id="602b9-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="602b9-139">Mandatory</span></span><br/>    | <span data-ttu-id="602b9-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="602b9-140">string</span></span><br/>  | <span data-ttu-id="602b9-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="602b9-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="602b9-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="602b9-142">Multiple</span></span><br/>     | <span data-ttu-id="602b9-143">integer</span><span class="sxs-lookup"><span data-stu-id="602b9-143">integer</span></span><br/> | <span data-ttu-id="602b9-144">1</span><span class="sxs-lookup"><span data-stu-id="602b9-144">1</span></span><br/>               |
| <span data-ttu-id="602b9-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="602b9-145">UnitType</span></span><br/>     | <span data-ttu-id="602b9-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="602b9-146">string</span></span><br/>  | <span data-ttu-id="602b9-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="602b9-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="602b9-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="602b9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="602b9-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="602b9-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




