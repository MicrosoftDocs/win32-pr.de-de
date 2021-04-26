---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d46a03cfb1b2129f4c89a6ea7c751e23cd565e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996877"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="27a52-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="27a52-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="27a52-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="27a52-105">This topic is not current.</span></span> <span data-ttu-id="27a52-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="27a52-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="27a52-107">Gibt die Transparenz für das Wasserzeichen an.</span><span class="sxs-lookup"><span data-stu-id="27a52-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="27a52-108">Vollständig undurchsichtig würde den Wert 0 haben.</span><span class="sxs-lookup"><span data-stu-id="27a52-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="27a52-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="27a52-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="27a52-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="27a52-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="27a52-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="27a52-111">Element Information</span></span>



| <span data-ttu-id="27a52-112">Name</span><span class="sxs-lookup"><span data-stu-id="27a52-112">Name</span></span> | <span data-ttu-id="27a52-113">Wert</span><span class="sxs-lookup"><span data-stu-id="27a52-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="27a52-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="27a52-114">Element Type</span></span> <br/>   | <span data-ttu-id="27a52-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="27a52-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="27a52-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="27a52-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="27a52-117">Seite</span><span class="sxs-lookup"><span data-stu-id="27a52-117">Page</span></span><br/>                            |
| <span data-ttu-id="27a52-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="27a52-118">Notes</span></span> <br/>          | <span data-ttu-id="27a52-119">Verknüpft mit dem PageWatermark-Element</span><span class="sxs-lookup"><span data-stu-id="27a52-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="27a52-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="27a52-120">Structure Content</span></span>

<span data-ttu-id="27a52-121">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="27a52-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="27a52-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="27a52-122">Structure Properties</span></span>

<span data-ttu-id="27a52-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="27a52-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="27a52-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="27a52-124">Property</span></span>                | <span data-ttu-id="27a52-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="27a52-125">xsi:type</span></span>           | <span data-ttu-id="27a52-126">Wert</span><span class="sxs-lookup"><span data-stu-id="27a52-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="27a52-127">DataType</span><span class="sxs-lookup"><span data-stu-id="27a52-127">DataType</span></span><br/>     | <span data-ttu-id="27a52-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="27a52-128">string</span></span><br/>  | <span data-ttu-id="27a52-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="27a52-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="27a52-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="27a52-130">DefaultValue</span></span><br/> | <span data-ttu-id="27a52-131">integer</span><span class="sxs-lookup"><span data-stu-id="27a52-131">integer</span></span><br/> | <span data-ttu-id="27a52-132">0</span><span class="sxs-lookup"><span data-stu-id="27a52-132">0</span></span><br/>               |
| <span data-ttu-id="27a52-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="27a52-133">MaxValue</span></span><br/>     | <span data-ttu-id="27a52-134">integer</span><span class="sxs-lookup"><span data-stu-id="27a52-134">integer</span></span><br/> | <span data-ttu-id="27a52-135">100</span><span class="sxs-lookup"><span data-stu-id="27a52-135">100</span></span><br/>             |
| <span data-ttu-id="27a52-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="27a52-136">MinValue</span></span><br/>     | <span data-ttu-id="27a52-137">integer</span><span class="sxs-lookup"><span data-stu-id="27a52-137">integer</span></span><br/> | <span data-ttu-id="27a52-138">0</span><span class="sxs-lookup"><span data-stu-id="27a52-138">0</span></span><br/>               |
| <span data-ttu-id="27a52-139">Mehrere</span><span class="sxs-lookup"><span data-stu-id="27a52-139">Multiple</span></span><br/>     | <span data-ttu-id="27a52-140">integer</span><span class="sxs-lookup"><span data-stu-id="27a52-140">integer</span></span><br/> | <span data-ttu-id="27a52-141">1</span><span class="sxs-lookup"><span data-stu-id="27a52-141">1</span></span><br/>               |
| <span data-ttu-id="27a52-142">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="27a52-142">Mandatory</span></span><br/>    | <span data-ttu-id="27a52-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="27a52-143">string</span></span><br/>  | <span data-ttu-id="27a52-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="27a52-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="27a52-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="27a52-145">UnitType</span></span><br/>     | <span data-ttu-id="27a52-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="27a52-146">string</span></span><br/>  | <span data-ttu-id="27a52-147">Prozent</span><span class="sxs-lookup"><span data-stu-id="27a52-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="27a52-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27a52-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27a52-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="27a52-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




