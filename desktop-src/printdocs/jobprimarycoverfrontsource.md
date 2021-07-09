---
description: Abrufen von Informationen zum JobPrimaryCoverFrontSource-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: f27c5e65-87b0-47a4-a5dc-27b52082f097
title: JobPrimaryCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4698d826e59e513d5eb171381cd1b18ea4a751
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549398"
---
# <a name="jobprimarycoverfrontsource"></a><span data-ttu-id="e2558-105">JobPrimaryCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="e2558-105">JobPrimaryCoverFrontSource</span></span>

<span data-ttu-id="e2558-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e2558-106">This topic is not current.</span></span> <span data-ttu-id="e2558-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="e2558-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e2558-108">Gibt die Quelle für ein benutzerdefiniertes Front Cover-Primärblatt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="e2558-108">Specifies the source for a custom front-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="e2558-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e2558-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e2558-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e2558-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e2558-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e2558-111">Element Information</span></span>



| <span data-ttu-id="e2558-112">Name</span><span class="sxs-lookup"><span data-stu-id="e2558-112">Name</span></span> | <span data-ttu-id="e2558-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e2558-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="e2558-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e2558-114">Element Type</span></span> <br/>   | <span data-ttu-id="e2558-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e2558-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="e2558-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="e2558-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e2558-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e2558-117">Job</span></span><br/>                             |
| <span data-ttu-id="e2558-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2558-118">Notes</span></span> <br/>          | <span data-ttu-id="e2558-119">Verknüpft mit dem JobCoverFront-Element</span><span class="sxs-lookup"><span data-stu-id="e2558-119">Linked to JobCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e2558-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e2558-120">Structure Content</span></span>

<span data-ttu-id="e2558-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="e2558-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverFrontSource">
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

## <a name="structure-properties"></a><span data-ttu-id="e2558-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2558-122">Structure Properties</span></span>

<span data-ttu-id="e2558-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e2558-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e2558-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e2558-124">Property</span></span>                | <span data-ttu-id="e2558-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e2558-125">xsi:type</span></span>           | <span data-ttu-id="e2558-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e2558-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e2558-127">DataType</span><span class="sxs-lookup"><span data-stu-id="e2558-127">DataType</span></span><br/>     | <span data-ttu-id="e2558-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e2558-128">string</span></span><br/>  | <span data-ttu-id="e2558-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="e2558-129">xs:string</span></span><br/>       |
| <span data-ttu-id="e2558-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e2558-130">DefaultValue</span></span><br/> | <span data-ttu-id="e2558-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e2558-131">string</span></span><br/>  | <span data-ttu-id="e2558-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e2558-132">undefined</span></span><br/>       |
| <span data-ttu-id="e2558-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e2558-133">MaxLength</span></span><br/>    | <span data-ttu-id="e2558-134">integer</span><span class="sxs-lookup"><span data-stu-id="e2558-134">integer</span></span><br/> | <span data-ttu-id="e2558-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e2558-135">undefined</span></span><br/>       |
| <span data-ttu-id="e2558-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="e2558-136">MinLength</span></span><br/>    | <span data-ttu-id="e2558-137">integer</span><span class="sxs-lookup"><span data-stu-id="e2558-137">integer</span></span><br/> | <span data-ttu-id="e2558-138">1</span><span class="sxs-lookup"><span data-stu-id="e2558-138">1</span></span><br/>               |
| <span data-ttu-id="e2558-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="e2558-139">Mandatory</span></span><br/>    | <span data-ttu-id="e2558-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e2558-140">string</span></span><br/>  | <span data-ttu-id="e2558-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="e2558-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e2558-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="e2558-142">UnitType</span></span><br/>     | <span data-ttu-id="e2558-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e2558-143">string</span></span><br/>  | <span data-ttu-id="e2558-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e2558-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e2558-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2558-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2558-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="e2558-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




