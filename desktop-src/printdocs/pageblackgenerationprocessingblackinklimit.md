---
description: Erfahren Sie mehr über den PageBlackGenerationProcessingBlackInkLimit-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c753554b240a5fef0012a81c533b6efe938075e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118425"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="391d2-105">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="391d2-105">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="391d2-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="391d2-106">This topic is not current.</span></span> <span data-ttu-id="391d2-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="391d2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="391d2-108">Anwendungsinhalt mit der angegebenen benannten Farbe MUSS bei allen Farbtrennungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="391d2-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="391d2-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="391d2-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="391d2-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="391d2-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="391d2-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="391d2-111">Element Information</span></span>



| <span data-ttu-id="391d2-112">Name</span><span class="sxs-lookup"><span data-stu-id="391d2-112">Name</span></span> | <span data-ttu-id="391d2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="391d2-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="391d2-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="391d2-114">Element Type</span></span> <br/>   | <span data-ttu-id="391d2-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="391d2-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="391d2-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="391d2-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="391d2-117">Seite</span><span class="sxs-lookup"><span data-stu-id="391d2-117">Page</span></span><br/>                                            |
| <span data-ttu-id="391d2-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="391d2-118">Notes</span></span> <br/>          | <span data-ttu-id="391d2-119">Verknüpft mit dem PageBlackGenerationProcessing-Element</span><span class="sxs-lookup"><span data-stu-id="391d2-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="391d2-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="391d2-120">Structure Content</span></span>

<span data-ttu-id="391d2-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="391d2-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
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

## <a name="structure-properties"></a><span data-ttu-id="391d2-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="391d2-122">Structure Properties</span></span>

<span data-ttu-id="391d2-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="391d2-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="391d2-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="391d2-124">Property</span></span>                | <span data-ttu-id="391d2-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="391d2-125">xsi:type</span></span>           | <span data-ttu-id="391d2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="391d2-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="391d2-127">DataType</span><span class="sxs-lookup"><span data-stu-id="391d2-127">DataType</span></span><br/>     | <span data-ttu-id="391d2-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="391d2-128">string</span></span><br/>  | <span data-ttu-id="391d2-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="391d2-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="391d2-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="391d2-130">DefaultValue</span></span><br/> | <span data-ttu-id="391d2-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="391d2-131">string</span></span><br/>  | <span data-ttu-id="391d2-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="391d2-132">undefined</span></span><br/>       |
| <span data-ttu-id="391d2-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="391d2-133">MaxValue</span></span><br/>     | <span data-ttu-id="391d2-134">integer</span><span class="sxs-lookup"><span data-stu-id="391d2-134">integer</span></span><br/> | <span data-ttu-id="391d2-135">100</span><span class="sxs-lookup"><span data-stu-id="391d2-135">100</span></span><br/>             |
| <span data-ttu-id="391d2-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="391d2-136">MinValue</span></span><br/>     | <span data-ttu-id="391d2-137">integer</span><span class="sxs-lookup"><span data-stu-id="391d2-137">integer</span></span><br/> | <span data-ttu-id="391d2-138">0</span><span class="sxs-lookup"><span data-stu-id="391d2-138">0</span></span><br/>               |
| <span data-ttu-id="391d2-139">Mehrere</span><span class="sxs-lookup"><span data-stu-id="391d2-139">Multiple</span></span><br/>     | <span data-ttu-id="391d2-140">integer</span><span class="sxs-lookup"><span data-stu-id="391d2-140">integer</span></span><br/> | <span data-ttu-id="391d2-141">1</span><span class="sxs-lookup"><span data-stu-id="391d2-141">1</span></span><br/>               |
| <span data-ttu-id="391d2-142">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="391d2-142">Mandatory</span></span><br/>    | <span data-ttu-id="391d2-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="391d2-143">string</span></span><br/>  | <span data-ttu-id="391d2-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="391d2-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="391d2-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="391d2-145">UnitType</span></span><br/>     | <span data-ttu-id="391d2-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="391d2-146">string</span></span><br/>  | <span data-ttu-id="391d2-147">Prozent</span><span class="sxs-lookup"><span data-stu-id="391d2-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="391d2-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="391d2-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="391d2-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="391d2-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




