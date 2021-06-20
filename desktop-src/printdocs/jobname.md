---
description: Erfahren Sie mehr über das JobName-Element, das einen beschreibenden Namen für den Auftrag angibt. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfb63a54e9501ff5dc45ff09a925396c168b20c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408873"
---
# <a name="jobname"></a><span data-ttu-id="2cabf-104">JobName</span><span class="sxs-lookup"><span data-stu-id="2cabf-104">JobName</span></span>

<span data-ttu-id="2cabf-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="2cabf-105">This topic is not current.</span></span> <span data-ttu-id="2cabf-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="2cabf-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2cabf-107">Gibt einen beschreibenden Namen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="2cabf-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="2cabf-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2cabf-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2cabf-109">Strukturell</span><span class="sxs-lookup"><span data-stu-id="2cabf-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2cabf-110">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="2cabf-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2cabf-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2cabf-111">Element Information</span></span>



| <span data-ttu-id="2cabf-112">Name</span><span class="sxs-lookup"><span data-stu-id="2cabf-112">Name</span></span> | <span data-ttu-id="2cabf-113">Wert</span><span class="sxs-lookup"><span data-stu-id="2cabf-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="2cabf-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="2cabf-114">Element Type</span></span> <br/>   | <span data-ttu-id="2cabf-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2cabf-115">Property</span></span><br/> |
| <span data-ttu-id="2cabf-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="2cabf-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2cabf-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="2cabf-117">Job</span></span><br/>      |
| <span data-ttu-id="2cabf-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2cabf-118">Notes</span></span> <br/>          | <span data-ttu-id="2cabf-119">Keine</span><span class="sxs-lookup"><span data-stu-id="2cabf-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="2cabf-120">Strukturell</span><span class="sxs-lookup"><span data-stu-id="2cabf-120">Structural Content</span></span>

<span data-ttu-id="2cabf-121">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="2cabf-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="2cabf-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="2cabf-122">Structure Variables</span></span>

<span data-ttu-id="2cabf-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2cabf-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2cabf-124">Name</span><span class="sxs-lookup"><span data-stu-id="2cabf-124">Name</span></span>                        | <span data-ttu-id="2cabf-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2cabf-125">Data type</span></span>         | <span data-ttu-id="2cabf-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="2cabf-126">Unit</span></span> | <span data-ttu-id="2cabf-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="2cabf-127">Supported values</span></span> | <span data-ttu-id="2cabf-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2cabf-128">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="2cabf-129">\_JobNameValue\_</span><span class="sxs-lookup"><span data-stu-id="2cabf-129">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="2cabf-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2cabf-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2cabf-131">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="2cabf-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="2cabf-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2cabf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cabf-133">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="2cabf-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




