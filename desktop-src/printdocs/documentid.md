---
description: Erfahren Sie mehr über das DocumentID-Element, das eine eindeutige ID für das Dokument angibt. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b267fead0322351cde396bf2eb6d0efa8c523f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409283"
---
# <a name="documentid"></a><span data-ttu-id="3ab4a-104">DocumentID</span><span class="sxs-lookup"><span data-stu-id="3ab4a-104">DocumentID</span></span>

<span data-ttu-id="3ab4a-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3ab4a-105">This topic is not current.</span></span> <span data-ttu-id="3ab4a-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="3ab4a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3ab4a-107">Gibt eine eindeutige ID für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="3ab4a-107">Specifies a unique ID for the document.</span></span>

-   [<span data-ttu-id="3ab4a-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3ab4a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3ab4a-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="3ab4a-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3ab4a-110">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="3ab4a-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3ab4a-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3ab4a-111">Element Information</span></span>



| <span data-ttu-id="3ab4a-112">Name</span><span class="sxs-lookup"><span data-stu-id="3ab4a-112">Name</span></span> | <span data-ttu-id="3ab4a-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3ab4a-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="3ab4a-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="3ab4a-114">Element Type</span></span> <br/>   | <span data-ttu-id="3ab4a-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ab4a-115">Property</span></span><br/> |
| <span data-ttu-id="3ab4a-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="3ab4a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3ab4a-117">Dokument</span><span class="sxs-lookup"><span data-stu-id="3ab4a-117">Document</span></span><br/> |
| <span data-ttu-id="3ab4a-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3ab4a-118">Notes</span></span> <br/>          | <span data-ttu-id="3ab4a-119">Keine</span><span class="sxs-lookup"><span data-stu-id="3ab4a-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="3ab4a-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="3ab4a-120">Structural Content</span></span>

<span data-ttu-id="3ab4a-121">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ab4a-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="3ab4a-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="3ab4a-122">Structure Variables</span></span>

<span data-ttu-id="3ab4a-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3ab4a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3ab4a-124">Name</span><span class="sxs-lookup"><span data-stu-id="3ab4a-124">Name</span></span>                           | <span data-ttu-id="3ab4a-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3ab4a-125">Data type</span></span>         | <span data-ttu-id="3ab4a-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="3ab4a-126">Unit</span></span> | <span data-ttu-id="3ab4a-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="3ab4a-127">Supported values</span></span> | <span data-ttu-id="3ab4a-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3ab4a-128">Summary</span></span> |
|--------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="3ab4a-129">\_DocumentIDValue\_</span><span class="sxs-lookup"><span data-stu-id="3ab4a-129">\_DocumentIDValue\_</span></span><br/> | <span data-ttu-id="3ab4a-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3ab4a-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3ab4a-131">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="3ab4a-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="3ab4a-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3ab4a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ab4a-133">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="3ab4a-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




