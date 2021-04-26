---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd89bea06d3004b435cb55ff51612b1b91380c7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996267"
---
# <a name="documentcoverfront"></a><span data-ttu-id="4826e-104">DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="4826e-104">DocumentCoverFront</span></span>

<span data-ttu-id="4826e-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4826e-105">This topic is not current.</span></span> <span data-ttu-id="4826e-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="4826e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4826e-107">Beschreibt das vordere (beginnende) Coversheet.</span><span class="sxs-lookup"><span data-stu-id="4826e-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="4826e-108">Jedes Dokument hat ein separates Blatt.</span><span class="sxs-lookup"><span data-stu-id="4826e-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="4826e-109">Das Coverblatt sollte auf den Seiten "PageMediaSize" und "PageMediaType" gedruckt werden, die für die erste Seite des Dokuments verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4826e-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="4826e-110">Das Coversheet sollte in Verarbeitungsoptionen (z. B. DocumentDuplex, DocumentNUp) integriert werden, wie durch die angegebene Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="4826e-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="4826e-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4826e-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4826e-112">Strukturell</span><span class="sxs-lookup"><span data-stu-id="4826e-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4826e-113">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="4826e-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4826e-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4826e-114">Element Information</span></span>



| <span data-ttu-id="4826e-115">Name</span><span class="sxs-lookup"><span data-stu-id="4826e-115">Name</span></span> | <span data-ttu-id="4826e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4826e-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4826e-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4826e-117">Element Type</span></span> <br/>   | <span data-ttu-id="4826e-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="4826e-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="4826e-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="4826e-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4826e-120">Dokument</span><span class="sxs-lookup"><span data-stu-id="4826e-120">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="4826e-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4826e-121">Notes</span></span> <br/>          | <span data-ttu-id="4826e-122">XPS-kompatible Consumer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Dokument mit Druckfunktionen oder printTicket auf einen Teilnamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="4826e-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="4826e-123">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="4826e-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="4826e-124">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="4826e-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="4826e-125">URIs, auf die in einem Dokument mit Druckfunktionen oder in PrintTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4826e-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="4826e-126">Dies ist unsicher, da sie möglicherweise nicht wie vorgesehen aufgelöst werden und schädliche Sicherheitsrisiken für Treiber und Betriebssystem darstellen können.</span><span class="sxs-lookup"><span data-stu-id="4826e-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="4826e-127">Strukturell</span><span class="sxs-lookup"><span data-stu-id="4826e-127">Structural Content</span></span>

<span data-ttu-id="4826e-128">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="4826e-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="4826e-129">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="4826e-129">Structure Variables</span></span>

<span data-ttu-id="4826e-130">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4826e-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4826e-131">Name</span><span class="sxs-lookup"><span data-stu-id="4826e-131">Name</span></span>                               | <span data-ttu-id="4826e-132">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4826e-132">Data type</span></span>         | <span data-ttu-id="4826e-133">Einheit</span><span class="sxs-lookup"><span data-stu-id="4826e-133">Unit</span></span>                  | <span data-ttu-id="4826e-134">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="4826e-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4826e-135">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4826e-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4826e-136">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="4826e-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4826e-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4826e-137">string</span></span><br/> | <span data-ttu-id="4826e-138">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="4826e-138">characters</span></span><br/> | <span data-ttu-id="4826e-139">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="4826e-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4826e-140">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="4826e-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4826e-141">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="4826e-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4826e-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4826e-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4826e-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4826e-143">string</span></span><br/> | <span data-ttu-id="4826e-144">–</span><span class="sxs-lookup"><span data-stu-id="4826e-144">n/a</span></span><br/>        | <span data-ttu-id="4826e-145">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="4826e-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4826e-146">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="4826e-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4826e-147">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4826e-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4826e-148">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="4826e-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4826e-149">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="4826e-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="4826e-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4826e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4826e-151">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="4826e-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




