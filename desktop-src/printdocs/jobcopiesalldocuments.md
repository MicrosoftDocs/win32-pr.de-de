---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8e606095462dc3a2eee1391121bf663de3655c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998367"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="cf471-104">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="cf471-104">JobCopiesAllDocuments</span></span>

<span data-ttu-id="cf471-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="cf471-105">This topic is not current.</span></span> <span data-ttu-id="cf471-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="cf471-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cf471-107">Gibt die Anzahl der Kopien eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="cf471-107">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="cf471-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="cf471-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cf471-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="cf471-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="cf471-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="cf471-110">Element Information</span></span>



| <span data-ttu-id="cf471-111">Name</span><span class="sxs-lookup"><span data-stu-id="cf471-111">Name</span></span> | <span data-ttu-id="cf471-112">Wert</span><span class="sxs-lookup"><span data-stu-id="cf471-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="cf471-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="cf471-113">Element Type</span></span> <br/>   | <span data-ttu-id="cf471-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="cf471-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="cf471-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="cf471-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cf471-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="cf471-116">Job</span></span><br/>          |
| <span data-ttu-id="cf471-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cf471-117">Notes</span></span> <br/>          | <span data-ttu-id="cf471-118">Keine</span><span class="sxs-lookup"><span data-stu-id="cf471-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="cf471-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="cf471-119">Structure Content</span></span>

<span data-ttu-id="cf471-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="cf471-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="cf471-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="cf471-121">Structure Properties</span></span>

<span data-ttu-id="cf471-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="cf471-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cf471-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cf471-123">Property</span></span>                | <span data-ttu-id="cf471-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cf471-124">xsi:type</span></span>           | <span data-ttu-id="cf471-125">Wert</span><span class="sxs-lookup"><span data-stu-id="cf471-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="cf471-126">DataType</span><span class="sxs-lookup"><span data-stu-id="cf471-126">DataType</span></span><br/>     | <span data-ttu-id="cf471-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cf471-127">string</span></span><br/>  | <span data-ttu-id="cf471-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cf471-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="cf471-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cf471-129">DefaultValue</span></span><br/> | <span data-ttu-id="cf471-130">integer</span><span class="sxs-lookup"><span data-stu-id="cf471-130">integer</span></span><br/> | <span data-ttu-id="cf471-131">1</span><span class="sxs-lookup"><span data-stu-id="cf471-131">1</span></span><br/>                 |
| <span data-ttu-id="cf471-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="cf471-132">MaxValue</span></span><br/>     | <span data-ttu-id="cf471-133">integer</span><span class="sxs-lookup"><span data-stu-id="cf471-133">integer</span></span><br/> | <span data-ttu-id="cf471-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="cf471-134">undefined</span></span><br/>         |
| <span data-ttu-id="cf471-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="cf471-135">MinValue</span></span><br/>     | <span data-ttu-id="cf471-136">integer</span><span class="sxs-lookup"><span data-stu-id="cf471-136">integer</span></span><br/> | <span data-ttu-id="cf471-137">1</span><span class="sxs-lookup"><span data-stu-id="cf471-137">1</span></span><br/>                 |
| <span data-ttu-id="cf471-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cf471-138">Mandatory</span></span><br/>    | <span data-ttu-id="cf471-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cf471-139">string</span></span><br/>  | <span data-ttu-id="cf471-140">psk:Unconditional</span><span class="sxs-lookup"><span data-stu-id="cf471-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="cf471-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="cf471-141">Multiple</span></span><br/>     | <span data-ttu-id="cf471-142">integer</span><span class="sxs-lookup"><span data-stu-id="cf471-142">integer</span></span><br/> | <span data-ttu-id="cf471-143">1</span><span class="sxs-lookup"><span data-stu-id="cf471-143">1</span></span><br/>                 |
| <span data-ttu-id="cf471-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="cf471-144">UnitType</span></span><br/>     | <span data-ttu-id="cf471-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cf471-145">string</span></span><br/>  | <span data-ttu-id="cf471-146">Kopien</span><span class="sxs-lookup"><span data-stu-id="cf471-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="cf471-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cf471-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf471-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="cf471-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




