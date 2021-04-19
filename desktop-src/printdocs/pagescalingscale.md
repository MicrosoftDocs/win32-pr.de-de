---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246f77c5878b74e1b149c6d4020230030fb3c5b0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355115"
---
# <a name="pagescalingscale"></a><span data-ttu-id="fb288-104">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="fb288-104">PageScalingScale</span></span>

<span data-ttu-id="fb288-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="fb288-105">This topic is not current.</span></span> <span data-ttu-id="fb288-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fb288-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fb288-107">Gibt den Skalierungsfaktor für die benutzerdefinierte quadratische Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="fb288-107">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="fb288-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fb288-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fb288-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="fb288-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fb288-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fb288-110">Element Information</span></span>



| <span data-ttu-id="fb288-111">Name</span><span class="sxs-lookup"><span data-stu-id="fb288-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="fb288-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="fb288-112">Element Type</span></span> <br/>   | <span data-ttu-id="fb288-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fb288-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="fb288-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="fb288-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fb288-115">Seite</span><span class="sxs-lookup"><span data-stu-id="fb288-115">Page</span></span><br/>                                         |
| <span data-ttu-id="fb288-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb288-116">Notes</span></span> <br/>          | <span data-ttu-id="fb288-117">Verknüpft mit PageScaling-Element, benutzerdefinierte Option</span><span class="sxs-lookup"><span data-stu-id="fb288-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fb288-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="fb288-118">Structure Content</span></span>

<span data-ttu-id="fb288-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="fb288-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
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

## <a name="structure-properties"></a><span data-ttu-id="fb288-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb288-120">Structure Properties</span></span>

<span data-ttu-id="fb288-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="fb288-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fb288-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fb288-122">Property</span></span>                | <span data-ttu-id="fb288-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fb288-123">xsi:type</span></span>           | <span data-ttu-id="fb288-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fb288-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fb288-125">DataType</span><span class="sxs-lookup"><span data-stu-id="fb288-125">DataType</span></span><br/>     | <span data-ttu-id="fb288-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fb288-126">string</span></span><br/>  | <span data-ttu-id="fb288-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="fb288-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="fb288-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fb288-128">DefaultValue</span></span><br/> | <span data-ttu-id="fb288-129">integer</span><span class="sxs-lookup"><span data-stu-id="fb288-129">integer</span></span><br/> | <span data-ttu-id="fb288-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="fb288-130">undefined</span></span><br/>       |
| <span data-ttu-id="fb288-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="fb288-131">MaxValue</span></span><br/>     | <span data-ttu-id="fb288-132">integer</span><span class="sxs-lookup"><span data-stu-id="fb288-132">integer</span></span><br/> | <span data-ttu-id="fb288-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="fb288-133">undefined</span></span><br/>       |
| <span data-ttu-id="fb288-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="fb288-134">MinValue</span></span><br/>     | <span data-ttu-id="fb288-135">integer</span><span class="sxs-lookup"><span data-stu-id="fb288-135">integer</span></span><br/> | <span data-ttu-id="fb288-136">1</span><span class="sxs-lookup"><span data-stu-id="fb288-136">1</span></span><br/>               |
| <span data-ttu-id="fb288-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="fb288-137">Mandatory</span></span><br/>    | <span data-ttu-id="fb288-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fb288-138">string</span></span><br/>  | <span data-ttu-id="fb288-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="fb288-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fb288-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="fb288-140">Multiple</span></span><br/>     | <span data-ttu-id="fb288-141">integer</span><span class="sxs-lookup"><span data-stu-id="fb288-141">integer</span></span><br/> | <span data-ttu-id="fb288-142">1</span><span class="sxs-lookup"><span data-stu-id="fb288-142">1</span></span><br/>               |
| <span data-ttu-id="fb288-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="fb288-143">UnitType</span></span><br/>     | <span data-ttu-id="fb288-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fb288-144">string</span></span><br/>  | <span data-ttu-id="fb288-145">Prozent</span><span class="sxs-lookup"><span data-stu-id="fb288-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="fb288-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fb288-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb288-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="fb288-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




