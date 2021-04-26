---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50df088fd25a69ee566e1406d3f1b833aa6131f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997567"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="44d21-104">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="44d21-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="44d21-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="44d21-105">This topic is not current.</span></span> <span data-ttu-id="44d21-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="44d21-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="44d21-107">Gibt die MediaSizeWidth-Richtung der Dimension für die Option Custom MediaSize an.</span><span class="sxs-lookup"><span data-stu-id="44d21-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="44d21-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="44d21-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="44d21-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="44d21-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="44d21-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="44d21-110">Element Information</span></span>



| <span data-ttu-id="44d21-111">Name</span><span class="sxs-lookup"><span data-stu-id="44d21-111">Name</span></span> | <span data-ttu-id="44d21-112">Wert</span><span class="sxs-lookup"><span data-stu-id="44d21-112">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="44d21-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="44d21-113">Element Type</span></span> <br/>   | <span data-ttu-id="44d21-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="44d21-114">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="44d21-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="44d21-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="44d21-116">Seite</span><span class="sxs-lookup"><span data-stu-id="44d21-116">Page</span></span><br/>                                           |
| <span data-ttu-id="44d21-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="44d21-117">Notes</span></span> <br/>          | <span data-ttu-id="44d21-118">Mit PageMediaSize-Element verknüpft, Option "Benutzerdefiniert"</span><span class="sxs-lookup"><span data-stu-id="44d21-118">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="44d21-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="44d21-119">Structure Content</span></span>

<span data-ttu-id="44d21-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="44d21-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="44d21-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="44d21-121">Structure Properties</span></span>

<span data-ttu-id="44d21-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="44d21-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="44d21-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44d21-123">Property</span></span>                | <span data-ttu-id="44d21-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="44d21-124">xsi:type</span></span>           | <span data-ttu-id="44d21-125">Wert</span><span class="sxs-lookup"><span data-stu-id="44d21-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="44d21-126">DataType</span><span class="sxs-lookup"><span data-stu-id="44d21-126">DataType</span></span><br/>     | <span data-ttu-id="44d21-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="44d21-127">string</span></span><br/>  | <span data-ttu-id="44d21-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="44d21-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="44d21-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="44d21-129">DefaultValue</span></span><br/> | <span data-ttu-id="44d21-130">integer</span><span class="sxs-lookup"><span data-stu-id="44d21-130">integer</span></span><br/> | <span data-ttu-id="44d21-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="44d21-131">undefined</span></span><br/>       |
| <span data-ttu-id="44d21-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="44d21-132">MaxValue</span></span><br/>     | <span data-ttu-id="44d21-133">integer</span><span class="sxs-lookup"><span data-stu-id="44d21-133">integer</span></span><br/> | <span data-ttu-id="44d21-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="44d21-134">undefined</span></span><br/>       |
| <span data-ttu-id="44d21-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="44d21-135">MinValue</span></span><br/>     | <span data-ttu-id="44d21-136">integer</span><span class="sxs-lookup"><span data-stu-id="44d21-136">integer</span></span><br/> | <span data-ttu-id="44d21-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="44d21-137">undefined</span></span><br/>       |
| <span data-ttu-id="44d21-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="44d21-138">Mandatory</span></span><br/>    | <span data-ttu-id="44d21-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="44d21-139">string</span></span><br/>  | <span data-ttu-id="44d21-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="44d21-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="44d21-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="44d21-141">Multiple</span></span><br/>     | <span data-ttu-id="44d21-142">integer</span><span class="sxs-lookup"><span data-stu-id="44d21-142">integer</span></span><br/> | <span data-ttu-id="44d21-143">1</span><span class="sxs-lookup"><span data-stu-id="44d21-143">1</span></span><br/>               |
| <span data-ttu-id="44d21-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="44d21-144">UnitType</span></span><br/>     | <span data-ttu-id="44d21-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="44d21-145">string</span></span><br/>  | <span data-ttu-id="44d21-146">Mikron</span><span class="sxs-lookup"><span data-stu-id="44d21-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="44d21-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44d21-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44d21-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="44d21-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




