---
description: Hier finden Sie Informationen zum DocumentBindingGutter-Parameter. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45839aa07d740d8498e477809b45aa823460b23f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118465"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="ed49c-105">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="ed49c-105">DocumentBindingGutter</span></span>

<span data-ttu-id="ed49c-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ed49c-106">This topic is not current.</span></span> <span data-ttu-id="ed49c-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="ed49c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ed49c-108">Gibt die Breite des Bindungsrinnenstrichs an.</span><span class="sxs-lookup"><span data-stu-id="ed49c-108">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="ed49c-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ed49c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ed49c-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ed49c-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ed49c-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ed49c-111">Element Information</span></span>



| <span data-ttu-id="ed49c-112">Name</span><span class="sxs-lookup"><span data-stu-id="ed49c-112">Name</span></span> | <span data-ttu-id="ed49c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ed49c-113">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="ed49c-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ed49c-114">Element Type</span></span> <br/>   | <span data-ttu-id="ed49c-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ed49c-115">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="ed49c-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="ed49c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ed49c-117">Dokument</span><span class="sxs-lookup"><span data-stu-id="ed49c-117">Document</span></span><br/>                          |
| <span data-ttu-id="ed49c-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed49c-118">Notes</span></span> <br/>          | <span data-ttu-id="ed49c-119">Mit DocumentBinding-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="ed49c-119">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ed49c-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ed49c-120">Structure Content</span></span>

<span data-ttu-id="ed49c-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="ed49c-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBindingGutter">
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

## <a name="structure-properties"></a><span data-ttu-id="ed49c-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed49c-122">Structure Properties</span></span>

<span data-ttu-id="ed49c-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ed49c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ed49c-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ed49c-124">Property</span></span>                | <span data-ttu-id="ed49c-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ed49c-125">xsi:type</span></span>           | <span data-ttu-id="ed49c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ed49c-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ed49c-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ed49c-127">DataType</span></span><br/>     | <span data-ttu-id="ed49c-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ed49c-128">string</span></span><br/>  | <span data-ttu-id="ed49c-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ed49c-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="ed49c-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ed49c-130">DefaultValue</span></span><br/> | <span data-ttu-id="ed49c-131">integer</span><span class="sxs-lookup"><span data-stu-id="ed49c-131">integer</span></span><br/> | <span data-ttu-id="ed49c-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ed49c-132">undefined</span></span><br/>       |
| <span data-ttu-id="ed49c-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ed49c-133">MaxValue</span></span><br/>     | <span data-ttu-id="ed49c-134">integer</span><span class="sxs-lookup"><span data-stu-id="ed49c-134">integer</span></span><br/> | <span data-ttu-id="ed49c-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ed49c-135">undefined</span></span><br/>       |
| <span data-ttu-id="ed49c-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="ed49c-136">MinValue</span></span><br/>     | <span data-ttu-id="ed49c-137">integer</span><span class="sxs-lookup"><span data-stu-id="ed49c-137">integer</span></span><br/> | <span data-ttu-id="ed49c-138">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ed49c-138">undefined</span></span><br/>       |
| <span data-ttu-id="ed49c-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ed49c-139">Mandatory</span></span><br/>    | <span data-ttu-id="ed49c-140">String</span><span class="sxs-lookup"><span data-stu-id="ed49c-140">String</span></span><br/>  | <span data-ttu-id="ed49c-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="ed49c-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ed49c-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="ed49c-142">Multiple</span></span><br/>     | <span data-ttu-id="ed49c-143">integer</span><span class="sxs-lookup"><span data-stu-id="ed49c-143">integer</span></span><br/> | <span data-ttu-id="ed49c-144">1</span><span class="sxs-lookup"><span data-stu-id="ed49c-144">1</span></span><br/>               |
| <span data-ttu-id="ed49c-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="ed49c-145">UnitType</span></span><br/>     | <span data-ttu-id="ed49c-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ed49c-146">string</span></span><br/>  | <span data-ttu-id="ed49c-147">Mikron</span><span class="sxs-lookup"><span data-stu-id="ed49c-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ed49c-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed49c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed49c-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="ed49c-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




