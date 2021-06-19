---
description: Weitere Informationen zum PageWatermarkTextText-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db5ef33008f0ccb66b6af34e2cc245b90c1ebea
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395965"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="c04fa-105">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="c04fa-105">PageWatermarkTextText</span></span>

<span data-ttu-id="c04fa-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c04fa-106">This topic is not current.</span></span> <span data-ttu-id="c04fa-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c04fa-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c04fa-108">Gibt den Text des Wasserzeichens an.</span><span class="sxs-lookup"><span data-stu-id="c04fa-108">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="c04fa-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c04fa-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c04fa-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="c04fa-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c04fa-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c04fa-111">Element Information</span></span>



| <span data-ttu-id="c04fa-112">Name</span><span class="sxs-lookup"><span data-stu-id="c04fa-112">Name</span></span> | <span data-ttu-id="c04fa-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c04fa-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="c04fa-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c04fa-114">Element Type</span></span> <br/>   | <span data-ttu-id="c04fa-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c04fa-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="c04fa-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="c04fa-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c04fa-117">Seite</span><span class="sxs-lookup"><span data-stu-id="c04fa-117">Page</span></span><br/>                            |
| <span data-ttu-id="c04fa-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c04fa-118">Notes</span></span> <br/>          | <span data-ttu-id="c04fa-119">Verknüpft mit dem PageWatermark-Element</span><span class="sxs-lookup"><span data-stu-id="c04fa-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c04fa-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="c04fa-120">Structure Content</span></span>

<span data-ttu-id="c04fa-121">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="c04fa-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextText">
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

## <a name="structure-properties"></a><span data-ttu-id="c04fa-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="c04fa-122">Structure Properties</span></span>

<span data-ttu-id="c04fa-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c04fa-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c04fa-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c04fa-124">Property</span></span>                | <span data-ttu-id="c04fa-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c04fa-125">xsi:type</span></span>           | <span data-ttu-id="c04fa-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c04fa-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c04fa-127">DataType</span><span class="sxs-lookup"><span data-stu-id="c04fa-127">DataType</span></span><br/>     | <span data-ttu-id="c04fa-128">String</span><span class="sxs-lookup"><span data-stu-id="c04fa-128">String</span></span><br/>  | <span data-ttu-id="c04fa-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="c04fa-129">xs:string</span></span><br/>       |
| <span data-ttu-id="c04fa-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c04fa-130">DefaultValue</span></span><br/> | <span data-ttu-id="c04fa-131">Integer</span><span class="sxs-lookup"><span data-stu-id="c04fa-131">Integer</span></span><br/> | <span data-ttu-id="c04fa-132">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="c04fa-132">undefined</span></span><br/>       |
| <span data-ttu-id="c04fa-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="c04fa-133">MaxLength</span></span><br/>    | <span data-ttu-id="c04fa-134">Integer</span><span class="sxs-lookup"><span data-stu-id="c04fa-134">Integer</span></span><br/> | <span data-ttu-id="c04fa-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="c04fa-135">undefined</span></span><br/>       |
| <span data-ttu-id="c04fa-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="c04fa-136">MinLength</span></span><br/>    | <span data-ttu-id="c04fa-137">Integer</span><span class="sxs-lookup"><span data-stu-id="c04fa-137">Integer</span></span><br/> | <span data-ttu-id="c04fa-138">1</span><span class="sxs-lookup"><span data-stu-id="c04fa-138">1</span></span><br/>               |
| <span data-ttu-id="c04fa-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="c04fa-139">Mandatory</span></span><br/>    | <span data-ttu-id="c04fa-140">String</span><span class="sxs-lookup"><span data-stu-id="c04fa-140">String</span></span><br/>  | <span data-ttu-id="c04fa-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="c04fa-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c04fa-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="c04fa-142">UnitType</span></span><br/>     | <span data-ttu-id="c04fa-143">String</span><span class="sxs-lookup"><span data-stu-id="c04fa-143">String</span></span><br/>  | <span data-ttu-id="c04fa-144">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="c04fa-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="c04fa-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c04fa-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c04fa-146">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c04fa-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




