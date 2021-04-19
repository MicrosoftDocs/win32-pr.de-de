---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161801e56a27e33cdf921cc07c93e59836d4dd90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106350596"
---
# <a name="jobname"></a><span data-ttu-id="f784c-104">JobName</span><span class="sxs-lookup"><span data-stu-id="f784c-104">JobName</span></span>

<span data-ttu-id="f784c-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="f784c-105">This topic is not current.</span></span> <span data-ttu-id="f784c-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f784c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f784c-107">Gibt einen beschreibenden Namen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="f784c-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="f784c-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f784c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f784c-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="f784c-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f784c-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="f784c-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f784c-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f784c-111">Element Information</span></span>



| <span data-ttu-id="f784c-112">Name</span><span class="sxs-lookup"><span data-stu-id="f784c-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="f784c-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="f784c-113">Element Type</span></span> <br/>   | <span data-ttu-id="f784c-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f784c-114">Property</span></span><br/> |
| <span data-ttu-id="f784c-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="f784c-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f784c-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="f784c-116">Job</span></span><br/>      |
| <span data-ttu-id="f784c-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f784c-117">Notes</span></span> <br/>          | <span data-ttu-id="f784c-118">Keine</span><span class="sxs-lookup"><span data-stu-id="f784c-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="f784c-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="f784c-119">Structural Content</span></span>

<span data-ttu-id="f784c-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f784c-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="f784c-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="f784c-121">Structure Variables</span></span>

<span data-ttu-id="f784c-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f784c-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f784c-123">Name</span><span class="sxs-lookup"><span data-stu-id="f784c-123">Name</span></span>                        | <span data-ttu-id="f784c-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f784c-124">Data type</span></span>         | <span data-ttu-id="f784c-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="f784c-125">Unit</span></span> | <span data-ttu-id="f784c-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="f784c-126">Supported values</span></span> | <span data-ttu-id="f784c-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f784c-127">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="f784c-128">\_Jobnamevalue\_</span><span class="sxs-lookup"><span data-stu-id="f784c-128">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="f784c-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f784c-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f784c-130">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="f784c-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="f784c-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f784c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f784c-132">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="f784c-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




