---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: Pagemediasizepsheighworffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e02129d5c8c20fceef01a9cd5cf40e5827374a7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106351855"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="28219-104">Pagemediasizepsheighworffset</span><span class="sxs-lookup"><span data-stu-id="28219-104">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="28219-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="28219-105">This topic is not current.</span></span> <span data-ttu-id="28219-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="28219-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="28219-107">Gibt den Offset an, und zwar parallel zur Richtung der Feed-Ausrichtung (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="28219-107">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="28219-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="28219-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="28219-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="28219-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="28219-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="28219-110">Element Information</span></span>



| <span data-ttu-id="28219-111">Name</span><span class="sxs-lookup"><span data-stu-id="28219-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="28219-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="28219-112">Element Type</span></span> <br/>   | <span data-ttu-id="28219-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="28219-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="28219-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="28219-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="28219-115">Seite</span><span class="sxs-lookup"><span data-stu-id="28219-115">Page</span></span><br/>                                             |
| <span data-ttu-id="28219-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="28219-116">Notes</span></span> <br/>          | <span data-ttu-id="28219-117">Verknüpft mit PageMediaSize-Element, customps-Option</span><span class="sxs-lookup"><span data-stu-id="28219-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="28219-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="28219-118">Structure Content</span></span>

<span data-ttu-id="28219-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="28219-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="28219-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28219-120">Structure Properties</span></span>

<span data-ttu-id="28219-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="28219-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="28219-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="28219-122">Property</span></span>                | <span data-ttu-id="28219-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="28219-123">xsi:type</span></span>           | <span data-ttu-id="28219-124">Wert</span><span class="sxs-lookup"><span data-stu-id="28219-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="28219-125">DataType</span><span class="sxs-lookup"><span data-stu-id="28219-125">DataType</span></span><br/>     | <span data-ttu-id="28219-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="28219-126">string</span></span><br/>  | <span data-ttu-id="28219-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="28219-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="28219-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="28219-128">DefaultValue</span></span><br/> | <span data-ttu-id="28219-129">integer</span><span class="sxs-lookup"><span data-stu-id="28219-129">integer</span></span><br/> | <span data-ttu-id="28219-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="28219-130">undefined</span></span><br/>       |
| <span data-ttu-id="28219-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="28219-131">MaxValue</span></span><br/>     | <span data-ttu-id="28219-132">integer</span><span class="sxs-lookup"><span data-stu-id="28219-132">integer</span></span><br/> | <span data-ttu-id="28219-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="28219-133">undefined</span></span><br/>       |
| <span data-ttu-id="28219-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="28219-134">MinValue</span></span><br/>     | <span data-ttu-id="28219-135">integer</span><span class="sxs-lookup"><span data-stu-id="28219-135">integer</span></span><br/> | <span data-ttu-id="28219-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="28219-136">undefined</span></span><br/>       |
| <span data-ttu-id="28219-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="28219-137">Mandatory</span></span><br/>    | <span data-ttu-id="28219-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="28219-138">string</span></span><br/>  | <span data-ttu-id="28219-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="28219-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="28219-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="28219-140">Multiple</span></span><br/>     | <span data-ttu-id="28219-141">integer</span><span class="sxs-lookup"><span data-stu-id="28219-141">integer</span></span><br/> | <span data-ttu-id="28219-142">1</span><span class="sxs-lookup"><span data-stu-id="28219-142">1</span></span><br/>               |
| <span data-ttu-id="28219-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="28219-143">UnitType</span></span><br/>     | <span data-ttu-id="28219-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="28219-144">string</span></span><br/>  | <span data-ttu-id="28219-145">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="28219-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="28219-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28219-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28219-147">Datei Format Spezifikation für PostScript-Drucker Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28219-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="28219-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="28219-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




