---
description: Erfahren Sie mehr über das DocumentPageRanges-Element, das den Ausgabebereich des Dokuments auf Seiten beschreibt.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e854736c72b3bff5ba2e4750e0b09e0b87c2c9f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409253"
---
# <a name="documentpageranges"></a><span data-ttu-id="14ad1-103">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="14ad1-103">DocumentPageRanges</span></span>

<span data-ttu-id="14ad1-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="14ad1-104">This topic is not current.</span></span> <span data-ttu-id="14ad1-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="14ad1-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="14ad1-106">Beschreibt den Ausgabebereich des Dokuments auf Seiten.</span><span class="sxs-lookup"><span data-stu-id="14ad1-106">Describes the output range of the document in pages.</span></span> <span data-ttu-id="14ad1-107">Der Parameterwert muss der folgenden Struktur entsprechen:</span><span class="sxs-lookup"><span data-stu-id="14ad1-107">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="14ad1-108">PageRangeText: "*PageRange*" oder "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="14ad1-108">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="14ad1-109">PageRange: "*PageNumber*" oder "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="14ad1-109">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="14ad1-110">PageNumber: 1 bis N, wobei N die Anzahl der Seiten im Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="14ad1-110">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="14ad1-111">Wenn *PageNumber* > N, dann *PageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="14ad1-111">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="14ad1-112">Leerzeichen in der Zeichenfolge sollten ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="14ad1-112">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="14ad1-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="14ad1-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="14ad1-114">Strukturell</span><span class="sxs-lookup"><span data-stu-id="14ad1-114">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="14ad1-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="14ad1-115">Element Information</span></span>



| <span data-ttu-id="14ad1-116">Name</span><span class="sxs-lookup"><span data-stu-id="14ad1-116">Name</span></span> | <span data-ttu-id="14ad1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="14ad1-117">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="14ad1-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="14ad1-118">Element Type</span></span> <br/>   | <span data-ttu-id="14ad1-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="14ad1-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="14ad1-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="14ad1-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="14ad1-121">Dokument</span><span class="sxs-lookup"><span data-stu-id="14ad1-121">Document</span></span><br/>     |
| <span data-ttu-id="14ad1-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="14ad1-122">Notes</span></span> <br/>          | <span data-ttu-id="14ad1-123">Keine</span><span class="sxs-lookup"><span data-stu-id="14ad1-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="14ad1-124">Strukturell</span><span class="sxs-lookup"><span data-stu-id="14ad1-124">Structural Content</span></span>

<span data-ttu-id="14ad1-125">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="14ad1-125">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="14ad1-126">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="14ad1-126">Structure Properties</span></span>

<span data-ttu-id="14ad1-127">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="14ad1-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="14ad1-128">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="14ad1-128">Property</span></span>                | <span data-ttu-id="14ad1-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="14ad1-129">xsi:type</span></span>           | <span data-ttu-id="14ad1-130">Wert</span><span class="sxs-lookup"><span data-stu-id="14ad1-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="14ad1-131">DataType</span><span class="sxs-lookup"><span data-stu-id="14ad1-131">DataType</span></span><br/>     | <span data-ttu-id="14ad1-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14ad1-132">string</span></span><br/>  | <span data-ttu-id="14ad1-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="14ad1-133">xs:string</span></span><br/>       |
| <span data-ttu-id="14ad1-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="14ad1-134">DefaultValue</span></span><br/> | <span data-ttu-id="14ad1-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14ad1-135">string</span></span><br/>  | <span data-ttu-id="14ad1-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="14ad1-136">undefined</span></span><br/>       |
| <span data-ttu-id="14ad1-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="14ad1-137">MaxLength</span></span><br/>    | <span data-ttu-id="14ad1-138">integer</span><span class="sxs-lookup"><span data-stu-id="14ad1-138">integer</span></span><br/> | <span data-ttu-id="14ad1-139">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="14ad1-139">undefined</span></span><br/>       |
| <span data-ttu-id="14ad1-140">Minlength</span><span class="sxs-lookup"><span data-stu-id="14ad1-140">MinLength</span></span><br/>    | <span data-ttu-id="14ad1-141">integer</span><span class="sxs-lookup"><span data-stu-id="14ad1-141">integer</span></span><br/> | <span data-ttu-id="14ad1-142">1</span><span class="sxs-lookup"><span data-stu-id="14ad1-142">1</span></span><br/>               |
| <span data-ttu-id="14ad1-143">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="14ad1-143">Mandatory</span></span><br/>    | <span data-ttu-id="14ad1-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14ad1-144">string</span></span><br/>  | <span data-ttu-id="14ad1-145">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="14ad1-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="14ad1-146">Unittype</span><span class="sxs-lookup"><span data-stu-id="14ad1-146">UnitType</span></span><br/>     | <span data-ttu-id="14ad1-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14ad1-147">string</span></span><br/>  | <span data-ttu-id="14ad1-148">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="14ad1-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="14ad1-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="14ad1-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14ad1-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="14ad1-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




