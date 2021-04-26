---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3052d8cec8fd46c2f7607e6366aa6868cccbdbda
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996187"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="a5ff0-104">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="a5ff0-104">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="a5ff0-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a5ff0-105">This topic is not current.</span></span> <span data-ttu-id="a5ff0-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a5ff0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a5ff0-107">Anwendungsinhalt mit der angegebenen benannten Farbe MUSS bei allen Farbtrennungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5ff0-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="a5ff0-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a5ff0-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a5ff0-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="a5ff0-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a5ff0-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a5ff0-110">Element Information</span></span>



| <span data-ttu-id="a5ff0-111">Name</span><span class="sxs-lookup"><span data-stu-id="a5ff0-111">Name</span></span> | <span data-ttu-id="a5ff0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a5ff0-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="a5ff0-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a5ff0-113">Element Type</span></span> <br/>   | <span data-ttu-id="a5ff0-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a5ff0-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="a5ff0-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a5ff0-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a5ff0-116">Seite</span><span class="sxs-lookup"><span data-stu-id="a5ff0-116">Page</span></span><br/>                                            |
| <span data-ttu-id="a5ff0-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a5ff0-117">Notes</span></span> <br/>          | <span data-ttu-id="a5ff0-118">Verknüpft mit dem PageBlackGenerationProcessing-Element</span><span class="sxs-lookup"><span data-stu-id="a5ff0-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a5ff0-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="a5ff0-119">Structure Content</span></span>

<span data-ttu-id="a5ff0-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="a5ff0-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a5ff0-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5ff0-121">Structure Properties</span></span>

<span data-ttu-id="a5ff0-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a5ff0-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a5ff0-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a5ff0-123">Property</span></span>                | <span data-ttu-id="a5ff0-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a5ff0-124">xsi:type</span></span>           | <span data-ttu-id="a5ff0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a5ff0-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a5ff0-126">DataType</span><span class="sxs-lookup"><span data-stu-id="a5ff0-126">DataType</span></span><br/>     | <span data-ttu-id="a5ff0-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a5ff0-127">string</span></span><br/>  | <span data-ttu-id="a5ff0-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a5ff0-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="a5ff0-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a5ff0-129">DefaultValue</span></span><br/> | <span data-ttu-id="a5ff0-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a5ff0-130">string</span></span><br/>  | <span data-ttu-id="a5ff0-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="a5ff0-131">undefined</span></span><br/>       |
| <span data-ttu-id="a5ff0-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a5ff0-132">MaxValue</span></span><br/>     | <span data-ttu-id="a5ff0-133">integer</span><span class="sxs-lookup"><span data-stu-id="a5ff0-133">integer</span></span><br/> | <span data-ttu-id="a5ff0-134">100</span><span class="sxs-lookup"><span data-stu-id="a5ff0-134">100</span></span><br/>             |
| <span data-ttu-id="a5ff0-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="a5ff0-135">MinValue</span></span><br/>     | <span data-ttu-id="a5ff0-136">integer</span><span class="sxs-lookup"><span data-stu-id="a5ff0-136">integer</span></span><br/> | <span data-ttu-id="a5ff0-137">0</span><span class="sxs-lookup"><span data-stu-id="a5ff0-137">0</span></span><br/>               |
| <span data-ttu-id="a5ff0-138">Mehrere</span><span class="sxs-lookup"><span data-stu-id="a5ff0-138">Multiple</span></span><br/>     | <span data-ttu-id="a5ff0-139">integer</span><span class="sxs-lookup"><span data-stu-id="a5ff0-139">integer</span></span><br/> | <span data-ttu-id="a5ff0-140">1</span><span class="sxs-lookup"><span data-stu-id="a5ff0-140">1</span></span><br/>               |
| <span data-ttu-id="a5ff0-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="a5ff0-141">Mandatory</span></span><br/>    | <span data-ttu-id="a5ff0-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a5ff0-142">string</span></span><br/>  | <span data-ttu-id="a5ff0-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="a5ff0-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a5ff0-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="a5ff0-144">UnitType</span></span><br/>     | <span data-ttu-id="a5ff0-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a5ff0-145">string</span></span><br/>  | <span data-ttu-id="a5ff0-146">Prozent</span><span class="sxs-lookup"><span data-stu-id="a5ff0-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a5ff0-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5ff0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5ff0-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a5ff0-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




