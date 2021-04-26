---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: Documentname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66809ef18edb7aa313ea5218f9122acf4ddd1ee8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997797"
---
# <a name="documentname"></a><span data-ttu-id="1ea03-104">Documentname</span><span class="sxs-lookup"><span data-stu-id="1ea03-104">DocumentName</span></span>

<span data-ttu-id="1ea03-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="1ea03-105">This topic is not current.</span></span> <span data-ttu-id="1ea03-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="1ea03-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1ea03-107">Gibt einen beschreibenden Namen für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="1ea03-107">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="1ea03-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1ea03-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1ea03-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="1ea03-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1ea03-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1ea03-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1ea03-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1ea03-111">Element Information</span></span>



| <span data-ttu-id="1ea03-112">Name</span><span class="sxs-lookup"><span data-stu-id="1ea03-112">Name</span></span> | <span data-ttu-id="1ea03-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1ea03-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="1ea03-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="1ea03-114">Element Type</span></span> <br/>   | <span data-ttu-id="1ea03-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1ea03-115">Property</span></span><br/> |
| <span data-ttu-id="1ea03-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="1ea03-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1ea03-117">Dokument</span><span class="sxs-lookup"><span data-stu-id="1ea03-117">Document</span></span><br/> |
| <span data-ttu-id="1ea03-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ea03-118">Notes</span></span> <br/>          | <span data-ttu-id="1ea03-119">Keine</span><span class="sxs-lookup"><span data-stu-id="1ea03-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="1ea03-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="1ea03-120">Structural Content</span></span>

<span data-ttu-id="1ea03-121">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1ea03-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="1ea03-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="1ea03-122">Structure Variables</span></span>

<span data-ttu-id="1ea03-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1ea03-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1ea03-124">Name</span><span class="sxs-lookup"><span data-stu-id="1ea03-124">Name</span></span>                             | <span data-ttu-id="1ea03-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1ea03-125">Data type</span></span>         | <span data-ttu-id="1ea03-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="1ea03-126">Unit</span></span> | <span data-ttu-id="1ea03-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="1ea03-127">Supported values</span></span> | <span data-ttu-id="1ea03-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1ea03-128">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="1ea03-129">\_DocumentNameValue\_</span><span class="sxs-lookup"><span data-stu-id="1ea03-129">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="1ea03-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1ea03-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1ea03-131">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1ea03-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="1ea03-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ea03-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ea03-133">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="1ea03-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




