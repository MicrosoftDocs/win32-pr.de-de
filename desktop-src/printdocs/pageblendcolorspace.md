---
description: Erfahren Sie mehr über das vom Benutzer konfigurierbare PageBlendColorSpace-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36ce3a1def74058014fc396d9ef53aed6a32302
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549338"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="6a9a2-105">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="6a9a2-105">PageBlendColorSpace</span></span>

<span data-ttu-id="6a9a2-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-106">This topic is not current.</span></span> <span data-ttu-id="6a9a2-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="6a9a2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6a9a2-108">Beschreibt den Farbraum, der für Blendingvorgänge verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-108">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="6a9a2-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6a9a2-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6a9a2-110">Strukturell</span><span class="sxs-lookup"><span data-stu-id="6a9a2-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6a9a2-111">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="6a9a2-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6a9a2-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6a9a2-112">Element Information</span></span>



| <span data-ttu-id="6a9a2-113">Name</span><span class="sxs-lookup"><span data-stu-id="6a9a2-113">Name</span></span> | <span data-ttu-id="6a9a2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6a9a2-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9a2-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="6a9a2-115">Element Type</span></span> <br/>   | <span data-ttu-id="6a9a2-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="6a9a2-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6a9a2-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="6a9a2-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6a9a2-118">Auftrag</span><span class="sxs-lookup"><span data-stu-id="6a9a2-118">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6a9a2-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a9a2-119">Notes</span></span> <br/>          | <span data-ttu-id="6a9a2-120">XPS-kompatible Consumer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Dokument mit Druckfunktionen oder printTicket auf einen Teilnamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="6a9a2-121">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="6a9a2-122">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="6a9a2-123">URIs, auf die in einem Dokument mit Druckfunktionen oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="6a9a2-124">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt aufgelöst werden und schädliche Sicherheitsrisiken für Treiber und Betriebssystem darstellen können.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="6a9a2-125">Strukturell</span><span class="sxs-lookup"><span data-stu-id="6a9a2-125">Structural Content</span></span>

<span data-ttu-id="6a9a2-126">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="6a9a2-126">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="6a9a2-127">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="6a9a2-127">Structure Variables</span></span>

<span data-ttu-id="6a9a2-128">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6a9a2-129">Name</span><span class="sxs-lookup"><span data-stu-id="6a9a2-129">Name</span></span>                               | <span data-ttu-id="6a9a2-130">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6a9a2-130">Data type</span></span>         | <span data-ttu-id="6a9a2-131">Einheit</span><span class="sxs-lookup"><span data-stu-id="6a9a2-131">Unit</span></span>                  | <span data-ttu-id="6a9a2-132">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="6a9a2-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6a9a2-133">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6a9a2-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6a9a2-134">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="6a9a2-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6a9a2-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6a9a2-135">string</span></span><br/> | <span data-ttu-id="6a9a2-136">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="6a9a2-136">characters</span></span><br/> | <span data-ttu-id="6a9a2-137">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6a9a2-138">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6a9a2-139">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6a9a2-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6a9a2-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6a9a2-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6a9a2-141">string</span></span><br/> | <span data-ttu-id="6a9a2-142">n/v</span><span class="sxs-lookup"><span data-stu-id="6a9a2-142">n/a</span></span><br/>        | <span data-ttu-id="6a9a2-143">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="6a9a2-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6a9a2-144">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6a9a2-145">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="6a9a2-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6a9a2-146">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="6a9a2-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6a9a2-147">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="6a9a2-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6a9a2-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a9a2-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a9a2-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="6a9a2-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




