---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6bd0d58c5b361b167d22c672b7e080e4498d3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997057"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="bc331-104">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="bc331-104">DocumentSeparatorSheet</span></span>

<span data-ttu-id="bc331-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="bc331-105">This topic is not current.</span></span> <span data-ttu-id="bc331-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="bc331-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bc331-107">Beschreibt die Verwendung von Trennblättern für ein Dokument.</span><span class="sxs-lookup"><span data-stu-id="bc331-107">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="bc331-108">Trennzeichenblätter sollten in der Ausgabe angezeigt werden, wie in der unten angegebenen Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="bc331-108">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="bc331-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="bc331-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bc331-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="bc331-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bc331-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bc331-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bc331-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="bc331-112">Element Information</span></span>



| <span data-ttu-id="bc331-113">Name</span><span class="sxs-lookup"><span data-stu-id="bc331-113">Name</span></span> | <span data-ttu-id="bc331-114">Wert</span><span class="sxs-lookup"><span data-stu-id="bc331-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="bc331-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="bc331-115">Element Type</span></span> <br/>   | <span data-ttu-id="bc331-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="bc331-116">Feature</span></span><br/>  |
| <span data-ttu-id="bc331-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="bc331-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bc331-118">Dokument</span><span class="sxs-lookup"><span data-stu-id="bc331-118">Document</span></span><br/> |
| <span data-ttu-id="bc331-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc331-119">Notes</span></span> <br/>          | <span data-ttu-id="bc331-120">Keine</span><span class="sxs-lookup"><span data-stu-id="bc331-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="bc331-121">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="bc331-121">Structural Content</span></span>

<span data-ttu-id="bc331-122">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="bc331-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="bc331-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="bc331-123">Structure Variables</span></span>

<span data-ttu-id="bc331-124">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bc331-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bc331-125">Name</span><span class="sxs-lookup"><span data-stu-id="bc331-125">Name</span></span>                               | <span data-ttu-id="bc331-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bc331-126">Data type</span></span>         | <span data-ttu-id="bc331-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="bc331-127">Unit</span></span>                  | <span data-ttu-id="bc331-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="bc331-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bc331-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bc331-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bc331-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="bc331-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="bc331-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bc331-131">string</span></span><br/> | <span data-ttu-id="bc331-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="bc331-132">characters</span></span><br/> | <span data-ttu-id="bc331-133">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="bc331-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bc331-134">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="bc331-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bc331-135">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="bc331-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="bc331-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bc331-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="bc331-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bc331-137">string</span></span><br/> | <span data-ttu-id="bc331-138">–</span><span class="sxs-lookup"><span data-stu-id="bc331-138">n/a</span></span><br/>        | <span data-ttu-id="bc331-139">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="bc331-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bc331-140">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="bc331-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bc331-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bc331-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bc331-142">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="bc331-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bc331-143">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="bc331-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a separator sheet at the start and end of the document. -->
  <psf:Option name="psk:BothSheets" />
  <!-- Specifies a separator sheet at the end of the document. -->
  <psf:Option name="psk:EndSheet" />
  <!-- Specifies no separator sheet(s). -->
  <psf:Option name="psk:None" />
  <!-- Specifies a separator sheet at the start of the document. -->
  <psf:Option name="psk:StartSheet" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="bc331-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc331-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc331-145">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="bc331-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




