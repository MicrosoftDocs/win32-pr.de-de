---
description: Erfahren Sie mehr über das JobPrimaryBannerSheet-Element, das das Bannerblatt beschreibt, das für den Auftrag ausgegeben werden soll.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39922f65d71ea0cc6d6de6103bc159f79467038f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408753"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="0b947-103">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="0b947-103">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="0b947-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0b947-104">This topic is not current.</span></span> <span data-ttu-id="0b947-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="0b947-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0b947-106">Beschreibt das Bannerblatt, das für den Auftrag ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b947-106">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="0b947-107">Das Bannerblatt sollte in der Standardeinstellung PageMediaSize und unter Verwendung des Standardmäßigen PageMediaType ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0b947-107">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="0b947-108">Das Bannerblatt sollte vom Rest des Auftrags isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="0b947-108">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="0b947-109">Dies bedeutet, dass alle End- oder Verarbeitungsoptionen (z. B. JobDuplexAllDocumentsContiguously, JobStapleAllDocuments oder JobBindAllDocuments) das Bannerblatt nicht enthalten sollten.</span><span class="sxs-lookup"><span data-stu-id="0b947-109">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="0b947-110">Das Bannerblatt sollte als erstes Blatt des Auftrags auftreten.</span><span class="sxs-lookup"><span data-stu-id="0b947-110">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="0b947-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0b947-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0b947-112">Strukturell</span><span class="sxs-lookup"><span data-stu-id="0b947-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0b947-113">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="0b947-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0b947-114">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0b947-114">Element Information</span></span>



| <span data-ttu-id="0b947-115">Name</span><span class="sxs-lookup"><span data-stu-id="0b947-115">Name</span></span> | <span data-ttu-id="0b947-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0b947-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b947-117">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0b947-117">Element Type</span></span> <br/>   | <span data-ttu-id="0b947-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="0b947-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="0b947-119">Bereichspräfix</span><span class="sxs-lookup"><span data-stu-id="0b947-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0b947-120">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0b947-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0b947-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b947-121">Notes</span></span> <br/>          | <span data-ttu-id="0b947-122">XPS-kompatible Consumer MÜSSEN erzwingen, dass ein URI-Verweis auf eine Ressource, z. B. ein Bild oder Farbprofil, entweder in einem Dokument mit Druckfunktionen oder printTicket auf einen Teilnamen (einen relativen URI zum Paketstamm) innerhalb desselben XPS-Dokumentpakets verweisen muss, das das resultierende PrintTicket enthält.</span><span class="sxs-lookup"><span data-stu-id="0b947-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="0b947-123">Ein kompatibler XPS-Consumer DARF KEINEN URI verwenden, der nicht mit der Partnamenssyntax kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="0b947-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="0b947-124">Diese Einstellungen sind XPS-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="0b947-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="0b947-125">URIs, auf die in einem Dokument mit Druckfunktionen oder in PrintTicket verwiesen wird, DÜRFEN NICHT als URLs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="0b947-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="0b947-126">Dies ist unsicher, da sie möglicherweise nicht wie beabsichtigt aufgelöst werden und schädliche Sicherheitsrisiken für Treiber und Betriebssystem darstellen können.</span><span class="sxs-lookup"><span data-stu-id="0b947-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0b947-127">Strukturell</span><span class="sxs-lookup"><span data-stu-id="0b947-127">Structural Content</span></span>

<span data-ttu-id="0b947-128">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="0b947-128">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0b947-129">Strukturvariablen</span><span class="sxs-lookup"><span data-stu-id="0b947-129">Structure Variables</span></span>

<span data-ttu-id="0b947-130">In der folgenden Tabelle werden die Merkmale der in der XML-Struktur definierten Variablen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0b947-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0b947-131">Name</span><span class="sxs-lookup"><span data-stu-id="0b947-131">Name</span></span>                               | <span data-ttu-id="0b947-132">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0b947-132">Data type</span></span>         | <span data-ttu-id="0b947-133">Einheit</span><span class="sxs-lookup"><span data-stu-id="0b947-133">Unit</span></span>                  | <span data-ttu-id="0b947-134">Unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="0b947-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0b947-135">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0b947-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0b947-136">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="0b947-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0b947-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0b947-137">string</span></span><br/> | <span data-ttu-id="0b947-138">Buchstaben</span><span class="sxs-lookup"><span data-stu-id="0b947-138">characters</span></span><br/> | <span data-ttu-id="0b947-139">Gültiger vollqualifizierte Name, wie von [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/)definiert.</span><span class="sxs-lookup"><span data-stu-id="0b947-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0b947-140">Wenn kein Namespace angegeben ist, wird der Standardnamespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="0b947-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0b947-141">Der Name der Option.</span><span class="sxs-lookup"><span data-stu-id="0b947-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0b947-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0b947-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0b947-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0b947-143">string</span></span><br/> | <span data-ttu-id="0b947-144">–</span><span class="sxs-lookup"><span data-stu-id="0b947-144">n/a</span></span><br/>        | <span data-ttu-id="0b947-145">TRUE, FALSE</span><span class="sxs-lookup"><span data-stu-id="0b947-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0b947-146">Definiert eine Option, die diese Funktion deaktiviert, wenn sie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0b947-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0b947-147">xml-Inhalt (Extensible Markup Language)</span><span class="sxs-lookup"><span data-stu-id="0b947-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0b947-148">Die Schlüsselwörter für das öffentliche Druckschema werden im https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords -Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="0b947-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0b947-149">Der Inhalt des öffentlichen Extensible Markup Language (XML) für dieses Schlüsselwort ist unten definiert:</span><span class="sxs-lookup"><span data-stu-id="0b947-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0b947-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b947-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b947-151">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="0b947-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




