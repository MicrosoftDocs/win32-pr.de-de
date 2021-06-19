---
description: Lesen Sie Referenzinformationen zum PageCopies-Parameter. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5002850fa1df5a86b0022a941e3b2a1f7e414a44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396685"
---
# <a name="pagecopies"></a><span data-ttu-id="001ee-105">PageCopies</span><span class="sxs-lookup"><span data-stu-id="001ee-105">PageCopies</span></span>

<span data-ttu-id="001ee-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="001ee-106">This topic is not current.</span></span> <span data-ttu-id="001ee-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="001ee-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="001ee-108">Gibt die Anzahl der Kopien einer Seite an.</span><span class="sxs-lookup"><span data-stu-id="001ee-108">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="001ee-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="001ee-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="001ee-110">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="001ee-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="001ee-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="001ee-111">Element Information</span></span>



| <span data-ttu-id="001ee-112">Name</span><span class="sxs-lookup"><span data-stu-id="001ee-112">Name</span></span> | <span data-ttu-id="001ee-113">Wert</span><span class="sxs-lookup"><span data-stu-id="001ee-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="001ee-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="001ee-114">Element Type</span></span> <br/>   | <span data-ttu-id="001ee-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="001ee-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="001ee-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="001ee-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="001ee-117">Seite</span><span class="sxs-lookup"><span data-stu-id="001ee-117">Page</span></span><br/>         |
| <span data-ttu-id="001ee-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="001ee-118">Notes</span></span> <br/>          | <span data-ttu-id="001ee-119">Keine</span><span class="sxs-lookup"><span data-stu-id="001ee-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="001ee-120">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="001ee-120">Structure Content</span></span>

<span data-ttu-id="001ee-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="001ee-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
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

## <a name="structure-properties"></a><span data-ttu-id="001ee-122">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="001ee-122">Structure Properties</span></span>

<span data-ttu-id="001ee-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="001ee-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="001ee-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="001ee-124">Property</span></span>                | <span data-ttu-id="001ee-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="001ee-125">xsi:type</span></span>           | <span data-ttu-id="001ee-126">Wert</span><span class="sxs-lookup"><span data-stu-id="001ee-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="001ee-127">DataType</span><span class="sxs-lookup"><span data-stu-id="001ee-127">DataType</span></span><br/>     | <span data-ttu-id="001ee-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="001ee-128">string</span></span><br/>  | <span data-ttu-id="001ee-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="001ee-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="001ee-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="001ee-130">DefaultValue</span></span><br/> | <span data-ttu-id="001ee-131">integer</span><span class="sxs-lookup"><span data-stu-id="001ee-131">integer</span></span><br/> | <span data-ttu-id="001ee-132">1</span><span class="sxs-lookup"><span data-stu-id="001ee-132">1</span></span><br/>                 |
| <span data-ttu-id="001ee-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="001ee-133">MaxValue</span></span><br/>     | <span data-ttu-id="001ee-134">integer</span><span class="sxs-lookup"><span data-stu-id="001ee-134">integer</span></span><br/> | <span data-ttu-id="001ee-135">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="001ee-135">undefined</span></span><br/>         |
| <span data-ttu-id="001ee-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="001ee-136">MinValue</span></span><br/>     | <span data-ttu-id="001ee-137">integer</span><span class="sxs-lookup"><span data-stu-id="001ee-137">integer</span></span><br/> | <span data-ttu-id="001ee-138">1</span><span class="sxs-lookup"><span data-stu-id="001ee-138">1</span></span><br/>                 |
| <span data-ttu-id="001ee-139">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="001ee-139">Mandatory</span></span><br/>    | <span data-ttu-id="001ee-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="001ee-140">string</span></span><br/>  | <span data-ttu-id="001ee-141">psk:Bedingungslos</span><span class="sxs-lookup"><span data-stu-id="001ee-141">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="001ee-142">Mehrere</span><span class="sxs-lookup"><span data-stu-id="001ee-142">Multiple</span></span><br/>     | <span data-ttu-id="001ee-143">integer</span><span class="sxs-lookup"><span data-stu-id="001ee-143">integer</span></span><br/> | <span data-ttu-id="001ee-144">1</span><span class="sxs-lookup"><span data-stu-id="001ee-144">1</span></span><br/>                 |
| <span data-ttu-id="001ee-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="001ee-145">UnitType</span></span><br/>     | <span data-ttu-id="001ee-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="001ee-146">string</span></span><br/>  | <span data-ttu-id="001ee-147">Kopien</span><span class="sxs-lookup"><span data-stu-id="001ee-147">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="001ee-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="001ee-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="001ee-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="001ee-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




