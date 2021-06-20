---
description: Erfahren Sie mehr über das DocumentCoverBackSource-Element, das die Quelle für ein benutzerdefiniertes Hintergrundblatt angibt.
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: DocumentCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be16ab26a4aa3dd7109fee7d630ed354b9b686d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409353"
---
# <a name="documentcoverbacksource"></a><span data-ttu-id="4d6fe-103">DocumentCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="4d6fe-103">DocumentCoverBackSource</span></span>

<span data-ttu-id="4d6fe-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4d6fe-104">This topic is not current.</span></span> <span data-ttu-id="4d6fe-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="4d6fe-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4d6fe-106">Gibt die Quelle für ein benutzerdefiniertes Hintergrundblatt an.</span><span class="sxs-lookup"><span data-stu-id="4d6fe-106">Specifies the source for a custom back-cover sheet.</span></span>

-   [<span data-ttu-id="4d6fe-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4d6fe-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4d6fe-108">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4d6fe-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4d6fe-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4d6fe-109">Element Information</span></span>



| <span data-ttu-id="4d6fe-110">Name</span><span class="sxs-lookup"><span data-stu-id="4d6fe-110">Name</span></span> | <span data-ttu-id="4d6fe-111">Wert</span><span class="sxs-lookup"><span data-stu-id="4d6fe-111">Value</span></span> |
|----------------------------|------------------------------------------------|
| <span data-ttu-id="4d6fe-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4d6fe-112">Element Type</span></span> <br/>   | <span data-ttu-id="4d6fe-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4d6fe-113">ParameterDef</span></span><br/>                        |
| <span data-ttu-id="4d6fe-114">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="4d6fe-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4d6fe-115">Dokument</span><span class="sxs-lookup"><span data-stu-id="4d6fe-115">Document</span></span><br/>                            |
| <span data-ttu-id="4d6fe-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d6fe-116">Notes</span></span> <br/>          | <span data-ttu-id="4d6fe-117">Verknüpft mit dem DocumentCoverBack-Element</span><span class="sxs-lookup"><span data-stu-id="4d6fe-117">Linked to DocumentCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4d6fe-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4d6fe-118">Structure Content</span></span>

<span data-ttu-id="4d6fe-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="4d6fe-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverBackSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a><span data-ttu-id="4d6fe-120">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d6fe-120">Structure Properties</span></span>

<span data-ttu-id="4d6fe-121">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4d6fe-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4d6fe-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d6fe-122">Property</span></span>                | <span data-ttu-id="4d6fe-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4d6fe-123">xsi:type</span></span>           | <span data-ttu-id="4d6fe-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4d6fe-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4d6fe-125">DataType</span><span class="sxs-lookup"><span data-stu-id="4d6fe-125">DataType</span></span><br/>     | <span data-ttu-id="4d6fe-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4d6fe-126">string</span></span><br/>  | <span data-ttu-id="4d6fe-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="4d6fe-127">xs:string</span></span><br/>       |
| <span data-ttu-id="4d6fe-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4d6fe-128">DefaultValue</span></span><br/> | <span data-ttu-id="4d6fe-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4d6fe-129">string</span></span><br/>  | <span data-ttu-id="4d6fe-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4d6fe-130">undefined</span></span><br/>       |
| <span data-ttu-id="4d6fe-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="4d6fe-131">MaxLength</span></span><br/>    | <span data-ttu-id="4d6fe-132">integer</span><span class="sxs-lookup"><span data-stu-id="4d6fe-132">integer</span></span><br/> | <span data-ttu-id="4d6fe-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="4d6fe-133">undefined</span></span><br/>       |
| <span data-ttu-id="4d6fe-134">Minlength</span><span class="sxs-lookup"><span data-stu-id="4d6fe-134">MinLength</span></span><br/>    | <span data-ttu-id="4d6fe-135">integer</span><span class="sxs-lookup"><span data-stu-id="4d6fe-135">integer</span></span><br/> | <span data-ttu-id="4d6fe-136">1</span><span class="sxs-lookup"><span data-stu-id="4d6fe-136">1</span></span><br/>               |
| <span data-ttu-id="4d6fe-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="4d6fe-137">Mandatory</span></span><br/>    | <span data-ttu-id="4d6fe-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4d6fe-138">string</span></span><br/>  | <span data-ttu-id="4d6fe-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="4d6fe-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4d6fe-140">Unittype</span><span class="sxs-lookup"><span data-stu-id="4d6fe-140">UnitType</span></span><br/>     | <span data-ttu-id="4d6fe-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4d6fe-141">string</span></span><br/>  | <span data-ttu-id="4d6fe-142">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="4d6fe-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="4d6fe-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d6fe-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d6fe-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="4d6fe-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




