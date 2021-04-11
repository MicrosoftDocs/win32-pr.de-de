---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: "\"Pgewatermarktextfontsize\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678630b7b7f6650a1317efef95c30effc71c6082
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050736"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="55fce-104">"Pgewatermarktextfontsize"</span><span class="sxs-lookup"><span data-stu-id="55fce-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="55fce-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="55fce-105">This topic is not current.</span></span> <span data-ttu-id="55fce-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="55fce-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="55fce-107">Definiert die verfügbaren Schriftgrößen für den Wasserzeichen Text.</span><span class="sxs-lookup"><span data-stu-id="55fce-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="55fce-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="55fce-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="55fce-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="55fce-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="55fce-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="55fce-110">Element Information</span></span>



| <span data-ttu-id="55fce-111">Name</span><span class="sxs-lookup"><span data-stu-id="55fce-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="55fce-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="55fce-112">Element Type</span></span> <br/>   | <span data-ttu-id="55fce-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="55fce-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="55fce-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="55fce-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="55fce-115">Seite</span><span class="sxs-lookup"><span data-stu-id="55fce-115">Page</span></span><br/>                            |
| <span data-ttu-id="55fce-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="55fce-116">Notes</span></span> <br/>          | <span data-ttu-id="55fce-117">Mit dem Element "pgewatermark" verknüpft</span><span class="sxs-lookup"><span data-stu-id="55fce-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="55fce-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="55fce-118">Structure Content</span></span>

<span data-ttu-id="55fce-119">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="55fce-119">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="55fce-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55fce-120">Structure Properties</span></span>

<span data-ttu-id="55fce-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="55fce-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="55fce-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55fce-122">Property</span></span>                | <span data-ttu-id="55fce-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="55fce-123">xsi:type</span></span>           | <span data-ttu-id="55fce-124">Wert</span><span class="sxs-lookup"><span data-stu-id="55fce-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="55fce-125">DataType</span><span class="sxs-lookup"><span data-stu-id="55fce-125">DataType</span></span><br/>     | <span data-ttu-id="55fce-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="55fce-126">string</span></span><br/>  | <span data-ttu-id="55fce-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="55fce-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="55fce-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="55fce-128">DefaultValue</span></span><br/> | <span data-ttu-id="55fce-129">integer</span><span class="sxs-lookup"><span data-stu-id="55fce-129">integer</span></span><br/> | <span data-ttu-id="55fce-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="55fce-130">undefined</span></span><br/>       |
| <span data-ttu-id="55fce-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="55fce-131">MaxValue</span></span><br/>     | <span data-ttu-id="55fce-132">integer</span><span class="sxs-lookup"><span data-stu-id="55fce-132">integer</span></span><br/> | <span data-ttu-id="55fce-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="55fce-133">undefined</span></span><br/>       |
| <span data-ttu-id="55fce-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="55fce-134">MinValue</span></span><br/>     | <span data-ttu-id="55fce-135">integer</span><span class="sxs-lookup"><span data-stu-id="55fce-135">integer</span></span><br/> | <span data-ttu-id="55fce-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="55fce-136">undefined</span></span><br/>       |
| <span data-ttu-id="55fce-137">Mehrere</span><span class="sxs-lookup"><span data-stu-id="55fce-137">Multiple</span></span><br/>     | <span data-ttu-id="55fce-138">integer</span><span class="sxs-lookup"><span data-stu-id="55fce-138">integer</span></span><br/> | <span data-ttu-id="55fce-139">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="55fce-139">undefined</span></span><br/>       |
| <span data-ttu-id="55fce-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="55fce-140">Mandatory</span></span><br/>    | <span data-ttu-id="55fce-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="55fce-141">string</span></span><br/>  | <span data-ttu-id="55fce-142">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="55fce-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="55fce-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="55fce-143">UnitType</span></span><br/>     | <span data-ttu-id="55fce-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="55fce-144">string</span></span><br/>  | <span data-ttu-id="55fce-145">Punkte</span><span class="sxs-lookup"><span data-stu-id="55fce-145">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="55fce-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55fce-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55fce-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="55fce-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




