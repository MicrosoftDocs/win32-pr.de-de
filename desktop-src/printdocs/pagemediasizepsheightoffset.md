---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2e1e0a75c5bb6ec95a611d304d575fcf91a13e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998057"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="5cf27-104">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="5cf27-104">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="5cf27-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5cf27-105">This topic is not current.</span></span> <span data-ttu-id="5cf27-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="5cf27-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5cf27-107">Gibt den Offset parallel zur Ausrichtungsrichtung des Feeds an (Referenz zur Spezifikation des [PostScript-Druckerbeschreibungsdateiformats).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="5cf27-107">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="5cf27-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5cf27-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5cf27-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="5cf27-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5cf27-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5cf27-110">Element Information</span></span>



| <span data-ttu-id="5cf27-111">Name</span><span class="sxs-lookup"><span data-stu-id="5cf27-111">Name</span></span> | <span data-ttu-id="5cf27-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5cf27-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="5cf27-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="5cf27-113">Element Type</span></span> <br/>   | <span data-ttu-id="5cf27-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5cf27-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="5cf27-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="5cf27-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5cf27-116">Seite</span><span class="sxs-lookup"><span data-stu-id="5cf27-116">Page</span></span><br/>                                             |
| <span data-ttu-id="5cf27-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5cf27-117">Notes</span></span> <br/>          | <span data-ttu-id="5cf27-118">Mit PageMediaSize-Element verknüpft, CustomPS-Option</span><span class="sxs-lookup"><span data-stu-id="5cf27-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5cf27-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="5cf27-119">Structure Content</span></span>

<span data-ttu-id="5cf27-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="5cf27-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5cf27-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="5cf27-121">Structure Properties</span></span>

<span data-ttu-id="5cf27-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5cf27-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5cf27-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5cf27-123">Property</span></span>                | <span data-ttu-id="5cf27-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5cf27-124">xsi:type</span></span>           | <span data-ttu-id="5cf27-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5cf27-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5cf27-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5cf27-126">DataType</span></span><br/>     | <span data-ttu-id="5cf27-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5cf27-127">string</span></span><br/>  | <span data-ttu-id="5cf27-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5cf27-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="5cf27-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5cf27-129">DefaultValue</span></span><br/> | <span data-ttu-id="5cf27-130">integer</span><span class="sxs-lookup"><span data-stu-id="5cf27-130">integer</span></span><br/> | <span data-ttu-id="5cf27-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="5cf27-131">undefined</span></span><br/>       |
| <span data-ttu-id="5cf27-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5cf27-132">MaxValue</span></span><br/>     | <span data-ttu-id="5cf27-133">integer</span><span class="sxs-lookup"><span data-stu-id="5cf27-133">integer</span></span><br/> | <span data-ttu-id="5cf27-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="5cf27-134">undefined</span></span><br/>       |
| <span data-ttu-id="5cf27-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="5cf27-135">MinValue</span></span><br/>     | <span data-ttu-id="5cf27-136">integer</span><span class="sxs-lookup"><span data-stu-id="5cf27-136">integer</span></span><br/> | <span data-ttu-id="5cf27-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="5cf27-137">undefined</span></span><br/>       |
| <span data-ttu-id="5cf27-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="5cf27-138">Mandatory</span></span><br/>    | <span data-ttu-id="5cf27-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5cf27-139">string</span></span><br/>  | <span data-ttu-id="5cf27-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="5cf27-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5cf27-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="5cf27-141">Multiple</span></span><br/>     | <span data-ttu-id="5cf27-142">integer</span><span class="sxs-lookup"><span data-stu-id="5cf27-142">integer</span></span><br/> | <span data-ttu-id="5cf27-143">1</span><span class="sxs-lookup"><span data-stu-id="5cf27-143">1</span></span><br/>               |
| <span data-ttu-id="5cf27-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="5cf27-144">UnitType</span></span><br/>     | <span data-ttu-id="5cf27-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5cf27-145">string</span></span><br/>  | <span data-ttu-id="5cf27-146">Mikron</span><span class="sxs-lookup"><span data-stu-id="5cf27-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5cf27-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5cf27-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cf27-148">Spezifikation des PostScript-Druckerbeschreibungsdateiformats</span><span class="sxs-lookup"><span data-stu-id="5cf27-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="5cf27-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="5cf27-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




