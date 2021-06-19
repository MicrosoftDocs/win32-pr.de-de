---
description: Abrufen von Informationen zum PageWatermarkTransparency-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba405c3cd4a269edc4585ad8cba4c81f2c05e9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394785"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="dd38c-105">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="dd38c-105">PageWatermarkTransparency</span></span>

<span data-ttu-id="dd38c-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="dd38c-106">This topic is not current.</span></span> <span data-ttu-id="dd38c-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="dd38c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dd38c-108">Gibt die Transparenz für das Wasserzeichen an.</span><span class="sxs-lookup"><span data-stu-id="dd38c-108">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="dd38c-109">Vollständig undurchsichtig würde den Wert 0 haben.</span><span class="sxs-lookup"><span data-stu-id="dd38c-109">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="dd38c-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="dd38c-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dd38c-111">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="dd38c-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dd38c-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="dd38c-112">Element Information</span></span>



| <span data-ttu-id="dd38c-113">Name</span><span class="sxs-lookup"><span data-stu-id="dd38c-113">Name</span></span> | <span data-ttu-id="dd38c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="dd38c-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="dd38c-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="dd38c-115">Element Type</span></span> <br/>   | <span data-ttu-id="dd38c-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dd38c-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="dd38c-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="dd38c-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dd38c-118">Seite</span><span class="sxs-lookup"><span data-stu-id="dd38c-118">Page</span></span><br/>                            |
| <span data-ttu-id="dd38c-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd38c-119">Notes</span></span> <br/>          | <span data-ttu-id="dd38c-120">Verknüpft mit dem PageWatermark-Element</span><span class="sxs-lookup"><span data-stu-id="dd38c-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dd38c-121">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="dd38c-121">Structure Content</span></span>

<span data-ttu-id="dd38c-122">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="dd38c-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="dd38c-123">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd38c-123">Structure Properties</span></span>

<span data-ttu-id="dd38c-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dd38c-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dd38c-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dd38c-125">Property</span></span>                | <span data-ttu-id="dd38c-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dd38c-126">xsi:type</span></span>           | <span data-ttu-id="dd38c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="dd38c-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dd38c-128">DataType</span><span class="sxs-lookup"><span data-stu-id="dd38c-128">DataType</span></span><br/>     | <span data-ttu-id="dd38c-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="dd38c-129">string</span></span><br/>  | <span data-ttu-id="dd38c-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dd38c-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="dd38c-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dd38c-131">DefaultValue</span></span><br/> | <span data-ttu-id="dd38c-132">integer</span><span class="sxs-lookup"><span data-stu-id="dd38c-132">integer</span></span><br/> | <span data-ttu-id="dd38c-133">0</span><span class="sxs-lookup"><span data-stu-id="dd38c-133">0</span></span><br/>               |
| <span data-ttu-id="dd38c-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dd38c-134">MaxValue</span></span><br/>     | <span data-ttu-id="dd38c-135">integer</span><span class="sxs-lookup"><span data-stu-id="dd38c-135">integer</span></span><br/> | <span data-ttu-id="dd38c-136">100</span><span class="sxs-lookup"><span data-stu-id="dd38c-136">100</span></span><br/>             |
| <span data-ttu-id="dd38c-137">Minvalue</span><span class="sxs-lookup"><span data-stu-id="dd38c-137">MinValue</span></span><br/>     | <span data-ttu-id="dd38c-138">integer</span><span class="sxs-lookup"><span data-stu-id="dd38c-138">integer</span></span><br/> | <span data-ttu-id="dd38c-139">0</span><span class="sxs-lookup"><span data-stu-id="dd38c-139">0</span></span><br/>               |
| <span data-ttu-id="dd38c-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="dd38c-140">Multiple</span></span><br/>     | <span data-ttu-id="dd38c-141">integer</span><span class="sxs-lookup"><span data-stu-id="dd38c-141">integer</span></span><br/> | <span data-ttu-id="dd38c-142">1</span><span class="sxs-lookup"><span data-stu-id="dd38c-142">1</span></span><br/>               |
| <span data-ttu-id="dd38c-143">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="dd38c-143">Mandatory</span></span><br/>    | <span data-ttu-id="dd38c-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="dd38c-144">string</span></span><br/>  | <span data-ttu-id="dd38c-145">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="dd38c-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dd38c-146">Unittype</span><span class="sxs-lookup"><span data-stu-id="dd38c-146">UnitType</span></span><br/>     | <span data-ttu-id="dd38c-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="dd38c-147">string</span></span><br/>  | <span data-ttu-id="dd38c-148">Prozent</span><span class="sxs-lookup"><span data-stu-id="dd38c-148">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="dd38c-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd38c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd38c-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="dd38c-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




