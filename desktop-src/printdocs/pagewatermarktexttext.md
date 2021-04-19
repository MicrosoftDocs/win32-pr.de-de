---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: "\"Pgewatermarktexttext\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef2310efaa91532493f7add14de8c2510e24e9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353641"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="e5c32-104">"Pgewatermarktexttext"</span><span class="sxs-lookup"><span data-stu-id="e5c32-104">PageWatermarkTextText</span></span>

<span data-ttu-id="e5c32-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e5c32-105">This topic is not current.</span></span> <span data-ttu-id="e5c32-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e5c32-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e5c32-107">Gibt den Text des Wasserzeichens an.</span><span class="sxs-lookup"><span data-stu-id="e5c32-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="e5c32-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e5c32-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e5c32-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e5c32-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e5c32-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e5c32-110">Element Information</span></span>



| <span data-ttu-id="e5c32-111">Name</span><span class="sxs-lookup"><span data-stu-id="e5c32-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="e5c32-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e5c32-112">Element Type</span></span> <br/>   | <span data-ttu-id="e5c32-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e5c32-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="e5c32-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="e5c32-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e5c32-115">Seite</span><span class="sxs-lookup"><span data-stu-id="e5c32-115">Page</span></span><br/>                            |
| <span data-ttu-id="e5c32-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5c32-116">Notes</span></span> <br/>          | <span data-ttu-id="e5c32-117">Mit dem Element "pgewatermark" verknüpft</span><span class="sxs-lookup"><span data-stu-id="e5c32-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e5c32-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="e5c32-118">Structure Content</span></span>

<span data-ttu-id="e5c32-119">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e5c32-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextText">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="e5c32-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5c32-120">Structure Properties</span></span>

<span data-ttu-id="e5c32-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e5c32-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e5c32-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e5c32-122">Property</span></span>                | <span data-ttu-id="e5c32-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e5c32-123">xsi:type</span></span>           | <span data-ttu-id="e5c32-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e5c32-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e5c32-125">DataType</span><span class="sxs-lookup"><span data-stu-id="e5c32-125">DataType</span></span><br/>     | <span data-ttu-id="e5c32-126">String</span><span class="sxs-lookup"><span data-stu-id="e5c32-126">String</span></span><br/>  | <span data-ttu-id="e5c32-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="e5c32-127">xs:string</span></span><br/>       |
| <span data-ttu-id="e5c32-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e5c32-128">DefaultValue</span></span><br/> | <span data-ttu-id="e5c32-129">Integer</span><span class="sxs-lookup"><span data-stu-id="e5c32-129">Integer</span></span><br/> | <span data-ttu-id="e5c32-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e5c32-130">undefined</span></span><br/>       |
| <span data-ttu-id="e5c32-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e5c32-131">MaxLength</span></span><br/>    | <span data-ttu-id="e5c32-132">Integer</span><span class="sxs-lookup"><span data-stu-id="e5c32-132">Integer</span></span><br/> | <span data-ttu-id="e5c32-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="e5c32-133">undefined</span></span><br/>       |
| <span data-ttu-id="e5c32-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="e5c32-134">MinLength</span></span><br/>    | <span data-ttu-id="e5c32-135">Integer</span><span class="sxs-lookup"><span data-stu-id="e5c32-135">Integer</span></span><br/> | <span data-ttu-id="e5c32-136">1</span><span class="sxs-lookup"><span data-stu-id="e5c32-136">1</span></span><br/>               |
| <span data-ttu-id="e5c32-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="e5c32-137">Mandatory</span></span><br/>    | <span data-ttu-id="e5c32-138">String</span><span class="sxs-lookup"><span data-stu-id="e5c32-138">String</span></span><br/>  | <span data-ttu-id="e5c32-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="e5c32-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e5c32-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="e5c32-140">UnitType</span></span><br/>     | <span data-ttu-id="e5c32-141">String</span><span class="sxs-lookup"><span data-stu-id="e5c32-141">String</span></span><br/>  | <span data-ttu-id="e5c32-142">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e5c32-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e5c32-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5c32-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5c32-144">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="e5c32-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




