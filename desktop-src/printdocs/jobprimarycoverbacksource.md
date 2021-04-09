---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: Jobprimarycoverbacksource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c15d5f5b8545b70f19bf181a00d05a8379212
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050728"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="afc1f-104">Jobprimarycoverbacksource</span><span class="sxs-lookup"><span data-stu-id="afc1f-104">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="afc1f-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="afc1f-105">This topic is not current.</span></span> <span data-ttu-id="afc1f-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="afc1f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="afc1f-107">Gibt die Quelle für ein benutzerdefiniertes Back-Cover-primär Blatt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="afc1f-107">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="afc1f-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="afc1f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="afc1f-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="afc1f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="afc1f-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="afc1f-110">Element Information</span></span>



| <span data-ttu-id="afc1f-111">Name</span><span class="sxs-lookup"><span data-stu-id="afc1f-111">Name</span></span>                       |                                           |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="afc1f-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="afc1f-112">Element Type</span></span> <br/>   | <span data-ttu-id="afc1f-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="afc1f-113">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="afc1f-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="afc1f-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="afc1f-115">Auftrag</span><span class="sxs-lookup"><span data-stu-id="afc1f-115">Job</span></span><br/>                            |
| <span data-ttu-id="afc1f-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="afc1f-116">Notes</span></span> <br/>          | <span data-ttu-id="afc1f-117">Verknüpft mit jobcoverback-Element</span><span class="sxs-lookup"><span data-stu-id="afc1f-117">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="afc1f-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="afc1f-118">Structure Content</span></span>

<span data-ttu-id="afc1f-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="afc1f-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="afc1f-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="afc1f-120">Structure Properties</span></span>

<span data-ttu-id="afc1f-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="afc1f-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="afc1f-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="afc1f-122">Property</span></span>                | <span data-ttu-id="afc1f-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="afc1f-123">xsi:type</span></span>           | <span data-ttu-id="afc1f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="afc1f-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="afc1f-125">DataType</span><span class="sxs-lookup"><span data-stu-id="afc1f-125">DataType</span></span><br/>     | <span data-ttu-id="afc1f-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="afc1f-126">string</span></span><br/>  | <span data-ttu-id="afc1f-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="afc1f-127">xs:string</span></span><br/>       |
| <span data-ttu-id="afc1f-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="afc1f-128">DefaultValue</span></span><br/> | <span data-ttu-id="afc1f-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="afc1f-129">string</span></span><br/>  | <span data-ttu-id="afc1f-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="afc1f-130">undefined</span></span><br/>       |
| <span data-ttu-id="afc1f-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="afc1f-131">MaxLength</span></span><br/>    | <span data-ttu-id="afc1f-132">integer</span><span class="sxs-lookup"><span data-stu-id="afc1f-132">integer</span></span><br/> | <span data-ttu-id="afc1f-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="afc1f-133">undefined</span></span><br/>       |
| <span data-ttu-id="afc1f-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="afc1f-134">MinLength</span></span><br/>    | <span data-ttu-id="afc1f-135">integer</span><span class="sxs-lookup"><span data-stu-id="afc1f-135">integer</span></span><br/> | <span data-ttu-id="afc1f-136">1</span><span class="sxs-lookup"><span data-stu-id="afc1f-136">1</span></span><br/>               |
| <span data-ttu-id="afc1f-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="afc1f-137">Mandatory</span></span><br/>    | <span data-ttu-id="afc1f-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="afc1f-138">string</span></span><br/>  | <span data-ttu-id="afc1f-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="afc1f-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="afc1f-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="afc1f-140">UnitType</span></span><br/>     | <span data-ttu-id="afc1f-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="afc1f-141">string</span></span><br/>  | <span data-ttu-id="afc1f-142">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="afc1f-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="afc1f-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="afc1f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afc1f-144">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="afc1f-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




