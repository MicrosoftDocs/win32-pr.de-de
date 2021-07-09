---
description: Abrufen von Informationen zur DocumentURI-Eigenschaft. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb4d1572417ac85e14c25c238be1d49611ba858
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548808"
---
# <a name="documenturi"></a><span data-ttu-id="a8f50-105">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="a8f50-105">DocumentURI</span></span>

<span data-ttu-id="a8f50-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a8f50-106">This topic is not current.</span></span> <span data-ttu-id="a8f50-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a8f50-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a8f50-108">Gibt einen URI (Uniform Resource Identifier) für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="a8f50-108">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="a8f50-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a8f50-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a8f50-110">Strukturell</span><span class="sxs-lookup"><span data-stu-id="a8f50-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a8f50-111">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="a8f50-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a8f50-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a8f50-112">Element Information</span></span>



| <span data-ttu-id="a8f50-113">Name</span><span class="sxs-lookup"><span data-stu-id="a8f50-113">Name</span></span> | <span data-ttu-id="a8f50-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a8f50-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="a8f50-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a8f50-115">Element Type</span></span> <br/>   | <span data-ttu-id="a8f50-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a8f50-116">Property</span></span><br/> |
| <span data-ttu-id="a8f50-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a8f50-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a8f50-118">Dokument</span><span class="sxs-lookup"><span data-stu-id="a8f50-118">Document</span></span><br/> |
| <span data-ttu-id="a8f50-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8f50-119">Notes</span></span> <br/>          | <span data-ttu-id="a8f50-120">Keine</span><span class="sxs-lookup"><span data-stu-id="a8f50-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="a8f50-121">Strukturell</span><span class="sxs-lookup"><span data-stu-id="a8f50-121">Structural Content</span></span>

<span data-ttu-id="a8f50-122">Die XML-Struktur dieses Elements sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="a8f50-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="a8f50-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a8f50-123">Structure Variables</span></span>

<span data-ttu-id="a8f50-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a8f50-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a8f50-125">Name</span><span class="sxs-lookup"><span data-stu-id="a8f50-125">Name</span></span>                            | <span data-ttu-id="a8f50-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a8f50-126">Data type</span></span>         | <span data-ttu-id="a8f50-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="a8f50-127">Unit</span></span> | <span data-ttu-id="a8f50-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a8f50-128">Supported values</span></span> | <span data-ttu-id="a8f50-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a8f50-129">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="a8f50-130">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="a8f50-130">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="a8f50-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a8f50-131">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a8f50-132">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="a8f50-132">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="a8f50-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a8f50-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8f50-134">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a8f50-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




