---
description: Erfahren Sie mehr über das JobPrimaryCoverBackSource-Element, das die Quelle für ein benutzerdefiniertes primäres Back-Cover-Blatt für den Auftrag angibt.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ed9bbc1b49e230eabc3fd7f45773a73401e058
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408693"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="92db9-103">JobPrimaryCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="92db9-103">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="92db9-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="92db9-104">This topic is not current.</span></span> <span data-ttu-id="92db9-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="92db9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="92db9-106">Gibt die Quelle für ein benutzerdefiniertes primäres Back-Cover-Blatt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="92db9-106">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="92db9-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="92db9-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92db9-108">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="92db9-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="92db9-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="92db9-109">Element Information</span></span>



| <span data-ttu-id="92db9-110">Name</span><span class="sxs-lookup"><span data-stu-id="92db9-110">Name</span></span> | <span data-ttu-id="92db9-111">Wert</span><span class="sxs-lookup"><span data-stu-id="92db9-111">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="92db9-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="92db9-112">Element Type</span></span> <br/>   | <span data-ttu-id="92db9-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="92db9-113">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="92db9-114">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="92db9-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="92db9-115">Auftrag</span><span class="sxs-lookup"><span data-stu-id="92db9-115">Job</span></span><br/>                            |
| <span data-ttu-id="92db9-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="92db9-116">Notes</span></span> <br/>          | <span data-ttu-id="92db9-117">Mit JobCoverBack-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="92db9-117">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="92db9-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="92db9-118">Structure Content</span></span>

<span data-ttu-id="92db9-119">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="92db9-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="92db9-120">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="92db9-120">Structure Properties</span></span>

<span data-ttu-id="92db9-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="92db9-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="92db9-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="92db9-122">Property</span></span>                | <span data-ttu-id="92db9-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="92db9-123">xsi:type</span></span>           | <span data-ttu-id="92db9-124">Wert</span><span class="sxs-lookup"><span data-stu-id="92db9-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="92db9-125">DataType</span><span class="sxs-lookup"><span data-stu-id="92db9-125">DataType</span></span><br/>     | <span data-ttu-id="92db9-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92db9-126">string</span></span><br/>  | <span data-ttu-id="92db9-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="92db9-127">xs:string</span></span><br/>       |
| <span data-ttu-id="92db9-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="92db9-128">DefaultValue</span></span><br/> | <span data-ttu-id="92db9-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92db9-129">string</span></span><br/>  | <span data-ttu-id="92db9-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="92db9-130">undefined</span></span><br/>       |
| <span data-ttu-id="92db9-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="92db9-131">MaxLength</span></span><br/>    | <span data-ttu-id="92db9-132">integer</span><span class="sxs-lookup"><span data-stu-id="92db9-132">integer</span></span><br/> | <span data-ttu-id="92db9-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="92db9-133">undefined</span></span><br/>       |
| <span data-ttu-id="92db9-134">Minlength</span><span class="sxs-lookup"><span data-stu-id="92db9-134">MinLength</span></span><br/>    | <span data-ttu-id="92db9-135">integer</span><span class="sxs-lookup"><span data-stu-id="92db9-135">integer</span></span><br/> | <span data-ttu-id="92db9-136">1</span><span class="sxs-lookup"><span data-stu-id="92db9-136">1</span></span><br/>               |
| <span data-ttu-id="92db9-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="92db9-137">Mandatory</span></span><br/>    | <span data-ttu-id="92db9-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92db9-138">string</span></span><br/>  | <span data-ttu-id="92db9-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="92db9-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="92db9-140">Unittype</span><span class="sxs-lookup"><span data-stu-id="92db9-140">UnitType</span></span><br/>     | <span data-ttu-id="92db9-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92db9-141">string</span></span><br/>  | <span data-ttu-id="92db9-142">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="92db9-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="92db9-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92db9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92db9-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="92db9-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




