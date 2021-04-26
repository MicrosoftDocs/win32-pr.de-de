---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: PageMediaSizePSWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4399b75f047c2705983c893075995800396120
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997547"
---
# <a name="pagemediasizepswidth"></a><span data-ttu-id="b6bd7-104">PageMediaSizePSWidth</span><span class="sxs-lookup"><span data-stu-id="b6bd7-104">PageMediaSizePSWidth</span></span>

<span data-ttu-id="b6bd7-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-105">This topic is not current.</span></span> <span data-ttu-id="b6bd7-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="b6bd7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b6bd7-107">Gibt die Breite der Seite an, die der Ausrichtungsrichtung des Feeds entspricht (Referenz [zur Spezifikation des Dateiformats der PostScript-Druckerbeschreibung](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="b6bd7-107">Specifies the width of the page perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="b6bd7-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b6bd7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b6bd7-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b6bd7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b6bd7-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b6bd7-110">Element Information</span></span>



| <span data-ttu-id="b6bd7-111">Name</span><span class="sxs-lookup"><span data-stu-id="b6bd7-111">Name</span></span> | <span data-ttu-id="b6bd7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b6bd7-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b6bd7-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="b6bd7-113">Element Type</span></span> <br/>   | <span data-ttu-id="b6bd7-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b6bd7-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="b6bd7-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="b6bd7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b6bd7-116">Seite</span><span class="sxs-lookup"><span data-stu-id="b6bd7-116">Page</span></span><br/>                                             |
| <span data-ttu-id="b6bd7-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b6bd7-117">Notes</span></span> <br/>          | <span data-ttu-id="b6bd7-118">Mit PageMediaSize-Element verknüpft, CustomPS-Option</span><span class="sxs-lookup"><span data-stu-id="b6bd7-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b6bd7-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b6bd7-119">Structure Content</span></span>

<span data-ttu-id="b6bd7-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="b6bd7-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b6bd7-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6bd7-121">Structure Properties</span></span>

<span data-ttu-id="b6bd7-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b6bd7-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b6bd7-123">Property</span></span>                | <span data-ttu-id="b6bd7-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b6bd7-124">xsi:type</span></span>           | <span data-ttu-id="b6bd7-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b6bd7-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b6bd7-126">DataType</span><span class="sxs-lookup"><span data-stu-id="b6bd7-126">DataType</span></span><br/>     | <span data-ttu-id="b6bd7-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b6bd7-127">string</span></span><br/>  | <span data-ttu-id="b6bd7-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b6bd7-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="b6bd7-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b6bd7-129">DefaultValue</span></span><br/> | <span data-ttu-id="b6bd7-130">integer</span><span class="sxs-lookup"><span data-stu-id="b6bd7-130">integer</span></span><br/> | <span data-ttu-id="b6bd7-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b6bd7-131">undefined</span></span><br/>       |
| <span data-ttu-id="b6bd7-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b6bd7-132">MaxValue</span></span><br/>     | <span data-ttu-id="b6bd7-133">integer</span><span class="sxs-lookup"><span data-stu-id="b6bd7-133">integer</span></span><br/> | <span data-ttu-id="b6bd7-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b6bd7-134">undefined</span></span><br/>       |
| <span data-ttu-id="b6bd7-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="b6bd7-135">MinValue</span></span><br/>     | <span data-ttu-id="b6bd7-136">integer</span><span class="sxs-lookup"><span data-stu-id="b6bd7-136">integer</span></span><br/> | <span data-ttu-id="b6bd7-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b6bd7-137">undefined</span></span><br/>       |
| <span data-ttu-id="b6bd7-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-138">Mandatory</span></span><br/>    | <span data-ttu-id="b6bd7-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b6bd7-139">string</span></span><br/>  | <span data-ttu-id="b6bd7-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="b6bd7-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b6bd7-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="b6bd7-141">Multiple</span></span><br/>     | <span data-ttu-id="b6bd7-142">integer</span><span class="sxs-lookup"><span data-stu-id="b6bd7-142">integer</span></span><br/> | <span data-ttu-id="b6bd7-143">1</span><span class="sxs-lookup"><span data-stu-id="b6bd7-143">1</span></span><br/>               |
| <span data-ttu-id="b6bd7-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="b6bd7-144">UnitType</span></span><br/>     | <span data-ttu-id="b6bd7-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b6bd7-145">string</span></span><br/>  | <span data-ttu-id="b6bd7-146">Mikron</span><span class="sxs-lookup"><span data-stu-id="b6bd7-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b6bd7-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6bd7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6bd7-148">Spezifikation des Dateiformats der PostScript-Druckerbeschreibung</span><span class="sxs-lookup"><span data-stu-id="b6bd7-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="b6bd7-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="b6bd7-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




