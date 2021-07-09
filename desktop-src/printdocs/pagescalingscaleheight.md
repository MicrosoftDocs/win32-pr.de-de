---
description: Abrufen von Informationen zum PageScalingScaleHeight-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51bdb5577b5e3863cfadab1fa9eb74ff40d54da
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548838"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="6a589-105">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="6a589-105">PageScalingScaleHeight</span></span>

<span data-ttu-id="6a589-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="6a589-106">This topic is not current.</span></span> <span data-ttu-id="6a589-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="6a589-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6a589-108">Gibt den Skalierungsfaktor in der Richtung ImageableSizeHeight für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="6a589-108">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="6a589-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6a589-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6a589-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="6a589-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6a589-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6a589-111">Element Information</span></span>



| <span data-ttu-id="6a589-112">Name</span><span class="sxs-lookup"><span data-stu-id="6a589-112">Name</span></span> | <span data-ttu-id="6a589-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6a589-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="6a589-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="6a589-114">Element Type</span></span> <br/>   | <span data-ttu-id="6a589-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6a589-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="6a589-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="6a589-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6a589-117">Seite</span><span class="sxs-lookup"><span data-stu-id="6a589-117">Page</span></span><br/>                                         |
| <span data-ttu-id="6a589-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a589-118">Notes</span></span> <br/>          | <span data-ttu-id="6a589-119">Mit PageScaling-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="6a589-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6a589-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="6a589-120">Structure Content</span></span>

<span data-ttu-id="6a589-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="6a589-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="6a589-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a589-122">Structure Properties</span></span>

<span data-ttu-id="6a589-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6a589-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6a589-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a589-124">Property</span></span>                | <span data-ttu-id="6a589-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6a589-125">xsi:type</span></span>           | <span data-ttu-id="6a589-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6a589-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6a589-127">DataType</span><span class="sxs-lookup"><span data-stu-id="6a589-127">DataType</span></span><br/>     | <span data-ttu-id="6a589-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6a589-128">String</span></span><br/>  | <span data-ttu-id="6a589-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6a589-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="6a589-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6a589-130">DefaultValue</span></span><br/> | <span data-ttu-id="6a589-131">Integer</span><span class="sxs-lookup"><span data-stu-id="6a589-131">Integer</span></span><br/> | <span data-ttu-id="6a589-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="6a589-132">undefined</span></span><br/>       |
| <span data-ttu-id="6a589-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6a589-133">MaxValue</span></span><br/>     | <span data-ttu-id="6a589-134">Integer</span><span class="sxs-lookup"><span data-stu-id="6a589-134">Integer</span></span><br/> | <span data-ttu-id="6a589-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="6a589-135">undefined</span></span><br/>       |
| <span data-ttu-id="6a589-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="6a589-136">MinValue</span></span><br/>     | <span data-ttu-id="6a589-137">Integer</span><span class="sxs-lookup"><span data-stu-id="6a589-137">Integer</span></span><br/> | <span data-ttu-id="6a589-138">1</span><span class="sxs-lookup"><span data-stu-id="6a589-138">1</span></span><br/>               |
| <span data-ttu-id="6a589-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="6a589-139">Mandatory</span></span><br/>    | <span data-ttu-id="6a589-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6a589-140">String</span></span><br/>  | <span data-ttu-id="6a589-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="6a589-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6a589-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="6a589-142">Multiple</span></span><br/>     | <span data-ttu-id="6a589-143">Integer</span><span class="sxs-lookup"><span data-stu-id="6a589-143">Integer</span></span><br/> | <span data-ttu-id="6a589-144">1</span><span class="sxs-lookup"><span data-stu-id="6a589-144">1</span></span><br/>               |
| <span data-ttu-id="6a589-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="6a589-145">UnitType</span></span><br/>     | <span data-ttu-id="6a589-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6a589-146">String</span></span><br/>  | <span data-ttu-id="6a589-147">Prozent</span><span class="sxs-lookup"><span data-stu-id="6a589-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="6a589-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a589-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a589-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="6a589-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




