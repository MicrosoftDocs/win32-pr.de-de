---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: DocumentCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b558a044716c5c13ae012665193f958f8ce6aa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997897"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="4ca1a-104">DocumentCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="4ca1a-104">DocumentCoverFrontSource</span></span>

<span data-ttu-id="4ca1a-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-105">This topic is not current.</span></span> <span data-ttu-id="4ca1a-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="4ca1a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4ca1a-107">Gibt die Quelle für ein benutzerdefiniertes Front-Cover-Blatt an.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-107">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="4ca1a-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4ca1a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4ca1a-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4ca1a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4ca1a-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4ca1a-110">Element Information</span></span>



| <span data-ttu-id="4ca1a-111">Name</span><span class="sxs-lookup"><span data-stu-id="4ca1a-111">Name</span></span> | <span data-ttu-id="4ca1a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4ca1a-112">Value</span></span> |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="4ca1a-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4ca1a-113">Element Type</span></span> <br/>   | <span data-ttu-id="4ca1a-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4ca1a-114">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="4ca1a-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="4ca1a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4ca1a-116">Dokument</span><span class="sxs-lookup"><span data-stu-id="4ca1a-116">Document</span></span><br/>                             |
| <span data-ttu-id="4ca1a-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4ca1a-117">Notes</span></span> <br/>          | <span data-ttu-id="4ca1a-118">Mit DocumentCoverFront-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="4ca1a-118">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4ca1a-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4ca1a-119">Structure Content</span></span>

<span data-ttu-id="4ca1a-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="4ca1a-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverFrontSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a><span data-ttu-id="4ca1a-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ca1a-121">Structure Properties</span></span>

<span data-ttu-id="4ca1a-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4ca1a-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4ca1a-123">Property</span></span>                | <span data-ttu-id="4ca1a-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4ca1a-124">xsi:type</span></span>           | <span data-ttu-id="4ca1a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4ca1a-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4ca1a-126">DataType</span><span class="sxs-lookup"><span data-stu-id="4ca1a-126">DataType</span></span><br/>     | <span data-ttu-id="4ca1a-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ca1a-127">string</span></span><br/>  | <span data-ttu-id="4ca1a-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="4ca1a-128">xs:string</span></span><br/>       |
| <span data-ttu-id="4ca1a-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4ca1a-129">DefaultValue</span></span><br/> | <span data-ttu-id="4ca1a-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ca1a-130">string</span></span><br/>  | <span data-ttu-id="4ca1a-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4ca1a-131">undefined</span></span><br/>       |
| <span data-ttu-id="4ca1a-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="4ca1a-132">MaxLength</span></span><br/>    | <span data-ttu-id="4ca1a-133">integer</span><span class="sxs-lookup"><span data-stu-id="4ca1a-133">integer</span></span><br/> | <span data-ttu-id="4ca1a-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4ca1a-134">undefined</span></span><br/>       |
| <span data-ttu-id="4ca1a-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="4ca1a-135">MinLength</span></span><br/>    | <span data-ttu-id="4ca1a-136">integer</span><span class="sxs-lookup"><span data-stu-id="4ca1a-136">integer</span></span><br/> | <span data-ttu-id="4ca1a-137">1</span><span class="sxs-lookup"><span data-stu-id="4ca1a-137">1</span></span><br/>               |
| <span data-ttu-id="4ca1a-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-138">Mandatory</span></span><br/>    | <span data-ttu-id="4ca1a-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ca1a-139">string</span></span><br/>  | <span data-ttu-id="4ca1a-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="4ca1a-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4ca1a-141">Unittype</span><span class="sxs-lookup"><span data-stu-id="4ca1a-141">UnitType</span></span><br/>     | <span data-ttu-id="4ca1a-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ca1a-142">string</span></span><br/>  | <span data-ttu-id="4ca1a-143">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="4ca1a-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="4ca1a-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ca1a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ca1a-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="4ca1a-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




