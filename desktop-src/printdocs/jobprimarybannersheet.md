---
description: Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c438cd0f33bc7b3a80fc3e654e0d64831e3b6777
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996927"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="e501e-104">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="e501e-104">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="e501e-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e501e-105">This topic is not current.</span></span> <span data-ttu-id="e501e-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="e501e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e501e-107">Beschreibt das Bannerblatt, das für den Auftrag ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e501e-107">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="e501e-108">Das Bannerblatt sollte in der Standardeinstellung PageMediaSize und unter Verwendung des Standardmäßigen PageMediaType ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e501e-108">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="e501e-109">Das Bannerblatt sollte vom Rest des Auftrags isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="e501e-109">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="e501e-110">Dies bedeutet, dass alle End- oder Verarbeitungsoptionen (z. B. JobDuplexAllDocumentsContiguously, JobStapleAllDocuments oder JobBindAllDocuments) das Bannerblatt nicht enthalten sollten.</span><span class="sxs-lookup"><span data-stu-id="e501e-110">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="e501e-111">Das Bannerblatt sollte als erstes Blatt des Auftrags auftreten.</span><span class="sxs-lookup"><span data-stu-id="e501e-111">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="e501e-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e501e-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e501e-113">Strukturell</span><span class="sxs-lookup"><span data-stu-id="e501e-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e501e-114">Extensible Markup Language -Inhalt (XML)</span><span class="sxs-lookup"><span data-stu-id="e501e-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e501e-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e501e-115">Element Information</span></span>



| <span data-ttu-id="e501e-116">Name</span><span class="sxs-lookup"><span data-stu-id="e501e-116">Name</span></span> | <span data-ttu-id="e501e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e501e-117">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e501e-118">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="e501e-118">Element Type</span></span> <br/>   | <span data-ttu-id="e501e-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="e501e-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e501e-120">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="e501e-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e501e-121">Auftrag</span><span class="sxs-lookup"><span data-stu-id="e501e-121">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="e501e-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e501e-122">Notes</span></span> <br/>          | <span data-ttu-id="e501e-123">XPS-kompatible Consumer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Dokument mit Druckfunktionen oder printTicket auf einen Teilnamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="e501e-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="e501e-124">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="e501e-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="e501e-125">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="e501e-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="e501e-126">URIs, auf die in einem Dokument mit Druckfunktionen oder in PrintTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="e501e-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="e501e-127">Dies ist unsicher, da sie möglicherweise nicht wie vorgesehen aufgelöst werden und schädliche Sicherheitsrisiken für Treiber und Betriebssystem darstellen können.</span><span class="sxs-lookup"><span data-stu-id="e501e-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e501e-128">Strukturell</span><span class="sxs-lookup"><span data-stu-id="e501e-128">Structural Content</span></span>

<span data-ttu-id="e501e-129">Die XML-Struktur dieses Elements ist:</span><span class="sxs-lookup"><span data-stu-id="e501e-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the banner sheet. -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="e501e-130">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="e501e-130">Structure Variables</span></span>

<span data-ttu-id="e501e-131">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e501e-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e501e-132">Name</span><span class="sxs-lookup"><span data-stu-id="e501e-132">Name</span></span>                               | <span data-ttu-id="e501e-133">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e501e-133">Data type</span></span>         | <span data-ttu-id="e501e-134">Einheit</span><span class="sxs-lookup"><span data-stu-id="e501e-134">Unit</span></span>                  | <span data-ttu-id="e501e-135">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="e501e-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e501e-136">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e501e-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e501e-137">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="e501e-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e501e-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e501e-138">string</span></span><br/> | <span data-ttu-id="e501e-139">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e501e-139">characters</span></span><br/> | <span data-ttu-id="e501e-140">Gültiger vollqualifizierter Name, wie durch [Namespaces in XML definiert.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="e501e-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e501e-141">Wenn kein Namespace angegeben wird, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="e501e-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e501e-142">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="e501e-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e501e-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e501e-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e501e-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e501e-144">string</span></span><br/> | <span data-ttu-id="e501e-145">–</span><span class="sxs-lookup"><span data-stu-id="e501e-145">n/a</span></span><br/>        | <span data-ttu-id="e501e-146">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="e501e-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e501e-147">Definiert eine Option, durch die diese Funktion deaktiviert wird, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e501e-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e501e-148">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e501e-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e501e-149">Die Schlüsselwörter des öffentlichen Druckschemas werden im -Namespace https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords definiert.</span><span class="sxs-lookup"><span data-stu-id="e501e-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e501e-150">Der öffentliche Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="e501e-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a JobPrimaryBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored.  -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="e501e-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e501e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e501e-152">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="e501e-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




