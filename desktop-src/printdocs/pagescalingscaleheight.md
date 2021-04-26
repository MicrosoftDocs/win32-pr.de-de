---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d718d80f6b3cc369ddcb5c088a1299d639634b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997477"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="fc445-104">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="fc445-104">PageScalingScaleHeight</span></span>

<span data-ttu-id="fc445-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="fc445-105">This topic is not current.</span></span> <span data-ttu-id="fc445-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="fc445-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fc445-107">Gibt den Skalierungsfaktor in der Richtung ImageableSizeHeight für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="fc445-107">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="fc445-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fc445-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fc445-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="fc445-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fc445-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fc445-110">Element Information</span></span>



| <span data-ttu-id="fc445-111">Name</span><span class="sxs-lookup"><span data-stu-id="fc445-111">Name</span></span> | <span data-ttu-id="fc445-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fc445-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="fc445-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="fc445-113">Element Type</span></span> <br/>   | <span data-ttu-id="fc445-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fc445-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="fc445-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="fc445-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fc445-116">Seite</span><span class="sxs-lookup"><span data-stu-id="fc445-116">Page</span></span><br/>                                         |
| <span data-ttu-id="fc445-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fc445-117">Notes</span></span> <br/>          | <span data-ttu-id="fc445-118">Mit PageScaling-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="fc445-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fc445-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="fc445-119">Structure Content</span></span>

<span data-ttu-id="fc445-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="fc445-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="fc445-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc445-121">Structure Properties</span></span>

<span data-ttu-id="fc445-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc445-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fc445-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fc445-123">Property</span></span>                | <span data-ttu-id="fc445-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fc445-124">xsi:type</span></span>           | <span data-ttu-id="fc445-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fc445-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fc445-126">DataType</span><span class="sxs-lookup"><span data-stu-id="fc445-126">DataType</span></span><br/>     | <span data-ttu-id="fc445-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fc445-127">String</span></span><br/>  | <span data-ttu-id="fc445-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="fc445-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="fc445-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fc445-129">DefaultValue</span></span><br/> | <span data-ttu-id="fc445-130">Integer</span><span class="sxs-lookup"><span data-stu-id="fc445-130">Integer</span></span><br/> | <span data-ttu-id="fc445-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="fc445-131">undefined</span></span><br/>       |
| <span data-ttu-id="fc445-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="fc445-132">MaxValue</span></span><br/>     | <span data-ttu-id="fc445-133">Integer</span><span class="sxs-lookup"><span data-stu-id="fc445-133">Integer</span></span><br/> | <span data-ttu-id="fc445-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="fc445-134">undefined</span></span><br/>       |
| <span data-ttu-id="fc445-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="fc445-135">MinValue</span></span><br/>     | <span data-ttu-id="fc445-136">Integer</span><span class="sxs-lookup"><span data-stu-id="fc445-136">Integer</span></span><br/> | <span data-ttu-id="fc445-137">1</span><span class="sxs-lookup"><span data-stu-id="fc445-137">1</span></span><br/>               |
| <span data-ttu-id="fc445-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="fc445-138">Mandatory</span></span><br/>    | <span data-ttu-id="fc445-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fc445-139">String</span></span><br/>  | <span data-ttu-id="fc445-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="fc445-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fc445-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="fc445-141">Multiple</span></span><br/>     | <span data-ttu-id="fc445-142">Integer</span><span class="sxs-lookup"><span data-stu-id="fc445-142">Integer</span></span><br/> | <span data-ttu-id="fc445-143">1</span><span class="sxs-lookup"><span data-stu-id="fc445-143">1</span></span><br/>               |
| <span data-ttu-id="fc445-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="fc445-144">UnitType</span></span><br/>     | <span data-ttu-id="fc445-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fc445-145">String</span></span><br/>  | <span data-ttu-id="fc445-146">Prozent</span><span class="sxs-lookup"><span data-stu-id="fc445-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="fc445-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc445-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc445-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="fc445-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




