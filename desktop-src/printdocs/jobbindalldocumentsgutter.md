---
description: Erfahren Sie mehr über das JobBindAllDocumentsGutter-Element, das die Breite des Bindungsdarms angibt.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42180ff9a00d1502d844b270fe5da7324825ca3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409073"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="08c36-103">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="08c36-103">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="08c36-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="08c36-104">This topic is not current.</span></span> <span data-ttu-id="08c36-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="08c36-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="08c36-106">Gibt die Breite des Bindungsrinnenstrichs an.</span><span class="sxs-lookup"><span data-stu-id="08c36-106">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="08c36-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="08c36-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="08c36-108">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="08c36-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="08c36-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="08c36-109">Element Information</span></span>



| <span data-ttu-id="08c36-110">Name</span><span class="sxs-lookup"><span data-stu-id="08c36-110">Name</span></span> | <span data-ttu-id="08c36-111">Wert</span><span class="sxs-lookup"><span data-stu-id="08c36-111">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="08c36-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="08c36-112">Element Type</span></span> <br/>   | <span data-ttu-id="08c36-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="08c36-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="08c36-114">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="08c36-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="08c36-115">Auftrag</span><span class="sxs-lookup"><span data-stu-id="08c36-115">Job</span></span> <br/>                         |
| <span data-ttu-id="08c36-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="08c36-116">Notes</span></span> <br/>          | <span data-ttu-id="08c36-117">Mit JobBinding-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="08c36-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="08c36-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="08c36-118">Structure Content</span></span>

<span data-ttu-id="08c36-119">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="08c36-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="08c36-120">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="08c36-120">Structure Properties</span></span>

<span data-ttu-id="08c36-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="08c36-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="08c36-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08c36-122">Property</span></span>                | <span data-ttu-id="08c36-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="08c36-123">xsi:type</span></span>           | <span data-ttu-id="08c36-124">Wert</span><span class="sxs-lookup"><span data-stu-id="08c36-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="08c36-125">DataType</span><span class="sxs-lookup"><span data-stu-id="08c36-125">DataType</span></span><br/>     | <span data-ttu-id="08c36-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="08c36-126">string</span></span><br/>  | <span data-ttu-id="08c36-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="08c36-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="08c36-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="08c36-128">DefaultValue</span></span><br/> | <span data-ttu-id="08c36-129">integer</span><span class="sxs-lookup"><span data-stu-id="08c36-129">integer</span></span><br/> | <span data-ttu-id="08c36-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="08c36-130">undefined</span></span><br/>       |
| <span data-ttu-id="08c36-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="08c36-131">MaxValue</span></span><br/>     | <span data-ttu-id="08c36-132">integer</span><span class="sxs-lookup"><span data-stu-id="08c36-132">integer</span></span><br/> | <span data-ttu-id="08c36-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="08c36-133">undefined</span></span><br/>       |
| <span data-ttu-id="08c36-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="08c36-134">MinValue</span></span><br/>     | <span data-ttu-id="08c36-135">integer</span><span class="sxs-lookup"><span data-stu-id="08c36-135">integer</span></span><br/> | <span data-ttu-id="08c36-136">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="08c36-136">undefined</span></span><br/>       |
| <span data-ttu-id="08c36-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="08c36-137">Mandatory</span></span><br/>    | <span data-ttu-id="08c36-138">String</span><span class="sxs-lookup"><span data-stu-id="08c36-138">String</span></span><br/>  | <span data-ttu-id="08c36-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="08c36-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="08c36-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="08c36-140">Multiple</span></span><br/>     | <span data-ttu-id="08c36-141">integer</span><span class="sxs-lookup"><span data-stu-id="08c36-141">integer</span></span><br/> | <span data-ttu-id="08c36-142">1</span><span class="sxs-lookup"><span data-stu-id="08c36-142">1</span></span><br/>               |
| <span data-ttu-id="08c36-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="08c36-143">UnitType</span></span><br/>     | <span data-ttu-id="08c36-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="08c36-144">string</span></span><br/>  | <span data-ttu-id="08c36-145">Mikron</span><span class="sxs-lookup"><span data-stu-id="08c36-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="08c36-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08c36-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08c36-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="08c36-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




