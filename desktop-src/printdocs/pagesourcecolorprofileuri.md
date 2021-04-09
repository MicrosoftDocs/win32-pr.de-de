---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 25c3c70f-20e3-4e44-9c59-bb66b4bd14d9
title: Pagesourcecolorprofileuri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b3f2396fe3a886ed797392a3e1fd9f3c6d0170
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050739"
---
# <a name="pagesourcecolorprofileuri"></a><span data-ttu-id="4da83-104">Pagesourcecolorprofileuri</span><span class="sxs-lookup"><span data-stu-id="4da83-104">PageSourceColorProfileURI</span></span>

<span data-ttu-id="4da83-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4da83-105">This topic is not current.</span></span> <span data-ttu-id="4da83-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4da83-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4da83-107">Gibt die Quelle für das Farbprofil an.</span><span class="sxs-lookup"><span data-stu-id="4da83-107">Specifies the source for color profile.</span></span>

-   [<span data-ttu-id="4da83-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4da83-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4da83-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4da83-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4da83-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4da83-110">Element Information</span></span>



| <span data-ttu-id="4da83-111">Name</span><span class="sxs-lookup"><span data-stu-id="4da83-111">Name</span></span>                       |                                                     |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="4da83-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4da83-112">Element Type</span></span> <br/>   | <span data-ttu-id="4da83-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4da83-113">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="4da83-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="4da83-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4da83-115">Seite</span><span class="sxs-lookup"><span data-stu-id="4da83-115">Page</span></span><br/>                                     |
| <span data-ttu-id="4da83-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="4da83-116">Notes</span></span> <br/>          | <span data-ttu-id="4da83-117">Verknüpft mit pagesourcecolorprofile-Element</span><span class="sxs-lookup"><span data-stu-id="4da83-117">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4da83-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4da83-118">Structure Content</span></span>

<span data-ttu-id="4da83-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="4da83-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="4da83-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4da83-120">Structure Properties</span></span>

<span data-ttu-id="4da83-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4da83-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4da83-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4da83-122">Property</span></span>                | <span data-ttu-id="4da83-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4da83-123">xsi:type</span></span>           | <span data-ttu-id="4da83-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4da83-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4da83-125">DataType</span><span class="sxs-lookup"><span data-stu-id="4da83-125">DataType</span></span><br/>     | <span data-ttu-id="4da83-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4da83-126">string</span></span><br/>  | <span data-ttu-id="4da83-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="4da83-127">xs:string</span></span><br/>       |
| <span data-ttu-id="4da83-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4da83-128">DefaultValue</span></span><br/> | <span data-ttu-id="4da83-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4da83-129">string</span></span><br/>  | <span data-ttu-id="4da83-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4da83-130">undefined</span></span><br/>       |
| <span data-ttu-id="4da83-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="4da83-131">MaxLength</span></span><br/>    | <span data-ttu-id="4da83-132">integer</span><span class="sxs-lookup"><span data-stu-id="4da83-132">integer</span></span><br/> | <span data-ttu-id="4da83-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4da83-133">undefined</span></span><br/>       |
| <span data-ttu-id="4da83-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="4da83-134">MinLength</span></span><br/>    | <span data-ttu-id="4da83-135">integer</span><span class="sxs-lookup"><span data-stu-id="4da83-135">integer</span></span><br/> | <span data-ttu-id="4da83-136">1</span><span class="sxs-lookup"><span data-stu-id="4da83-136">1</span></span><br/>               |
| <span data-ttu-id="4da83-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="4da83-137">Mandatory</span></span><br/>    | <span data-ttu-id="4da83-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4da83-138">string</span></span><br/>  | <span data-ttu-id="4da83-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="4da83-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4da83-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="4da83-140">UnitType</span></span><br/>     | <span data-ttu-id="4da83-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4da83-141">string</span></span><br/>  | <span data-ttu-id="4da83-142">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="4da83-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="4da83-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4da83-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4da83-144">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="4da83-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




