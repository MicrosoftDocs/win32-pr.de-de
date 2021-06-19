---
description: Hier finden Sie Informationen zum PageMediaSizePSOrientation-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1b3aff1099199a98d6c8be899824dd1a1f17c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395725"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="98317-105">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="98317-105">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="98317-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="98317-106">This topic is not current.</span></span> <span data-ttu-id="98317-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="98317-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="98317-108">Gibt die Ausrichtung relativ zur Ausrichtungsrichtung des Feeds an (Referenz [zur Spezifikation des Dateiformats der PostScript-Druckerbeschreibung](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="98317-108">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="98317-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="98317-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="98317-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="98317-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="98317-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="98317-111">Element Information</span></span>



| <span data-ttu-id="98317-112">Name</span><span class="sxs-lookup"><span data-stu-id="98317-112">Name</span></span> | <span data-ttu-id="98317-113">Wert</span><span class="sxs-lookup"><span data-stu-id="98317-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="98317-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="98317-114">Element Type</span></span> <br/>   | <span data-ttu-id="98317-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="98317-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="98317-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="98317-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="98317-117">Seite</span><span class="sxs-lookup"><span data-stu-id="98317-117">Page</span></span><br/>                                             |
| <span data-ttu-id="98317-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98317-118">Notes</span></span> <br/>          | <span data-ttu-id="98317-119">Verknüpft mit PageMediaSize-Element, CustomPS-Option</span><span class="sxs-lookup"><span data-stu-id="98317-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="98317-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="98317-120">Structure Content</span></span>

<span data-ttu-id="98317-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="98317-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="98317-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="98317-122">Structure Properties</span></span>

<span data-ttu-id="98317-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="98317-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="98317-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="98317-124">Property</span></span>                | <span data-ttu-id="98317-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="98317-125">xsi:type</span></span>           | <span data-ttu-id="98317-126">Wert</span><span class="sxs-lookup"><span data-stu-id="98317-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="98317-127">DataType</span><span class="sxs-lookup"><span data-stu-id="98317-127">DataType</span></span><br/>     | <span data-ttu-id="98317-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="98317-128">string</span></span><br/>  | <span data-ttu-id="98317-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="98317-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="98317-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="98317-130">DefaultValue</span></span><br/> | <span data-ttu-id="98317-131">integer</span><span class="sxs-lookup"><span data-stu-id="98317-131">integer</span></span><br/> | <span data-ttu-id="98317-132">0</span><span class="sxs-lookup"><span data-stu-id="98317-132">0</span></span><br/>                 |
| <span data-ttu-id="98317-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="98317-133">MaxValue</span></span><br/>     | <span data-ttu-id="98317-134">integer</span><span class="sxs-lookup"><span data-stu-id="98317-134">integer</span></span><br/> | <span data-ttu-id="98317-135">3</span><span class="sxs-lookup"><span data-stu-id="98317-135">3</span></span><br/>                 |
| <span data-ttu-id="98317-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="98317-136">MinValue</span></span><br/>     | <span data-ttu-id="98317-137">integer</span><span class="sxs-lookup"><span data-stu-id="98317-137">integer</span></span><br/> | <span data-ttu-id="98317-138">0</span><span class="sxs-lookup"><span data-stu-id="98317-138">0</span></span><br/>                 |
| <span data-ttu-id="98317-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="98317-139">Mandatory</span></span><br/>    | <span data-ttu-id="98317-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="98317-140">string</span></span><br/>  | <span data-ttu-id="98317-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="98317-141">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="98317-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="98317-142">Multiple</span></span><br/>     | <span data-ttu-id="98317-143">integer</span><span class="sxs-lookup"><span data-stu-id="98317-143">integer</span></span><br/> | <span data-ttu-id="98317-144">1</span><span class="sxs-lookup"><span data-stu-id="98317-144">1</span></span><br/>                 |
| <span data-ttu-id="98317-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="98317-145">UnitType</span></span><br/>     | <span data-ttu-id="98317-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="98317-146">string</span></span><br/>  | <span data-ttu-id="98317-147">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="98317-147">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="98317-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98317-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98317-149">Spezifikation des Dateiformats der PostScript-Druckerbeschreibung</span><span class="sxs-lookup"><span data-stu-id="98317-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="98317-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="98317-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




