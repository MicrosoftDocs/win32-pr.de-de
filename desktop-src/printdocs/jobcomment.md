---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210b80d4f81771dfa98d79d4ecf187b3ef145f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998347"
---
# <a name="jobcomment"></a><span data-ttu-id="a4f40-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="a4f40-104">JobComment</span></span>

<span data-ttu-id="a4f40-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a4f40-105">This topic is not current.</span></span> <span data-ttu-id="a4f40-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a4f40-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a4f40-107">Gibt einen Kommentar an, der dem Auftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a4f40-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="a4f40-108">Beispiel: "Please deliver to room 1234 when completed".</span><span class="sxs-lookup"><span data-stu-id="a4f40-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="a4f40-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a4f40-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a4f40-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="a4f40-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a4f40-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a4f40-111">Element Information</span></span>



| <span data-ttu-id="a4f40-112">Name</span><span class="sxs-lookup"><span data-stu-id="a4f40-112">Name</span></span> | <span data-ttu-id="a4f40-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a4f40-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="a4f40-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a4f40-114">Element Type</span></span> <br/>   | <span data-ttu-id="a4f40-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a4f40-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="a4f40-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a4f40-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a4f40-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a4f40-117">Job</span></span><br/>          |
| <span data-ttu-id="a4f40-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a4f40-118">Notes</span></span> <br/>          | <span data-ttu-id="a4f40-119">Keine</span><span class="sxs-lookup"><span data-stu-id="a4f40-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="a4f40-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="a4f40-120">Structure Content</span></span>

<span data-ttu-id="a4f40-121">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="a4f40-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a4f40-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4f40-122">Structure Properties</span></span>

<span data-ttu-id="a4f40-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a4f40-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a4f40-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4f40-124">Property</span></span>                | <span data-ttu-id="a4f40-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a4f40-125">xsi:type</span></span>           | <span data-ttu-id="a4f40-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a4f40-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a4f40-127">DataType</span><span class="sxs-lookup"><span data-stu-id="a4f40-127">DataType</span></span><br/>     | <span data-ttu-id="a4f40-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4f40-128">string</span></span><br/>  | <span data-ttu-id="a4f40-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="a4f40-129">xs:string</span></span><br/>       |
| <span data-ttu-id="a4f40-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a4f40-130">DefaultValue</span></span><br/> | <span data-ttu-id="a4f40-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4f40-131">string</span></span><br/>  | <span data-ttu-id="a4f40-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="a4f40-132">undefined</span></span><br/>       |
| <span data-ttu-id="a4f40-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a4f40-133">MaxLength</span></span><br/>    | <span data-ttu-id="a4f40-134">integer</span><span class="sxs-lookup"><span data-stu-id="a4f40-134">integer</span></span><br/> | <span data-ttu-id="a4f40-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="a4f40-135">undefined</span></span><br/>       |
| <span data-ttu-id="a4f40-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="a4f40-136">MinLength</span></span><br/>    | <span data-ttu-id="a4f40-137">integer</span><span class="sxs-lookup"><span data-stu-id="a4f40-137">integer</span></span><br/> | <span data-ttu-id="a4f40-138">1</span><span class="sxs-lookup"><span data-stu-id="a4f40-138">1</span></span><br/>               |
| <span data-ttu-id="a4f40-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="a4f40-139">Mandatory</span></span><br/>    | <span data-ttu-id="a4f40-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4f40-140">string</span></span><br/>  | <span data-ttu-id="a4f40-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="a4f40-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a4f40-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="a4f40-142">UnitType</span></span><br/>     | <span data-ttu-id="a4f40-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4f40-143">string</span></span><br/>  | <span data-ttu-id="a4f40-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a4f40-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a4f40-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4f40-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4f40-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a4f40-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




