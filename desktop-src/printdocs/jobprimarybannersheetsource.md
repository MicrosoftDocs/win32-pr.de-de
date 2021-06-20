---
description: Erfahren Sie mehr über das JobPrimaryBannerSheetSource-Element, das die Quelle für ein primäres benutzerdefiniertes Bannerblatt für den Auftrag angibt.
ms.assetid: ad33b2cd-8409-4782-8eb9-5f12aca8405b
title: JobPrimaryBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366266576fca98762fd7d3dcb7e491a6cc94f529
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408713"
---
# <a name="jobprimarybannersheetsource"></a><span data-ttu-id="439dc-103">JobPrimaryBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="439dc-103">JobPrimaryBannerSheetSource</span></span>

<span data-ttu-id="439dc-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="439dc-104">This topic is not current.</span></span> <span data-ttu-id="439dc-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="439dc-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="439dc-106">Gibt die Quelle für ein primäres benutzerdefiniertes Bannerblatt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="439dc-106">Specifies the source for a primary custom banner sheet for the job.</span></span>

-   [<span data-ttu-id="439dc-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="439dc-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="439dc-108">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="439dc-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="439dc-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="439dc-109">Element Information</span></span>



| <span data-ttu-id="439dc-110">Name</span><span class="sxs-lookup"><span data-stu-id="439dc-110">Name</span></span> | <span data-ttu-id="439dc-111">Wert</span><span class="sxs-lookup"><span data-stu-id="439dc-111">Value</span></span> |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="439dc-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="439dc-112">Element Type</span></span> <br/>   | <span data-ttu-id="439dc-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="439dc-113">ParameterDef</span></span><br/>                     |
| <span data-ttu-id="439dc-114">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="439dc-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="439dc-115">Auftrag</span><span class="sxs-lookup"><span data-stu-id="439dc-115">Job</span></span><br/>                              |
| <span data-ttu-id="439dc-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="439dc-116">Notes</span></span> <br/>          | <span data-ttu-id="439dc-117">Verknüpft mit dem JobBannerSheet-Element</span><span class="sxs-lookup"><span data-stu-id="439dc-117">Linked to JobBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="439dc-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="439dc-118">Structure Content</span></span>

<span data-ttu-id="439dc-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="439dc-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryBannerSheetSource">
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

## <a name="structure-properties"></a><span data-ttu-id="439dc-120">Struktureigenschaften</span><span class="sxs-lookup"><span data-stu-id="439dc-120">Structure Properties</span></span>

<span data-ttu-id="439dc-121">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="439dc-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="439dc-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="439dc-122">Property</span></span>                | <span data-ttu-id="439dc-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="439dc-123">xsi:type</span></span>           | <span data-ttu-id="439dc-124">Wert</span><span class="sxs-lookup"><span data-stu-id="439dc-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="439dc-125">DataType</span><span class="sxs-lookup"><span data-stu-id="439dc-125">DataType</span></span><br/>     | <span data-ttu-id="439dc-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="439dc-126">string</span></span><br/>  | <span data-ttu-id="439dc-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="439dc-127">xs:string</span></span><br/>       |
| <span data-ttu-id="439dc-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="439dc-128">DefaultValue</span></span><br/> | <span data-ttu-id="439dc-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="439dc-129">string</span></span><br/>  | <span data-ttu-id="439dc-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="439dc-130">undefined</span></span><br/>       |
| <span data-ttu-id="439dc-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="439dc-131">MaxLength</span></span><br/>    | <span data-ttu-id="439dc-132">integer</span><span class="sxs-lookup"><span data-stu-id="439dc-132">integer</span></span><br/> | <span data-ttu-id="439dc-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="439dc-133">undefined</span></span><br/>       |
| <span data-ttu-id="439dc-134">Minlength</span><span class="sxs-lookup"><span data-stu-id="439dc-134">MinLength</span></span><br/>    | <span data-ttu-id="439dc-135">integer</span><span class="sxs-lookup"><span data-stu-id="439dc-135">integer</span></span><br/> | <span data-ttu-id="439dc-136">1</span><span class="sxs-lookup"><span data-stu-id="439dc-136">1</span></span><br/>               |
| <span data-ttu-id="439dc-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="439dc-137">Mandatory</span></span><br/>    | <span data-ttu-id="439dc-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="439dc-138">string</span></span><br/>  | <span data-ttu-id="439dc-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="439dc-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="439dc-140">Unittype</span><span class="sxs-lookup"><span data-stu-id="439dc-140">UnitType</span></span><br/>     | <span data-ttu-id="439dc-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="439dc-141">string</span></span><br/>  | <span data-ttu-id="439dc-142">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="439dc-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="439dc-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="439dc-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="439dc-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="439dc-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




