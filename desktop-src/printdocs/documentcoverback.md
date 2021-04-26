---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 29d0bf2d-4897-43ed-ba3d-0b38b2f30375
title: DocumentCoverBack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5822921fe3dc1852100569b29a1ded8b37bc9aa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994537"
---
# <a name="documentcoverback"></a><span data-ttu-id="80697-104">DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="80697-104">DocumentCoverBack</span></span>

<span data-ttu-id="80697-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="80697-105">This topic is not current.</span></span> <span data-ttu-id="80697-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="80697-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="80697-107">Beschreibt das Coversheet für die Rückseite (Ende).</span><span class="sxs-lookup"><span data-stu-id="80697-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="80697-108">Jedes Dokument enthält ein separates Blatt.</span><span class="sxs-lookup"><span data-stu-id="80697-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="80697-109">Das Titelblatt sollte auf den Seiten "PageMediaSize" und "PageMediaType" gedruckt werden, die für die letzte Seite des Dokuments verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80697-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the document.</span></span> <span data-ttu-id="80697-110">Das Coversheet sollte in Verarbeitungsoptionen (z. B. DocumentDuplex, DocumentNUp) integriert werden, wie durch die angegebene Option angegeben.</span><span class="sxs-lookup"><span data-stu-id="80697-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="80697-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="80697-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="80697-112">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="80697-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="80697-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="80697-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="80697-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="80697-114">Element Information</span></span>



| <span data-ttu-id="80697-115">Name</span><span class="sxs-lookup"><span data-stu-id="80697-115">Name</span></span> | <span data-ttu-id="80697-116">Wert</span><span class="sxs-lookup"><span data-stu-id="80697-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80697-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="80697-117">Element Type</span></span> <br/>   | <span data-ttu-id="80697-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="80697-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="80697-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="80697-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="80697-120">Dokument</span><span class="sxs-lookup"><span data-stu-id="80697-120">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="80697-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80697-121">Notes</span></span> <br/>          | <span data-ttu-id="80697-122">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="80697-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="80697-123">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="80697-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="80697-124">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="80697-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="80697-125">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="80697-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="80697-126">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="80697-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="80697-127">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="80697-127">Structural Content</span></span>

<span data-ttu-id="80697-128">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="80697-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!--Specifies the XPS specific part name for the back cover sheet-->
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="80697-129">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="80697-129">Structure Variables</span></span>

<span data-ttu-id="80697-130">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="80697-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="80697-131">Name</span><span class="sxs-lookup"><span data-stu-id="80697-131">Name</span></span>                               | <span data-ttu-id="80697-132">Datentyp</span><span class="sxs-lookup"><span data-stu-id="80697-132">Data type</span></span>         | <span data-ttu-id="80697-133">Einheit</span><span class="sxs-lookup"><span data-stu-id="80697-133">Unit</span></span>                  | <span data-ttu-id="80697-134">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="80697-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="80697-135">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="80697-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="80697-136">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="80697-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="80697-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="80697-137">string</span></span><br/> | <span data-ttu-id="80697-138">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="80697-138">characters</span></span><br/> | <span data-ttu-id="80697-139">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="80697-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="80697-140">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="80697-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="80697-141">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="80697-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="80697-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="80697-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="80697-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="80697-143">string</span></span><br/> | <span data-ttu-id="80697-144">–</span><span class="sxs-lookup"><span data-stu-id="80697-144">n/a</span></span><br/>        | <span data-ttu-id="80697-145">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="80697-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="80697-146">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="80697-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="80697-147">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="80697-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="80697-148">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="80697-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="80697-149">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="80697-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" may be printed on either sides 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="80697-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80697-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80697-151">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="80697-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




