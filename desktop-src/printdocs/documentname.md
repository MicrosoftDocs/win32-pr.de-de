---
description: Erfahren Sie mehr über die DocumentName-Eigenschaft, die einen beschreibenden Namen für das Dokument angibt.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: Documentname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202ff1f5bac85fec3feac9f141834adfcd37e70
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409273"
---
# <a name="documentname"></a><span data-ttu-id="72909-103">Documentname</span><span class="sxs-lookup"><span data-stu-id="72909-103">DocumentName</span></span>

<span data-ttu-id="72909-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="72909-104">This topic is not current.</span></span> <span data-ttu-id="72909-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="72909-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="72909-106">Gibt einen beschreibenden Namen für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="72909-106">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="72909-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="72909-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="72909-108">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="72909-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="72909-109">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="72909-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="72909-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="72909-110">Element Information</span></span>



| <span data-ttu-id="72909-111">Name</span><span class="sxs-lookup"><span data-stu-id="72909-111">Name</span></span> | <span data-ttu-id="72909-112">Wert</span><span class="sxs-lookup"><span data-stu-id="72909-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="72909-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="72909-113">Element Type</span></span> <br/>   | <span data-ttu-id="72909-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="72909-114">Property</span></span><br/> |
| <span data-ttu-id="72909-115">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="72909-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="72909-116">Dokument</span><span class="sxs-lookup"><span data-stu-id="72909-116">Document</span></span><br/> |
| <span data-ttu-id="72909-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72909-117">Notes</span></span> <br/>          | <span data-ttu-id="72909-118">Keine</span><span class="sxs-lookup"><span data-stu-id="72909-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="72909-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="72909-119">Structural Content</span></span>

<span data-ttu-id="72909-120">Die XML-Struktur dieses Elements lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="72909-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="72909-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="72909-121">Structure Variables</span></span>

<span data-ttu-id="72909-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="72909-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="72909-123">Name</span><span class="sxs-lookup"><span data-stu-id="72909-123">Name</span></span>                             | <span data-ttu-id="72909-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="72909-124">Data type</span></span>         | <span data-ttu-id="72909-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="72909-125">Unit</span></span> | <span data-ttu-id="72909-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="72909-126">Supported values</span></span> | <span data-ttu-id="72909-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="72909-127">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="72909-128">\_DocumentNameValue\_</span><span class="sxs-lookup"><span data-stu-id="72909-128">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="72909-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="72909-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="72909-130">Extensible Markup Language (XML)-Inhalt</span><span class="sxs-lookup"><span data-stu-id="72909-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="72909-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72909-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72909-132">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="72909-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




