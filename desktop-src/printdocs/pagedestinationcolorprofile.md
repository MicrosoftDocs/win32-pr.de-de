---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92845b635aa7db1f44394cb6ef76b32292ea0dd4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996137"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="01387-104">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="01387-104">PageDestinationColorProfile</span></span>

<span data-ttu-id="01387-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="01387-105">This topic is not current.</span></span> <span data-ttu-id="01387-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="01387-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="01387-107">Definiert die Merkmale des Zielfarbprofils.</span><span class="sxs-lookup"><span data-stu-id="01387-107">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="01387-108">Beschreibt, ob die Anwendung oder der Treiber das zu verwendende Zielfarbprofil auswählt.</span><span class="sxs-lookup"><span data-stu-id="01387-108">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="01387-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="01387-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="01387-110">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="01387-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="01387-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="01387-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="01387-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="01387-112">Element Information</span></span>



| <span data-ttu-id="01387-113">Name</span><span class="sxs-lookup"><span data-stu-id="01387-113">Name</span></span> | <span data-ttu-id="01387-114">Wert</span><span class="sxs-lookup"><span data-stu-id="01387-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01387-115">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="01387-115">Element Type</span></span> <br/>   | <span data-ttu-id="01387-116">Funktion</span><span class="sxs-lookup"><span data-stu-id="01387-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="01387-117">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="01387-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="01387-118">Seite</span><span class="sxs-lookup"><span data-stu-id="01387-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="01387-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01387-119">Notes</span></span> <br/>          | <span data-ttu-id="01387-120">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="01387-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="01387-121">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="01387-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="01387-122">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="01387-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="01387-123">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="01387-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="01387-124">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="01387-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="01387-125">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="01387-125">Structural Content</span></span>

<span data-ttu-id="01387-126">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="01387-126">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="01387-127">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="01387-127">Structure Variables</span></span>

<span data-ttu-id="01387-128">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="01387-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="01387-129">Name</span><span class="sxs-lookup"><span data-stu-id="01387-129">Name</span></span>                               | <span data-ttu-id="01387-130">Datentyp</span><span class="sxs-lookup"><span data-stu-id="01387-130">Data type</span></span>         | <span data-ttu-id="01387-131">Einheit</span><span class="sxs-lookup"><span data-stu-id="01387-131">Unit</span></span>                  | <span data-ttu-id="01387-132">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="01387-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="01387-133">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="01387-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="01387-134">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="01387-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="01387-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="01387-135">string</span></span><br/> | <span data-ttu-id="01387-136">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="01387-136">characters</span></span><br/> | <span data-ttu-id="01387-137">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="01387-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="01387-138">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="01387-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="01387-139">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="01387-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="01387-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="01387-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="01387-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="01387-141">string</span></span><br/> | <span data-ttu-id="01387-142">–</span><span class="sxs-lookup"><span data-stu-id="01387-142">n/a</span></span><br/>        | <span data-ttu-id="01387-143">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="01387-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="01387-144">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="01387-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="01387-145">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="01387-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="01387-146">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="01387-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="01387-147">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="01387-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="01387-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01387-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01387-149">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="01387-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




