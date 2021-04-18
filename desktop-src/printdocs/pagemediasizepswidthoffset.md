---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: Pagemediasizepswidthoffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cb8440af2b35bbe8f3f4a82a567beee43d1d44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106361131"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="b4bc2-104">Pagemediasizepswidthoffset</span><span class="sxs-lookup"><span data-stu-id="b4bc2-104">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="b4bc2-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b4bc2-105">This topic is not current.</span></span> <span data-ttu-id="b4bc2-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b4bc2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b4bc2-107">Gibt den Offset an, der senkrecht zur Richtung der Feed-Ausrichtung (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)) steht.</span><span class="sxs-lookup"><span data-stu-id="b4bc2-107">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="b4bc2-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b4bc2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b4bc2-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b4bc2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b4bc2-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b4bc2-110">Element Information</span></span>



| <span data-ttu-id="b4bc2-111">Name</span><span class="sxs-lookup"><span data-stu-id="b4bc2-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b4bc2-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="b4bc2-112">Element Type</span></span> <br/>   | <span data-ttu-id="b4bc2-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b4bc2-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="b4bc2-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="b4bc2-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b4bc2-115">Seite</span><span class="sxs-lookup"><span data-stu-id="b4bc2-115">Page</span></span><br/>                                             |
| <span data-ttu-id="b4bc2-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4bc2-116">Notes</span></span> <br/>          | <span data-ttu-id="b4bc2-117">Verknüpft mit PageMediaSize-Element, customps-Option</span><span class="sxs-lookup"><span data-stu-id="b4bc2-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b4bc2-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b4bc2-118">Structure Content</span></span>

<span data-ttu-id="b4bc2-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="b4bc2-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidthOffset">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="b4bc2-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4bc2-120">Structure Properties</span></span>

<span data-ttu-id="b4bc2-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b4bc2-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b4bc2-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4bc2-122">Property</span></span>                | <span data-ttu-id="b4bc2-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b4bc2-123">xsi:type</span></span>           | <span data-ttu-id="b4bc2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b4bc2-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b4bc2-125">DataType</span><span class="sxs-lookup"><span data-stu-id="b4bc2-125">DataType</span></span><br/>     | <span data-ttu-id="b4bc2-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b4bc2-126">string</span></span><br/>  | <span data-ttu-id="b4bc2-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b4bc2-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="b4bc2-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b4bc2-128">DefaultValue</span></span><br/> | <span data-ttu-id="b4bc2-129">integer</span><span class="sxs-lookup"><span data-stu-id="b4bc2-129">integer</span></span><br/> | <span data-ttu-id="b4bc2-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b4bc2-130">undefined</span></span><br/>       |
| <span data-ttu-id="b4bc2-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b4bc2-131">MaxValue</span></span><br/>     | <span data-ttu-id="b4bc2-132">integer</span><span class="sxs-lookup"><span data-stu-id="b4bc2-132">integer</span></span><br/> | <span data-ttu-id="b4bc2-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b4bc2-133">undefined</span></span><br/>       |
| <span data-ttu-id="b4bc2-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="b4bc2-134">MinValue</span></span><br/>     | <span data-ttu-id="b4bc2-135">integer</span><span class="sxs-lookup"><span data-stu-id="b4bc2-135">integer</span></span><br/> | <span data-ttu-id="b4bc2-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b4bc2-136">undefined</span></span><br/>       |
| <span data-ttu-id="b4bc2-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="b4bc2-137">Mandatory</span></span><br/>    | <span data-ttu-id="b4bc2-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b4bc2-138">string</span></span><br/>  | <span data-ttu-id="b4bc2-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="b4bc2-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b4bc2-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="b4bc2-140">Multiple</span></span><br/>     | <span data-ttu-id="b4bc2-141">integer</span><span class="sxs-lookup"><span data-stu-id="b4bc2-141">integer</span></span><br/> | <span data-ttu-id="b4bc2-142">1</span><span class="sxs-lookup"><span data-stu-id="b4bc2-142">1</span></span><br/>               |
| <span data-ttu-id="b4bc2-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="b4bc2-143">UnitType</span></span><br/>     | <span data-ttu-id="b4bc2-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b4bc2-144">string</span></span><br/>  | <span data-ttu-id="b4bc2-145">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="b4bc2-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b4bc2-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4bc2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4bc2-147">Datei Format Spezifikation für PostScript-Drucker Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4bc2-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="b4bc2-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="b4bc2-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




