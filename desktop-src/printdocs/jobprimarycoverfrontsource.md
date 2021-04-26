---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: f27c5e65-87b0-47a4-a5dc-27b52082f097
title: JobPrimaryCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f45b4125ce7d899597631abf4e01211724bee8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993956"
---
# <a name="jobprimarycoverfrontsource"></a><span data-ttu-id="745fe-104">JobPrimaryCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="745fe-104">JobPrimaryCoverFrontSource</span></span>

<span data-ttu-id="745fe-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="745fe-105">This topic is not current.</span></span> <span data-ttu-id="745fe-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="745fe-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="745fe-107">Gibt die Quelle für ein benutzerdefiniertes Front Cover-Primärblatt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="745fe-107">Specifies the source for a custom front-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="745fe-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="745fe-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="745fe-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="745fe-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="745fe-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="745fe-110">Element Information</span></span>



| <span data-ttu-id="745fe-111">Name</span><span class="sxs-lookup"><span data-stu-id="745fe-111">Name</span></span> | <span data-ttu-id="745fe-112">Wert</span><span class="sxs-lookup"><span data-stu-id="745fe-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="745fe-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="745fe-113">Element Type</span></span> <br/>   | <span data-ttu-id="745fe-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="745fe-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="745fe-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="745fe-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="745fe-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="745fe-116">Job</span></span><br/>                             |
| <span data-ttu-id="745fe-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="745fe-117">Notes</span></span> <br/>          | <span data-ttu-id="745fe-118">Verknüpft mit dem JobCoverFront-Element</span><span class="sxs-lookup"><span data-stu-id="745fe-118">Linked to JobCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="745fe-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="745fe-119">Structure Content</span></span>

<span data-ttu-id="745fe-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="745fe-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="745fe-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="745fe-121">Structure Properties</span></span>

<span data-ttu-id="745fe-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="745fe-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="745fe-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="745fe-123">Property</span></span>                | <span data-ttu-id="745fe-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="745fe-124">xsi:type</span></span>           | <span data-ttu-id="745fe-125">Wert</span><span class="sxs-lookup"><span data-stu-id="745fe-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="745fe-126">DataType</span><span class="sxs-lookup"><span data-stu-id="745fe-126">DataType</span></span><br/>     | <span data-ttu-id="745fe-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="745fe-127">string</span></span><br/>  | <span data-ttu-id="745fe-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="745fe-128">xs:string</span></span><br/>       |
| <span data-ttu-id="745fe-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="745fe-129">DefaultValue</span></span><br/> | <span data-ttu-id="745fe-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="745fe-130">string</span></span><br/>  | <span data-ttu-id="745fe-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="745fe-131">undefined</span></span><br/>       |
| <span data-ttu-id="745fe-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="745fe-132">MaxLength</span></span><br/>    | <span data-ttu-id="745fe-133">integer</span><span class="sxs-lookup"><span data-stu-id="745fe-133">integer</span></span><br/> | <span data-ttu-id="745fe-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="745fe-134">undefined</span></span><br/>       |
| <span data-ttu-id="745fe-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="745fe-135">MinLength</span></span><br/>    | <span data-ttu-id="745fe-136">integer</span><span class="sxs-lookup"><span data-stu-id="745fe-136">integer</span></span><br/> | <span data-ttu-id="745fe-137">1</span><span class="sxs-lookup"><span data-stu-id="745fe-137">1</span></span><br/>               |
| <span data-ttu-id="745fe-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="745fe-138">Mandatory</span></span><br/>    | <span data-ttu-id="745fe-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="745fe-139">string</span></span><br/>  | <span data-ttu-id="745fe-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="745fe-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="745fe-141">Unittype</span><span class="sxs-lookup"><span data-stu-id="745fe-141">UnitType</span></span><br/>     | <span data-ttu-id="745fe-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="745fe-142">string</span></span><br/>  | <span data-ttu-id="745fe-143">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="745fe-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="745fe-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="745fe-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="745fe-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="745fe-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




