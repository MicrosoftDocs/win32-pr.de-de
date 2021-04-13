---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: Pagemediasizemediasizewidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1f72e667f3de3bce86beb1c65c5fde4ebc8669
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351788"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="0c993-104">Pagemediasizemediasizewidth</span><span class="sxs-lookup"><span data-stu-id="0c993-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="0c993-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0c993-105">This topic is not current.</span></span> <span data-ttu-id="0c993-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0c993-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0c993-107">Gibt die mediasizewidth-Dimensions Richtung für die benutzerdefinierte mediasize-Option an.</span><span class="sxs-lookup"><span data-stu-id="0c993-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="0c993-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0c993-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0c993-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="0c993-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0c993-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0c993-110">Element Information</span></span>



| <span data-ttu-id="0c993-111">Name</span><span class="sxs-lookup"><span data-stu-id="0c993-111">Name</span></span>                       |                                                           |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="0c993-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0c993-112">Element Type</span></span> <br/>   | <span data-ttu-id="0c993-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0c993-113">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="0c993-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="0c993-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0c993-115">Seite</span><span class="sxs-lookup"><span data-stu-id="0c993-115">Page</span></span><br/>                                           |
| <span data-ttu-id="0c993-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c993-116">Notes</span></span> <br/>          | <span data-ttu-id="0c993-117">Verknüpft mit PageMediaSize-Element, benutzerdefinierte Option</span><span class="sxs-lookup"><span data-stu-id="0c993-117">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0c993-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="0c993-118">Structure Content</span></span>

<span data-ttu-id="0c993-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="0c993-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="0c993-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c993-120">Structure Properties</span></span>

<span data-ttu-id="0c993-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0c993-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0c993-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0c993-122">Property</span></span>                | <span data-ttu-id="0c993-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0c993-123">xsi:type</span></span>           | <span data-ttu-id="0c993-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0c993-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0c993-125">DataType</span><span class="sxs-lookup"><span data-stu-id="0c993-125">DataType</span></span><br/>     | <span data-ttu-id="0c993-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c993-126">string</span></span><br/>  | <span data-ttu-id="0c993-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0c993-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="0c993-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0c993-128">DefaultValue</span></span><br/> | <span data-ttu-id="0c993-129">integer</span><span class="sxs-lookup"><span data-stu-id="0c993-129">integer</span></span><br/> | <span data-ttu-id="0c993-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="0c993-130">undefined</span></span><br/>       |
| <span data-ttu-id="0c993-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0c993-131">MaxValue</span></span><br/>     | <span data-ttu-id="0c993-132">integer</span><span class="sxs-lookup"><span data-stu-id="0c993-132">integer</span></span><br/> | <span data-ttu-id="0c993-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="0c993-133">undefined</span></span><br/>       |
| <span data-ttu-id="0c993-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="0c993-134">MinValue</span></span><br/>     | <span data-ttu-id="0c993-135">integer</span><span class="sxs-lookup"><span data-stu-id="0c993-135">integer</span></span><br/> | <span data-ttu-id="0c993-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="0c993-136">undefined</span></span><br/>       |
| <span data-ttu-id="0c993-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="0c993-137">Mandatory</span></span><br/>    | <span data-ttu-id="0c993-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c993-138">string</span></span><br/>  | <span data-ttu-id="0c993-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="0c993-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0c993-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="0c993-140">Multiple</span></span><br/>     | <span data-ttu-id="0c993-141">integer</span><span class="sxs-lookup"><span data-stu-id="0c993-141">integer</span></span><br/> | <span data-ttu-id="0c993-142">1</span><span class="sxs-lookup"><span data-stu-id="0c993-142">1</span></span><br/>               |
| <span data-ttu-id="0c993-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="0c993-143">UnitType</span></span><br/>     | <span data-ttu-id="0c993-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c993-144">string</span></span><br/>  | <span data-ttu-id="0c993-145">Mikrometern</span><span class="sxs-lookup"><span data-stu-id="0c993-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="0c993-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0c993-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c993-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="0c993-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




