---
description: Erfahren Sie mehr über den PageDestinationColorProfileEmbedded-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: PageDestinationColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05865636b6554873844a99b523f8c21fe2bfc1c7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549208"
---
# <a name="pagedestinationcolorprofileembedded"></a><span data-ttu-id="27f9d-105">PageDestinationColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="27f9d-105">PageDestinationColorProfileEmbedded</span></span>

<span data-ttu-id="27f9d-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="27f9d-106">This topic is not current.</span></span> <span data-ttu-id="27f9d-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="27f9d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="27f9d-108">Gibt das eingebettete Zielfarbprofil an.</span><span class="sxs-lookup"><span data-stu-id="27f9d-108">Specifies the embedded destination color profile.</span></span>

-   [<span data-ttu-id="27f9d-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="27f9d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="27f9d-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="27f9d-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="27f9d-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="27f9d-111">Element Information</span></span>



| <span data-ttu-id="27f9d-112">Name</span><span class="sxs-lookup"><span data-stu-id="27f9d-112">Name</span></span> | <span data-ttu-id="27f9d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="27f9d-113">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="27f9d-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="27f9d-114">Element Type</span></span> <br/>   | <span data-ttu-id="27f9d-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="27f9d-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="27f9d-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="27f9d-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="27f9d-117">Seite</span><span class="sxs-lookup"><span data-stu-id="27f9d-117">Page</span></span><br/>                                          |
| <span data-ttu-id="27f9d-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="27f9d-118">Notes</span></span> <br/>          | <span data-ttu-id="27f9d-119">Mit PageDestinationColorProfile-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="27f9d-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="27f9d-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="27f9d-120">Structure Content</span></span>

<span data-ttu-id="27f9d-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="27f9d-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileEmbedded">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="27f9d-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="27f9d-122">Structure Properties</span></span>

<span data-ttu-id="27f9d-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="27f9d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="27f9d-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="27f9d-124">Property</span></span>                | <span data-ttu-id="27f9d-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="27f9d-125">xsi:type</span></span>           | <span data-ttu-id="27f9d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="27f9d-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="27f9d-127">DataType</span><span class="sxs-lookup"><span data-stu-id="27f9d-127">DataType</span></span><br/>     | <span data-ttu-id="27f9d-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="27f9d-128">string</span></span><br/>  | <span data-ttu-id="27f9d-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="27f9d-129">xs:string</span></span><br/>       |
| <span data-ttu-id="27f9d-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="27f9d-130">DefaultValue</span></span><br/> | <span data-ttu-id="27f9d-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="27f9d-131">string</span></span><br/>  | <span data-ttu-id="27f9d-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="27f9d-132">undefined</span></span><br/>       |
| <span data-ttu-id="27f9d-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="27f9d-133">MaxLength</span></span><br/>    | <span data-ttu-id="27f9d-134">integer</span><span class="sxs-lookup"><span data-stu-id="27f9d-134">integer</span></span><br/> | <span data-ttu-id="27f9d-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="27f9d-135">undefined</span></span><br/>       |
| <span data-ttu-id="27f9d-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="27f9d-136">MinLength</span></span><br/>    | <span data-ttu-id="27f9d-137">integer</span><span class="sxs-lookup"><span data-stu-id="27f9d-137">integer</span></span><br/> | <span data-ttu-id="27f9d-138">1</span><span class="sxs-lookup"><span data-stu-id="27f9d-138">1</span></span><br/>               |
| <span data-ttu-id="27f9d-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="27f9d-139">Mandatory</span></span><br/>    | <span data-ttu-id="27f9d-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="27f9d-140">string</span></span><br/>  | <span data-ttu-id="27f9d-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="27f9d-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="27f9d-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="27f9d-142">UnitType</span></span><br/>     | <span data-ttu-id="27f9d-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="27f9d-143">string</span></span><br/>  | <span data-ttu-id="27f9d-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="27f9d-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="27f9d-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27f9d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27f9d-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="27f9d-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




