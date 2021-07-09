---
description: Hier finden Sie Informationen zum PageMediaSizePSWidthOffset-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: PageMediaSizePSWidthOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265acad803dbc334be115440e195967465b3ef50
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549102"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="8fa3f-105">PageMediaSizePSWidthOffset</span><span class="sxs-lookup"><span data-stu-id="8fa3f-105">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="8fa3f-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-106">This topic is not current.</span></span> <span data-ttu-id="8fa3f-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="8fa3f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8fa3f-108">Gibt den Offset zur Ausrichtungsrichtung des Feeds an (Referenz PostScript [Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="8fa3f-108">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="8fa3f-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8fa3f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8fa3f-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="8fa3f-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8fa3f-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8fa3f-111">Element Information</span></span>



| <span data-ttu-id="8fa3f-112">Name</span><span class="sxs-lookup"><span data-stu-id="8fa3f-112">Name</span></span> | <span data-ttu-id="8fa3f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8fa3f-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8fa3f-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="8fa3f-114">Element Type</span></span> <br/>   | <span data-ttu-id="8fa3f-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8fa3f-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="8fa3f-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="8fa3f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8fa3f-117">Seite</span><span class="sxs-lookup"><span data-stu-id="8fa3f-117">Page</span></span><br/>                                             |
| <span data-ttu-id="8fa3f-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8fa3f-118">Notes</span></span> <br/>          | <span data-ttu-id="8fa3f-119">Mit PageMediaSize-Element verknüpft, CustomPS-Option</span><span class="sxs-lookup"><span data-stu-id="8fa3f-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8fa3f-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="8fa3f-120">Structure Content</span></span>

<span data-ttu-id="8fa3f-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="8fa3f-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8fa3f-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="8fa3f-122">Structure Properties</span></span>

<span data-ttu-id="8fa3f-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8fa3f-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8fa3f-124">Property</span></span>                | <span data-ttu-id="8fa3f-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8fa3f-125">xsi:type</span></span>           | <span data-ttu-id="8fa3f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8fa3f-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8fa3f-127">DataType</span><span class="sxs-lookup"><span data-stu-id="8fa3f-127">DataType</span></span><br/>     | <span data-ttu-id="8fa3f-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8fa3f-128">string</span></span><br/>  | <span data-ttu-id="8fa3f-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8fa3f-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="8fa3f-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8fa3f-130">DefaultValue</span></span><br/> | <span data-ttu-id="8fa3f-131">integer</span><span class="sxs-lookup"><span data-stu-id="8fa3f-131">integer</span></span><br/> | <span data-ttu-id="8fa3f-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="8fa3f-132">undefined</span></span><br/>       |
| <span data-ttu-id="8fa3f-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8fa3f-133">MaxValue</span></span><br/>     | <span data-ttu-id="8fa3f-134">integer</span><span class="sxs-lookup"><span data-stu-id="8fa3f-134">integer</span></span><br/> | <span data-ttu-id="8fa3f-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="8fa3f-135">undefined</span></span><br/>       |
| <span data-ttu-id="8fa3f-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="8fa3f-136">MinValue</span></span><br/>     | <span data-ttu-id="8fa3f-137">integer</span><span class="sxs-lookup"><span data-stu-id="8fa3f-137">integer</span></span><br/> | <span data-ttu-id="8fa3f-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="8fa3f-138">undefined</span></span><br/>       |
| <span data-ttu-id="8fa3f-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-139">Mandatory</span></span><br/>    | <span data-ttu-id="8fa3f-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8fa3f-140">string</span></span><br/>  | <span data-ttu-id="8fa3f-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="8fa3f-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8fa3f-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="8fa3f-142">Multiple</span></span><br/>     | <span data-ttu-id="8fa3f-143">integer</span><span class="sxs-lookup"><span data-stu-id="8fa3f-143">integer</span></span><br/> | <span data-ttu-id="8fa3f-144">1</span><span class="sxs-lookup"><span data-stu-id="8fa3f-144">1</span></span><br/>               |
| <span data-ttu-id="8fa3f-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="8fa3f-145">UnitType</span></span><br/>     | <span data-ttu-id="8fa3f-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8fa3f-146">string</span></span><br/>  | <span data-ttu-id="8fa3f-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="8fa3f-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="8fa3f-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8fa3f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fa3f-149">PostScript Spezifikation des Dateiformats der Druckerbeschreibung</span><span class="sxs-lookup"><span data-stu-id="8fa3f-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="8fa3f-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="8fa3f-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




