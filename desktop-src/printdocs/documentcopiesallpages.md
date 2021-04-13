---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: DocumentCopiesAllPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8941f8a6f1f7ef8ec554fa0eba937ddd6f686ad
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351798"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="65f29-104">DocumentCopiesAllPages</span><span class="sxs-lookup"><span data-stu-id="65f29-104">DocumentCopiesAllPages</span></span>

<span data-ttu-id="65f29-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="65f29-105">This topic is not current.</span></span> <span data-ttu-id="65f29-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="65f29-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="65f29-107">Gibt die Anzahl der Kopien eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="65f29-107">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="65f29-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="65f29-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="65f29-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="65f29-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="65f29-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="65f29-110">Element Information</span></span>



| <span data-ttu-id="65f29-111">Name</span><span class="sxs-lookup"><span data-stu-id="65f29-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="65f29-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="65f29-112">Element Type</span></span> <br/>   | <span data-ttu-id="65f29-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="65f29-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="65f29-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="65f29-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="65f29-115">Dokument</span><span class="sxs-lookup"><span data-stu-id="65f29-115">Document</span></span><br/>     |
| <span data-ttu-id="65f29-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65f29-116">Notes</span></span> <br/>          | <span data-ttu-id="65f29-117">Keine</span><span class="sxs-lookup"><span data-stu-id="65f29-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="65f29-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="65f29-118">Structure Content</span></span>

<span data-ttu-id="65f29-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="65f29-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCopiesAllPages">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="65f29-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="65f29-120">Structure Properties</span></span>

<span data-ttu-id="65f29-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="65f29-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="65f29-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="65f29-122">Property</span></span>                | <span data-ttu-id="65f29-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="65f29-123">xsi:type</span></span>           | <span data-ttu-id="65f29-124">Wert</span><span class="sxs-lookup"><span data-stu-id="65f29-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="65f29-125">DataType</span><span class="sxs-lookup"><span data-stu-id="65f29-125">DataType</span></span><br/>     | <span data-ttu-id="65f29-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65f29-126">string</span></span><br/>  | <span data-ttu-id="65f29-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="65f29-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="65f29-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="65f29-128">DefaultValue</span></span><br/> | <span data-ttu-id="65f29-129">integer</span><span class="sxs-lookup"><span data-stu-id="65f29-129">integer</span></span><br/> | <span data-ttu-id="65f29-130">1</span><span class="sxs-lookup"><span data-stu-id="65f29-130">1</span></span><br/>                 |
| <span data-ttu-id="65f29-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="65f29-131">MaxValue</span></span><br/>     | <span data-ttu-id="65f29-132">integer</span><span class="sxs-lookup"><span data-stu-id="65f29-132">integer</span></span><br/> | <span data-ttu-id="65f29-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="65f29-133">undefined</span></span><br/>         |
| <span data-ttu-id="65f29-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="65f29-134">MinValue</span></span><br/>     | <span data-ttu-id="65f29-135">integer</span><span class="sxs-lookup"><span data-stu-id="65f29-135">integer</span></span><br/> | <span data-ttu-id="65f29-136">1</span><span class="sxs-lookup"><span data-stu-id="65f29-136">1</span></span><br/>                 |
| <span data-ttu-id="65f29-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="65f29-137">Mandatory</span></span><br/>    | <span data-ttu-id="65f29-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65f29-138">string</span></span><br/>  | <span data-ttu-id="65f29-139">PSK: nicht bedingt</span><span class="sxs-lookup"><span data-stu-id="65f29-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="65f29-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="65f29-140">Multiple</span></span><br/>     | <span data-ttu-id="65f29-141">integer</span><span class="sxs-lookup"><span data-stu-id="65f29-141">integer</span></span><br/> | <span data-ttu-id="65f29-142">1</span><span class="sxs-lookup"><span data-stu-id="65f29-142">1</span></span><br/>                 |
| <span data-ttu-id="65f29-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="65f29-143">UnitType</span></span><br/>     | <span data-ttu-id="65f29-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65f29-144">string</span></span><br/>  | <span data-ttu-id="65f29-145">Uni</span><span class="sxs-lookup"><span data-stu-id="65f29-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="65f29-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="65f29-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65f29-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="65f29-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




