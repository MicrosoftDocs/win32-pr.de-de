---
description: Hier finden Sie Informationen zum PageMediaSizePSHeight-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b1e7a30935c27fadb5d6ebb8dfb8f377e05a5e3
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549097"
---
# <a name="pagemediasizepsheight"></a><span data-ttu-id="85527-105">PageMediaSizePSHeight</span><span class="sxs-lookup"><span data-stu-id="85527-105">PageMediaSizePSHeight</span></span>

<span data-ttu-id="85527-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="85527-106">This topic is not current.</span></span> <span data-ttu-id="85527-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="85527-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="85527-108">Gibt die Höhe der Seite parallel zur Ausrichtungsrichtung des Feeds an (Referenz PostScript [Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="85527-108">Specifies the height of the page, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="85527-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="85527-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="85527-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="85527-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="85527-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="85527-111">Element Information</span></span>



| <span data-ttu-id="85527-112">Name</span><span class="sxs-lookup"><span data-stu-id="85527-112">Name</span></span> | <span data-ttu-id="85527-113">Wert</span><span class="sxs-lookup"><span data-stu-id="85527-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="85527-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="85527-114">Element Type</span></span> <br/>   | <span data-ttu-id="85527-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="85527-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="85527-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="85527-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="85527-117">Seite</span><span class="sxs-lookup"><span data-stu-id="85527-117">Page</span></span><br/>                                             |
| <span data-ttu-id="85527-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="85527-118">Notes</span></span> <br/>          | <span data-ttu-id="85527-119">Mit PageMediaSize-Element verknüpft, CustomPS-Option</span><span class="sxs-lookup"><span data-stu-id="85527-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="85527-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="85527-120">Structure Content</span></span>

<span data-ttu-id="85527-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="85527-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="85527-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="85527-122">Structure Properties</span></span>

<span data-ttu-id="85527-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="85527-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="85527-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="85527-124">Property</span></span>                | <span data-ttu-id="85527-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="85527-125">xsi:type</span></span>           | <span data-ttu-id="85527-126">Wert</span><span class="sxs-lookup"><span data-stu-id="85527-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="85527-127">DataType</span><span class="sxs-lookup"><span data-stu-id="85527-127">DataType</span></span><br/>     | <span data-ttu-id="85527-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="85527-128">string</span></span><br/>  | <span data-ttu-id="85527-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="85527-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="85527-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="85527-130">DefaultValue</span></span><br/> | <span data-ttu-id="85527-131">integer</span><span class="sxs-lookup"><span data-stu-id="85527-131">integer</span></span><br/> | <span data-ttu-id="85527-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="85527-132">undefined</span></span><br/>       |
| <span data-ttu-id="85527-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="85527-133">MaxValue</span></span><br/>     | <span data-ttu-id="85527-134">integer</span><span class="sxs-lookup"><span data-stu-id="85527-134">integer</span></span><br/> | <span data-ttu-id="85527-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="85527-135">undefined</span></span><br/>       |
| <span data-ttu-id="85527-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="85527-136">MinValue</span></span><br/>     | <span data-ttu-id="85527-137">integer</span><span class="sxs-lookup"><span data-stu-id="85527-137">integer</span></span><br/> | <span data-ttu-id="85527-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="85527-138">undefined</span></span><br/>       |
| <span data-ttu-id="85527-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="85527-139">Mandatory</span></span><br/>    | <span data-ttu-id="85527-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="85527-140">string</span></span><br/>  | <span data-ttu-id="85527-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="85527-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="85527-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="85527-142">Multiple</span></span><br/>     | <span data-ttu-id="85527-143">integer</span><span class="sxs-lookup"><span data-stu-id="85527-143">integer</span></span><br/> | <span data-ttu-id="85527-144">1</span><span class="sxs-lookup"><span data-stu-id="85527-144">1</span></span><br/>               |
| <span data-ttu-id="85527-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="85527-145">UnitType</span></span><br/>     | <span data-ttu-id="85527-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="85527-146">string</span></span><br/>  | <span data-ttu-id="85527-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="85527-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="85527-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85527-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85527-149">PostScript Spezifikation des Dateiformats der Druckerbeschreibung</span><span class="sxs-lookup"><span data-stu-id="85527-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="85527-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="85527-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




