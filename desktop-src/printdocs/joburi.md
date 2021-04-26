---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c80611a4e7dbd10f4841fae098578f0a8fdc96
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993887"
---
# <a name="joburi"></a><span data-ttu-id="b51e7-104">JobURI</span><span class="sxs-lookup"><span data-stu-id="b51e7-104">JobURI</span></span>

<span data-ttu-id="b51e7-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="b51e7-105">This topic is not current.</span></span> <span data-ttu-id="b51e7-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="b51e7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b51e7-107">Gibt einen URI (Uniform Resource Identifier) für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="b51e7-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="b51e7-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b51e7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b51e7-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="b51e7-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b51e7-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="b51e7-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b51e7-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b51e7-111">Element Information</span></span>



| <span data-ttu-id="b51e7-112">Name</span><span class="sxs-lookup"><span data-stu-id="b51e7-112">Name</span></span> | <span data-ttu-id="b51e7-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b51e7-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="b51e7-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="b51e7-114">Element Type</span></span> <br/>   | <span data-ttu-id="b51e7-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b51e7-115">Property</span></span><br/> |
| <span data-ttu-id="b51e7-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="b51e7-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b51e7-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="b51e7-117">Job</span></span><br/>      |
| <span data-ttu-id="b51e7-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b51e7-118">Notes</span></span> <br/>          | <span data-ttu-id="b51e7-119">Keine</span><span class="sxs-lookup"><span data-stu-id="b51e7-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="b51e7-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="b51e7-120">Structural Content</span></span>

<span data-ttu-id="b51e7-121">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b51e7-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="b51e7-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="b51e7-122">Structure Variables</span></span>

<span data-ttu-id="b51e7-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b51e7-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b51e7-124">Name</span><span class="sxs-lookup"><span data-stu-id="b51e7-124">Name</span></span>                       | <span data-ttu-id="b51e7-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b51e7-125">Data type</span></span>         | <span data-ttu-id="b51e7-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="b51e7-126">Unit</span></span> | <span data-ttu-id="b51e7-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="b51e7-127">Supported values</span></span> | <span data-ttu-id="b51e7-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b51e7-128">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="b51e7-129">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="b51e7-129">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="b51e7-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b51e7-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b51e7-131">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="b51e7-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="b51e7-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b51e7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b51e7-133">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="b51e7-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




