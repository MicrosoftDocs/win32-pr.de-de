---
description: Erfahren Sie mehr über das vom Benutzer konfigurierbare DocumentBannerSheet-Element. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce05ffae190835e4a8b4082c634b34e26103ab
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548768"
---
# <a name="documentbannersheet"></a><span data-ttu-id="87d38-105">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="87d38-105">DocumentBannerSheet</span></span>

<span data-ttu-id="87d38-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="87d38-106">This topic is not current.</span></span> <span data-ttu-id="87d38-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="87d38-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="87d38-108">Beschreibt das Bannerblatt, das für ein bestimmtes Dokument ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="87d38-108">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="87d38-109">Das Bannerblatt sollte unter Verwendung des Standardmäßigen PageMediaType auf der Standardseite "PageMediaSize" ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="87d38-109">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="87d38-110">Das Bannerblatt sollte auch vom Rest des Dokuments isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="87d38-110">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="87d38-111">Dies bedeutet, dass alle Optionen zum Beenden oder Verarbeiten von Dokumenten (z. B. DocumentDuplex, DocumentStaple oder DocumentBinding) das Bannerblatt nicht enthalten sollten.</span><span class="sxs-lookup"><span data-stu-id="87d38-111">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="87d38-112">Das Bannerblatt kann vom Rest des Auftrags isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="87d38-112">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="87d38-113">Dies bedeutet, dass alle Optionen zum Beenden oder Verarbeiten von Aufgaben das Dokumentbannerblatt enthalten können.</span><span class="sxs-lookup"><span data-stu-id="87d38-113">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="87d38-114">Das Bannerblatt sollte als erstes Blatt des Dokuments angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="87d38-114">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="87d38-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="87d38-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="87d38-116">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="87d38-116">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="87d38-117">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="87d38-117">Element Information</span></span>



| <span data-ttu-id="87d38-118">Name</span><span class="sxs-lookup"><span data-stu-id="87d38-118">Name</span></span> | <span data-ttu-id="87d38-119">Wert</span><span class="sxs-lookup"><span data-stu-id="87d38-119">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d38-120">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="87d38-120">Element Type</span></span> <br/>   | <span data-ttu-id="87d38-121">Funktion</span><span class="sxs-lookup"><span data-stu-id="87d38-121">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="87d38-122">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="87d38-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="87d38-123">Dokument</span><span class="sxs-lookup"><span data-stu-id="87d38-123">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="87d38-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="87d38-124">Notes</span></span> <br/>          | <span data-ttu-id="87d38-125">XPS-kompatible Benutzer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Druckfunktionendokument oder printTicket auf einen Teilenamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="87d38-125">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="87d38-126">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="87d38-126">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="87d38-127">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="87d38-127">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="87d38-128">URIs, auf die entweder in einem Druckfunktionendokument oder printTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="87d38-128">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="87d38-129">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt gelöst werden und zu schädlichen Sicherheitsrisiken für treiber und betriebssystem könnten.</span><span class="sxs-lookup"><span data-stu-id="87d38-129">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="87d38-130">Strukturelle Inhalte</span><span class="sxs-lookup"><span data-stu-id="87d38-130">Structural Content</span></span>

<span data-ttu-id="87d38-131">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="87d38-131">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="87d38-132">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="87d38-132">Structure Variables</span></span>

<span data-ttu-id="87d38-133">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="87d38-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="87d38-134">Name</span><span class="sxs-lookup"><span data-stu-id="87d38-134">Name</span></span>                               | <span data-ttu-id="87d38-135">Datentyp</span><span class="sxs-lookup"><span data-stu-id="87d38-135">Data type</span></span>         | <span data-ttu-id="87d38-136">Einheit</span><span class="sxs-lookup"><span data-stu-id="87d38-136">Unit</span></span>                   | <span data-ttu-id="87d38-137">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="87d38-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="87d38-138">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="87d38-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="87d38-139">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="87d38-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="87d38-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="87d38-140">string</span></span><br/> | <span data-ttu-id="87d38-141">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="87d38-141">characters</span></span> <br/> | <span data-ttu-id="87d38-142">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="87d38-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="87d38-143">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="87d38-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="87d38-144">Der Name der Option</span><span class="sxs-lookup"><span data-stu-id="87d38-144">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="87d38-145">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="87d38-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="87d38-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="87d38-146">string</span></span><br/> | <span data-ttu-id="87d38-147">n/v</span><span class="sxs-lookup"><span data-stu-id="87d38-147">n/a</span></span><br/>         | <span data-ttu-id="87d38-148">True, False</span><span class="sxs-lookup"><span data-stu-id="87d38-148">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="87d38-149">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="87d38-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="87d38-150">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="87d38-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="87d38-151">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="87d38-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="87d38-152">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="87d38-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="87d38-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="87d38-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87d38-154">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="87d38-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




