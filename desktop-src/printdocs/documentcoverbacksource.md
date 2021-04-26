---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: DocumentCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6547ac2dc2c3f91ea4d0ebeea87622c790ae7d4d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996277"
---
# <a name="documentcoverbacksource"></a><span data-ttu-id="fe841-104">DocumentCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="fe841-104">DocumentCoverBackSource</span></span>

<span data-ttu-id="fe841-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="fe841-105">This topic is not current.</span></span> <span data-ttu-id="fe841-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="fe841-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fe841-107">Gibt die Quelle für ein benutzerdefiniertes Hintergrundblatt an.</span><span class="sxs-lookup"><span data-stu-id="fe841-107">Specifies the source for a custom back-cover sheet.</span></span>

-   [<span data-ttu-id="fe841-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fe841-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fe841-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="fe841-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fe841-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fe841-110">Element Information</span></span>



| <span data-ttu-id="fe841-111">Name</span><span class="sxs-lookup"><span data-stu-id="fe841-111">Name</span></span> | <span data-ttu-id="fe841-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fe841-112">Value</span></span> |
|----------------------------|------------------------------------------------|
| <span data-ttu-id="fe841-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="fe841-113">Element Type</span></span> <br/>   | <span data-ttu-id="fe841-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fe841-114">ParameterDef</span></span><br/>                        |
| <span data-ttu-id="fe841-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="fe841-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fe841-116">Dokument</span><span class="sxs-lookup"><span data-stu-id="fe841-116">Document</span></span><br/>                            |
| <span data-ttu-id="fe841-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe841-117">Notes</span></span> <br/>          | <span data-ttu-id="fe841-118">Mit DocumentCoverBack-Element verknüpft</span><span class="sxs-lookup"><span data-stu-id="fe841-118">Linked to DocumentCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fe841-119">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="fe841-119">Structure Content</span></span>

<span data-ttu-id="fe841-120">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="fe841-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="fe841-121">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe841-121">Structure Properties</span></span>

<span data-ttu-id="fe841-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="fe841-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fe841-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fe841-123">Property</span></span>                | <span data-ttu-id="fe841-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fe841-124">xsi:type</span></span>           | <span data-ttu-id="fe841-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fe841-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fe841-126">DataType</span><span class="sxs-lookup"><span data-stu-id="fe841-126">DataType</span></span><br/>     | <span data-ttu-id="fe841-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe841-127">string</span></span><br/>  | <span data-ttu-id="fe841-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe841-128">xs:string</span></span><br/>       |
| <span data-ttu-id="fe841-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fe841-129">DefaultValue</span></span><br/> | <span data-ttu-id="fe841-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe841-130">string</span></span><br/>  | <span data-ttu-id="fe841-131">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="fe841-131">undefined</span></span><br/>       |
| <span data-ttu-id="fe841-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="fe841-132">MaxLength</span></span><br/>    | <span data-ttu-id="fe841-133">integer</span><span class="sxs-lookup"><span data-stu-id="fe841-133">integer</span></span><br/> | <span data-ttu-id="fe841-134">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="fe841-134">undefined</span></span><br/>       |
| <span data-ttu-id="fe841-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="fe841-135">MinLength</span></span><br/>    | <span data-ttu-id="fe841-136">integer</span><span class="sxs-lookup"><span data-stu-id="fe841-136">integer</span></span><br/> | <span data-ttu-id="fe841-137">1</span><span class="sxs-lookup"><span data-stu-id="fe841-137">1</span></span><br/>               |
| <span data-ttu-id="fe841-138">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="fe841-138">Mandatory</span></span><br/>    | <span data-ttu-id="fe841-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe841-139">string</span></span><br/>  | <span data-ttu-id="fe841-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="fe841-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fe841-141">Unittype</span><span class="sxs-lookup"><span data-stu-id="fe841-141">UnitType</span></span><br/>     | <span data-ttu-id="fe841-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe841-142">string</span></span><br/>  | <span data-ttu-id="fe841-143">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="fe841-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="fe841-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe841-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe841-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="fe841-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




