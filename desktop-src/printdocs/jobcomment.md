---
description: Erfahren Sie mehr über das JobComment-Element, das einen Kommentar angibt, der dem Auftrag zugeordnet ist, z. B. Bitte senden Sie nach Abschluss an Raum 1234.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1decf4cf3af7b3a992b07d8008579ac005d3d14e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409043"
---
# <a name="jobcomment"></a><span data-ttu-id="b09a7-103">JobComment</span><span class="sxs-lookup"><span data-stu-id="b09a7-103">JobComment</span></span>

<span data-ttu-id="b09a7-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b09a7-104">This topic is not current.</span></span> <span data-ttu-id="b09a7-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="b09a7-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b09a7-106">Gibt einen Kommentar an, der dem Auftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b09a7-106">Specifies a comment associated with the job.</span></span> <span data-ttu-id="b09a7-107">Beispiel: "Please deliver to room 1234 when completed".</span><span class="sxs-lookup"><span data-stu-id="b09a7-107">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="b09a7-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b09a7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b09a7-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b09a7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b09a7-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b09a7-110">Element Information</span></span>



| <span data-ttu-id="b09a7-111">Name</span><span class="sxs-lookup"><span data-stu-id="b09a7-111">Name</span></span> | <span data-ttu-id="b09a7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b09a7-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="b09a7-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="b09a7-113">Element Type</span></span> <br/>   | <span data-ttu-id="b09a7-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b09a7-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="b09a7-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="b09a7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b09a7-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b09a7-116">Job</span></span><br/>          |
| <span data-ttu-id="b09a7-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b09a7-117">Notes</span></span> <br/>          | <span data-ttu-id="b09a7-118">Keine</span><span class="sxs-lookup"><span data-stu-id="b09a7-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="b09a7-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b09a7-119">Structure Content</span></span>

<span data-ttu-id="b09a7-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b09a7-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobComment">
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

## <a name="structure-properties"></a><span data-ttu-id="b09a7-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="b09a7-121">Structure Properties</span></span>

<span data-ttu-id="b09a7-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b09a7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b09a7-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b09a7-123">Property</span></span>                | <span data-ttu-id="b09a7-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b09a7-124">xsi:type</span></span>           | <span data-ttu-id="b09a7-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b09a7-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b09a7-126">DataType</span><span class="sxs-lookup"><span data-stu-id="b09a7-126">DataType</span></span><br/>     | <span data-ttu-id="b09a7-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b09a7-127">string</span></span><br/>  | <span data-ttu-id="b09a7-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="b09a7-128">xs:string</span></span><br/>       |
| <span data-ttu-id="b09a7-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b09a7-129">DefaultValue</span></span><br/> | <span data-ttu-id="b09a7-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b09a7-130">string</span></span><br/>  | <span data-ttu-id="b09a7-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b09a7-131">undefined</span></span><br/>       |
| <span data-ttu-id="b09a7-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="b09a7-132">MaxLength</span></span><br/>    | <span data-ttu-id="b09a7-133">integer</span><span class="sxs-lookup"><span data-stu-id="b09a7-133">integer</span></span><br/> | <span data-ttu-id="b09a7-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b09a7-134">undefined</span></span><br/>       |
| <span data-ttu-id="b09a7-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="b09a7-135">MinLength</span></span><br/>    | <span data-ttu-id="b09a7-136">integer</span><span class="sxs-lookup"><span data-stu-id="b09a7-136">integer</span></span><br/> | <span data-ttu-id="b09a7-137">1</span><span class="sxs-lookup"><span data-stu-id="b09a7-137">1</span></span><br/>               |
| <span data-ttu-id="b09a7-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="b09a7-138">Mandatory</span></span><br/>    | <span data-ttu-id="b09a7-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b09a7-139">string</span></span><br/>  | <span data-ttu-id="b09a7-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="b09a7-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b09a7-141">Unittype</span><span class="sxs-lookup"><span data-stu-id="b09a7-141">UnitType</span></span><br/>     | <span data-ttu-id="b09a7-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b09a7-142">string</span></span><br/>  | <span data-ttu-id="b09a7-143">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="b09a7-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="b09a7-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b09a7-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b09a7-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="b09a7-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




