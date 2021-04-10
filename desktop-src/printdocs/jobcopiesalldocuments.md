---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f8be33f98b540cab56b88df49cfb1e3c067988
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761547"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="c4744-104">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="c4744-104">JobCopiesAllDocuments</span></span>

<span data-ttu-id="c4744-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c4744-105">This topic is not current.</span></span> <span data-ttu-id="c4744-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c4744-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c4744-107">Gibt die Anzahl der Kopien eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="c4744-107">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="c4744-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c4744-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c4744-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="c4744-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c4744-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c4744-110">Element Information</span></span>



| <span data-ttu-id="c4744-111">Name</span><span class="sxs-lookup"><span data-stu-id="c4744-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="c4744-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c4744-112">Element Type</span></span> <br/>   | <span data-ttu-id="c4744-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c4744-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="c4744-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="c4744-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c4744-115">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c4744-115">Job</span></span><br/>          |
| <span data-ttu-id="c4744-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4744-116">Notes</span></span> <br/>          | <span data-ttu-id="c4744-117">Keine</span><span class="sxs-lookup"><span data-stu-id="c4744-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="c4744-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="c4744-118">Structure Content</span></span>

<span data-ttu-id="c4744-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="c4744-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
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

## <a name="structure-properties"></a><span data-ttu-id="c4744-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4744-120">Structure Properties</span></span>

<span data-ttu-id="c4744-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c4744-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c4744-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c4744-122">Property</span></span>                | <span data-ttu-id="c4744-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c4744-123">xsi:type</span></span>           | <span data-ttu-id="c4744-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c4744-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="c4744-125">DataType</span><span class="sxs-lookup"><span data-stu-id="c4744-125">DataType</span></span><br/>     | <span data-ttu-id="c4744-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c4744-126">string</span></span><br/>  | <span data-ttu-id="c4744-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c4744-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="c4744-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c4744-128">DefaultValue</span></span><br/> | <span data-ttu-id="c4744-129">integer</span><span class="sxs-lookup"><span data-stu-id="c4744-129">integer</span></span><br/> | <span data-ttu-id="c4744-130">1</span><span class="sxs-lookup"><span data-stu-id="c4744-130">1</span></span><br/>                 |
| <span data-ttu-id="c4744-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c4744-131">MaxValue</span></span><br/>     | <span data-ttu-id="c4744-132">integer</span><span class="sxs-lookup"><span data-stu-id="c4744-132">integer</span></span><br/> | <span data-ttu-id="c4744-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="c4744-133">undefined</span></span><br/>         |
| <span data-ttu-id="c4744-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="c4744-134">MinValue</span></span><br/>     | <span data-ttu-id="c4744-135">integer</span><span class="sxs-lookup"><span data-stu-id="c4744-135">integer</span></span><br/> | <span data-ttu-id="c4744-136">1</span><span class="sxs-lookup"><span data-stu-id="c4744-136">1</span></span><br/>                 |
| <span data-ttu-id="c4744-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="c4744-137">Mandatory</span></span><br/>    | <span data-ttu-id="c4744-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c4744-138">string</span></span><br/>  | <span data-ttu-id="c4744-139">PSK: nicht bedingt</span><span class="sxs-lookup"><span data-stu-id="c4744-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="c4744-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="c4744-140">Multiple</span></span><br/>     | <span data-ttu-id="c4744-141">integer</span><span class="sxs-lookup"><span data-stu-id="c4744-141">integer</span></span><br/> | <span data-ttu-id="c4744-142">1</span><span class="sxs-lookup"><span data-stu-id="c4744-142">1</span></span><br/>                 |
| <span data-ttu-id="c4744-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="c4744-143">UnitType</span></span><br/>     | <span data-ttu-id="c4744-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c4744-144">string</span></span><br/>  | <span data-ttu-id="c4744-145">Uni</span><span class="sxs-lookup"><span data-stu-id="c4744-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="c4744-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4744-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4744-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="c4744-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




