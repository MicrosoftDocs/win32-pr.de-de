---
description: Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ef61001e45178989d6f89e17d8cc38b82c1354
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996307"
---
# <a name="documentbannersheet"></a><span data-ttu-id="9da70-104">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="9da70-104">DocumentBannerSheet</span></span>

<span data-ttu-id="9da70-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9da70-105">This topic is not current.</span></span> <span data-ttu-id="9da70-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="9da70-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9da70-107">Beschreibt das Bannerblatt, das für ein bestimmtes Dokument ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9da70-107">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="9da70-108">Das Bannerblatt sollte unter Verwendung des Standardmäßigen PageMediaType auf der Standardseite "PageMediaSize" ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9da70-108">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="9da70-109">Das Bannerblatt sollte auch vom Rest des Dokuments isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="9da70-109">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="9da70-110">Dies bedeutet, dass alle Optionen zum Beenden oder Verarbeiten von Dokumenten (z. B. DocumentDuplex, DocumentStaple oder DocumentBinding) das Bannerblatt nicht enthalten sollten.</span><span class="sxs-lookup"><span data-stu-id="9da70-110">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="9da70-111">Das Bannerblatt kann vom Rest des Auftrags isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="9da70-111">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="9da70-112">Dies bedeutet, dass alle Optionen zum Beenden oder Verarbeiten von Aufgaben das Dokumentbannerblatt enthalten können.</span><span class="sxs-lookup"><span data-stu-id="9da70-112">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="9da70-113">Das Bannerblatt sollte als erstes Blatt des Dokuments angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9da70-113">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="9da70-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9da70-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9da70-115">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="9da70-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="9da70-116">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9da70-116">Element Information</span></span>



| <span data-ttu-id="9da70-117">Name</span><span class="sxs-lookup"><span data-stu-id="9da70-117">Name</span></span> | <span data-ttu-id="9da70-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9da70-118">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da70-119">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="9da70-119">Element Type</span></span> <br/>   | <span data-ttu-id="9da70-120">Funktion</span><span class="sxs-lookup"><span data-stu-id="9da70-120">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9da70-121">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="9da70-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9da70-122">Dokument</span><span class="sxs-lookup"><span data-stu-id="9da70-122">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9da70-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9da70-123">Notes</span></span> <br/>          | <span data-ttu-id="9da70-124">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="9da70-124">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="9da70-125">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="9da70-125">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="9da70-126">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="9da70-126">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="9da70-127">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="9da70-127">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="9da70-128">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="9da70-128">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="9da70-129">Strukturell</span><span class="sxs-lookup"><span data-stu-id="9da70-129">Structural Content</span></span>

<span data-ttu-id="9da70-130">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="9da70-130">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="9da70-131">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="9da70-131">Structure Variables</span></span>

<span data-ttu-id="9da70-132">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9da70-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9da70-133">Name</span><span class="sxs-lookup"><span data-stu-id="9da70-133">Name</span></span>                               | <span data-ttu-id="9da70-134">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9da70-134">Data type</span></span>         | <span data-ttu-id="9da70-135">Einheit</span><span class="sxs-lookup"><span data-stu-id="9da70-135">Unit</span></span>                   | <span data-ttu-id="9da70-136">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="9da70-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9da70-137">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9da70-137">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9da70-138">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="9da70-138">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9da70-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9da70-139">string</span></span><br/> | <span data-ttu-id="9da70-140">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="9da70-140">characters</span></span> <br/> | <span data-ttu-id="9da70-141">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="9da70-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9da70-142">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="9da70-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9da70-143">Der Name der Option</span><span class="sxs-lookup"><span data-stu-id="9da70-143">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="9da70-144">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9da70-144">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9da70-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9da70-145">string</span></span><br/> | <span data-ttu-id="9da70-146">–</span><span class="sxs-lookup"><span data-stu-id="9da70-146">n/a</span></span><br/>         | <span data-ttu-id="9da70-147">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="9da70-147">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="9da70-148">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9da70-148">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9da70-149">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="9da70-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9da70-150">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="9da70-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9da70-151">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="9da70-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="9da70-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9da70-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9da70-153">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="9da70-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




