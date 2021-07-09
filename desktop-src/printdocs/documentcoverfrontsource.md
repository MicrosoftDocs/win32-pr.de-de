---
description: Hier finden Sie Informationen zum DocumentCoverFrontSource-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: DocumentCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb6ecb089eb271e0b8fff136e73a20194f0c8f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548758"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="9014e-105">DocumentCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="9014e-105">DocumentCoverFrontSource</span></span>

<span data-ttu-id="9014e-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9014e-106">This topic is not current.</span></span> <span data-ttu-id="9014e-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="9014e-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9014e-108">Gibt die Quelle für ein benutzerdefiniertes Front-Cover-Blatt an.</span><span class="sxs-lookup"><span data-stu-id="9014e-108">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="9014e-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9014e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9014e-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="9014e-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9014e-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9014e-111">Element Information</span></span>



| <span data-ttu-id="9014e-112">Name</span><span class="sxs-lookup"><span data-stu-id="9014e-112">Name</span></span> | <span data-ttu-id="9014e-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9014e-113">Value</span></span> |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="9014e-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="9014e-114">Element Type</span></span> <br/>   | <span data-ttu-id="9014e-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9014e-115">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="9014e-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="9014e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9014e-117">Dokument</span><span class="sxs-lookup"><span data-stu-id="9014e-117">Document</span></span><br/>                             |
| <span data-ttu-id="9014e-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9014e-118">Notes</span></span> <br/>          | <span data-ttu-id="9014e-119">Mit DocumentCoverFront-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="9014e-119">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="9014e-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="9014e-120">Structure Content</span></span>

<span data-ttu-id="9014e-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="9014e-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="9014e-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="9014e-122">Structure Properties</span></span>

<span data-ttu-id="9014e-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9014e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9014e-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9014e-124">Property</span></span>                | <span data-ttu-id="9014e-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9014e-125">xsi:type</span></span>           | <span data-ttu-id="9014e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9014e-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9014e-127">DataType</span><span class="sxs-lookup"><span data-stu-id="9014e-127">DataType</span></span><br/>     | <span data-ttu-id="9014e-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9014e-128">string</span></span><br/>  | <span data-ttu-id="9014e-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="9014e-129">xs:string</span></span><br/>       |
| <span data-ttu-id="9014e-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9014e-130">DefaultValue</span></span><br/> | <span data-ttu-id="9014e-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9014e-131">string</span></span><br/>  | <span data-ttu-id="9014e-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="9014e-132">undefined</span></span><br/>       |
| <span data-ttu-id="9014e-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="9014e-133">MaxLength</span></span><br/>    | <span data-ttu-id="9014e-134">integer</span><span class="sxs-lookup"><span data-stu-id="9014e-134">integer</span></span><br/> | <span data-ttu-id="9014e-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="9014e-135">undefined</span></span><br/>       |
| <span data-ttu-id="9014e-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="9014e-136">MinLength</span></span><br/>    | <span data-ttu-id="9014e-137">integer</span><span class="sxs-lookup"><span data-stu-id="9014e-137">integer</span></span><br/> | <span data-ttu-id="9014e-138">1</span><span class="sxs-lookup"><span data-stu-id="9014e-138">1</span></span><br/>               |
| <span data-ttu-id="9014e-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="9014e-139">Mandatory</span></span><br/>    | <span data-ttu-id="9014e-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9014e-140">string</span></span><br/>  | <span data-ttu-id="9014e-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="9014e-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9014e-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="9014e-142">UnitType</span></span><br/>     | <span data-ttu-id="9014e-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9014e-143">string</span></span><br/>  | <span data-ttu-id="9014e-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="9014e-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="9014e-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9014e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9014e-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="9014e-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




