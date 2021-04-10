---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: Documenturi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9964df145e75fe2b30d670d5575928485e00c5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961259"
---
# <a name="documenturi"></a><span data-ttu-id="24883-104">Documenturi</span><span class="sxs-lookup"><span data-stu-id="24883-104">DocumentURI</span></span>

<span data-ttu-id="24883-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="24883-105">This topic is not current.</span></span> <span data-ttu-id="24883-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="24883-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="24883-107">Gibt einen URI (Uniform Resource Identifier) für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="24883-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="24883-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="24883-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="24883-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="24883-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="24883-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="24883-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="24883-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="24883-111">Element Information</span></span>



| <span data-ttu-id="24883-112">Name</span><span class="sxs-lookup"><span data-stu-id="24883-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="24883-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="24883-113">Element Type</span></span> <br/>   | <span data-ttu-id="24883-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="24883-114">Property</span></span><br/> |
| <span data-ttu-id="24883-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="24883-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="24883-116">Dokument</span><span class="sxs-lookup"><span data-stu-id="24883-116">Document</span></span><br/> |
| <span data-ttu-id="24883-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24883-117">Notes</span></span> <br/>          | <span data-ttu-id="24883-118">Keine</span><span class="sxs-lookup"><span data-stu-id="24883-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="24883-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="24883-119">Structural Content</span></span>

<span data-ttu-id="24883-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="24883-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="24883-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="24883-121">Structure Variables</span></span>

<span data-ttu-id="24883-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="24883-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="24883-123">Name</span><span class="sxs-lookup"><span data-stu-id="24883-123">Name</span></span>                            | <span data-ttu-id="24883-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="24883-124">Data type</span></span>         | <span data-ttu-id="24883-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="24883-125">Unit</span></span> | <span data-ttu-id="24883-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="24883-126">Supported values</span></span> | <span data-ttu-id="24883-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="24883-127">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="24883-128">\_Documenturivalue\_</span><span class="sxs-lookup"><span data-stu-id="24883-128">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="24883-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="24883-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="24883-130">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="24883-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="24883-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24883-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24883-132">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="24883-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




