---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: Documentseparatorsheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722e5db4f1a3bfebe8895c8a0777a849a88f11e
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351988"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="9eeae-104">Documentseparatorsheet</span><span class="sxs-lookup"><span data-stu-id="9eeae-104">DocumentSeparatorSheet</span></span>

<span data-ttu-id="9eeae-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9eeae-105">This topic is not current.</span></span> <span data-ttu-id="9eeae-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9eeae-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9eeae-107">Beschreibt die Verwendung des Trenn Blatts für ein Dokument.</span><span class="sxs-lookup"><span data-stu-id="9eeae-107">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="9eeae-108">Trennzeichen Blätter sollten in der Ausgabe angezeigt werden, wie in der unten angegebenen Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="9eeae-108">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="9eeae-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9eeae-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9eeae-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9eeae-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9eeae-111">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9eeae-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9eeae-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9eeae-112">Element Information</span></span>



| <span data-ttu-id="9eeae-113">Name</span><span class="sxs-lookup"><span data-stu-id="9eeae-113">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="9eeae-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="9eeae-114">Element Type</span></span> <br/>   | <span data-ttu-id="9eeae-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="9eeae-115">Feature</span></span><br/>  |
| <span data-ttu-id="9eeae-116">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="9eeae-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9eeae-117">Dokument</span><span class="sxs-lookup"><span data-stu-id="9eeae-117">Document</span></span><br/> |
| <span data-ttu-id="9eeae-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9eeae-118">Notes</span></span> <br/>          | <span data-ttu-id="9eeae-119">Keine</span><span class="sxs-lookup"><span data-stu-id="9eeae-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="9eeae-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9eeae-120">Structural Content</span></span>

<span data-ttu-id="9eeae-121">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="9eeae-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="9eeae-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="9eeae-122">Structure Variables</span></span>

<span data-ttu-id="9eeae-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9eeae-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9eeae-124">Name</span><span class="sxs-lookup"><span data-stu-id="9eeae-124">Name</span></span>                               | <span data-ttu-id="9eeae-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9eeae-125">Data type</span></span>         | <span data-ttu-id="9eeae-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="9eeae-126">Unit</span></span>                  | <span data-ttu-id="9eeae-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="9eeae-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9eeae-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9eeae-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9eeae-129">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="9eeae-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9eeae-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9eeae-130">string</span></span><br/> | <span data-ttu-id="9eeae-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="9eeae-131">characters</span></span><br/> | <span data-ttu-id="9eeae-132">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="9eeae-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9eeae-133">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="9eeae-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9eeae-134">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="9eeae-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9eeae-135">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="9eeae-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9eeae-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9eeae-136">string</span></span><br/> | <span data-ttu-id="9eeae-137">–</span><span class="sxs-lookup"><span data-stu-id="9eeae-137">n/a</span></span><br/>        | <span data-ttu-id="9eeae-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="9eeae-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9eeae-139">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9eeae-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9eeae-140">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9eeae-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9eeae-141">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="9eeae-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9eeae-142">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="9eeae-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9eeae-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9eeae-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eeae-144">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="9eeae-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




