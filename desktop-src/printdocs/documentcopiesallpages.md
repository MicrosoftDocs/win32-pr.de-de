---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: DocumentCopiesAllPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723242ddd127113b573f167e6902b27fcca9665a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993987"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="ee197-104">DocumentCopiesAllPages</span><span class="sxs-lookup"><span data-stu-id="ee197-104">DocumentCopiesAllPages</span></span>

<span data-ttu-id="ee197-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ee197-105">This topic is not current.</span></span> <span data-ttu-id="ee197-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="ee197-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ee197-107">Gibt die Anzahl der Kopien eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="ee197-107">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="ee197-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ee197-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ee197-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ee197-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ee197-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ee197-110">Element Information</span></span>



| <span data-ttu-id="ee197-111">Name</span><span class="sxs-lookup"><span data-stu-id="ee197-111">Name</span></span> | <span data-ttu-id="ee197-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ee197-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="ee197-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ee197-113">Element Type</span></span> <br/>   | <span data-ttu-id="ee197-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ee197-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="ee197-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="ee197-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ee197-116">Dokument</span><span class="sxs-lookup"><span data-stu-id="ee197-116">Document</span></span><br/>     |
| <span data-ttu-id="ee197-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee197-117">Notes</span></span> <br/>          | <span data-ttu-id="ee197-118">Keine</span><span class="sxs-lookup"><span data-stu-id="ee197-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="ee197-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ee197-119">Structure Content</span></span>

<span data-ttu-id="ee197-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="ee197-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="ee197-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee197-121">Structure Properties</span></span>

<span data-ttu-id="ee197-122">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee197-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ee197-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ee197-123">Property</span></span>                | <span data-ttu-id="ee197-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ee197-124">xsi:type</span></span>           | <span data-ttu-id="ee197-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ee197-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="ee197-126">DataType</span><span class="sxs-lookup"><span data-stu-id="ee197-126">DataType</span></span><br/>     | <span data-ttu-id="ee197-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ee197-127">string</span></span><br/>  | <span data-ttu-id="ee197-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ee197-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="ee197-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ee197-129">DefaultValue</span></span><br/> | <span data-ttu-id="ee197-130">integer</span><span class="sxs-lookup"><span data-stu-id="ee197-130">integer</span></span><br/> | <span data-ttu-id="ee197-131">1</span><span class="sxs-lookup"><span data-stu-id="ee197-131">1</span></span><br/>                 |
| <span data-ttu-id="ee197-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ee197-132">MaxValue</span></span><br/>     | <span data-ttu-id="ee197-133">integer</span><span class="sxs-lookup"><span data-stu-id="ee197-133">integer</span></span><br/> | <span data-ttu-id="ee197-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ee197-134">undefined</span></span><br/>         |
| <span data-ttu-id="ee197-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="ee197-135">MinValue</span></span><br/>     | <span data-ttu-id="ee197-136">integer</span><span class="sxs-lookup"><span data-stu-id="ee197-136">integer</span></span><br/> | <span data-ttu-id="ee197-137">1</span><span class="sxs-lookup"><span data-stu-id="ee197-137">1</span></span><br/>                 |
| <span data-ttu-id="ee197-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ee197-138">Mandatory</span></span><br/>    | <span data-ttu-id="ee197-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ee197-139">string</span></span><br/>  | <span data-ttu-id="ee197-140">psk:Bedingungslos</span><span class="sxs-lookup"><span data-stu-id="ee197-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="ee197-141">Mehrere</span><span class="sxs-lookup"><span data-stu-id="ee197-141">Multiple</span></span><br/>     | <span data-ttu-id="ee197-142">integer</span><span class="sxs-lookup"><span data-stu-id="ee197-142">integer</span></span><br/> | <span data-ttu-id="ee197-143">1</span><span class="sxs-lookup"><span data-stu-id="ee197-143">1</span></span><br/>                 |
| <span data-ttu-id="ee197-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="ee197-144">UnitType</span></span><br/>     | <span data-ttu-id="ee197-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ee197-145">string</span></span><br/>  | <span data-ttu-id="ee197-146">Kopien</span><span class="sxs-lookup"><span data-stu-id="ee197-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="ee197-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee197-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee197-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="ee197-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




