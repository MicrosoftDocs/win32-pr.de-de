---
description: Erfahren Sie mehr über den PageSourceColorProfileEmbedded-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0633fa061601c1d575f174ab5572582efdf9a89e
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395635"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="6ecce-105">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="6ecce-105">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="6ecce-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="6ecce-106">This topic is not current.</span></span> <span data-ttu-id="6ecce-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="6ecce-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6ecce-108">Gibt das eingebettete Quellfarbprofil an.</span><span class="sxs-lookup"><span data-stu-id="6ecce-108">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="6ecce-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6ecce-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6ecce-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="6ecce-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6ecce-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6ecce-111">Element Information</span></span>



| <span data-ttu-id="6ecce-112">Name</span><span class="sxs-lookup"><span data-stu-id="6ecce-112">Name</span></span> | <span data-ttu-id="6ecce-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6ecce-113">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="6ecce-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="6ecce-114">Element Type</span></span> <br/>   | <span data-ttu-id="6ecce-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6ecce-115">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="6ecce-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="6ecce-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6ecce-117">Seite</span><span class="sxs-lookup"><span data-stu-id="6ecce-117">Page</span></span><br/>                                     |
| <span data-ttu-id="6ecce-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ecce-118">Notes</span></span> <br/>          | <span data-ttu-id="6ecce-119">Verknüpft mit dem PageSourceColorProfile-Element</span><span class="sxs-lookup"><span data-stu-id="6ecce-119">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6ecce-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="6ecce-120">Structure Content</span></span>

<span data-ttu-id="6ecce-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="6ecce-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="6ecce-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ecce-122">Structure Properties</span></span>

<span data-ttu-id="6ecce-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ecce-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6ecce-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6ecce-124">Property</span></span>                | <span data-ttu-id="6ecce-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6ecce-125">xsi:type</span></span>           | <span data-ttu-id="6ecce-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6ecce-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6ecce-127">DataType</span><span class="sxs-lookup"><span data-stu-id="6ecce-127">DataType</span></span><br/>     | <span data-ttu-id="6ecce-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6ecce-128">string</span></span><br/>  | <span data-ttu-id="6ecce-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="6ecce-129">xs:string</span></span><br/>       |
| <span data-ttu-id="6ecce-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6ecce-130">DefaultValue</span></span><br/> | <span data-ttu-id="6ecce-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6ecce-131">string</span></span><br/>  | <span data-ttu-id="6ecce-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="6ecce-132">undefined</span></span><br/>       |
| <span data-ttu-id="6ecce-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="6ecce-133">MaxLength</span></span><br/>    | <span data-ttu-id="6ecce-134">integer</span><span class="sxs-lookup"><span data-stu-id="6ecce-134">integer</span></span><br/> | <span data-ttu-id="6ecce-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="6ecce-135">undefined</span></span><br/>       |
| <span data-ttu-id="6ecce-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="6ecce-136">MinLength</span></span><br/>    | <span data-ttu-id="6ecce-137">integer</span><span class="sxs-lookup"><span data-stu-id="6ecce-137">integer</span></span><br/> | <span data-ttu-id="6ecce-138">1</span><span class="sxs-lookup"><span data-stu-id="6ecce-138">1</span></span><br/>               |
| <span data-ttu-id="6ecce-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="6ecce-139">Mandatory</span></span><br/>    | <span data-ttu-id="6ecce-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6ecce-140">string</span></span><br/>  | <span data-ttu-id="6ecce-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="6ecce-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6ecce-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="6ecce-142">UnitType</span></span><br/>     | <span data-ttu-id="6ecce-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6ecce-143">string</span></span><br/>  | <span data-ttu-id="6ecce-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="6ecce-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="6ecce-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ecce-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ecce-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="6ecce-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




