---
description: Abrufen von Informationen zum PageScalingScaleWidth-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6180395eb656ee40d8558f7208fec2ad2fce8
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548798"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="a8cdd-105">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="a8cdd-105">PageScalingScaleWidth</span></span>

<span data-ttu-id="a8cdd-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a8cdd-106">This topic is not current.</span></span> <span data-ttu-id="a8cdd-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a8cdd-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a8cdd-108">Gibt den Skalierungsfaktor in der Richtung ImageableSizeWidth für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="a8cdd-108">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="a8cdd-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a8cdd-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a8cdd-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="a8cdd-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a8cdd-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a8cdd-111">Element Information</span></span>



| <span data-ttu-id="a8cdd-112">Name</span><span class="sxs-lookup"><span data-stu-id="a8cdd-112">Name</span></span> | <span data-ttu-id="a8cdd-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a8cdd-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="a8cdd-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a8cdd-114">Element Type</span></span> <br/>   | <span data-ttu-id="a8cdd-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a8cdd-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="a8cdd-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a8cdd-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a8cdd-117">Seite</span><span class="sxs-lookup"><span data-stu-id="a8cdd-117">Page</span></span><br/>                                         |
| <span data-ttu-id="a8cdd-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8cdd-118">Notes</span></span> <br/>          | <span data-ttu-id="a8cdd-119">Mit PageScaling-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="a8cdd-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a8cdd-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="a8cdd-120">Structure Content</span></span>

<span data-ttu-id="a8cdd-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="a8cdd-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleWidth">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="a8cdd-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8cdd-122">Structure Properties</span></span>

<span data-ttu-id="a8cdd-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a8cdd-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a8cdd-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a8cdd-124">Property</span></span>                | <span data-ttu-id="a8cdd-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a8cdd-125">xsi:type</span></span>           | <span data-ttu-id="a8cdd-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a8cdd-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a8cdd-127">DataType</span><span class="sxs-lookup"><span data-stu-id="a8cdd-127">DataType</span></span><br/>     | <span data-ttu-id="a8cdd-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a8cdd-128">String</span></span><br/>  | <span data-ttu-id="a8cdd-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a8cdd-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="a8cdd-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a8cdd-130">DefaultValue</span></span><br/> | <span data-ttu-id="a8cdd-131">Integer</span><span class="sxs-lookup"><span data-stu-id="a8cdd-131">Integer</span></span><br/> | <span data-ttu-id="a8cdd-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="a8cdd-132">undefined</span></span><br/>       |
| <span data-ttu-id="a8cdd-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a8cdd-133">MaxValue</span></span><br/>     | <span data-ttu-id="a8cdd-134">Integer</span><span class="sxs-lookup"><span data-stu-id="a8cdd-134">Integer</span></span><br/> | <span data-ttu-id="a8cdd-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="a8cdd-135">undefined</span></span><br/>       |
| <span data-ttu-id="a8cdd-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="a8cdd-136">MinValue</span></span><br/>     | <span data-ttu-id="a8cdd-137">Integer</span><span class="sxs-lookup"><span data-stu-id="a8cdd-137">Integer</span></span><br/> | <span data-ttu-id="a8cdd-138">1</span><span class="sxs-lookup"><span data-stu-id="a8cdd-138">1</span></span><br/>               |
| <span data-ttu-id="a8cdd-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="a8cdd-139">Mandatory</span></span><br/>    | <span data-ttu-id="a8cdd-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a8cdd-140">String</span></span><br/>  | <span data-ttu-id="a8cdd-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="a8cdd-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a8cdd-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="a8cdd-142">Multiple</span></span><br/>     | <span data-ttu-id="a8cdd-143">Integer</span><span class="sxs-lookup"><span data-stu-id="a8cdd-143">Integer</span></span><br/> | <span data-ttu-id="a8cdd-144">1</span><span class="sxs-lookup"><span data-stu-id="a8cdd-144">1</span></span><br/>               |
| <span data-ttu-id="a8cdd-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="a8cdd-145">UnitType</span></span><br/>     | <span data-ttu-id="a8cdd-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a8cdd-146">String</span></span><br/>  | <span data-ttu-id="a8cdd-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="a8cdd-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a8cdd-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a8cdd-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8cdd-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a8cdd-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




