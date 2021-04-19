---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: Jobcomment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ebfbd2e62c18153dd0930197b6f49cbb3480d6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355735"
---
# <a name="jobcomment"></a><span data-ttu-id="e80e9-104">Jobcomment</span><span class="sxs-lookup"><span data-stu-id="e80e9-104">JobComment</span></span>

<span data-ttu-id="e80e9-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e80e9-105">This topic is not current.</span></span> <span data-ttu-id="e80e9-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e80e9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e80e9-107">Gibt einen Kommentar an, der dem Auftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e80e9-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="e80e9-108">Beispiel: "Bitte übermitteln Sie den Raum 1234, wenn dies abgeschlossen ist".</span><span class="sxs-lookup"><span data-stu-id="e80e9-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="e80e9-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e80e9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e80e9-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e80e9-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e80e9-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e80e9-111">Element Information</span></span>



| <span data-ttu-id="e80e9-112">Name</span><span class="sxs-lookup"><span data-stu-id="e80e9-112">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="e80e9-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e80e9-113">Element Type</span></span> <br/>   | <span data-ttu-id="e80e9-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e80e9-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="e80e9-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="e80e9-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e80e9-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e80e9-116">Job</span></span><br/>          |
| <span data-ttu-id="e80e9-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e80e9-117">Notes</span></span> <br/>          | <span data-ttu-id="e80e9-118">Keine</span><span class="sxs-lookup"><span data-stu-id="e80e9-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="e80e9-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e80e9-119">Structure Content</span></span>

<span data-ttu-id="e80e9-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e80e9-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e80e9-121">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e80e9-121">Structure Properties</span></span>

<span data-ttu-id="e80e9-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e80e9-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e80e9-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e80e9-123">Property</span></span>                | <span data-ttu-id="e80e9-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e80e9-124">xsi:type</span></span>           | <span data-ttu-id="e80e9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e80e9-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e80e9-126">DataType</span><span class="sxs-lookup"><span data-stu-id="e80e9-126">DataType</span></span><br/>     | <span data-ttu-id="e80e9-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e80e9-127">string</span></span><br/>  | <span data-ttu-id="e80e9-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e80e9-128">xs:string</span></span><br/>       |
| <span data-ttu-id="e80e9-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e80e9-129">DefaultValue</span></span><br/> | <span data-ttu-id="e80e9-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e80e9-130">string</span></span><br/>  | <span data-ttu-id="e80e9-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e80e9-131">undefined</span></span><br/>       |
| <span data-ttu-id="e80e9-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e80e9-132">MaxLength</span></span><br/>    | <span data-ttu-id="e80e9-133">integer</span><span class="sxs-lookup"><span data-stu-id="e80e9-133">integer</span></span><br/> | <span data-ttu-id="e80e9-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e80e9-134">undefined</span></span><br/>       |
| <span data-ttu-id="e80e9-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="e80e9-135">MinLength</span></span><br/>    | <span data-ttu-id="e80e9-136">integer</span><span class="sxs-lookup"><span data-stu-id="e80e9-136">integer</span></span><br/> | <span data-ttu-id="e80e9-137">1</span><span class="sxs-lookup"><span data-stu-id="e80e9-137">1</span></span><br/>               |
| <span data-ttu-id="e80e9-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="e80e9-138">Mandatory</span></span><br/>    | <span data-ttu-id="e80e9-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e80e9-139">string</span></span><br/>  | <span data-ttu-id="e80e9-140">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="e80e9-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e80e9-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="e80e9-141">UnitType</span></span><br/>     | <span data-ttu-id="e80e9-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e80e9-142">string</span></span><br/>  | <span data-ttu-id="e80e9-143">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e80e9-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e80e9-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e80e9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e80e9-145">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="e80e9-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




