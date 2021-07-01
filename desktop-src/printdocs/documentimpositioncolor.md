---
description: Erfahren Sie mehr über den DocumentImpositionColor-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: DocumentImpositionColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b747487c19160d29778f306a91b62cf43d245f65
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120005"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="71059-105">DocumentImpositionColor</span><span class="sxs-lookup"><span data-stu-id="71059-105">DocumentImpositionColor</span></span>

<span data-ttu-id="71059-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="71059-106">This topic is not current.</span></span> <span data-ttu-id="71059-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="71059-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="71059-108">Anwendungsinhalt mit der angegebenen benannten Farbe MUSS in allen Farbtrennungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="71059-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="71059-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="71059-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="71059-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="71059-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="71059-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="71059-111">Element Information</span></span>



| <span data-ttu-id="71059-112">Name</span><span class="sxs-lookup"><span data-stu-id="71059-112">Name</span></span> | <span data-ttu-id="71059-113">Wert</span><span class="sxs-lookup"><span data-stu-id="71059-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="71059-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="71059-114">Element Type</span></span> <br/>   | <span data-ttu-id="71059-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="71059-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="71059-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="71059-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="71059-117">Dokument</span><span class="sxs-lookup"><span data-stu-id="71059-117">Document</span></span><br/>     |
| <span data-ttu-id="71059-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="71059-118">Notes</span></span> <br/>          | <span data-ttu-id="71059-119">Keine</span><span class="sxs-lookup"><span data-stu-id="71059-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="71059-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="71059-120">Structure Content</span></span>

<span data-ttu-id="71059-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="71059-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentImpositionColor">
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

## <a name="structure-properties"></a><span data-ttu-id="71059-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="71059-122">Structure Properties</span></span>

<span data-ttu-id="71059-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="71059-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="71059-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="71059-124">Property</span></span>                | <span data-ttu-id="71059-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="71059-125">xsi:type</span></span>           | <span data-ttu-id="71059-126">Wert</span><span class="sxs-lookup"><span data-stu-id="71059-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="71059-127">DataType</span><span class="sxs-lookup"><span data-stu-id="71059-127">DataType</span></span><br/>     | <span data-ttu-id="71059-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71059-128">string</span></span><br/>  | <span data-ttu-id="71059-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="71059-129">xs:string</span></span><br/>       |
| <span data-ttu-id="71059-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="71059-130">DefaultValue</span></span><br/> | <span data-ttu-id="71059-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71059-131">string</span></span><br/>  | <span data-ttu-id="71059-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="71059-132">undefined</span></span><br/>       |
| <span data-ttu-id="71059-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="71059-133">MaxLength</span></span><br/>    | <span data-ttu-id="71059-134">integer</span><span class="sxs-lookup"><span data-stu-id="71059-134">integer</span></span><br/> | <span data-ttu-id="71059-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="71059-135">undefined</span></span><br/>       |
| <span data-ttu-id="71059-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="71059-136">MinLength</span></span><br/>    | <span data-ttu-id="71059-137">integer</span><span class="sxs-lookup"><span data-stu-id="71059-137">integer</span></span><br/> | <span data-ttu-id="71059-138">1</span><span class="sxs-lookup"><span data-stu-id="71059-138">1</span></span><br/>               |
| <span data-ttu-id="71059-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="71059-139">Mandatory</span></span><br/>    | <span data-ttu-id="71059-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71059-140">string</span></span><br/>  | <span data-ttu-id="71059-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="71059-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="71059-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="71059-142">UnitType</span></span><br/>     | <span data-ttu-id="71059-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71059-143">string</span></span><br/>  | <span data-ttu-id="71059-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="71059-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="71059-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71059-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71059-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="71059-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




