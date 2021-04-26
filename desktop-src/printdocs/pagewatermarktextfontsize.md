---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cc8c7f3c9a692ffbe180c253d448d7c4e320d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999127"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="a8806-104">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="a8806-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="a8806-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a8806-105">This topic is not current.</span></span> <span data-ttu-id="a8806-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a8806-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a8806-107">Definiert die verfügbaren Schriftgrade für den Wasserzeichentext.</span><span class="sxs-lookup"><span data-stu-id="a8806-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="a8806-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a8806-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a8806-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="a8806-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a8806-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a8806-110">Element Information</span></span>



| <span data-ttu-id="a8806-111">Name</span><span class="sxs-lookup"><span data-stu-id="a8806-111">Name</span></span> | <span data-ttu-id="a8806-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a8806-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="a8806-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a8806-113">Element Type</span></span> <br/>   | <span data-ttu-id="a8806-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a8806-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="a8806-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a8806-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a8806-116">Seite</span><span class="sxs-lookup"><span data-stu-id="a8806-116">Page</span></span><br/>                            |
| <span data-ttu-id="a8806-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8806-117">Notes</span></span> <br/>          | <span data-ttu-id="a8806-118">Verknüpft mit dem PageWatermark-Element</span><span class="sxs-lookup"><span data-stu-id="a8806-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a8806-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="a8806-119">Structure Content</span></span>

<span data-ttu-id="a8806-120">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="a8806-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a8806-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8806-121">Structure Properties</span></span>

<span data-ttu-id="a8806-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a8806-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a8806-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a8806-123">Property</span></span>                | <span data-ttu-id="a8806-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a8806-124">xsi:type</span></span>           | <span data-ttu-id="a8806-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a8806-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a8806-126">DataType</span><span class="sxs-lookup"><span data-stu-id="a8806-126">DataType</span></span><br/>     | <span data-ttu-id="a8806-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a8806-127">string</span></span><br/>  | <span data-ttu-id="a8806-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a8806-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="a8806-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a8806-129">DefaultValue</span></span><br/> | <span data-ttu-id="a8806-130">integer</span><span class="sxs-lookup"><span data-stu-id="a8806-130">integer</span></span><br/> | <span data-ttu-id="a8806-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="a8806-131">undefined</span></span><br/>       |
| <span data-ttu-id="a8806-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a8806-132">MaxValue</span></span><br/>     | <span data-ttu-id="a8806-133">integer</span><span class="sxs-lookup"><span data-stu-id="a8806-133">integer</span></span><br/> | <span data-ttu-id="a8806-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="a8806-134">undefined</span></span><br/>       |
| <span data-ttu-id="a8806-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="a8806-135">MinValue</span></span><br/>     | <span data-ttu-id="a8806-136">integer</span><span class="sxs-lookup"><span data-stu-id="a8806-136">integer</span></span><br/> | <span data-ttu-id="a8806-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="a8806-137">undefined</span></span><br/>       |
| <span data-ttu-id="a8806-138">Mehrere</span><span class="sxs-lookup"><span data-stu-id="a8806-138">Multiple</span></span><br/>     | <span data-ttu-id="a8806-139">integer</span><span class="sxs-lookup"><span data-stu-id="a8806-139">integer</span></span><br/> | <span data-ttu-id="a8806-140">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="a8806-140">undefined</span></span><br/>       |
| <span data-ttu-id="a8806-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="a8806-141">Mandatory</span></span><br/>    | <span data-ttu-id="a8806-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a8806-142">string</span></span><br/>  | <span data-ttu-id="a8806-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="a8806-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a8806-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="a8806-144">UnitType</span></span><br/>     | <span data-ttu-id="a8806-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a8806-145">string</span></span><br/>  | <span data-ttu-id="a8806-146">Punkte</span><span class="sxs-lookup"><span data-stu-id="a8806-146">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="a8806-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a8806-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8806-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a8806-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




