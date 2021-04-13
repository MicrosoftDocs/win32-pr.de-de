---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ad33b2cd-8409-4782-8eb9-5f12aca8405b
title: Jobprimarybannersheetsource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c86e840c3507fce80bda0f4c31efe8b0d714242
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351878"
---
# <a name="jobprimarybannersheetsource"></a><span data-ttu-id="f93a3-104">Jobprimarybannersheetsource</span><span class="sxs-lookup"><span data-stu-id="f93a3-104">JobPrimaryBannerSheetSource</span></span>

<span data-ttu-id="f93a3-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="f93a3-105">This topic is not current.</span></span> <span data-ttu-id="f93a3-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f93a3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f93a3-107">Gibt die Quelle für ein primäres benutzerdefiniertes Banner Blatt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="f93a3-107">Specifies the source for a primary custom banner sheet for the job.</span></span>

-   [<span data-ttu-id="f93a3-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f93a3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f93a3-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="f93a3-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f93a3-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f93a3-110">Element Information</span></span>



| <span data-ttu-id="f93a3-111">Name</span><span class="sxs-lookup"><span data-stu-id="f93a3-111">Name</span></span>                       |                                             |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="f93a3-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="f93a3-112">Element Type</span></span> <br/>   | <span data-ttu-id="f93a3-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f93a3-113">ParameterDef</span></span><br/>                     |
| <span data-ttu-id="f93a3-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="f93a3-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f93a3-115">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f93a3-115">Job</span></span><br/>                              |
| <span data-ttu-id="f93a3-116">Notizen</span><span class="sxs-lookup"><span data-stu-id="f93a3-116">Notes</span></span> <br/>          | <span data-ttu-id="f93a3-117">Verknüpft mit jobbannersheet-Element</span><span class="sxs-lookup"><span data-stu-id="f93a3-117">Linked to JobBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f93a3-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="f93a3-118">Structure Content</span></span>

<span data-ttu-id="f93a3-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="f93a3-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f93a3-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f93a3-120">Structure Properties</span></span>

<span data-ttu-id="f93a3-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f93a3-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f93a3-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f93a3-122">Property</span></span>                | <span data-ttu-id="f93a3-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f93a3-123">xsi:type</span></span>           | <span data-ttu-id="f93a3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f93a3-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f93a3-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f93a3-125">DataType</span></span><br/>     | <span data-ttu-id="f93a3-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f93a3-126">string</span></span><br/>  | <span data-ttu-id="f93a3-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="f93a3-127">xs:string</span></span><br/>       |
| <span data-ttu-id="f93a3-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f93a3-128">DefaultValue</span></span><br/> | <span data-ttu-id="f93a3-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f93a3-129">string</span></span><br/>  | <span data-ttu-id="f93a3-130">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="f93a3-130">undefined</span></span><br/>       |
| <span data-ttu-id="f93a3-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="f93a3-131">MaxLength</span></span><br/>    | <span data-ttu-id="f93a3-132">integer</span><span class="sxs-lookup"><span data-stu-id="f93a3-132">integer</span></span><br/> | <span data-ttu-id="f93a3-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="f93a3-133">undefined</span></span><br/>       |
| <span data-ttu-id="f93a3-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="f93a3-134">MinLength</span></span><br/>    | <span data-ttu-id="f93a3-135">integer</span><span class="sxs-lookup"><span data-stu-id="f93a3-135">integer</span></span><br/> | <span data-ttu-id="f93a3-136">1</span><span class="sxs-lookup"><span data-stu-id="f93a3-136">1</span></span><br/>               |
| <span data-ttu-id="f93a3-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="f93a3-137">Mandatory</span></span><br/>    | <span data-ttu-id="f93a3-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f93a3-138">string</span></span><br/>  | <span data-ttu-id="f93a3-139">PSK: bedingt</span><span class="sxs-lookup"><span data-stu-id="f93a3-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f93a3-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="f93a3-140">UnitType</span></span><br/>     | <span data-ttu-id="f93a3-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f93a3-141">string</span></span><br/>  | <span data-ttu-id="f93a3-142">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="f93a3-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="f93a3-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f93a3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f93a3-144">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="f93a3-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




