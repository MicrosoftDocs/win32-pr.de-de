---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2372636ea22610e6a209cfad3f1fe6297be34833
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997187"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="b219b-104">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="b219b-104">DocumentBindingGutter</span></span>

<span data-ttu-id="b219b-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b219b-105">This topic is not current.</span></span> <span data-ttu-id="b219b-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="b219b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b219b-107">Gibt die Breite des Bindungsstegs an.</span><span class="sxs-lookup"><span data-stu-id="b219b-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="b219b-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b219b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b219b-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b219b-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b219b-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b219b-110">Element Information</span></span>



| <span data-ttu-id="b219b-111">Name</span><span class="sxs-lookup"><span data-stu-id="b219b-111">Name</span></span> | <span data-ttu-id="b219b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b219b-112">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="b219b-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="b219b-113">Element Type</span></span> <br/>   | <span data-ttu-id="b219b-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b219b-114">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="b219b-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="b219b-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b219b-116">Dokument</span><span class="sxs-lookup"><span data-stu-id="b219b-116">Document</span></span><br/>                          |
| <span data-ttu-id="b219b-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b219b-117">Notes</span></span> <br/>          | <span data-ttu-id="b219b-118">Verknüpft mit dem DocumentBinding-Element</span><span class="sxs-lookup"><span data-stu-id="b219b-118">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b219b-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="b219b-119">Structure Content</span></span>

<span data-ttu-id="b219b-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="b219b-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b219b-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="b219b-121">Structure Properties</span></span>

<span data-ttu-id="b219b-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b219b-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b219b-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b219b-123">Property</span></span>                | <span data-ttu-id="b219b-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b219b-124">xsi:type</span></span>           | <span data-ttu-id="b219b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b219b-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b219b-126">DataType</span><span class="sxs-lookup"><span data-stu-id="b219b-126">DataType</span></span><br/>     | <span data-ttu-id="b219b-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b219b-127">string</span></span><br/>  | <span data-ttu-id="b219b-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b219b-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="b219b-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b219b-129">DefaultValue</span></span><br/> | <span data-ttu-id="b219b-130">integer</span><span class="sxs-lookup"><span data-stu-id="b219b-130">integer</span></span><br/> | <span data-ttu-id="b219b-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b219b-131">undefined</span></span><br/>       |
| <span data-ttu-id="b219b-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b219b-132">MaxValue</span></span><br/>     | <span data-ttu-id="b219b-133">integer</span><span class="sxs-lookup"><span data-stu-id="b219b-133">integer</span></span><br/> | <span data-ttu-id="b219b-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b219b-134">undefined</span></span><br/>       |
| <span data-ttu-id="b219b-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="b219b-135">MinValue</span></span><br/>     | <span data-ttu-id="b219b-136">integer</span><span class="sxs-lookup"><span data-stu-id="b219b-136">integer</span></span><br/> | <span data-ttu-id="b219b-137">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="b219b-137">undefined</span></span><br/>       |
| <span data-ttu-id="b219b-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="b219b-138">Mandatory</span></span><br/>    | <span data-ttu-id="b219b-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b219b-139">String</span></span><br/>  | <span data-ttu-id="b219b-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="b219b-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b219b-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="b219b-141">Multiple</span></span><br/>     | <span data-ttu-id="b219b-142">integer</span><span class="sxs-lookup"><span data-stu-id="b219b-142">integer</span></span><br/> | <span data-ttu-id="b219b-143">1</span><span class="sxs-lookup"><span data-stu-id="b219b-143">1</span></span><br/>               |
| <span data-ttu-id="b219b-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="b219b-144">UnitType</span></span><br/>     | <span data-ttu-id="b219b-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b219b-145">string</span></span><br/>  | <span data-ttu-id="b219b-146">Mikron</span><span class="sxs-lookup"><span data-stu-id="b219b-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b219b-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b219b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b219b-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="b219b-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




