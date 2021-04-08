---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: DocumentName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5f087744f40111f176e6797dab356c5d290d8f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761541"
---
# <a name="documentname"></a><span data-ttu-id="0a199-104">DocumentName</span><span class="sxs-lookup"><span data-stu-id="0a199-104">DocumentName</span></span>

<span data-ttu-id="0a199-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0a199-105">This topic is not current.</span></span> <span data-ttu-id="0a199-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0a199-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0a199-107">Gibt einen beschreibenden Namen für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="0a199-107">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="0a199-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0a199-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0a199-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="0a199-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0a199-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0a199-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0a199-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0a199-111">Element Information</span></span>



| <span data-ttu-id="0a199-112">Name</span><span class="sxs-lookup"><span data-stu-id="0a199-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="0a199-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0a199-113">Element Type</span></span> <br/>   | <span data-ttu-id="0a199-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0a199-114">Property</span></span><br/> |
| <span data-ttu-id="0a199-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="0a199-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0a199-116">Dokument</span><span class="sxs-lookup"><span data-stu-id="0a199-116">Document</span></span><br/> |
| <span data-ttu-id="0a199-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0a199-117">Notes</span></span> <br/>          | <span data-ttu-id="0a199-118">Keine</span><span class="sxs-lookup"><span data-stu-id="0a199-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="0a199-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="0a199-119">Structural Content</span></span>

<span data-ttu-id="0a199-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0a199-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="0a199-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="0a199-121">Structure Variables</span></span>

<span data-ttu-id="0a199-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0a199-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0a199-123">Name</span><span class="sxs-lookup"><span data-stu-id="0a199-123">Name</span></span>                             | <span data-ttu-id="0a199-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0a199-124">Data type</span></span>         | <span data-ttu-id="0a199-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="0a199-125">Unit</span></span> | <span data-ttu-id="0a199-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="0a199-126">Supported values</span></span> | <span data-ttu-id="0a199-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0a199-127">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="0a199-128">\_Documentnamevalue\_</span><span class="sxs-lookup"><span data-stu-id="0a199-128">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="0a199-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0a199-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0a199-130">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0a199-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="0a199-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a199-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a199-132">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="0a199-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




