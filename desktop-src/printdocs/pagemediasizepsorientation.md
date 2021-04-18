---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: Pagemediasizepsorientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a188c61d3bb3c47286b887406174a3fc41f3c58a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106365008"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="49959-104">Pagemediasizepsorientation</span><span class="sxs-lookup"><span data-stu-id="49959-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="49959-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="49959-105">This topic is not current.</span></span> <span data-ttu-id="49959-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="49959-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="49959-107">Gibt die Ausrichtung in Relation zur Richtung der Feed-Ausrichtung an (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="49959-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="49959-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="49959-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="49959-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="49959-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="49959-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="49959-110">Element Information</span></span>



| <span data-ttu-id="49959-111">Name</span><span class="sxs-lookup"><span data-stu-id="49959-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="49959-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="49959-112">Element Type</span></span> <br/>   | <span data-ttu-id="49959-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="49959-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="49959-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="49959-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="49959-115">Seite</span><span class="sxs-lookup"><span data-stu-id="49959-115">Page</span></span><br/>                                             |
| <span data-ttu-id="49959-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="49959-116">Notes</span></span> <br/>          | <span data-ttu-id="49959-117">Verknüpft mit PageMediaSize-Element, customps-Option</span><span class="sxs-lookup"><span data-stu-id="49959-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="49959-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="49959-118">Structure Content</span></span>

<span data-ttu-id="49959-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="49959-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
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
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="49959-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49959-120">Structure Properties</span></span>

<span data-ttu-id="49959-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="49959-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="49959-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="49959-122">Property</span></span>                | <span data-ttu-id="49959-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="49959-123">xsi:type</span></span>           | <span data-ttu-id="49959-124">Wert</span><span class="sxs-lookup"><span data-stu-id="49959-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="49959-125">DataType</span><span class="sxs-lookup"><span data-stu-id="49959-125">DataType</span></span><br/>     | <span data-ttu-id="49959-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="49959-126">string</span></span><br/>  | <span data-ttu-id="49959-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="49959-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="49959-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="49959-128">DefaultValue</span></span><br/> | <span data-ttu-id="49959-129">integer</span><span class="sxs-lookup"><span data-stu-id="49959-129">integer</span></span><br/> | <span data-ttu-id="49959-130">0</span><span class="sxs-lookup"><span data-stu-id="49959-130">0</span></span><br/>                 |
| <span data-ttu-id="49959-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="49959-131">MaxValue</span></span><br/>     | <span data-ttu-id="49959-132">integer</span><span class="sxs-lookup"><span data-stu-id="49959-132">integer</span></span><br/> | <span data-ttu-id="49959-133">3</span><span class="sxs-lookup"><span data-stu-id="49959-133">3</span></span><br/>                 |
| <span data-ttu-id="49959-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="49959-134">MinValue</span></span><br/>     | <span data-ttu-id="49959-135">integer</span><span class="sxs-lookup"><span data-stu-id="49959-135">integer</span></span><br/> | <span data-ttu-id="49959-136">0</span><span class="sxs-lookup"><span data-stu-id="49959-136">0</span></span><br/>                 |
| <span data-ttu-id="49959-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="49959-137">Mandatory</span></span><br/>    | <span data-ttu-id="49959-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="49959-138">string</span></span><br/>  | <span data-ttu-id="49959-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="49959-139">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="49959-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="49959-140">Multiple</span></span><br/>     | <span data-ttu-id="49959-141">integer</span><span class="sxs-lookup"><span data-stu-id="49959-141">integer</span></span><br/> | <span data-ttu-id="49959-142">1</span><span class="sxs-lookup"><span data-stu-id="49959-142">1</span></span><br/>                 |
| <span data-ttu-id="49959-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="49959-143">UnitType</span></span><br/>     | <span data-ttu-id="49959-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="49959-144">string</span></span><br/>  | <span data-ttu-id="49959-145">Pagemediasizeaufumum</span><span class="sxs-lookup"><span data-stu-id="49959-145">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="49959-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49959-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49959-147">Datei Format Spezifikation für PostScript-Drucker Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49959-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="49959-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="49959-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




