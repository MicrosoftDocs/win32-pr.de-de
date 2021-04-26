---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: PagePoster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46cad46abcad7541f1282d691c950211bb7670c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996087"
---
# <a name="pageposter"></a><span data-ttu-id="a82cb-104">PagePoster</span><span class="sxs-lookup"><span data-stu-id="a82cb-104">PagePoster</span></span>

<span data-ttu-id="a82cb-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a82cb-105">This topic is not current.</span></span> <span data-ttu-id="a82cb-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a82cb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a82cb-107">Beschreibt die Ausgabe einer einzelnen Seite auf mehrere physische Medienblätter.</span><span class="sxs-lookup"><span data-stu-id="a82cb-107">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="a82cb-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a82cb-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a82cb-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a82cb-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a82cb-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a82cb-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a82cb-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a82cb-111">Element Information</span></span>



| <span data-ttu-id="a82cb-112">Name</span><span class="sxs-lookup"><span data-stu-id="a82cb-112">Name</span></span> | <span data-ttu-id="a82cb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a82cb-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a82cb-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a82cb-114">Element Type</span></span> <br/>   | <span data-ttu-id="a82cb-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="a82cb-115">Feature</span></span><br/> |
| <span data-ttu-id="a82cb-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="a82cb-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a82cb-117">Seite</span><span class="sxs-lookup"><span data-stu-id="a82cb-117">Page</span></span><br/>    |
| <span data-ttu-id="a82cb-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a82cb-118">Notes</span></span> <br/>          | <span data-ttu-id="a82cb-119">Keine</span><span class="sxs-lookup"><span data-stu-id="a82cb-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a82cb-120">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="a82cb-120">Structural Content</span></span>

<span data-ttu-id="a82cb-121">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="a82cb-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a82cb-122">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="a82cb-122">Structure Variables</span></span>

<span data-ttu-id="a82cb-123">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a82cb-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a82cb-124">Name</span><span class="sxs-lookup"><span data-stu-id="a82cb-124">Name</span></span>                               | <span data-ttu-id="a82cb-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a82cb-125">Data type</span></span>          | <span data-ttu-id="a82cb-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="a82cb-126">Unit</span></span>                  | <span data-ttu-id="a82cb-127">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="a82cb-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a82cb-128">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a82cb-128">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a82cb-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="a82cb-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a82cb-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a82cb-130">string</span></span><br/>  | <span data-ttu-id="a82cb-131">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a82cb-131">characters</span></span><br/> | <span data-ttu-id="a82cb-132">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a82cb-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a82cb-133">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="a82cb-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a82cb-134">Der Name der Option</span><span class="sxs-lookup"><span data-stu-id="a82cb-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="a82cb-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a82cb-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a82cb-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a82cb-136">string</span></span><br/>  | <span data-ttu-id="a82cb-137">–</span><span class="sxs-lookup"><span data-stu-id="a82cb-137">n/a</span></span><br/>        | <span data-ttu-id="a82cb-138">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="a82cb-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="a82cb-139">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a82cb-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="a82cb-140">\_SheetsPerPageValue\_</span><span class="sxs-lookup"><span data-stu-id="a82cb-140">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="a82cb-141">integer</span><span class="sxs-lookup"><span data-stu-id="a82cb-141">integer</span></span><br/> | <span data-ttu-id="a82cb-142">Seiten</span><span class="sxs-lookup"><span data-stu-id="a82cb-142">pages</span></span><br/>      | <span data-ttu-id="a82cb-143">Größer oder gleich 0.</span><span class="sxs-lookup"><span data-stu-id="a82cb-143">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="a82cb-144">Gibt die Anzahl der physischen Blätter pro logischer Seite an.</span><span class="sxs-lookup"><span data-stu-id="a82cb-144">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a82cb-145">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="a82cb-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a82cb-146">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="a82cb-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a82cb-147">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a82cb-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a82cb-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a82cb-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a82cb-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a82cb-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




