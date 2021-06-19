---
description: Hier finden Sie Informationen zum PageMediaSizePSWidth-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: PageMediaSizePSWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe678107d2a183ee0f0bf6ce290dfe230fa8cc2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395645"
---
# <a name="pagemediasizepswidth"></a><span data-ttu-id="ad8f9-105">PageMediaSizePSWidth</span><span class="sxs-lookup"><span data-stu-id="ad8f9-105">PageMediaSizePSWidth</span></span>

<span data-ttu-id="ad8f9-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ad8f9-106">This topic is not current.</span></span> <span data-ttu-id="ad8f9-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="ad8f9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ad8f9-108">Gibt die Breite der Seite an, die an die Ausrichtungsrichtung des Feeds angibt (Referenz zur Spezifikation des Dateiformats der [PostScript-Druckerbeschreibung](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="ad8f9-108">Specifies the width of the page perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="ad8f9-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ad8f9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ad8f9-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ad8f9-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ad8f9-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ad8f9-111">Element Information</span></span>



| <span data-ttu-id="ad8f9-112">Name</span><span class="sxs-lookup"><span data-stu-id="ad8f9-112">Name</span></span> | <span data-ttu-id="ad8f9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ad8f9-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ad8f9-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ad8f9-114">Element Type</span></span> <br/>   | <span data-ttu-id="ad8f9-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ad8f9-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="ad8f9-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="ad8f9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ad8f9-117">Seite</span><span class="sxs-lookup"><span data-stu-id="ad8f9-117">Page</span></span><br/>                                             |
| <span data-ttu-id="ad8f9-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad8f9-118">Notes</span></span> <br/>          | <span data-ttu-id="ad8f9-119">Verknüpft mit PageMediaSize-Element, CustomPS-Option</span><span class="sxs-lookup"><span data-stu-id="ad8f9-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ad8f9-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ad8f9-120">Structure Content</span></span>

<span data-ttu-id="ad8f9-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="ad8f9-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="ad8f9-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad8f9-122">Structure Properties</span></span>

<span data-ttu-id="ad8f9-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ad8f9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ad8f9-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ad8f9-124">Property</span></span>                | <span data-ttu-id="ad8f9-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ad8f9-125">xsi:type</span></span>           | <span data-ttu-id="ad8f9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ad8f9-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ad8f9-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ad8f9-127">DataType</span></span><br/>     | <span data-ttu-id="ad8f9-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad8f9-128">string</span></span><br/>  | <span data-ttu-id="ad8f9-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ad8f9-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="ad8f9-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ad8f9-130">DefaultValue</span></span><br/> | <span data-ttu-id="ad8f9-131">integer</span><span class="sxs-lookup"><span data-stu-id="ad8f9-131">integer</span></span><br/> | <span data-ttu-id="ad8f9-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ad8f9-132">undefined</span></span><br/>       |
| <span data-ttu-id="ad8f9-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ad8f9-133">MaxValue</span></span><br/>     | <span data-ttu-id="ad8f9-134">integer</span><span class="sxs-lookup"><span data-stu-id="ad8f9-134">integer</span></span><br/> | <span data-ttu-id="ad8f9-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ad8f9-135">undefined</span></span><br/>       |
| <span data-ttu-id="ad8f9-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="ad8f9-136">MinValue</span></span><br/>     | <span data-ttu-id="ad8f9-137">integer</span><span class="sxs-lookup"><span data-stu-id="ad8f9-137">integer</span></span><br/> | <span data-ttu-id="ad8f9-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ad8f9-138">undefined</span></span><br/>       |
| <span data-ttu-id="ad8f9-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ad8f9-139">Mandatory</span></span><br/>    | <span data-ttu-id="ad8f9-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad8f9-140">string</span></span><br/>  | <span data-ttu-id="ad8f9-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="ad8f9-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ad8f9-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="ad8f9-142">Multiple</span></span><br/>     | <span data-ttu-id="ad8f9-143">integer</span><span class="sxs-lookup"><span data-stu-id="ad8f9-143">integer</span></span><br/> | <span data-ttu-id="ad8f9-144">1</span><span class="sxs-lookup"><span data-stu-id="ad8f9-144">1</span></span><br/>               |
| <span data-ttu-id="ad8f9-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="ad8f9-145">UnitType</span></span><br/>     | <span data-ttu-id="ad8f9-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad8f9-146">string</span></span><br/>  | <span data-ttu-id="ad8f9-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="ad8f9-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ad8f9-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad8f9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad8f9-149">Spezifikation des Dateiformats der PostScript-Druckerbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ad8f9-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="ad8f9-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="ad8f9-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




