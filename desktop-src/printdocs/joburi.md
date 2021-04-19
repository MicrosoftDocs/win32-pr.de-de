---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: Joburi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb06148438b0fd6715370c56ff9efe54d512219
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355116"
---
# <a name="joburi"></a><span data-ttu-id="6a31a-104">Joburi</span><span class="sxs-lookup"><span data-stu-id="6a31a-104">JobURI</span></span>

<span data-ttu-id="6a31a-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="6a31a-105">This topic is not current.</span></span> <span data-ttu-id="6a31a-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6a31a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6a31a-107">Gibt einen URI (Uniform Resource Identifier) für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="6a31a-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="6a31a-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6a31a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6a31a-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="6a31a-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6a31a-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6a31a-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6a31a-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6a31a-111">Element Information</span></span>



| <span data-ttu-id="6a31a-112">Name</span><span class="sxs-lookup"><span data-stu-id="6a31a-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="6a31a-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="6a31a-113">Element Type</span></span> <br/>   | <span data-ttu-id="6a31a-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a31a-114">Property</span></span><br/> |
| <span data-ttu-id="6a31a-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="6a31a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6a31a-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6a31a-116">Job</span></span><br/>      |
| <span data-ttu-id="6a31a-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a31a-117">Notes</span></span> <br/>          | <span data-ttu-id="6a31a-118">Keine</span><span class="sxs-lookup"><span data-stu-id="6a31a-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="6a31a-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="6a31a-119">Structural Content</span></span>

<span data-ttu-id="6a31a-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6a31a-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="6a31a-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="6a31a-121">Structure Variables</span></span>

<span data-ttu-id="6a31a-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="6a31a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6a31a-123">Name</span><span class="sxs-lookup"><span data-stu-id="6a31a-123">Name</span></span>                       | <span data-ttu-id="6a31a-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6a31a-124">Data type</span></span>         | <span data-ttu-id="6a31a-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="6a31a-125">Unit</span></span> | <span data-ttu-id="6a31a-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="6a31a-126">Supported values</span></span> | <span data-ttu-id="6a31a-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6a31a-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="6a31a-128">\_Joburivalue\_</span><span class="sxs-lookup"><span data-stu-id="6a31a-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="6a31a-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6a31a-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6a31a-130">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6a31a-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="6a31a-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a31a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a31a-132">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="6a31a-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




