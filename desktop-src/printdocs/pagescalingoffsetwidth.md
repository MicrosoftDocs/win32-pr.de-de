---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: Pagescalingoffte twidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a9cd5532bf4d109b94c579ef2ad21d242aca9a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106351860"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="60805-104">Pagescalingoffte twidth</span><span class="sxs-lookup"><span data-stu-id="60805-104">PageScalingOffsetWidth</span></span>

<span data-ttu-id="60805-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="60805-105">This topic is not current.</span></span> <span data-ttu-id="60805-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="60805-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="60805-107">Gibt den Skalierungs Offset in der imageablesizewidth-Richtung für die benutzerdefinierte Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="60805-107">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="60805-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="60805-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="60805-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="60805-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="60805-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="60805-110">Element Information</span></span>



| <span data-ttu-id="60805-111">Name</span><span class="sxs-lookup"><span data-stu-id="60805-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="60805-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="60805-112">Element Type</span></span> <br/>   | <span data-ttu-id="60805-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="60805-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="60805-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="60805-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="60805-115">Seite</span><span class="sxs-lookup"><span data-stu-id="60805-115">Page</span></span><br/>                                         |
| <span data-ttu-id="60805-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="60805-116">Notes</span></span> <br/>          | <span data-ttu-id="60805-117">Verknüpft mit PageScaling-Element, benutzerdefinierte Option</span><span class="sxs-lookup"><span data-stu-id="60805-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="60805-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="60805-118">Structure Content</span></span>

<span data-ttu-id="60805-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="60805-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="60805-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60805-120">Structure Properties</span></span>

<span data-ttu-id="60805-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="60805-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="60805-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="60805-122">Property</span></span>                | <span data-ttu-id="60805-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="60805-123">xsi:type</span></span>           | <span data-ttu-id="60805-124">Wert</span><span class="sxs-lookup"><span data-stu-id="60805-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="60805-125">DataType</span><span class="sxs-lookup"><span data-stu-id="60805-125">DataType</span></span><br/>     | <span data-ttu-id="60805-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="60805-126">string</span></span><br/>  | <span data-ttu-id="60805-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="60805-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="60805-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="60805-128">DefaultValue</span></span><br/> | <span data-ttu-id="60805-129">integer</span><span class="sxs-lookup"><span data-stu-id="60805-129">integer</span></span><br/> | <span data-ttu-id="60805-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="60805-130">undefined</span></span><br/>       |
| <span data-ttu-id="60805-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="60805-131">MaxValue</span></span><br/>     | <span data-ttu-id="60805-132">integer</span><span class="sxs-lookup"><span data-stu-id="60805-132">integer</span></span><br/> | <span data-ttu-id="60805-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="60805-133">undefined</span></span><br/>       |
| <span data-ttu-id="60805-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="60805-134">MinValue</span></span><br/>     | <span data-ttu-id="60805-135">integer</span><span class="sxs-lookup"><span data-stu-id="60805-135">integer</span></span><br/> | <span data-ttu-id="60805-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="60805-136">undefined</span></span><br/>       |
| <span data-ttu-id="60805-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="60805-137">Mandatory</span></span><br/>    | <span data-ttu-id="60805-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="60805-138">string</span></span><br/>  | <span data-ttu-id="60805-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="60805-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="60805-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="60805-140">Multiple</span></span><br/>     | <span data-ttu-id="60805-141">integer</span><span class="sxs-lookup"><span data-stu-id="60805-141">integer</span></span><br/> | <span data-ttu-id="60805-142">1</span><span class="sxs-lookup"><span data-stu-id="60805-142">1</span></span><br/>               |
| <span data-ttu-id="60805-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="60805-143">UnitType</span></span><br/>     | <span data-ttu-id="60805-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="60805-144">string</span></span><br/>  | <span data-ttu-id="60805-145">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="60805-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="60805-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60805-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60805-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="60805-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




