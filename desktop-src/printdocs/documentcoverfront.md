---
description: Erfahren Sie mehr über das vom Benutzer konfigurierbare DocumentCoverFront-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301b67c9a741caa48024646854b208ac5dffbb20
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119825"
---
# <a name="documentcoverfront"></a><span data-ttu-id="bbf5d-105">DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="bbf5d-105">DocumentCoverFront</span></span>

<span data-ttu-id="bbf5d-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-106">This topic is not current.</span></span> <span data-ttu-id="bbf5d-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="bbf5d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bbf5d-108">Beschreibt das Front-Cover-Blatt (Anfang).</span><span class="sxs-lookup"><span data-stu-id="bbf5d-108">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="bbf5d-109">Jedes Dokument enthält ein separates Blatt.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-109">Each document will have a separate sheet.</span></span> <span data-ttu-id="bbf5d-110">Das Titelblatt sollte auf der ersten Seite des Dokuments auf PageMediaSize und PageMediaType gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-110">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="bbf5d-111">Das Coversheet sollte in Verarbeitungsoptionen (z. B. DocumentDuplex, DocumentNUp) integriert werden, wie durch die angegebene Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-111">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="bbf5d-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="bbf5d-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bbf5d-113">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="bbf5d-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bbf5d-114">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bbf5d-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bbf5d-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="bbf5d-115">Element Information</span></span>



| <span data-ttu-id="bbf5d-116">Name</span><span class="sxs-lookup"><span data-stu-id="bbf5d-116">Name</span></span> | <span data-ttu-id="bbf5d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bbf5d-117">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf5d-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="bbf5d-118">Element Type</span></span> <br/>   | <span data-ttu-id="bbf5d-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="bbf5d-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="bbf5d-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="bbf5d-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bbf5d-121">Dokument</span><span class="sxs-lookup"><span data-stu-id="bbf5d-121">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="bbf5d-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bbf5d-122">Notes</span></span> <br/>          | <span data-ttu-id="bbf5d-123">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="bbf5d-124">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="bbf5d-125">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="bbf5d-126">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="bbf5d-127">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="bbf5d-128">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="bbf5d-128">Structural Content</span></span>

<span data-ttu-id="bbf5d-129">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="bbf5d-129">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="bbf5d-130">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="bbf5d-130">Structure Variables</span></span>

<span data-ttu-id="bbf5d-131">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bbf5d-132">Name</span><span class="sxs-lookup"><span data-stu-id="bbf5d-132">Name</span></span>                               | <span data-ttu-id="bbf5d-133">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bbf5d-133">Data type</span></span>         | <span data-ttu-id="bbf5d-134">Einheit</span><span class="sxs-lookup"><span data-stu-id="bbf5d-134">Unit</span></span>                  | <span data-ttu-id="bbf5d-135">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="bbf5d-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bbf5d-136">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bbf5d-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bbf5d-137">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="bbf5d-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="bbf5d-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbf5d-138">string</span></span><br/> | <span data-ttu-id="bbf5d-139">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="bbf5d-139">characters</span></span><br/> | <span data-ttu-id="bbf5d-140">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="bbf5d-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bbf5d-141">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bbf5d-142">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="bbf5d-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bbf5d-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="bbf5d-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbf5d-144">string</span></span><br/> | <span data-ttu-id="bbf5d-145">–</span><span class="sxs-lookup"><span data-stu-id="bbf5d-145">n/a</span></span><br/>        | <span data-ttu-id="bbf5d-146">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="bbf5d-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bbf5d-147">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bbf5d-148">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bbf5d-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bbf5d-149">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="bbf5d-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bbf5d-150">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="bbf5d-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bbf5d-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbf5d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbf5d-152">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="bbf5d-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




