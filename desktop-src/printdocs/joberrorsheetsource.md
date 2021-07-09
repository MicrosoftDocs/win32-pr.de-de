---
description: Hier finden Sie Informationen zum JobErrorSheetSource-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 6de13ed8-bf15-4e2c-b42a-ea8178a6b5f9
title: JobErrorSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656d71422c46800d6155c1dea1e221f9c6dfe021
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549388"
---
# <a name="joberrorsheetsource"></a><span data-ttu-id="36cb3-105">JobErrorSheetSource</span><span class="sxs-lookup"><span data-stu-id="36cb3-105">JobErrorSheetSource</span></span>

<span data-ttu-id="36cb3-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="36cb3-106">This topic is not current.</span></span> <span data-ttu-id="36cb3-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="36cb3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="36cb3-108">Gibt die Quelle für ein benutzerdefiniertes Fehlerblatt an.</span><span class="sxs-lookup"><span data-stu-id="36cb3-108">Specifies the source for a custom error sheet.</span></span>

-   [<span data-ttu-id="36cb3-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="36cb3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="36cb3-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="36cb3-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="36cb3-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="36cb3-111">Element Information</span></span>



| <span data-ttu-id="36cb3-112">Name</span><span class="sxs-lookup"><span data-stu-id="36cb3-112">Name</span></span> | <span data-ttu-id="36cb3-113">Wert</span><span class="sxs-lookup"><span data-stu-id="36cb3-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="36cb3-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="36cb3-114">Element Type</span></span> <br/>   | <span data-ttu-id="36cb3-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="36cb3-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="36cb3-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="36cb3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="36cb3-117">Dokument</span><span class="sxs-lookup"><span data-stu-id="36cb3-117">Document</span></span><br/>                        |
| <span data-ttu-id="36cb3-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36cb3-118">Notes</span></span> <br/>          | <span data-ttu-id="36cb3-119">Mit JobErrorSheet-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="36cb3-119">Linked to JobErrorSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="36cb3-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="36cb3-120">Structure Content</span></span>

<span data-ttu-id="36cb3-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="36cb3-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobErrorSheetSource">
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

## <a name="structure-properties"></a><span data-ttu-id="36cb3-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="36cb3-122">Structure Properties</span></span>

<span data-ttu-id="36cb3-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="36cb3-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="36cb3-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="36cb3-124">Property</span></span>                | <span data-ttu-id="36cb3-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="36cb3-125">xsi:type</span></span>           | <span data-ttu-id="36cb3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="36cb3-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="36cb3-127">DataType</span><span class="sxs-lookup"><span data-stu-id="36cb3-127">DataType</span></span><br/>     | <span data-ttu-id="36cb3-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="36cb3-128">string</span></span><br/>  | <span data-ttu-id="36cb3-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="36cb3-129">xs:string</span></span><br/>       |
| <span data-ttu-id="36cb3-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="36cb3-130">DefaultValue</span></span><br/> | <span data-ttu-id="36cb3-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="36cb3-131">string</span></span><br/>  | <span data-ttu-id="36cb3-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="36cb3-132">undefined</span></span><br/>       |
| <span data-ttu-id="36cb3-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="36cb3-133">MaxLength</span></span><br/>    | <span data-ttu-id="36cb3-134">integer</span><span class="sxs-lookup"><span data-stu-id="36cb3-134">integer</span></span><br/> | <span data-ttu-id="36cb3-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="36cb3-135">undefined</span></span><br/>       |
| <span data-ttu-id="36cb3-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="36cb3-136">MinLength</span></span><br/>    | <span data-ttu-id="36cb3-137">integer</span><span class="sxs-lookup"><span data-stu-id="36cb3-137">integer</span></span><br/> | <span data-ttu-id="36cb3-138">1</span><span class="sxs-lookup"><span data-stu-id="36cb3-138">1</span></span><br/>               |
| <span data-ttu-id="36cb3-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="36cb3-139">Mandatory</span></span><br/>    | <span data-ttu-id="36cb3-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="36cb3-140">string</span></span><br/>  | <span data-ttu-id="36cb3-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="36cb3-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="36cb3-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="36cb3-142">UnitType</span></span><br/>     | <span data-ttu-id="36cb3-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="36cb3-143">string</span></span><br/>  | <span data-ttu-id="36cb3-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="36cb3-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="36cb3-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36cb3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36cb3-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="36cb3-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




