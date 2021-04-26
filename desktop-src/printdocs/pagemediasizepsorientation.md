---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16a9a2e59ebffb41ad7c9a9c16eaf41497ade62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997557"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="bf222-104">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="bf222-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="bf222-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="bf222-105">This topic is not current.</span></span> <span data-ttu-id="bf222-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="bf222-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bf222-107">Gibt die Ausrichtung relativ zur Richtung der Feedausrichtung an (Referenz zur Spezifikation des [PostScript-Druckerbeschreibungsdateiformats).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="bf222-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="bf222-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="bf222-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bf222-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="bf222-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="bf222-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="bf222-110">Element Information</span></span>



| <span data-ttu-id="bf222-111">Name</span><span class="sxs-lookup"><span data-stu-id="bf222-111">Name</span></span> | <span data-ttu-id="bf222-112">Wert</span><span class="sxs-lookup"><span data-stu-id="bf222-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bf222-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="bf222-113">Element Type</span></span> <br/>   | <span data-ttu-id="bf222-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="bf222-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="bf222-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="bf222-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bf222-116">Seite</span><span class="sxs-lookup"><span data-stu-id="bf222-116">Page</span></span><br/>                                             |
| <span data-ttu-id="bf222-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bf222-117">Notes</span></span> <br/>          | <span data-ttu-id="bf222-118">Mit PageMediaSize-Element verknüpft, CustomPS-Option</span><span class="sxs-lookup"><span data-stu-id="bf222-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="bf222-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="bf222-119">Structure Content</span></span>

<span data-ttu-id="bf222-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="bf222-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="bf222-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf222-121">Structure Properties</span></span>

<span data-ttu-id="bf222-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bf222-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bf222-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf222-123">Property</span></span>                | <span data-ttu-id="bf222-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="bf222-124">xsi:type</span></span>           | <span data-ttu-id="bf222-125">Wert</span><span class="sxs-lookup"><span data-stu-id="bf222-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="bf222-126">DataType</span><span class="sxs-lookup"><span data-stu-id="bf222-126">DataType</span></span><br/>     | <span data-ttu-id="bf222-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf222-127">string</span></span><br/>  | <span data-ttu-id="bf222-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="bf222-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="bf222-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="bf222-129">DefaultValue</span></span><br/> | <span data-ttu-id="bf222-130">integer</span><span class="sxs-lookup"><span data-stu-id="bf222-130">integer</span></span><br/> | <span data-ttu-id="bf222-131">0</span><span class="sxs-lookup"><span data-stu-id="bf222-131">0</span></span><br/>                 |
| <span data-ttu-id="bf222-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="bf222-132">MaxValue</span></span><br/>     | <span data-ttu-id="bf222-133">integer</span><span class="sxs-lookup"><span data-stu-id="bf222-133">integer</span></span><br/> | <span data-ttu-id="bf222-134">3</span><span class="sxs-lookup"><span data-stu-id="bf222-134">3</span></span><br/>                 |
| <span data-ttu-id="bf222-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="bf222-135">MinValue</span></span><br/>     | <span data-ttu-id="bf222-136">integer</span><span class="sxs-lookup"><span data-stu-id="bf222-136">integer</span></span><br/> | <span data-ttu-id="bf222-137">0</span><span class="sxs-lookup"><span data-stu-id="bf222-137">0</span></span><br/>                 |
| <span data-ttu-id="bf222-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="bf222-138">Mandatory</span></span><br/>    | <span data-ttu-id="bf222-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf222-139">string</span></span><br/>  | <span data-ttu-id="bf222-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="bf222-140">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="bf222-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="bf222-141">Multiple</span></span><br/>     | <span data-ttu-id="bf222-142">integer</span><span class="sxs-lookup"><span data-stu-id="bf222-142">integer</span></span><br/> | <span data-ttu-id="bf222-143">1</span><span class="sxs-lookup"><span data-stu-id="bf222-143">1</span></span><br/>                 |
| <span data-ttu-id="bf222-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="bf222-144">UnitType</span></span><br/>     | <span data-ttu-id="bf222-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf222-145">string</span></span><br/>  | <span data-ttu-id="bf222-146">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="bf222-146">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="bf222-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf222-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf222-148">Spezifikation des PostScript-Druckerbeschreibungsdateiformats</span><span class="sxs-lookup"><span data-stu-id="bf222-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="bf222-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="bf222-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




