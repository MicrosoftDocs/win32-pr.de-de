---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12002b25265a66a0aa3a5168f29e1e8e542ce31
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998077"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="c1ad4-104">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="c1ad4-104">PageBlendColorSpace</span></span>

<span data-ttu-id="c1ad4-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-105">This topic is not current.</span></span> <span data-ttu-id="c1ad4-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c1ad4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c1ad4-107">Beschreibt den Farbraum, der für Blendingvorgänge verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-107">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="c1ad4-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c1ad4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c1ad4-109">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="c1ad4-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c1ad4-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="c1ad4-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c1ad4-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c1ad4-111">Element Information</span></span>



| <span data-ttu-id="c1ad4-112">Name</span><span class="sxs-lookup"><span data-stu-id="c1ad4-112">Name</span></span> | <span data-ttu-id="c1ad4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c1ad4-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ad4-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c1ad4-114">Element Type</span></span> <br/>   | <span data-ttu-id="c1ad4-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="c1ad4-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c1ad4-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="c1ad4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c1ad4-117">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c1ad4-117">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c1ad4-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1ad4-118">Notes</span></span> <br/>          | <span data-ttu-id="c1ad4-119">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="c1ad4-120">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="c1ad4-121">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="c1ad4-122">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="c1ad4-123">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c1ad4-124">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="c1ad4-124">Structural Content</span></span>

<span data-ttu-id="c1ad4-125">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="c1ad4-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
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

## <a name="structure-variables"></a><span data-ttu-id="c1ad4-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="c1ad4-126">Structure Variables</span></span>

<span data-ttu-id="c1ad4-127">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c1ad4-128">Name</span><span class="sxs-lookup"><span data-stu-id="c1ad4-128">Name</span></span>                               | <span data-ttu-id="c1ad4-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c1ad4-129">Data type</span></span>         | <span data-ttu-id="c1ad4-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="c1ad4-130">Unit</span></span>                  | <span data-ttu-id="c1ad4-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="c1ad4-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c1ad4-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c1ad4-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c1ad4-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="c1ad4-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c1ad4-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c1ad4-134">string</span></span><br/> | <span data-ttu-id="c1ad4-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="c1ad4-135">characters</span></span><br/> | <span data-ttu-id="c1ad4-136">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="c1ad4-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c1ad4-137">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c1ad4-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c1ad4-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c1ad4-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c1ad4-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c1ad4-140">string</span></span><br/> | <span data-ttu-id="c1ad4-141">–</span><span class="sxs-lookup"><span data-stu-id="c1ad4-141">n/a</span></span><br/>        | <span data-ttu-id="c1ad4-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="c1ad4-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c1ad4-143">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c1ad4-144">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="c1ad4-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c1ad4-145">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="c1ad4-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c1ad4-146">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="c1ad4-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- sRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:sRGB" />
  <!-- scRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:scRGB" />
  <!-- Specifies an ICC profile defining the color space that SHOULD be used for blending.  Note: This applies to XPS Documents only and should not be used in arbitrary PrintTickets. -->
  <psf:Option name="psk:ICCProfile">
    <!-- XPS specific part name for the blend mode ICC Profile -->
    <psf:ScoredProperty name="psk:URI">
      <psf:ParameterRef name="psk:PageBlendColorSpaceICCProfileURI" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="c1ad4-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1ad4-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1ad4-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c1ad4-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




