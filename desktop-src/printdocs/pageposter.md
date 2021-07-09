---
description: Abrufen von Informationen über das vom Benutzer konfigurierbare PagePoster-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: PagePoster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b8bb7b57074fe058c7cc5be8dd609577ceb6c1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548968"
---
# <a name="pageposter"></a><span data-ttu-id="1ee22-105">PagePoster</span><span class="sxs-lookup"><span data-stu-id="1ee22-105">PagePoster</span></span>

<span data-ttu-id="1ee22-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="1ee22-106">This topic is not current.</span></span> <span data-ttu-id="1ee22-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="1ee22-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1ee22-108">Beschreibt die Ausgabe einer einzelnen Seite an mehrere physische Medienblätter.</span><span class="sxs-lookup"><span data-stu-id="1ee22-108">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="1ee22-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1ee22-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1ee22-110">Strukturell</span><span class="sxs-lookup"><span data-stu-id="1ee22-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1ee22-111">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="1ee22-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1ee22-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1ee22-112">Element Information</span></span>



| <span data-ttu-id="1ee22-113">Name</span><span class="sxs-lookup"><span data-stu-id="1ee22-113">Name</span></span> | <span data-ttu-id="1ee22-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1ee22-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="1ee22-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="1ee22-115">Element Type</span></span> <br/>   | <span data-ttu-id="1ee22-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="1ee22-116">Feature</span></span><br/> |
| <span data-ttu-id="1ee22-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="1ee22-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1ee22-118">Seite</span><span class="sxs-lookup"><span data-stu-id="1ee22-118">Page</span></span><br/>    |
| <span data-ttu-id="1ee22-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ee22-119">Notes</span></span> <br/>          | <span data-ttu-id="1ee22-120">Keine</span><span class="sxs-lookup"><span data-stu-id="1ee22-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1ee22-121">Strukturell</span><span class="sxs-lookup"><span data-stu-id="1ee22-121">Structural Content</span></span>

<span data-ttu-id="1ee22-122">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="1ee22-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1ee22-123">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="1ee22-123">Structure Variables</span></span>

<span data-ttu-id="1ee22-124">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1ee22-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1ee22-125">Name</span><span class="sxs-lookup"><span data-stu-id="1ee22-125">Name</span></span>                               | <span data-ttu-id="1ee22-126">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1ee22-126">Data type</span></span>          | <span data-ttu-id="1ee22-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="1ee22-127">Unit</span></span>                  | <span data-ttu-id="1ee22-128">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="1ee22-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1ee22-129">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1ee22-129">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1ee22-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="1ee22-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1ee22-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1ee22-131">string</span></span><br/>  | <span data-ttu-id="1ee22-132">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="1ee22-132">characters</span></span><br/> | <span data-ttu-id="1ee22-133">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="1ee22-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1ee22-134">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="1ee22-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1ee22-135">Der Name der Option</span><span class="sxs-lookup"><span data-stu-id="1ee22-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="1ee22-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1ee22-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1ee22-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1ee22-137">string</span></span><br/>  | <span data-ttu-id="1ee22-138">n/v</span><span class="sxs-lookup"><span data-stu-id="1ee22-138">n/a</span></span><br/>        | <span data-ttu-id="1ee22-139">True, False</span><span class="sxs-lookup"><span data-stu-id="1ee22-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="1ee22-140">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="1ee22-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="1ee22-141">\_SheetsPerPageValue\_</span><span class="sxs-lookup"><span data-stu-id="1ee22-141">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="1ee22-142">integer</span><span class="sxs-lookup"><span data-stu-id="1ee22-142">integer</span></span><br/> | <span data-ttu-id="1ee22-143">Seiten</span><span class="sxs-lookup"><span data-stu-id="1ee22-143">pages</span></span><br/>      | <span data-ttu-id="1ee22-144">Größer als oder gleich 0.</span><span class="sxs-lookup"><span data-stu-id="1ee22-144">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="1ee22-145">Gibt die Anzahl der physischen Blätter pro logischer Seite an.</span><span class="sxs-lookup"><span data-stu-id="1ee22-145">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1ee22-146">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="1ee22-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1ee22-147">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="1ee22-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1ee22-148">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="1ee22-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1ee22-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ee22-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ee22-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="1ee22-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




