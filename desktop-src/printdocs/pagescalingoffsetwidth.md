---
description: Abrufen von Informationen zum PageScalingOffsetWidth-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63152e6a3d9f8ea47bac3b5a0efe559e71e0cb35
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548848"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="ec245-105">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="ec245-105">PageScalingOffsetWidth</span></span>

<span data-ttu-id="ec245-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ec245-106">This topic is not current.</span></span> <span data-ttu-id="ec245-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="ec245-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ec245-108">Gibt den Skalierungsoffset in der Richtung ImageableSizeWidth für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="ec245-108">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="ec245-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ec245-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ec245-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ec245-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ec245-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ec245-111">Element Information</span></span>



| <span data-ttu-id="ec245-112">Name</span><span class="sxs-lookup"><span data-stu-id="ec245-112">Name</span></span> | <span data-ttu-id="ec245-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ec245-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="ec245-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ec245-114">Element Type</span></span> <br/>   | <span data-ttu-id="ec245-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ec245-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="ec245-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="ec245-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ec245-117">Seite</span><span class="sxs-lookup"><span data-stu-id="ec245-117">Page</span></span><br/>                                         |
| <span data-ttu-id="ec245-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec245-118">Notes</span></span> <br/>          | <span data-ttu-id="ec245-119">Mit PageScaling-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="ec245-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ec245-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ec245-120">Structure Content</span></span>

<span data-ttu-id="ec245-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="ec245-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="ec245-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="ec245-122">Structure Properties</span></span>

<span data-ttu-id="ec245-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ec245-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ec245-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ec245-124">Property</span></span>                | <span data-ttu-id="ec245-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ec245-125">xsi:type</span></span>           | <span data-ttu-id="ec245-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ec245-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ec245-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ec245-127">DataType</span></span><br/>     | <span data-ttu-id="ec245-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ec245-128">string</span></span><br/>  | <span data-ttu-id="ec245-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ec245-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="ec245-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ec245-130">DefaultValue</span></span><br/> | <span data-ttu-id="ec245-131">integer</span><span class="sxs-lookup"><span data-stu-id="ec245-131">integer</span></span><br/> | <span data-ttu-id="ec245-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ec245-132">undefined</span></span><br/>       |
| <span data-ttu-id="ec245-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ec245-133">MaxValue</span></span><br/>     | <span data-ttu-id="ec245-134">integer</span><span class="sxs-lookup"><span data-stu-id="ec245-134">integer</span></span><br/> | <span data-ttu-id="ec245-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ec245-135">undefined</span></span><br/>       |
| <span data-ttu-id="ec245-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="ec245-136">MinValue</span></span><br/>     | <span data-ttu-id="ec245-137">integer</span><span class="sxs-lookup"><span data-stu-id="ec245-137">integer</span></span><br/> | <span data-ttu-id="ec245-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ec245-138">undefined</span></span><br/>       |
| <span data-ttu-id="ec245-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ec245-139">Mandatory</span></span><br/>    | <span data-ttu-id="ec245-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ec245-140">string</span></span><br/>  | <span data-ttu-id="ec245-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="ec245-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ec245-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="ec245-142">Multiple</span></span><br/>     | <span data-ttu-id="ec245-143">integer</span><span class="sxs-lookup"><span data-stu-id="ec245-143">integer</span></span><br/> | <span data-ttu-id="ec245-144">1</span><span class="sxs-lookup"><span data-stu-id="ec245-144">1</span></span><br/>               |
| <span data-ttu-id="ec245-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="ec245-145">UnitType</span></span><br/>     | <span data-ttu-id="ec245-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ec245-146">string</span></span><br/>  | <span data-ttu-id="ec245-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="ec245-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ec245-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec245-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec245-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="ec245-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




