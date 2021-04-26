---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 3b55935f-3d71-43cc-9c59-5019d7eb5cc5
title: DocumentBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5a2802094a0d20cf1b8b0a177a5b774489bb37
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996317"
---
# <a name="documentbannersheetsource"></a><span data-ttu-id="73194-104">DocumentBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="73194-104">DocumentBannerSheetSource</span></span>

<span data-ttu-id="73194-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="73194-105">This topic is not current.</span></span> <span data-ttu-id="73194-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="73194-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="73194-107">Gibt die Quelle für ein benutzerdefiniertes Bannerblatt an.</span><span class="sxs-lookup"><span data-stu-id="73194-107">Specifies the source for a custom banner sheet.</span></span>

-   [<span data-ttu-id="73194-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="73194-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="73194-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="73194-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="73194-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="73194-110">Element Information</span></span>



| <span data-ttu-id="73194-111">Name</span><span class="sxs-lookup"><span data-stu-id="73194-111">Name</span></span> | <span data-ttu-id="73194-112">Wert</span><span class="sxs-lookup"><span data-stu-id="73194-112">Value</span></span> |
|----------------------------|--------------------------------------------------|
| <span data-ttu-id="73194-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="73194-113">Element Type</span></span> <br/>   | <span data-ttu-id="73194-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="73194-114">ParameterDef</span></span><br/>                          |
| <span data-ttu-id="73194-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="73194-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="73194-116">Dokument</span><span class="sxs-lookup"><span data-stu-id="73194-116">Document</span></span><br/>                              |
| <span data-ttu-id="73194-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="73194-117">Notes</span></span> <br/>          | <span data-ttu-id="73194-118">Mit DocumentBannerSheet-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="73194-118">Linked to DocumentBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="73194-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="73194-119">Structure Content</span></span>

<span data-ttu-id="73194-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="73194-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="73194-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="73194-121">Structure Properties</span></span>

<span data-ttu-id="73194-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="73194-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="73194-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="73194-123">Property</span></span>                | <span data-ttu-id="73194-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="73194-124">xsi:type</span></span>           | <span data-ttu-id="73194-125">Wert</span><span class="sxs-lookup"><span data-stu-id="73194-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="73194-126">DataType</span><span class="sxs-lookup"><span data-stu-id="73194-126">DataType</span></span><br/>     | <span data-ttu-id="73194-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73194-127">string</span></span><br/>  | <span data-ttu-id="73194-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="73194-128">xs:string</span></span><br/>       |
| <span data-ttu-id="73194-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="73194-129">DefaultValue</span></span><br/> | <span data-ttu-id="73194-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73194-130">string</span></span><br/>  | <span data-ttu-id="73194-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="73194-131">undefined</span></span><br/>       |
| <span data-ttu-id="73194-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="73194-132">MaxLength</span></span><br/>    | <span data-ttu-id="73194-133">integer</span><span class="sxs-lookup"><span data-stu-id="73194-133">integer</span></span><br/> | <span data-ttu-id="73194-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="73194-134">undefined</span></span><br/>       |
| <span data-ttu-id="73194-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="73194-135">MinLength</span></span><br/>    | <span data-ttu-id="73194-136">integer</span><span class="sxs-lookup"><span data-stu-id="73194-136">integer</span></span><br/> | <span data-ttu-id="73194-137">1</span><span class="sxs-lookup"><span data-stu-id="73194-137">1</span></span><br/>               |
| <span data-ttu-id="73194-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="73194-138">Mandatory</span></span><br/>    | <span data-ttu-id="73194-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73194-139">string</span></span><br/>  | <span data-ttu-id="73194-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="73194-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="73194-141">Unittype</span><span class="sxs-lookup"><span data-stu-id="73194-141">UnitType</span></span><br/>     | <span data-ttu-id="73194-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73194-142">string</span></span><br/>  | <span data-ttu-id="73194-143">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="73194-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="73194-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73194-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73194-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="73194-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




