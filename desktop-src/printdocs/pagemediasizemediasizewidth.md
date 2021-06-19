---
description: Hier finden Sie Informationen zum PageMediaSizeMediaSizeWidth-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f84e36f689d4b3c5ca060020327d78b12f7d6
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395835"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="0700f-105">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="0700f-105">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="0700f-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0700f-106">This topic is not current.</span></span> <span data-ttu-id="0700f-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="0700f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0700f-108">Gibt die MediaSizeWidth-Richtung der Dimension für die Option Custom MediaSize an.</span><span class="sxs-lookup"><span data-stu-id="0700f-108">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="0700f-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0700f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0700f-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="0700f-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0700f-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0700f-111">Element Information</span></span>



| <span data-ttu-id="0700f-112">Name</span><span class="sxs-lookup"><span data-stu-id="0700f-112">Name</span></span> | <span data-ttu-id="0700f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0700f-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="0700f-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0700f-114">Element Type</span></span> <br/>   | <span data-ttu-id="0700f-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0700f-115">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="0700f-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="0700f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0700f-117">Seite</span><span class="sxs-lookup"><span data-stu-id="0700f-117">Page</span></span><br/>                                           |
| <span data-ttu-id="0700f-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0700f-118">Notes</span></span> <br/>          | <span data-ttu-id="0700f-119">Mit PageMediaSize-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="0700f-119">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0700f-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="0700f-120">Structure Content</span></span>

<span data-ttu-id="0700f-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="0700f-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0700f-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="0700f-122">Structure Properties</span></span>

<span data-ttu-id="0700f-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0700f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0700f-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0700f-124">Property</span></span>                | <span data-ttu-id="0700f-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0700f-125">xsi:type</span></span>           | <span data-ttu-id="0700f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0700f-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0700f-127">DataType</span><span class="sxs-lookup"><span data-stu-id="0700f-127">DataType</span></span><br/>     | <span data-ttu-id="0700f-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0700f-128">string</span></span><br/>  | <span data-ttu-id="0700f-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0700f-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="0700f-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0700f-130">DefaultValue</span></span><br/> | <span data-ttu-id="0700f-131">integer</span><span class="sxs-lookup"><span data-stu-id="0700f-131">integer</span></span><br/> | <span data-ttu-id="0700f-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="0700f-132">undefined</span></span><br/>       |
| <span data-ttu-id="0700f-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0700f-133">MaxValue</span></span><br/>     | <span data-ttu-id="0700f-134">integer</span><span class="sxs-lookup"><span data-stu-id="0700f-134">integer</span></span><br/> | <span data-ttu-id="0700f-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="0700f-135">undefined</span></span><br/>       |
| <span data-ttu-id="0700f-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="0700f-136">MinValue</span></span><br/>     | <span data-ttu-id="0700f-137">integer</span><span class="sxs-lookup"><span data-stu-id="0700f-137">integer</span></span><br/> | <span data-ttu-id="0700f-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="0700f-138">undefined</span></span><br/>       |
| <span data-ttu-id="0700f-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="0700f-139">Mandatory</span></span><br/>    | <span data-ttu-id="0700f-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0700f-140">string</span></span><br/>  | <span data-ttu-id="0700f-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="0700f-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0700f-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="0700f-142">Multiple</span></span><br/>     | <span data-ttu-id="0700f-143">integer</span><span class="sxs-lookup"><span data-stu-id="0700f-143">integer</span></span><br/> | <span data-ttu-id="0700f-144">1</span><span class="sxs-lookup"><span data-stu-id="0700f-144">1</span></span><br/>               |
| <span data-ttu-id="0700f-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="0700f-145">UnitType</span></span><br/>     | <span data-ttu-id="0700f-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0700f-146">string</span></span><br/>  | <span data-ttu-id="0700f-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="0700f-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="0700f-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0700f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0700f-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="0700f-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




