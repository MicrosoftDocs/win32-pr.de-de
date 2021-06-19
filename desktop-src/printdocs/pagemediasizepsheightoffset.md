---
description: Hier finden Sie Informationen zum PageMediaSizePSHeightOffset-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2c0e3802a6c461fe2f9eec68b28677c254be9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395735"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="dff1c-105">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="dff1c-105">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="dff1c-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="dff1c-106">This topic is not current.</span></span> <span data-ttu-id="dff1c-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="dff1c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dff1c-108">Gibt den Offset parallel zur Ausrichtungsrichtung des Feeds an (Referenz [zur Spezifikation des PostScript-Druckerbeschreibungsdateiformats](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="dff1c-108">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="dff1c-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="dff1c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dff1c-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="dff1c-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dff1c-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="dff1c-111">Element Information</span></span>



| <span data-ttu-id="dff1c-112">Name</span><span class="sxs-lookup"><span data-stu-id="dff1c-112">Name</span></span> | <span data-ttu-id="dff1c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="dff1c-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="dff1c-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="dff1c-114">Element Type</span></span> <br/>   | <span data-ttu-id="dff1c-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dff1c-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="dff1c-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="dff1c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dff1c-117">Seite</span><span class="sxs-lookup"><span data-stu-id="dff1c-117">Page</span></span><br/>                                             |
| <span data-ttu-id="dff1c-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dff1c-118">Notes</span></span> <br/>          | <span data-ttu-id="dff1c-119">Verknüpft mit PageMediaSize-Element, CustomPS-Option</span><span class="sxs-lookup"><span data-stu-id="dff1c-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dff1c-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="dff1c-120">Structure Content</span></span>

<span data-ttu-id="dff1c-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="dff1c-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeightOffset">
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

## <a name="structure-properties"></a><span data-ttu-id="dff1c-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="dff1c-122">Structure Properties</span></span>

<span data-ttu-id="dff1c-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="dff1c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dff1c-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dff1c-124">Property</span></span>                | <span data-ttu-id="dff1c-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dff1c-125">xsi:type</span></span>           | <span data-ttu-id="dff1c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="dff1c-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dff1c-127">DataType</span><span class="sxs-lookup"><span data-stu-id="dff1c-127">DataType</span></span><br/>     | <span data-ttu-id="dff1c-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="dff1c-128">string</span></span><br/>  | <span data-ttu-id="dff1c-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dff1c-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="dff1c-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dff1c-130">DefaultValue</span></span><br/> | <span data-ttu-id="dff1c-131">integer</span><span class="sxs-lookup"><span data-stu-id="dff1c-131">integer</span></span><br/> | <span data-ttu-id="dff1c-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="dff1c-132">undefined</span></span><br/>       |
| <span data-ttu-id="dff1c-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dff1c-133">MaxValue</span></span><br/>     | <span data-ttu-id="dff1c-134">integer</span><span class="sxs-lookup"><span data-stu-id="dff1c-134">integer</span></span><br/> | <span data-ttu-id="dff1c-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="dff1c-135">undefined</span></span><br/>       |
| <span data-ttu-id="dff1c-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="dff1c-136">MinValue</span></span><br/>     | <span data-ttu-id="dff1c-137">integer</span><span class="sxs-lookup"><span data-stu-id="dff1c-137">integer</span></span><br/> | <span data-ttu-id="dff1c-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="dff1c-138">undefined</span></span><br/>       |
| <span data-ttu-id="dff1c-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="dff1c-139">Mandatory</span></span><br/>    | <span data-ttu-id="dff1c-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="dff1c-140">string</span></span><br/>  | <span data-ttu-id="dff1c-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="dff1c-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dff1c-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="dff1c-142">Multiple</span></span><br/>     | <span data-ttu-id="dff1c-143">integer</span><span class="sxs-lookup"><span data-stu-id="dff1c-143">integer</span></span><br/> | <span data-ttu-id="dff1c-144">1</span><span class="sxs-lookup"><span data-stu-id="dff1c-144">1</span></span><br/>               |
| <span data-ttu-id="dff1c-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="dff1c-145">UnitType</span></span><br/>     | <span data-ttu-id="dff1c-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="dff1c-146">string</span></span><br/>  | <span data-ttu-id="dff1c-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="dff1c-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="dff1c-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dff1c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dff1c-149">Spezifikation des Dateiformats der PostScript-Druckerbeschreibung</span><span class="sxs-lookup"><span data-stu-id="dff1c-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="dff1c-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="dff1c-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




