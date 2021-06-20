---
description: Erfahren Sie mehr über das PageBlackGenerationProcessingTotalInkCoverageLimit-Element, das die maximal zulässige Summe der vier Freikmalabdeckungen an einer beliebigen Stelle in einem Bild angibt.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68410cabdfafa5ce82450821e4ae45709ee8d4c9
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408443"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="d0cdc-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="d0cdc-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="d0cdc-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="d0cdc-104">This topic is not current.</span></span> <span data-ttu-id="d0cdc-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="d0cdc-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d0cdc-106">Gibt die maximal zulässige Summe der vier Ink-Abdeckungen an einer beliebigen Stelle in einem Bild an.</span><span class="sxs-lookup"><span data-stu-id="d0cdc-106">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="d0cdc-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d0cdc-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d0cdc-108">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="d0cdc-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d0cdc-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d0cdc-109">Element Information</span></span>



| <span data-ttu-id="d0cdc-110">Name</span><span class="sxs-lookup"><span data-stu-id="d0cdc-110">Name</span></span> | <span data-ttu-id="d0cdc-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d0cdc-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="d0cdc-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="d0cdc-112">Element Type</span></span> <br/>   | <span data-ttu-id="d0cdc-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d0cdc-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="d0cdc-114">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="d0cdc-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d0cdc-115">Seite</span><span class="sxs-lookup"><span data-stu-id="d0cdc-115">Page</span></span><br/>                                            |
| <span data-ttu-id="d0cdc-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0cdc-116">Notes</span></span> <br/>          | <span data-ttu-id="d0cdc-117">Mit PageBlackGenerationProcessing-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="d0cdc-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d0cdc-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="d0cdc-118">Structure Content</span></span>

<span data-ttu-id="d0cdc-119">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="d0cdc-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="d0cdc-120">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0cdc-120">Structure Properties</span></span>

<span data-ttu-id="d0cdc-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d0cdc-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d0cdc-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d0cdc-122">Property</span></span>                | <span data-ttu-id="d0cdc-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d0cdc-123">xsi:type</span></span>           | <span data-ttu-id="d0cdc-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d0cdc-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d0cdc-125">DataType</span><span class="sxs-lookup"><span data-stu-id="d0cdc-125">DataType</span></span><br/>     | <span data-ttu-id="d0cdc-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d0cdc-126">string</span></span><br/>  | <span data-ttu-id="d0cdc-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d0cdc-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="d0cdc-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d0cdc-128">DefaultValue</span></span><br/> | <span data-ttu-id="d0cdc-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d0cdc-129">string</span></span><br/>  | <span data-ttu-id="d0cdc-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="d0cdc-130">undefined</span></span><br/>       |
| <span data-ttu-id="d0cdc-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d0cdc-131">MaxValue</span></span><br/>     | <span data-ttu-id="d0cdc-132">integer</span><span class="sxs-lookup"><span data-stu-id="d0cdc-132">integer</span></span><br/> | <span data-ttu-id="d0cdc-133">400</span><span class="sxs-lookup"><span data-stu-id="d0cdc-133">400</span></span><br/>             |
| <span data-ttu-id="d0cdc-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="d0cdc-134">MinValue</span></span><br/>     | <span data-ttu-id="d0cdc-135">integer</span><span class="sxs-lookup"><span data-stu-id="d0cdc-135">integer</span></span><br/> | <span data-ttu-id="d0cdc-136">200</span><span class="sxs-lookup"><span data-stu-id="d0cdc-136">200</span></span><br/>             |
| <span data-ttu-id="d0cdc-137">Mehrere</span><span class="sxs-lookup"><span data-stu-id="d0cdc-137">Multiple</span></span><br/>     | <span data-ttu-id="d0cdc-138">integer</span><span class="sxs-lookup"><span data-stu-id="d0cdc-138">integer</span></span><br/> | <span data-ttu-id="d0cdc-139">1</span><span class="sxs-lookup"><span data-stu-id="d0cdc-139">1</span></span><br/>               |
| <span data-ttu-id="d0cdc-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="d0cdc-140">Mandatory</span></span><br/>    | <span data-ttu-id="d0cdc-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d0cdc-141">string</span></span><br/>  | <span data-ttu-id="d0cdc-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="d0cdc-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d0cdc-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="d0cdc-143">UnitType</span></span><br/>     | <span data-ttu-id="d0cdc-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d0cdc-144">string</span></span><br/>  | <span data-ttu-id="d0cdc-145">Prozent</span><span class="sxs-lookup"><span data-stu-id="d0cdc-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d0cdc-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0cdc-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0cdc-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="d0cdc-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




