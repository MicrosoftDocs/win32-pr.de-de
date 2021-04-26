---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a91178f1506196ab505a90de8bf3a3163fa8a3c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993738"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="36bc0-104">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="36bc0-104">PageScalingOffsetHeight</span></span>

<span data-ttu-id="36bc0-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="36bc0-105">This topic is not current.</span></span> <span data-ttu-id="36bc0-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="36bc0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="36bc0-107">Gibt den Skalierungsoffset in der Richtung ImageableSizeHeight für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="36bc0-107">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="36bc0-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="36bc0-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="36bc0-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="36bc0-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="36bc0-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="36bc0-110">Element Information</span></span>



| <span data-ttu-id="36bc0-111">Name</span><span class="sxs-lookup"><span data-stu-id="36bc0-111">Name</span></span> | <span data-ttu-id="36bc0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="36bc0-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="36bc0-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="36bc0-113">Element Type</span></span> <br/>   | <span data-ttu-id="36bc0-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="36bc0-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="36bc0-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="36bc0-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="36bc0-116">Seite</span><span class="sxs-lookup"><span data-stu-id="36bc0-116">Page</span></span><br/>                                         |
| <span data-ttu-id="36bc0-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36bc0-117">Notes</span></span> <br/>          | <span data-ttu-id="36bc0-118">Mit PageScaling-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="36bc0-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="36bc0-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="36bc0-119">Structure Content</span></span>

<span data-ttu-id="36bc0-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="36bc0-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="36bc0-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="36bc0-121">Structure Properties</span></span>

<span data-ttu-id="36bc0-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="36bc0-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="36bc0-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="36bc0-123">Property</span></span>                | <span data-ttu-id="36bc0-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="36bc0-124">xsi:type</span></span>           | <span data-ttu-id="36bc0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="36bc0-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="36bc0-126">DataType</span><span class="sxs-lookup"><span data-stu-id="36bc0-126">DataType</span></span><br/>     | <span data-ttu-id="36bc0-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="36bc0-127">string</span></span><br/>  | <span data-ttu-id="36bc0-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="36bc0-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="36bc0-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="36bc0-129">DefaultValue</span></span><br/> | <span data-ttu-id="36bc0-130">integer</span><span class="sxs-lookup"><span data-stu-id="36bc0-130">integer</span></span><br/> | <span data-ttu-id="36bc0-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="36bc0-131">undefined</span></span><br/>       |
| <span data-ttu-id="36bc0-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="36bc0-132">MaxValue</span></span><br/>     | <span data-ttu-id="36bc0-133">integer</span><span class="sxs-lookup"><span data-stu-id="36bc0-133">integer</span></span><br/> | <span data-ttu-id="36bc0-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="36bc0-134">undefined</span></span><br/>       |
| <span data-ttu-id="36bc0-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="36bc0-135">MinValue</span></span><br/>     | <span data-ttu-id="36bc0-136">integer</span><span class="sxs-lookup"><span data-stu-id="36bc0-136">integer</span></span><br/> | <span data-ttu-id="36bc0-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="36bc0-137">undefined</span></span><br/>       |
| <span data-ttu-id="36bc0-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="36bc0-138">Mandatory</span></span><br/>    | <span data-ttu-id="36bc0-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="36bc0-139">string</span></span><br/>  | <span data-ttu-id="36bc0-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="36bc0-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="36bc0-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="36bc0-141">Multiple</span></span><br/>     | <span data-ttu-id="36bc0-142">integer</span><span class="sxs-lookup"><span data-stu-id="36bc0-142">integer</span></span><br/> | <span data-ttu-id="36bc0-143">1</span><span class="sxs-lookup"><span data-stu-id="36bc0-143">1</span></span><br/>               |
| <span data-ttu-id="36bc0-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="36bc0-144">UnitType</span></span><br/>     | <span data-ttu-id="36bc0-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="36bc0-145">string</span></span><br/>  | <span data-ttu-id="36bc0-146">Mikron</span><span class="sxs-lookup"><span data-stu-id="36bc0-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="36bc0-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36bc0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36bc0-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="36bc0-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




