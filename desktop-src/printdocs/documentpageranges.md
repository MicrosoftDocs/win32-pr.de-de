---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ded7c18fc781fd4374feb8958a98b845d95546
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997177"
---
# <a name="documentpageranges"></a><span data-ttu-id="72a00-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="72a00-104">DocumentPageRanges</span></span>

<span data-ttu-id="72a00-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="72a00-105">This topic is not current.</span></span> <span data-ttu-id="72a00-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="72a00-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="72a00-107">Beschreibt den Ausgabebereich des Dokuments auf Seiten.</span><span class="sxs-lookup"><span data-stu-id="72a00-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="72a00-108">Der Parameterwert muss der folgenden Struktur entsprechen:</span><span class="sxs-lookup"><span data-stu-id="72a00-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="72a00-109">PageRangeText: "*PageRange*" oder "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="72a00-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="72a00-110">PageRange: "*PageNumber*" oder "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="72a00-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="72a00-111">PageNumber: 1 bis N, wobei N die Anzahl der Seiten im Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="72a00-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="72a00-112">Wenn *PageNumber* > N, dann *PageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="72a00-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="72a00-113">Leerzeichen in der Zeichenfolge sollten ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="72a00-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="72a00-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="72a00-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="72a00-115">Strukturell</span><span class="sxs-lookup"><span data-stu-id="72a00-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="72a00-116">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="72a00-116">Element Information</span></span>



| <span data-ttu-id="72a00-117">Name</span><span class="sxs-lookup"><span data-stu-id="72a00-117">Name</span></span> | <span data-ttu-id="72a00-118">Wert</span><span class="sxs-lookup"><span data-stu-id="72a00-118">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="72a00-119">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="72a00-119">Element Type</span></span> <br/>   | <span data-ttu-id="72a00-120">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="72a00-120">ParameterDef</span></span><br/> |
| <span data-ttu-id="72a00-121">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="72a00-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="72a00-122">Dokument</span><span class="sxs-lookup"><span data-stu-id="72a00-122">Document</span></span><br/>     |
| <span data-ttu-id="72a00-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72a00-123">Notes</span></span> <br/>          | <span data-ttu-id="72a00-124">Keine</span><span class="sxs-lookup"><span data-stu-id="72a00-124">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="72a00-125">Strukturell</span><span class="sxs-lookup"><span data-stu-id="72a00-125">Structural Content</span></span>

<span data-ttu-id="72a00-126">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="72a00-126">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="72a00-127">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="72a00-127">Structure Properties</span></span>

<span data-ttu-id="72a00-128">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="72a00-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="72a00-129">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="72a00-129">Property</span></span>                | <span data-ttu-id="72a00-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="72a00-130">xsi:type</span></span>           | <span data-ttu-id="72a00-131">Wert</span><span class="sxs-lookup"><span data-stu-id="72a00-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="72a00-132">DataType</span><span class="sxs-lookup"><span data-stu-id="72a00-132">DataType</span></span><br/>     | <span data-ttu-id="72a00-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="72a00-133">string</span></span><br/>  | <span data-ttu-id="72a00-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="72a00-134">xs:string</span></span><br/>       |
| <span data-ttu-id="72a00-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="72a00-135">DefaultValue</span></span><br/> | <span data-ttu-id="72a00-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="72a00-136">string</span></span><br/>  | <span data-ttu-id="72a00-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="72a00-137">undefined</span></span><br/>       |
| <span data-ttu-id="72a00-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="72a00-138">MaxLength</span></span><br/>    | <span data-ttu-id="72a00-139">integer</span><span class="sxs-lookup"><span data-stu-id="72a00-139">integer</span></span><br/> | <span data-ttu-id="72a00-140">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="72a00-140">undefined</span></span><br/>       |
| <span data-ttu-id="72a00-141">Minlength</span><span class="sxs-lookup"><span data-stu-id="72a00-141">MinLength</span></span><br/>    | <span data-ttu-id="72a00-142">integer</span><span class="sxs-lookup"><span data-stu-id="72a00-142">integer</span></span><br/> | <span data-ttu-id="72a00-143">1</span><span class="sxs-lookup"><span data-stu-id="72a00-143">1</span></span><br/>               |
| <span data-ttu-id="72a00-144">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="72a00-144">Mandatory</span></span><br/>    | <span data-ttu-id="72a00-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="72a00-145">string</span></span><br/>  | <span data-ttu-id="72a00-146">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="72a00-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="72a00-147">Unittype</span><span class="sxs-lookup"><span data-stu-id="72a00-147">UnitType</span></span><br/>     | <span data-ttu-id="72a00-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="72a00-148">string</span></span><br/>  | <span data-ttu-id="72a00-149">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="72a00-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="72a00-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72a00-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72a00-151">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="72a00-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




