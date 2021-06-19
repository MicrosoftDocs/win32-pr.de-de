---
description: Abrufen von Informationen zum PageWatermarkTextColor-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7cb7b893ec9a2ecf774173cf2a9f2410549087
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396015"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="22a27-105">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="22a27-105">PageWatermarkTextColor</span></span>

<span data-ttu-id="22a27-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="22a27-106">This topic is not current.</span></span> <span data-ttu-id="22a27-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="22a27-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="22a27-108">Definiert die sRGB-Farbe für den Wasserzeichentext.</span><span class="sxs-lookup"><span data-stu-id="22a27-108">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="22a27-109">Das Format ist ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="22a27-109">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="22a27-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="22a27-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="22a27-111">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="22a27-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="22a27-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="22a27-112">Element Information</span></span>



| <span data-ttu-id="22a27-113">Name</span><span class="sxs-lookup"><span data-stu-id="22a27-113">Name</span></span> | <span data-ttu-id="22a27-114">Wert</span><span class="sxs-lookup"><span data-stu-id="22a27-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="22a27-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="22a27-115">Element Type</span></span> <br/>   | <span data-ttu-id="22a27-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="22a27-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="22a27-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="22a27-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="22a27-118">Seite</span><span class="sxs-lookup"><span data-stu-id="22a27-118">Page</span></span><br/>                            |
| <span data-ttu-id="22a27-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22a27-119">Notes</span></span> <br/>          | <span data-ttu-id="22a27-120">Verknüpft mit dem PageWatermark-Element</span><span class="sxs-lookup"><span data-stu-id="22a27-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="22a27-121">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="22a27-121">Structure Content</span></span>

<span data-ttu-id="22a27-122">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="22a27-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="22a27-123">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="22a27-123">Structure Properties</span></span>

<span data-ttu-id="22a27-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="22a27-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="22a27-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22a27-125">Property</span></span>                | <span data-ttu-id="22a27-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="22a27-126">xsi:type</span></span>           | <span data-ttu-id="22a27-127">Wert</span><span class="sxs-lookup"><span data-stu-id="22a27-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="22a27-128">DataType</span><span class="sxs-lookup"><span data-stu-id="22a27-128">DataType</span></span><br/>     | <span data-ttu-id="22a27-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22a27-129">string</span></span><br/>  | <span data-ttu-id="22a27-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="22a27-130">xs:string</span></span><br/>       |
| <span data-ttu-id="22a27-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="22a27-131">DefaultValue</span></span><br/> | <span data-ttu-id="22a27-132">integer</span><span class="sxs-lookup"><span data-stu-id="22a27-132">integer</span></span><br/> | <span data-ttu-id="22a27-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="22a27-133">undefined</span></span><br/>       |
| <span data-ttu-id="22a27-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="22a27-134">MaxValue</span></span><br/>     | <span data-ttu-id="22a27-135">integer</span><span class="sxs-lookup"><span data-stu-id="22a27-135">integer</span></span><br/> | <span data-ttu-id="22a27-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="22a27-136">undefined</span></span><br/>       |
| <span data-ttu-id="22a27-137">Minvalue</span><span class="sxs-lookup"><span data-stu-id="22a27-137">MinValue</span></span><br/>     | <span data-ttu-id="22a27-138">integer</span><span class="sxs-lookup"><span data-stu-id="22a27-138">integer</span></span><br/> | <span data-ttu-id="22a27-139">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="22a27-139">undefined</span></span><br/>       |
| <span data-ttu-id="22a27-140">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="22a27-140">Mandatory</span></span><br/>    | <span data-ttu-id="22a27-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22a27-141">string</span></span><br/>  | <span data-ttu-id="22a27-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="22a27-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="22a27-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="22a27-143">UnitType</span></span><br/>     | <span data-ttu-id="22a27-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22a27-144">string</span></span><br/>  | <span data-ttu-id="22a27-145">Srgb</span><span class="sxs-lookup"><span data-stu-id="22a27-145">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="22a27-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22a27-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22a27-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="22a27-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




