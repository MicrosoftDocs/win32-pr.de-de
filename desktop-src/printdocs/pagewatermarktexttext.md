---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb19f5965347e79732aa116e5be51f90e4ef6943
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996077"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="fcc51-104">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="fcc51-104">PageWatermarkTextText</span></span>

<span data-ttu-id="fcc51-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="fcc51-105">This topic is not current.</span></span> <span data-ttu-id="fcc51-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="fcc51-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fcc51-107">Gibt den Text des Wasserzeichens an.</span><span class="sxs-lookup"><span data-stu-id="fcc51-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="fcc51-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fcc51-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fcc51-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="fcc51-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fcc51-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fcc51-110">Element Information</span></span>



| <span data-ttu-id="fcc51-111">Name</span><span class="sxs-lookup"><span data-stu-id="fcc51-111">Name</span></span> | <span data-ttu-id="fcc51-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fcc51-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="fcc51-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="fcc51-113">Element Type</span></span> <br/>   | <span data-ttu-id="fcc51-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fcc51-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="fcc51-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="fcc51-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fcc51-116">Seite</span><span class="sxs-lookup"><span data-stu-id="fcc51-116">Page</span></span><br/>                            |
| <span data-ttu-id="fcc51-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fcc51-117">Notes</span></span> <br/>          | <span data-ttu-id="fcc51-118">Verknüpft mit dem PageWatermark-Element</span><span class="sxs-lookup"><span data-stu-id="fcc51-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fcc51-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="fcc51-119">Structure Content</span></span>

<span data-ttu-id="fcc51-120">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="fcc51-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="fcc51-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="fcc51-121">Structure Properties</span></span>

<span data-ttu-id="fcc51-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fcc51-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fcc51-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fcc51-123">Property</span></span>                | <span data-ttu-id="fcc51-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fcc51-124">xsi:type</span></span>           | <span data-ttu-id="fcc51-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fcc51-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fcc51-126">DataType</span><span class="sxs-lookup"><span data-stu-id="fcc51-126">DataType</span></span><br/>     | <span data-ttu-id="fcc51-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fcc51-127">String</span></span><br/>  | <span data-ttu-id="fcc51-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcc51-128">xs:string</span></span><br/>       |
| <span data-ttu-id="fcc51-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fcc51-129">DefaultValue</span></span><br/> | <span data-ttu-id="fcc51-130">Integer</span><span class="sxs-lookup"><span data-stu-id="fcc51-130">Integer</span></span><br/> | <span data-ttu-id="fcc51-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="fcc51-131">undefined</span></span><br/>       |
| <span data-ttu-id="fcc51-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="fcc51-132">MaxLength</span></span><br/>    | <span data-ttu-id="fcc51-133">Integer</span><span class="sxs-lookup"><span data-stu-id="fcc51-133">Integer</span></span><br/> | <span data-ttu-id="fcc51-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="fcc51-134">undefined</span></span><br/>       |
| <span data-ttu-id="fcc51-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="fcc51-135">MinLength</span></span><br/>    | <span data-ttu-id="fcc51-136">Integer</span><span class="sxs-lookup"><span data-stu-id="fcc51-136">Integer</span></span><br/> | <span data-ttu-id="fcc51-137">1</span><span class="sxs-lookup"><span data-stu-id="fcc51-137">1</span></span><br/>               |
| <span data-ttu-id="fcc51-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="fcc51-138">Mandatory</span></span><br/>    | <span data-ttu-id="fcc51-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fcc51-139">String</span></span><br/>  | <span data-ttu-id="fcc51-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="fcc51-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fcc51-141">Unittype</span><span class="sxs-lookup"><span data-stu-id="fcc51-141">UnitType</span></span><br/>     | <span data-ttu-id="fcc51-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fcc51-142">String</span></span><br/>  | <span data-ttu-id="fcc51-143">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="fcc51-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="fcc51-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fcc51-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcc51-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="fcc51-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




