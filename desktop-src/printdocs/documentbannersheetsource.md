---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 3b55935f-3d71-43cc-9c59-5019d7eb5cc5
title: Documentbannersheetsource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 157cea832015c0dfb208e3f89b31ec19ac2c4313
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106350601"
---
# <a name="documentbannersheetsource"></a><span data-ttu-id="272d3-104">Documentbannersheetsource</span><span class="sxs-lookup"><span data-stu-id="272d3-104">DocumentBannerSheetSource</span></span>

<span data-ttu-id="272d3-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="272d3-105">This topic is not current.</span></span> <span data-ttu-id="272d3-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="272d3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="272d3-107">Gibt die Quelle für ein benutzerdefiniertes Banner Blatt an.</span><span class="sxs-lookup"><span data-stu-id="272d3-107">Specifies the source for a custom banner sheet.</span></span>

-   [<span data-ttu-id="272d3-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="272d3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="272d3-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="272d3-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="272d3-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="272d3-110">Element Information</span></span>



| <span data-ttu-id="272d3-111">Name</span><span class="sxs-lookup"><span data-stu-id="272d3-111">Name</span></span>                       |                                                  |
|----------------------------|--------------------------------------------------|
| <span data-ttu-id="272d3-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="272d3-112">Element Type</span></span> <br/>   | <span data-ttu-id="272d3-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="272d3-113">ParameterDef</span></span><br/>                          |
| <span data-ttu-id="272d3-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="272d3-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="272d3-115">Dokument</span><span class="sxs-lookup"><span data-stu-id="272d3-115">Document</span></span><br/>                              |
| <span data-ttu-id="272d3-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="272d3-116">Notes</span></span> <br/>          | <span data-ttu-id="272d3-117">Verknüpft mit documentbannersheet-Element</span><span class="sxs-lookup"><span data-stu-id="272d3-117">Linked to DocumentBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="272d3-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="272d3-118">Structure Content</span></span>

<span data-ttu-id="272d3-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="272d3-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBannerSheetSource">
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

## <a name="structure-properties"></a><span data-ttu-id="272d3-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="272d3-120">Structure Properties</span></span>

<span data-ttu-id="272d3-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="272d3-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="272d3-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="272d3-122">Property</span></span>                | <span data-ttu-id="272d3-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="272d3-123">xsi:type</span></span>           | <span data-ttu-id="272d3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="272d3-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="272d3-125">DataType</span><span class="sxs-lookup"><span data-stu-id="272d3-125">DataType</span></span><br/>     | <span data-ttu-id="272d3-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="272d3-126">string</span></span><br/>  | <span data-ttu-id="272d3-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="272d3-127">xs:string</span></span><br/>       |
| <span data-ttu-id="272d3-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="272d3-128">DefaultValue</span></span><br/> | <span data-ttu-id="272d3-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="272d3-129">string</span></span><br/>  | <span data-ttu-id="272d3-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="272d3-130">undefined</span></span><br/>       |
| <span data-ttu-id="272d3-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="272d3-131">MaxLength</span></span><br/>    | <span data-ttu-id="272d3-132">integer</span><span class="sxs-lookup"><span data-stu-id="272d3-132">integer</span></span><br/> | <span data-ttu-id="272d3-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="272d3-133">undefined</span></span><br/>       |
| <span data-ttu-id="272d3-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="272d3-134">MinLength</span></span><br/>    | <span data-ttu-id="272d3-135">integer</span><span class="sxs-lookup"><span data-stu-id="272d3-135">integer</span></span><br/> | <span data-ttu-id="272d3-136">1</span><span class="sxs-lookup"><span data-stu-id="272d3-136">1</span></span><br/>               |
| <span data-ttu-id="272d3-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="272d3-137">Mandatory</span></span><br/>    | <span data-ttu-id="272d3-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="272d3-138">string</span></span><br/>  | <span data-ttu-id="272d3-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="272d3-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="272d3-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="272d3-140">UnitType</span></span><br/>     | <span data-ttu-id="272d3-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="272d3-141">string</span></span><br/>  | <span data-ttu-id="272d3-142">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="272d3-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="272d3-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="272d3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="272d3-144">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="272d3-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




