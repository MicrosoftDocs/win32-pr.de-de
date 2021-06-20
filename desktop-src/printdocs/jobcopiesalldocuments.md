---
description: Erfahren Sie mehr über das JobCopiesAllDocuments-Element, das die Anzahl der Kopien eines Auftrags angibt.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05166715a5985c5ddee33fa6808d0fb6b150774b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409033"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="f7472-103">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="f7472-103">JobCopiesAllDocuments</span></span>

<span data-ttu-id="f7472-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="f7472-104">This topic is not current.</span></span> <span data-ttu-id="f7472-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="f7472-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f7472-106">Gibt die Anzahl der Kopien eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="f7472-106">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="f7472-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f7472-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f7472-108">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="f7472-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f7472-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f7472-109">Element Information</span></span>



| <span data-ttu-id="f7472-110">Name</span><span class="sxs-lookup"><span data-stu-id="f7472-110">Name</span></span> | <span data-ttu-id="f7472-111">Wert</span><span class="sxs-lookup"><span data-stu-id="f7472-111">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="f7472-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="f7472-112">Element Type</span></span> <br/>   | <span data-ttu-id="f7472-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f7472-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="f7472-114">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="f7472-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f7472-115">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f7472-115">Job</span></span><br/>          |
| <span data-ttu-id="f7472-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f7472-116">Notes</span></span> <br/>          | <span data-ttu-id="f7472-117">Keine</span><span class="sxs-lookup"><span data-stu-id="f7472-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="f7472-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="f7472-118">Structure Content</span></span>

<span data-ttu-id="f7472-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="f7472-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f7472-120">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="f7472-120">Structure Properties</span></span>

<span data-ttu-id="f7472-121">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f7472-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f7472-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7472-122">Property</span></span>                | <span data-ttu-id="f7472-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f7472-123">xsi:type</span></span>           | <span data-ttu-id="f7472-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f7472-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="f7472-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f7472-125">DataType</span></span><br/>     | <span data-ttu-id="f7472-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7472-126">string</span></span><br/>  | <span data-ttu-id="f7472-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f7472-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="f7472-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f7472-128">DefaultValue</span></span><br/> | <span data-ttu-id="f7472-129">integer</span><span class="sxs-lookup"><span data-stu-id="f7472-129">integer</span></span><br/> | <span data-ttu-id="f7472-130">1</span><span class="sxs-lookup"><span data-stu-id="f7472-130">1</span></span><br/>                 |
| <span data-ttu-id="f7472-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f7472-131">MaxValue</span></span><br/>     | <span data-ttu-id="f7472-132">integer</span><span class="sxs-lookup"><span data-stu-id="f7472-132">integer</span></span><br/> | <span data-ttu-id="f7472-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="f7472-133">undefined</span></span><br/>         |
| <span data-ttu-id="f7472-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="f7472-134">MinValue</span></span><br/>     | <span data-ttu-id="f7472-135">integer</span><span class="sxs-lookup"><span data-stu-id="f7472-135">integer</span></span><br/> | <span data-ttu-id="f7472-136">1</span><span class="sxs-lookup"><span data-stu-id="f7472-136">1</span></span><br/>                 |
| <span data-ttu-id="f7472-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="f7472-137">Mandatory</span></span><br/>    | <span data-ttu-id="f7472-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7472-138">string</span></span><br/>  | <span data-ttu-id="f7472-139">psk:Bedingungslos</span><span class="sxs-lookup"><span data-stu-id="f7472-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="f7472-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="f7472-140">Multiple</span></span><br/>     | <span data-ttu-id="f7472-141">integer</span><span class="sxs-lookup"><span data-stu-id="f7472-141">integer</span></span><br/> | <span data-ttu-id="f7472-142">1</span><span class="sxs-lookup"><span data-stu-id="f7472-142">1</span></span><br/>                 |
| <span data-ttu-id="f7472-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="f7472-143">UnitType</span></span><br/>     | <span data-ttu-id="f7472-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7472-144">string</span></span><br/>  | <span data-ttu-id="f7472-145">Kopien</span><span class="sxs-lookup"><span data-stu-id="f7472-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="f7472-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7472-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7472-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="f7472-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




