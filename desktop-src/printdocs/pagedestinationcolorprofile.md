---
description: Überprüfen Sie das benutzerkonfigurierbare PageDestinationColorProfile-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c12e8b6e322f024c3603abc97b0e4e0413d5b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549218"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="ee9a9-105">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="ee9a9-105">PageDestinationColorProfile</span></span>

<span data-ttu-id="ee9a9-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-106">This topic is not current.</span></span> <span data-ttu-id="ee9a9-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="ee9a9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ee9a9-108">Definiert die Merkmale des Zielfarbprofils.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-108">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="ee9a9-109">Beschreibt, ob die Anwendung oder der Treiber das zu verwendende Zielfarbprofil auswählt.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-109">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="ee9a9-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ee9a9-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ee9a9-111">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="ee9a9-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ee9a9-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ee9a9-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ee9a9-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ee9a9-113">Element Information</span></span>



| <span data-ttu-id="ee9a9-114">Name</span><span class="sxs-lookup"><span data-stu-id="ee9a9-114">Name</span></span> | <span data-ttu-id="ee9a9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ee9a9-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9a9-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ee9a9-116">Element Type</span></span> <br/>   | <span data-ttu-id="ee9a9-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="ee9a9-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ee9a9-118">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="ee9a9-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ee9a9-119">Seite</span><span class="sxs-lookup"><span data-stu-id="ee9a9-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ee9a9-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee9a9-120">Notes</span></span> <br/>          | <span data-ttu-id="ee9a9-121">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="ee9a9-122">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="ee9a9-123">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="ee9a9-124">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="ee9a9-125">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="ee9a9-126">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="ee9a9-126">Structural Content</span></span>

<span data-ttu-id="ee9a9-127">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="ee9a9-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="ee9a9-128">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="ee9a9-128">Structure Variables</span></span>

<span data-ttu-id="ee9a9-129">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ee9a9-130">Name</span><span class="sxs-lookup"><span data-stu-id="ee9a9-130">Name</span></span>                               | <span data-ttu-id="ee9a9-131">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ee9a9-131">Data type</span></span>         | <span data-ttu-id="ee9a9-132">Einheit</span><span class="sxs-lookup"><span data-stu-id="ee9a9-132">Unit</span></span>                  | <span data-ttu-id="ee9a9-133">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="ee9a9-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ee9a9-134">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ee9a9-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ee9a9-135">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="ee9a9-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ee9a9-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ee9a9-136">string</span></span><br/> | <span data-ttu-id="ee9a9-137">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="ee9a9-137">characters</span></span><br/> | <span data-ttu-id="ee9a9-138">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="ee9a9-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ee9a9-139">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ee9a9-140">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ee9a9-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ee9a9-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ee9a9-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ee9a9-142">string</span></span><br/> | <span data-ttu-id="ee9a9-143">n/v</span><span class="sxs-lookup"><span data-stu-id="ee9a9-143">n/a</span></span><br/>        | <span data-ttu-id="ee9a9-144">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="ee9a9-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ee9a9-145">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ee9a9-146">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ee9a9-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ee9a9-147">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ee9a9-148">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="ee9a9-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <!-- Application specifies the destination profile to be used. -->
  <psf:Option name="psk:Application">
    <!-- Destination profile used to perform color management. -->
    <psf:ScoredProperty name="psk:DestinationColorProfileURI">
      <psf:ParameterRef name="psk:PageDestinationColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DestinationColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageDestinationColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Driver selects the destination profile that best matches its current configuration. -->
  <psf:Option name="psk:DriverConfiguration" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="ee9a9-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee9a9-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee9a9-150">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="ee9a9-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




