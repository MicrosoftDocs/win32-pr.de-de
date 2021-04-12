---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563ed1746743d3329e0cd31c84c32bb8b407c56c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351808"
---
# <a name="documentpageranges"></a><span data-ttu-id="00f17-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="00f17-104">DocumentPageRanges</span></span>

<span data-ttu-id="00f17-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="00f17-105">This topic is not current.</span></span> <span data-ttu-id="00f17-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="00f17-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="00f17-107">Beschreibt den Ausgabebereich des Dokuments in Seiten.</span><span class="sxs-lookup"><span data-stu-id="00f17-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="00f17-108">Der Parameterwert muss der folgenden Struktur entsprechen:</span><span class="sxs-lookup"><span data-stu-id="00f17-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="00f17-109">PageRangeText: "*PageRange*" oder "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="00f17-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="00f17-110">PageRange: "*PageNumber*" oder "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="00f17-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="00f17-111">PageNumber: 1 bis n, wobei N die Anzahl der Seiten im Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="00f17-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="00f17-112">Wenn *PageNumber* > N, dann *PageNumber* = n.</span><span class="sxs-lookup"><span data-stu-id="00f17-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="00f17-113">Leerraum in der Zeichenfolge sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="00f17-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="00f17-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="00f17-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="00f17-115">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="00f17-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="00f17-116">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="00f17-116">Element Information</span></span>



| <span data-ttu-id="00f17-117">Name</span><span class="sxs-lookup"><span data-stu-id="00f17-117">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="00f17-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="00f17-118">Element Type</span></span> <br/>   | <span data-ttu-id="00f17-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="00f17-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="00f17-120">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="00f17-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="00f17-121">Dokument</span><span class="sxs-lookup"><span data-stu-id="00f17-121">Document</span></span><br/>     |
| <span data-ttu-id="00f17-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00f17-122">Notes</span></span> <br/>          | <span data-ttu-id="00f17-123">Keine</span><span class="sxs-lookup"><span data-stu-id="00f17-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="00f17-124">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="00f17-124">Structural Content</span></span>

<span data-ttu-id="00f17-125">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="00f17-125">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="00f17-126">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00f17-126">Structure Properties</span></span>

<span data-ttu-id="00f17-127">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="00f17-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="00f17-128">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="00f17-128">Property</span></span>                | <span data-ttu-id="00f17-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="00f17-129">xsi:type</span></span>           | <span data-ttu-id="00f17-130">Wert</span><span class="sxs-lookup"><span data-stu-id="00f17-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="00f17-131">DataType</span><span class="sxs-lookup"><span data-stu-id="00f17-131">DataType</span></span><br/>     | <span data-ttu-id="00f17-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="00f17-132">string</span></span><br/>  | <span data-ttu-id="00f17-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="00f17-133">xs:string</span></span><br/>       |
| <span data-ttu-id="00f17-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="00f17-134">DefaultValue</span></span><br/> | <span data-ttu-id="00f17-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="00f17-135">string</span></span><br/>  | <span data-ttu-id="00f17-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="00f17-136">undefined</span></span><br/>       |
| <span data-ttu-id="00f17-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="00f17-137">MaxLength</span></span><br/>    | <span data-ttu-id="00f17-138">integer</span><span class="sxs-lookup"><span data-stu-id="00f17-138">integer</span></span><br/> | <span data-ttu-id="00f17-139">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="00f17-139">undefined</span></span><br/>       |
| <span data-ttu-id="00f17-140">MinLength</span><span class="sxs-lookup"><span data-stu-id="00f17-140">MinLength</span></span><br/>    | <span data-ttu-id="00f17-141">integer</span><span class="sxs-lookup"><span data-stu-id="00f17-141">integer</span></span><br/> | <span data-ttu-id="00f17-142">1</span><span class="sxs-lookup"><span data-stu-id="00f17-142">1</span></span><br/>               |
| <span data-ttu-id="00f17-143">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="00f17-143">Mandatory</span></span><br/>    | <span data-ttu-id="00f17-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="00f17-144">string</span></span><br/>  | <span data-ttu-id="00f17-145">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="00f17-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="00f17-146">UnitType</span><span class="sxs-lookup"><span data-stu-id="00f17-146">UnitType</span></span><br/>     | <span data-ttu-id="00f17-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="00f17-147">string</span></span><br/>  | <span data-ttu-id="00f17-148">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="00f17-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="00f17-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00f17-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00f17-150">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="00f17-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




