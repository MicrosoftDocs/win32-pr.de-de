---
description: Abrufen von Informationen zum PageWatermarkTextFontSize-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb28044ca676dedfb136cb58190db90a06fd624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395995"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="1e9ac-105">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="1e9ac-105">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="1e9ac-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="1e9ac-106">This topic is not current.</span></span> <span data-ttu-id="1e9ac-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="1e9ac-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1e9ac-108">Definiert die verfügbaren Schriftgrade für den Wasserzeichentext.</span><span class="sxs-lookup"><span data-stu-id="1e9ac-108">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="1e9ac-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1e9ac-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1e9ac-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="1e9ac-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1e9ac-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1e9ac-111">Element Information</span></span>



| <span data-ttu-id="1e9ac-112">Name</span><span class="sxs-lookup"><span data-stu-id="1e9ac-112">Name</span></span> | <span data-ttu-id="1e9ac-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1e9ac-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="1e9ac-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="1e9ac-114">Element Type</span></span> <br/>   | <span data-ttu-id="1e9ac-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1e9ac-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="1e9ac-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="1e9ac-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1e9ac-117">Seite</span><span class="sxs-lookup"><span data-stu-id="1e9ac-117">Page</span></span><br/>                            |
| <span data-ttu-id="1e9ac-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1e9ac-118">Notes</span></span> <br/>          | <span data-ttu-id="1e9ac-119">Verknüpft mit dem PageWatermark-Element</span><span class="sxs-lookup"><span data-stu-id="1e9ac-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1e9ac-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="1e9ac-120">Structure Content</span></span>

<span data-ttu-id="1e9ac-121">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="1e9ac-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextFontSize">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">points</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="1e9ac-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e9ac-122">Structure Properties</span></span>

<span data-ttu-id="1e9ac-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1e9ac-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1e9ac-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1e9ac-124">Property</span></span>                | <span data-ttu-id="1e9ac-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1e9ac-125">xsi:type</span></span>           | <span data-ttu-id="1e9ac-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1e9ac-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1e9ac-127">DataType</span><span class="sxs-lookup"><span data-stu-id="1e9ac-127">DataType</span></span><br/>     | <span data-ttu-id="1e9ac-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e9ac-128">string</span></span><br/>  | <span data-ttu-id="1e9ac-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1e9ac-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="1e9ac-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1e9ac-130">DefaultValue</span></span><br/> | <span data-ttu-id="1e9ac-131">integer</span><span class="sxs-lookup"><span data-stu-id="1e9ac-131">integer</span></span><br/> | <span data-ttu-id="1e9ac-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="1e9ac-132">undefined</span></span><br/>       |
| <span data-ttu-id="1e9ac-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1e9ac-133">MaxValue</span></span><br/>     | <span data-ttu-id="1e9ac-134">integer</span><span class="sxs-lookup"><span data-stu-id="1e9ac-134">integer</span></span><br/> | <span data-ttu-id="1e9ac-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="1e9ac-135">undefined</span></span><br/>       |
| <span data-ttu-id="1e9ac-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="1e9ac-136">MinValue</span></span><br/>     | <span data-ttu-id="1e9ac-137">integer</span><span class="sxs-lookup"><span data-stu-id="1e9ac-137">integer</span></span><br/> | <span data-ttu-id="1e9ac-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="1e9ac-138">undefined</span></span><br/>       |
| <span data-ttu-id="1e9ac-139">Mehrere</span><span class="sxs-lookup"><span data-stu-id="1e9ac-139">Multiple</span></span><br/>     | <span data-ttu-id="1e9ac-140">integer</span><span class="sxs-lookup"><span data-stu-id="1e9ac-140">integer</span></span><br/> | <span data-ttu-id="1e9ac-141">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="1e9ac-141">undefined</span></span><br/>       |
| <span data-ttu-id="1e9ac-142">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="1e9ac-142">Mandatory</span></span><br/>    | <span data-ttu-id="1e9ac-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e9ac-143">string</span></span><br/>  | <span data-ttu-id="1e9ac-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="1e9ac-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1e9ac-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="1e9ac-145">UnitType</span></span><br/>     | <span data-ttu-id="1e9ac-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e9ac-146">string</span></span><br/>  | <span data-ttu-id="1e9ac-147">Punkte</span><span class="sxs-lookup"><span data-stu-id="1e9ac-147">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="1e9ac-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e9ac-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e9ac-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="1e9ac-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




