---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d41bb96fe904a80210a951f700830604030eadd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106357160"
---
# <a name="documentid"></a><span data-ttu-id="d146d-104">DocumentID</span><span class="sxs-lookup"><span data-stu-id="d146d-104">DocumentID</span></span>

<span data-ttu-id="d146d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="d146d-105">This topic is not current.</span></span> <span data-ttu-id="d146d-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d146d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d146d-107">Gibt eine eindeutige ID für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="d146d-107">Specifies a unique ID for the document.</span></span>

-   [<span data-ttu-id="d146d-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d146d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d146d-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="d146d-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d146d-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d146d-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d146d-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d146d-111">Element Information</span></span>



| <span data-ttu-id="d146d-112">Name</span><span class="sxs-lookup"><span data-stu-id="d146d-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="d146d-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="d146d-113">Element Type</span></span> <br/>   | <span data-ttu-id="d146d-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d146d-114">Property</span></span><br/> |
| <span data-ttu-id="d146d-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="d146d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d146d-116">Dokument</span><span class="sxs-lookup"><span data-stu-id="d146d-116">Document</span></span><br/> |
| <span data-ttu-id="d146d-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d146d-117">Notes</span></span> <br/>          | <span data-ttu-id="d146d-118">Keine</span><span class="sxs-lookup"><span data-stu-id="d146d-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="d146d-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="d146d-119">Structural Content</span></span>

<span data-ttu-id="d146d-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d146d-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="d146d-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="d146d-121">Structure Variables</span></span>

<span data-ttu-id="d146d-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d146d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d146d-123">Name</span><span class="sxs-lookup"><span data-stu-id="d146d-123">Name</span></span>                           | <span data-ttu-id="d146d-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d146d-124">Data type</span></span>         | <span data-ttu-id="d146d-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="d146d-125">Unit</span></span> | <span data-ttu-id="d146d-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="d146d-126">Supported values</span></span> | <span data-ttu-id="d146d-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d146d-127">Summary</span></span> |
|--------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="d146d-128">\_Documentidvalue\_</span><span class="sxs-lookup"><span data-stu-id="d146d-128">\_DocumentIDValue\_</span></span><br/> | <span data-ttu-id="d146d-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d146d-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d146d-130">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d146d-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="d146d-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d146d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d146d-132">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="d146d-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




