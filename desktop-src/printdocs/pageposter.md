---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: Pageposter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281da67f3f6b90e4e49d0cdc57ba3065d719397b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106355124"
---
# <a name="pageposter"></a><span data-ttu-id="03de2-104">Pageposter</span><span class="sxs-lookup"><span data-stu-id="03de2-104">PagePoster</span></span>

<span data-ttu-id="03de2-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="03de2-105">This topic is not current.</span></span> <span data-ttu-id="03de2-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="03de2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="03de2-107">Beschreibt die Ausgabe einer einzelnen Seite in mehrere physische Medien Blätter.</span><span class="sxs-lookup"><span data-stu-id="03de2-107">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="03de2-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="03de2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="03de2-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="03de2-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="03de2-110">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="03de2-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="03de2-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="03de2-111">Element Information</span></span>



| <span data-ttu-id="03de2-112">Name</span><span class="sxs-lookup"><span data-stu-id="03de2-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="03de2-113">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="03de2-113">Element Type</span></span> <br/>   | <span data-ttu-id="03de2-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="03de2-114">Feature</span></span><br/> |
| <span data-ttu-id="03de2-115">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="03de2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="03de2-116">Seite</span><span class="sxs-lookup"><span data-stu-id="03de2-116">Page</span></span><br/>    |
| <span data-ttu-id="03de2-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="03de2-117">Notes</span></span> <br/>          | <span data-ttu-id="03de2-118">Keine</span><span class="sxs-lookup"><span data-stu-id="03de2-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="03de2-119">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="03de2-119">Structural Content</span></span>

<span data-ttu-id="03de2-120">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="03de2-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_SheetsPerPageValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="03de2-121">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="03de2-121">Structure Variables</span></span>

<span data-ttu-id="03de2-122">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="03de2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="03de2-123">Name</span><span class="sxs-lookup"><span data-stu-id="03de2-123">Name</span></span>                               | <span data-ttu-id="03de2-124">Datentyp</span><span class="sxs-lookup"><span data-stu-id="03de2-124">Data type</span></span>          | <span data-ttu-id="03de2-125">Einheit</span><span class="sxs-lookup"><span data-stu-id="03de2-125">Unit</span></span>                  | <span data-ttu-id="03de2-126">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="03de2-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="03de2-127">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="03de2-127">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="03de2-128">\_Optionsname\_</span><span class="sxs-lookup"><span data-stu-id="03de2-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="03de2-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="03de2-129">string</span></span><br/>  | <span data-ttu-id="03de2-130">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="03de2-130">characters</span></span><br/> | <span data-ttu-id="03de2-131">Gültiger, voll qualifizierter Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="03de2-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="03de2-132">Wenn kein Namespace angegeben wird, wird der Standard Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="03de2-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="03de2-133">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="03de2-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="03de2-134">\_Identityoptionvalue\_</span><span class="sxs-lookup"><span data-stu-id="03de2-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="03de2-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="03de2-135">string</span></span><br/>  | <span data-ttu-id="03de2-136">–</span><span class="sxs-lookup"><span data-stu-id="03de2-136">n/a</span></span><br/>        | <span data-ttu-id="03de2-137">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="03de2-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="03de2-138">Definiert eine Option, die diese Funktion deaktiviert, wenn Sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="03de2-138">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="03de2-139">\_Sheetsperpagevalue\_</span><span class="sxs-lookup"><span data-stu-id="03de2-139">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="03de2-140">integer</span><span class="sxs-lookup"><span data-stu-id="03de2-140">integer</span></span><br/> | <span data-ttu-id="03de2-141">Seiten</span><span class="sxs-lookup"><span data-stu-id="03de2-141">pages</span></span><br/>      | <span data-ttu-id="03de2-142">Größer oder gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="03de2-142">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="03de2-143">Gibt die Anzahl der physischen Blätter pro logischer Seite an.</span><span class="sxs-lookup"><span data-stu-id="03de2-143">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="03de2-144">Inhalt der Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="03de2-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="03de2-145">Die Schlüsselwörter der öffentlichen Druck Schemas werden im- https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="03de2-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="03de2-146">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort wird unten definiert:</span><span class="sxs-lookup"><span data-stu-id="03de2-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies media sheets per page. -->
  <psf:Option>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="03de2-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="03de2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03de2-148">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="03de2-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




