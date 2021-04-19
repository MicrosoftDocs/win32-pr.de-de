---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: Pagemediasizepsheight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb576ce7d623f4d036db1332b0339e6cef518d3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106364299"
---
# <a name="pagemediasizepsheight"></a><span data-ttu-id="3f30d-104">Pagemediasizepsheight</span><span class="sxs-lookup"><span data-stu-id="3f30d-104">PageMediaSizePSHeight</span></span>

<span data-ttu-id="3f30d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3f30d-105">This topic is not current.</span></span> <span data-ttu-id="3f30d-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3f30d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3f30d-107">Gibt die Höhe der Seite an, und zwar parallel zur Richtung der Feed-Ausrichtung (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="3f30d-107">Specifies the height of the page, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="3f30d-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3f30d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3f30d-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="3f30d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3f30d-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3f30d-110">Element Information</span></span>



| <span data-ttu-id="3f30d-111">Name</span><span class="sxs-lookup"><span data-stu-id="3f30d-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="3f30d-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="3f30d-112">Element Type</span></span> <br/>   | <span data-ttu-id="3f30d-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3f30d-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="3f30d-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="3f30d-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3f30d-115">Seite</span><span class="sxs-lookup"><span data-stu-id="3f30d-115">Page</span></span><br/>                                             |
| <span data-ttu-id="3f30d-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f30d-116">Notes</span></span> <br/>          | <span data-ttu-id="3f30d-117">Verknüpft mit PageMediaSize-Element, customps-Option</span><span class="sxs-lookup"><span data-stu-id="3f30d-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3f30d-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="3f30d-118">Structure Content</span></span>

<span data-ttu-id="3f30d-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="3f30d-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3f30d-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f30d-120">Structure Properties</span></span>

<span data-ttu-id="3f30d-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3f30d-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3f30d-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3f30d-122">Property</span></span>                | <span data-ttu-id="3f30d-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3f30d-123">xsi:type</span></span>           | <span data-ttu-id="3f30d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3f30d-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3f30d-125">DataType</span><span class="sxs-lookup"><span data-stu-id="3f30d-125">DataType</span></span><br/>     | <span data-ttu-id="3f30d-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3f30d-126">string</span></span><br/>  | <span data-ttu-id="3f30d-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3f30d-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="3f30d-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3f30d-128">DefaultValue</span></span><br/> | <span data-ttu-id="3f30d-129">integer</span><span class="sxs-lookup"><span data-stu-id="3f30d-129">integer</span></span><br/> | <span data-ttu-id="3f30d-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="3f30d-130">undefined</span></span><br/>       |
| <span data-ttu-id="3f30d-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="3f30d-131">MaxValue</span></span><br/>     | <span data-ttu-id="3f30d-132">integer</span><span class="sxs-lookup"><span data-stu-id="3f30d-132">integer</span></span><br/> | <span data-ttu-id="3f30d-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="3f30d-133">undefined</span></span><br/>       |
| <span data-ttu-id="3f30d-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="3f30d-134">MinValue</span></span><br/>     | <span data-ttu-id="3f30d-135">integer</span><span class="sxs-lookup"><span data-stu-id="3f30d-135">integer</span></span><br/> | <span data-ttu-id="3f30d-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="3f30d-136">undefined</span></span><br/>       |
| <span data-ttu-id="3f30d-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="3f30d-137">Mandatory</span></span><br/>    | <span data-ttu-id="3f30d-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3f30d-138">string</span></span><br/>  | <span data-ttu-id="3f30d-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="3f30d-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3f30d-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="3f30d-140">Multiple</span></span><br/>     | <span data-ttu-id="3f30d-141">integer</span><span class="sxs-lookup"><span data-stu-id="3f30d-141">integer</span></span><br/> | <span data-ttu-id="3f30d-142">1</span><span class="sxs-lookup"><span data-stu-id="3f30d-142">1</span></span><br/>               |
| <span data-ttu-id="3f30d-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="3f30d-143">UnitType</span></span><br/>     | <span data-ttu-id="3f30d-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3f30d-144">string</span></span><br/>  | <span data-ttu-id="3f30d-145">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="3f30d-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="3f30d-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f30d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f30d-147">Datei Format Spezifikation für PostScript-Drucker Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f30d-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="3f30d-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="3f30d-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




