---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: "\"Pgewatermarktransparenz\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e96382656b1092a0dbc71352e788208f70b34
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106364300"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="eab78-104">"Pgewatermarktransparenz"</span><span class="sxs-lookup"><span data-stu-id="eab78-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="eab78-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="eab78-105">This topic is not current.</span></span> <span data-ttu-id="eab78-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eab78-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eab78-107">Gibt die Transparenz für das Wasserzeichen an.</span><span class="sxs-lookup"><span data-stu-id="eab78-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="eab78-108">Vollständig nicht transparent wäre der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="eab78-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="eab78-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="eab78-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eab78-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="eab78-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="eab78-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="eab78-111">Element Information</span></span>



| <span data-ttu-id="eab78-112">Name</span><span class="sxs-lookup"><span data-stu-id="eab78-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="eab78-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="eab78-113">Element Type</span></span> <br/>   | <span data-ttu-id="eab78-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="eab78-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="eab78-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="eab78-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eab78-116">Seite</span><span class="sxs-lookup"><span data-stu-id="eab78-116">Page</span></span><br/>                            |
| <span data-ttu-id="eab78-117">Notizen</span><span class="sxs-lookup"><span data-stu-id="eab78-117">Notes</span></span> <br/>          | <span data-ttu-id="eab78-118">Mit dem Element "pgewatermark" verknüpft</span><span class="sxs-lookup"><span data-stu-id="eab78-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="eab78-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="eab78-119">Structure Content</span></span>

<span data-ttu-id="eab78-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="eab78-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="eab78-121">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eab78-121">Structure Properties</span></span>

<span data-ttu-id="eab78-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="eab78-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eab78-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eab78-123">Property</span></span>                | <span data-ttu-id="eab78-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="eab78-124">xsi:type</span></span>           | <span data-ttu-id="eab78-125">Wert</span><span class="sxs-lookup"><span data-stu-id="eab78-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="eab78-126">DataType</span><span class="sxs-lookup"><span data-stu-id="eab78-126">DataType</span></span><br/>     | <span data-ttu-id="eab78-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eab78-127">string</span></span><br/>  | <span data-ttu-id="eab78-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="eab78-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="eab78-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="eab78-129">DefaultValue</span></span><br/> | <span data-ttu-id="eab78-130">integer</span><span class="sxs-lookup"><span data-stu-id="eab78-130">integer</span></span><br/> | <span data-ttu-id="eab78-131">0</span><span class="sxs-lookup"><span data-stu-id="eab78-131">0</span></span><br/>               |
| <span data-ttu-id="eab78-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="eab78-132">MaxValue</span></span><br/>     | <span data-ttu-id="eab78-133">integer</span><span class="sxs-lookup"><span data-stu-id="eab78-133">integer</span></span><br/> | <span data-ttu-id="eab78-134">100</span><span class="sxs-lookup"><span data-stu-id="eab78-134">100</span></span><br/>             |
| <span data-ttu-id="eab78-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="eab78-135">MinValue</span></span><br/>     | <span data-ttu-id="eab78-136">integer</span><span class="sxs-lookup"><span data-stu-id="eab78-136">integer</span></span><br/> | <span data-ttu-id="eab78-137">0</span><span class="sxs-lookup"><span data-stu-id="eab78-137">0</span></span><br/>               |
| <span data-ttu-id="eab78-138">Mehrere</span><span class="sxs-lookup"><span data-stu-id="eab78-138">Multiple</span></span><br/>     | <span data-ttu-id="eab78-139">integer</span><span class="sxs-lookup"><span data-stu-id="eab78-139">integer</span></span><br/> | <span data-ttu-id="eab78-140">1</span><span class="sxs-lookup"><span data-stu-id="eab78-140">1</span></span><br/>               |
| <span data-ttu-id="eab78-141">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="eab78-141">Mandatory</span></span><br/>    | <span data-ttu-id="eab78-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eab78-142">string</span></span><br/>  | <span data-ttu-id="eab78-143">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="eab78-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="eab78-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="eab78-144">UnitType</span></span><br/>     | <span data-ttu-id="eab78-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eab78-145">string</span></span><br/>  | <span data-ttu-id="eab78-146">Prozent</span><span class="sxs-lookup"><span data-stu-id="eab78-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="eab78-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eab78-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eab78-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="eab78-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




