---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2608535c65cbde04005334ed970c0d27cb1feffb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996177"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="7c253-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="7c253-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="7c253-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="7c253-105">This topic is not current.</span></span> <span data-ttu-id="7c253-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="7c253-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7c253-107">Beschreibt den Punkt im Bereich "Hervorhebung bis Schatten", an dem GCR beginnen soll (100 % dunkelster Schatten).</span><span class="sxs-lookup"><span data-stu-id="7c253-107">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="7c253-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7c253-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7c253-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="7c253-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7c253-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7c253-110">Element Information</span></span>



| <span data-ttu-id="7c253-111">Name</span><span class="sxs-lookup"><span data-stu-id="7c253-111">Name</span></span> | <span data-ttu-id="7c253-112">Wert</span><span class="sxs-lookup"><span data-stu-id="7c253-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="7c253-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="7c253-113">Element Type</span></span> <br/>   | <span data-ttu-id="7c253-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7c253-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="7c253-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="7c253-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7c253-116">Seite</span><span class="sxs-lookup"><span data-stu-id="7c253-116">Page</span></span><br/>                                            |
| <span data-ttu-id="7c253-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c253-117">Notes</span></span> <br/>          | <span data-ttu-id="7c253-118">Mit PageBlackGenerationProcessing-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="7c253-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7c253-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="7c253-119">Structure Content</span></span>

<span data-ttu-id="7c253-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="7c253-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="7c253-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c253-121">Structure Properties</span></span>

<span data-ttu-id="7c253-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7c253-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7c253-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7c253-123">Property</span></span>                | <span data-ttu-id="7c253-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7c253-124">xsi:type</span></span>           | <span data-ttu-id="7c253-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7c253-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7c253-126">DataType</span><span class="sxs-lookup"><span data-stu-id="7c253-126">DataType</span></span><br/>     | <span data-ttu-id="7c253-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c253-127">string</span></span><br/>  | <span data-ttu-id="7c253-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7c253-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="7c253-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7c253-129">DefaultValue</span></span><br/> | <span data-ttu-id="7c253-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c253-130">string</span></span><br/>  | <span data-ttu-id="7c253-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="7c253-131">undefined</span></span><br/>       |
| <span data-ttu-id="7c253-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7c253-132">MaxValue</span></span><br/>     | <span data-ttu-id="7c253-133">integer</span><span class="sxs-lookup"><span data-stu-id="7c253-133">integer</span></span><br/> | <span data-ttu-id="7c253-134">100</span><span class="sxs-lookup"><span data-stu-id="7c253-134">100</span></span><br/>             |
| <span data-ttu-id="7c253-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="7c253-135">MinValue</span></span><br/>     | <span data-ttu-id="7c253-136">integer</span><span class="sxs-lookup"><span data-stu-id="7c253-136">integer</span></span><br/> | <span data-ttu-id="7c253-137">0</span><span class="sxs-lookup"><span data-stu-id="7c253-137">0</span></span><br/>               |
| <span data-ttu-id="7c253-138">Mehrere</span><span class="sxs-lookup"><span data-stu-id="7c253-138">Multiple</span></span><br/>     | <span data-ttu-id="7c253-139">integer</span><span class="sxs-lookup"><span data-stu-id="7c253-139">integer</span></span><br/> | <span data-ttu-id="7c253-140">1</span><span class="sxs-lookup"><span data-stu-id="7c253-140">1</span></span><br/>               |
| <span data-ttu-id="7c253-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="7c253-141">Mandatory</span></span><br/>    | <span data-ttu-id="7c253-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c253-142">string</span></span><br/>  | <span data-ttu-id="7c253-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="7c253-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7c253-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="7c253-144">UnitType</span></span><br/>     | <span data-ttu-id="7c253-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c253-145">string</span></span><br/>  | <span data-ttu-id="7c253-146">Prozent</span><span class="sxs-lookup"><span data-stu-id="7c253-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7c253-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c253-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c253-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="7c253-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




