---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ef53d9fe2906ae04cd1e7e3ea1513a631bc162
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997457"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="4d63e-104">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="4d63e-104">PageScalingScaleWidth</span></span>

<span data-ttu-id="4d63e-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4d63e-105">This topic is not current.</span></span> <span data-ttu-id="4d63e-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="4d63e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4d63e-107">Gibt den Skalierungsfaktor in der Richtung ImageableSizeWidth für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="4d63e-107">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="4d63e-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4d63e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4d63e-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4d63e-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4d63e-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4d63e-110">Element Information</span></span>



| <span data-ttu-id="4d63e-111">Name</span><span class="sxs-lookup"><span data-stu-id="4d63e-111">Name</span></span> | <span data-ttu-id="4d63e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4d63e-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="4d63e-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4d63e-113">Element Type</span></span> <br/>   | <span data-ttu-id="4d63e-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4d63e-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="4d63e-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="4d63e-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4d63e-116">Seite</span><span class="sxs-lookup"><span data-stu-id="4d63e-116">Page</span></span><br/>                                         |
| <span data-ttu-id="4d63e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d63e-117">Notes</span></span> <br/>          | <span data-ttu-id="4d63e-118">Mit PageScaling-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="4d63e-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4d63e-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4d63e-119">Structure Content</span></span>

<span data-ttu-id="4d63e-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="4d63e-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="4d63e-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d63e-121">Structure Properties</span></span>

<span data-ttu-id="4d63e-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4d63e-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4d63e-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d63e-123">Property</span></span>                | <span data-ttu-id="4d63e-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4d63e-124">xsi:type</span></span>           | <span data-ttu-id="4d63e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4d63e-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4d63e-126">DataType</span><span class="sxs-lookup"><span data-stu-id="4d63e-126">DataType</span></span><br/>     | <span data-ttu-id="4d63e-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4d63e-127">String</span></span><br/>  | <span data-ttu-id="4d63e-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4d63e-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="4d63e-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4d63e-129">DefaultValue</span></span><br/> | <span data-ttu-id="4d63e-130">Integer</span><span class="sxs-lookup"><span data-stu-id="4d63e-130">Integer</span></span><br/> | <span data-ttu-id="4d63e-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4d63e-131">undefined</span></span><br/>       |
| <span data-ttu-id="4d63e-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4d63e-132">MaxValue</span></span><br/>     | <span data-ttu-id="4d63e-133">Integer</span><span class="sxs-lookup"><span data-stu-id="4d63e-133">Integer</span></span><br/> | <span data-ttu-id="4d63e-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4d63e-134">undefined</span></span><br/>       |
| <span data-ttu-id="4d63e-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="4d63e-135">MinValue</span></span><br/>     | <span data-ttu-id="4d63e-136">Integer</span><span class="sxs-lookup"><span data-stu-id="4d63e-136">Integer</span></span><br/> | <span data-ttu-id="4d63e-137">1</span><span class="sxs-lookup"><span data-stu-id="4d63e-137">1</span></span><br/>               |
| <span data-ttu-id="4d63e-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="4d63e-138">Mandatory</span></span><br/>    | <span data-ttu-id="4d63e-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4d63e-139">String</span></span><br/>  | <span data-ttu-id="4d63e-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="4d63e-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4d63e-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="4d63e-141">Multiple</span></span><br/>     | <span data-ttu-id="4d63e-142">Integer</span><span class="sxs-lookup"><span data-stu-id="4d63e-142">Integer</span></span><br/> | <span data-ttu-id="4d63e-143">1</span><span class="sxs-lookup"><span data-stu-id="4d63e-143">1</span></span><br/>               |
| <span data-ttu-id="4d63e-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="4d63e-144">UnitType</span></span><br/>     | <span data-ttu-id="4d63e-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4d63e-145">String</span></span><br/>  | <span data-ttu-id="4d63e-146">Mikron</span><span class="sxs-lookup"><span data-stu-id="4d63e-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4d63e-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d63e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d63e-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="4d63e-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




