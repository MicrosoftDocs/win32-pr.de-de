---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d339b1b469f276492f7989b0ed7951ca1edad8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997067"
---
# <a name="documenturi"></a><span data-ttu-id="54749-104">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="54749-104">DocumentURI</span></span>

<span data-ttu-id="54749-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="54749-105">This topic is not current.</span></span> <span data-ttu-id="54749-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="54749-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="54749-107">Gibt einen URI (Uniform Resource Identifier) für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="54749-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="54749-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="54749-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="54749-109">Strukturell</span><span class="sxs-lookup"><span data-stu-id="54749-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="54749-110">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="54749-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="54749-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="54749-111">Element Information</span></span>



| <span data-ttu-id="54749-112">Name</span><span class="sxs-lookup"><span data-stu-id="54749-112">Name</span></span> | <span data-ttu-id="54749-113">Wert</span><span class="sxs-lookup"><span data-stu-id="54749-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="54749-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="54749-114">Element Type</span></span> <br/>   | <span data-ttu-id="54749-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="54749-115">Property</span></span><br/> |
| <span data-ttu-id="54749-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="54749-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="54749-117">Dokument</span><span class="sxs-lookup"><span data-stu-id="54749-117">Document</span></span><br/> |
| <span data-ttu-id="54749-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54749-118">Notes</span></span> <br/>          | <span data-ttu-id="54749-119">Keine</span><span class="sxs-lookup"><span data-stu-id="54749-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="54749-120">Strukturell</span><span class="sxs-lookup"><span data-stu-id="54749-120">Structural Content</span></span>

<span data-ttu-id="54749-121">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="54749-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="54749-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="54749-122">Structure Variables</span></span>

<span data-ttu-id="54749-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="54749-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="54749-124">Name</span><span class="sxs-lookup"><span data-stu-id="54749-124">Name</span></span>                            | <span data-ttu-id="54749-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="54749-125">Data type</span></span>         | <span data-ttu-id="54749-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="54749-126">Unit</span></span> | <span data-ttu-id="54749-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="54749-127">Supported values</span></span> | <span data-ttu-id="54749-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="54749-128">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="54749-129">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="54749-129">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="54749-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="54749-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="54749-131">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="54749-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="54749-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54749-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54749-133">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="54749-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




