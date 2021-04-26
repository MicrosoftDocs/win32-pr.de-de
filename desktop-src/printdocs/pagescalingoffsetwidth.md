---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b82c2b0c0f2c86a792706ec7e00819ccda1038c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997957"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="02ac9-104">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="02ac9-104">PageScalingOffsetWidth</span></span>

<span data-ttu-id="02ac9-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="02ac9-105">This topic is not current.</span></span> <span data-ttu-id="02ac9-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="02ac9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="02ac9-107">Gibt den Skalierungsoffset in der Richtung ImageableSizeWidth für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="02ac9-107">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="02ac9-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="02ac9-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="02ac9-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="02ac9-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="02ac9-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="02ac9-110">Element Information</span></span>



| <span data-ttu-id="02ac9-111">Name</span><span class="sxs-lookup"><span data-stu-id="02ac9-111">Name</span></span> | <span data-ttu-id="02ac9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="02ac9-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="02ac9-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="02ac9-113">Element Type</span></span> <br/>   | <span data-ttu-id="02ac9-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="02ac9-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="02ac9-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="02ac9-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="02ac9-116">Seite</span><span class="sxs-lookup"><span data-stu-id="02ac9-116">Page</span></span><br/>                                         |
| <span data-ttu-id="02ac9-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02ac9-117">Notes</span></span> <br/>          | <span data-ttu-id="02ac9-118">Mit PageScaling-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="02ac9-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="02ac9-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="02ac9-119">Structure Content</span></span>

<span data-ttu-id="02ac9-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="02ac9-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="02ac9-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="02ac9-121">Structure Properties</span></span>

<span data-ttu-id="02ac9-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="02ac9-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="02ac9-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="02ac9-123">Property</span></span>                | <span data-ttu-id="02ac9-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="02ac9-124">xsi:type</span></span>           | <span data-ttu-id="02ac9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="02ac9-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="02ac9-126">DataType</span><span class="sxs-lookup"><span data-stu-id="02ac9-126">DataType</span></span><br/>     | <span data-ttu-id="02ac9-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02ac9-127">string</span></span><br/>  | <span data-ttu-id="02ac9-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="02ac9-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="02ac9-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="02ac9-129">DefaultValue</span></span><br/> | <span data-ttu-id="02ac9-130">integer</span><span class="sxs-lookup"><span data-stu-id="02ac9-130">integer</span></span><br/> | <span data-ttu-id="02ac9-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="02ac9-131">undefined</span></span><br/>       |
| <span data-ttu-id="02ac9-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="02ac9-132">MaxValue</span></span><br/>     | <span data-ttu-id="02ac9-133">integer</span><span class="sxs-lookup"><span data-stu-id="02ac9-133">integer</span></span><br/> | <span data-ttu-id="02ac9-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="02ac9-134">undefined</span></span><br/>       |
| <span data-ttu-id="02ac9-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="02ac9-135">MinValue</span></span><br/>     | <span data-ttu-id="02ac9-136">integer</span><span class="sxs-lookup"><span data-stu-id="02ac9-136">integer</span></span><br/> | <span data-ttu-id="02ac9-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="02ac9-137">undefined</span></span><br/>       |
| <span data-ttu-id="02ac9-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="02ac9-138">Mandatory</span></span><br/>    | <span data-ttu-id="02ac9-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02ac9-139">string</span></span><br/>  | <span data-ttu-id="02ac9-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="02ac9-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="02ac9-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="02ac9-141">Multiple</span></span><br/>     | <span data-ttu-id="02ac9-142">integer</span><span class="sxs-lookup"><span data-stu-id="02ac9-142">integer</span></span><br/> | <span data-ttu-id="02ac9-143">1</span><span class="sxs-lookup"><span data-stu-id="02ac9-143">1</span></span><br/>               |
| <span data-ttu-id="02ac9-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="02ac9-144">UnitType</span></span><br/>     | <span data-ttu-id="02ac9-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02ac9-145">string</span></span><br/>  | <span data-ttu-id="02ac9-146">Mikron</span><span class="sxs-lookup"><span data-stu-id="02ac9-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="02ac9-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02ac9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02ac9-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="02ac9-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




