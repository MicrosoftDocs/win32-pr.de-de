---
description: Erfahren Sie mehr über das JobURI-Element, das einen URI (Uniform Resource Identifier) für das Dokument angibt.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc145ac9a393c09ecab762b84e9ac7d58870ddf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408613"
---
# <a name="joburi"></a><span data-ttu-id="e9ad9-103">JobURI</span><span class="sxs-lookup"><span data-stu-id="e9ad9-103">JobURI</span></span>

<span data-ttu-id="e9ad9-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e9ad9-104">This topic is not current.</span></span> <span data-ttu-id="e9ad9-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="e9ad9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e9ad9-106">Gibt einen URI (Uniform Resource Identifier) für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="e9ad9-106">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="e9ad9-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e9ad9-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e9ad9-108">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="e9ad9-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e9ad9-109">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="e9ad9-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e9ad9-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e9ad9-110">Element Information</span></span>



| <span data-ttu-id="e9ad9-111">Name</span><span class="sxs-lookup"><span data-stu-id="e9ad9-111">Name</span></span> | <span data-ttu-id="e9ad9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e9ad9-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="e9ad9-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e9ad9-113">Element Type</span></span> <br/>   | <span data-ttu-id="e9ad9-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e9ad9-114">Property</span></span><br/> |
| <span data-ttu-id="e9ad9-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="e9ad9-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e9ad9-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e9ad9-116">Job</span></span><br/>      |
| <span data-ttu-id="e9ad9-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e9ad9-117">Notes</span></span> <br/>          | <span data-ttu-id="e9ad9-118">Keine</span><span class="sxs-lookup"><span data-stu-id="e9ad9-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="e9ad9-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="e9ad9-119">Structural Content</span></span>

<span data-ttu-id="e9ad9-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e9ad9-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="e9ad9-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="e9ad9-121">Structure Variables</span></span>

<span data-ttu-id="e9ad9-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e9ad9-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e9ad9-123">Name</span><span class="sxs-lookup"><span data-stu-id="e9ad9-123">Name</span></span>                       | <span data-ttu-id="e9ad9-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e9ad9-124">Data type</span></span>         | <span data-ttu-id="e9ad9-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="e9ad9-125">Unit</span></span> | <span data-ttu-id="e9ad9-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="e9ad9-126">Supported values</span></span> | <span data-ttu-id="e9ad9-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e9ad9-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="e9ad9-128">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="e9ad9-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="e9ad9-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e9ad9-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e9ad9-130">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="e9ad9-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="e9ad9-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9ad9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9ad9-132">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="e9ad9-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




