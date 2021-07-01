---
description: Erfahren Sie mehr über das PageSourceColorProfile-Element. Dieses Element definiert die Merkmale des Quellfarbprofils.
ms.assetid: aa4f5425-6ca1-4820-b15d-bbead1f6d735
title: PageSourceColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709d44f8af7ea6c2709201e57bc047fe9b2d21b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118995"
---
# <a name="pagesourcecolorprofile"></a><span data-ttu-id="c6d6b-104">PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="c6d6b-104">PageSourceColorProfile</span></span>

<span data-ttu-id="c6d6b-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-105">This topic is not current.</span></span> <span data-ttu-id="c6d6b-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c6d6b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c6d6b-107">Definiert die Merkmale des Quellfarbprofils.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-107">Defines the characteristics of the source color profile.</span></span>

-   [<span data-ttu-id="c6d6b-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c6d6b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c6d6b-109">Strukturell</span><span class="sxs-lookup"><span data-stu-id="c6d6b-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c6d6b-110">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="c6d6b-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c6d6b-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c6d6b-111">Element Information</span></span>



| <span data-ttu-id="c6d6b-112">Name</span><span class="sxs-lookup"><span data-stu-id="c6d6b-112">Name</span></span>                       | <span data-ttu-id="c6d6b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c6d6b-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d6b-114">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c6d6b-114">Element Type</span></span> <br/>   | <span data-ttu-id="c6d6b-115">Funktion</span><span class="sxs-lookup"><span data-stu-id="c6d6b-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c6d6b-116">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="c6d6b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c6d6b-117">Seite</span><span class="sxs-lookup"><span data-stu-id="c6d6b-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c6d6b-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c6d6b-118">Notes</span></span> <br/>          | <span data-ttu-id="c6d6b-119">XPS-kompatible Consumer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Dokument mit Druckfunktionen oder printTicket auf einen Teilnamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="c6d6b-120">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="c6d6b-121">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="c6d6b-122">URIs, auf die in einem Dokument mit Druckfunktionen oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="c6d6b-123">Dies ist unsicher, da sie möglicherweise nicht wie vorgesehen aufgelöst werden und schädliche Sicherheitsrisiken für Treiber und Betriebssystem darstellen können.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c6d6b-124">Strukturell</span><span class="sxs-lookup"><span data-stu-id="c6d6b-124">Structural Content</span></span>

<span data-ttu-id="c6d6b-125">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="c6d6b-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="c6d6b-126">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="c6d6b-126">Structure Variables</span></span>

<span data-ttu-id="c6d6b-127">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c6d6b-128">Name</span><span class="sxs-lookup"><span data-stu-id="c6d6b-128">Name</span></span>                               | <span data-ttu-id="c6d6b-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c6d6b-129">Data type</span></span>         | <span data-ttu-id="c6d6b-130">Einheit</span><span class="sxs-lookup"><span data-stu-id="c6d6b-130">Unit</span></span>                  | <span data-ttu-id="c6d6b-131">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="c6d6b-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c6d6b-132">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c6d6b-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c6d6b-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="c6d6b-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c6d6b-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c6d6b-134">string</span></span><br/> | <span data-ttu-id="c6d6b-135">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="c6d6b-135">characters</span></span><br/> | <span data-ttu-id="c6d6b-136">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c6d6b-137">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c6d6b-138">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c6d6b-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c6d6b-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c6d6b-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c6d6b-140">string</span></span><br/> | <span data-ttu-id="c6d6b-141">–</span><span class="sxs-lookup"><span data-stu-id="c6d6b-141">n/a</span></span><br/>        | <span data-ttu-id="c6d6b-142">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="c6d6b-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c6d6b-143">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c6d6b-144">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="c6d6b-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c6d6b-145">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="c6d6b-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c6d6b-146">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="c6d6b-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
  <psf:Option name="psk:RGB">
    <!-- Source profile used to perform color management for untagged RGB data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:CMYK">
    <!-- Source profile used to perform color management for untagged CMYK data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="c6d6b-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6d6b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6d6b-148">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c6d6b-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




