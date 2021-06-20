---
description: Erfahren Sie mehr über das JobID-Element, das eine eindeutige ID für den Auftrag angibt. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfd17d068f34b56d45e4851c06b7ed1d9bd6fcc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408883"
---
# <a name="jobid"></a><span data-ttu-id="f8e77-104">JobID</span><span class="sxs-lookup"><span data-stu-id="f8e77-104">JobID</span></span>

<span data-ttu-id="f8e77-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="f8e77-105">This topic is not current.</span></span> <span data-ttu-id="f8e77-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="f8e77-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f8e77-107">Gibt eine eindeutige ID für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="f8e77-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="f8e77-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f8e77-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f8e77-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="f8e77-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f8e77-110">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="f8e77-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f8e77-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f8e77-111">Element Information</span></span>



| <span data-ttu-id="f8e77-112">Name</span><span class="sxs-lookup"><span data-stu-id="f8e77-112">Name</span></span> | <span data-ttu-id="f8e77-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f8e77-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="f8e77-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="f8e77-114">Element Type</span></span> <br/>   | <span data-ttu-id="f8e77-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f8e77-115">Property</span></span><br/> |
| <span data-ttu-id="f8e77-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="f8e77-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f8e77-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f8e77-117">Job</span></span><br/>      |
| <span data-ttu-id="f8e77-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8e77-118">Notes</span></span> <br/>          | <span data-ttu-id="f8e77-119">Keine</span><span class="sxs-lookup"><span data-stu-id="f8e77-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="f8e77-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="f8e77-120">Structural Content</span></span>

<span data-ttu-id="f8e77-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="f8e77-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="f8e77-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="f8e77-122">Structure Variables</span></span>

<span data-ttu-id="f8e77-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f8e77-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f8e77-124">Name</span><span class="sxs-lookup"><span data-stu-id="f8e77-124">Name</span></span>                      | <span data-ttu-id="f8e77-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f8e77-125">Data type</span></span>         | <span data-ttu-id="f8e77-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="f8e77-126">Unit</span></span> | <span data-ttu-id="f8e77-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="f8e77-127">Supported values</span></span> | <span data-ttu-id="f8e77-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f8e77-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="f8e77-129">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="f8e77-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="f8e77-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f8e77-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f8e77-131">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="f8e77-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="f8e77-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8e77-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8e77-133">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="f8e77-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




