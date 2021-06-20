---
description: Erfahren Sie mehr über das DocumentBannerSheetSource-Element, das die Quelle für ein benutzerdefiniertes Bannerblatt angibt.
ms.assetid: 3b55935f-3d71-43cc-9c59-5019d7eb5cc5
title: DocumentBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33aa949982e98781c42cbf6aa770dbd4e3d1707
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409473"
---
# <a name="documentbannersheetsource"></a><span data-ttu-id="94a4d-103">DocumentBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="94a4d-103">DocumentBannerSheetSource</span></span>

<span data-ttu-id="94a4d-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="94a4d-104">This topic is not current.</span></span> <span data-ttu-id="94a4d-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="94a4d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="94a4d-106">Gibt die Quelle für ein benutzerdefiniertes Bannerblatt an.</span><span class="sxs-lookup"><span data-stu-id="94a4d-106">Specifies the source for a custom banner sheet.</span></span>

-   [<span data-ttu-id="94a4d-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="94a4d-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="94a4d-108">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="94a4d-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="94a4d-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="94a4d-109">Element Information</span></span>



| <span data-ttu-id="94a4d-110">Name</span><span class="sxs-lookup"><span data-stu-id="94a4d-110">Name</span></span> | <span data-ttu-id="94a4d-111">Wert</span><span class="sxs-lookup"><span data-stu-id="94a4d-111">Value</span></span> |
|----------------------------|--------------------------------------------------|
| <span data-ttu-id="94a4d-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="94a4d-112">Element Type</span></span> <br/>   | <span data-ttu-id="94a4d-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="94a4d-113">ParameterDef</span></span><br/>                          |
| <span data-ttu-id="94a4d-114">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="94a4d-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="94a4d-115">Dokument</span><span class="sxs-lookup"><span data-stu-id="94a4d-115">Document</span></span><br/>                              |
| <span data-ttu-id="94a4d-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="94a4d-116">Notes</span></span> <br/>          | <span data-ttu-id="94a4d-117">Verknüpft mit dem DocumentBannerSheet-Element</span><span class="sxs-lookup"><span data-stu-id="94a4d-117">Linked to DocumentBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="94a4d-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="94a4d-118">Structure Content</span></span>

<span data-ttu-id="94a4d-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="94a4d-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="94a4d-120">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="94a4d-120">Structure Properties</span></span>

<span data-ttu-id="94a4d-121">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="94a4d-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="94a4d-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94a4d-122">Property</span></span>                | <span data-ttu-id="94a4d-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="94a4d-123">xsi:type</span></span>           | <span data-ttu-id="94a4d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="94a4d-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="94a4d-125">DataType</span><span class="sxs-lookup"><span data-stu-id="94a4d-125">DataType</span></span><br/>     | <span data-ttu-id="94a4d-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="94a4d-126">string</span></span><br/>  | <span data-ttu-id="94a4d-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="94a4d-127">xs:string</span></span><br/>       |
| <span data-ttu-id="94a4d-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="94a4d-128">DefaultValue</span></span><br/> | <span data-ttu-id="94a4d-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="94a4d-129">string</span></span><br/>  | <span data-ttu-id="94a4d-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="94a4d-130">undefined</span></span><br/>       |
| <span data-ttu-id="94a4d-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="94a4d-131">MaxLength</span></span><br/>    | <span data-ttu-id="94a4d-132">integer</span><span class="sxs-lookup"><span data-stu-id="94a4d-132">integer</span></span><br/> | <span data-ttu-id="94a4d-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="94a4d-133">undefined</span></span><br/>       |
| <span data-ttu-id="94a4d-134">Minlength</span><span class="sxs-lookup"><span data-stu-id="94a4d-134">MinLength</span></span><br/>    | <span data-ttu-id="94a4d-135">integer</span><span class="sxs-lookup"><span data-stu-id="94a4d-135">integer</span></span><br/> | <span data-ttu-id="94a4d-136">1</span><span class="sxs-lookup"><span data-stu-id="94a4d-136">1</span></span><br/>               |
| <span data-ttu-id="94a4d-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="94a4d-137">Mandatory</span></span><br/>    | <span data-ttu-id="94a4d-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="94a4d-138">string</span></span><br/>  | <span data-ttu-id="94a4d-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="94a4d-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="94a4d-140">Unittype</span><span class="sxs-lookup"><span data-stu-id="94a4d-140">UnitType</span></span><br/>     | <span data-ttu-id="94a4d-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="94a4d-141">string</span></span><br/>  | <span data-ttu-id="94a4d-142">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="94a4d-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="94a4d-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94a4d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94a4d-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="94a4d-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




