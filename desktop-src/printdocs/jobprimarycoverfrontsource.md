---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: f27c5e65-87b0-47a4-a5dc-27b52082f097
title: Jobprimarycoverfrontsource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3dfc50d060093c1c2ee1baf494305ae6afd6ce
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106361779"
---
# <a name="jobprimarycoverfrontsource"></a><span data-ttu-id="22a6b-104">Jobprimarycoverfrontsource</span><span class="sxs-lookup"><span data-stu-id="22a6b-104">JobPrimaryCoverFrontSource</span></span>

<span data-ttu-id="22a6b-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="22a6b-105">This topic is not current.</span></span> <span data-ttu-id="22a6b-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="22a6b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="22a6b-107">Gibt die Quelle für ein benutzerdefiniertes Front-Cover-primär Blatt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="22a6b-107">Specifies the source for a custom front-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="22a6b-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="22a6b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="22a6b-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="22a6b-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="22a6b-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="22a6b-110">Element Information</span></span>



| <span data-ttu-id="22a6b-111">Name</span><span class="sxs-lookup"><span data-stu-id="22a6b-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="22a6b-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="22a6b-112">Element Type</span></span> <br/>   | <span data-ttu-id="22a6b-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="22a6b-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="22a6b-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="22a6b-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="22a6b-115">Auftrag</span><span class="sxs-lookup"><span data-stu-id="22a6b-115">Job</span></span><br/>                             |
| <span data-ttu-id="22a6b-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="22a6b-116">Notes</span></span> <br/>          | <span data-ttu-id="22a6b-117">Verknüpft mit jobcoverfront-Element</span><span class="sxs-lookup"><span data-stu-id="22a6b-117">Linked to JobCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="22a6b-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="22a6b-118">Structure Content</span></span>

<span data-ttu-id="22a6b-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="22a6b-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="22a6b-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22a6b-120">Structure Properties</span></span>

<span data-ttu-id="22a6b-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="22a6b-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="22a6b-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22a6b-122">Property</span></span>                | <span data-ttu-id="22a6b-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="22a6b-123">xsi:type</span></span>           | <span data-ttu-id="22a6b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="22a6b-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="22a6b-125">DataType</span><span class="sxs-lookup"><span data-stu-id="22a6b-125">DataType</span></span><br/>     | <span data-ttu-id="22a6b-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22a6b-126">string</span></span><br/>  | <span data-ttu-id="22a6b-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="22a6b-127">xs:string</span></span><br/>       |
| <span data-ttu-id="22a6b-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="22a6b-128">DefaultValue</span></span><br/> | <span data-ttu-id="22a6b-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22a6b-129">string</span></span><br/>  | <span data-ttu-id="22a6b-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="22a6b-130">undefined</span></span><br/>       |
| <span data-ttu-id="22a6b-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="22a6b-131">MaxLength</span></span><br/>    | <span data-ttu-id="22a6b-132">integer</span><span class="sxs-lookup"><span data-stu-id="22a6b-132">integer</span></span><br/> | <span data-ttu-id="22a6b-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="22a6b-133">undefined</span></span><br/>       |
| <span data-ttu-id="22a6b-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="22a6b-134">MinLength</span></span><br/>    | <span data-ttu-id="22a6b-135">integer</span><span class="sxs-lookup"><span data-stu-id="22a6b-135">integer</span></span><br/> | <span data-ttu-id="22a6b-136">1</span><span class="sxs-lookup"><span data-stu-id="22a6b-136">1</span></span><br/>               |
| <span data-ttu-id="22a6b-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="22a6b-137">Mandatory</span></span><br/>    | <span data-ttu-id="22a6b-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22a6b-138">string</span></span><br/>  | <span data-ttu-id="22a6b-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="22a6b-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="22a6b-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="22a6b-140">UnitType</span></span><br/>     | <span data-ttu-id="22a6b-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22a6b-141">string</span></span><br/>  | <span data-ttu-id="22a6b-142">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="22a6b-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="22a6b-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22a6b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22a6b-144">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="22a6b-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




