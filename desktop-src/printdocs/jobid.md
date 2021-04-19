---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c182e5d0bfcfb395eb553570cca745b618fc56b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353272"
---
# <a name="jobid"></a><span data-ttu-id="499d0-104">JobID</span><span class="sxs-lookup"><span data-stu-id="499d0-104">JobID</span></span>

<span data-ttu-id="499d0-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="499d0-105">This topic is not current.</span></span> <span data-ttu-id="499d0-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="499d0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="499d0-107">Gibt eine eindeutige ID für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="499d0-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="499d0-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="499d0-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="499d0-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="499d0-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="499d0-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="499d0-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="499d0-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="499d0-111">Element Information</span></span>



| <span data-ttu-id="499d0-112">Name</span><span class="sxs-lookup"><span data-stu-id="499d0-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="499d0-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="499d0-113">Element Type</span></span> <br/>   | <span data-ttu-id="499d0-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="499d0-114">Property</span></span><br/> |
| <span data-ttu-id="499d0-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="499d0-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="499d0-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="499d0-116">Job</span></span><br/>      |
| <span data-ttu-id="499d0-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="499d0-117">Notes</span></span> <br/>          | <span data-ttu-id="499d0-118">Keine</span><span class="sxs-lookup"><span data-stu-id="499d0-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="499d0-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="499d0-119">Structural Content</span></span>

<span data-ttu-id="499d0-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="499d0-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="499d0-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="499d0-121">Structure Variables</span></span>

<span data-ttu-id="499d0-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="499d0-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="499d0-123">Name</span><span class="sxs-lookup"><span data-stu-id="499d0-123">Name</span></span>                      | <span data-ttu-id="499d0-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="499d0-124">Data type</span></span>         | <span data-ttu-id="499d0-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="499d0-125">Unit</span></span> | <span data-ttu-id="499d0-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="499d0-126">Supported values</span></span> | <span data-ttu-id="499d0-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="499d0-127">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="499d0-128">\_Jobidvalue\_</span><span class="sxs-lookup"><span data-stu-id="499d0-128">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="499d0-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="499d0-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="499d0-130">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="499d0-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="499d0-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="499d0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="499d0-132">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="499d0-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




