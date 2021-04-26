---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e97e768561fd13d5033b12f69a9bc481448e0e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999117"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="5615e-104">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="5615e-104">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="5615e-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5615e-105">This topic is not current.</span></span> <span data-ttu-id="5615e-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="5615e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5615e-107">Gibt das eingebettete Quellfarbprofil an.</span><span class="sxs-lookup"><span data-stu-id="5615e-107">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="5615e-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5615e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5615e-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="5615e-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5615e-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5615e-110">Element Information</span></span>



| <span data-ttu-id="5615e-111">Name</span><span class="sxs-lookup"><span data-stu-id="5615e-111">Name</span></span> | <span data-ttu-id="5615e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5615e-112">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="5615e-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="5615e-113">Element Type</span></span> <br/>   | <span data-ttu-id="5615e-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5615e-114">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="5615e-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="5615e-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5615e-116">Seite</span><span class="sxs-lookup"><span data-stu-id="5615e-116">Page</span></span><br/>                                     |
| <span data-ttu-id="5615e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5615e-117">Notes</span></span> <br/>          | <span data-ttu-id="5615e-118">Verknüpft mit dem PageSourceColorProfile-Element</span><span class="sxs-lookup"><span data-stu-id="5615e-118">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5615e-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="5615e-119">Structure Content</span></span>

<span data-ttu-id="5615e-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="5615e-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5615e-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="5615e-121">Structure Properties</span></span>

<span data-ttu-id="5615e-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5615e-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5615e-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5615e-123">Property</span></span>                | <span data-ttu-id="5615e-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5615e-124">xsi:type</span></span>           | <span data-ttu-id="5615e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5615e-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5615e-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5615e-126">DataType</span></span><br/>     | <span data-ttu-id="5615e-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5615e-127">string</span></span><br/>  | <span data-ttu-id="5615e-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="5615e-128">xs:string</span></span><br/>       |
| <span data-ttu-id="5615e-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5615e-129">DefaultValue</span></span><br/> | <span data-ttu-id="5615e-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5615e-130">string</span></span><br/>  | <span data-ttu-id="5615e-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="5615e-131">undefined</span></span><br/>       |
| <span data-ttu-id="5615e-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="5615e-132">MaxLength</span></span><br/>    | <span data-ttu-id="5615e-133">integer</span><span class="sxs-lookup"><span data-stu-id="5615e-133">integer</span></span><br/> | <span data-ttu-id="5615e-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="5615e-134">undefined</span></span><br/>       |
| <span data-ttu-id="5615e-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="5615e-135">MinLength</span></span><br/>    | <span data-ttu-id="5615e-136">integer</span><span class="sxs-lookup"><span data-stu-id="5615e-136">integer</span></span><br/> | <span data-ttu-id="5615e-137">1</span><span class="sxs-lookup"><span data-stu-id="5615e-137">1</span></span><br/>               |
| <span data-ttu-id="5615e-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="5615e-138">Mandatory</span></span><br/>    | <span data-ttu-id="5615e-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5615e-139">string</span></span><br/>  | <span data-ttu-id="5615e-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="5615e-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5615e-141">Unittype</span><span class="sxs-lookup"><span data-stu-id="5615e-141">UnitType</span></span><br/>     | <span data-ttu-id="5615e-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5615e-142">string</span></span><br/>  | <span data-ttu-id="5615e-143">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="5615e-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="5615e-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5615e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5615e-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="5615e-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




