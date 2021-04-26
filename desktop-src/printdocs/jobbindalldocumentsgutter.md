---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04615b85939d483f6bd2e720afa65a88d44c1caf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998377"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="39df3-104">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="39df3-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="39df3-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="39df3-105">This topic is not current.</span></span> <span data-ttu-id="39df3-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="39df3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="39df3-107">Gibt die Breite des Bindungsstegs an.</span><span class="sxs-lookup"><span data-stu-id="39df3-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="39df3-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="39df3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="39df3-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="39df3-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="39df3-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="39df3-110">Element Information</span></span>



| <span data-ttu-id="39df3-111">Name</span><span class="sxs-lookup"><span data-stu-id="39df3-111">Name</span></span> | <span data-ttu-id="39df3-112">Wert</span><span class="sxs-lookup"><span data-stu-id="39df3-112">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="39df3-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="39df3-113">Element Type</span></span> <br/>   | <span data-ttu-id="39df3-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="39df3-114">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="39df3-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="39df3-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="39df3-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="39df3-116">Job</span></span> <br/>                         |
| <span data-ttu-id="39df3-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39df3-117">Notes</span></span> <br/>          | <span data-ttu-id="39df3-118">Verknüpft mit dem JobBinding-Element</span><span class="sxs-lookup"><span data-stu-id="39df3-118">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="39df3-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="39df3-119">Structure Content</span></span>

<span data-ttu-id="39df3-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="39df3-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobBindAllDocumentsGutter">
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

## <a name="structure-properties"></a><span data-ttu-id="39df3-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="39df3-121">Structure Properties</span></span>

<span data-ttu-id="39df3-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="39df3-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="39df3-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39df3-123">Property</span></span>                | <span data-ttu-id="39df3-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="39df3-124">xsi:type</span></span>           | <span data-ttu-id="39df3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="39df3-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="39df3-126">DataType</span><span class="sxs-lookup"><span data-stu-id="39df3-126">DataType</span></span><br/>     | <span data-ttu-id="39df3-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="39df3-127">string</span></span><br/>  | <span data-ttu-id="39df3-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="39df3-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="39df3-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="39df3-129">DefaultValue</span></span><br/> | <span data-ttu-id="39df3-130">integer</span><span class="sxs-lookup"><span data-stu-id="39df3-130">integer</span></span><br/> | <span data-ttu-id="39df3-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="39df3-131">undefined</span></span><br/>       |
| <span data-ttu-id="39df3-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="39df3-132">MaxValue</span></span><br/>     | <span data-ttu-id="39df3-133">integer</span><span class="sxs-lookup"><span data-stu-id="39df3-133">integer</span></span><br/> | <span data-ttu-id="39df3-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="39df3-134">undefined</span></span><br/>       |
| <span data-ttu-id="39df3-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="39df3-135">MinValue</span></span><br/>     | <span data-ttu-id="39df3-136">integer</span><span class="sxs-lookup"><span data-stu-id="39df3-136">integer</span></span><br/> | <span data-ttu-id="39df3-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="39df3-137">undefined</span></span><br/>       |
| <span data-ttu-id="39df3-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="39df3-138">Mandatory</span></span><br/>    | <span data-ttu-id="39df3-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="39df3-139">String</span></span><br/>  | <span data-ttu-id="39df3-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="39df3-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="39df3-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="39df3-141">Multiple</span></span><br/>     | <span data-ttu-id="39df3-142">integer</span><span class="sxs-lookup"><span data-stu-id="39df3-142">integer</span></span><br/> | <span data-ttu-id="39df3-143">1</span><span class="sxs-lookup"><span data-stu-id="39df3-143">1</span></span><br/>               |
| <span data-ttu-id="39df3-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="39df3-144">UnitType</span></span><br/>     | <span data-ttu-id="39df3-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="39df3-145">string</span></span><br/>  | <span data-ttu-id="39df3-146">Mikron</span><span class="sxs-lookup"><span data-stu-id="39df3-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="39df3-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39df3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39df3-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="39df3-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




