---
description: Erfahren Sie mehr über das DocumentSeparatorSheet-Element, das die Verwendung des Trennblatts für ein Dokument beschreibt.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38195c2d1c52e5c02d9da4844b5fa981866a61bc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409163"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="65049-103">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="65049-103">DocumentSeparatorSheet</span></span>

<span data-ttu-id="65049-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="65049-104">This topic is not current.</span></span> <span data-ttu-id="65049-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="65049-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="65049-106">Beschreibt die Verwendung des Trennblatts für ein Dokument.</span><span class="sxs-lookup"><span data-stu-id="65049-106">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="65049-107">Trennzeichenblätter sollten in der Ausgabe angezeigt werden, wie durch die unten angegebene Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="65049-107">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="65049-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="65049-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="65049-109">Strukturell</span><span class="sxs-lookup"><span data-stu-id="65049-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="65049-110">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="65049-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="65049-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="65049-111">Element Information</span></span>



| <span data-ttu-id="65049-112">Name</span><span class="sxs-lookup"><span data-stu-id="65049-112">Name</span></span> | <span data-ttu-id="65049-113">Wert</span><span class="sxs-lookup"><span data-stu-id="65049-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="65049-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="65049-114">Element Type</span></span> <br/>   | <span data-ttu-id="65049-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="65049-115">Feature</span></span><br/>  |
| <span data-ttu-id="65049-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="65049-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="65049-117">Dokument</span><span class="sxs-lookup"><span data-stu-id="65049-117">Document</span></span><br/> |
| <span data-ttu-id="65049-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65049-118">Notes</span></span> <br/>          | <span data-ttu-id="65049-119">Keine</span><span class="sxs-lookup"><span data-stu-id="65049-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="65049-120">Strukturell</span><span class="sxs-lookup"><span data-stu-id="65049-120">Structural Content</span></span>

<span data-ttu-id="65049-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="65049-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="65049-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="65049-122">Structure Variables</span></span>

<span data-ttu-id="65049-123">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="65049-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="65049-124">Name</span><span class="sxs-lookup"><span data-stu-id="65049-124">Name</span></span>                               | <span data-ttu-id="65049-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="65049-125">Data type</span></span>         | <span data-ttu-id="65049-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="65049-126">Unit</span></span>                  | <span data-ttu-id="65049-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="65049-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="65049-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="65049-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="65049-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="65049-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="65049-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65049-130">string</span></span><br/> | <span data-ttu-id="65049-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="65049-131">characters</span></span><br/> | <span data-ttu-id="65049-132">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="65049-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="65049-133">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="65049-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="65049-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="65049-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="65049-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="65049-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="65049-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65049-136">string</span></span><br/> | <span data-ttu-id="65049-137">–</span><span class="sxs-lookup"><span data-stu-id="65049-137">n/a</span></span><br/>        | <span data-ttu-id="65049-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="65049-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="65049-139">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="65049-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="65049-140">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="65049-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="65049-141">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="65049-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="65049-142">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="65049-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="65049-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="65049-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65049-144">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="65049-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




